<template>
    <div class="container">
        <app-new-quote @quoteAdded="newQuote"></app-new-quote>
        <app-quote-grid @quoteDeleted="deleteQuote" :quotes="quotes"></app-quote-grid>
    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid.vue'
    import NewQuote from './components/NewQuote.vue'
    export default {
        data() {
            return {
                quotes: [
                    "Simple quote"
                ],
                maxQuotes: 10
            }
        },
        components: {
            appQuoteGrid: QuoteGrid,
            appNewQuote: NewQuote
        },
        methods: {
            newQuote(quote) {
                this.quotes.push(quote)
            },
            deleteQuote(index) {
                this.quotes.splice(index, 1)
            }
        }
    }
</script>

<style>
</style>
