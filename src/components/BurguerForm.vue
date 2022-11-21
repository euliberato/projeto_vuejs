<template>
    <div>
        <p>Comp. de Mensagem</p>
        <div>
            <form id="burguer-form">
                <div class="input-container">
                    <label for="nome">Nome do cliente:</label>
                    <input type="text" name="name" id="nome" v-model="nome" placeholder="Digite seu nome">
                </div>
                <div class="input-container">
                    <label for="pao">Escolha o pão:</label>
                    <select name="pao" id="pao" v-model="pao">
                        <option value="">Selecione o seu:</option>
                        <option value="integral">Integral</option>
                    </select>
                </div>
                <div class="input-container">
                    <label for="carne">Escolha a carne:</label>
                    <select name="carne" id="carne" v-model="carne">
                        <option value="">Selecione a sua:</option>
                        <option value="picanha">Picanha</option>
                    </select>
                </div>
                <div class="input-container" id="opcionais-container">
                    <label for="opcionais" id="opcionais-title">Selecione os opcionais:</label>
                    <div class="checkbox-container">
                        <input type="checkbox" name="opcionais" v-model="opcionais" value="opcionais">
                        <span>Verduras</span>
                    </div>
                    <div class="input-container">
                        <input type="submit" value="Criar" class="submit-btn">
                    </div>
                </div>
            </form>
        </div>
    </div>
</template>

<script>
export default {
    name: "BurguerForm"
}
</script>

<style scoped>
    #burguer-form {
        max-width: 400px;
        margin: 0 auto;
    }

    .input-container {
        display: flex;
        flex-direction: column;
        margin-bottom: 20px;
    }

    label {
        font-weight: bold;
        margin-bottom: 15px;
        color: #222;
        padding: 5px 10px;
        border-left: 4px solid #fcba03;
    }

    input, select {
        padding: 5px 10px;
        width: 300px;
    }

    #opcionais-container {
        flex-direction: row;
        flex-wrap: wrap;
    }

    #opcionais-title {
        width: 100%;

    }

    .checkbox-container {
        display: flex;
        align-items: flex-start;
    }

    .checkbox-container span,
    .checkbox-container input {
        width: auto;
    }

    .checkbox-container span {
        margin-left: 6px;
        font-weight: bold;
    }

    .submit-btn {
        background-color: #222;
        color: #fcba03;
        font-weight: bold;
        border: 2px solid #222;
        padding: 10px;
        font-size: 16px;
        margin: 0 auto;
        cursor: pointer;
        transition: .5s;
    }

    .submit-btn:hover {
        background-color: transparent;
        color: #222;
    }

</style>