---
title: IAgentCharacter GestureAt
description: IAgentCharacter GestureAt
ms.assetid: ece84652-383e-4397-a6d9-f0209dd80767
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 266dc2d5e797ec0c7b30f7f827a094cd01c04195
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419208"
---
# <a name="iagentcharactergestureat"></a>IAgentCharacter::GestureAt

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT GestureAt(
   short x,         // x-coordinate of specified location
   short y,         // y-coordinate of specified location
   long * pdwReqID  // address of a request ID
);
```

Reproduce la animación de estado de **gesturing** asociada en función de la ubicación especificada.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente. Cuando la función devuelve, *pdwReqID* contiene el identificador de la solicitud.

<dl> <dt>

<span id="x"></span><span id="X"></span>*x1*
</dt> <dd>

Coordenada x de la ubicación especificada en píxeles, con respecto al origen de la pantalla (superior izquierda).

</dd> <dt>

<span id="y"></span><span id="Y"></span>*sí*
</dt> <dd>

Coordenada y de la ubicación especificada en píxeles, con respecto al origen de la pantalla (superior izquierda).

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador de solicitud **GestureAt** .

</dd> </dl>

El servidor determina y reproduce automáticamente la animación gesturing adecuada según la posición actual del carácter y la ubicación especificada. Al usar el protocolo HTTP para tener acceso a los datos de animación y de caracteres, utilice el método [**Prepare**](iagentcharacter--prepare.md) para asegurarse de que las animaciones estén disponibles antes de llamar a este método.

 

 




