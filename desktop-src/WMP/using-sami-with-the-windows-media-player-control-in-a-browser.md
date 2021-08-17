---
title: Uso de SAMI con Reproductor de Windows Media Control en un explorador
description: Uso de SAMI con Reproductor de Windows Media Control en un explorador
ms.assetid: 41906e57-adaa-4df7-86ba-19b8a757e216
keywords:
- Reproductor de Windows Media,Synchronized Accessible Media Interchange (SAMI)
- Reproductor de Windows Media modelo de objetos, Intercambio multimedia accesible sincronizado (SAMI)
- modelo de objetos, intercambio multimedia accesible sincronizado (SAMI)
- Reproductor de Windows Media Intercambio multimedia accesible móvil y sincronizado (SAMI)
- Reproductor de Windows Media ActiveX control, Intercambio multimedia accesible sincronizado (SAMI)
- Reproductor de Windows Media Control ActiveX móvil, intercambio multimedia accesible sincronizado (SAMI)
- ActiveX control,Intercambio multimedia accesible sincronizado (SAMI)
- Intercambio multimedia accesible sincronizado (SAMI),files
- SAMI (intercambio multimedia accesible sincronizado), archivos
- Intercambio multimedia accesible sincronizado (SAMI), código de ejemplo
- SAMI (intercambio de medios accesible sincronizado),código de ejemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d277f2849e6036d85bc8c03940a7dbd59df8b81083ca88240ebd68be768fde9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134348"
---
# <a name="using-sami-with-the-windows-media-player-control-in-a-browser"></a>Uso de SAMI con Reproductor de Windows Media Control en un explorador

En lugar de crear un archivo SAMI para cada estilo de fuente o lenguaje, puede declarar clases de estilo diferentes en un archivo mediante el scripting básico y el modelo de objetos Reproductor de Windows Media control. Puede crear controles personalizados que permitan al usuario elegir entre las distintas opciones de estilo y lenguaje. Además, tiene un control completo sobre el diseño de la interfaz player y la personalización de cada función.

Para obtener información detallada sobre cómo insertar el control Reproductor de Windows Media en una página web, vea Ejemplo simple de [scripting en una página web](simple-example-of-scripting-in-a-web-page.md).

En el código de ejemplo siguiente se muestra cómo usar subtítulos con el control Reproductor de Windows Media insertado en una página web. Incluye controles para permitir al usuario seleccionar el estilo de fuente y el idioma.


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

[**Adición de subtítulos a medios digitales**](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




