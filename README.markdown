# Ruby on Rails Tutorial: sample application

This is the sample application for
[*Ruby on Rails Tutorial: Learn Rails by Example*](http://railstutorial.org/)
by [Michael Hartl](http://michaelhartl.com/).

## Comandos
Iniciando um projeto Rails sem os testes defaults do Rails.
	$ rails new exemplo -T -d mysql

Instalando as gems descritas no arquivo Gemfile no projeto Rails.
	$ bundle install

Instala a gem do heroku para poder enviar a aplicação para web.
	$ [sudo] gem install heroku
	$ heroku keys:add
	$ heroku create

Instala o rspec no seu projeto rails.
	$ rails generate rspec:install

Instalando o autotest no mac para que ele mande as mensagens de RED-GREEN pelo growl.
	$ [sudo] gem install autotest -v 4.4.6
	$ [sudo] gem install autotest-rails-pure -v 4.1.2
	$ [sudo] gem install autotest-fsevent -v 0.2.4
	$ [sudo] gem install autotest-growl -v 0.2.9

Configurando um arquivo default de autotest onde o faça require as gems para funcionar a mensagem pelo growl.
	$ mate ~/.autotest
	require 'autotest/growl'
	require 'autotest/fsevent'

Remover essas pastas se está utilizando o Rspec no projeto.
	$ git rm -r spec/views
	$ git rm -r spec/helpers
	$ rm -rf spec/views
	$ rm -rf spec/helpers

Executando o Rspec.
	$ time rspec --drb spec/
	$ rspec spec/
	
Criar um arquivo default do Rspec no projeto.
	$ mate .rspec
	--colour
	--drb
	
Executando o autoteste.
	$ autotest

Com o spork deixa o autotest/Rspec mais rápido porque cria vários forks
	$ spork --bootstrap
	$ spork
