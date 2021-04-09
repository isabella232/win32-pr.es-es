---
title: Button (marco de cinta de Windows)
description: El botón es un control en el que el usuario puede hacer clic para proporcionar la entrada a una aplicación.
ms.assetid: 6d4aa571-dbea-4139-a6b7-45a85595dd04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1514a1ae66e383d18f81d1ca0ee1a5a8e453335d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149776"
---
# <a name="button-windows-ribbon-framework"></a><span data-ttu-id="7113d-103">Button (marco de cinta de Windows)</span><span class="sxs-lookup"><span data-stu-id="7113d-103">Button (Windows Ribbon Framework)</span></span>

<span data-ttu-id="7113d-104">El botón es un control en el que el usuario puede hacer clic para proporcionar la entrada a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="7113d-104">The Button is a control the user can click to provide input to an application.</span></span>

-   [<span data-ttu-id="7113d-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="7113d-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="7113d-106">Propiedades del botón</span><span class="sxs-lookup"><span data-stu-id="7113d-106">Button Properties</span></span>](#button-properties)
-   [<span data-ttu-id="7113d-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7113d-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="7113d-108">Introducción</span><span class="sxs-lookup"><span data-stu-id="7113d-108">Introduction</span></span>

<span data-ttu-id="7113d-109">La siguiente captura de pantalla contiene tres ejemplos del elemento botón de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="7113d-109">The following screen shot contains three examples of the Ribbon Button element.</span></span>

![captura de pantalla de los controles de botón en la cinta de opciones de WordPad de Microsoft.](images/controls/button.png)

## <a name="button-properties"></a><span data-ttu-id="7113d-111">Propiedades del botón</span><span class="sxs-lookup"><span data-stu-id="7113d-111">Button Properties</span></span>

<span data-ttu-id="7113d-112">El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de botón.</span><span class="sxs-lookup"><span data-stu-id="7113d-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Button control.</span></span>

<span data-ttu-id="7113d-113">Normalmente, una propiedad de botón se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="7113d-113">Typically, a Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="7113d-114">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="7113d-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="7113d-115">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="7113d-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="7113d-116">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="7113d-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="7113d-117">En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="7113d-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="7113d-118">En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de botón.</span><span class="sxs-lookup"><span data-stu-id="7113d-118">The following table lists the property keys that are associated with the Button control.</span></span>



| <span data-ttu-id="7113d-119">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="7113d-119">Property Key</span></span>                                                                                             | <span data-ttu-id="7113d-120">Notas</span><span class="sxs-lookup"><span data-stu-id="7113d-120">Notes</span></span>                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7113d-121">PKEY de IU \_ \_ habilitada</span><span class="sxs-lookup"><span data-stu-id="7113d-121">UI\_PKEY\_Enabled</span></span>](windowsribbon-reference-properties-uipkey-enabled.md)                               | <span data-ttu-id="7113d-122">Admite [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span><span class="sxs-lookup"><span data-stu-id="7113d-122">Supports [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) and [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty).</span></span> |
| [<span data-ttu-id="7113d-123">KeyTip de UI \_ PKEY \_</span><span class="sxs-lookup"><span data-stu-id="7113d-123">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)                                 | <span data-ttu-id="7113d-124">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7113d-124">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="7113d-125">\_Etiqueta PKEY de IU \_</span><span class="sxs-lookup"><span data-stu-id="7113d-125">UI\_PKEY\_Label</span></span>](windowsribbon-reference-properties-uipkey-label.md)                                   | <span data-ttu-id="7113d-126">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7113d-126">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="7113d-127">UI \_ PKEY \_ LabelDescription</span><span class="sxs-lookup"><span data-stu-id="7113d-127">UI\_PKEY\_LabelDescription</span></span>](windowsribbon-reference-properties-uipkey-labeldescription.md)             | <span data-ttu-id="7113d-128">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7113d-128">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="7113d-129">UI \_ PKEY \_ LargeHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="7113d-129">UI\_PKEY\_LargeHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-largehighcontrastimage.md) | <span data-ttu-id="7113d-130">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7113d-130">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="7113d-131">UI \_ PKEY \_ LargeImage</span><span class="sxs-lookup"><span data-stu-id="7113d-131">UI\_PKEY\_LargeImage</span></span>](windowsribbon-reference-properties-uipkey-largeimage.md)                         | <span data-ttu-id="7113d-132">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7113d-132">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="7113d-133">UI \_ PKEY \_ SmallHighContrastImage</span><span class="sxs-lookup"><span data-stu-id="7113d-133">UI\_PKEY\_SmallHighContrastImage</span></span>](windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md) | <span data-ttu-id="7113d-134">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7113d-134">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="7113d-135">UI \_ PKEY \_ SmallImage</span><span class="sxs-lookup"><span data-stu-id="7113d-135">UI\_PKEY\_SmallImage</span></span>](windowsribbon-reference-properties-uipkey-smallimage.md)                         | <span data-ttu-id="7113d-136">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7113d-136">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="7113d-137">UI \_ PKEY \_ TooltipDescription</span><span class="sxs-lookup"><span data-stu-id="7113d-137">UI\_PKEY\_TooltipDescription</span></span>](windowsribbon-reference-properties-uipkey-tooltipdescription.md)         | <span data-ttu-id="7113d-138">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7113d-138">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="7113d-139">UI \_ PKEY \_ TooltipTitle</span><span class="sxs-lookup"><span data-stu-id="7113d-139">UI\_PKEY\_TooltipTitle</span></span>](windowsribbon-reference-properties-uipkey-tooltiptitle.md)                     | <span data-ttu-id="7113d-140">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7113d-140">Can only be updated through invalidation.</span></span>                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="7113d-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7113d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7113d-142">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="7113d-142">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="7113d-143">**Elemento de marcado de botón**</span><span class="sxs-lookup"><span data-stu-id="7113d-143">**Button markup element**</span></span>](windowsribbon-element-button.md)
</dt> </dl>

 

 
