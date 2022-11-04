<template>
    <div class="playground">
        <GameMap/>
    </div>
</template>

<script>

import { useStore } from 'vuex';
import GameMap from './GameMap.vue';
import { onMounted } from 'vue';

export default {
    components: {
        GameMap,
    },
    
    setup() {
        const store = useStore();
        onMounted(() => {
            store.state.pk.gameObject.start();
        })
    }
}

</script>

<style scoped>

div.playground {
    width: 60vw;
    height: 70vh;
    margin: 50px auto;
}

</style>