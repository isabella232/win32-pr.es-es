---
title: Usar SAMI con el control de Media Player de Windows en un explorador
description: Usar SAMI con el control de Media Player de Windows en un explorador
ms.assetid: 41906e57-adaa-4df7-86ba-19b8a757e216
keywords:
- Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Modelo de objetos de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- modelo de objetos, intercambio de multimedia accesible sincronizado (SAMI)
- Windows Media Player Mobile, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX de Windows Media Player, intercambio de multimedia accesible sincronizado (SAMI)
- Control ActiveX móvil de Windows Media Player, intercambio de contenido multimedia accesible sincronizado (SAMI)
- Control ActiveX, intercambio de multimedia accesible sincronizado (SAMI)
- Intercambio de contenido multimedia accesible sincronizado (SAMI), archivos
- SAMI (intercambio de multimedia accesible sincronizado), archivos
- Intercambio de multimedia accesible sincronizado (SAMI), código de ejemplo
- SAMI (intercambio de multimedia accesible sincronizado), código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b651c3af117942d56ffc5334323913d26cdf6f99
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994565"
---
# <a name="using-sami-with-the-windows-media-player-control-in-a-browser"></a>Usar SAMI con el control de Media Player de Windows en un explorador

En lugar de crear un archivo SAMI para cada estilo de fuente o lenguaje, puede declarar diferentes clases de estilo en un archivo mediante scripting básico y el modelo de objetos de control de Windows Media Player. Puede crear controles personalizados que permitan al usuario elegir entre las distintas opciones de estilo y lenguaje. Además, tiene un control completo sobre el diseño de la interfaz del reproductor y la personalización de cada función.

Para obtener información detallada sobre cómo insertar el control Media Player de Windows en una página web, vea [ejemplo simple de scripting en una página web](simple-example-of-scripting-in-a-web-page.md).

En el ejemplo de código siguiente se muestra cómo usar subtítulos cerrados con el control de Windows Media Player incrustado en una página web. Incluye controles que permiten al usuario seleccionar el estilo y el idioma de la fuente.


```C++
<HTML>
<HEAD>

<SCRIPT>
  // The following variable is used to prevent multiple initialization.
  var initialized = false;
  // The following function populates the select boxes.
  // It is called the first time the media file is opened.
  // Before then, the SAMI settings cannot be retrieved.
  function initialize() {
    var newOption;
    for (var i = 0; i < Player.closedCaption.SAMILangCount; i++) {
      newOption = document.createElement("OPTION");
      newOption.text = Player.closedCaption.getSAMILangName(i);
      newOption.value = newOption.text;
      CCLang.options.add(newOption);
    }
    for (var i = 0; i < Player.closedCaption.SAMIStyleCount; i++) {
      newOption = document.createElement("OPTION");
      newOption.text = Player.closedCaption.getSAMIStyleName(i);
      newOption.value = newOption.text;
      CCStyle.options.add(newOption);
    }
    initialized = true;
  }
</SCRIPT>

<!-- The following script code runs when the page is fully loaded. -->
<SCRIPT for="window" event="onload()">
  Player.closedCaption.captioningID = "captions";
  Player.closedCaption.SAMIFileName = "https://www.proseware.com/Media/seattle.smi";
  // The digital media file will open automatically, after which
  // the OpenStateChange event (handled below) will fire.
  Player.URL = "https://www.proseware.com/Media/seattle.wmv";
</SCRIPT>

<!-- The following script code runs when a media file is opened. -->
<SCRIPT for="Player" event="OpenStateChange(NewState)">
  // The first time this event fires, the Player stops and the 
  // initialize function is called. This allows the user to 
  // select a language and style before viewing the file.
  if (13 == NewState && !initialized) {
    Player.controls.stop();
    initialize();
  }
</SCRIPT>

</HEAD>
<BODY>

<OBJECT 
  ID="Player" 
  classID="clsid:6BF52A52-394A-11d3-B153-00C04F79FAA6"
  height="200" 
  width="250"
>
</OBJECT>

<TABLE height="100" width="250" border="3" bordercolor="blue">
  <TR align="center">
    <TD bgcolor="white">
      <SELECT ID="CCLang" onClick="Player.closedCaption.SAMILang = value"></SELECT>
      <SELECT ID="CCStyle" onClick="Player.closedCaption.SAMIStyle = value"></SELECT>
    </TD>
  </TR>
  <TR height="75">
    <TD bgcolor="blue">
      <DIV id="captions"></DIV>
    </TD>
  </TR>
</TABLE>

</BODY>
</HTML>

```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Agregar subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




