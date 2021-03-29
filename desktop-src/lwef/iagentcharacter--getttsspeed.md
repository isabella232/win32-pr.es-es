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
# <a name="iagentcharactergetttsspeed"></a><span data-ttu-id="dc775-103">IAgentCharacter::GetTTSSpeed</span><span class="sxs-lookup"><span data-stu-id="dc775-103">IAgentCharacter::GetTTSSpeed</span></span>

<span data-ttu-id="dc775-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="dc775-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSSpeed(
   long * pdwSpeed  // address of variable for character TTS output speed
);
```

<span data-ttu-id="dc775-105">Recupera la configuración de la velocidad de salida TTS del carácter.</span><span class="sxs-lookup"><span data-stu-id="dc775-105">Retrieves the character's TTS output speed setting.</span></span>

-   <span data-ttu-id="dc775-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="dc775-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="dc775-107"><span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*</span><span class="sxs-lookup"><span data-stu-id="dc775-107"><span id="pdwSpeed"></span><span id="pdwspeed"></span><span id="PDWSPEED"></span>*pdwSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="dc775-108">Dirección de una variable que recibe la velocidad de salida del carácter en palabras por minuto.</span><span class="sxs-lookup"><span data-stu-id="dc775-108">Address of a variable that receives the output speed of the character in words per minute.</span></span>

</dd> </dl>

<span data-ttu-id="dc775-109">Aunque la aplicación no puede escribir este valor, puede incluir etiquetas de velocidad en el texto de salida que acelerarán temporalmente la salida de un utterance determinado.</span><span class="sxs-lookup"><span data-stu-id="dc775-109">Although your application cannot write this value, you can include speed tags in your output text that will temporarily speed up the output for a particular utterance.</span></span>

<span data-ttu-id="dc775-110">Esta propiedad devuelve el valor actual de la velocidad de salida de habla para el carácter.</span><span class="sxs-lookup"><span data-stu-id="dc775-110">This property returns the current speaking output speed setting for the character.</span></span> <span data-ttu-id="dc775-111">En el caso de los caracteres que usan la salida de TTS, la propiedad devuelve la salida de TTS real para el carácter.</span><span class="sxs-lookup"><span data-stu-id="dc775-111">For characters using TTS output, the property returns the actual TTS output for the character.</span></span> <span data-ttu-id="dc775-112">Si TTS no está habilitado o el carácter no admite la salida de TTS, el valor refleja la configuración de usuario para la velocidad de salida.</span><span class="sxs-lookup"><span data-stu-id="dc775-112">If TTS is not enabled or the character does not support TTS output, the setting reflects the user setting for output speed.</span></span>

 

 




