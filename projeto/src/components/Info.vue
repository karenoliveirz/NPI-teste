<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
       <p v-else> Estou em busca de novas oportunidades </p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ul>
            <li>JavaScript</li>
            <li>CSS</li>
            <li>HTML</li>
        </ul>
        <div>
            <button @click= "showEmail" >Mostrar e-mail</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para {{ email }} </p>
        <p>Para acessar meu portfólio <a v-bind:href="meu_link" target="_blank">basta clicar aqui</a></p>
        <Picture/>
    </div>
</template>

<script>
import Picture from './Picture.vue'

export default{
    name: 'Info',
    components:{
        Picture
    },
    
    data(){
        return{
            esta_trabalhando: true,
            mostrar_email: false,
            email: 'karen@npi.com',
            meu_link: 'https://google.com'
    }
    },
    methods:{
        showEmail(){
            console.log('testando') 
            //this.mostrar_email =!this.mostrar_email
        }
    }
}
</script>
