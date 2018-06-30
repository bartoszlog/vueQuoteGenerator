<template>
    <div>
        <h3>Quote!</h3>
        <button class="btn btn-primary" @click.prevent="addQuote">Add Quote!</button>
        <div>
            <textarea v-model="quote" cols="30" rows="10"></textarea>
        </div>        
    </div>
</template>


<script>
    export default {
        data() {
            return {
                quote: ''
            }
        },
        methods: {
            addQuote() {
                this.$emit('quoteAdded', this.quote)
                this.quote = ''
            }
        }
    }
</script>

<style scoped>

</style>
