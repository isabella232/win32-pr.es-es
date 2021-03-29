---
title: Solución de problemas de conexiones a Internet
description: En este escenario, un usuario está intentando explorar www.msn.com con el protocolo HTTPS, pero no puede conectarse. Puede usar netsh y Monitor de red para recopilar y ver seguimientos con el fin de ayudar a determinar por qué se produjo un error en la conexión.
ms.assetid: e10fcc24-4670-461c-a145-3910c102e81f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753636c1186243a96e3cef5a4ab73244556daec4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903358"
---
# <a name="troubleshooting-internet-connections"></a><span data-ttu-id="f2d7d-104">Solución de problemas de conexiones a Internet</span><span class="sxs-lookup"><span data-stu-id="f2d7d-104">Troubleshooting Internet Connections</span></span>

<span data-ttu-id="f2d7d-105">En este escenario, un usuario está intentando explorar www.msn.com con el protocolo HTTPS, pero no puede conectarse.</span><span class="sxs-lookup"><span data-stu-id="f2d7d-105">In this scenario, a user is attempting to browse to www.msn.com using the https protocol, but is unable to connect.</span></span> <span data-ttu-id="f2d7d-106">Puede usar netsh y Monitor de red para recopilar y ver seguimientos con el fin de ayudar a determinar por qué se produjo un error en la conexión.</span><span class="sxs-lookup"><span data-stu-id="f2d7d-106">You can use Netsh and Network Monitor to collect and view traces in order to help determine why the connection failed.</span></span>

<span data-ttu-id="f2d7d-107">En primer lugar, puede usar Netsh para iniciar un seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f2d7d-107">First, you can use netsh to start a trace.</span></span> <span data-ttu-id="f2d7d-108">Al escribir **netsh Trace Start Scenario = InternetClient de seguimiento = MSN. ETL** se inicia el seguimiento de todos los proveedores habilitados en el escenario InternetClient y guarda los resultados en un archivo denominado MSN. ETL.</span><span class="sxs-lookup"><span data-stu-id="f2d7d-108">Typing **netsh trace start scenario = InternetClient tracefile=msn.etl** starts tracing for all of the providers enabled under the InternetClient scenario, saving the results to a file named msn.etl.</span></span> <span data-ttu-id="f2d7d-109">Después de usar un explorador Web para intentar llegar a www.msn.com, escribir **netsh Trace STOP** finaliza y correlaciona el archivo de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="f2d7d-109">After using a web browser to attempt to reach www.msn.com, typing **netsh trace stop** terminates and correlates the trace file.</span></span>

<span data-ttu-id="f2d7d-110">Después, puede abrir el archivo MSN. ETL en Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="f2d7d-110">You can then open the msn.etl file in Network Monitor.</span></span> <span data-ttu-id="f2d7d-111">Los eventos se agrupan por ID. de actividad en el panel izquierdo.</span><span class="sxs-lookup"><span data-stu-id="f2d7d-111">The events are grouped by activity ID in the left pane.</span></span> <span data-ttu-id="f2d7d-112">Con la descripción del filtro **. Contains ("MSN")** mostrará solo los eventos que incluyen la cadena "MSN" en la descripción del protocolo.</span><span class="sxs-lookup"><span data-stu-id="f2d7d-112">Using the filter **description.contains("msn")** will show only those events which include the string "msn" in their protocol description.</span></span>

![solución de problemas de conexiones a Internet con el monitor de red (1)](images/internetclient1.png)

<span data-ttu-id="f2d7d-114">A continuación, puede revisar los eventos en el Resumen de fotogramas para identificar un evento que parezca relevante.</span><span class="sxs-lookup"><span data-stu-id="f2d7d-114">Next, you can review the events in the frame summary to identify an event which looks relevant.</span></span> <span data-ttu-id="f2d7d-115">Después de seleccionar el evento, haga clic con el botón derecho y seleccione Buscar conversaciones y, luego, haga clic en UTEvent para seleccionar la conversación en el nivel de UTEvent.</span><span class="sxs-lookup"><span data-stu-id="f2d7d-115">After you select the event, right-click and point to Find Conversations, then click UTEvent to select the conversation at the UTEvent level.</span></span>

![solución de problemas de conexiones a Internet con el monitor de red (2)](images/internetclient2.png)

<span data-ttu-id="f2d7d-117">A continuación, se resalta la actividad normalizada asociada en el panel izquierdo, en este caso UTEvent ActivityID 397.</span><span class="sxs-lookup"><span data-stu-id="f2d7d-117">The associated normalized activity in the left pane is then highlighted, in this case UTEvent ActivityID 397.</span></span>

![solución de problemas de conexiones a Internet con el monitor de red (3)](images/internetclient3.png)

<span data-ttu-id="f2d7d-119">Al usar Monitor de red para ver y filtrar la información de seguimiento, el número de eventos que se van a examinar se ha reducido de 1989 a 96.</span><span class="sxs-lookup"><span data-stu-id="f2d7d-119">By using Network Monitor to view and filter the trace information, the number of events to examine has been reduced from 1989 to 96.</span></span>

 

 




