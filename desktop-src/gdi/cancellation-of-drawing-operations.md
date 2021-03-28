---
description: Cuando las aplicaciones de dibujo complejas realizan operaciones de gráficos largas, consumen valiosos recursos del sistema.
ms.assetid: 3beef852-27fe-4ee2-b38b-3dc50e5d2fcf
title: Cancelación de operaciones de dibujo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98e3bdb7a57c7c427e7cd15ffddb62b1c492c25b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997420"
---
# <a name="cancellation-of-drawing-operations"></a><span data-ttu-id="1902c-103">Cancelación de operaciones de dibujo</span><span class="sxs-lookup"><span data-stu-id="1902c-103">Cancellation of Drawing Operations</span></span>

<span data-ttu-id="1902c-104">Cuando las aplicaciones de dibujo complejas realizan operaciones de gráficos largas, consumen valiosos recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="1902c-104">When complex drawing applications perform lengthy graphics operations, they consume valuable system resources.</span></span> <span data-ttu-id="1902c-105">Aprovechando las características de multitarea del sistema, una aplicación puede usar subprocesos y la función [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) para administrar estas operaciones.</span><span class="sxs-lookup"><span data-stu-id="1902c-105">By taking advantage of the system's multitasking features, an application can use threads and the [**CancelDC**](/windows/desktop/api/Wingdi/nf-wingdi-canceldc) function to manage these operations.</span></span> <span data-ttu-id="1902c-106">Por ejemplo, si la operación de gráficos realizada por el subproceso A está consumiendo los recursos necesarios, el subproceso B puede llamar a la función CancelDC para detener esa operación.</span><span class="sxs-lookup"><span data-stu-id="1902c-106">For example, if the graphics operation performed by thread A is consuming needed resources, thread B can call the CancelDC function to halt that operation.</span></span>

 

 



