---
title: Solución de problemas de conexiones LAN inalámbricas
description: En este escenario, un usuario está intentando conectarse a una LAN inalámbrica, pero no puede conectarse. Puede usar netsh y Monitor de red para recopilar y ver seguimientos con el fin de ayudar a determinar por qué se produjo un error en la conexión.
ms.assetid: 558dae83-aa16-4751-a497-d7a0da01ce5d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55878afcee0091634415d4dbc465d1b143f46057
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076195"
---
# <a name="troubleshooting-wireless-lan-connections"></a><span data-ttu-id="eaaf2-104">Solución de problemas de conexiones LAN inalámbricas</span><span class="sxs-lookup"><span data-stu-id="eaaf2-104">Troubleshooting Wireless LAN Connections</span></span>

<span data-ttu-id="eaaf2-105">En este escenario, un usuario está intentando conectarse a una LAN inalámbrica, pero no puede conectarse.</span><span class="sxs-lookup"><span data-stu-id="eaaf2-105">In this scenario, a user is attempting to connect to a wireless LAN, but is unable to connect.</span></span> <span data-ttu-id="eaaf2-106">Puede usar netsh y Monitor de red para recopilar y ver seguimientos con el fin de ayudar a determinar por qué se produjo un error en la conexión.</span><span class="sxs-lookup"><span data-stu-id="eaaf2-106">You can use Netsh and Network Monitor to collect and view traces in order to help determine why the connection failed.</span></span>

<span data-ttu-id="eaaf2-107">En primer lugar, puede usar Netsh para iniciar un seguimiento.</span><span class="sxs-lookup"><span data-stu-id="eaaf2-107">First, you can use netsh to start a trace.</span></span> <span data-ttu-id="eaaf2-108">Escribiendo **netsh Trace Start Scenario = WLAN seguimiento = wlanwpp. ETL** inicia el seguimiento de todos los proveedores habilitados en el escenario de WLAN y guarda los resultados en un archivo denominado wlanwpp. ETL.</span><span class="sxs-lookup"><span data-stu-id="eaaf2-108">Typing **netsh trace start scenario = wlan tracefile=wlanwpp.etl** starts tracing for all of the providers enabled under the WLAN scenario, saving the results to a file named wlanwpp.etl.</span></span> <span data-ttu-id="eaaf2-109">Después de intentar conectarse a la LAN inalámbrica, escribir **netsh Trace STOP** finaliza y correlaciona el archivo de seguimiento.</span><span class="sxs-lookup"><span data-stu-id="eaaf2-109">After attempting to connect to the wireless LAN, typing **netsh trace stop** terminates and correlates the trace file.</span></span>

<span data-ttu-id="eaaf2-110">Después, puede abrir el archivo wlanwpp. ETL en Monitor de red.</span><span class="sxs-lookup"><span data-stu-id="eaaf2-110">You can then open the wlanwpp.etl file in Network Monitor.</span></span> <span data-ttu-id="eaaf2-111">Los eventos se agrupan por ID. de actividad en el panel izquierdo.</span><span class="sxs-lookup"><span data-stu-id="eaaf2-111">The events are grouped by activity ID in the left pane.</span></span>

![solución de problemas de conexiones LAN inalámbricas mediante el monitor de red (1)](images/1wlan.png)

<span data-ttu-id="eaaf2-113">ETL contiene muchos seguimientos de otros proveedores de red que están habilitados.</span><span class="sxs-lookup"><span data-stu-id="eaaf2-113">The ETL contains lot of traces from other network providers that are enabled.</span></span> <span data-ttu-id="eaaf2-114">Puede aplicar un filtro para mostrar solo los eventos que son relevantes para el proveedor **de \_ MicrosoftWindowsWlanAutoConfig de WLAN** .</span><span class="sxs-lookup"><span data-stu-id="eaaf2-114">You can apply a filter to display only those events which are relevant to the **WLAN\_MicrosoftWindowsWlanAutoConfig** provider.</span></span>

![solución de problemas de conexiones LAN inalámbricas mediante el monitor de red (2)](images/2wlan.png)

<span data-ttu-id="eaaf2-116">Una vez aplicado el filtro, puede revisar los eventos en el resumen del marco para identificar un evento que parezca relevante.</span><span class="sxs-lookup"><span data-stu-id="eaaf2-116">After the filter has been applied, you can review the events in the frame summary to identify an event which looks relevant.</span></span> <span data-ttu-id="eaaf2-117">Después de seleccionar el evento, haga clic con el botón derecho y seleccione Buscar conversaciones y, a continuación, haga clic en NetEvent.</span><span class="sxs-lookup"><span data-stu-id="eaaf2-117">After you select the event, right-click and point to Find Conversations, then click NetEvent.</span></span>

![solución de problemas de conexiones LAN inalámbricas mediante el monitor de red (3)](images/3wlan.png)

<span data-ttu-id="eaaf2-119">La expansión de los elementos en un ID. de actividad en el panel izquierdo le permitirá ver todos los demás proveedores relevantes para el intento de conexión.</span><span class="sxs-lookup"><span data-stu-id="eaaf2-119">Expanding the items under an activity ID in the left pane will allow you to view all of the other relevant providers for the connection attempt.</span></span> <span data-ttu-id="eaaf2-120">Para ver los eventos de otros proveedores, se quitan todos los filtros haciendo clic en **quitar** en el panel **Mostrar filtro** .</span><span class="sxs-lookup"><span data-stu-id="eaaf2-120">To view the events from other providers, all filters are removed by clicking **Remove** in the **Display Filter** pane.</span></span> <span data-ttu-id="eaaf2-121">Los seguimientos se pueden analizar desplazándose por el resumen del marco y seleccionando eventos adicionales según sea necesario para recopilar más información.</span><span class="sxs-lookup"><span data-stu-id="eaaf2-121">The traces can be analyzed by scrolling through the frame summary, selecting additional events as needed to gather more information.</span></span> <span data-ttu-id="eaaf2-122">En este caso, el panel Detalles del marco proporciona información de que el error se debe a un error de intercambio de claves, probablemente debido a que el usuario escribe la clave de paso equivocada.</span><span class="sxs-lookup"><span data-stu-id="eaaf2-122">In this case, the Frame Details pane provides information that the failure is due to key exchange failure, most likely due to the user entering the wrong pass key.</span></span>

 

 




