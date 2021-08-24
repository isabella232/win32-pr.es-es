---
title: IAgentCharacter SetSoundEffectsOn
description: IAgentCharacter SetSoundEffectsOn
ms.assetid: 141dd9a8-5fd8-42c6-880a-856c61cb8940
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71abb6adebf09182d4329202e77355e7dc365899291995e97eca66305a00ab94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725025"
---
# <a name="iagentcharactersetsoundeffectson"></a>IAgentCharacter::SetSoundEffectsOn

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

Determina si se reproducen los efectos de sonido del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Bon*
</dt> <dd>

Configuración de efectos de sonido. Si este parámetro es **True**, los efectos de sonido de las animaciones se reproducen cuando se reproduce la animación; si **es False**, no se reproducen los efectos de sonido.

</dd> </dl>

Esta configuración determina si los efectos de sonido compilados como parte del carácter se reproducen cuando se reproduce una animación asociada. La configuración de esta propiedad se aplica a todos los clientes del carácter. La configuración también está sujeta a la configuración de efectos de sonido global del usuario [**en IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [ **IAgentAudioOutputProperties::GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




