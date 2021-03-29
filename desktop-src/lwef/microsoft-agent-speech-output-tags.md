---
title: Etiquetas de salida de voz del agente de Microsoft
description: Etiquetas de salida de voz del agente de Microsoft
ms.assetid: b7939974-bc54-4dd8-8e79-3ebd24e76215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d365d4837df3e3a5afb57c355e229f21ade0b5a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903508"
---
# <a name="microsoft-agent-speech-output-tags"></a>Etiquetas de salida de voz del agente de Microsoft

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

Los servicios del agente de Microsoft admiten la modificación de la salida de voz a través de etiquetas especiales insertadas en la cadena de texto de voz. Estas etiquetas le ayudan a cambiar las características de la expresión de salida del carácter.

Las etiquetas de salida de voz usan las siguientes reglas de sintaxis:

-   Todas las etiquetas comienzan y terminan con un carácter de barra diagonal inversa ( \) .
-   El carácter de barra diagonal inversa única no está habilitado dentro de una etiqueta. Para incluir un carácter de barra diagonal inversa en un parámetro de texto de una etiqueta, utilice una doble barra diagonal inversa ( \\ \) .
-   Las etiquetas no distinguen mayúsculas de minúsculas. Por ejemplo, \\ Pit \\ es igual que \\ Pit \\ .
-   Las etiquetas dependen del espacio en blanco. Por ejemplo, \\ RST \\ no es lo mismo que \\ RST \\ .

A menos que otra etiqueta especifique o modifique de otro modo, la salida de voz conservará la característica establecida por la etiqueta en el texto especificado en un solo método [**Speak**](speak-method.md) . La salida de voz se restablece automáticamente a través de los parámetros definidos por el usuario una vez completado un método **Speak** .

Algunas etiquetas incluyen cadenas entre comillas. En algunos lenguajes de programación, como Visual Basic Scripting Edition (VBScript) y Visual Basic, esto significa que puede que tenga que utilizar dos comillas para designar el parámetro de la etiqueta o concatenar un carácter de comilla doble como parte de la cadena. Este último se muestra en este Visual Basic ejemplo:


```
Agent1.Characters("Genie").Speak "This is \map=" + chr(34) + "Spoken text" _
+ chr(34) + "=" + chr(34) + "Balloon text" + chr(34) + "\."
```



Para C, C++ y Java™ programación, preceden a las barras diagonales inversas y comillas dobles con una barra diagonal inversa. Por ejemplo:


```
BSTR bszSpeak = SysAllocString(L"This is \\map=\"Spoken text\"=\"Balloon text\"\\");

pCharacter->Speak(bszSpeak, ......);
```



En el caso de los idiomas externos que admiten caracteres de juegos de caracteres de doble byte (DBCS), puede usar caracteres de doble byte para especificar parámetros de cadena. Sin embargo, use caracteres de un solo byte para todos los demás parámetros y caracteres que se usan para definir la etiqueta, incluida la propia etiqueta.

Se admiten las siguientes etiquetas:

-   [**Chr**](chr-tag.md)
-   [**CTX**](ctx-tag.md)
-   [**Empleado**](emp-tag.md)
-   [**LST**](lst-tag.md)
-   [**Conectarse**](map-tag.md)
-   [**Mrk**](mrk-tag.md)
-   [**Pau**](pau-tag.md)
-   [**Pozo**](pit-tag.md)
-   [**RST**](rst-tag.md)
-   [**DOCUP**](spd-tag.md)
-   [**Volumen**](vol-tag.md)

Las etiquetas están diseñadas principalmente para ajustar los resultados generados por texto a voz (TTS). Solo se pueden usar las etiquetas [**MRK**](mrk-tag.md) y [**map**](map-tag.md) con la salida de voz basada en archivos de sonido.

> [!Note]  
> El agente de Microsoft no admite todas las etiquetas documentadas en el SDK de Microsoft Speech. Los parámetros también pueden variar en función del motor TTS seleccionado. Puede establecer un motor TTS específico mediante [**TTSModeID**](ttsmodeid-property.md).

 

 

 




