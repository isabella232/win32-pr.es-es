---
title: IAgentCharacter GetTTSPitch
description: IAgentCharacter GetTTSPitch
ms.assetid: b21ae1f1-daf6-42e5-9c52-f28722180021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dff1bb7999795cf27e29a7d064dd500b47bb419
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695482"
---
# <a name="iagentcharactergetttspitch"></a><span data-ttu-id="c56d1-103">IAgentCharacter::GetTTSPitch</span><span class="sxs-lookup"><span data-stu-id="c56d1-103">IAgentCharacter::GetTTSPitch</span></span>

<span data-ttu-id="c56d1-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c56d1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSPitch(
   long * pdwPitch  // address of variable for character TTS pitch
);
```

<span data-ttu-id="c56d1-105">Recupera la configuración del tono de salida de TTS del carácter.</span><span class="sxs-lookup"><span data-stu-id="c56d1-105">Retrieves the character's TTS output pitch setting.</span></span>

-   <span data-ttu-id="c56d1-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c56d1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c56d1-107"><span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*</span><span class="sxs-lookup"><span data-stu-id="c56d1-107"><span id="pdwPitch"></span><span id="pdwpitch"></span><span id="PDWPITCH"></span>*pdwPitch*</span></span>
</dt> <dd>

<span data-ttu-id="c56d1-108">Dirección de una variable que recibe la configuración de tono de TTS actual del carácter en hercios.</span><span class="sxs-lookup"><span data-stu-id="c56d1-108">Address of a variable that receives the character's current TTS pitch setting in Hertz.</span></span>

</dd> </dl>

<span data-ttu-id="c56d1-109">Aunque la aplicación no puede escribir este valor, puede incluir etiquetas de paso en el texto de salida que aumentarán temporalmente el paso de un utterance determinado.</span><span class="sxs-lookup"><span data-stu-id="c56d1-109">Although your application cannot write this value, you can include pitch tags in your output text that will temporarily increase the pitch for a particular utterance.</span></span> <span data-ttu-id="c56d1-110">Este método solo se aplica a los caracteres configurados para la salida de TTS.</span><span class="sxs-lookup"><span data-stu-id="c56d1-110">This method applies only to characters configured for TTS output.</span></span> <span data-ttu-id="c56d1-111">Si el motor de síntesis de voz (TTS) no está habilitado (o instalado) o el carácter no admite la salida de TTS, este método devuelve cero (0).</span><span class="sxs-lookup"><span data-stu-id="c56d1-111">If the speech synthesis (TTS) engine is not enabled (or installed) or the character does not support TTS output, this method returns zero (0).</span></span>

 

 




