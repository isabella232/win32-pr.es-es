---
title: IAgentCharacter GetSoundEffectsOn
description: IAgentCharacter GetSoundEffectsOn
ms.assetid: 11bc074e-7654-4a78-920e-acd56db52c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a40f18a4fb8e7778c116c54391a7dc50e5267af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695483"
---
# <a name="iagentcharactergetsoundeffectson"></a><span data-ttu-id="13e28-103">IAgentCharacter::GetSoundEffectsOn</span><span class="sxs-lookup"><span data-stu-id="13e28-103">IAgentCharacter::GetSoundEffectsOn</span></span>

<span data-ttu-id="13e28-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="13e28-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetSoundEffectsOn(
   long * pbOn  // address of variable for sound effects setting 
);
```

<span data-ttu-id="13e28-105">Recupera si está habilitada la configuración de efectos sonoros del carácter.</span><span class="sxs-lookup"><span data-stu-id="13e28-105">Retrieves whether the character's sound effects setting is enabled.</span></span>

-   <span data-ttu-id="13e28-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="13e28-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="13e28-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span><span class="sxs-lookup"><span data-stu-id="13e28-107"><span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*</span></span>
</dt> <dd>

<span data-ttu-id="13e28-108">Dirección de una variable que recibe **true** si está habilitada la configuración de efectos sonoros del carácter, **false** si está deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="13e28-108">Address of a variable that receives **True** if the character's sound effects setting is enabled, **False** if disabled.</span></span>

</dd> </dl>

<span data-ttu-id="13e28-109">La configuración de efectos sonoros del carácter determina si se reproducen efectos sonoros compilados como parte del carácter al reproducir una animación asociada.</span><span class="sxs-lookup"><span data-stu-id="13e28-109">The character's sound effects setting determines whether sound effects compiled as a part of the character are played when you play an associated animation.</span></span> <span data-ttu-id="13e28-110">La configuración está sujeta a la configuración de efectos de sonido globales del usuario en [**IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span><span class="sxs-lookup"><span data-stu-id="13e28-110">The setting is subject to the user's global sound effects setting in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="13e28-111">Consulte también</span><span class="sxs-lookup"><span data-stu-id="13e28-111">See Also</span></span>

<span data-ttu-id="13e28-112">[**IAgentCharacter:: SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md), [ **IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span><span class="sxs-lookup"><span data-stu-id="13e28-112">[**IAgentCharacter::SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md), [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span></span>


 

 




