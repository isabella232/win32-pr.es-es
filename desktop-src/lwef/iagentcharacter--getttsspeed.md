---
title: IAgentCharacter GetTTSSpeed
description: IAgentCharacter GetTTSSpeed
ms.assetid: 25526ef7-581f-489c-a299-bd3b5ac9ea61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 551074e1647cffc88e0b5f9f530cea931cd21ff9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419203"
---
# <a name="iagentcharactergetttsspeed"></a>IAgentCharacter::GetTTSSpeed

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

Recupera la configuración de la velocidad de salida TTS del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*
</dt> <dd>

Dirección de una variable que recibe la velocidad de salida del carácter en palabras por minuto.

</dd> </dl>

Aunque la aplicación no puede escribir este valor, puede incluir etiquetas de velocidad en el texto de salida que acelerarán temporalmente la salida de un utterance determinado.

Esta propiedad devuelve el valor actual de la velocidad de salida de habla para el carácter. En el caso de los caracteres que usan la salida de TTS, la propiedad devuelve la salida de TTS real para el carácter. Si TTS no está habilitado o el carácter no admite la salida de TTS, el valor refleja la configuración de usuario para la velocidad de salida.

 

 




