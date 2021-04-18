---
description: Los ejemplos de aplicaciones WMI en esta sección están escritos en C++.
ms.assetid: 5c4c4c4c-adbc-4702-a6fe-5f98a6db3ba1
ms.tgt_platform: multiple
title: Ejemplos de aplicaciones de C++ de WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883b51bd00de5e3938fef8467c68d299ac60683a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696784"
---
# <a name="wmi-c-application-examples"></a><span data-ttu-id="38260-103">Ejemplos de aplicaciones de C++ de WMI</span><span class="sxs-lookup"><span data-stu-id="38260-103">WMI C++ Application Examples</span></span>

<span data-ttu-id="38260-104">Los ejemplos de aplicaciones WMI en esta sección están escritos en C++.</span><span class="sxs-lookup"><span data-stu-id="38260-104">The WMI application examples in this section are written in C++.</span></span> <span data-ttu-id="38260-105">Muestran una serie de tareas que se pueden completar mediante componentes WMI y ofrecen una alternativa sobre el uso de scripts Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="38260-105">They demonstrate a range of tasks that can be completed using WMI components and offer an alternative over using Visual Basic scripts.</span></span> <span data-ttu-id="38260-106">Cada aplicación se divide en una serie de pasos de una manera similar, de modo que las secciones de código de distintos ejemplos se pueden combinar fácilmente para formar aplicaciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="38260-106">Each application is separated into a series of steps in a similar way so that code sections from different examples can easily be combined to form customized applications.</span></span>

<span data-ttu-id="38260-107">En la tabla siguiente se enumeran los ejemplos de C++ de esta sección.</span><span class="sxs-lookup"><span data-stu-id="38260-107">The following table lists the C++ examples in this section.</span></span>



| <span data-ttu-id="38260-108">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="38260-108">Example</span></span>                                                                                                                                  | <span data-ttu-id="38260-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="38260-109">Description</span></span>                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="38260-110">Ejemplo: obtener datos de WMI del equipo local</span><span class="sxs-lookup"><span data-stu-id="38260-110">Example: Getting WMI Data from the Local Computer</span></span>](example--getting-wmi-data-from-the-local-computer.md)                               | <span data-ttu-id="38260-111">Este ejemplo se conecta al espacio de nombres WMI en el equipo local y obtiene los datos de una consulta en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="38260-111">This example connects to the WMI namespace on the local computer and gets data from a query on the local computer.</span></span> <span data-ttu-id="38260-112">Los datos se recopilan de forma semisincrónica.</span><span class="sxs-lookup"><span data-stu-id="38260-112">The data is gathered semisynchronously.</span></span> |
| [<span data-ttu-id="38260-113">Ejemplo: obtener datos de WMI del equipo local de forma asincrónica</span><span class="sxs-lookup"><span data-stu-id="38260-113">Example: Getting WMI Data from the Local Computer Asynchronously</span></span>](example--getting-wmi-data-from-the-local-computer-asynchronously.md) | <span data-ttu-id="38260-114">Este ejemplo se conecta al espacio de nombres WMI en el equipo local y obtiene los datos de una consulta en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="38260-114">This example connects to the WMI namespace on the local computer and gets data from a query on the local computer.</span></span> <span data-ttu-id="38260-115">Los datos se recopilan de forma asincrónica.</span><span class="sxs-lookup"><span data-stu-id="38260-115">The data is gathered asynchronously.</span></span>    |
| [<span data-ttu-id="38260-116">Ejemplo: obtención de datos WMI desde un equipo remoto</span><span class="sxs-lookup"><span data-stu-id="38260-116">Example: Getting WMI Data from a Remote Computer</span></span>](example--getting-wmi-data-from-a-remote-computer.md)                                 | <span data-ttu-id="38260-117">Este ejemplo se conecta al espacio de nombres WMI en un equipo remoto y obtiene los datos de una consulta en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="38260-117">This example connects to the WMI namespace on a remote computer and gets data from a query on the remote computer.</span></span> <span data-ttu-id="38260-118">Los datos se recopilan de forma semisincrónica.</span><span class="sxs-lookup"><span data-stu-id="38260-118">The data is gathered semisynchronously.</span></span> |
| [<span data-ttu-id="38260-119">Ejemplo: llamar a un método de proveedor</span><span class="sxs-lookup"><span data-stu-id="38260-119">Example: Calling a Provider Method</span></span>](example--calling-a-provider-method.md)                                                             | <span data-ttu-id="38260-120">Este ejemplo se conecta al espacio de nombres WMI en el equipo local y llama a un método en WMI.</span><span class="sxs-lookup"><span data-stu-id="38260-120">This example connects to the WMI namespace on the local computer and calls a method in WMI.</span></span> <span data-ttu-id="38260-121">El método se ejecuta sincrónicamente.</span><span class="sxs-lookup"><span data-stu-id="38260-121">The method is executed synchronously.</span></span>                          |
| [<span data-ttu-id="38260-122">Ejemplo: recibir notificaciones de eventos a través de WMI</span><span class="sxs-lookup"><span data-stu-id="38260-122">Example: Receiving Event Notifications Through WMI</span></span>](example--receiving-event-notifications-through-wmi-.md)                            | <span data-ttu-id="38260-123">Este ejemplo se conecta al espacio de nombres WMI en el equipo local y recibe un evento del equipo local.</span><span class="sxs-lookup"><span data-stu-id="38260-123">This example connects to the WMI namespace on the local computer and receives an event from the local computer.</span></span> <span data-ttu-id="38260-124">El evento se recibe de forma semisincrónica.</span><span class="sxs-lookup"><span data-stu-id="38260-124">The event is received semisynchronously.</span></span>   |



 

 

 



