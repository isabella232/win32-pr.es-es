---
title: IAgentBalloon GetFontItalic
description: IAgentBalloon GetFontItalic
ms.assetid: 03f40210-71b3-4488-9a44-5a9322db010a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e31c1a0e1e649e325e84d4a78eee087e102e8d1e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714179"
---
# <a name="iagentballoongetfontitalic"></a>IAgentBalloon::GetFontItalic

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetFontItalic(
   long * pbFontItalic  // address of variable for italic setting for 
);                      // font displayed in word balloon 
```

Indica si la fuente utilizada en un globo de palabras está en cursiva.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbFontItalic"></span><span id="pbfontitalic"></span><span id="PBFONTITALIC"></span>*pbFontItalic*
</dt> <dd>

La dirección de un valor que recibe **true** si la fuente es cursiva y **false** si no está en cursiva.

</dd> </dl>

El estilo de fuente utilizado en el globo de palabras de un carácter se define en el editor de caracteres del agente de Microsoft. No se puede cambiar por una aplicación. Sin embargo, el usuario puede invalidar la configuración de fuente para todos los caracteres a través de la hoja de propiedades del agente de Microsoft.

 

 




