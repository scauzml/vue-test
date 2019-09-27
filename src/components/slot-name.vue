<template>
    <div class="container">
        <header>
            <!-- 我们希望把页头放这里 -->
            <slot name="header"></slot>
        </header>
        <main>
            <!-- 我们希望把主要内容放这里 -->
            <slot v-bind:user="user">
                {{user.lastName}}
            </slot>
        </main>
        <footer>
            <!-- 我们希望把页脚放这里 -->
            <slot name="footer" >

            </slot>
        </footer>

    </div>
</template>

<script>

    export default {
        name: 'a',
        components: {

        },
        data(){
            return{
            user:{
                firstName:'first',
                lastName:'last'
            }
            }
        }
    }
</script>

<style>

</style>
