---
title: Criterios para las entradas del servicio de nombres
description: Criterios para las entradas del servicio de nombres con llamada a procedimiento remoto (RPC).
ms.assetid: f9a7b935-7104-489c-93a8-0c3793d17348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb32314dc86b179ea98bdf07000dc5ea359bdc77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104486890"
---
# <a name="criteria-for-name-service-entries"></a><span data-ttu-id="0781b-103">Criterios para las entradas del servicio de nombres</span><span class="sxs-lookup"><span data-stu-id="0781b-103">Criteria for Name Service Entries</span></span>

<span data-ttu-id="0781b-104">Cuando se procesan entradas de servicio de nombres, se usan los siguientes criterios:</span><span class="sxs-lookup"><span data-stu-id="0781b-104">The following criteria are used when processing name service entries:</span></span>

-   <span data-ttu-id="0781b-105">Si proporciona un nombre de entrada que no sea **null** para [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), esa entrada será la única entrada buscada para los identificadores de enlace.</span><span class="sxs-lookup"><span data-stu-id="0781b-105">If you provide a non-**NULL** entry name for [**RpcNsBindingLookupBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina), that entry will be the only entry searched for binding handles.</span></span> <span data-ttu-id="0781b-106">Si pasa **null**, se buscarán todas las entradas del dominio de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="0781b-106">If you pass **NULL**, all entries in your logon domain will be searched.</span></span> <span data-ttu-id="0781b-107">Tenga en cuenta que esto no incluye dominios de confianza.</span><span class="sxs-lookup"><span data-stu-id="0781b-107">Note that this does not include trusted domains.</span></span>
-   <span data-ttu-id="0781b-108">Si proporciona un identificador de interfaz, solo se devuelven los identificadores de enlace de una entrada si la sección de la interfaz de la entrada contiene una versión compatible de ese UUID de interfaz.</span><span class="sxs-lookup"><span data-stu-id="0781b-108">If you provide an interface handle, binding handles are returned from an entry only if the interface section of the entry contains a compatible version of that interface UUID.</span></span> <span data-ttu-id="0781b-109">Es decir, el número de versión principal debe ser el mismo que el UUID de la interfaz, mientras que el número de versión secundaria debe ser igual o mayor que el suyo.</span><span class="sxs-lookup"><span data-stu-id="0781b-109">That is, the major version number must be the same as your interface UUID, while the minor version number must be equal to or greater than yours.</span></span>
-   <span data-ttu-id="0781b-110">Si proporciona un UUID de objeto, solo se devuelven los identificadores de enlace de una entrada si la sección de UUID del objeto de la entrada contiene ese UUID de objeto concreto.</span><span class="sxs-lookup"><span data-stu-id="0781b-110">If you provide an object UUID, binding handles are returned from an entry only if the object UUID section of the entry contains that particular object UUID.</span></span>

<span data-ttu-id="0781b-111">Si una entrada del servicio de nombres sobrevive los criterios descritos anteriormente, se recopilan todos los identificadores de enlace de esas entradas.</span><span class="sxs-lookup"><span data-stu-id="0781b-111">If a name service entry survives the criteria described above, all the binding handles from those entries are gathered.</span></span> <span data-ttu-id="0781b-112">Los identificadores con una secuencia de protocolo que no es compatible con el cliente se descartan y se devuelven los controladores restantes como resultado de [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).</span><span class="sxs-lookup"><span data-stu-id="0781b-112">Handles with a protocol sequence that is unsupported by the client are discarded and the remaining handles are returned to you as the output from [**RpcNsBindingLookupNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext).</span></span>

 

 




