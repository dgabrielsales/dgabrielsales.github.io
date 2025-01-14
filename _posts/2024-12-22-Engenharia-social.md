
Engenharia social é uma das ferramentas mais poderosas no arsenal de um hacker. Em vez de explorar diretamente vulnerabilidades de sistemas, essa técnica se concentra na parte mais fraca da cadeia de segurança: **o ser humano**. Um dos métodos mais usados nesse contexto é a **clonagem de páginas de login fake**.

## O que é Clonagem de Páginas de Login Fake?

Clonar uma página de login consiste em criar uma réplica idêntica de uma página legítima, como a de redes sociais, e-commerce ou provedores de e-mail. O objetivo é enganar a vítima para que ela insira suas credenciais, que são enviadas diretamente ao atacante.

Por exemplo:
- Um atacante pode enviar um e-mail ou mensagem com um link que direciona a vítima para uma página falsa.
- Essa página falsa imita com perfeição a aparência de um site real, incluindo logotipos, fontes e até certificados HTTPS fraudulentos.

## Como Funciona na Prática?

1. **Engajamento Inicial**: O atacante usa técnicas de phishing para levar a vítima até a página clonada.
2. **Confiança Visual**: A página falsa é construída para parecer legítima, usando ferramentas para copiar o site original.
3. **Captura de Credenciais**: Quando a vítima insere suas informações, os dados são enviados para o servidor do atacante.
4. **Uso Malicioso**: As credenciais podem ser usadas para acessar contas ou realizar outras ações maliciosas.

## Ferramentas Comuns para Clonagem

SET (Social Engineering Toolkit), BeEF (Browser Exploitation Framework) e Zphisher, no meu caso usei o Zphisher para demonstrar. 



---


## Meu Caso de Teste - Zphisher

Com a intenção de conscientizar um determinado grupo de pessoas, pensei em algumas possibilidades de aplicar algo que pudesse ser minimamente convincente a fim de capturar informações confidenciais.

![Descrição da imagem](images/image01.png)

Usando a ferramenta Zphisher, criei páginas de login do Instagram. Temos 3 opções, e como o acesso seria fora da minha rede, optei por escolher a opção 3 (LocalXpose). Este cria um túnel de acesso para a página de login. Quando o alvo acessa o site e envia os dados nos campos de nome e senha, essas informações são enviadas ao servidor do atacante. A URL pode ser personalizada para ajudar o usuário a criar uma confiança maior. Por exemplo, podemos criar algo assim: “instagram.reels/dominio”. Em meu caso de teste, usei palavras contidas em um domínio oficial do Instagram, como a palavra “reels”, criando algo assim: “instagram.reels@is.gd/xxxxx”.


## Sobre o LocalXpose 

O LocalXpose é uma ferramenta que oferece um serviço de túnel reverso, permitindo expor de maneira segura um servidor local para a web. No contexto de um ataque de phishing, isso significa que você pode rodar uma página de login falsa em seu servidor local e usá-la para capturar informações de um usuário.

Quando o usuário acessa a página falsa e insere suas credenciais, o LocalXpose redireciona o tráfego para o servidor local, permitindo que você capture as informações inseridas, como nomes de usuário e senhas.


![Descrição da imagem](images/image02.png)

Como podemos ver, temos 3 URLs, sendo uma personalizada. Esta é a que visivelmente tem boas chances de ser confundida com uma possível URL oficial. Pegando a URL que leva para a página falsa, fiz algo assim e enviei no WhatsApp para um dos alvos do teste:


![Descrição da imagem](images/image03.png)

Sim, eu sei… para quem tem um mínimo de noção, isso parece óbvio. Mas acredite, o alvo caiu. E o pior: ele forneceu suas credenciais ao atacante sem sequer perceber. A ideia por trás disso é simples: o primeiro link, com o nome oficial do Instagram, não é clicável, mas ainda assim engana, criando a ilusão de ser legítimo.

## Como se Proteger?

1. **Verifique URLs**: Antes de inserir informações, sempre confira se a URL está correta e começa com `https://`.
2. **Evite Clicar em Links Desconhecidos**: Sempre desconfie de mensagens que pedem informações urgentes.
3. **Use Autenticação de Dois Fatores (2FA)**: Isso pode proteger sua conta mesmo que suas credenciais sejam comprometidas.
4. **Educação**: Ensine funcionários e colegas sobre os riscos da engenharia social.


## Conclusão
A engenharia social, como a clonagem de páginas falsas, mostra que, muitas vezes, os maiores riscos vêm do lado humano, e não da tecnologia em si. Mesmo com todas as ferramentas de segurança que temos, a melhor proteção é nossa atenção e cuidado ao navegar na web.

Com ferramentas como o Zphisher e o LocalXpose, vemos como é fácil enganar alguém e capturar dados. Mas o importante aqui é entender como esses ataques funcionam para saber se proteger. Sempre verifique os links, evite clicar em mensagens estranhas e, se possível, ative a autenticação de dois fatores.

No fim, a chave para se manter seguro online é estar sempre alerta e nunca parar de aprender. Quanto mais sabemos sobre como os ataques acontecem, mais preparados ficamos para evitar cair nessas armadilhas.

---


> **Nota:** 
Este post é estritamente para fins educacionais. O uso indevido das técnicas descritas aqui é ilegal e pode trazer consequências graves. O objetivo é aumentar a conscientização sobre os riscos de engenharia social e como as pessoas podem se proteger contra esses tipos de ataques. Nunca use essas técnicas para prejudicar ou manipular outras pessoas.



Fique seguro e continue aprendendo!  