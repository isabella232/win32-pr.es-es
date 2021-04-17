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
# <a name="iagentcharactersetsoundeffectson"></a>IAgentCharacter::SetSoundEffectsOn

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT SetSoundEffectsOn(
   long bOn  // character sound effects setting 
);
```

Determina si se reproducen los efectos de sonido del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="bOn"></span><span id="bon"></span><span id="BON"></span>*Despedida*
</dt> <dd>

Configuración de efectos de sonido. Si este parámetro es **true**, los efectos sonoros de las animaciones se reproducirán cuando se reproduzca la animación. Si **es false**, no se reproducen los efectos sonoros.

</dd> </dl>

Esta configuración determina si se reproducen efectos sonoros compilados como parte del carácter al reproducir una animación asociada. La configuración de esta propiedad se aplica a todos los clientes del carácter. La configuración también está sujeta a la configuración de efectos de sonido globales del usuario en [**IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: GetSoundEffectsOn**](iagentcharacter--getsoundeffectson.md), [ **IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




