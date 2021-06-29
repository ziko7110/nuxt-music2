<template>
    <no-ssr>
        <Music />
    </no-ssr>
</template>

<script>
import Music from '~/components/Music'

export default {
    components: {
        Music
    }
}
</script>

<style>
.main{
    width: 100%;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
}

.startBtn{
    padding: 10px 20px;
}

.touchZone{
    background: linear-gradient( 45deg, rgb(255,255,255),rgb(100,255,255) );
    width: 100%;
    min-width: 100%;
    height: 100vh;
    min-height: 100vh;
}
</style>