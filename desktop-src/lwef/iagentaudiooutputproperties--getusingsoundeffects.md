---
title: IAgentAudioOutputProperties GetUsing SoundEffects
description: IAgentAudioOutputProperties GetUsing SoundEffects
ms.assetid: 3ccf90b1-a2aa-482a-9f96-85d735532c11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6750dbfee36039337025a03b9f77573a2134f85d15a56d77b2d512482c7bb0e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118751459"
---
# <a name="iagentaudiooutputpropertiesgetusingsoundeffects"></a>IAgentAudioOutputProperties::GetUsing SoundEffects

\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetUsingSoundEffects(
long * pbUsingSoundEffects  // address of variable sound effects output 
);                          // setting 
```

Recupera un valor que indica si la salida de efectos de sonido está habilitada.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbUsingSoundEffects"></span><span id="pbusingsoundeffects"></span><span id="PBUSINGSOUNDEFFECTS"></span>*pbUsingEffects*
</dt> <dd>

Dirección de una variable que recibe **True si** la salida de efectos de sonido está habilitada actualmente y **False** si está deshabilitada.

</dd> </dl>

Los efectos de sonido de la animación de un carácter se asignan en el Editor de caracteres de Microsoft Agent. Dado que esta configuración afecta a la salida de efectos de sonido de todos los caracteres, solo el usuario puede cambiar esta propiedad en la hoja de propiedades de Microsoft Agent.

 

 




