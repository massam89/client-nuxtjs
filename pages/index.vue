<template>
  <div>
     <div class="container">
    <Hero/>
    <div class="this">
      <LargeCardDisplay v-for="cardInfo in largeCardInfo" :key="cardInfo.id" :cardsSection="cardInfo" />
    </div>

    <div class="this">
      <SmallCardDisplay v-for="cardInfo in smallCardSections" :key="cardInfo.id" :cardsSection="cardInfo" />
    </div>


    
  </div>
  </div>
 
</template>

<script>
import { largeCardSections, smallCardSections } from '@/assets/data'

export default {
  data() {
    return {
      largeCardInfo: largeCardSections,
      smallCardSections: smallCardSections
    }
  }
}
</script>

<style scoped>
 .this {
   margin-top:200px;
 }
</style>
