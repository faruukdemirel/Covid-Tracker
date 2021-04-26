<template>
    <div>
        <select 
        class="form-select mt-10 block w-full border p-3 rounded "
        @change="onChangeSelect()"
         v-model="selected">
            <option value="0">Select Country</option>
            <option  v-for="country in countries" :key="country.ID" :value="country.ID">
                {{country.Country}}
            </option>
        </select>
    </div>
</template>

<script>
    export default {
        name:'CountrySelect',
        props:['countries'],
        data(){
            return{
                selected:0
            }
        },
        methods:{
            onChangeSelect(){
                const country=this.countries.find((item)=>item.ID == this.selected)
                this.$emit('get-country',country)
            }
        }
    }
</script>

<style scoped>

</style>