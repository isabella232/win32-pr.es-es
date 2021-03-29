---
title: Grupo de pestañas
description: Un grupo de pestañas es un control contextual que se oculta o se muestra en tiempo de ejecución, en función del estado del documento o del área de trabajo. El grupo de pestañas contiene un conjunto de controles de ficha relacionados con el contexto.
ms.assetid: 5b74ff46-2543-43f3-ab42-dab1bc67a75e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253c803a07c0d27692442ddb7a291930a261a2ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359265"
---
# <a name="tab-group"></a><span data-ttu-id="65832-104">Grupo de pestañas</span><span class="sxs-lookup"><span data-stu-id="65832-104">Tab Group</span></span>

<span data-ttu-id="65832-105">Un grupo de pestañas es un control contextual que se oculta o se muestra en tiempo de ejecución, en función del estado del documento o del área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="65832-105">A Tab Group is a contextual control that is hidden or displayed at run time, based on a document or workspace state.</span></span> <span data-ttu-id="65832-106">El grupo de pestañas contiene un conjunto de controles de [ficha](windowsribbon-controls-tab.md) relacionados con el contexto.</span><span class="sxs-lookup"><span data-stu-id="65832-106">The Tab Group contains a set of context-related [Tab](windowsribbon-controls-tab.md) controls.</span></span>

-   [<span data-ttu-id="65832-107">Detalles</span><span class="sxs-lookup"><span data-stu-id="65832-107">Details</span></span>](#details)
-   [<span data-ttu-id="65832-108">Propiedades del grupo de pestañas</span><span class="sxs-lookup"><span data-stu-id="65832-108">Tab Group Properties</span></span>](#tab-group-properties)
-   [<span data-ttu-id="65832-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="65832-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="65832-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="65832-110">Details</span></span>

<span data-ttu-id="65832-111">Normalmente, se muestra un grupo de pestañas durante los Estados específicos del documento o del área de trabajo, como cuando un usuario selecciona un tipo de objeto determinado.</span><span class="sxs-lookup"><span data-stu-id="65832-111">Typically, a Tab Group is displayed during specific document or workspace states, such as when a user selects a particular object type.</span></span> <span data-ttu-id="65832-112">Por ejemplo, la selección de una imagen contenida en el encabezado de una tabla podría requerir que se muestren varias pestañas contextuales que exponen la funcionalidad de tabla e imagen.</span><span class="sxs-lookup"><span data-stu-id="65832-112">For example, the selection of an image contained in the header of a table might require various contextual tabs to be displayed that expose both table and image functionality.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="65832-113">Un grupo de pestañas no admite los [modos de aplicación](ribbon-applicationmodes.md).</span><span class="sxs-lookup"><span data-stu-id="65832-113">A Tab Group does not support [application modes](ribbon-applicationmodes.md).</span></span> <span data-ttu-id="65832-114">Sin embargo, los controles de [ficha](windowsribbon-controls-tab.md) individuales dentro de un grupo de pestañas pueden.</span><span class="sxs-lookup"><span data-stu-id="65832-114">However, the individual [Tab](windowsribbon-controls-tab.md) controls within a Tab Group may.</span></span>

 

<span data-ttu-id="65832-115">En la siguiente captura de pantalla se muestra una [pestaña](windowsribbon-controls-tab.md) contextual de Paint de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="65832-115">The following screen shot shows a contextual [Tab](windowsribbon-controls-tab.md) from Windows 7 Paint.</span></span>

![captura de pantalla que muestra un control de pestaña contextual.](images/controls/contextualtab.png)

## <a name="tab-group-properties"></a><span data-ttu-id="65832-117">Propiedades del grupo de pestañas</span><span class="sxs-lookup"><span data-stu-id="65832-117">Tab Group Properties</span></span>

<span data-ttu-id="65832-118">El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de grupo de pestañas.</span><span class="sxs-lookup"><span data-stu-id="65832-118">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Tab Group control.</span></span>

<span data-ttu-id="65832-119">Normalmente, una propiedad de grupo de pestañas se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="65832-119">Typically, a Tab Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="65832-120">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="65832-120">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="65832-121">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="65832-121">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="65832-122">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="65832-122">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="65832-123">En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="65832-123">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="65832-124">En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de grupo de pestañas.</span><span class="sxs-lookup"><span data-stu-id="65832-124">The following table lists the property keys that are associated with the Tab Group control.</span></span>



| <span data-ttu-id="65832-125">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="65832-125">Property Key</span></span>                                                                                     | <span data-ttu-id="65832-126">Notas</span><span class="sxs-lookup"><span data-stu-id="65832-126">Notes</span></span>                                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="65832-127">UI \_ PKEY \_ ContextAvailable</span><span class="sxs-lookup"><span data-stu-id="65832-127">UI\_PKEY\_ContextAvailable</span></span>](windowsribbon-reference-properties-uipkey-contextavailable.md)     | <span data-ttu-id="65832-128">Admite [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="65832-128">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="65832-129">KeyTip de UI \_ PKEY \_</span><span class="sxs-lookup"><span data-stu-id="65832-129">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="65832-130">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="65832-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="65832-131">\_Etiqueta PKEY de IU \_</span><span class="sxs-lookup"><span data-stu-id="65832-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="65832-132">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="65832-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="65832-133">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="65832-133">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="65832-134">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="65832-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="65832-135">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="65832-135">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="65832-136">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="65832-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="65832-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="65832-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65832-138">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="65832-138">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="65832-139">**Elemento de marcado TabGroup**</span><span class="sxs-lookup"><span data-stu-id="65832-139">**TabGroup markup element**</span></span>](windowsribbon-element-tabgroup.md)
</dt> </dl>

 

 