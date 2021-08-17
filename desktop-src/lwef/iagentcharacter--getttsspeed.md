---
title: IAgentCharacter GetTTSSpeed
description: IAgentCharacter GetTTSSpeed
ms.assetid: 25526ef7-581f-489c-a299-bd3b5ac9ea61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e7fbe4cbba7eaed22f49865e1a0f0994c512867fb6f233ef2bbfa01dcaafcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609875"
---
# <a name="iagentcharactergetttsspeed"></a>IAgentCharacter::GetTTSSpeed

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

Recupera la configuración de velocidad de salida de TTS del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*
</dt> <dd>

Dirección de una variable que recibe la velocidad de salida del carácter en palabras por minuto.

</dd> </dl>

Aunque la aplicación no puede escribir este valor, puede incluir etiquetas de velocidad en el texto de salida que acelerarán temporalmente la salida de una expresión determinada.

Esta propiedad devuelve la configuración de velocidad de salida de habla actual para el carácter. Para los caracteres que usan la salida de TTS, la propiedad devuelve la salida de TTS real para el carácter. Si TTS no está habilitado o el carácter no admite la salida de TTS, la configuración refleja la configuración del usuario para la velocidad de salida.

 

 




