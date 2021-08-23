---
title: IAgentCharacter Play
description: IAgentCharacter Play
ms.assetid: a0158693-ff62-4da4-8b68-402e8d5b1c2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320572322d7a28b52693c80eb918ebf78fcb50083e012e35c65df3a7bffdf0a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976405"
---
# <a name="iagentcharacterplay"></a>IAgentCharacter::P lay

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Play(
   BSTR bszAnimation,  // name of an animation
   long * pdwReqID     // address of request ID
);
```

Reproduce la animación especificada.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente. Cuando la función devuelve un resultado, *pdwReqID* contiene el identificador de la solicitud.

<dl> <dt>

<span id="bszAnimation"></span><span id="bszanimation"></span><span id="BSZANIMATION"></span>*bszAnimation*
</dt> <dd>

Nombre de una animación.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador de solicitud **IAgentCharacter::P lay.**

</dd> </dl>

El nombre de una animación se define cuando el carácter se compila con el Editor de caracteres de Microsoft Agent. Antes de reproducir la animación especificada, el servidor intenta reproducir la animación **Devolución** de la animación anterior (si se ha asignado una).

Cuando los datos de animación de un carácter se almacenan en la máquina local del usuario, puede usar el método **IAgentCharacter::P lay** y especificar el nombre de la animación. Cuando use el protocolo HTTP para acceder a los datos de animación, use el [**método Prepare**](iagentcharacter--prepare.md) para garantizar la disponibilidad de la animación antes de llamar a este método.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::P repare**](iagentcharacter--prepare.md)


 

 




