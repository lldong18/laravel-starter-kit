<template>
    <div class="page_wrap_vue users_view">
        <v-tabs dark v-model="active">
            <v-tabs-bar class="cyan">
                <v-tabs-item href="#users" ripple>
                    Users
                </v-tabs-item>
                <v-tabs-item href="#groups" ripple>
                    Groups
                </v-tabs-item>
                <v-tabs-item href="#permissions" ripple>
                    Permissions
                </v-tabs-item>
                <v-tabs-slider class="yellow"></v-tabs-slider>
            </v-tabs-bar>
            <v-tabs-items>
                <v-tabs-content id="users">
                    <v-card flat>
                        <v-card-text>
                            <user-lists></user-lists>
                        </v-card-text>
                    </v-card>
                </v-tabs-content>
                <v-tabs-content id="groups">
                    <v-card flat>
                        <v-card-text>
                            <group-lists></group-lists>
                        </v-card-text>
                    </v-card>
                </v-tabs-content>
                <v-tabs-content id="permissions">
                    <v-card flat>
                        <v-card-text>
                            <permission-lists></permission-lists>
                        </v-card-text>
                    </v-card>
                </v-tabs-content>
            </v-tabs-items>
        </v-tabs>
    </div>
</template>

<script>
    import UserLists from '../components/user/UserLists.vue';
    import GroupLists from '../components/user/GroupLists.vue';
    import PermissionLists from '../components/user/PermissionLists.vue';
    export default {
        components: {
            UserLists,
            GroupLists,
            PermissionLists
        },
        data() {
            return {
                active: ''
            }
        },
        watch: {
            active(v) {
                console.log('active tab: ' + v);
            }
        },
        mounted() {
            console.log('pages.Users.vue');

            const self = this;
        }
    }
</script>