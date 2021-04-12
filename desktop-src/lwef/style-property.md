---
title: Propiedad de estilo
description: Propiedad de estilo
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 024d46dd7f7ce0e2fdc16b8b17f9074b1eef30c0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357121"
---
# <a name="style-property"></a>Propiedad de estilo

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**
</dt> <dd>

Devuelve o establece el estilo de salida de globo de palabra del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**
</dt> <dd>

*agente. ***Caracteres ("*** CharacterID * *"). Estilo de globo. Style* *  \[  =  \]



| Parte    | Descripción                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Estilo* | Entero que representa el estilo de salida del globo. La configuración de estilo es un campo de bits con bits que corresponden a: globo-sobre (bit 0), tamaño a texto (bit 1), ocultación automática (bit 2), velocidad automática (bit 3), número de caracteres por línea (bits 16-23) y número de líneas (bits 24-31). |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Cuando el bit de estilo de globo está establecido en 1, el globo de palabras aparece cuando se [**usa un método**](https://www.bing.com/search?q=**Speak**) de lectura o de [**reflexión**](think-method.md) , a menos que el usuario Invalide este valor en la hoja de propiedades del agente de Microsoft. Cuando se establece en 0, no aparece un globo.

Cuando el bit de estilo de tamaño a texto se establece en 1, el globo de palabras ajusta automáticamente el alto del globo al tamaño actual del texto para la [**instrucción de lectura o de**](https://www.bing.com/search?q=**Speak**) [**reflexión**](think-method.md) . Cuando se establece en 0, el alto del globo se basa en el valor de la propiedad [**NumberOfLines**](numberoflines-property.md) . Si este bit de estilo se establece en 1 y se intenta establecer la propiedad **NumberOfLines** , el agente genera un error.

Cuando el bit de estilo de ocultación automática está establecido en 1, el globo de palabras se oculta automáticamente cuando se completa la salida de voz. Cuando se establece en 0, el globo sigue mostrándose hasta la siguiente llamada de [**hablar**](https://www.bing.com/search?q=**Speak**) o [**pensar**](think-method.md) , el carácter está oculto o el usuario hace clic en el carácter o lo arrastra.

Cuando el bit de estilo auto-Pace está establecido en 1, el globo de palabras acelera la salida en función de la tasa de salida actual, por ejemplo, una palabra a la vez. Cuando la salida supera el tamaño del globo, el texto anterior se desplaza automáticamente. Cuando se establece en 0, todo el texto incluido en una instrucción [**Speak**](https://www.bing.com/search?q=**Speak**) o de [**reflexión**](think-method.md) se muestra a la vez.

Para recuperar solo el valor de los cuatro bits inferiores **y** el valor devuelto por el **estilo** con 255. Para establecer un valor de bit **o** el valor devuelto con el valor de los bits que desea establecer. Para desactivar un bit **y** el valor devuelto con uno de los complementos del bit:


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



La propiedad de **estilo** también devuelve el número de caracteres por línea en el byte inferior de la palabra superior y el número de líneas en el byte alto de la palabra superior. Aunque esto se puede leer más fácilmente mediante las propiedades [**CharsPerLine**](charsperline-property.md) y [**NumberOfLines**](numberoflines-property.md), la propiedad **Style** también permite establecer esos valores.

Por ejemplo, para cambiar el número de líneas, desactive los bits 24 a 31 con una operación **and** lógica antes de establecer el nuevo valor como el producto del nuevo valor las horas 2 ^ 24, agregados al valor existente de la propiedad **Style** .


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



Para establecer el número de caracteres por línea, desactive los bits 16 a 23 con una operación **and** lógica antes de establecer el nuevo valor como el producto del nuevo valor las veces 2 ^ 16, agregados al valor existente de la propiedad Style.


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



La propiedad de **estilo** se puede establecer incluso si el usuario ha deshabilitado la presentación de globos mediante la hoja de propiedades de Microsoft Agent. Sin embargo, los valores para el número de líneas deben estar entre 1 y 128 y el número de caracteres por línea debe estar entre 8 y 255. Si proporciona un valor no válido para la propiedad **Style** , el agente producirá un error.

Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

Los valores predeterminados para estos bits de estilo se basan en su configuración cuando el carácter se compila con el editor de caracteres del agente de Microsoft.

 

 




