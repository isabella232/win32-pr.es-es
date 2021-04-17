---
title: Propiedad de paso
description: Propiedad de paso
ms.assetid: 98b2ada3-93c6-4fa1-bf12-353eb229c30c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 998ee4bcf77878062425086d67066040f5d58421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419155"
---
# <a name="pitch-property"></a><span data-ttu-id="6eb8d-103">Propiedad de paso</span><span class="sxs-lookup"><span data-stu-id="6eb8d-103">Pitch Property</span></span>

<span data-ttu-id="6eb8d-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="6eb8d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="6eb8d-105"><span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="6eb8d-105"><span id="Description_"></span><span id="description_"></span><span id="DESCRIPTION_"></span>**Description**</span></span> 
</dt> <dd>

<span data-ttu-id="6eb8d-106">Devuelve un entero largo para la configuración de tono de salida de voz (TTS) del carácter especificado.</span><span class="sxs-lookup"><span data-stu-id="6eb8d-106">Returns a Long integer for the specified character's speech output (TTS) pitch setting.</span></span>

</dd> <dt>

<span data-ttu-id="6eb8d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="6eb8d-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="6eb8d-108">*agente ***. Caracteres ("*** CharacterID \* *"). Espacia**</span><span class="sxs-lookup"><span data-stu-id="6eb8d-108">*agent ***.Characters ("*** CharacterID\*\*\*").Pitch*\*</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6eb8d-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6eb8d-109">Remarks</span></span>

<span data-ttu-id="6eb8d-110">Esta propiedad solo se aplica a los caracteres configurados para la salida de TTS.</span><span class="sxs-lookup"><span data-stu-id="6eb8d-110">This property applies only to characters configured for TTS output.</span></span> <span data-ttu-id="6eb8d-111">Si el carácter no admite la salida de TTS, esta propiedad devuelve cero (0).</span><span class="sxs-lookup"><span data-stu-id="6eb8d-111">If the character does not support TTS output, this property returns zero (0).</span></span>

<span data-ttu-id="6eb8d-112">Aunque la aplicación no puede escribir este valor, puede incluir etiquetas **Pit** (Brea) en el texto de salida que aumentarán temporalmente el paso de un utterance determinado.</span><span class="sxs-lookup"><span data-stu-id="6eb8d-112">Although your application cannot write this value, you can include **Pit** (pitch) tags in your output text that will temporarily increase the pitch for a particular utterance.</span></span> <span data-ttu-id="6eb8d-113">Sin embargo, el uso de la etiqueta **Pit** para cambiar el paso no cambiará el valor de la propiedad de **paso** .</span><span class="sxs-lookup"><span data-stu-id="6eb8d-113">However, using the **Pit** tag to change the pitch will not change the **Pitch** property setting.</span></span> <span data-ttu-id="6eb8d-114">Para obtener más información, consulte [etiquetas de salida de voz](pit-tag.md).</span><span class="sxs-lookup"><span data-stu-id="6eb8d-114">For further information, see [Speech Output Tags](pit-tag.md).</span></span>

 

 




