---
description: El servicio Instrumental de COM+ le permite compilar sus propios programas de registro y administración de eventos COM+ cuando desee mostrar varias métricas de rendimiento para los componentes COM+.
ms.assetid: 07f68734-a382-4fe5-86af-90805f61c68d
title: Conceptos de instrumentación de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d86b5dbb7bb3f6db14d82220d88c58dbc0a8255
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714819"
---
# <a name="com-instrumentation-concepts"></a><span data-ttu-id="213d0-103">Conceptos de instrumentación de COM+</span><span class="sxs-lookup"><span data-stu-id="213d0-103">COM+ Instrumentation Concepts</span></span>

<span data-ttu-id="213d0-104">El servicio Instrumental de COM+ le permite compilar sus propios programas de registro y administración de eventos COM+ cuando desee mostrar varias métricas de rendimiento para los componentes COM+.</span><span class="sxs-lookup"><span data-stu-id="213d0-104">The COM+ instrumentation service enables you to build your own COM+ event management and logging programs when you want to display various performance metrics for your COM+ components.</span></span> <span data-ttu-id="213d0-105">La instrumentación de COM+ también se puede utilizar para configurar eventos definidos por el usuario y convertir los eventos COM+ al formato de Visual Studio Analyzer (VSA) al actualizar paquetes MTS que reciben eventos MTS.</span><span class="sxs-lookup"><span data-stu-id="213d0-105">COM+ instrumentation can also be used to configure user-defined events and to convert COM+ events to Visual Studio Analyzer (VSA) format when you are upgrading MTS packages that are receiving MTS events.</span></span>

> [!Note]  
> <span data-ttu-id="213d0-106">A partir de Windows Server 2003, solo los administradores tienen privilegios de acceso de lectura a los registros de seguimiento de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="213d0-106">As of Windows Server 2003, only administrators have read access privileges to the trace logs for system events.</span></span>

 

<span data-ttu-id="213d0-107">Al suscribirse a los eventos publicados por el publicador de eventos del sistema, los clientes pueden implementar las [interfaces de instrumentación de com+](com--instrumentation-interfaces.md) para recibir notificaciones para una variedad de métricas de rendimiento de com+, como información sobre objetos com+ específicos, aplicaciones com+ y servicios com+.</span><span class="sxs-lookup"><span data-stu-id="213d0-107">By subscribing to the events published by the system events publisher, clients can implement the [COM+ instrumentation interfaces](com--instrumentation-interfaces.md) to receive notifications for a variety of COM+ performance metrics, such as information about specific COM+ objects, COM+ applications, and COM+ services.</span></span> <span data-ttu-id="213d0-108">Las métricas se publican en el cliente mediante el [servicio de eventos com+](com--events.md), un sistema de eventos débilmente acoplados (LCE) que almacena información de eventos de distintos publicadores en un almacén de eventos del catálogo de com+.</span><span class="sxs-lookup"><span data-stu-id="213d0-108">The metrics are published to the client by using the [COM+ events service](com--events.md), a loosely coupled events (LCE) system that stores event information from different publishers in an event store in the COM+ catalog.</span></span>

> [!Note]  
> <span data-ttu-id="213d0-109">La instrumentación de COM+ no garantiza la entrega de un evento.</span><span class="sxs-lookup"><span data-stu-id="213d0-109">COM+ instrumentation does not guarantee the delivery of an event.</span></span>

 

<span data-ttu-id="213d0-110">Cada métrica tiene una marca de tiempo que indica la hora a la que se generó la métrica, no el tiempo que se envió o recibió.</span><span class="sxs-lookup"><span data-stu-id="213d0-110">Every metric has a timestamp that indicates the time when the metric was generated, not the time that it was dispatched or received.</span></span> <span data-ttu-id="213d0-111">El cliente puede correlacionar la marca de tiempo y averiguar el costo de ejecutar una aplicación COM+, el costo de una transacción ejecutada dentro de una aplicación COM+ o el costo de una llamada al método dentro de una aplicación COM+.</span><span class="sxs-lookup"><span data-stu-id="213d0-111">The client can correlate the timestamp and find out the cost of running a COM+ application, the cost of a transaction executed inside a COM+ application, or the cost of a method call inside of a COM+ application.</span></span>

<span data-ttu-id="213d0-112">También puede usar el servicio de instrumentación de COM+ para filtrar la información de métricas de rendimiento específica que desee ver.</span><span class="sxs-lookup"><span data-stu-id="213d0-112">You can also use the COM+ Instrumentation service to filter for the specific performance metrics information that you want to see.</span></span> <span data-ttu-id="213d0-113">Por ejemplo, al suscribirse a un método o una interfaz de instrumentación de COM+, puede especificar las propiedades de la suscripción en la estructura [**COMSVCSEVENTINFO**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) , como el identificador de la aplicación (miembro **guidApp** ) o el identificador de proceso (miembro **dwPid** ).</span><span class="sxs-lookup"><span data-stu-id="213d0-113">For example, when you subscribe to a COM+ instrumentation interface or method, you can specify properties for the subscription in the [**COMSVCSEVENTINFO**](/windows/win32/api/comsvcs/ns-comsvcs-comsvcseventinfo) structure, such as the application ID (**guidApp** member) or the process ID (**dwPid** member).</span></span>

<span data-ttu-id="213d0-114">Cuando se especifica el identificador de la aplicación, solo recibe las métricas de la aplicación especificada.</span><span class="sxs-lookup"><span data-stu-id="213d0-114">When the application ID is specified, you receive only the metrics from the specified application.</span></span> <span data-ttu-id="213d0-115">Cuando se especifica el identificador de proceso, recibe métricas de la aplicación de servidor y las aplicaciones de biblioteca especificadas que se cargan en ese proceso.</span><span class="sxs-lookup"><span data-stu-id="213d0-115">When the process ID is specified, you receive metrics from the specified server application and library applications that are loaded in that process.</span></span> <span data-ttu-id="213d0-116">El usuario puede especificar el identificador de la aplicación y el identificador del proceso, pero el identificador de la aplicación debe ser el de la aplicación de servidor que se ejecuta en el proceso con el identificador de proceso especificado.</span><span class="sxs-lookup"><span data-stu-id="213d0-116">The user can specify both the application ID and the process ID, but the application ID has to be that of the server application running in the process with the specified process ID.</span></span> <span data-ttu-id="213d0-117">Si no se especifica ninguno, el usuario recibe métricas de todas las aplicaciones de servidor y de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="213d0-117">If neither is specified, the user receives metrics from all the server and library applications.</span></span>

<span data-ttu-id="213d0-118">Las métricas de instrumentación de COM+ proporcionan información suficiente para que la aplicación de supervisión las correlacione con las métricas del sistema operativo para el análisis de rendimiento, el planeamiento de la capacidad y el modelado y la predicción.</span><span class="sxs-lookup"><span data-stu-id="213d0-118">The COM+ instrumentation metrics provide enough information for the monitoring application to correlate them with the operating system metrics for performance analysis, capacity planning, and for modeling and prediction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="213d0-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="213d0-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="213d0-120">Interfaces de instrumentación de COM+</span><span class="sxs-lookup"><span data-stu-id="213d0-120">COM+ Instrumentation Interfaces</span></span>](com--instrumentation-interfaces.md)
</dt> </dl>

 

 



