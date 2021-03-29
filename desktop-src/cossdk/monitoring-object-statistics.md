---
description: Puede supervisar las estadísticas de objetos a medida que se ejecuta una aplicación. Al hacerlo, puede ajustar las características del grupo de objetos para lograr el equilibrio en el rendimiento y los recursos que desea tener.
ms.assetid: 57987cc1-8bb5-4bbd-a425-fda2e5a8b597
title: Supervisión de estadísticas de objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f438bc7081546083f1930fe31f16a2198b09b48
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360039"
---
# <a name="monitoring-object-statistics"></a><span data-ttu-id="f8a3a-104">Supervisión de estadísticas de objetos</span><span class="sxs-lookup"><span data-stu-id="f8a3a-104">Monitoring Object Statistics</span></span>

<span data-ttu-id="f8a3a-105">Puede supervisar las estadísticas de objetos a medida que se ejecuta una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f8a3a-105">You can monitor object statistics as an application runs.</span></span> <span data-ttu-id="f8a3a-106">Al hacerlo, puede ajustar las características del grupo de objetos para lograr el equilibrio en el rendimiento y los recursos que desea tener.</span><span class="sxs-lookup"><span data-stu-id="f8a3a-106">By doing so, you can fine-tune the object pool characteristics to achieve the balance in performance and resources that you would like to have.</span></span>

<span data-ttu-id="f8a3a-107">Puede supervisar el estado de los objetos configurados para admitir las estadísticas de objetos y los informes de eventos.</span><span class="sxs-lookup"><span data-stu-id="f8a3a-107">You can monitor status for any objects that are configured to support object statistics and event reporting.</span></span> <span data-ttu-id="f8a3a-108">Habilitar las estadísticas de objetos tiene una pequeña sobrecarga de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f8a3a-108">Enabling object statistics has a very slight performance overhead.</span></span>

<span data-ttu-id="f8a3a-109">**Para habilitar las estadísticas de objetos**</span><span class="sxs-lookup"><span data-stu-id="f8a3a-109">**To enable object statistics**</span></span>

1.  <span data-ttu-id="f8a3a-110">En el panel de detalles de la herramienta administrativa Servicios de componentes, haga clic con el botón secundario en el componente que desee configurar y, a continuación, haga clic en **propiedades**.</span><span class="sxs-lookup"><span data-stu-id="f8a3a-110">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>

2.  <span data-ttu-id="f8a3a-111">En el cuadro de diálogo Propiedades de componente, haga clic en la pestaña **activación** .</span><span class="sxs-lookup"><span data-stu-id="f8a3a-111">In the component properties dialog box, click the **Activation** tab.</span></span>

3.  <span data-ttu-id="f8a3a-112">Para habilitar las estadísticas de objetos para el componente, en **contexto de activación**, active la casilla el **componente admite eventos y estadísticas** .</span><span class="sxs-lookup"><span data-stu-id="f8a3a-112">To enable object statistics for the component, under **Activation Context**, select the **Component supports events and statistics** check box.</span></span>

<span data-ttu-id="f8a3a-113">**Para supervisar el estado de los objetos**</span><span class="sxs-lookup"><span data-stu-id="f8a3a-113">**To monitor object status**</span></span>

1.  <span data-ttu-id="f8a3a-114">En el árbol de consola de la herramienta administrativa Servicios de componentes, abra la carpeta de la aplicación que incluye los componentes que desea supervisar.</span><span class="sxs-lookup"><span data-stu-id="f8a3a-114">In the console tree of the Component Services administrative tool, open the folder for the application that includes the components you want to monitor.</span></span>

2.  <span data-ttu-id="f8a3a-115">Haga clic con el botón secundario en la carpeta **componentes** , elija **Ver** y, a continuación, haga clic en **vista estado**.</span><span class="sxs-lookup"><span data-stu-id="f8a3a-115">Right-click the **Components** folder, point to **View**, and then click **Status View**.</span></span> <span data-ttu-id="f8a3a-116">En el panel de detalles se muestra ahora la vista de estado de todos los componentes de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="f8a3a-116">The details pane now displays the status view for all components in the application.</span></span> <span data-ttu-id="f8a3a-117">En la tabla siguiente se describen las seis columnas de la vista de estado.</span><span class="sxs-lookup"><span data-stu-id="f8a3a-117">The following table describes the six columns in the status view.</span></span>

    

    | <span data-ttu-id="f8a3a-118">Columna</span><span class="sxs-lookup"><span data-stu-id="f8a3a-118">Column</span></span>                        | <span data-ttu-id="f8a3a-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="f8a3a-119">Description</span></span>                                                                                                                                                                                                                |
    |-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="f8a3a-120">**ProgID**</span><span class="sxs-lookup"><span data-stu-id="f8a3a-120">**ProgID**</span></span><br/>         | <span data-ttu-id="f8a3a-121">Identifica un componente específico.</span><span class="sxs-lookup"><span data-stu-id="f8a3a-121">Identifies a specific component.</span></span><br/>                                                                                                                                                                                |
    | <span data-ttu-id="f8a3a-122">**Objects**</span><span class="sxs-lookup"><span data-stu-id="f8a3a-122">**Objects**</span></span><br/>        | <span data-ttu-id="f8a3a-123">Muestra el número de objetos que se encuentran actualmente en referencias de cliente.</span><span class="sxs-lookup"><span data-stu-id="f8a3a-123">Shows the number of objects that are currently held by client references.</span></span><br/>                                                                                                                                       |
    | <span data-ttu-id="f8a3a-124">**Desactiva**</span><span class="sxs-lookup"><span data-stu-id="f8a3a-124">**Activated**</span></span><br/>      | <span data-ttu-id="f8a3a-125">Muestra el número de objetos que están activados actualmente.</span><span class="sxs-lookup"><span data-stu-id="f8a3a-125">Shows the number of objects that are currently activated.</span></span> <br/>                                                                                                                                                      |
    | <span data-ttu-id="f8a3a-126">**Agrupados**</span><span class="sxs-lookup"><span data-stu-id="f8a3a-126">**Pooled**</span></span><br/>         | <span data-ttu-id="f8a3a-127">Muestra el número total de objetos creados por el grupo, incluidos los objetos que están en uso y los objetos que están desactivados.</span><span class="sxs-lookup"><span data-stu-id="f8a3a-127">Shows the total number of objects created by the pool, including objects that are in use and objects that are deactivated.</span></span><br/>                                                                                      |
    | <span data-ttu-id="f8a3a-128">**En la llamada**</span><span class="sxs-lookup"><span data-stu-id="f8a3a-128">**In Call**</span></span><br/>        | <span data-ttu-id="f8a3a-129">Identifica los objetos de la llamada.</span><span class="sxs-lookup"><span data-stu-id="f8a3a-129">Identifies objects in call.</span></span><br/>                                                                                                                                                                                     |
    | <span data-ttu-id="f8a3a-130">**Tiempo de llamada (MS)**</span><span class="sxs-lookup"><span data-stu-id="f8a3a-130">**Call Time (ms)**</span></span><br/> | <span data-ttu-id="f8a3a-131">Muestra la duración media de la llamada (en milisegundos) de las llamadas a métodos realizadas en los últimos 20 segundos (hasta 20 llamadas).</span><span class="sxs-lookup"><span data-stu-id="f8a3a-131">Shows the average call duration (in milliseconds) of method calls made in the last 20 seconds (up to 20 calls).</span></span> <span data-ttu-id="f8a3a-132">El tiempo de llamada se mide en el objeto y no incluye el tiempo usado para atravesar la red.</span><span class="sxs-lookup"><span data-stu-id="f8a3a-132">Call time is measured at the object and does not include the time used to traverse the network.</span></span><br/> |

    

     

## <a name="related-topics"></a><span data-ttu-id="f8a3a-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f8a3a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8a3a-134">Configuración de un componente que se va a agrupar</span><span class="sxs-lookup"><span data-stu-id="f8a3a-134">Configuring a Component to Be Pooled</span></span>](configuring-a-component-to-be-pooled.md)
</dt> </dl>

 

 




