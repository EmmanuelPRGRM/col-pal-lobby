<template>
    <v-container fill-height fluid black class="container">
    <v-overlay
            absolute
            z-index="0"
            opacity="1"
        >
            <v-img 
                :src="bgDark"
                :style="{opacity:1, width:'100vw', height: '100vh'}"></v-img>
        </v-overlay>
            <div :style="{
                position: 'absolute',
                width:'100%',
                height:'100%'
                }">
                <div
                    class="ma-auto parent"
                    :style="{
                        height: '100%',
                        width: '100%',
                        maxHeight:'56vw',
                        maxWidth:'178vh',
                        backgroundImage: `url(${bg})`,
                        backgroundSize: 'contain',
                        backgroundPosition: 'center',
                        zIndex:2,
                        position:'absolute',
                        top:0,
                        left:0,
                        bottom:0,
                        right:0,
                    }"
                >
                <!-- contents here-->
                <v-img 
                    class="blue-border"
                    src="@/assets/blue-border-gameon.png"
                    :style="{width:'70%', height:'70%', top:'13%'}">
                </v-img>
                <div style="margin-top: 8%; margin-left:7%">
                  <v-img
                    :src="item.url"
                    class="cursor-pulse"
                    v-for="(item, key) of clickables"
                    :key="key"
                    :style="{
                        position:'relative',
                        top: item.y,
                        left: item.x,
                        width: item.width,
                        height: item.height,
                    }"
                    ></v-img>
                </div>
                </div>
            </div>
</v-container>
</template>

<script>
export default {

      data: () => ({
         bgDark: require('@/assets/lobby-bg-2.png'),
         bg:require('@/assets/lobby-bg.png'),
         clickables: [
            {
                name: 'photobooth-btn',
                url: require('@/assets/photobooth-btn.png'),
                x: '0%',
                y: '15%',
                width:'15%',
                height: '8%'
            },
            {
                name: 'vlounge-btn',
                url: require('@/assets/vlounge-btn.png'),
                x: '0%',
                y: '15%',
                width:'15%',
                height: '8%'
            },
            {
                name: 'game-btn',
                url: require('@/assets/game-btn.png'),
                x: '0%',
                y: '15%',
                width:'15%',
                height: '8%'
            },
            {
                name: 'leaderboard-btn',
                url: require('@/assets/leaderboard-btn.png'),
                x: '0%',
                y: '15%',
                width:'15%',
                height: '8%'
            },
         ]
      })
    
}
</script>

<style scoped>
.blue-border
{
    z-index: 20;
}

.cursor-pulse
{
    display: inline-block;
    cursor: pointer;
}

</style>