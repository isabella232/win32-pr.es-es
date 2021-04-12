---
title: Problemas de programación de RTMv2
description: Las funciones de RTMv2 se escriben con los siguientes supuestos.
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- Problemas de programación, RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b607adc939ff72a4d9fee99c15f6aa5192fa4c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357064"
---
# <a name="rtmv2-programming-issues"></a><span data-ttu-id="b975d-104">Problemas de programación de RTMv2</span><span class="sxs-lookup"><span data-stu-id="b975d-104">RTMv2 Programming Issues</span></span>

<span data-ttu-id="b975d-105">Las funciones de RTMv2 se escriben con los siguientes supuestos.</span><span class="sxs-lookup"><span data-stu-id="b975d-105">RTMv2 functions are written with the following assumptions.</span></span>

-   <span data-ttu-id="b975d-106">Las funciones RTMv2 no asignan memoria para el cliente.</span><span class="sxs-lookup"><span data-stu-id="b975d-106">RTMv2 functions do not allocate memory for the client.</span></span> <span data-ttu-id="b975d-107">El cliente siempre debe asignar memoria.</span><span class="sxs-lookup"><span data-stu-id="b975d-107">The client must always allocate memory.</span></span>
-   <span data-ttu-id="b975d-108">Cuando se anula el registro de un cliente, debe realizar las operaciones de limpieza, como liberar toda la memoria asignada.</span><span class="sxs-lookup"><span data-stu-id="b975d-108">When a client is unregistering, it must perform clean-up operations itself, such as releasing all memory allocated.</span></span>
-   <span data-ttu-id="b975d-109">Los clientes deben liberar los identificadores correctamente; pueden producirse pérdidas de memoria si un cliente no observa esta práctica.</span><span class="sxs-lookup"><span data-stu-id="b975d-109">Clients must release handles correctly; memory leaks can occur if a client does not observe this practice.</span></span>

 

 




