=============
SMS - O que é
=============

A necessidade
=============
Quando falamos em segurança e proteção de sistemas de computador, caímos sempre na pilha
de serviços para Autenticação, Autorização e Auditoria (Authentication, Authorization and
Audit), ou somente Serviços AAA, e mais simples ainda, A3S (AAA Services).

Conheça nossa ideia para serviços AAA `aqui <https://github.com/e5r/aaa-simplesample>`_.

.. code-block:: text

 #    /---\
 #   ( a1s )===$
 #    '---'    ~
 #             ~
 #             ~
 #    /---\    ~
 #   ( a2s )=$ ~
 #    '---'  ~ ~
 #           ~ ~
 #          /---\
 #         ( a2s )
 #          '---'

A1S - Authentication
--------------------
O Serviço de Autenticação (Authentication Service) é responsável por somente validar a
identidade dos indivíduos que solicitam interagir com os sistemas sob proteção, e deve
negar acesso as demais camadas da pilha caso isso não seja possível.

A2S - Authorization
-------------------
O Serviço de Autorização (Authorization Service) é responsável por informar a que
funcionalidades o indivíduo pode, e que nível de acesso o mesmo deve ter em cada sistemas
sob proteção.

A3S - Audit
-----------
O Serviço de Auditoria (Audit Service) é responsável por provê uma interface simples,
completa, abstrata e transparente para que os sistemas sob proteção possam comunicar a
ocorrência de eventos em suas dependências pelos indivíduos que interagem com eles.
Essa auditoria é totalmente desacoplada dos sistemas e pode existir até mesmo com
a remoção dos próprios sistemas. Isso garante o princípio da rastreabilidade total.

A proposta
==========
Tendo explanado brevemente sobre o conceito A3S, continuamos...

Uma das maiores preocupações com proteção de sistemas de computador é estabelecer um
mecanismo seguro de troca de mensagens entre esses componentes, e deles com os próprios
sistemas sob proteção, além da comunicação com os indivíduos que os acessa (pessoas ou
outros sistemas).

Devemos garantir que os dados trafegados, sejam íntegros tanto com verificações de
identificaão, senhas e contra-senhas, como também, garantir que essas identificações,
senhas e contra-senhas possam trafegar com segurança (para garantir a integridade) e
protegidas de espiões. Com isso entendemos que a segurança/proteção deve ser garantida
antes mesmo do indivíduo informar a primeira informação.

Para isso propomos o padrão SMS - Secure Messaging Session (Sessão de Troca de Mensagens
Seguras). Trata-se de um fluxo baseado em SSL independente de tecnologia de implementação
que pode ser usado para reforçar a segurança e proteção de sistemas de computadores.
Acreditamos ser ideal para aplicação em serviços de Intranet's corporativas.

`INDEX <../README.rst>`_
=====
1. O que é o SMS
2. `O problema do HTTPS <02_https_problem.rst>`_
3. `Criptografia Síncrona e Assíncrona <03_encryption.rst>`_
4. `A historinha do fluxo <04_the_history.rst>`_
5. `Regras do fluxo <05_rules.rst>`_
6. `A especificação <06_specification.rst>`_
