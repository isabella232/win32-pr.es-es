---
title: Casilla
description: La casilla es un control en el que el usuario puede hacer clic para proporcionar la entrada a una aplicación. El control proporciona un estado de alternancia que se representa visualmente.
ms.assetid: fe07aa5c-1818-41e2-b48d-5fefe50d733f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41e283facf81e8c3d2adad670329fcf0cf168d09
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "103795718"
---
# <a name="check-box"></a><span data-ttu-id="7586c-104">Casilla</span><span class="sxs-lookup"><span data-stu-id="7586c-104">Check Box</span></span>

<span data-ttu-id="7586c-105">La casilla es un control en el que el usuario puede hacer clic para proporcionar la entrada a una aplicación.</span><span class="sxs-lookup"><span data-stu-id="7586c-105">The Check Box is a control the user can click to provide input to an application.</span></span> <span data-ttu-id="7586c-106">El control proporciona un estado de alternancia que se representa visualmente.</span><span class="sxs-lookup"><span data-stu-id="7586c-106">The control provides a toggle state that is represented visually.</span></span>

-   [<span data-ttu-id="7586c-107">Detalles</span><span class="sxs-lookup"><span data-stu-id="7586c-107">Details</span></span>](#details)
-   [<span data-ttu-id="7586c-108">Propiedades de las casillas</span><span class="sxs-lookup"><span data-stu-id="7586c-108">Check Box Properties</span></span>](#check-box-properties)
-   [<span data-ttu-id="7586c-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7586c-109">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="7586c-110">Detalles</span><span class="sxs-lookup"><span data-stu-id="7586c-110">Details</span></span>

<span data-ttu-id="7586c-111">La casilla no admite un estado terciario o indeterminado.</span><span class="sxs-lookup"><span data-stu-id="7586c-111">The Check Box does not support a tertiary, or indeterminate, state.</span></span>

<span data-ttu-id="7586c-112">La siguiente captura de pantalla muestra el elemento de casilla de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="7586c-112">The following screen shot illustrates the Ribbon Check Box element.</span></span>

![captura de pantalla de un control CheckBox en la cinta de opciones de Microsoft Paint.](images/controls/checkbox.png)

## <a name="check-box-properties"></a><span data-ttu-id="7586c-114">Propiedades de las casillas</span><span class="sxs-lookup"><span data-stu-id="7586c-114">Check Box Properties</span></span>

<span data-ttu-id="7586c-115">El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de casilla.</span><span class="sxs-lookup"><span data-stu-id="7586c-115">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Check Box control.</span></span>

<span data-ttu-id="7586c-116">Normalmente, una propiedad de casilla se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="7586c-116">Typically, a Check Box property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="7586c-117">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="7586c-117">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="7586c-118">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="7586c-118">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="7586c-119">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="7586c-119">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="7586c-120">En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="7586c-120">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="7586c-121">En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de casilla.</span><span class="sxs-lookup"><span data-stu-id="7586c-121">The following table lists the property keys that are associated with the Check Box control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7586c-122">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="7586c-122">Property Key</span></span></th>
<th><span data-ttu-id="7586c-123">Notas</span><span class="sxs-lookup"><span data-stu-id="7586c-123">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7586c-124"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span><span class="sxs-lookup"><span data-stu-id="7586c-124"><a href="windowsribbon-reference-properties-uipkey-booleanvalue.md">UI_PKEY_BooleanValue</a></span></span></td>
<td><span data-ttu-id="7586c-125">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7586c-125">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7586c-126">Si el comando asociado al control se invalida mediante una llamada a <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework:: InvalidateUICommand</strong></a>, el marco consulta esta propiedad cuando <code>UI_INVALIDATIONS_VALUE</code> se pasa como el valor de <em>Flags</em>.</span><span class="sxs-lookup"><span data-stu-id="7586c-126">If the Command associated with the control is invalidated through a call to <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand"><strong>IUIFramework::InvalidateUICommand</strong></a>, the framework queries this property when <code>UI_INVALIDATIONS_VALUE</code> is passed as the value of <em>flags</em>.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7586c-127"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="7586c-127"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="7586c-128">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="7586c-128">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7586c-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="7586c-129"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="7586c-130">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7586c-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7586c-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="7586c-131"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="7586c-132">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7586c-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7586c-133"><a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a></span><span class="sxs-lookup"><span data-stu-id="7586c-133"><a href="windowsribbon-reference-properties-uipkey-labeldescription.md">UI_PKEY_LabelDescription</a></span></span></td>
<td><span data-ttu-id="7586c-134">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7586c-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7586c-135"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="7586c-135"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="7586c-136">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7586c-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7586c-137"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="7586c-137"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="7586c-138">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7586c-138">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7586c-139"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="7586c-139"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="7586c-140">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7586c-140">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7586c-141"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="7586c-141"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="7586c-142">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7586c-142">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7586c-143"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="7586c-143"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="7586c-144">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7586c-144">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7586c-145"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="7586c-145"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="7586c-146">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="7586c-146">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7586c-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7586c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7586c-148">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="7586c-148">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="7586c-149">**CheckBox (elemento de marcado)**</span><span class="sxs-lookup"><span data-stu-id="7586c-149">**CheckBox markup element**</span></span>](windowsribbon-element-checkbox.md)
</dt> </dl>

