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