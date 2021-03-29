---
title: Uso de Monitor de red para ver archivos ETL
description: Monitor de red 3,3 permite a los usuarios analizar, filtrar y ver un archivo ETL (con Windows Vista o posterior).
ms.assetid: 932be193-70f9-48f9-95d8-18916d3b7064
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04120f860654f4859aa930f32a4711999682eaf8
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/03/2021
ms.locfileid: "104003255"
---
# <a name="using-network-monitor-to-view-etl-files"></a><span data-ttu-id="39f64-103">Uso de Monitor de red para ver archivos ETL</span><span class="sxs-lookup"><span data-stu-id="39f64-103">Using Network Monitor to View ETL Files</span></span>

<span data-ttu-id="39f64-104">[Monitor de red 3,3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) permite a los usuarios analizar, filtrar y ver un archivo ETL (con Windows Vista o posterior).</span><span class="sxs-lookup"><span data-stu-id="39f64-104">[Network Monitor 3.3](https://connect.microsoft.com/site/sitehome.aspx?SiteID=216) enables users to parse, filter, and view an ETL file (using Windows Vista or later).</span></span> <span data-ttu-id="39f64-105">(Si usa Monitor de red 3,2, tendrá que descargar e instalar analizadores adicionales desde [CodePlex](https://www.codeplex.com/NMParsers) para representar los eventos de seguimiento de red).</span><span class="sxs-lookup"><span data-stu-id="39f64-105">(If using Network Monitor 3.2, you will need to download and install additional parsers from [CodePlex](https://www.codeplex.com/NMParsers) in order to render the network tracing events.)</span></span>

<span data-ttu-id="39f64-106">Los archivos ETL correlacionados agrupan los eventos correspondientes.</span><span class="sxs-lookup"><span data-stu-id="39f64-106">Correlated ETL files group the relevant events together.</span></span> <span data-ttu-id="39f64-107">En el ScrollBar siguiente se muestra un archivo correlacionado abierto en Monitor de red, con la conversación habilitada.</span><span class="sxs-lookup"><span data-stu-id="39f64-107">The illlustration below shows a correlated file opened in Network Monitor, with conversation enabled.</span></span>

![Captura de pantalla que muestra el Monitor de red, con eventos correlacionados resaltados en la ventana de la izquierda y UTEvent resaltados en la lista desplegable.](images/ut-netmon1.png)

<span data-ttu-id="39f64-109">Los eventos correlacionados se agrupan por actividad en el panel izquierdo.</span><span class="sxs-lookup"><span data-stu-id="39f64-109">Correlated events are grouped by activity in the left pane.</span></span> <span data-ttu-id="39f64-110">Puede seleccionar un evento en el panel de Resumen de fotogramas y, a continuación, hacer clic con el botón derecho para seleccionar la conversación en el nivel de evento de red.</span><span class="sxs-lookup"><span data-stu-id="39f64-110">You can select an event in the Frame Summary pane, then right-click to select the conversation at the network event level.</span></span> <span data-ttu-id="39f64-111">Esto mostrará una actividad relacionada en el panel izquierdo.</span><span class="sxs-lookup"><span data-stu-id="39f64-111">This will display a related activity in the left pane.</span></span>

<span data-ttu-id="39f64-112">Si selecciona una actividad determinada en el panel izquierdo y la expande, se mostrará la lista de proveedores de los eventos correlacionados.</span><span class="sxs-lookup"><span data-stu-id="39f64-112">Selecting a particular activity from the left pane and expanding it will show the list of providers for the correlated events.</span></span>

![Captura de pantalla que muestra el Monitor de red con una actividad seleccionada en el panel izquierdo y los eventos correspondientes a ese evento en el panel derecho.](images/ut-netmon2.png)

<span data-ttu-id="39f64-114">Al seleccionar un proveedor específico en el panel izquierdo, se mostrará una lista de eventos específicos de ese proveedor y actividad en el panel Resumen de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="39f64-114">When you select a specific provider in the left pane, a list of events specific to that provider and activity will be displayed in the Frame Summary pane.</span></span>

![Captura de pantalla que muestra un proveedor específico seleccionado en el panel izquierdo y una lista de eventos específicos del proveedor que se resaltan en el panel superior derecho.](images/ut-netmon3.png)

<span data-ttu-id="39f64-116">Los filtros se pueden aplicar en Monitor de red para que sea más fácil ver y encontrar los eventos o paquetes correctos.</span><span class="sxs-lookup"><span data-stu-id="39f64-116">Filters can be applied in Network Monitor to make it easier to view and find the right events or packet.</span></span> <span data-ttu-id="39f64-117">Por ejemplo, puede aplicar un filtro a los eventos de error seleccionados (por ejemplo, **UTEvent. header. descriptor. LEVEL = = 2**) para mostrarlos en un determinado color.</span><span class="sxs-lookup"><span data-stu-id="39f64-117">For example, you can apply a filter to selected error events (for example, **UTEvent.Header.Descriptor.Level == 2**) to display them in a certain color.</span></span>

![Captura de pantalla que muestra el cuadro de diálogo "editar filtro de color".](images/ut-netmon4.png)

<span data-ttu-id="39f64-119">Los filtros también se pueden aplicar para marcar diferentes proveedores en diferentes colores para que los resultados sean más fáciles de ver.</span><span class="sxs-lookup"><span data-stu-id="39f64-119">Filters can also be applied to mark different providers in different colors so that the results are easier to view.</span></span>

![Captura de pantalla que muestra un ejemplo de distintos proveedores marcados con distintos colores.](images/ut-netmon5.png)

<span data-ttu-id="39f64-121">Para aplicar un filtro, haga clic en **ColorFilters** en el menú **filtros** .</span><span class="sxs-lookup"><span data-stu-id="39f64-121">To apply a filter, click **ColorFilters** on the **Filters** menu.</span></span>

<span data-ttu-id="39f64-122">En la tabla siguiente se muestran algunos ejemplos de filtros útiles.</span><span class="sxs-lookup"><span data-stu-id="39f64-122">The following table shows some examples of useful filters.</span></span>



| <span data-ttu-id="39f64-123">Filter</span><span class="sxs-lookup"><span data-stu-id="39f64-123">Filter</span></span>                                                                        | <span data-ttu-id="39f64-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="39f64-124">Description</span></span>                                                       |
|-------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="39f64-125">UTEvent. header. descriptor. LEVEL = = 2</span><span class="sxs-lookup"><span data-stu-id="39f64-125">UTEvent.Header.Descriptor.Level == 2</span></span>                                          | <span data-ttu-id="39f64-126">Filtra solo los eventos de error.</span><span class="sxs-lookup"><span data-stu-id="39f64-126">Filters only error events.</span></span>                                        |
| <span data-ttu-id="39f64-127">UTEvent. header. descriptor. Level = = 3</span><span class="sxs-lookup"><span data-stu-id="39f64-127">UTEvent.Header.Descriptor.Level == 3</span></span>                                          | <span data-ttu-id="39f64-128">Filtra solo los eventos de advertencia.</span><span class="sxs-lookup"><span data-stu-id="39f64-128">Filters only warning events.</span></span>                                      |
| <span data-ttu-id="39f64-129">UTEvent.Header.Descriptor.Id = = 2001</span><span class="sxs-lookup"><span data-stu-id="39f64-129">UTEvent.Header.Descriptor.Id == 2001</span></span>                                          | <span data-ttu-id="39f64-130">Filtra solo los eventos con el ID. de evento 2001.</span><span class="sxs-lookup"><span data-stu-id="39f64-130">Filters only events with event ID 2001.</span></span>                           |
| <span data-ttu-id="39f64-131">MicrosoftWindowsWLANAutoConfig de WLAN \_</span><span class="sxs-lookup"><span data-stu-id="39f64-131">WLAN\_MicrosoftWindowsWLANAutoConfig</span></span>                                          | <span data-ttu-id="39f64-132">Filtra solo los eventos del servicio WLAN.</span><span class="sxs-lookup"><span data-stu-id="39f64-132">Filters only events from WLAN service.</span></span>                            |
| <span data-ttu-id="39f64-133">N802 \_ MicrosoftWindowsNWiFi</span><span class="sxs-lookup"><span data-stu-id="39f64-133">N802\_MicrosoftWindowsNWiFi</span></span>                                                   | <span data-ttu-id="39f64-134">Filtra solo los eventos del controlador WIFI nativo.</span><span class="sxs-lookup"><span data-stu-id="39f64-134">Filters only events from the Native Wifi driver.</span></span>                  |
| <span data-ttu-id="39f64-135">WLAN \_ MICROSOFTWINDOWSWLANAUTOCONFIG y UTEvent.header.descriptor.ID = = 2001</span><span class="sxs-lookup"><span data-stu-id="39f64-135">WLAN\_MicrosoftWindowsWLANAutoConfig AND UTEvent.Header.Descriptor.Id == 2001</span></span> | <span data-ttu-id="39f64-136">Filtra solo los eventos con el ID. de evento 2001 emitido desde el servicio WLAN.</span><span class="sxs-lookup"><span data-stu-id="39f64-136">Filters only events with event ID 2001 emitted from WLAN service.</span></span> |



 

 

 




