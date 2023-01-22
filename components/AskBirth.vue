<template>
    <div>
        <h1>When is your birthday?</h1>
        <input v-model="dateInput" type="date"/>
        <h3>My birthday is on {{ dateInput }}.

        <!-- <div v-if="dateInput > Date.now()">I am the future.</div>
        <div v-else-if="dateInput < Date.now()">I am the past.</div>
        <div v-else>I am now.</div>  -->

            <div v-if="parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) >= 321 && parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) <=419">I am Aries.</div>
            <div v-else-if="parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) >= 420 && parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) <=520">I am Taurus.</div>
            <div v-else-if="parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) >= 521 && parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) <=620">I am Gemini.</div>
            <div v-else-if="parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) >= 621 && parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) <= 722">I am Cancer.</div>
            <div v-else-if="parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) >= 723 && parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) <= 822">I am Leo.</div>
            <div v-else-if="parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) >= 823 && parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) <= 922">I am Virgo.</div>
            <div v-else-if="parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) >= 923 && parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) <= 1022">I am Libra.</div>
            <div v-else-if="parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) >= 1023 && parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) <= 1121">I am Scorpio.</div>
            <div v-else-if="parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) >= 1122 && parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) <= 1221">I am Sagittarius.</div>
            <div v-else-if="parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) >= 1222">I am Capricorn.</div>
            <div v-else-if="parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) <= 119">I am Capricorn.</div>
            <div v-else-if="parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) >= 120 && parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) <= 218">I am Aquarius.</div>
            <div v-else-if="parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) >= 219 && parseInt(dateInput.split('-')[1] + dateInput.split('-')[2]) <= 320">I am Pisces.</div>
            <div v-else>I am the future.</div>
        </h3>
        <br/>
        <br/>
        

        <h1>Then next, click your star sign below!</h1>
            <h3>
                <ul>
                    <li v-for="sign in signs" :key="sign" type="circle" @click="mysign(sign)">
                        {{ sign }}
                    </li>
                </ul>
            </h3>
        
        

    </div>
</template>

<script>
    export default {
        data(){
            return{
                dateInput: '',
                signs: ['Aries', 'Tauru', 'Gemini', 'Cancer','Leo','Virgo','Libra','Scorpio','Sagittarius','Capricorn','Aquarius', 'Pisces'],
                abc: '2022-03-12'
            }
        },
        watch:{
            dateInput(newVal, oldVal){
                console.log('dateInput',newVal);
                console.log('new Date(dateInput)', new Date(newVal))
                console.log("new Date('2022-03-21')", new Date('2022-03-21'))
                console.log("new Date('2022-04-19')", new Date('2022-04-19'))
            }
        },
        methods:{
            mysign(sign){
                alert('My star sign is ' + sign + '.')
            }
            // newabc(){
            //     this.abc = parseInt(this.abc.split('-')[1] + this.abc.split('-')[2])
            //     return this.abc
            // }
        },
        
    }
</script>

<style lang="scss" scoped>

</style>