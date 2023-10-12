# Trabalho realizado na Semana #3

## Identificação

- A CVE-2021-3156, é uma vulnerabilidade crítica que afeta os privilégios no Sudo, uma ferramenta comum que serve para administrar sistemas operancionais Unix/Linux.
- Trata-se de uma falha de segurança que afeta da versão 1.8.2 até à 1.8.31p2 e da 1.9.0 até à 1.9.5p1.
- A vulnerabilidade permitia que um utilizador conseguisse executar comandos com privilégios elevados 'root acess' o que podia levar à execução de um código qualquer no sistema.

## Catalogação

- A vulnerabilidade foi reportada dia 26 de janeiro de 2021 por um especialista em segurança da Qualys.
- Foi classificada com uma gravidade alta e com uma pontuação de 7.2 no sistema de pontuação CVSS.
-Foram lançados logo de seguida patches de segurança para corrigir a vulnerabilidade, porque a falha recebeu muita atenção da comunidade de cibersegurança e foi muito divulgada.

## Exploit

- O exploit para esta vulnerabilidade é relativamente simples, através de um comando para o sudo ele passa a alocar mais memória do que o suposto.
- O facto de ele alocar mais memória que o suposto faz com que possa ocorrer um heap overflow, fazendo com que o sudo pare de funcionar corretamente.
- Com o sudo a funcionar incorretamente era permitido ao utilizador te acesso a privilégios mais elevados no sistema.
- Tudo isto levava a que fosse possivel executar comandos maliciosos no sistema, instalar malwares ou criar backdoors que permitam ao invasor manter o acesso ao sistema.

## Ataques

- Várias organizações relataram tentativas de ataques bem sucedidas, incluindo distribuição de amostras de malware que usavam o exploit.
- Houve um caso em que o invasor conseguiu obter o acesso root num servidor Ubuntu, com o objetivo de aceder a informações confidenciais.
- As amostras de malware foram distribuidas em vários emails de phishing e podiam permitir que o invasor tivesse acesso ao sistema agora comprometido.
