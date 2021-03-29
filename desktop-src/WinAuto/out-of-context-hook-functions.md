---
title: Funciones de enlace fuera de contexto
ms.assetid: c0156485-db1e-42d3-bbbd-c51835a597ed
description: 'Más información sobre: funciones de enlace fuera de contexto'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d5837c39850c5821d44146498f62d4c874e7802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911773"
---
# <a name="out-of-context-hook-functions"></a><span data-ttu-id="26ebf-103">Funciones de enlace fuera de contexto</span><span class="sxs-lookup"><span data-stu-id="26ebf-103">Out-of-Context Hook Functions</span></span>

<span data-ttu-id="26ebf-104">En la siguiente lista se describen los aspectos clave de las funciones de enlace fuera de contexto:</span><span class="sxs-lookup"><span data-stu-id="26ebf-104">The following list outlines the key aspects of out-of-context hook functions:</span></span>

-   <span data-ttu-id="26ebf-105">Las funciones de enlace fuera del contexto se encuentran en el espacio de direcciones del cliente, tanto si están en el cuerpo del código como en un archivo DLL.</span><span class="sxs-lookup"><span data-stu-id="26ebf-105">Out-of-context hook functions are located in the client's address space, whether it is in the code body or in a DLL.</span></span>
-   <span data-ttu-id="26ebf-106">Las funciones de enlace fuera de contexto no se asignan al espacio de direcciones del servidor.</span><span class="sxs-lookup"><span data-stu-id="26ebf-106">Out-of-context hook functions are not mapped into the server's address space.</span></span>
-   <span data-ttu-id="26ebf-107">Cuando se desencadena un evento, se calculan las referencias de los parámetros de la función de enlace a través de los límites del proceso.</span><span class="sxs-lookup"><span data-stu-id="26ebf-107">When an event is triggered, the parameters for the hook function are marshaled across process boundaries.</span></span>
-   <span data-ttu-id="26ebf-108">Las funciones de enlace fuera de contexto son notablemente más lentas que las funciones de enlace en contexto debido al cálculo de referencias.</span><span class="sxs-lookup"><span data-stu-id="26ebf-108">Out-of-context hook functions are noticeably slower than in-context hook functions due to marshaling.</span></span>
-   <span data-ttu-id="26ebf-109">El sistema pone en cola las notificaciones de eventos para que lleguen de forma asincrónica (debido al tiempo necesario para realizar el cálculo de referencias).</span><span class="sxs-lookup"><span data-stu-id="26ebf-109">The system queues the event notifications so that they arrive asynchronously (because of the time required to perform marshaling).</span></span>

<span data-ttu-id="26ebf-110">Aunque las notificaciones de eventos son asincrónicas, Microsoft Active Accessibility garantiza que la función de devolución de llamada recibe todos los eventos en el orden en el que se generan.</span><span class="sxs-lookup"><span data-stu-id="26ebf-110">Although the event notifications are asynchronous, Microsoft Active Accessibility assures that the callback function receives all events in the order in which they are generated.</span></span>

<span data-ttu-id="26ebf-111">El componente de usuario del sistema operativo asigna memoria a los eventos que se controlan mediante funciones de enlace fuera de contexto.</span><span class="sxs-lookup"><span data-stu-id="26ebf-111">The USER component of the operating system allocates memory for events that are handled by out-of-context hook functions.</span></span> <span data-ttu-id="26ebf-112">La memoria se libera cuando las funciones de enlace devuelven.</span><span class="sxs-lookup"><span data-stu-id="26ebf-112">The memory is freed when the hook functions return.</span></span> <span data-ttu-id="26ebf-113">Si una función de enlace no procesa los eventos lo suficientemente rápido, los recursos de usuario se reducen, lo que finalmente produce un error o un tiempo de respuesta muy lento.</span><span class="sxs-lookup"><span data-stu-id="26ebf-113">If a hook function does not process events quickly enough, USER resources are lowered, eventually resulting in a fault or extremely slow response times.</span></span> <span data-ttu-id="26ebf-114">Estos problemas pueden producirse si:</span><span class="sxs-lookup"><span data-stu-id="26ebf-114">These problems may occur if:</span></span>

-   <span data-ttu-id="26ebf-115">Los eventos se desencadenan muy rápidamente.</span><span class="sxs-lookup"><span data-stu-id="26ebf-115">Events are fired very rapidly.</span></span>
-   <span data-ttu-id="26ebf-116">El sistema es lento.</span><span class="sxs-lookup"><span data-stu-id="26ebf-116">The system is slow.</span></span>
-   <span data-ttu-id="26ebf-117">La función de enlace procesa los eventos lentamente.</span><span class="sxs-lookup"><span data-stu-id="26ebf-117">The hook function processes events slowly.</span></span>
-   <span data-ttu-id="26ebf-118">El cliente se ejecuta en Windows 9x.</span><span class="sxs-lookup"><span data-stu-id="26ebf-118">The client is running on Windows 9x.</span></span>

 

 




