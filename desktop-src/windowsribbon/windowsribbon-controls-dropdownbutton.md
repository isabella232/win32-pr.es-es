---
title: Botón Drop-Down
description: El botón Drop-Down está compuesto de un botón en el que, cuando se hace clic en él, se muestra una lista desplegable de elementos mutuamente excluyentes.
ms.assetid: 41c5da07-43f7-4544-83be-248941cb8633
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e87e6a776dd705fe503e5e93ec601baf6cc2b3cf
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "104359472"
---
# <a name="drop-down-button"></a><span data-ttu-id="c5538-103">Botón Drop-Down</span><span class="sxs-lookup"><span data-stu-id="c5538-103">Drop-Down Button</span></span>

<span data-ttu-id="c5538-104">El botón Drop-Down está compuesto de un botón en el que, cuando se hace clic en él, se muestra una lista desplegable de elementos mutuamente excluyentes.</span><span class="sxs-lookup"><span data-stu-id="c5538-104">The Drop-Down Button consists of a button that when clicked displays a drop-down list of mutually exclusive items.</span></span>

-   [<span data-ttu-id="c5538-105">Detalles</span><span class="sxs-lookup"><span data-stu-id="c5538-105">Details</span></span>](#details)
-   [<span data-ttu-id="c5538-106">Propiedades del botón desplegable</span><span class="sxs-lookup"><span data-stu-id="c5538-106">Drop-Down Button Properties</span></span>](#drop-down-button-properties)
-   [<span data-ttu-id="c5538-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c5538-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="c5538-108">Detalles</span><span class="sxs-lookup"><span data-stu-id="c5538-108">Details</span></span>

<span data-ttu-id="c5538-109">Este control es útil para exponer elementos estrechamente relacionados en los casos en los que no hay ningún valor predeterminado obvio disponible y donde los elementos individuales se pueden representar mediante una imagen, texto o ambos.</span><span class="sxs-lookup"><span data-stu-id="c5538-109">This control is useful for exposing closely related items in cases where no obvious default is available and where the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="c5538-110">La siguiente captura de pantalla muestra el botón Drop-Down de la cinta de opciones en una cinta de opciones de ejemplo.</span><span class="sxs-lookup"><span data-stu-id="c5538-110">The following screen shot illustrates the Ribbon Drop-Down Button in a sample Ribbon.</span></span>

![captura de pantalla de un control DropDownButton en una cinta de opciones de ejemplo.](images/controls/dropdownbutton.png)

## <a name="drop-down-button-properties"></a><span data-ttu-id="c5538-112">Drop-Down propiedades del botón</span><span class="sxs-lookup"><span data-stu-id="c5538-112">Drop-Down Button Properties</span></span>

<span data-ttu-id="c5538-113">El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de botón de Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="c5538-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Drop-Down Button control.</span></span>

<span data-ttu-id="c5538-114">Normalmente, una propiedad de botón de Drop-Down se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="c5538-114">Typically, a Drop-Down Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="c5538-115">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="c5538-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="c5538-116">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="c5538-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="c5538-117">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="c5538-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="c5538-118">En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="c5538-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="c5538-119">En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de botón de Drop-Down.</span><span class="sxs-lookup"><span data-stu-id="c5538-119">The following table lists the property keys that are associated with the Drop-Down Button control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c5538-120">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="c5538-120">Property Key</span></span></th>
<th><span data-ttu-id="c5538-121">Notas</span><span class="sxs-lookup"><span data-stu-id="c5538-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c5538-122"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span><span class="sxs-lookup"><span data-stu-id="c5538-122"><a href="windowsribbon-reference-properties-uipkey-categories.md">UI_PKEY_Categories</a></span></span></td>
<td><span data-ttu-id="c5538-123">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c5538-123">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5538-124"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="c5538-124"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="c5538-125">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c5538-125">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span><br/> <span data-ttu-id="c5538-126">Si todos los elementos secundarios están deshabilitados, el marco de trabajo establece <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> en false (0).</span><span class="sxs-lookup"><span data-stu-id="c5538-126">If all child items are disabled, the framework sets <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> to false (0).</span></span> <span data-ttu-id="c5538-127">De lo contrario, si se habilitan uno o más elementos secundarios, UI_PKEY_Enabled se establece en true (-1).</span><span class="sxs-lookup"><span data-stu-id="c5538-127">Otherwise, if one or more child items are enabled, UI_PKEY_Enabled is set to true (-1).</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="c5538-128">La propiedad <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> para el control de botón Drop-Down debe invalidarse después de habilitar o deshabilitar uno o varios elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="c5538-128">The <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> property for the Drop-Down Button control should be invalidated after one or more child items are enabled or disabled.</span></span> <span data-ttu-id="c5538-129">Esto garantiza que el marco de trabajo consulta el valor de propiedad actualizado y actualiza el estado del control de botón Drop-Down en la interfaz de usuario de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="c5538-129">This ensures that the framework queries the updated property value and refreshes the state of the Drop-Down Button control in the ribbon UI.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5538-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span><span class="sxs-lookup"><span data-stu-id="c5538-130"><a href="windowsribbon-reference-properties-uipkey-itemssource.md">UI_PKEY_ItemsSource</a></span></span></td>
<td><span data-ttu-id="c5538-131">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c5538-131">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5538-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="c5538-132"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="c5538-133">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="c5538-133">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5538-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="c5538-134"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="c5538-135">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="c5538-135">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5538-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="c5538-136"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="c5538-137">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="c5538-137">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5538-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="c5538-138"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="c5538-139">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="c5538-139">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5538-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span><span class="sxs-lookup"><span data-stu-id="c5538-140"><a href="windowsribbon-reference-properties-uipkey-selecteditem.md">UI_PKEY_SelectedItem</a></span></span></td>
<td><span data-ttu-id="c5538-141">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="c5538-141">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c5538-142">Si el comando asociado al control se invalida mediante una llamada a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework:: InvalidateUICommand</strong></a>, el marco consulta esta propiedad cuando <code>UI_INVALIDATIONS_VALUE</code> se pasa como el valor de <em>Flags</em>.</span><span class="sxs-lookup"><span data-stu-id="c5538-142">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5538-143"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="c5538-143"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="c5538-144">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="c5538-144">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5538-145"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="c5538-145"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="c5538-146">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="c5538-146">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c5538-147"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="c5538-147"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="c5538-148">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="c5538-148">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c5538-149"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="c5538-149"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="c5538-150">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="c5538-150">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="c5538-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c5538-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5538-152">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="c5538-152">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="c5538-153">**Elemento de marcado DropDownButton**</span><span class="sxs-lookup"><span data-stu-id="c5538-153">**DropDownButton markup element**</span></span>](windowsribbon-element-dropdownbutton.md)
</dt> </dl>