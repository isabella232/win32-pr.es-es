---
title: IAgentAudioOutputProperties GetEnabled
description: IAgentAudioOutputProperties GetEnabled
ms.assetid: a1e555e1-98f1-4a3d-b6ba-4cd35348db2b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a8f5247a767f82a66920f4c27b48d33044336d5b6d179b68587b06c95c2b502
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062045"
---
# <a name="iagentaudiooutputpropertiesgetenabled"></a>IAgentAudioOutputProperties::GetEnabled

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetEnabled(
long * pbEnabled  // address of variable for audio output Enabled setting 
);                      
```

Recupera un valor que indica si la salida de voz de caracteres está habilitada.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

Dirección de una variable que recibe **True si** la salida de voz está habilitada actualmente y **False** si está deshabilitada.

</dd> </dl>

Dado que esta configuración afecta a la salida hablada (TTS y archivo de sonido) para todos los caracteres, solo el usuario puede cambiar esta propiedad en la hoja de propiedades de Microsoft Agent.

 

 




