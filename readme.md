## Um breve resumo sobre o ScubaPHP - Day 00

Trabalhar com PHP é sempre um desafio: devemos focar em melhorar o código ou apenas implementar a regra de negócio usando a estrutura existente?

O seu líder provavelmente irá priorizar aquilo que agrega valor ao negócio, nada de errado nisso, é o trabalho dele!

Você como uma pessoa desenvolvedora precisa aprender a negociar a inclusão de melhorias, pois a longo prazo um código deficiente acaba gerando grandes atrasos. É preciso realizar pequenas refatorações sem comprometer a entrega daquilo que é esperado pela gestão.

O seu projeto vai simular uma demanda no mundo real, no qual existem tanto códigos lindos nas mais modernas arquiteturas quanto códigos legados com algumas (muitas) dívidas técnicas. Você conseguiria negociar a refatoração de um trecho de código no framework fictício ScubaPHP?

Você irá, usando apenas código PHP e o framework que será disponibilizado, implementar as seguintes funcionalidades: login, cadastro, validação de email, recuperação de senha e refatorar o ScubaPHP para algo mais moderno.

Além de abordar temas como criptografia, envio de emails, sessão, protocolo HTTP, manipulação de arquivos, também abordará a técnica Spin Selling, muito usada para vendas e extremamente útil para negociar possíveis melhorias no código com pessoas que possivelmente não terão conhecimentos técnicos avançados.

São hard skills e soft skills em um case simulando o mundo real. Tenho certeza que irá te ajudar a lidar com problemas complexos no seu dia a dia!

### Uma breve análise da estrutura atual do ScubaPHP:

/data: pasta onde serão armazenados os dados dos usuários
/view: pasta com as templates
/resource: pasta com imagens e css
boot.php: responsável por carregar os arquivos
config.php: responsável por setar constantes
index.php: ponto de entrada do sistema
routes.php: responsável define o que será feito caso uma determinada url seja acionada

=== 

Criar os arquivos `controller.php` e `view.php` - usando ao similar ao MVC.
Esses dois novos arquivos farão o trabalho que hoje é feito por route.php.

Você criará as funções `do_register()`, `do_login()` e `do_not_found()` no arquivo `controller.php.` Já no arquivo `view.php`, você criará a função `render_view($template)`.

No arquivo `routes.php`, em vez de carregar o template da resposta, você chamará a função de `controller.php` de acordo com o parâmetro `GET ?page=value`

Já o `controller.php` usará a função do arquivo `view.php` para renderizar o conteúdo da resposta.