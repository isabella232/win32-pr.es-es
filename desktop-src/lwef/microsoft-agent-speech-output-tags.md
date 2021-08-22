---
title: Etiquetas de salida de voz de Microsoft Agent
description: Etiquetas de salida de voz de Microsoft Agent
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27add35cc9be72a002cdb1a6fba60ef61d47cca61ef532a6d80fd6ed4a5794d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118747903"
---
# <a name="microsoft-agent-speech-output-tags"></a>Etiquetas de salida de voz de Microsoft Agent

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

Los servicios de Microsoft Agent admiten la modificación de la salida de voz a través de etiquetas especiales insertadas en la cadena de texto de voz. Estas etiquetas le ayudan a cambiar las características de la expresión de salida del carácter.

Las etiquetas de salida de voz usan las siguientes reglas de sintaxis:

-   Todas las etiquetas comienzan y terminan con un carácter de barra diagonal inversa ( \\ ).
-   El carácter de barra diagonal inversa única no está habilitado dentro de una etiqueta. Para incluir un carácter de barra diagonal inversa en un parámetro de texto de una etiqueta, use una doble barra diagonal inversa ( \\ \\ ).
-   Las etiquetas no tienen en cuenta las mayúsculas y minúsculas. Por ejemplo, \\ pit es igual que \\ \\ \\ PIT.
-   Las etiquetas dependen del espacio en blanco. Por ejemplo, \\ Rst \\ no es lo mismo que \\ \\ Rst.

A menos que otra etiqueta especifique o modifique lo contrario, la salida de voz conserva la característica establecida por la etiqueta dentro del texto especificado en un único [**método Speak.**](speak-method.md) La salida de voz se restablece automáticamente a través de los parámetros definidos por el usuario una vez completado un método **Speak.**

Algunas etiquetas incluyen cadenas entre comillas. Para algunos lenguajes de programación, como Visual Basic Scripting Edition (VBScript) y Visual Basic, es posible que tenga que usar dos comillas para designar el parámetro de la etiqueta o concatenar un carácter de comillas dobles como parte de la cadena. Este último ejemplo se muestra en Visual Basic ejemplo:


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



Para C, C++ y Java™ programación, preceda las barras diagonales inversas y las comillas dobles con una barra diagonal inversa. Por ejemplo:


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



Para los idiomas externos que admiten caracteres de juego de caracteres de doble byte (DBCS), puede usar caracteres de doble byte para especificar parámetros de cadena. Sin embargo, use caracteres de un solo byte para todos los demás parámetros y caracteres que se usan para definir la etiqueta, incluida la propia etiqueta.

Se admiten las siguientes etiquetas:

-   [**Chr**](chr-tag.md)
-   [**Ctx**](ctx-tag.md)
-   [**Emp**](emp-tag.md)
-   [**Lst**](lst-tag.md)
-   [**Mapa**](map-tag.md)
-   [**Mrk**](mrk-tag.md)
-   [**Pau**](pau-tag.md)
-   [**Hoyo**](pit-tag.md)
-   [**Rst**](rst-tag.md)
-   [**Spd**](spd-tag.md)
-   [**Vol**](vol-tag.md)

Las etiquetas están diseñadas principalmente para ajustar la salida generada por texto a voz (TTS). Solo se pueden usar las [**etiquetas**](map-tag.md) [**Mrk**](mrk-tag.md) y Map con una salida hablada basada en archivos de sonido.

> [!Note]  
> Microsoft Agent no admite todas las etiquetas documentadas en el SDK de Voz de Microsoft. Los parámetros también pueden variar en función del motor de TTS seleccionado. Puede establecer un motor de TTS específico mediante [**TTSModeID**](ttsmodeid-property.md).

 

 

 




