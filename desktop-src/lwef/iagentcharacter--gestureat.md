---
title: IAgentCharacter GestureAt
description: IAgentCharacter GestureAt
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bde86f9e1e60820aa7e1bc3a3f839dc920efda001f5b15e4f1ec7df4fc0cd7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976455"
---
# <a name="iagentcharactergestureat"></a>IAgentCharacter::GestureAt

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

Reproduce la animación **de estado Gesturing** asociada en función de la ubicación especificada.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente. Cuando la función vuelve, *pdwReqID* contiene el identificador de la solicitud.

<dl> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordenada x de la ubicación especificada en píxeles, en relación con el origen de la pantalla (esquina superior izquierda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordenada y de la ubicación especificada en píxeles, en relación con el origen de la pantalla (esquina superior izquierda).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador **de solicitud GestureAt.**

</dd> </dl>

El servidor determina y reproduce automáticamente la animación de gestura adecuada en función de la posición actual del carácter y la ubicación especificada. Cuando use el protocolo HTTP para acceder a los datos de caracteres y animaciones, use el método [**Prepare**](iagentcharacter--prepare.md) para asegurarse de que las animaciones están disponibles antes de llamar a este método.

 

 




