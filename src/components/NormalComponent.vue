<script setup lang='ts'>
import { ref } from 'vue'
import AnimatedBeam from '../components/AnimatedBeam.vue'
import Circle from '../components/Circle.vue'

const containerRef = ref<HTMLDivElement>()
const div1Ref = ref<HTMLElement>()
const div2Ref = ref()
</script>

<template>
    <div class="flex flex-col space-y-3">
        <h1 class="font-medium text-lg">Normal Component ( Without the reverse prop )</h1>
        <div ref="containerRef"
            class="relative flex w-full max-w-[500px] items-center justify-center overflow-hidden rounded-lg border bg-background p-10 md:shadow-xl">
            <div class="flex size-full flex-col items-stretch justify-between gap-10">
                <div class="flex flex-row justify-between">
                    <Circle ref="div1Ref">
                        <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 128 128">
                            <path fill="none"
                                d="m0 8.934l49.854.158l14.167 24.47l14.432-24.47L128 8.935l-63.834 110.14zm126.98.637l-24.36.02l-38.476 66.053L25.691 9.592L.942 9.572l63.211 107.89zm-25.149-.008l-22.745.168l-15.053 24.647L49.216 9.73l-22.794-.168l37.731 64.476zm-75.834-.17l23.002.009m-23.002-.01l23.002.01" />
                            <path fill="#35495e"
                                d="m25.997 9.393l23.002.009L64.035 34.36L79.018 9.404L102 9.398L64.15 75.053z" />
                            <path fill="#41b883"
                                d="m.91 9.569l25.067-.172l38.15 65.659L101.98 9.401l25.11.026l-62.966 108.06z" />
                        </svg>
                    </Circle>
                    <Circle ref="div2Ref">
                        <svg xmlns="http://www.w3.org/2000/svg" width="48.77" height="32" viewBox="0 0 256 168">
                            <path fill="#00DC82"
                                d="M143.618 167.029h95.166c3.023 0 5.992-.771 8.61-2.237a16.96 16.96 0 0 0 6.302-6.115a16.3 16.3 0 0 0 2.304-8.352c0-2.932-.799-5.811-2.312-8.35L189.778 34.6a16.97 16.97 0 0 0-6.301-6.113a17.6 17.6 0 0 0-8.608-2.238c-3.023 0-5.991.772-8.609 2.238a16.96 16.96 0 0 0-6.3 6.113l-16.342 27.473l-31.95-53.724a17 17 0 0 0-6.304-6.112A17.64 17.64 0 0 0 96.754 0c-3.022 0-5.992.772-8.61 2.237a17 17 0 0 0-6.303 6.112L2.31 141.975a16.3 16.3 0 0 0-2.31 8.35c0 2.932.793 5.813 2.304 8.352a16.96 16.96 0 0 0 6.302 6.115a17.6 17.6 0 0 0 8.61 2.237h59.737c23.669 0 41.123-10.084 53.134-29.758l29.159-48.983l15.618-26.215l46.874 78.742h-62.492zm-67.64-26.24l-41.688-.01L96.782 35.796l31.181 52.492l-20.877 35.084c-7.976 12.765-17.037 17.416-31.107 17.416" />
                        </svg>
                    </Circle>
                </div>
            </div>
            <AnimatedBeam :duration="3" :container-ref="containerRef" :from-ref="div1Ref" :to-ref="div2Ref" />
        </div>
    </div>
</template>