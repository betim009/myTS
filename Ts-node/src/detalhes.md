Tipos primitivos
Em JavaScript, um valor que não é um objeto nem uma função é de um tipo primitivo. Os mais comuns em JavaScript são:

string: uma sequência de quaisquer caracteres que pertençam ao padrão UTF-16 Unicode.
number: recebe valores numéricos, sejam eles inteiros ou frações.
boolean: recebe verdadeiro (true) ou falso (false).
null: representa a ausência intencional de um valor. É como dizer “aqui não há valor e isso é proposital”.
undefined: representa a ausência de um valor cujo tipo não foi explicitado no código.
Todos esses tipos primitivos têm um valor correspondente em TypeScript (com os mesmos nomes). Além deles, o TypeScript também oferece alguns tipos adicionais que não existem em JavaScript, mas que são muito úteis.

any
Esse tipo é um coringa. Ao utilizá-lo, você afirma “eu não sei qual é o tipo desse valor e não me importo com isso”. É uma forma de desabilitar as checagens de tipo e sinalizar para o TypeScript que você não quer que ele faça a verificação de tipagens para aquele valor.

Como qualquer coringa, é preciso usá-lo com responsabilidade - a tipagem estática do TypeScript está aí por um motivo, então não a dispense sem ter muita convicção do que está fazendo.

No implicit any
Quando o TypeScript, por alguma razão, não consegue identificar o tipo de um valor, o tipo any é inferido e atribuído ao valor de forma implícita.

É comum que a regra noImplicitAny esteja habilitada nas configurações do projeto (arquivo tsconfig.json), pois isso faz com que o compilador sinalize qualquer any implícito como erro. Ou seja, com essa regra, caso queiramos utilizar o any, somos obrigados a fazê-lo de forma explícita, afim de evitar seu uso irrestrito.

unknown
Muitas vezes, ao consumir APIs externas, por exemplo, não se sabe qual tipo de valor será retornado. Nesses casos, usar o tipo any poderia parecer uma escolha natural, mas o TypeScript oferece uma alternativa mais segura: o unknown!

Ao contrário do any, ao tipar um valor como unknown você está dizendo “eu não sei qual é o tipo desse valor, mas me importo bastante com isso”! Desse modo, o compilador obrigará você a fazer verificações que garantam o tipo correto do valor antes de usá-lo.

Anota aí 📝: O any e o unknown são tipos que existem em TypeScript mas eles não são considerados tipos primitivos. Isso porque eles não são tipos que existem em JavaScript, mas sim tipos adicionados pelo TypeScript.

O próximo passo, então, é como dizer ao TypeScript qual o tipo de uma variável!