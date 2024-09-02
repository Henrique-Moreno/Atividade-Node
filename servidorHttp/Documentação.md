<h1>Documentação - Criação do Servidor HTTP</h1>

<h2>Descrição</h2>
<p>
    Este documento descreve a criação de um servidor HTTP utilizando o framework Express no Node.js. O servidor é configurado para lidar com requisições HTTP básicas e também inclui testes para validar o comportamento das rotas.
</p>

<h2>Funcionamento</h2>

<h3>Importação de Dependências</h3>
<p>
    O código utiliza o framework <code>Express</code> para facilitar a criação e gestão do servidor HTTP. O módulo <code>express</code> é importado com a sintaxe <code>import</code>, o que requer que o projeto esteja configurado como um módulo ECMAScript (ESM).
    Isso pode ser feito adicionando <code>"type": "module"</code> ao <code>package.json</code> ou renomeando o arquivo para <code>.mjs</code>.
</p>

<h3>Criação do Servidor</h3>
<p>
    O servidor é criado e configurado no arquivo <code>server.js</code>. As principais funcionalidades do servidor são descritas a seguir:
</p>
<ul>
    <li><strong>Criação da Instância do Aplicativo</strong>: Uma instância do aplicativo Express é criada com <code>const app = express();</code>.</li>
    <li><strong>Middleware para JSON</strong>: O middleware <code>express.json()</code> é utilizado para analisar o corpo das requisições como JSON.</li>
    <li><strong>Rotas</strong>:
        <ul>
            <li><code>/</code>: Retorna a mensagem "Hello World".</li>
            <li><code>/data</code>: Recebe dados no corpo da requisição e retorna uma resposta JSON com a mensagem "Sucesso" e os dados recebidos.</li>
        </ul>
    </li>
    <li><strong>Configuração da Porta</strong>: O servidor escuta na porta 3000, configurada na variável <code>PORT</code>.</li>
    <li><strong>Início do Servidor</strong>: O servidor é iniciado com <code>app.listen(PORT, () => { console.log(`Servidor rodando na porta ${PORT}`); });</code>.</li>
</ul>

<h3>Testes de Integração</h3>
<p>
    Testes de integração são escritos utilizando <code>Mocha</code> e <code>Chai</code> para validar o comportamento das rotas. O arquivo <code>test/integration.test.js</code> contém os seguintes testes:
</p>
<ul>
    <li><strong>Teste da Rota GET /</strong>: Verifica se a rota <code>/</code> retorna a mensagem "Hello World" com o status 200.</li>
    <li><strong>Teste da Rota POST /data</strong>: Verifica se a rota <code>/data</code> aceita um JSON e retorna a mesma estrutura JSON com a mensagem "Sucesso".</li>
</ul>

<h3>Criação de Funções Matemáticas</h3>
<p>
    Além do servidor, um arquivo <code>math.js</code> foi criado para implementar funções básicas de matemática:
</p>
<ul>
    <li><code>adicao(a, b)</code>: Retorna a soma de <code>a</code> e <code>b</code>.</li>
    <li><code>subtracao(a, b)</code>: Retorna a diferença entre <code>a</code> e <code>b</code>.</li>
    <li><code>multiplicacao(a, b)</code>: Retorna o produto de <code>a</code> e <code>b</code>.</li>
    <li><code>divisao(a, b)</code>: Retorna o quociente de <code>a</code> dividido por <code>b</code>.</li>
</ul>

<h2>Procedimentos para a Realização da Atividade</h2>

<h3>1. Configuração do Projeto</h3>
<p>
    Inicialize um novo projeto Node.js e instale as dependências necessárias: <code>express</code>, <code>mocha</code>, <code>chai</code>, e <code>chai-http</code>.
</p>

<h3>2. Criação do Servidor HTTP</h3>
<p>
    Crie um arquivo <code>server.js</code> para configurar e iniciar o servidor HTTP básico utilizando Express. Adicione duas rotas: uma rota GET para <code>/</code> e uma rota POST para <code>/data</code>.
</p>

<h3>3. Estrutura do Projeto</h3>
<p>
    Crie um arquivo <code>math.js</code> para implementar funções simples de matemática.
</p>

<h3>4. Escrever Testes de Integração</h3>
<p>
    No arquivo <code>test/integration.test.js</code>, escreva testes de integração para validar o comportamento das rotas do servidor usando Mocha e Chai.
</p>

<h3>5. Executar os Testes</h3>
<p>
    Configure um script no <code>package.json</code> para rodar os testes e execute-os para garantir que todos os testes passem.
</p>

<h3>6. Documentação e Entrega</h3>
<p>
    Documente o projeto conforme descrito neste documento e entregue conforme os requisitos especificados.
</p>
