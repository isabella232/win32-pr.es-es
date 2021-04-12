---
title: Errores de asignación de búfer de RPC
description: Dado que la biblioteca en tiempo de ejecución de RPC asigna memoria para los búferes de envío y recepción, la función debe esperar errores de asignación de RPC.
ms.assetid: be9105df-1183-48d6-8cea-391ca628c8b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbe48c113d644447b5ff7b69988f2534d7de3a9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357066"
---
# <a name="rpc-buffer-allocation-errors"></a><span data-ttu-id="7751f-103">Errores de asignación de búfer de RPC</span><span class="sxs-lookup"><span data-stu-id="7751f-103">RPC Buffer Allocation Errors</span></span>

<span data-ttu-id="7751f-104">Dado que la biblioteca en tiempo de ejecución de RPC asigna memoria para los búferes de envío y recepción, la función debe esperar errores de asignación de RPC.</span><span class="sxs-lookup"><span data-stu-id="7751f-104">Because the RPC run-time library allocates memory for send and receive buffers, the function should expect RPC allocation errors.</span></span> <span data-ttu-id="7751f-105">En caso de un error de asignación de RPC, se invalida un identificador reanudable.</span><span class="sxs-lookup"><span data-stu-id="7751f-105">In the event of an RPC allocation error, a resumable handle is invalidated.</span></span> <span data-ttu-id="7751f-106">Este es un requisito porque las funciones reanudables no se pueden rebobinar.</span><span class="sxs-lookup"><span data-stu-id="7751f-106">This is a requirement because resumable functions are not rewindable.</span></span>

 

 




