<script setup>
import ExpandBox from './components/ExpandBox.vue';
import Card from './components/Card.vue';
import CardFull from './components/CardFull.vue';
const caixas = [
    { id: 1, title:'Caixa1', content:'Conteudo 1', qty:100},
    { id: 1, title:'Caixa2', qty:30},
    { id: 1, title:'Caixa3', content:'Conteudo 3'},
    { id: 1, title:'Caixa4'},
]
</script>

<template>
    <h1>componentes</h1>
    <hr>
    <h2>cards</h2>
    <Card title="Título do card">
      <p>Conteúdo do card</p>
    </Card>
    <Card title="Card 2"></Card>
    <hr>
    <CardFull>
        <p>Body</p>
      <template #header>
        <h1>Header</h1>
      </template>
      <template #footer>
        <p>Footer</p>
      </template>
    </CardFull>
<p>ain</p>
    
    <CardFull>
      <template #header>
        <h1>Header</h1>
      </template>
      <p>Body</p>
    </CardFull>
<hr>
    <h2>props</h2>
    <Expand-box v-for="caixa in caixas" :key="caixa.id" v-bind="caixa"/>
   <!-- <ExpandBox title="caixa1" content="ain nobru apelão"/>
    <expand-box qty="50"/>-->

</template>

<style scoped></style>
