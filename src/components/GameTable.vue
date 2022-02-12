<template>
    <div>
        <p class="count" v-if="count == 15">Вы победили!</p>
        <transition-group name="flip-list" class="table" tag="div">
            <div v-for="item in items" :key="item.id"  @click="flipCard(item)" class="memory-card" :class="{'flip': item.status}">
                <img class="front-face" :src="item.url"/>
                <img class="back-face" :src="item.card"/>
            </div>
        </transition-group>
    </div>
</template>

<script>
import _shuffle from "lodash.shuffle";
export default {
    props: {
        list: {
            type: Array,
            required: true
        }
    },
    data(){
        return{
            items: this.list,
            count: 0,
            firstCard: Object,
            lastCard: Object,
            hasFlipCard: false
        }
    },
    methods: {
        flipCard(item){
            if(this.hasFlipCard == false){
                item.status = true
                this.firstCard = item
                return this.hasFlipCard = true
            }if(this.hasFlipCard == true){
                 item.status = true
                 this.lastCard = item
                 this.tr()
            }else{
                item.status = false
            }
        },
        
        tr(){
            console.log(this.firstCard.number)
            console.log(this.lastCard.number)
            if(this.firstCard.number == this.lastCard.number){
                console.log("правильно")
                this.hasFlipCard = false
                this.firstCard = {}
                this.lastCard = {}
                this.count ++

            }else{
                this.hasFlipCard = false
                setTimeout(() => {
                    this.firstCard.status = false
                    this.lastCard.status = false
                    this.firstCard = {}
                    this.lastCard = {}
                },1500)
               console.log("неправильно")
            }
        },
        qw(){
            this.items.forEach(function (item) {
                item.status = false
                
            })
        }
    },
    
    mounted(){
        this.items = _shuffle(this.items);
        setTimeout(() => {
            this.qw()
        },3000)
    },
    

    
}
</script>

<style lang="scss" scoped>
.table{
    width: 1420px;
    padding: 6em 0;
    margin: 0 auto;
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    grid-column-gap: 30px;
    grid-row-gap: 2em;
    perspective: 1000px;

}

.flip-list-move {
  transition: transform 1s;
}
.memory-card{
   width: 100%;
   height: 350px;
  margin: 5px;
  position: relative;
  box-shadow: 1px 1px 1px rgba(0,0,0,.3);
  transform: scale(1);
  transform-style: preserve-3d;
  transition: transform .5s;
  &:active{
      transform: scale(0.97);
      transition: transform .2s;
  }
}
.memory-card.flip{
    transform: rotateY(180deg);
}
.back-face{
    top: 0;
    left: 0;
width: 100%;
  height: 100%;
  position: absolute;
  padding: 20px;
  border-radius: 5px;
  background: #1C7CCC;
  backface-visibility: hidden;
}
.front-face{
 width: 100%;
  height: 100%;
  padding: 20px;
  border-radius: 5px;
  background: #1C7CCC;
}
.count{
    font-size: 30px;
    color: rgb(255, 0, 0);
    font-weight: 600;
}
</style>