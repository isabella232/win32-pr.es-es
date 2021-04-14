---
title: Botón de alternancia
description: Al hacer clic en el botón de alternancia, se proporciona la entrada a una aplicación. El control representa un estado de alternancia mutuamente excluyente.
ms.assetid: 290052b7-0528-41c5-b6f4-958cc42d502b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d72c06f8382e7210f1041960b92de5f6054548d1
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104564341"
---
# <a name="toggle-button"></a><span data-ttu-id="e1c04-104">Botón de alternancia</span><span class="sxs-lookup"><span data-stu-id="e1c04-104">Toggle Button</span></span>

<span data-ttu-id="e1c04-105">Al hacer clic en el botón de alternancia, se proporciona la entrada a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e1c04-105">The Toggle Button when clicked provides input to an application.</span></span> <span data-ttu-id="e1c04-106">El control representa un estado de alternancia mutuamente excluyente.</span><span class="sxs-lookup"><span data-stu-id="e1c04-106">The control represents a mutually exclusive toggle state.</span></span>

-   [<span data-ttu-id="e1c04-107">Detalles</span><span class="sxs-lookup"><span data-stu-id="e1c04-107">Details</span></span>](#details)
-   [<span data-ttu-id="e1c04-108">Alternar propiedades del botón</span><span class="sxs-lookup"><span data-stu-id="e1c04-108">Toggle Button Properties</span></span>](#toggle-button-properties)
-   [<span data-ttu-id="e1c04-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1c04-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="e1c04-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="e1c04-110">Details</span></span>

<span data-ttu-id="e1c04-111">La siguiente captura de pantalla muestra el botón de alternancia de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="e1c04-111">The following screen shot illustrates the Ribbon Toggle Button.</span></span>

![captura de pantalla de un control ToggleButton en la cinta de opciones de Microsoft Paint.](images/controls/togglebutton.png)

## <a name="toggle-button-properties"></a><span data-ttu-id="e1c04-113">Alternar propiedades del botón</span><span class="sxs-lookup"><span data-stu-id="e1c04-113">Toggle Button Properties</span></span>

<span data-ttu-id="e1c04-114">El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de botón de alternancia.</span><span class="sxs-lookup"><span data-stu-id="e1c04-114">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Toggle Button control.</span></span>

<span data-ttu-id="e1c04-115">Normalmente, una propiedad de botón de alternancia se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="e1c04-115">Typically, a Toggle Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="e1c04-116">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="e1c04-116">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="e1c04-117">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e1c04-117">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="e1c04-118">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="e1c04-118">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="e1c04-119">En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="e1c04-119">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="e1c04-120">En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de botón de alternancia.</span><span class="sxs-lookup"><span data-stu-id="e1c04-120">The following table lists the property keys that are associated with the Toggle Button control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1c04-121">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="e1c04-121">Property Key</span></span></th>
<th><span data-ttu-id="e1c04-122">Notas</span><span class="sxs-lookup"><span data-stu-id="e1c04-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1c04-123"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span><span class="sxs-lookup"><span data-stu-id="e1c04-123"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span></span></td>
<td><span data-ttu-id="e1c04-124">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e1c04-124">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="e1c04-125">Si el comando asociado al control se invalida mediante una llamada a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework:: InvalidateUICommand</strong></a>, el marco consulta esta propiedad cuando <code>UI_INVALIDATIONS_VALUE</code> se pasa como el valor de <em>Flags</em>.</span><span class="sxs-lookup"><span data-stu-id="e1c04-125">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1c04-126"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="e1c04-126"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="e1c04-127">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="e1c04-127">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1c04-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="e1c04-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="e1c04-129">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="e1c04-129">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1c04-130"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="e1c04-130"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="e1c04-131">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="e1c04-131">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1c04-132"><a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a></span><span class="sxs-lookup"><span data-stu-id="e1c04-132"><a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a></span></span></td>
<td><span data-ttu-id="e1c04-133">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="e1c04-133">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1c04-134"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="e1c04-134"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="e1c04-135">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="e1c04-135">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1c04-136"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="e1c04-136"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="e1c04-137">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="e1c04-137">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1c04-138"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="e1c04-138"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="e1c04-139">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="e1c04-139">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1c04-140"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="e1c04-140"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="e1c04-141">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="e1c04-141">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1c04-142"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="e1c04-142"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="e1c04-143">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="e1c04-143">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1c04-144"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="e1c04-144"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="e1c04-145">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="e1c04-145">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="e1c04-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e1c04-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1c04-147">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="e1c04-147">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="e1c04-148">**Elemento de marcado ToggleButton**</span><span class="sxs-lookup"><span data-stu-id="e1c04-148">**ToggleButton markup element**</span></span>](windowsribbon-element-togglebutton.md)
</dt> </dl>

