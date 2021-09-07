<div text align="center">

# ⛑ Health Check Hunter.io

</div>

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

- [x] Criar um Workspace colaborativo no Postman.
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
    <td><img src="https://img.shields.io/badge/API-Key-lightgrey"></td>
    <td> <img src="https://img.shields.io/badge/%E2%87%A3-GET-green"> </td>
    <td><a href="https://hunter.io/api-documentation/v2"><img src="https://img.shields.io/badge/%F0%9F%A6%8A-URL-9cf"></a></td>
    <td>leads</td>
    <td>Enviar requisição GET assíncrona para recuperar todos leads</td>
    <td>
      <img src="https://img.shields.io/badge/STATUS%20CODE-200-success">
      <img src="https://img.shields.io/badge/String%20'OK'%20-response-success">
      <img src="https://img.shields.io/badge/Tempo%20Execu%C3%A7%C3%A3o%20-%3C%202s-success">
    </td>
  </tr>
  <tr>
    <td>TC 02</td>
    <td>Recuperar lead específico</td>
    <td><img src="https://img.shields.io/badge/API-Key-lightgrey"></td>
    <td><img src="https://img.shields.io/badge/%E2%87%A3-GET-green"></td>
    <td><a href="https://hunter.io/api-documentation/v2"><img src="https://img.shields.io/badge/%F0%9F%A6%8A-URL-9cf"></a></td>
    <td>leads/{id}</td>
    <td>Enviar requisição GET assíncrona para recuperar lead específico</td>
    <td>
      <img src="https://img.shields.io/badge/STATUS%20CODE-200-success">
      <img src="https://img.shields.io/badge/String%20'OK'%20-response-success">
      <img src="https://img.shields.io/badge/Tempo%20Execu%C3%A7%C3%A3o%20-%3C%202s-success">
    </td>
  </tr>
    <tr>
    <td>TC 03</td>
    <td>Criar novo lead</td>
    <td><img src="https://img.shields.io/badge/API-Key-lightgrey"></td>
    <td><img src="https://img.shields.io/badge/%E2%87%A1-POST-yellow"></td>
    <td><a href="https://hunter.io/api-documentation/v2"><img src="https://img.shields.io/badge/%F0%9F%A6%8A-URL-9cf"></a></td>
    <td>leads</td>
    <td>Enviar requisição POST assincrona para criar novo Lead</td>
    <td>
      <img src="https://img.shields.io/badge/STATUS%20CODE-200%2C%20201%2C%20202-success">
      <img src="https://img.shields.io/badge/String%20'Created'%20-response-success">
      <img src="https://img.shields.io/badge/Tempo%20Execu%C3%A7%C3%A3o%20-%3C%202s-success">
    </td>
  </tr>
    </tr>
    <tr>
    <td>TC 04</td>
    <td>Editar lead</td>
    <td><img src="https://img.shields.io/badge/API-Key-lightgrey"></td>
    <td><img src="https://img.shields.io/badge/%E2%87%A1-PUT-blue"></td>
    <td><a href="https://hunter.io/api-documentation/v2"><img src="https://img.shields.io/badge/%F0%9F%A6%8A-URL-9cf"></a></td>
    <td>leads/{id}</td>
    <td>Enviar requisição PUT assincrona para alterar Lead</td>
    <td>
      <img src="https://img.shields.io/badge/STATUS%20CODE-204-success">
      <img src="https://img.shields.io/badge/String%20'No%20Content'-response-success">
    </td>
  </tr>
    </tr>
    <tr>
    <td>TC 05</td>
    <td>Excluir lead</td>
    <td><img src="https://img.shields.io/badge/API-Key-lightgrey"></td>
    <td><img src="https://img.shields.io/badge/%E2%98%A0%EF%B8%8E-DEL-red"></td>
    <td><a href="https://hunter.io/api-documentation/v2"><img src="https://img.shields.io/badge/%F0%9F%A6%8A-URL-9cf"></a></td>
    <td>leads/{id}</td>
    <td>Enviar requisição DELETE assincrona para deletar lead específico</td>
    <td>
      <img src="https://img.shields.io/badge/STATUS%20CODE-204-success">
      <img src="https://img.shields.io/badge/String%20'No%20Content'-response-success">
    </td>
  </tr>
    </tr>
    <tr>
    <td>TC 06</td>
    <td>Recuperar todas listas de leads cadastradas</td>
    <td><img src="https://img.shields.io/badge/API-Key-lightgrey"></td>
    <td><img src="https://img.shields.io/badge/%E2%87%A3-GET-green"></td>
    <td><a href="https://hunter.io/api-documentation/v2"><img src="https://img.shields.io/badge/%F0%9F%A6%8A-URL-9cf"></a></td>
    <td>leads_lists</td>
    <td>Enviar requisição GET assíncrona para recuperar todas listas de leads</td>
    <td>
      <img src="https://img.shields.io/badge/STATUS%20CODE-200-success">
      <img src="https://img.shields.io/badge/String%20'OK'%20-response-success">
      <img src="https://img.shields.io/badge/Tempo%20Execu%C3%A7%C3%A3o%20-%3C%202s-success">
    </td>
  </tr>
    </tr>
    <tr>
    <td>TC 07</td>
    <td>Recuperar lista de lead específica</td>
    <td><img src="https://img.shields.io/badge/API-Key-lightgrey"></td>
    <td><img src="https://img.shields.io/badge/%E2%87%A3-GET-green"></td>
    <td><a href="https://hunter.io/api-documentation/v2"><img src="https://img.shields.io/badge/%F0%9F%A6%8A-URL-9cf"></a></td>
    <td>leads_lists/{id}</td>
    <td>Enviar requisição GET assíncrona para recuperar uma lista de leads específico</td>
    <td>
      <img src="https://img.shields.io/badge/STATUS%20CODE-200-success">
      <img src="https://img.shields.io/badge/String%20'OK'%20-response-success">
      <img src="https://img.shields.io/badge/Tempo%20Execu%C3%A7%C3%A3o%20-%3C%202s-success">
    </td>
  </tr>
    </tr>
    <tr>
    <td>TC 08</td>
    <td>Criar nova lista de lead</td>
    <td><img src="https://img.shields.io/badge/API-Key-lightgrey"></td>
    <td><img src="https://img.shields.io/badge/%E2%87%A1-POST-yellow"></td>
    <td><a href="https://hunter.io/api-documentation/v2"><img src="https://img.shields.io/badge/%F0%9F%A6%8A-URL-9cf"></a></td>
    <td>leads_lists</td>
    <td>Enviar requisição POST assincrona para criar nova lista de Lead</td>
    <td>
      <img src="https://img.shields.io/badge/STATUS%20CODE-200%2C%20201%2C%20202-success">
      <img src="https://img.shields.io/badge/String%20'Created'%20-response-success">
      <img src="https://img.shields.io/badge/Tempo%20Execu%C3%A7%C3%A3o%20-%3C%202s-success">
    </td>
  </tr>
    </tr>
    <tr>
    <td>TC 09</td>
    <td>Editar lista de lead</td>
    <td><img src="https://img.shields.io/badge/API-Key-lightgrey"></td>
    <td><img src="https://img.shields.io/badge/%E2%87%A1-PUT-blue"></td>
    <td><a href="https://hunter.io/api-documentation/v2"><img src="https://img.shields.io/badge/%F0%9F%A6%8A-URL-9cf"></a></td>
    <td>leads_lists/{id}</td>
    <td>Enviar requisição PUT assincrona para alterar lista de Lead</td>
    <td>
      <img src="https://img.shields.io/badge/STATUS%20CODE-204-success">
      <img src="https://img.shields.io/badge/String%20'No%20Content'-response-success">
    </td>
  </tr>
    </tr>
    <tr>
    <td>TC 10</td>
    <td>Excluir lista de lead</td>
    <td><img src="https://img.shields.io/badge/API-Key-lightgrey"></td>
    <td><img src="https://img.shields.io/badge/%E2%98%A0%EF%B8%8E-DEL-red"></td>
    <td><a href="https://hunter.io/api-documentation/v2"><img src="https://img.shields.io/badge/%F0%9F%A6%8A-URL-9cf"></a></td>
    <td>leads_lists/{id}</td>
    <td>Enviar requisição DELETE assincrona para deletar uma lista de lead específica</td>
    <td>
      <img src="https://img.shields.io/badge/STATUS%20CODE-204-success">
      <img src="https://img.shields.io/badge/String%20'No%20Content'-response-success">
    </td>
  </tr>
  
</tbody>
</table>

## Baby Steps

- [x] Estudar a documentação da API.
- [x] Criar o workspace no postman.
- [x] Convidar membros.
- [x] Criar Environments e variáveis de ambiente (ex: base_url).
<a href="https://user-images.githubusercontent.com/990877/132260121-7f2d0e6b-8c12-45f1-9610-d2d69c52b77f.png"><img src="https://img.shields.io/badge/ex%3A%20-png-9cf"></a>

- [x] Criar a estrutura das Collections.
<a href="https://user-images.githubusercontent.com/990877/132251798-69de8aba-4a2d-4b07-a600-704f9f87144e.png"><img src="https://img.shields.io/badge/ex%3A%20-png-9cf"></a>

- [x] Criar as requisições.
<a href="https://user-images.githubusercontent.com/990877/132255845-64c58d75-74cf-4818-a7cd-6c90e2c18088.png"><img src="https://img.shields.io/badge/ex%3A%20-png-9cf"></a>

- [x] Parametrizar as variáveis.
<a href="https://user-images.githubusercontent.com/990877/132256061-500cc661-1bba-4c05-b1c5-a58aece176c4.png"><img src="https://img.shields.io/badge/ex%3A%20-png-9cf"></a>

- [x] Criar o arquivo com a massa de dados.
<a href="https://user-images.githubusercontent.com/990877/132259231-28ab0e36-d194-4943-a2eb-1d2fd7657fd3.png"><img src="https://img.shields.io/badge/ex%3A%20-png-9cf"></a>

- [x] Parametrizar as autenticações.
<a href="https://user-images.githubusercontent.com/990877/132256061-500cc661-1bba-4c05-b1c5-a58aece176c4.png"><img src="https://img.shields.io/badge/ex%3A%20-png-9cf"></a>

- [x] Criar os Scripts de Pré-Requests.
<a href="https://user-images.githubusercontent.com/990877/132260029-62c8dcad-0f92-4ff1-afef-39672e3f375d.png"><img src="https://img.shields.io/badge/ex%3A%20-png-9cf"></a>

- [x] Criar os testes no Postman.
<a href="https://user-images.githubusercontent.com/990877/132261275-80eb7dab-8792-42a6-ab59-94f3f361f3f9.png"><img src="https://img.shields.io/badge/ex%3A%20-png-9cf"></a>
<a href="https://codebeautify.org/alleditor/cbded3c8"><img src="https://img.shields.io/badge/ex%3A%20-code-ff69b4"></a>

- [x] Criar e executar os testes via Monitor (um Monitor para cada Environment).
<a href="https://user-images.githubusercontent.com/990877/132272283-34a891c5-d4c5-4390-9b43-57507fbf6013.png"><img src="https://img.shields.io/badge/ex%3A%20-png-9cf"></a>
- [x] Exportar resultados das execuções.
<a href="https://user-images.githubusercontent.com/990877/132272524-90e468d7-2d19-4cb4-8dc8-2bf5a0d05a64.png"><img src="https://img.shields.io/badge/ex%3A%20-png-9cf"></a>
- [x] Exportar coleção e ambiente.
- [x] Preparar ambiente: nodeJS, newman, html-reporterextra.
- [x] Criar a hierarquia de arquivos para o newman.
- [x] Executar via newman a coleção e o Environment exportados.

```script
newman run -d data/data_lead.csv Hunter.io\ API.postman_collection.json -e Tests.postman_environment.json
```
![Screen Shot 2021-09-06 at 23 06 32](https://user-images.githubusercontent.com/990877/132273305-2cd41c71-e3a7-4b8c-9fcf-cbb25f2b1d04.png)

- [x] Gerar relatório Html.

```script
➜ newman run -d data/data_lead.csv Hunter.io\ API.postman_collection.json -e Tests.postman_environment.json --reporter-htmlextra-title "Relatorio Postman" -r htmlextra
```
![Screen Shot 2021-09-06 at 23 06 52](https://user-images.githubusercontent.com/990877/132273335-06ac518e-dcca-47a7-a62e-293c326daa99.png)

## Relatórios



##

## License

<div align="center">
  
<p>This project is licensed under the MIT License. See the
  <a href="https://mit-license.org/">
  <img src="https://img.shields.io/static/v1?label=license&message=MIT&color=5965E0&labelColor=121214" alt="License">
  </a> file for details.</p>
<p> Made with&nbsp;🧡 &nbsp;by Maic Miller | with the help of Erick Valentin</p>
  
<div>
