---
title: IAgentBalloon GetEnabled
description: IAgentBalloon GetEnabled
ms.assetid: 1a5ea6c0-6150-459f-95eb-a9c7598c1d94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd78245534b942e7972066ec90179172f7b556c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357720"
---
# <a name="iagentballoongetenabled"></a>IAgentBalloon::GetEnabled

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GetEnabled(
  long * pbEnabled  // address of variable for Enabled setting 
);                  // for word balloon
```

Recupera el valor de la propiedad [**Enabled**](enabled-property.md) de un globo de palabras.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="pbEnabled"></span><span id="pbenabled"></span><span id="PBENABLED"></span>*pbEnabled*
</dt> <dd>

La dirección de una variable que recibe **true** cuando el globo de palabras está habilitado y **false** cuando está deshabilitado.

</dd> </dl>

El servidor de Microsoft Agent muestra automáticamente el globo de palabras para la salida de voz, a menos que esté deshabilitado. El globo de palabras se puede deshabilitar para un carácter en el editor de caracteres del agente de Microsoft o (por el usuario) para todos los caracteres de la hoja de propiedades del agente de Microsoft. Si el usuario deshabilita el globo de palabras, el cliente no podrá restaurarlo.

 

 




