<script lang="ts">
import { obterCategorias } from '@/http';

    export default {
        data() {
            return {
                categorias: obterCategorias()
            }
        }
    }
</script>

<template>
    <section class="selecionar-ingredientes">
        <h1 class="cabecalho titulo-ingredientes">Ingredientes</h1>

        <p class="paragrafo-lg instrucoes">Selecione abaixo os ingredientes que você quer usar nesta receita:</p>

        <ul class="categorias">
            <li v-for="categoria in categorias" :key="categoria.nome">
                {{ categoria.nome }}
            </li>
        </ul>

        <p class="paragrafo dica">
            "Atenção: consideramos que você tem em casa sal, pimenta e água."
        </p>
    </section>
</template>