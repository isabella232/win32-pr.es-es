---
title: Contadores de rendimiento de escenario 3
description: Los contadores de rendimiento miden cantidades de información o datos, según el número, el tamaño, la duración y la velocidad de los datos que se solicitan o reciben.
ms.assetid: 1b264144-7600-402e-86f8-674a2d02f9f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de90607cbda0542ee385b83f44bec878927d509f
ms.sourcegitcommit: fc3f2a28a55e590ac38846048f10b64ba527a98d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/27/2020
ms.locfileid: "105665887"
---
# <a name="scenario-3-performance-counters"></a><span data-ttu-id="6c842-103">Escenario 3: contadores de rendimiento</span><span class="sxs-lookup"><span data-stu-id="6c842-103">Scenario 3: Performance Counters</span></span>

<span data-ttu-id="6c842-104">Los contadores de rendimiento miden cantidades de información o datos, según el número, el tamaño, la duración y la velocidad de los datos que se solicitan o reciben.</span><span class="sxs-lookup"><span data-stu-id="6c842-104">Performance counters measure quantities of information or data, according to the number, size, duration, and rate of data being requested or received.</span></span> <span data-ttu-id="6c842-105">No debería esperar obtener una lista de detalles de un contador, como una lista de mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="6c842-105">You should not expect to get a list of details from a counter, such as a list of error messages.</span></span> <span data-ttu-id="6c842-106">En su lugar, utilice los contadores de rendimiento para obtener cantidades, como el número de mensajes de error desde el inicio o la velocidad a la que se generan los mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="6c842-106">Instead, use performance counters to get quantities, such as the number of error message since startup or the rate at which error messages are being generated.</span></span>

## <a name="performance-counters-for-httpsys"></a><span data-ttu-id="6c842-107">Contadores de rendimiento para HTTP.sys</span><span class="sxs-lookup"><span data-stu-id="6c842-107">Performance Counters for HTTP.sys</span></span>

<span data-ttu-id="6c842-108">A partir de Windows Vista y Windows Server 2008, HTTP.sys tiene los siguientes contadores de métricas de rendimiento para ayudarle con la supervisión, el diagnóstico y la planificación de capacidad para los servidores Web: el componente API de servidor HTTP tiene los siguientes contadores de rendimiento para ayudarle con la supervisión, el diagnóstico y el planeamiento de capacidad para servidores Web:</span><span class="sxs-lookup"><span data-stu-id="6c842-108">Starting with Windows Vista and Windows Server 2008, HTTP.sys has the following performance metric counters to help you with monitoring, diagnosing, and capacity planning for Web servers: The HTTP Server API component has the following performance counters to help you with monitoring, diagnosing, and capacity planning for Web servers:</span></span>

- <span data-ttu-id="6c842-109">Contadores de servicios HTTP:</span><span class="sxs-lookup"><span data-stu-id="6c842-109">HTTP Service Counters:</span></span>
  - <span data-ttu-id="6c842-110">Número de URI en la memoria caché, agregados desde el inicio, eliminados desde el inicio y número de vaciados de caché</span><span class="sxs-lookup"><span data-stu-id="6c842-110">Number of URIs in the cache, added since startup, deleted since startup, and number of cache flushes</span></span>
  - <span data-ttu-id="6c842-111">Aciertos de caché/segundo y errores de caché por segundo</span><span class="sxs-lookup"><span data-stu-id="6c842-111">Cache hits/second and Cache misses/second</span></span>
- <span data-ttu-id="6c842-112">Grupos de direcciones URL del servicio HTTP:</span><span class="sxs-lookup"><span data-stu-id="6c842-112">HTTP Service URL Groups:</span></span>
  - <span data-ttu-id="6c842-113">Velocidad de envío de datos, velocidad de recepción de datos, bytes transferidos (enviados y recibidos)</span><span class="sxs-lookup"><span data-stu-id="6c842-113">Data send rate, data receive rate, bytes transferred (sent and received)</span></span>
  - <span data-ttu-id="6c842-114">Número máximo de conexiones, frecuencia de intentos de conexión, velocidad para solicitudes GET y HEAD y número total de solicitudes</span><span class="sxs-lookup"><span data-stu-id="6c842-114">Maximum number of connections, connection attempts rate, rate for GET and HEAD requests, and total number of requests</span></span>
- <span data-ttu-id="6c842-115">Colas de solicitudes de servicio HTTP:</span><span class="sxs-lookup"><span data-stu-id="6c842-115">HTTP Service Request Queues:</span></span>
  - <span data-ttu-id="6c842-116">Número de solicitudes en cola, antigüedad de las solicitudes más antiguas en la cola (antigüedad de la última solicitud en la cola)</span><span class="sxs-lookup"><span data-stu-id="6c842-116">Number of requests in queue, age of oldest requests in queue (age of the last request in the queue)</span></span>
  - <span data-ttu-id="6c842-117">Velocidad de llegada de la solicitud a la cola, tasa de rechazo, número total de solicitudes rechazadas, tasa de aciertos de caché</span><span class="sxs-lookup"><span data-stu-id="6c842-117">Rate of request arrivals into the queue, rate of rejection, total number of rejected requests, rate of cache hits</span></span>

<span data-ttu-id="6c842-118">**Obtener acceso a los contadores de rendimiento**</span><span class="sxs-lookup"><span data-stu-id="6c842-118">**Accessing Performance Counters**</span></span>

1.  <span data-ttu-id="6c842-119">Escriba **Perfmon** en el símbolo del sistema para iniciar la consola de diagnóstico de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="6c842-119">Type **perfmon** at the command prompt to start the Performance Diagnostic Console.</span></span>
2.  <span data-ttu-id="6c842-120">Seleccione **monitor de rendimiento** en el control de árbol y, a continuación, Abra **Agregar contadores** haciendo clic en **+** .</span><span class="sxs-lookup"><span data-stu-id="6c842-120">Select **Performance Monitor** in the tree control and then open the **Add Counters** by clicking **+**.</span></span>
3.  <span data-ttu-id="6c842-121">En **Agregar contadores** , seleccione entre los tres conjuntos de contadores de rendimiento: **servicio http**, **colas de solicitudes de servicio http** o **grupos de direcciones URL de servicio http**.</span><span class="sxs-lookup"><span data-stu-id="6c842-121">From **Add Counters** select from the three Performance Counters sets: **HTTP Service**, **HTTP Service Request Queues** , or **HTTP Service Url Groups**.</span></span>
4.  <span data-ttu-id="6c842-122">Para ver los contadores de los conjuntos de contadores **colas de solicitudes de servicio http** y **grupos de direcciones URL de servicio http** , seleccione **instancias** , haga clic en **Agregar** y, a continuación, haga clic en **Aceptar**.</span><span class="sxs-lookup"><span data-stu-id="6c842-122">To view counters from the **HTTP Service Request Queues** and **HTTP Service Url Groups** counter sets, select **instance(s)** and click **Add**, and then click **OK**.</span></span> <span data-ttu-id="6c842-123">Para ver los contadores de servicio HTTP, seleccione el conjunto de contadores en el panel izquierdo y haga clic en **Agregar**.</span><span class="sxs-lookup"><span data-stu-id="6c842-123">To view the HTTP Service counters, select the counter set in the left pane and click **Add**.</span></span>

> [!Note]  
> <span data-ttu-id="6c842-124">Solo existe una instancia de los contadores de API del servidor HTTP por equipo, ya que estos contadores representan el estado de todo el componente.</span><span class="sxs-lookup"><span data-stu-id="6c842-124">Only one instance of the HTTP Server API counters exists per machine, as these counters represent the component-wide state.</span></span> <span data-ttu-id="6c842-125">Con instancias de contadores de rendimiento de grupo de direcciones URL, el ID. de instancia (para el contador de rendimiento) coincidirá con el identificador de grupo de URL.</span><span class="sxs-lookup"><span data-stu-id="6c842-125">With instances of Url Group performance counters, the instance ID (for the performance counter) will match the Url Group ID.</span></span> <span data-ttu-id="6c842-126">El identificador de grupo de URL se puede ver ejecutando **netsh http show servicestate**.</span><span class="sxs-lookup"><span data-stu-id="6c842-126">The Url Group ID can be viewed by running **netsh http show servicestate**.</span></span> <span data-ttu-id="6c842-127">Con instancias de contadores de rendimiento de colas de solicitudes, el nombre de instancia corresponde al nombre de la cola de solicitudes.</span><span class="sxs-lookup"><span data-stu-id="6c842-127">With instances of Request Queues performance counters, the instance name corresponds to Request Queue Name.</span></span> <span data-ttu-id="6c842-128">El nombre de la cola de solicitudes (si existe) se puede mostrar en el mismo **netsh http show servicestate**.</span><span class="sxs-lookup"><span data-stu-id="6c842-128">The Request Queue Name (if one exists) can be shown by the same **netsh http show servicestate**.</span></span> <span data-ttu-id="6c842-129">Sin embargo, algunas aplicaciones de servidor pueden tener colas de solicitudes sin nombre que no se puedan asociar a un identificador de instancia de contador de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="6c842-129">However, some server applications may have unnamed Request Queues that cannot be matched to a performance counter instance ID.</span></span>

 

 

 




