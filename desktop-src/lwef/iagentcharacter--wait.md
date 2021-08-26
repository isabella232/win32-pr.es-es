---
title: Espera de IAgentCharacter
description: Espera de IAgentCharacter
ms.assetid: 4edb9a47-9385-49da-83ff-144780853ae7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fba3f292b9dc7a0651cf3a1a27adcfe0ea808127d8ce00ae62cb1e84cc126a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014225"
---
# <a name="iagentcharacterwait"></a>IAgentCharacter::Wait

\[Microsoft Agent está en desuso a partir Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

Mantiene la cola de animación del carácter en la animación especificada (solicitud) hasta que se complete otra solicitud de otro carácter.

-   Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.

<dl> <dt>

<span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*
</dt> <dd>

Identificador de la solicitud que se debe esperar.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Dirección de una variable que recibe el identificador **de solicitud wait.**

</dd> </dl>

Use este método solo cuando admita varios caracteres (simultáneos) y desee secuenciar su interacción. (Para un solo carácter, cada solicitud de animación se reproduce secuencialmente, una vez completada la solicitud anterior). Si tiene dos caracteres y desea que la solicitud de animación de un carácter espere hasta que se complete la animación del otro carácter, establezca el método **Wait** en el identificador de solicitud de animación del otro carácter.

 

 




