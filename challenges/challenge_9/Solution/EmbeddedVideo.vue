<template>
    <iframe
        :width="width"
        :height="height"
        :src="url"
        frameborder="0"
        allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
        allowfullscreen
    ></iframe>
</template>

<script>
    export default {
        name: "EmbeddedVideo",
        props: {
            url: {
                type: String,
                required: true,
                validator(value) {
                    return value.includes("youtube");
                }
            },
            height: {
                type: Number,
                default: 225
            },
            width: {
                type: Number,
                default: 400
            }
        }
    };
</script>

<style lang="scss" scoped>
</style>