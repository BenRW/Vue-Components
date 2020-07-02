<template>
    <div id="quiver-plot-vue">
        <svg height=300 width=600>
            <image v-for="item in items" :key="item.xcoord" :x="item.xcoord" :y="item.ycoord" :style="item.style" xlink:href="./assets/basic_arrow.svg" />
        </svg>
    </div>
</template>


<script>
export default {
    name: 'quiver-plot-vue',
    data (){
        return {
            items: [
                {xcoord: 0,
                 ycoord: 0,
                 style: "transform:Scale(0.2)"},
                {xcoord: 5*100,
                 ycoord: 5*50, 
                 style: "transform:Scale(0.2)"},
                 {xcoord: 5*200,
                 ycoord: 5*50, 
                 style: "transform:Scale(0.2)"}
            ],
        }
    },
}
</script>


<style>
svg {
    outline: 5px solid black;
}
</style>