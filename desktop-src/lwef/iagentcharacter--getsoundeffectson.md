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
# <a name="iagentcharactergetsoundeffectson"></a>IAgentCharacter::GetSoundEffectsOn

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetSoundEffectsOn(
   long * pbOn  // address of variable for sound effects setting 
);
```

Recupera si está habilitada la configuración de efectos sonoros del carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbOn"></span><span id="pbon"></span><span id="PBON"></span>*pbOn*
</dt> <dd>

Dirección de una variable que recibe **true** si está habilitada la configuración de efectos sonoros del carácter, **false** si está deshabilitada.

</dd> </dl>

La configuración de efectos sonoros del carácter determina si se reproducen efectos sonoros compilados como parte del carácter al reproducir una animación asociada. La configuración está sujeta a la configuración de efectos de sonido globales del usuario en [**IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md).

## <a name="see-also"></a>Consulte también

[**IAgentCharacter:: SetSoundEffectsOn**](iagentcharacter--setsoundeffectson.md), [ **IAgentAudioOutputProperties:: GetUsingSoundEffects**](iagentaudiooutputproperties--getusingsoundeffects.md)


 

 




