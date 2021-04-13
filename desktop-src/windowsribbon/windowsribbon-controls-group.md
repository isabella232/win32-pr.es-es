---
title: Grupo (marco de cinta de Windows)
description: El grupo organiza los comandos y controles relacionados en una pestaña.
ms.assetid: 5d098d3f-a4ee-4f76-8c81-832d0c49cb80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 903bd422d11fea81ed03a48bf8e9437f9caab699
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104421862"
---
# <a name="group-windows-ribbon-framework"></a><span data-ttu-id="b4b9c-103">Grupo (marco de cinta de Windows)</span><span class="sxs-lookup"><span data-stu-id="b4b9c-103">Group (Windows Ribbon Framework)</span></span>

<span data-ttu-id="b4b9c-104">El grupo organiza los comandos y controles relacionados en una [pestaña](windowsribbon-controls-tab.md).</span><span class="sxs-lookup"><span data-stu-id="b4b9c-104">The Group organizes related Commands and controls within a [Tab](windowsribbon-controls-tab.md).</span></span>

-   [<span data-ttu-id="b4b9c-105">Detalles</span><span class="sxs-lookup"><span data-stu-id="b4b9c-105">Details</span></span>](#details)
-   [<span data-ttu-id="b4b9c-106">Propiedades de grupo</span><span class="sxs-lookup"><span data-stu-id="b4b9c-106">Group Properties</span></span>](#group-properties)
-   [<span data-ttu-id="b4b9c-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b4b9c-107">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="b4b9c-108">Detalles</span><span class="sxs-lookup"><span data-stu-id="b4b9c-108">Details</span></span>

<span data-ttu-id="b4b9c-109">La siguiente captura de pantalla ilustra el control de grupo de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-109">The following screen shot illustrates the Ribbon Group control.</span></span>

![captura de pantalla con llamadas que muestran un grupo.](images/controls/group.png)

## <a name="group-properties"></a><span data-ttu-id="b4b9c-111">Propiedades de grupo</span><span class="sxs-lookup"><span data-stu-id="b4b9c-111">Group Properties</span></span>

<span data-ttu-id="b4b9c-112">El marco de la cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de grupo.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-112">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Group control.</span></span>

<span data-ttu-id="b4b9c-113">Normalmente, una propiedad de grupo se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="b4b9c-113">Typically, a Group property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="b4b9c-114">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="b4b9c-114">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="b4b9c-115">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-115">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="b4b9c-116">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-116">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="b4b9c-117">En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="b4b9c-117">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="b4b9c-118">En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de grupo.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-118">The following table lists the property keys that are associated with the Group control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4b9c-119">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="b4b9c-119">Property Key</span></span></th>
<th><span data-ttu-id="b4b9c-120">Notas</span><span class="sxs-lookup"><span data-stu-id="b4b9c-120">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b4b9c-121"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="b4b9c-121"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="b4b9c-122">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-122">Can only be updated through invalidation.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="b4b9c-123">El marco de trabajo requiere que el valor de <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> para un control de grupo comience con la letra Z en mayúsculas. Si el valor proporcionado por la aplicación en el método de devolución de llamada <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler:: UpdateProperty</strong></a> no comienza con la letra Z, se omite este valor y el marco de trabajo genera un valor en su lugar.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-123">The framework requires that the value of <a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a> for a Group control begins with the upper-case letter Z. If the value supplied by the application in the <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty"><strong>IUICommandHandler::UpdateProperty</strong></a> callback method does not begin with the letter Z, this value is ignored and a value is generated by the framework instead.</span></span> <span data-ttu-id="b4b9c-124">El valor de Framework es la letra Z seguido de un valor numérico que empieza en 1 y aumenta secuencialmente, según sea necesario, para los controles de grupo subsiguientes (Z1, Z2,..., ZX).</span><span class="sxs-lookup"><span data-stu-id="b4b9c-124">The framework value is the letter Z followed by a numeric value starting at 1 and increasing sequentially, as required, for subsequent Group controls (Z1, Z2, ..., Zx).</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4b9c-125"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span><span class="sxs-lookup"><span data-stu-id="b4b9c-125"><a href="windowsribbon-reference-properties-uipkey-label.md">UI_PKEY_Label</a></span></span></td>
<td><span data-ttu-id="b4b9c-126">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-126">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4b9c-127"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="b4b9c-127"><a href="windowsribbon-reference-properties-uipkey-largehighcontrastimage.md">UI_PKEY_LargeHighContrastImage</a></span></span></td>
<td><span data-ttu-id="b4b9c-128">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-128">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4b9c-129"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span><span class="sxs-lookup"><span data-stu-id="b4b9c-129"><a href="windowsribbon-reference-properties-uipkey-largeimage.md">UI_PKEY_LargeImage</a></span></span></td>
<td><span data-ttu-id="b4b9c-130">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-130">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4b9c-131"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span><span class="sxs-lookup"><span data-stu-id="b4b9c-131"><a href="windowsribbon-reference-properties-uipkey-smallhighcontrastimage.md">UI_PKEY_SmallHighContrastImage</a></span></span></td>
<td><span data-ttu-id="b4b9c-132">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-132">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4b9c-133"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span><span class="sxs-lookup"><span data-stu-id="b4b9c-133"><a href="windowsribbon-reference-properties-uipkey-smallimage.md">UI_PKEY_SmallImage</a></span></span></td>
<td><span data-ttu-id="b4b9c-134">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-134">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b4b9c-135"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="b4b9c-135"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="b4b9c-136">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-136">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b4b9c-137"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="b4b9c-137"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="b4b9c-138">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="b4b9c-138">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b4b9c-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b4b9c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4b9c-140">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="b4b9c-140">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="b4b9c-141">**Group, elemento**</span><span class="sxs-lookup"><span data-stu-id="b4b9c-141">**Group element**</span></span>](windowsribbon-element-group.md)
</dt> </dl>

