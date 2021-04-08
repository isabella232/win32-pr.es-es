---
title: Galería de Drop-Down
description: La galería de Drop-Down se compone de un botón en el que, cuando se hace clic en él, se muestra una lista desplegable que contiene una colección de elementos o comandos mutuamente excluyentes.
ms.assetid: 10644e10-f903-49f6-aecd-1a63d97fe447
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f07553dcc767b50786e271544ea44bd17670a2a9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103795304"
---
# <a name="drop-down-gallery"></a><span data-ttu-id="69f0e-103">Galería de Drop-Down</span><span class="sxs-lookup"><span data-stu-id="69f0e-103">Drop-Down Gallery</span></span>

<span data-ttu-id="69f0e-104">La galería de Drop-Down se compone de un botón en el que, cuando se hace clic en él, se muestra una lista desplegable que contiene una colección de elementos o comandos mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="69f0e-104">The Drop-Down Gallery consists of a button that when clicked displays a drop-down list containing a collection of mutually exclusive items or Commands.</span></span>

-   [<span data-ttu-id="69f0e-105">Detalles</span><span class="sxs-lookup"><span data-stu-id="69f0e-105">Details</span></span>](#details)
-   [<span data-ttu-id="69f0e-106">Propiedades de la Galería desplegable</span><span class="sxs-lookup"><span data-stu-id="69f0e-106">Drop-Down Gallery Properties</span></span>](#drop-down-gallery-properties)
-   [<span data-ttu-id="69f0e-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="69f0e-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="69f0e-108">Detalles</span><span class="sxs-lookup"><span data-stu-id="69f0e-108">Details</span></span>

<span data-ttu-id="69f0e-109">Este control es útil para exponer elementos o comandos relacionados en los que no hay ningún valor predeterminado obvio, y los elementos individuales se pueden representar mediante una imagen, texto o ambos.</span><span class="sxs-lookup"><span data-stu-id="69f0e-109">This control is useful for exposing related items or Commands where there is no obvious default, and the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="69f0e-110">La compatibilidad con las barras de redimensionamiento vertical y de esquina, o con los controladores de cambio de tamaño, se proporciona mediante el elemento [**DropDownGallery. MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) .</span><span class="sxs-lookup"><span data-stu-id="69f0e-110">Support for both vertical and corner gripper bars, or resizing handles, is provided through the [**DropDownGallery.MenuLayout**](windowsribbon-element-dropdowngallery-menulayout.md) element.</span></span>

<span data-ttu-id="69f0e-111">En la captura de pantalla siguiente se muestra la galería de Drop-Down de la cinta de opciones de Microsoft Paint.</span><span class="sxs-lookup"><span data-stu-id="69f0e-111">The following screen shot illustrates the Ribbon Drop-Down Gallery in Microsoft Paint.</span></span>

![captura de pantalla de un control dropdowngallery en la cinta de opciones de Microsoft Paint.](images/controls/dropdowngallery.png)

## <a name="drop-down-gallery-properties"></a><span data-ttu-id="69f0e-113">Propiedades de la galería de Drop-Down</span><span class="sxs-lookup"><span data-stu-id="69f0e-113">Drop-Down Gallery Properties</span></span>

<span data-ttu-id="69f0e-114">El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control galería de Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="69f0e-114">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Gallery control.</span></span>

<span data-ttu-id="69f0e-115">Normalmente, una propiedad de la galería de Drop-Down se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="69f0e-115">Typically, a Drop-Down Gallery property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="69f0e-116">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="69f0e-116">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="69f0e-117">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="69f0e-117">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="69f0e-118">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="69f0e-118">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="69f0e-119">En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="69f0e-119">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="69f0e-120">En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control Galería de Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="69f0e-120">The following table lists the property keys that are associated with the Drop-Down Gallery control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="69f0e-121">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="69f0e-121">Property Key</span></span></th>
<th><span data-ttu-id="69f0e-122">Notas</span><span class="sxs-lookup"><span data-stu-id="69f0e-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="69f0e-123"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="69f0e-123"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="69f0e-124">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="69f0e-124">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="69f0e-125"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="69f0e-125"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="69f0e-126">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="69f0e-126">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="69f0e-127"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="69f0e-127"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="69f0e-128">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="69f0e-128">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="69f0e-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="69f0e-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="69f0e-130">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="69f0e-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="69f0e-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="69f0e-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="69f0e-132">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="69f0e-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="69f0e-133"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="69f0e-133"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="69f0e-134">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="69f0e-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="69f0e-135"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="69f0e-135"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="69f0e-136">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="69f0e-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="69f0e-137"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(solo válido para una galería de elementos)</span><span class="sxs-lookup"><span data-stu-id="69f0e-137"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a>(only valid for an item gallery)</span></span><br/></td>
<td><span data-ttu-id="69f0e-138">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="69f0e-138">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="69f0e-139">Si el comando asociado al control se invalida mediante una llamada a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework:: InvalidateUICommand</strong></a>, el marco consulta esta propiedad cuando <code>UI_INVALIDATIONS_VALUE</code> se pasa como el valor de <em>Flags</em>.</span><span class="sxs-lookup"><span data-stu-id="69f0e-139">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="69f0e-140"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="69f0e-140"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="69f0e-141">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="69f0e-141">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="69f0e-142"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="69f0e-142"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="69f0e-143">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="69f0e-143">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="69f0e-144"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="69f0e-144"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="69f0e-145">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="69f0e-145">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="69f0e-146"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="69f0e-146"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="69f0e-147">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="69f0e-147">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="69f0e-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="69f0e-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69f0e-149">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="69f0e-149">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="69f0e-150">**Elemento de marcado DropDownGallery**</span><span class="sxs-lookup"><span data-stu-id="69f0e-150">**DropDownGallery markup element**</span></span>](windowsribbon-element-dropdowngallery.md)
</dt> <dt>

[<span data-ttu-id="69f0e-151">Trabajar con galerías</span><span class="sxs-lookup"><span data-stu-id="69f0e-151">Working with Galleries</span></span>](ribbon-controls-galleries.md)
</dt> <dt>

[<span data-ttu-id="69f0e-152">Ejemplo de la galería</span><span class="sxs-lookup"><span data-stu-id="69f0e-152">Gallery Sample</span></span>](windowsribbon-gallerysample.md)
</dt> </dl>

