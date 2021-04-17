---
title: IAgentCharacter SetSoundEffectsOn
description: IAgentCharacter SetSoundEffectsOn
ms.assetid: 141dd9a8-5fd8-42c6-880a-856c61cb8940
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a454a6ebeecc763cb7e5a964bb1f2897df6c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105714209"
---
# <a name="iagentcharactersetsoundeffectson"></a><span data-ttu-id="758f8-103">IAgentCharacter::SetSoundEffectsOn</span><span class="sxs-lookup"><span data-stu-id="758f8-103">IAgentCharacter::SetSoundEffectsOn</span></span>

<span data-ttu-id="758f8-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="758f8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

<span data-ttu-id="758f8-105">Determina si se reproducen los efectos de sonido del carácter.</span><span class="sxs-lookup"><span data-stu-id="758f8-105">Determines whether the character's sound effects are played.</span></span>

-   <span data-ttu-id="758f8-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="758f8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="758f8-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Despedida*</span><span class="sxs-lookup"><span data-stu-id="758f8-107"><span id="bOn"></span><span id="bon"></span><span id="BON"></span>*bOn*</span></span>
</dt> <dd>

<span data-ttu-id="758f8-108">Configuración de efectos de sonido.</span><span class="sxs-lookup"><span data-stu-id="758f8-108">Sound effects setting.</span></span> <span data-ttu-id="758f8-109">Si este parámetro es **true**, los efectos sonoros de las animaciones se reproducirán cuando se reproduzca la animación. Si **es false**, no se reproducen los efectos sonoros.</span><span class="sxs-lookup"><span data-stu-id="758f8-109">If this parameter is **True**, the sound effects for animations are played when the animation plays; if **False**, sound effects are not played.</span></span>

</dd> </dl>

<span data-ttu-id="758f8-110">Esta configuración determina si se reproducen efectos sonoros compilados como parte del carácter al reproducir una animación asociada.</span><span class="sxs-lookup"><span data-stu-id="758f8-110">This setting determines whether sound effects compiled as a part of the character are played when you play an associated animation.</span></span> <span data-ttu-id="758f8-111">La configuración de esta propiedad se aplica a todos los clientes del carácter.</span><span class="sxs-lookup"><span data-stu-id="758f8-111">This property's setting applies to all clients of the character.</span></span> <span data-ttu-id="758f8-112">La configuración también está sujeta a la configuración de efectos de sonido globales del usuario en [**IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span><span class="sxs-lookup"><span data-stu-id="758f8-112">The setting is also subject to the user's global sound effects setting in [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="758f8-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="758f8-113">See Also</span></span>

<span data-ttu-id="758f8-114">[**IAgentCharacter:: GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [ **IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span><span class="sxs-lookup"><span data-stu-id="758f8-114">[**IAgentCharacter::GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [**IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)</span></span>


 

 




