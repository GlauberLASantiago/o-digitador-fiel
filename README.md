# O Digitador Fiel

Aplicativo educacional para acompanhar o processo de produção textual do estudante, valorizando a escrita realizada diretamente no editor, a revisão e a autoria.

## Acesse o aplicativo

[Abrir O Digitador Fiel](https://glauberlasantiago.github.io/o-digitador-fiel/)

## Objetivo pedagógico

O Digitador Fiel foi desenvolvido para apoiar atividades de produção textual em contextos educacionais. Em vez de considerar apenas o texto final, o aplicativo registra informações sobre o percurso de escrita, como tempo de atividade, quantidade de palavras, correções e tentativas de colagem.

Esses dados podem auxiliar a avaliação formativa do professor, mas não devem ser interpretados isoladamente como prova de aprendizagem, fraude ou uso de inteligência artificial.

## Principais recursos

- Editor de texto com negrito, itálico e sublinhado.
- Diferentes tamanhos de fonte.
- Listas numeradas e listas com marcadores.
- Suporte às teclas `Enter` e `Tab`.
- Buffer de digitação que preserva caracteres digitados rapidamente.
- Bloqueio de colagem e de arrastar texto para o editor.
- Limite máximo de 2.000 caracteres por texto.
- Contagem de palavras e caracteres.
- Cálculo aproximado de palavras por minuto (PPM).
- Registro do tempo ativo e das saídas da aba.
- Nome completo do aluno obrigatório para gerar o relatório.
- Campos opcionais para matrícula ou RA e disciplina.
- Quatro temas visuais.
- Relatório em PDF com o conteúdo submetido, identificação e telemetria.
- Código de verificação baseado em SHA-256 para detectar alterações.
- Verificador de relatórios integrado ao aplicativo.
- Botão para copiar o código de incorporação em Moodle e outros sites.

## Como usar

1. Informe o nome completo do estudante, que é obrigatório. A matrícula ou RA e a disciplina são opcionais.
2. Digite o texto diretamente no editor.
3. Utilize os controles de formatação quando necessário, respeitando o limite de 2.000 caracteres.
4. Aguarde o buffer terminar, caso ainda existam caracteres pendentes.
5. Clique em **Gerar texto/relatório**.
6. Entregue o PDF ao professor conforme as orientações da atividade.

## Verificação de um relatório

1. Abra o aplicativo e clique em **Verificar relatório**.
2. Copie do PDF o código de verificação e cole no campo indicado.
3. Cole também o conteúdo submetido.
4. Clique em **Verificar agora**.

O mecanismo SHA-256 permite verificar se o conteúdo e os dados associados ao relatório correspondem ao código apresentado. Ele detecta alterações, mas, por funcionar inteiramente no navegador e sem uma chave privada protegida, não equivale a uma assinatura digital emitida por uma autoridade ou servidor.

## Incorporar no Moodle ou em outro site

No cabeçalho do aplicativo, clique em **`</> Incorporar`**. O código será copiado automaticamente para a área de transferência, com comentários que indicam onde ele começa e termina.

Depois:

1. Abra o editor HTML do Moodle ou do site.
2. Cole o código copiado.
3. Salve a página e verifique se o `iframe` é permitido pela plataforma.

Algumas instalações do Moodle podem bloquear `iframe` por configuração de segurança. Nesse caso, o administrador da plataforma deverá autorizar a incorporação do endereço do aplicativo.

## Executar localmente

O projeto é composto por um único arquivo principal, `index.html`.

Você pode abri-lo diretamente no navegador ou executar um servidor web local. Uma opção simples, caso o Python esteja instalado, é:

```bash
python -m http.server 8765
```

Em seguida, acesse:

```text
http://127.0.0.1:8765/index.html
```

O carregamento inicial requer conexão com a internet porque as bibliotecas Quill e jsPDF são obtidas por CDN.

## Tecnologias utilizadas

- HTML, CSS e JavaScript
- [Quill](https://quilljs.com/) para edição e formatação de texto
- [jsPDF](https://github.com/parallax/jsPDF) para geração do relatório em PDF
- Web Crypto API para o cálculo SHA-256

## Privacidade

O aplicativo funciona no navegador. O texto e os dados informados não são enviados pelo próprio aplicativo a um servidor. O relatório é gerado localmente no dispositivo do usuário.

## Autoria e créditos

Desenvolvido pelo professor **Glauber Santiago — DAC/UFSCar**.

- [Página institucional](http://servidores.ufscar.br/glauber/)
- [Glauberia](https://glauberia.web.app/)
- [Aprenda Música Comigo](https://aprenda-musica-comigo.web.app/)
- [Grupo de Pesquisa Horizonte](https://grupohorizonte.ufscar.br/)

## Repositório

[github.com/GlauberLASantiago/o-digitador-fiel](https://github.com/GlauberLASantiago/o-digitador-fiel)
