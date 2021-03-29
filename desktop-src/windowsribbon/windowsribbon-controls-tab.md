---
title: Tabulador (marco de cinta de Windows)
description: Una pestaña contiene grupos de controles relacionados.
ms.assetid: 7315ca96-73c8-4ea1-bce0-172ebc4dd43a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b760bfc0c588c71ee9dbffa32b6cebc12a39fea7
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359648"
---
# <a name="tab-windows-ribbon-framework"></a><span data-ttu-id="d7b6c-103">Tabulador (marco de cinta de Windows)</span><span class="sxs-lookup"><span data-stu-id="d7b6c-103">Tab (Windows Ribbon Framework)</span></span>

<span data-ttu-id="d7b6c-104">Una pestaña contiene [grupos](windowsribbon-controls-group.md) de controles relacionados.</span><span class="sxs-lookup"><span data-stu-id="d7b6c-104">A Tab contains [groups](windowsribbon-controls-group.md) of related controls.</span></span>

-   [<span data-ttu-id="d7b6c-105">Detalles</span><span class="sxs-lookup"><span data-stu-id="d7b6c-105">Details</span></span>](#details)
-   [<span data-ttu-id="d7b6c-106">Propiedades de la ficha</span><span class="sxs-lookup"><span data-stu-id="d7b6c-106">Tab Properties</span></span>](#tab-properties)
-   [<span data-ttu-id="d7b6c-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7b6c-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="d7b6c-108">Detalles</span><span class="sxs-lookup"><span data-stu-id="d7b6c-108">Details</span></span>

<span data-ttu-id="d7b6c-109">Hay tres tipos de pestaña en el marco de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="d7b6c-109">There are three types of Tab in the Ribbon framework.</span></span>



| <span data-ttu-id="d7b6c-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="d7b6c-110">Type</span></span>               | <span data-ttu-id="d7b6c-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7b6c-111">Description</span></span>                                                                                                                                                                                                                                                                         |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7b6c-112">**Pestaña principal**</span><span class="sxs-lookup"><span data-stu-id="d7b6c-112">**Core tab**</span></span>       | <span data-ttu-id="d7b6c-113">Pestañas principales que organizan las funciones predeterminadas de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="d7b6c-113">Core tabs that organize the default functions of the application.</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="d7b6c-114">**Pestaña contextual**</span><span class="sxs-lookup"><span data-stu-id="d7b6c-114">**Contextual tab**</span></span> | <span data-ttu-id="d7b6c-115">Pestañas que se muestran durante los Estados específicos del documento o del área de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d7b6c-115">Tabs that are displayed during specific document or workspace states.</span></span> <span data-ttu-id="d7b6c-116">Por ejemplo, si un usuario selecciona un tipo de objeto determinado, como una imagen contenida en el encabezado de una tabla, pueden mostrarse varias pestañas contextuales que exponen la funcionalidad de tabla e imagen.</span><span class="sxs-lookup"><span data-stu-id="d7b6c-116">For example, if a user selects a particular object type, such as an image contained in the header of a table, then various contextual tabs might be displayed that expose both table and image functionality.</span></span> |
| <span data-ttu-id="d7b6c-117">**Pestaña modal**</span><span class="sxs-lookup"><span data-stu-id="d7b6c-117">**Modal tab**</span></span>      | <span data-ttu-id="d7b6c-118">Pestañas principales que se muestran durante un documento o [modo de aplicación](ribbon-applicationmodes.md)de área de trabajo específico, como la vista previa de impresión.</span><span class="sxs-lookup"><span data-stu-id="d7b6c-118">Core tabs that are displayed during a specific document or workspace [application mode](ribbon-applicationmodes.md), such as print preview.</span></span>                                                                                                                                        |



 

<span data-ttu-id="d7b6c-119">En la siguiente captura de pantalla se muestra una pestaña básica de Paint de Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d7b6c-119">The following screen shot shows a core Tab from Windows 7 Paint.</span></span>

![captura de pantalla que muestra un control de ficha principal.](images/controls/coretab.png)

## <a name="tab-properties"></a><span data-ttu-id="d7b6c-121">Propiedades de la ficha</span><span class="sxs-lookup"><span data-stu-id="d7b6c-121">Tab Properties</span></span>

<span data-ttu-id="d7b6c-122">El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de pestaña.</span><span class="sxs-lookup"><span data-stu-id="d7b6c-122">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Tab control.</span></span>

<span data-ttu-id="d7b6c-123">Normalmente, una propiedad de ficha se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="d7b6c-123">Typically, a Tab property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="d7b6c-124">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="d7b6c-124">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="d7b6c-125">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="d7b6c-125">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="d7b6c-126">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="d7b6c-126">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="d7b6c-127">En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="d7b6c-127">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="d7b6c-128">En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de pestaña.</span><span class="sxs-lookup"><span data-stu-id="d7b6c-128">The following table lists the property keys that are associated with the Tab control.</span></span>



| <span data-ttu-id="d7b6c-129">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="d7b6c-129">Property Key</span></span>                                                                                     | <span data-ttu-id="d7b6c-130">Notas</span><span class="sxs-lookup"><span data-stu-id="d7b6c-130">Notes</span></span>                                     |
|--------------------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="d7b6c-131">\_Etiqueta PKEY de IU \_</span><span class="sxs-lookup"><span data-stu-id="d7b6c-131">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                           | <span data-ttu-id="d7b6c-132">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="d7b6c-132">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="d7b6c-133">KeyTip de UI \_ PKEY \_</span><span class="sxs-lookup"><span data-stu-id="d7b6c-133">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                         | <span data-ttu-id="d7b6c-134">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="d7b6c-134">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="d7b6c-135">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="d7b6c-135">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md) | <span data-ttu-id="d7b6c-136">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="d7b6c-136">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="d7b6c-137">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="d7b6c-137">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)             | <span data-ttu-id="d7b6c-138">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="d7b6c-138">Can only be updated through invalidation.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d7b6c-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7b6c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7b6c-140">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="d7b6c-140">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="d7b6c-141">**Elemento de marcado de tabulación**</span><span class="sxs-lookup"><span data-stu-id="d7b6c-141">**Tab markup element**</span></span>](windowsribbon-element-tab.md)
</dt> </dl>

 

 
