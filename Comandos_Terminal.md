## Comandos Linux
sudo = Permissões especiais. <br/>
sudo su = Obter privilégios de super usuário. <br/>
sudo yum install java-1.8.0-openjdk-devel  = Installing OpenJDK 8 on Red Hat Enterprise Linux.<br/>
sudo shutdown now = Comando sudo para desligar instancia linux. <br/>
cd "nome da pasta"= Navegar pelo sistema de arquivos. <br/>
 <br/>
pwd = exibe caminho/pasta atual (print working directory) <br/>
ls = Listagem de arquivos. <br/>
ls -al = Listagem de todos os arquivos e diretórios com informações detalhadas como permissões, tamanho, proprietário, etc. <br/>
dir = Listagem de arquivos. <br/>
mkdir "nome da pasta" = Cria pasta no diretorio atual. <br/>
clear = Limpar terminal. <br/>
cls = Limpar terminal. <br/>
 <br/>
cat "nome do arquivo" = Permite que você exiba arquivos no formato padrão de tela, lista conteúdos do arquivo. <br/>
cat > /pasta/origem/arquivo.txt = Permite escrita dentro do arquivo.txt, Ctrl+D para finalizar e salvar. <br/>
more "nome do arquivo" = ler arquivos de texto. <br/>
 <br/>
cp /pasta/origem/arquivo1 /pasta/destino/ = Copia o arquivo1 e cola na pasta de destino mantendo o mesmo nome. <br/>
cp /pasta/origem/arquivo1 /pasta/destino/arquivo2 = Copia renomeando o arquivo1 para arquivo2. <br/>
sudo cp -R /pasta/origem/arquivo1 /pasta/destino/ <br/>
 <br/>
chmod 777 -R "nome do arquivo/pasta" = O comando chmod serve para alterar as permissões sobre determinado diretório ou arquivo. A Permissão 777 significa acesso total. Se um diretório tem permissão 777, qualquer usuário pode mexer naquele diretório a todos os diretórios e arquivos a partir do raíz (libera acesso para transferencia/cópia externa). <br/>
free -h = verifica memoria <br/>
<br/>
ping / telnet = Testar comunicação. Comando baseado em protocolo, tem como princípios uma série de procedimentos e regras que são definidos para padronizar a comunicação. <br/>
 <br/>
grep = Procura por trechos de texto (strings) dentro de arquivos ou diretórios [ grep "trecho a procurar" arquivo.txt ]. <br/>
	telnet | grep 8080 <br/>
	ls | grep "trecho a procurar" <br/>
	grep blue notepad.txt = busca blue dentro do arquivo .txt <br/>
wget "seguido pelo link de download do arquivo" = baixar arquivos da internet <br/>
cd "path" ; wget "url" = (Separação por ponto e vírgula) Executa os 2 comandos na sequencia.<br/>
cd /opt/yaman-jmeter/ ; mkdir massa ; chmod 777 -R massa<br/>
 <br/>
## Comandos Git
git clone <br/>
git add . <br/>
git commit -m"texto" <br/>
git push <br/>
 <br/>
**-c http.sslVerify=false** = Desabilita verificação SSL. <br/>
git -c http.sslVerify=false push <br/>
git -c http.sslVerify=false clone <br/>
 <br/>
git -c http.sslVerify=false clone https://git.com.br/caminho/do/repositorio.git <br/>
 <br/>
 <br/>
 
## Comandos Windows

### Abrir Executar (Win+R) ou Terminal Prompt:
**shutdown -s -t 3600** = Desliga windows após 3600 segundos (1h). <br/>


### Configuração "MaxUserPort" Portas Rede:
ERRO: JMeter - java.net.bindexception: Address already in use connect<br/>
<br/>
HKEY_ LOCAL_ MACHINE\SYSTEM\CurrentControlSet\Services\Tcpip\Parameters\MaxUserPort<br/>
Criar novo: DWORD<br/>
Name: maxuserport<br/>
VALUE DATA: 64000 DECIMAL<br/>
Ou<br/>
VALUE DATA: 32768 DECIMAL<br/>
<br/>

Máquina Windows: Limite 64000 decimal<br/>
Máquina Linux: Limite 65000 decimal (Por padrão já é configurado automaticamente no SO Linux)<br/>
