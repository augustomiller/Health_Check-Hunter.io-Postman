# Health Check-Hunter.io
Projeto de automação da API hunter.io, para verificar a saúde dos recursos rodando um conjunto de testes periódicos a cada cinco minutos de forma automatizada.

<p align="center">
  <a href="#Documentação">Documentação</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#Premissas">Premissas</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#Tecnologias">Tecnologias</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#Plano-de-teste">Plano de teste</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#Baby-Steps">Baby steps</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="#License">License</a>
</p>

<p align="center">
  <a href="https://mit-license.org/">
  <img src="https://img.shields.io/static/v1?label=license&message=MIT&color=5965E0&labelColor=121214" alt="License">
  </a>
</p>

<br>

![hunterlogo](https://user-images.githubusercontent.com/990877/132140715-c9058f6d-aa91-40c1-9f22-5f24f39e281c.png)

![hunterio](https://user-images.githubusercontent.com/990877/132139561-b0200e2c-5eea-40f2-9805-1cd51b279495.png)

<p align="center">
  <a href="https://hunter.io/">hunter.io</a>&nbsp;&nbsp;&nbsp;|&nbsp;&nbsp;&nbsp;
  <a href="https://hunter.io/api-documentation/v2">hunter.doc</a>&nbsp;&nbsp;&nbsp;
</p>

## Tecnologias

- [Postman](https://www.postman.com/)
- [NodeJS](https://nodejs.org/en/)
- [Newman](https://www.npmjs.com/package/newman)
- [VSCode](https://code.visualstudio.com/)
- [Microsoft Excel](https://www.microsoft.com/pt-br/microsoft-365/excel)

### Premissas

- [ ] Criar um Workspace colaborativo no Postman.
- [ ] Deve ser executado no ambiente de desenvolvimento e ambiente de testes.
- [ ] Todos os testes do plano de teste devem ser executados.
- [ ] Todos os dados de reuisição precisam de body, devem ser parametrizados com valores de dados externos.
- [ ] Executar no mínimo de cinco iterações.
- [ ] Gerar documentação de testes.
- [ ] Exportar o resultado das execuções para um arquivo .json.
- [ ] Executar os testes do plano de testes no newman, gerando relatórios da execução.

## Plano de teste
- [x] [criar plano de teste.]()

<table>
<thead>
  <tr>
    <th>ID</th>
    <th>Caso de teste</th>
    <th>Autenticação</th>
     <th>Método</th>
     <th>Base URL</th>
     <th>Recurso</th>
     <th>Passos</th>
     <th>Resultado Esperado</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>TC 01</td>
    <td>Recuperar todos leads cadastrados</td>
    <td>API key</td>
    <td>GET</td>
    <td>api.hunter.io/v2</td>
    <td>leads</td>
    <td>Enviar requisição GET assíncrona para recuperar todos leads</td>
    <td>
      ✓Status code:200. ✓Stringo 'OK' no status code so response. ✓Tempo de execução < 2s.
    </td>
  </tr>
  <tr>
    <td>TC 02</td>
    <td>Recuperar lead específico</td>
    <td>API key</td>
    <td>GET</td>
    <td>api.hunter.io/v2</td>
    <td>leads/{id}</td>
    <td>Enviar requisição GET assíncrona para recuperar lead específico</td>
    <td>✓Status code: 200. ✓String 'OK' no response code. ✓Tempo de execução < 2 seg.</td>
  </tr>
    <tr>
    <td>TC 03</td>
    <td>Criar novo lead</td>
    <td>API key</td>
    <td>POST</td>
    <td>api.hunter.io/v2</td>
    <td>leads</td>
    <td>Enviar requisição POST assincrona para criar novo Lead</td>
    <td>✓Status code 200, 201 ou 202. ✓String 'Created' no status code do response. ✓Tempo de execução < 2 seg.</td>
  </tr>
    </tr>
    <tr>
    <td>TC 04</td>
    <td>Editar lead</td>
    <td>API key</td>
    <td>PUT</td>
    <td>api.hunter.io/v2</td>
    <td>leads/{id}</td>
    <td>Enviar requisição PUT assincrona para alterar Lead</td>
    <td>✓Status code: 204. ✓String 'No Content' no response code.</td>
  </tr>
    </tr>
    <tr>
    <td>TC 05</td>
    <td>Excluir lead</td>
    <td>API key</td>
    <td>DELETE</td>
    <td>api.hunter.io/v2</td>
    <td>leads/{id}</td>
    <td>Enviar requisição DELETE assincrona para deletar lead específico</td>
    <td>✓Status code: 204. ✓String 'No Content' no response code.</td>
  </tr>
    </tr>
    <tr>
    <td>TC 06</td>
    <td>Recuperar todas listas de leads cadastradas</td>
    <td>API key</td>
    <td>GET</td>
    <td>api.hunter.io/v2</td>
    <td>leads_lists</td>
    <td>Enviar requisição GET assíncrona para recuperar todas listas de leads</td>
    <td>✓Status code: 200. ✓String 'OK' no status code do response. ✓Tempo de execução < 2 seg.</td>
  </tr>
    </tr>
    <tr>
    <td>TC 07</td>
    <td>Recuperar lista de lead específica</td>
    <td>API key</td>
    <td>GET</td>
    <td>api.hunter.io/v2</td>
    <td>leads_lists/{id}</td>
    <td>Enviar requisição GET assíncrona para recuperar uma lista de leads específico</td>
    <td>✓Status code: 200. ✓String 'OK' no response code. ✓Tempo de execução < 2 seg.</td>
  </tr>
    </tr>
    <tr>
    <tdTC 08</td>
    <td>Criar nova lista de lead</td>
    <td>API key</td>
    <td>POST</td>
    <td>api.hunter.io/v2</td>
    <td>leads_lists</td>
    <td>Enviar requisição POST assincrona para criar nova lista de Lead</td>
    <td>✓Status code: 200, 201 ou 202. ✓String 'Created' no status code do response. ✓Tempo de execução < 2 seg.</td>
  </tr>
    </tr>
    <tr>
    <td>TC 09</td>
    <td>Editar lista de lead</td>
    <td>API key</td>
    <td>PUT</td>
    <td>api.hunter.io/v2</td>
    <td>leads_lists/{id}</td>
    <td>Enviar requisição PUT assincrona para alterar lista de Lead</td>
    <td>✓Status code: 204. ✓String 'No Content' no response code.</td>
  </tr>
    </tr>
    <tr>
    <td>TC 10</td>
    <td>Excluir lista de lead</td>
    <td>API key</td>
    <td>DELETE</td>
    <td>api.hunter.io/v2</td>
    <td>leads_lists/{id}</td>
    <td>Enviar requisição DELETE assincrona para deletar uma lista de lead específica</td>
    <td>✓Status code: 204. ✓String 'No Content' no response code.</td>
  </tr>
  
</tbody>
</table>

## Baby Steps

- [ ] Estudar a documentação da API.
- [ ] Criar o workspace no postman.
- [ ] Convidar membros.
- [ ] Criar Environments e variáveis.
- [ ] Criar a estrutura das Collections.
- [ ] Criar as requisições.
- [ ] Parametrizar as variáveis.
- [ ] Criar o arquivo com a massa de dados.
- [ ] Parametrizar as autenticações.
- [ ] Criar os Scripts de Pré-Requests.
- [ ] Criar os testes.
- [ ] Criar e executar com Monitor (um Monitor para cada Environment).
- [ ] Exportar resultados das execuções.
- [ ] Exportar coleção e ambiente.
- [ ] Preparar ambiente: nodeJS, newman, html-reporterextra.
- [ ] Criar a hierarquia de arquivos para o newman.
- [ ] Executar via newman a coleção e o Environment exportados.

##

## License

<div align="center">
  
<p>This project is licensed under the MIT License. See the
  <a href="https://mit-license.org/">
  <img src="https://img.shields.io/static/v1?label=license&message=MIT&color=5965E0&labelColor=121214" alt="License">
  </a> file for details.</p>
<p> Made with 🧡 &nbsp;by Maic Miller | with the help of Erick Valentin</p>
  
<div>
