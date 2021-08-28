---
title: IAgentCharacter GetEffectsOn
description: IAgentCharacter GetEffectsOn
ms.assetid: 11bc074e-7654-4a78-920e-acd56db52c98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f7133e41e4c291200feaf8fdb8ab3919cdb622ca927c155fc0941202fd555a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848645"
---
# <a name="iagentcharactergetsoundeffectson"></a>IAgentCharacter::GetEffectsOn

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetSoundEffectsOn(
   long * pbOn  // address of variable for sound effects setting 
);
```

Recupera si la configuración de efectos de sonido del carácter está habilitada.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*
</dt> <dd>

Dirección de una variable que recibe **True si** la configuración de efectos de sonido del carácter está habilitada, **False** si está deshabilitada.

</dd> </dl>

La configuración de efectos de sonido del carácter determina si los efectos de sonido compilados como parte del carácter se reproducen al reproducir una animación asociada. La configuración está sujeta a la configuración de efectos de sonido global del usuario [**en IAgentAudioOutputProperties::GetUsingEffects.**](iagentaudiooutputproperties--getusingsoundeffects.md)

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::SetEffectsOn**](iagentcharacter--setsoundeffectson.md), [ **IAgentAudioOutputProperties::GetUsing SoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




