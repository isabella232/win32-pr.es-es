---
title: Propiedad Speed
description: Propiedad Speed
ms.assetid: 43d0480b-d3a5-4992-a2a5-80eba37221e4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24738ac17d7efac45f2aefe7e4beb5ec018915a0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704623"
---
# <a name="speed-property"></a><span data-ttu-id="990c3-103">Propiedad Speed</span><span class="sxs-lookup"><span data-stu-id="990c3-103">Speed Property</span></span>

<span data-ttu-id="990c3-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="990c3-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="990c3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="990c3-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="990c3-106">Devuelve un entero largo que especifica la velocidad actual de la salida de voz del carácter.</span><span class="sxs-lookup"><span data-stu-id="990c3-106">Returns a Long integer that specifies the current speed of the character's speech output.</span></span>

</dd> <dt>

<span data-ttu-id="990c3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="990c3-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="990c3-108">*agente ***. Caracteres ("*** CharacterID \* *"). Rápidas**</span><span class="sxs-lookup"><span data-stu-id="990c3-108">*agent ***.Characters ("*** CharacterID\*\*\*").Speed*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="990c3-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="990c3-109">Remarks</span></span>

<span data-ttu-id="990c3-110">Esta propiedad devuelve el valor actual de la velocidad de salida de habla para el carácter.</span><span class="sxs-lookup"><span data-stu-id="990c3-110">This property returns the current speaking output speed setting for the character.</span></span> <span data-ttu-id="990c3-111">En el caso de los caracteres que usan la salida de TTS, la propiedad devuelve el valor de salida de TTS real para el carácter.</span><span class="sxs-lookup"><span data-stu-id="990c3-111">For characters using TTS output, the property returns the actual TTS output setting for the character.</span></span> <span data-ttu-id="990c3-112">Si TTS no está habilitado o el carácter no admite la salida de TTS, el valor refleja la configuración de usuario para la velocidad de salida.</span><span class="sxs-lookup"><span data-stu-id="990c3-112">If TTS is not enabled or the character does not support TTS output, the setting reflects the user setting for output speed.</span></span>

<span data-ttu-id="990c3-113">Aunque la aplicación no puede escribir este valor, puede incluir etiquetas **SPD** (Speed) en el texto de salida que acelerarán temporalmente la salida de un utterance determinado.</span><span class="sxs-lookup"><span data-stu-id="990c3-113">Although your application cannot write this value, you can include **Spd** (speed) tags in your output text that will temporarily speed up the output for a particular utterance.</span></span> <span data-ttu-id="990c3-114">Sin embargo, el uso de la etiqueta **SPD** para cambiar la salida de voz del carácter no afecta al valor de la propiedad **Speed** .</span><span class="sxs-lookup"><span data-stu-id="990c3-114">However, using the **Spd** tag to change the character's spoken output does not affect the **Speed** property setting.</span></span> <span data-ttu-id="990c3-115">Para obtener más información, consulte [etiquetas de salida de voz](microsoft-agent-speech-output-tags.md).</span><span class="sxs-lookup"><span data-stu-id="990c3-115">For further information, see [Speech Output Tags](microsoft-agent-speech-output-tags.md).</span></span>

 

 




