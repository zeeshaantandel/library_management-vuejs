<template>
    <div>
        <v-list dense>
            <v-header>Books</v-header>
            <v-list-item v-for="item in books" :key="item.id">
                <v-list-item-avatar>
                    <v-img :src="item.img"></v-img>
                </v-list-item-avatar>

                <v-list-item-content>
                    <v-list-item-title>{{ item.title }}</v-list-item-title>
                    <v-list-item-subtitle>{{ item.author.name }}</v-list-item-subtitle>
                    <v-list-item-subtitle>Pages: {{ item.pages }}</v-list-item-subtitle>
                </v-list-item-content>

                <v-list-item-icon>
                    <v-menu offset-y>
                        <template v-slot:activator="{ on, attrs }">
                            <v-btn v-bind="attrs" v-on="on" icon>
                                <v-icon>mdi-dots-vertical</v-icon>
                            </v-btn>
                        </template>
                        <v-list>
                            <v-list-item>
                                <v-list-item-title>Edit</v-list-item-title>
                                <v-icon>mdi-pencil</v-icon>
                            </v-list-item>
                            <v-list-item>
                                <v-list-item-title>Delete</v-list-item-title>
                                <v-list-item-title>mdi-delete</v-list-item-title>
                            </v-list-item>
                            <v-list-item>
                                <v-list-item-title>Issue</v-list-item-title>
                            </v-list-item>
                            <v-list-item>
                                <v-list-item-title>Return</v-list-item-title>
                            </v-list-item>
                        </v-list>
                    </v-menu>

                    Status
                </v-list-item-icon>

                

            </v-list-item>
        </v-list>
    </div>
</template>

<script>
    import booksList from '@/data/books.json'
    export default {
        data() {
            return {
                books: booksList
            }
        },
        
    }
</script>

<style lang="scss" scoped>

</style>