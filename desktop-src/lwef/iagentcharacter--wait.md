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
# <a name="iagentcharacterwait"></a><span data-ttu-id="c8966-103">IAgentCharacter:: wait</span><span class="sxs-lookup"><span data-stu-id="c8966-103">IAgentCharacter::Wait</span></span>

<span data-ttu-id="c8966-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="c8966-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Wait(
   long dwReqID,    // request ID
   long * pdwReqID  // address of request ID
);
```

<span data-ttu-id="c8966-105">Contiene la cola de animaciones del carácter en la animación (solicitud) especificada hasta que se completa otra solicitud de otro carácter.</span><span class="sxs-lookup"><span data-stu-id="c8966-105">Holds the character's animation queue at the specified animation (request) until another request for another character completes.</span></span>

-   <span data-ttu-id="c8966-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="c8966-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="c8966-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span><span class="sxs-lookup"><span data-stu-id="c8966-107"><span id="dwReqID"></span><span id="dwreqid"></span><span id="DWREQID"></span>*dwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="c8966-108">IDENTIFICADOR de la solicitud que se va a esperar.</span><span class="sxs-lookup"><span data-stu-id="c8966-108">The ID of the request to wait for.</span></span>

</dd> <dt>

<span data-ttu-id="c8966-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span><span class="sxs-lookup"><span data-stu-id="c8966-109"><span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*</span></span>
</dt> <dd>

<span data-ttu-id="c8966-110">Dirección de una variable que recibe el identificador de solicitud de **espera** .</span><span class="sxs-lookup"><span data-stu-id="c8966-110">Address of a variable that receives the **Wait** request ID.</span></span>

</dd> </dl>

<span data-ttu-id="c8966-111">Use este método solo cuando admita varios caracteres (simultáneos) y desee secuenciar su interacción.</span><span class="sxs-lookup"><span data-stu-id="c8966-111">Use this method only when you support multiple (simultaneous) characters and want to sequence their interaction.</span></span> <span data-ttu-id="c8966-112">(Para un solo carácter, cada solicitud de animación se reproduce secuencialmente, una vez completada la solicitud anterior). Si tiene dos caracteres y desea que la solicitud de animación de un carácter espere hasta que se complete la animación de otro carácter, establezca el método **Wait** en el identificador de la solicitud de animación de otro carácter.</span><span class="sxs-lookup"><span data-stu-id="c8966-112">(For a single character, each animation request is played sequentially--after the previous request completes.) If you have two characters and want one character's animation request to wait until the other character's animation completes, set the **Wait** method to the other character's animation request ID.</span></span>

 

 




