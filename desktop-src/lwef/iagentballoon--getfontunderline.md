---
title: IAgentBalloon GetFontUnderline
description: IAgentBalloon GetFontUnderline
ms.assetid: 19886e94-8095-4650-bd88-34ea9d96ddaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325f383aa76c55068ca7244b4ce0f822602651fa196ee336060fcc21fe3ab068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962365"
---
# <a name="iagentballoongetfontunderline"></a>IAgentBalloon::GetFontUnderline

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetFontUnderline(
   long * pbFontUnderline  // address of variable for underline setting
);                         // for font displayed in word balloon 
```

Indica si la fuente usada en un globo de palabras tiene el estilo de subrayado establecido.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbFontUnderline"></span><span id="pbfontunderline"></span><span id="PBFONTUNDERLINE"></span>*pbFontUnderline*
</dt> <dd>

Dirección de un valor que recibe **True** si se establece el estilo de subrayado de fuente y **False** si no es así.

</dd> </dl>

El estilo de fuente utilizado en un globo de palabras de caracteres se define en el Editor de caracteres de Microsoft Agent. Una aplicación no puede cambiarla. Sin embargo, el usuario puede invalidar la configuración de fuente de todos los caracteres mediante la hoja de propiedades de Microsoft Agent.

 

 




