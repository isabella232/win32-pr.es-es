---
title: Galería de In-Ribbon
description: La galería de In-Ribbon es un control que muestra una colección de elementos o comandos relacionados en la cinta de opciones. Si hay demasiados elementos en la galería, se proporciona una flecha de expansión para mostrar el resto de la colección en un panel expandido.
ms.assetid: d608dd0d-a0af-49a6-a129-7115195c0df2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef644128204fa0b20284dbb63368ef530b0dd0b3
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105676517"
---
# <a name="in-ribbon-gallery"></a><span data-ttu-id="5ab2f-104">Galería de In-Ribbon</span><span class="sxs-lookup"><span data-stu-id="5ab2f-104">In-Ribbon Gallery</span></span>

<span data-ttu-id="5ab2f-105">La galería de In-Ribbon es un control que muestra una colección de elementos o comandos relacionados en la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-105">The In-Ribbon Gallery is a control that displays a collection of related items or Commands in the Ribbon.</span></span> <span data-ttu-id="5ab2f-106">Si hay demasiados elementos en la galería, se proporciona una flecha de expansión para mostrar el resto de la colección en un panel expandido.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-106">If there are too many items in the gallery, an expand arrow is provided to display the rest of the collection in an expanded pane.</span></span>

-   [<span data-ttu-id="5ab2f-107">Detalles</span><span class="sxs-lookup"><span data-stu-id="5ab2f-107">Details</span></span>](#details)
-   [<span data-ttu-id="5ab2f-108">Propiedades de la galería de la cinta de opciones</span><span class="sxs-lookup"><span data-stu-id="5ab2f-108">In-Ribbon Gallery Properties</span></span>](#in-ribbon-gallery-properties)
-   [<span data-ttu-id="5ab2f-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ab2f-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="5ab2f-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="5ab2f-110">Details</span></span>

<span data-ttu-id="5ab2f-111">En la captura de pantalla siguiente se muestra el control Galería de In-Ribbon de la cinta de opciones de Microsoft Paint.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-111">The following screen shot illustrates the Ribbon In-Ribbon Gallery control in Microsoft Paint.</span></span>

![captura de pantalla de un control inribbongallery en la cinta de opciones de Microsoft Paint.](images/controls/inribbongallery.png)

## <a name="in-ribbon-gallery-properties"></a><span data-ttu-id="5ab2f-113">Propiedades de la galería de In-Ribbon</span><span class="sxs-lookup"><span data-stu-id="5ab2f-113">In-Ribbon Gallery Properties</span></span>

<span data-ttu-id="5ab2f-114">El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control galería de In-Ribbon.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-114">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the In-Ribbon Gallery control.</span></span>

<span data-ttu-id="5ab2f-115">Normalmente, una propiedad de la galería de In-Ribbon se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="5ab2f-115">Typically, an In-Ribbon Gallery property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="5ab2f-116">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="5ab2f-116">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="5ab2f-117">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-117">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="5ab2f-118">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-118">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="5ab2f-119">En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="5ab2f-119">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="5ab2f-120">En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control Galería de In-Ribbon.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-120">The following table lists the property keys that are associated with the In-Ribbon Gallery control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ab2f-121">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="5ab2f-121">Property Key</span></span></th>
<th><span data-ttu-id="5ab2f-122">Notas</span><span class="sxs-lookup"><span data-stu-id="5ab2f-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5ab2f-123"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="5ab2f-123"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="5ab2f-124">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-124">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ab2f-125"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="5ab2f-125"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="5ab2f-126">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-126">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ab2f-127"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="5ab2f-127"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="5ab2f-128">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-128">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ab2f-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="5ab2f-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="5ab2f-130">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ab2f-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="5ab2f-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="5ab2f-132">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ab2f-133"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="5ab2f-133"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="5ab2f-134">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ab2f-135"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="5ab2f-135"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="5ab2f-136">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ab2f-137"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(solo válido para una galería de elementos)</span><span class="sxs-lookup"><span data-stu-id="5ab2f-137"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(only valid for an item gallery)</span></span><br/></td>
<td><span data-ttu-id="5ab2f-138">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-138">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="5ab2f-139">Si el comando asociado al control se invalida mediante una llamada a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework:: InvalidateUICommand</strong></a>, el marco consulta esta propiedad cuando <code>UI_INVALIDATIONS_VALUE</code> se pasa como el valor de <em>Flags</em>.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-139">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ab2f-140"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="5ab2f-140"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="5ab2f-141">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-141">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ab2f-142"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="5ab2f-142"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="5ab2f-143">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-143">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5ab2f-144"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="5ab2f-144"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="5ab2f-145">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-145">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5ab2f-146"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="5ab2f-146"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="5ab2f-147">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="5ab2f-147">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="5ab2f-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5ab2f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ab2f-149">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="5ab2f-149">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="5ab2f-150">**Elemento InRibbonGallery**</span><span class="sxs-lookup"><span data-stu-id="5ab2f-150">**InRibbonGallery element**</span></span>](windowsribbon-element-inribbongallery.md)
</dt> <dt>

[<span data-ttu-id="5ab2f-151">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="5ab2f-151">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="5ab2f-152">Ejemplo de la galería</span><span class="sxs-lookup"><span data-stu-id="5ab2f-152">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

