<template>
    <div class="row">
        <div class="col-md-3"></div>
        <div class="col-md-6 pt-4">

            <!-- Vertical form -->
            <div class="card">

                <div class="card-body">
                    <form @submit.prevent="submit">
                        <div class="form-group">
                            <label>Comapany Name</label>
                            <input v-model="fields.company_name" type="text" class="form-control company_name">
                        </div>

                        <div class="form-group">
                            <label>Display Name</label>
                            <input v-model="fields.display_name" type="text" class="form-control display_name">
                        </div>

                        <div class="form-group">
                            <label>Company Status</label>
                            <select v-model="fields.status" class="form-control status">
                                <option value="1">Active</option>
                                <option value="0">InActive</option>
                            </select>
                        </div>

                        <div class="text-right pt-1">
                            <button type="submit" class="btn btn-primary">Submit form <i class="icon-paperplane ml-2"></i></button>
                        </div>
                    </form>
                </div>
            </div>
            <!-- /vertical form -->

        </div>
        <div class="col-md-2"></div>
    </div>
</template>

<script>
    export default{
        data() {
            return {
                fields : {},
                errors : {},
            };
        },
        methods :{
            submit(){
                axios
                .post("/api/company/create", this.fields)
                .then(()=>{
                    // this.$router.push({name: "Company"}) = response.data
                })
                .catch((error)=>{
                    console.log(error);
                });
                console.log(this.fields);
            },
        },
    }
</script>
