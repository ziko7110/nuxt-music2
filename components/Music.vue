<template>
    <main class="main">
        <button 
            class="musicBtn"
            @click="musicStart"
        >
            ミュージック
        </button>
        
        <button 
            class="startBtn"
            @click="appStart"
            v-if="isStarted==false">
            スタート
        </button>
        <section
            class="touchZone"
            v-else>
            &nbsp;
        </section>
    </main>
</template>

<script>
import * as Tone from 'tone'
export default {
    data(){
        return {
            isStarted: false
        }
    },
    methods: {
        appStart(){
            this.isStarted = true
        },
        musicStart(){
            var synth = new Tone.Synth().toMaster()
            synth.triggerAttackRelease('C4', '8n')
        }
    }
}
</script>

<style>
.startBtn,
.musicBtn{
    padding: 10px 20px;
}
</style>