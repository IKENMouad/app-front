<template>
    <div class="container mt-5">
        <div class="row">
            <div class="col-md-6 mx-auto">
                <div class="card">
                    <h4 class="card-header bg-white text-center ">
                        {{ loginForm }}
                    </h4>
                    <div class="card-body">
                        <div class="card-text">
                            <form>
                                <Input
                                    inputName="username"
                                    label="User name:"
                                    :isAutofocus="true"
                                    :value="loginForm.username"
                                />
                            </form>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import Input from '../../partials/Input.vue';
export default {
    name: 'Login',
    components: { Input },
    props: {},
    data() {
        return {
            loginForm: {
                username: '',
                email: '',
                password: ''
            }
        };
    }
};
</script>

<style></style>
