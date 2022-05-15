# Darling Bot
<a href="https://youtube.com/channel/UCGGHT-j0Xr96O15yDcBQa7g">tio Momonga</a>
<br>Esse bot foi feito com a biblioteca <a href="https://www.npmjs.com/package/@adiwajshing/baileys">@adiwajshing/Baileys</a>

# <h2>Instalação</h2>
<h3>Android</h3>
tutorial completo <a href="https://youtu.be/rS4KqcyeMNE">aqui</a>

# <h2>Enviando Mensagens</h2>

<h4>mensagem de texto</h4>
<span>send({<br>
type: "msg",<br>
content: "Olá mundo"<br>
})</span><br><br>
Parâmetros opcionais:<br>
<span>//Agir como humano?<br>
likeHuman: true || false <br><br>
//mensagem respondida<br>
quoted: quo("Olá mundo") || mek<br><br>
// mensagem encaminhada?<br>
forward: true || false<br><br>
// quantas vezes a mensagem foi encaminhada<br>
forwardScore: 999<br><br></span>

<h4>mensagem de imagem</h4>
<span>
send({<br>
type: "img",<br>
caption: "Olá mundo",<br>
file: "https://someimage.jpeg"<br>
})<br><br>
</span>

<h4>mensagem de vídeo</h4>
<span>
send({<br>
type: "vid",<br>
file: "./lib/media/vid/teste.mp4",<br>
caption: "Olá mundo!"
})<br><br>
</span>

<h4>mensagem de gif</h4>
<span>
send({<br>
type: "gif",<br>
file: "./lib/media/vid/teste.mp4",<br>
caption: "Olá mundo!"
})<br><br>
</span>

<h4>mensagem de áudio</h4>
<span>
send({<br>
type: "aud",<br>
file: "./lib/media/aud/teste.mp3",<br>
likeHuman: true<br>
})<br><br>
</span>

<h4>mensagem de botões</h4>
<span>
let buttonOptions = [<br>
{buttonId: "!id1",<br>
buttonText: {displayText: "Button 1"}, type: 1},<br>

{buttonId: "!id2",<br>
buttonText: {displayText: "Button 2"}, type: 1},<br>

{buttonId: "!id3",<br>
buttonText: {displayText: "Button 3"}, type: 1}<br>
];<br>

send({<br>
type: "but",<br>
content: "Legenda",<br>
footer: "descrição",<br>
buttonOptions: buttonOptions<br>
});<br><br>
</span>

<h4>mensagem de template</h4>
<span>
let templateOptions = [<br>
{index: 1, urlButton: {displayText: "Inscreva-se no meu canal!", url: "https://youtube.com/channel/UCGGHT-j0Xr96O15yDcBQa7g"}},<br>
{index: 2, callButton: {displayText: "Ligue para mim!", phoneNumber: "+99 (99) 99999999999"}},<br>
{index: 3, quickReplyButton: {displayText: "botão 1", id: `${PREFIX}id1`}},<br>
];<br>

send({<br>
type: "temp",<br>
content: "Descrição",<br>
footer: "legenda",<br>
buttonOptions: templateOptions<br>
});<br><br>
</span>

# <h2>Ações de grupo</h2>
<h4>adicionando membros</h4>
groupAction({<br>
type: "add",<br>
who: "55479999999@s.whatsapp.net"<br>
})<br><br>

<h4>removendo membros</h4>
groupAction({<br>
type: "remove",<br>
who: "55479999999@s.whatsapp.net"<br>
})<br><br>

<h4>promovendo a admin</h4>
groupAction({<br>
type: "promote",<br>
who: "55479999999@s.whatsapp.net"<br>
})<br><br>

<h4>despromover admin</h4>
groupAction({<br>
type: "demote",<br>
who: "55479999999@s.whatsapp.net"<br>
})<br><br>
