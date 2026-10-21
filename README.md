# Diagnóstico Fiscal de Criptomoedas

Página web com um questionário interativo para identificar o perfil de usuários de criptomoedas, apresentar orientações fiscais e direcionar o atendimento para o Contador do Trader.

## Como funciona

O questionário é dividido em seis etapas, com barra de progresso e validação das respostas obrigatórias:

1. **Seu perfil:** gênero e faixa etária.
2. **Sua perspectiva:** visão sobre criptomoedas e período em que começou a conhecê-las ou utilizá-las.
3. **Seu envolvimento:** frequência de uso e locais onde já operou, como exchanges nacionais, internacionais e carteiras/DEXs.
4. **Declaração e obrigações:** histórico de declaração de criptomoedas no IRPF.
5. **Barreiras:** dificuldades com organização, regras, câmbio e suporte.
6. **Objetivo:** o que o usuário busca resolver ou aprender.

Ao concluir, a página utiliza regras condicionais em JavaScript para montar um diagnóstico e um plano de ação com base nas respostas. As mensagens são predefinidas no próprio código.

O botão **Falar com um especialista** abre o WhatsApp com uma mensagem contendo as respostas do questionário. O envio depende da confirmação do usuário no WhatsApp. A página também oferece um link para baixar um e-book e a opção de refazer o questionário.

Todo o processamento do questionário acontece no navegador. O código não possui backend, banco de dados ou salvamento das respostas; ao recarregar a página ou clicar em **Refazer quiz**, o preenchimento é reiniciado.

> O resultado é orientativo, conforme as regras e os textos configurados no código. O questionário não calcula impostos nem confirma individualmente a obrigatoriedade de declarações ou entregas.



## Executar na máquina ou em uma VM Windows

### 1. Preparar o ambiente

- Baixe ou clone o repositório.
- Utilize um navegador atualizado, como Chrome, Edge ou Firefox, com JavaScript habilitado.
- Mantenha os arquivos `logo.png` e `favicon.png` na mesma pasta de `index.html` para exibir a identidade visual e o ícone da página.

O arquivo `index.html` contém a estrutura da página, os estilos CSS e toda a lógica JavaScript. As imagens são recursos externos ao HTML e devem ser adicionadas ao repositório com os nomes indicados.


### 2. Dependências

Não é necessário instalar bibliotecas, criar ambiente virtual ou executar comandos de instalação. A página utiliza HTML, CSS e JavaScript nativos do navegador.

O questionário pode ser utilizado localmente. Os botões de WhatsApp e download do e-book precisam de acesso à internet para abrir seus destinos externos.


### 3. Ajustar os contatos e conteúdos

No bloco `<script>` de **`index.html`**, ajuste a constante `WHATS_PHONE` para o número de atendimento, utilizando somente números, com código do país e DDD:

```javascript
const WHATS_PHONE = "5543999999999";
```

O número acima é apenas um exemplo. Substitua pelo contato que deve receber as solicitações.

Para alterar o e-book, substitua o endereço do atributo `href` no link **Baixar E-Book Cripto Grátis**. Verifique se o arquivo de destino possui permissão de acesso para o público desejado.

Os textos das perguntas e alternativas ficam no formulário HTML. As cores, fontes e demais estilos ficam no bloco `<style>`.


### 4. Iniciar

Abra o arquivo **`index.html`** diretamente no navegador, com um duplo clique ou pela opção **Abrir com**.



## Como utilizar

1. Abra a página de diagnóstico.
2. Responda às perguntas de cada etapa e clique em **Continuar**.
3. Utilize **Voltar** caso queira revisar alguma resposta.
4. Na etapa final, clique em **Ver meu resultado**.
5. Leia o diagnóstico e o plano de ação apresentados.
6. Para solicitar atendimento, clique em **Falar com um especialista**, confira a mensagem e confirme seu envio no WhatsApp.
7. Utilize **Baixar E-Book Cripto Grátis** para acessar o material ou **Refazer quiz** para iniciar um novo preenchimento.

A seleção dos locais onde o usuário já operou é opcional. As demais perguntas possuem validação para permitir o avanço entre as etapas.
