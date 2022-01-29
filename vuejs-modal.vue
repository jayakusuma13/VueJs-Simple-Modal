<!-- Use preprocessors via the lang attribute! e.g. <template lang="pug"> -->
<template>
  <div>
        <button type="submit" class="btn btn-primary" @click="showModal">Show Modal</button>

        <div class="fixed inset-0 w-full h-full z-20 bg-black bg-opacity-50 duration-300 overflow-y-auto" v-show="showModalVisible">
            <div class="relative sm:w-3/4 md:w-1/2 lg:w-1/3 mx-2 sm:mx-auto my-10 opacity-100">
                <div class="relative bg-white shadow-lg rounded-lg text-gray-900 z-20">
                    <div class="mx-auto">Test New Modal</div>
                        <div class="flex justify-center bg-transparent">
                            <button class="bg-green-600 font-semibold text-white py-3 w-full rounded-bl-md hover:bg-green-700 focus:outline-none focus:ring shadow-lg hover:shadow-none transition-all duration-300" type="submit">
                                Import 
                            </button>
                            <button class="bg-green-600 font-semibold text-white py-3 w-full rounded-bl-md hover:bg-green-700 focus:outline-none focus:ring shadow-lg hover:shadow-none transition-all duration-300" @click="activateSecondModal()">
                                Next 
                            </button>
                            <button class="bg-red-600 font-semibold text-white py-3 w-full rounded-br-md hover:bg-red-700 focus:outline-none focus:ring shadow-lg hover:shadow-none transition-all duration-300" @click="showModalVisible = false">
                                Close
                            </button>
                        </div>
                </div>
            </div>
        </div>

        <div class="fixed inset-0 w-full h-full z-70 bg-black bg-opacity-50 duration-300 overflow-y-auto" v-show="showModal2">
            <div class="relative sm:w-3/4 md:w-1/2 lg:w-1/3 mx-2 sm:mx-auto my-10 opacity-100">
                <div class="relative bg-white shadow-lg rounded-lg text-gray-900 z-20">
                    <div class="mx-auto">Test New Modal</div>
                        <div class="flex justify-center bg-transparent">
                            <button class="bg-green-600 font-semibold text-white py-3 w-full rounded-bl-md hover:bg-green-700 focus:outline-none focus:ring shadow-lg hover:shadow-none transition-all duration-300" type="submit">
                                Import 
                            </button>
                            <button class="bg-red-600 font-semibold text-white py-3 w-full rounded-br-md hover:bg-red-700 focus:outline-none focus:ring shadow-lg hover:shadow-none transition-all duration-300" @click="activateSecondModal()">
                                Close
                            </button>
                        </div>
                </div>
            </div>
        </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showModalVisible: false,
      showModal2: false
    };
  },
  methods: {
    doSomething() {
      alert('Hello!');
    },
    
    showModal(){
      this.showModalVisible = true;
    },
    
    activateSecondModal(){
      if(this.showModalVisible){
        this.showModal2 = true
        this.showModalVisible = false
      } else {
        this.showModalVisible = true
        this.showModal2 = false
      }
    },
  }
};
</script>

<!-- Use preprocessors via the lang attribute! e.g. <style lang="scss"> -->
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

a,
button {
  color: #4fc08d;
}

button {
  background: none;
  border: solid 1px;
  border-radius: 2em;
  font: inherit;
  padding: 0.75em 2em;
}
</style>