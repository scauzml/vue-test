<template>
    <div id="app">
        <aslot>
            slot{{username}}
        </aslot>
        <submit>
            save
        </submit>
        <slotName>
            <template #header>
                header
            </template>
            <template v-slot="{user}">
                {{user.firstName}}
            </template>
            <template v-slot:footer>
                hi
            </template>
        </slotName>
    </div>
</template>

<script>
    import aslot from './components/a'
    import submit from './components/SubmitButton'
    import slotName from './components/slot-name'

    export default {
        name: 'app',
        components: {
            aslot,
            submit,
            slotName
        },
        data() {
            return {
                username: 'li'
            }
        }
    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
</style>
