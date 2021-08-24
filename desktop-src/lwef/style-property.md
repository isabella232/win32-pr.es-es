---
title: Propiedad Style
description: Propiedad Style
ms.assetid: f01d7d51-8a16-4265-b9b7-93b64f4984e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37196aead474c5364c7a94780686707b74bab0f4c4831381cf4c40e47e350e17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715885"
---
# <a name="style-property"></a>Propiedad Style

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descripción**
</dt> <dd>

Devuelve o establece el estilo de salida del globo de palabras del carácter.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintaxis**
</dt> <dd>

*agent.***Characters("**_CharacterID_*_"). Estilo de_ *  \[  =  *Balloon.Style*\]



| Parte    | Descripción                                                                                                                                                                                                                                                                       |
|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Estilo* | Entero que representa el estilo de salida del globo. La configuración de estilo es un campo de bits con bits correspondientes a: globo (bit 0), tamaño a texto (bit 1), ocultación automática (bit 2), ritmo automático (bit 3), número de caracteres por línea (bits 16-23) y número de líneas (bits 24-31). |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Cuando el bit de estilo de globo se establece en 1, la palabra globo aparece cuando se usa un método [**Speak**](https://www.bing.com/search?q=**Speak**) o [**Think,**](think-method.md) a menos que el usuario invalide esta configuración en la hoja de propiedades de Microsoft Agent. Cuando se establece en 0, no aparece un globo.

Cuando el bit de estilo de tamaño a texto se establece en 1, la palabra globo ajusta automáticamente el tamaño del globo al tamaño actual del texto de la instrucción [**Speak**](https://www.bing.com/search?q=**Speak**) o [**Think.**](think-method.md) Cuando se establece en 0, el alto del globo se basa en la configuración de la propiedad [**NumberOfLines.**](numberoflines-property.md) Si este bit de estilo se establece en 1 e intenta establecer la **propiedad NumberOfLines,** el Agente genera un error.

Cuando el bit de estilo de ocultación automática está establecido en 1, la palabra globo se oculta automáticamente cuando se completa la salida hablada. Cuando se establece en 0, el globo permanece mostrado hasta la siguiente llamada [**a Speak**](https://www.bing.com/search?q=**Speak**) o [**Think,**](think-method.md) el carácter está oculto o el usuario hace clic o arrastra el carácter.

Cuando el bit de estilo de ritmo automático se establece en 1, la palabra globo marca el ritmo de la salida en función de la velocidad de salida actual, por ejemplo, una palabra a la vez. Cuando la salida supera el tamaño del globo, el texto anterior se desplaza automáticamente. Cuando se establece en 0, todo el texto incluido en una instrucción [**Speak**](https://www.bing.com/search?q=**Speak**) o [**Think**](think-method.md) se muestra a la vez.

Para recuperar solo el valor de los cuatro bits inferiores, **y** el valor devuelto por **Style** con 255. Para establecer un valor de bit, **o** bien el valor devuelto con el valor de los bits que desea establecer. Para desactivar un bit, **y** el valor devuelto con el complemento de uno del bit:


```
   Const BalloonOn = 1

   ' Turn the word balloon off
   Genie.Balloon.Style = Genie.Balloon.Style And (Not BalloonOn)
   Genie.Speak "No balloon"

   ' Turn the word balloon on
   Genie.Balloon.Style = Genie.Balloon.Style Or BalloonOn
   Genie.Speak "Balloon"
```



La **propiedad Style** también devuelve el número de caracteres por línea en el byte inferior de la palabra superior y el número de líneas en el byte superior de la palabra superior. Aunque esto se puede leer más fácilmente mediante las propiedades [**CharsPerLine**](charsperline-property.md) y [**NumberOfLines,**](numberoflines-property.md)la propiedad **Style** también permite establecer esos valores.

Por ejemplo, para cambiar el número de líneas, borre los bits 24 a 31 con una operación **LÓGICA AND** antes de establecer el nuevo valor como el producto del nuevo valor por 2^24, agregado al valor existente de la **propiedad Style.**


```
   ' Set the number of lines to 4
   Genie.Balloon.Style = (Genie.Balloon.Style <b>AND</b> &amp;H00FFFFFF) + (4*(2^24))
```



Para establecer el número de caracteres por línea, borre los bits 16 a 23 con una operación **LÓGICA AND** antes de establecer el nuevo valor como producto del nuevo valor por 2^16, agregado al valor existente de la propiedad Style.


```
   ' Set the number of characters per line to 16
   Genie.Balloon.Style = (Genie.Balloon.Style AND &amp;HFF00FFFF) + (16*(2^16))
```



La **propiedad Style** se puede establecer incluso si el usuario ha deshabilitado la presentación en globo mediante la hoja de propiedades de Microsoft Agent. Sin embargo, los valores para el número de líneas deben estar entre 1 y 128 y los caracteres numéricos por línea deben estar entre 8 y 255. Si proporciona un valor no válido para la **propiedad Style,** el Agente producirá un error.

Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.

Los valores predeterminados de estos bits de estilo se basan en su configuración cuando el carácter se compila con el Editor de caracteres de Microsoft Agent.

 

 




