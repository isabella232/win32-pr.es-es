---
title: Paneles de tareas de servicio
description: Paneles de tareas de servicio
ms.assetid: f626fa85-7590-4e87-bd5c-7ffdcb14be8b
keywords:
- Windows Media Player tiendas en línea, paneles de tareas de servicio
- tiendas en línea, paneles de tareas de servicio
- tipo 2 tiendas en línea, paneles de tareas de servicio
- Windows Media Player tiendas en línea, paneles de tareas
- tiendas en línea, paneles de tareas
- tipo 2 tiendas en línea, paneles de tareas
- Media Player de Windows, paneles de tareas de servicio
- Media Player de Windows, paneles de tareas
- paneles de tareas de servicio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4f882e46a7252792db5b551b25869c7711f9d31
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075868"
---
# <a name="service-task-panes"></a><span data-ttu-id="6145f-112">Paneles de tareas de servicio</span><span class="sxs-lookup"><span data-stu-id="6145f-112">Service Task Panes</span></span>

<span data-ttu-id="6145f-113">En Windows Media Player 10, los proveedores de tiendas en línea pueden configurar Windows Media Player para mostrar hasta tres paneles de tareas, denominados paneles de tareas de servicio.</span><span class="sxs-lookup"><span data-stu-id="6145f-113">In Windows Media Player 10, online store providers can configure Windows Media Player to display as many as three task panes, called service task panes.</span></span> <span data-ttu-id="6145f-114">Cada panel de tareas de servicio se representa mediante un botón personalizable que Windows Media Player muestra en el lado derecho de la barra de tareas de características.</span><span class="sxs-lookup"><span data-stu-id="6145f-114">Each service task pane is represented by a customizable button that Windows Media Player displays on the right side of the Features taskbar.</span></span>

<span data-ttu-id="6145f-115">Cada panel de tareas de servicio hospeda una página web que es la interfaz de usuario para una determinada característica de tienda en línea. La apariencia de los paneles de tareas de servicio se define mediante el documento XML de ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="6145f-115">Each service task pane hosts a webpage that is the user interface for a particular online store feature.The appearance of the service task panes is defined by the ServiceInfo XML document.</span></span> <span data-ttu-id="6145f-116">En este documento, los paneles de tareas de servicio se representan mediante tres elementos: **ServiceTask1**, **ServiceTask2** y **ServiceTask3**.</span><span class="sxs-lookup"><span data-stu-id="6145f-116">In this document, the service task panes are represented by three elements: **ServiceTask1**, **ServiceTask2**, and **ServiceTask3**.</span></span> <span data-ttu-id="6145f-117">Estos paneles de tareas de servicio están diseñados para proporcionar lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6145f-117">These service task panes are intended to provide the following:</span></span>

-   <span data-ttu-id="6145f-118">Un servicio de música.</span><span class="sxs-lookup"><span data-stu-id="6145f-118">A music service.</span></span>
-   <span data-ttu-id="6145f-119">Un servicio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6145f-119">A video service.</span></span>
-   <span data-ttu-id="6145f-120">Un servicio de radio.</span><span class="sxs-lookup"><span data-stu-id="6145f-120">A radio service.</span></span>

<span data-ttu-id="6145f-121">Puede colocar estas características en Windows Media Player en el orden que desee, pero **ServiceTask1** debe ser el panel de tareas principal para participar en la actividad comercial.</span><span class="sxs-lookup"><span data-stu-id="6145f-121">You can position these features in Windows Media Player in any order you like, but **ServiceTask1** must be the primary task pane for engaging in commercial activity.</span></span>

<span data-ttu-id="6145f-122">La página web hospedada en cada panel de tareas de servicio tiene acceso al objeto **externo** .</span><span class="sxs-lookup"><span data-stu-id="6145f-122">The webpage hosted in each service task pane has access to the **External** object.</span></span> <span data-ttu-id="6145f-123">Este objeto proporciona métodos, propiedades y un evento que proporcionan una funcionalidad especial para las páginas web en Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6145f-123">This object provides methods, properties, and an event that provide special functionality for webpages in Windows Media Player.</span></span> <span data-ttu-id="6145f-124">Por ejemplo, puede usar el evento y las propiedades de **externa** para que la apariencia de la página web coincida con la combinación de colores que el usuario haya elegido para Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="6145f-124">For instance, you can use the event and properties from **External** to make the appearance of your webpage match the color scheme that the user has chosen for Windows Media Player.</span></span>

<span data-ttu-id="6145f-125">En Windows Media Player 11, no hay paneles de tareas de servicio.</span><span class="sxs-lookup"><span data-stu-id="6145f-125">In Windows Media Player 11, there are no service task panes.</span></span> <span data-ttu-id="6145f-126">En su lugar, hay una sola pestaña **tiendas en línea** , que hospeda la página web principal de la tienda en línea activa.</span><span class="sxs-lookup"><span data-stu-id="6145f-126">Instead, there is a single **Online Stores** tab, which hosts the main webpage for the active online store.</span></span> <span data-ttu-id="6145f-127">En el documento ServiceInfo, la pestaña **tiendas en línea** se representa mediante el elemento **ServiceTask1** . se omiten los elementos **ServiceTask2** y **ServiceTask3** .</span><span class="sxs-lookup"><span data-stu-id="6145f-127">In the ServiceInfo document, the **Online Stores** tab is represented by the **ServiceTask1** element; the **ServiceTask2** and **ServiceTask3** elements are ignored.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6145f-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6145f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6145f-129">**Acerca de las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="6145f-129">**About Type 2 Online Stores**</span></span>](about-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="6145f-130">**Objeto externo para las tiendas en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="6145f-130">**External Object for Type 2 Online Stores**</span></span>](external-object-for-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="6145f-131">**Documento ServiceInfo para una tienda en línea de tipo 2**</span><span class="sxs-lookup"><span data-stu-id="6145f-131">**ServiceInfo Document for a Type 2 Online Store**</span></span>](serviceinfo-document-for-a-type-2-online-store.md)
</dt> </dl>

 

 




