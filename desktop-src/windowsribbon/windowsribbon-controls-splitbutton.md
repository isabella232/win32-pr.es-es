---
title: Botón de expansión
description: El botón de expansión es un control compuesto con el que el usuario puede seleccionar un valor predeterminado enlazado a un botón primario o seleccionarlo en una lista de valores mutuamente excluyentes que se muestran en una lista desplegable enlazada a un botón secundario.
ms.assetid: 0939b3be-fa88-4864-8096-a664ab2e97b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b78aa261eebb24404eeaf8b3fdad7f630331f58
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105695782"
---
# <a name="split-button"></a><span data-ttu-id="76152-103">Botón de expansión</span><span class="sxs-lookup"><span data-stu-id="76152-103">Split Button</span></span>

<span data-ttu-id="76152-104">El botón de expansión es un control compuesto con el que el usuario puede seleccionar un valor predeterminado enlazado a un botón primario o seleccionarlo en una lista de valores mutuamente excluyentes que se muestran en una lista desplegable enlazada a un botón secundario.</span><span class="sxs-lookup"><span data-stu-id="76152-104">The Split Button is a composite control with which the user can select a default value bound to a primary button, or select from a list of mutually exclusive values displayed in a drop-down list bound to a secondary button.</span></span>

-   [<span data-ttu-id="76152-105">Introducción</span><span class="sxs-lookup"><span data-stu-id="76152-105">Introduction</span></span>](#introduction)
-   [<span data-ttu-id="76152-106">Propiedades del botón de expansión</span><span class="sxs-lookup"><span data-stu-id="76152-106">Split Button Properties</span></span>](#split-button-properties)
-   [<span data-ttu-id="76152-107">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76152-107">Related topics</span></span>](#related-topics)

## <a name="introduction"></a><span data-ttu-id="76152-108">Introducción</span><span class="sxs-lookup"><span data-stu-id="76152-108">Introduction</span></span>

<span data-ttu-id="76152-109">Este control es útil para exponer elementos estrechamente relacionados en los casos en los que un valor predeterminado obvio está disponible y donde los elementos individuales se pueden representar mediante una imagen, texto o ambos.</span><span class="sxs-lookup"><span data-stu-id="76152-109">This control is useful for exposing closely related items in cases where an obvious default is available and where the individual items can be represented by an image, text, or both.</span></span>

<span data-ttu-id="76152-110">En la captura de pantalla siguiente se muestra el botón de expansión de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="76152-110">The following screen shot illustrates the Ribbon Split Button.</span></span>

![captura de pantalla de un control splitbutton en una cinta de opciones de ejemplo.](images/controls/splitbutton.png)

## <a name="split-button-properties"></a><span data-ttu-id="76152-112">Propiedades del botón de expansión</span><span class="sxs-lookup"><span data-stu-id="76152-112">Split Button Properties</span></span>

<span data-ttu-id="76152-113">El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de botón de expansión.</span><span class="sxs-lookup"><span data-stu-id="76152-113">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Split Button control.</span></span>

<span data-ttu-id="76152-114">Normalmente, una propiedad de botón de expansión se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="76152-114">Typically, a Split Button property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="76152-115">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="76152-115">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="76152-116">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="76152-116">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="76152-117">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="76152-117">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="76152-118">En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="76152-118">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="76152-119">En la tabla siguiente se enumeran las claves de propiedad que están asociadas al control de botón de expansión.</span><span class="sxs-lookup"><span data-stu-id="76152-119">The following table lists the property keys that are associated with the Split Button control.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="76152-120">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="76152-120">Property Key</span></span></th>
<th><span data-ttu-id="76152-121">Notas</span><span class="sxs-lookup"><span data-stu-id="76152-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76152-122"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span><span class="sxs-lookup"><span data-stu-id="76152-122"><a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a></span></span></td>
<td><span data-ttu-id="76152-123">Admite <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework:: GetUICommandProperty</strong></a> y <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework:: SetUICommandProperty</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="76152-123">Supports <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty"><strong>IUIFramework::GetUICommandProperty</strong></a> and <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty"><strong>IUIFramework::SetUICommandProperty</strong></a>.</span></span><br/> <span data-ttu-id="76152-124">Si todos los elementos secundarios están deshabilitados, el marco de trabajo establece <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> en false (0).</span><span class="sxs-lookup"><span data-stu-id="76152-124">If all child items are disabled, the framework sets <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> to false (0).</span></span> <span data-ttu-id="76152-125">De lo contrario, si se habilitan uno o más elementos secundarios, UI_PKEY_Enabled se establece en true (-1).</span><span class="sxs-lookup"><span data-stu-id="76152-125">Otherwise, if one or more child items are enabled, UI_PKEY_Enabled is set to true (-1).</span></span>
<blockquote>
[!Important]<br />
<span data-ttu-id="76152-126">La propiedad <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> del control de botón de expansión debe invalidarse después de habilitar o deshabilitar uno o varios elementos secundarios.</span><span class="sxs-lookup"><span data-stu-id="76152-126">The <a href="windowsribbon-reference-properties-uipkey-enabled.md">UI_PKEY_Enabled</a> property for the Split Button control should be invalidated after one or more child items are enabled or disabled.</span></span> <span data-ttu-id="76152-127">Esto garantiza que el marco de trabajo consulta el valor de propiedad actualizado y actualiza el estado del control de botón de expansión en la interfaz de usuario de la cinta de opciones.</span><span class="sxs-lookup"><span data-stu-id="76152-127">This ensures that the framework queries the updated property value and refreshes the state of the Split Button control in the ribbon UI.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76152-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span><span class="sxs-lookup"><span data-stu-id="76152-128"><a href="windowsribbon-reference-properties-uipkey-keytip.md">UI_PKEY_Keytip</a></span></span></td>
<td><span data-ttu-id="76152-129">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="76152-129">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76152-130"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span><span class="sxs-lookup"><span data-stu-id="76152-130"><a href="windowsribbon-reference-properties-uipkey-tooltipdescription.md">UI_PKEY_TooltipDescription</a></span></span></td>
<td><span data-ttu-id="76152-131">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="76152-131">Can only be updated through invalidation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76152-132"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span><span class="sxs-lookup"><span data-stu-id="76152-132"><a href="windowsribbon-reference-properties-uipkey-tooltiptitle.md">UI_PKEY_TooltipTitle</a></span></span></td>
<td><span data-ttu-id="76152-133">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="76152-133">Can only be updated through invalidation.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="76152-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="76152-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76152-135">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="76152-135">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="76152-136">**Elemento de marcado SplitButton**</span><span class="sxs-lookup"><span data-stu-id="76152-136">**SplitButton markup element**</span></span>](windowsribbon-element-splitbutton.md)
</dt> </dl>