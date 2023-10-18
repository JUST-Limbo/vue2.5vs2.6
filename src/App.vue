<template>
    <div id="app">
        <div class="wrapper">
            <div class="d1" @mouseover="d1MouseOver" @mouseout="d1MouseOut()"></div>
            <div class="d2" v-if="d2Visible" @mouseover="d2MouseOver" @mouseout="d2MouseOut"></div>
        </div>
    </div>
</template>
<script>
export default {
    name: 'AppRoot',
    data() {
        return {
            d2Visible: false,
        };
    },
    methods: {
        d1MouseOver() {
            console.log('d1MouseOver')
            this.d2Visible = true;
        },
        d1MouseOut() {
            debugger
            console.log('d1MouseOut')
            this.d2Visible = false;
        },
        d2MouseOver() {
            debugger
            console.log('d2MouseOver')
            this.d2Visible = true;
        },
        d2MouseOut() {
            console.log('d2MouseOut')
            this.d2Visible = false;
        },
    },
};
</script>

<style lang="scss">
.wrapper {
    position: relative;
}
.d1 {
    width: 100px;
    height: 200px;
    background: goldenrod;
}
.d2 {
    width: 300px;
    height: 200px;
    background: red;
}
</style>
