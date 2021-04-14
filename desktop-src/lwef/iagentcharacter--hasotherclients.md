---
title: IAgentCharacter HasOtherClients
description: IAgentCharacter HasOtherClients
ms.assetid: ee74fa9b-2842-43ac-8493-bc69b480581e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32380e31e63278f4181cfd854ecaada1775a4fd5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532500"
---
# <a name="iagentcharacterhasotherclients"></a><span data-ttu-id="282ba-103">IAgentCharacter::HasOtherClients</span><span class="sxs-lookup"><span data-stu-id="282ba-103">IAgentCharacter::HasOtherClients</span></span>

<span data-ttu-id="282ba-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="282ba-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT HasOtherClients(
   long * plNumOtherClients  // address of variable for number of clients 
);                           // for character 
```

<span data-ttu-id="282ba-105">Recupera si un carácter tiene otros clientes.</span><span class="sxs-lookup"><span data-stu-id="282ba-105">Retrieves whether a character has other clients.</span></span>

-   <span data-ttu-id="282ba-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="282ba-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="282ba-107"><span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*plNumOtherClients*</span><span class="sxs-lookup"><span data-stu-id="282ba-107"><span id="plNumOtherClients"></span><span id="plnumotherclients"></span><span id="PLNUMOTHERCLIENTS"></span>*plNumOtherClients*</span></span>
</dt> <dd>

<span data-ttu-id="282ba-108">Dirección de una variable que recibe el número de otros clientes conectados para el carácter (número total de clientes menos el cliente).</span><span class="sxs-lookup"><span data-stu-id="282ba-108">Address of a variable that receives the number of other connected clients for the character (total number of clients minus your client).</span></span>

</dd> </dl>

 

 




