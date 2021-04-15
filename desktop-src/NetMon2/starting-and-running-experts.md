---
description: Al hacer clic en ejecutar expertos en la ventana expertos de la interfaz de usuario de Monitor de red se inician los expertos seleccionados para el archivo de captura y se llama a la función ejecutar. Cuando se inicia, el experto analiza el archivo de captura mediante el uso de varias funciones de marco de experto.
ms.assetid: 6b8a66cb-d1d6-4e19-b668-049a03a40804
title: Expertos en Inicio y en ejecución
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bd41472d286727541d26bade1942eb3b6b5c593
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688632"
---
# <a name="starting-and-running-experts"></a><span data-ttu-id="42141-104">Expertos en Inicio y en ejecución</span><span class="sxs-lookup"><span data-stu-id="42141-104">Starting and Running Experts</span></span>

<span data-ttu-id="42141-105">Al hacer clic en **Ejecutar expertos** en la ventana expertos de la interfaz de usuario de monitor de red se inician los expertos seleccionados para el archivo de captura y se llama a la función [**Ejecutar**](run.md) .</span><span class="sxs-lookup"><span data-stu-id="42141-105">Clicking **Run Experts** from the Experts window of the Network Monitor UI starts the experts selected for the capture file and calls the [**Run**](run.md) function.</span></span> <span data-ttu-id="42141-106">Cuando se inicia, el experto analiza el archivo de captura mediante el uso de varias funciones de marco de experto.</span><span class="sxs-lookup"><span data-stu-id="42141-106">When started, the expert analyzes the capture file by using several expert frame functions.</span></span>

<span data-ttu-id="42141-107">La función [**ExpertIndicateStatus**](expertindicatestatus.md) proporciona información de estado del experto.</span><span class="sxs-lookup"><span data-stu-id="42141-107">The [**ExpertIndicateStatus**](expertindicatestatus.md) function provides status information from the expert.</span></span> <span data-ttu-id="42141-108">Al ejecutar un experto con Monitor de red, la ventana vista de estado de experto muestra información de estado actualizada periódicamente (de 0 a 100% de finalización).</span><span class="sxs-lookup"><span data-stu-id="42141-108">When you run an expert with Network Monitor, the Expert Status View window displays periodically updated status information (from 0 to 100 percent completion).</span></span>

![ventana vista de estado de experto](images/exview.png)

<span data-ttu-id="42141-110">El experto está activo hasta que los datos completan su paso a través del archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="42141-110">The expert is active until the data completes its pass though the capture file.</span></span> <span data-ttu-id="42141-111">Cuando se complete el paso, aparecerá una ventana de Visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="42141-111">When the pass is complete, an Event Viewer window appears.</span></span> <span data-ttu-id="42141-112">La información de esta ventana depende del tipo de experto que ha analizado los datos.</span><span class="sxs-lookup"><span data-stu-id="42141-112">The information in this window depends on the type of expert that analyzed the data.</span></span> <span data-ttu-id="42141-113">En la ilustración siguiente se muestra una vista experta de distribución de propiedades, que resume los datos del marco analizados por el experto.</span><span class="sxs-lookup"><span data-stu-id="42141-113">The following illustration shows a Property Distribution Expert view, which summarizes the frame data that the expert analyzed.</span></span>

![vista de experto de distribución de propiedades](images/exview1.png)

<span data-ttu-id="42141-115">Un segundo informe (no se muestra), resume los resultados del experto de retransmisión del Protocolo de control de transmisión (TCP).</span><span class="sxs-lookup"><span data-stu-id="42141-115">A second report (not shown), summarizes the results of the Transmission Control Protocol (TCP) Retransmit expert.</span></span>

<span data-ttu-id="42141-116">También puede:</span><span class="sxs-lookup"><span data-stu-id="42141-116">You can also:</span></span>

-   <span data-ttu-id="42141-117">Cree una entrada para una página de referencia de eventos (ERP) que aconseje al usuario las condiciones o problemas detectados (como se muestra en la ventana de análisis).</span><span class="sxs-lookup"><span data-stu-id="42141-117">Create an entry for an event reference page (ERP) that advises the user of detected conditions or problems (as shown in the Analysis window).</span></span>
-   <span data-ttu-id="42141-118">Cree entradas para correcciones o datos explicativos sugeridos que proporcionen información adicional (como se muestra en la ventana de resolución).</span><span class="sxs-lookup"><span data-stu-id="42141-118">Create entries for suggested fixes or explanatory data that provide additional information (as shown in the Resolution window).</span></span>

<span data-ttu-id="42141-119">Una vez que el experto completa su tarea, Monitor de red quita el experto de la memoria activa.</span><span class="sxs-lookup"><span data-stu-id="42141-119">After the expert completes its task, Network Monitor removes the expert from active memory.</span></span> <span data-ttu-id="42141-120">Los expertos deben usar las funciones de memoria protegida incluidas en el kit de desarrollo de software (SDK) de la plataforma. Estas funciones limpian la memoria si se produce un error en los expertos durante el tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="42141-120">Experts should use the protected memory functions included in the Platform Software Development Kit (SDK); these functions clean up memory if the experts fail during run time.</span></span>

 

 



