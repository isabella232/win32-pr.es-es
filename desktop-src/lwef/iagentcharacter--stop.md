---
title: IAgentCharacter Stop
description: IAgentCharacter Stop
ms.assetid: 3064bb3e-37a6-4022-bffb-130735736889
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297f187b7045b1da5773643f2765160c71fbca0d4eb7c6ec12c4032e2f1d5806
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114785"
---
# <a name="iagentcharacterstop"></a>IAgentCharacter::Stop

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Stop(
   long dwReqID  // request ID
);
```

Detiene la animación especificada (solicitud) y la quita de la cola de animación del carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

Identificador de la solicitud que se debe detener.

</dd> </dl>

**Stop** también se puede usar para detener las llamadas [**prepare en**](iagentcharacter--prepare.md) cola.

## <a name="see-also"></a>Consulte también

[**IAgentCharacter::P repare**](iagentcharacter--prepare.md), [ **IAgentCharacter::StopAll**](iagentcharacter--stopall.md)


 

 




