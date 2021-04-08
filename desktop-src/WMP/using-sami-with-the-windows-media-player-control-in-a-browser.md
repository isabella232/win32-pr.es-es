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
# <a name="using-sami-with-the-windows-media-player-control-in-a-browser"></a><span data-ttu-id="161ac-114">Usar SAMI con el control de Media Player de Windows en un explorador</span><span class="sxs-lookup"><span data-stu-id="161ac-114">Using SAMI with the Windows Media Player Control in a Browser</span></span>

<span data-ttu-id="161ac-115">En lugar de crear un archivo SAMI para cada estilo de fuente o lenguaje, puede declarar diferentes clases de estilo en un archivo mediante scripting básico y el modelo de objetos de control de Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="161ac-115">Instead of creating a SAMI file for each font style or language, you can declare different style classes in one file by using basic scripting and the Windows Media Player control object model.</span></span> <span data-ttu-id="161ac-116">Puede crear controles personalizados que permitan al usuario elegir entre las distintas opciones de estilo y lenguaje.</span><span class="sxs-lookup"><span data-stu-id="161ac-116">You can create custom controls that enable the user to choose between the different style and language options.</span></span> <span data-ttu-id="161ac-117">Además, tiene un control completo sobre el diseño de la interfaz del reproductor y la personalización de cada función.</span><span class="sxs-lookup"><span data-stu-id="161ac-117">Furthermore, you have complete control over the design of the Player interface and the customization of each function.</span></span>

<span data-ttu-id="161ac-118">Para obtener información detallada sobre cómo insertar el control Media Player de Windows en una página web, vea [ejemplo simple de scripting en una página web](simple-example-of-scripting-in-a-web-page.md).</span><span class="sxs-lookup"><span data-stu-id="161ac-118">For detailed information about embedding the Windows Media Player control in a webpage, see [Simple Example of Scripting in a Web Page](simple-example-of-scripting-in-a-web-page.md).</span></span>

<span data-ttu-id="161ac-119">En el ejemplo de código siguiente se muestra cómo usar subtítulos cerrados con el control de Windows Media Player incrustado en una página web.</span><span class="sxs-lookup"><span data-stu-id="161ac-119">The following example code demonstrates how to use closed captions with the Windows Media Player control embedded in a webpage.</span></span> <span data-ttu-id="161ac-120">Incluye controles que permiten al usuario seleccionar el estilo y el idioma de la fuente.</span><span class="sxs-lookup"><span data-stu-id="161ac-120">It includes controls to allow the user to select font style and language.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="161ac-121">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="161ac-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="161ac-122">**Agregar subtítulos a medios digitales**</span><span class="sxs-lookup"><span data-stu-id="161ac-122">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> </dl>

 

 




