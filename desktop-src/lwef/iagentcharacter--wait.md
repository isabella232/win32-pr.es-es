---
title: Espera de IAgentCharacter
description: Espera de IAgentCharacter
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d54ac2de03c78c220803a774537230938a00a776
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357456"
---
# <a name="iagentcharacterwait"></a>IAgentCharacter:: wait

\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

Contiene la cola de animaciones del carácter en la animación (solicitud) especificada hasta que se completa otra solicitud de otro carácter.

-   Devuelve S \_ OK para indicar que la operación se realizó correctamente.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

IDENTIFICADOR de la solicitud que se va a esperar.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador de solicitud de **espera** .

</dd> </dl>

Use este método solo cuando admita varios caracteres (simultáneos) y desee secuenciar su interacción. (Para un solo carácter, cada solicitud de animación se reproduce secuencialmente, una vez completada la solicitud anterior). Si tiene dos caracteres y desea que la solicitud de animación de un carácter espere hasta que se complete la animación de otro carácter, establezca el método **Wait** en el identificador de la solicitud de animación de otro carácter.

 

 




