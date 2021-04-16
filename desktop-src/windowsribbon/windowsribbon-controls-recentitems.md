---
title: Elementos recientes
description: La lista elementos recientes es un panel del menú aplicación que muestra los elementos usados más recientemente (MRU) para una aplicación.
ms.assetid: fdead358-d303-46de-9f8e-6fc2832d8e94
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f78c01fc4d6cc830eba644f7dcf22b6fb03e82
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104566597"
---
# <a name="recent-items"></a><span data-ttu-id="e645f-103">Elementos recientes</span><span class="sxs-lookup"><span data-stu-id="e645f-103">Recent Items</span></span>

<span data-ttu-id="e645f-104">La lista elementos recientes es un panel del [menú aplicación](windowsribbon-controls-applicationmenu.md) que muestra los elementos usados más recientemente (MRU) para una aplicación.</span><span class="sxs-lookup"><span data-stu-id="e645f-104">The Recent Items list is a pane in the [Application Menu](windowsribbon-controls-applicationmenu.md) that displays the most recently used (MRU) items for an application.</span></span>

-   [<span data-ttu-id="e645f-105">Detalles</span><span class="sxs-lookup"><span data-stu-id="e645f-105">Details</span></span>](#details)
-   [<span data-ttu-id="e645f-106">Propiedades de elementos recientes</span><span class="sxs-lookup"><span data-stu-id="e645f-106">Recent Items Properties</span></span>](#recent-items-properties)
-   [<span data-ttu-id="e645f-107">Comentarios:</span><span class="sxs-lookup"><span data-stu-id="e645f-107">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="e645f-108">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e645f-108">Related topics</span></span>](#related-topics)

## <a name="details"></a><span data-ttu-id="e645f-109">Detalles</span><span class="sxs-lookup"><span data-stu-id="e645f-109">Details</span></span>

<span data-ttu-id="e645f-110">En la siguiente captura de pantalla se muestra una lista de elementos recientes de WordPad para Windows 7).</span><span class="sxs-lookup"><span data-stu-id="e645f-110">The following screen shot illustrates a Recent Items list from WordPad for Windows 7).</span></span>

![captura de pantalla de la lista elementos recientes en la cinta de opciones de Microsoft Paint.](images/controls/recentitems.png)

<span data-ttu-id="e645f-112">El [menú aplicación](windowsribbon-controls-applicationmenu.md) puede tener como máximo una lista [**ApplicationMenu. RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) , representada por un elemento **ApplicationMenu. RecentItems** , para mostrar documentos recientes, imágenes, películas y otros proyectos en los que el usuario ha estado trabajando.</span><span class="sxs-lookup"><span data-stu-id="e645f-112">The [Application Menu](windowsribbon-controls-applicationmenu.md) can have at most one [**ApplicationMenu.RecentItems**](windowsribbon-element-applicationmenu-recentitems.md) list, represented by an **ApplicationMenu.RecentItems** element, for displaying recent documents, pictures, movies, and other projects a user has been working on.</span></span> <span data-ttu-id="e645f-113">El número de elementos de la lista va de cero al número máximo especificado en el marcado, con un valor predeterminado de diez.</span><span class="sxs-lookup"><span data-stu-id="e645f-113">The number of listed items ranges from zero to the maximum number specified in markup, with a default value of ten.</span></span> <span data-ttu-id="e645f-114">Los elementos recientes se muestran como una lista numerada de cadenas que indican los nombres de archivo.</span><span class="sxs-lookup"><span data-stu-id="e645f-114">The recent items are displayed as a numbered list of strings indicating file names.</span></span> <span data-ttu-id="e645f-115">Se recomienda usar la propiedad [**Command. LabelDescription**](windowsribbon-element-command-labeldescription.md) para proporcionar la ruta de acceso completa de la ubicación del archivo, como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e645f-115">It is recommended that the [**Command.LabelDescription**](windowsribbon-element-command-labeldescription.md) property be used to give the full path for the file location, as shown in the following screen shot .</span></span>

![captura de pantalla de una lista de elementos recientes en un menú de la aplicación.](images/overviews/applicationmenu-menurecentitems.png)

<span data-ttu-id="e645f-117">El elemento [**RecentItems**](windowsribbon-element-recentitems.md) tiene un atributo *EnablePinning* que, si se establece en `true` , muestra un icono de anclaje a la derecha de cada elemento de la lista, como se muestra en la siguiente captura de pantalla.</span><span class="sxs-lookup"><span data-stu-id="e645f-117">The [**RecentItems**](windowsribbon-element-recentitems.md) element has an *EnablePinning* attribute that, if set to `true`, displays a pin icon to the right of each item in the list, as shown in the following screen shot.</span></span>

> [!Note]  
> <span data-ttu-id="e645f-118">El anclaje está habilitado de forma predeterminada si no se especifica el atributo *EnablePinning* .</span><span class="sxs-lookup"><span data-stu-id="e645f-118">Pinning is enabled by default if the *EnablePinning* attribute is not specified.</span></span>

 

![captura de pantalla del anclaje de elementos recientes en un menú de la aplicación.](images/overviews/applicationmenu-menurecentitemspinned.png)

<span data-ttu-id="e645f-120">El algoritmo de anclaje está diseñado para evitar que los elementos caigan en la lista de **elementos recientes** .</span><span class="sxs-lookup"><span data-stu-id="e645f-120">The pinning algorithm is intended to keep items from falling off the **Recent items** list.</span></span> <span data-ttu-id="e645f-121">El algoritmo produce el comportamiento siguiente:</span><span class="sxs-lookup"><span data-stu-id="e645f-121">The algorithm produces the following behavior:</span></span>

-   <span data-ttu-id="e645f-122">Un nuevo elemento siempre se agrega en la parte superior de la lista de **elementos recientes** .</span><span class="sxs-lookup"><span data-stu-id="e645f-122">A new item is always added at the top of the **Recent items** list.</span></span>
-   <span data-ttu-id="e645f-123">Los elementos se desactivarán en la lista a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="e645f-123">Items will move down in the list over time.</span></span> <span data-ttu-id="e645f-124">Una vez que la lista está llena (alcanza el número máximo de elementos especificado en el marcado), los elementos más antiguos quedan fuera de la parte inferior de la lista a medida que se agregan nuevos elementos a la parte superior de la lista.</span><span class="sxs-lookup"><span data-stu-id="e645f-124">Once the list is full (reaches the maximum number of items specified in markup), older items fall off the bottom of the list as new items are added to the top of the list.</span></span>
-   <span data-ttu-id="e645f-125">Si un elemento ya aparece en alguna parte de la lista, pero se vuelve a acceder a él, se vuelve a colocar en la parte superior de la lista.</span><span class="sxs-lookup"><span data-stu-id="e645f-125">If an item already appears somewhere in the list but is accessed again, it moves back to the top of the list.</span></span>
-   <span data-ttu-id="e645f-126">Si un elemento está anclado, seguirá desplazando la lista, pero no se cerrará la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="e645f-126">If an item is pinned, it will still travel down the list, but it will not fall off the bottom.</span></span> <span data-ttu-id="e645f-127">En su lugar, una vez completada la lista, el primer elemento desanclado situado encima del elemento anclado se desactivará cuando se agregue un nuevo elemento a la lista.</span><span class="sxs-lookup"><span data-stu-id="e645f-127">Instead, once the list is full, the first unpinned item above the pinned item will fall off when a new item is added to the list.</span></span>
-   <span data-ttu-id="e645f-128">Si el número de elementos anclados alcanza siempre el número máximo de elementos, no se agregarán nuevos elementos a la lista hasta que se desancla un elemento.</span><span class="sxs-lookup"><span data-stu-id="e645f-128">If the number of pinned items ever reaches the maximum number of items, then no new items will get added to the list until an item is unpinned.</span></span>

## <a name="recent-items-properties"></a><span data-ttu-id="e645f-129">Propiedades de elementos recientes</span><span class="sxs-lookup"><span data-stu-id="e645f-129">Recent Items Properties</span></span>

<span data-ttu-id="e645f-130">El marco de cinta de opciones define una colección de [claves de propiedad](windowsribbon-reference-properties.md) para el control de elementos recientes.</span><span class="sxs-lookup"><span data-stu-id="e645f-130">The Ribbon framework defines a collection of [property keys](windowsribbon-reference-properties.md) for the Recent Items control.</span></span>

<span data-ttu-id="e645f-131">Normalmente, una propiedad de elementos recientes se actualiza en la interfaz de usuario de la cinta de opciones invalidando el comando asociado al control a través de una llamada al método [**IUIFramework:: InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) .</span><span class="sxs-lookup"><span data-stu-id="e645f-131">Typically, a Recent Items property is updated in the ribbon UI by invalidating the Command associated with the control through a call to the [**IUIFramework::InvalidateUICommand**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-invalidateuicommand) method.</span></span> <span data-ttu-id="e645f-132">Se controla el evento de invalidación y las actualizaciones de propiedades definidas por el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) .</span><span class="sxs-lookup"><span data-stu-id="e645f-132">The invalidation event is handled, and the property updates defined, by the [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method.</span></span>

<span data-ttu-id="e645f-133">No se ejecuta el método de devolución de llamada [**IUICommandHandler:: UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) y la aplicación solicitó un valor de propiedad actualizado hasta que el marco de trabajo requiera la propiedad.</span><span class="sxs-lookup"><span data-stu-id="e645f-133">The [**IUICommandHandler::UpdateProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-updateproperty) callback method is not executed, and the application queried for an updated property value, until the property is required by the framework.</span></span> <span data-ttu-id="e645f-134">Por ejemplo, cuando se activa una pestaña y se revela un control en la interfaz de usuario de la cinta de opciones, o cuando se muestra una información sobre herramientas.</span><span class="sxs-lookup"><span data-stu-id="e645f-134">For example, when a tab is activated and a control revealed in the ribbon UI, or when a tooltip is displayed.</span></span>

> [!Note]  
> <span data-ttu-id="e645f-135">En algunos casos, una propiedad se puede recuperar a través del método [**IUIFramework:: GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) y establecerse con el método [**IUIFramework:: SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) .</span><span class="sxs-lookup"><span data-stu-id="e645f-135">In some cases, a property can be retrieved through the [**IUIFramework::GetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-getuicommandproperty) method and set with the [**IUIFramework::SetUICommandProperty**](/windows/desktop/api/uiribbon/nf-uiribbon-iuiframework-setuicommandproperty) method.</span></span>

 

<span data-ttu-id="e645f-136">En la tabla siguiente se enumeran las claves de propiedades que están asociadas con el control de elementos recientes.</span><span class="sxs-lookup"><span data-stu-id="e645f-136">The following table lists the property keys that are associated with the Recent Items control.</span></span>



| <span data-ttu-id="e645f-137">Clave de propiedad</span><span class="sxs-lookup"><span data-stu-id="e645f-137">Property Key</span></span>                                                                       | <span data-ttu-id="e645f-138">Notas</span><span class="sxs-lookup"><span data-stu-id="e645f-138">Notes</span></span>                                     |
|------------------------------------------------------------------------------------|-------------------------------------------|
| [<span data-ttu-id="e645f-139">KeyTip de UI \_ PKEY \_</span><span class="sxs-lookup"><span data-stu-id="e645f-139">UI\_PKEY\_Keytip</span></span>](windowsribbon-reference-properties-uipkey-keytip.md)           | <span data-ttu-id="e645f-140">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="e645f-140">Can only be updated through invalidation.</span></span> |
| [<span data-ttu-id="e645f-141">UI \_ PKEY \_ RecentItems</span><span class="sxs-lookup"><span data-stu-id="e645f-141">UI\_PKEY\_RecentItems</span></span>](windowsribbon-reference-properties-uipkey-recentitems.md) | <span data-ttu-id="e645f-142">Solo se puede actualizar a través de la invalidación.</span><span class="sxs-lookup"><span data-stu-id="e645f-142">Can only be updated through invalidation.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="e645f-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e645f-143">Remarks</span></span>

<span data-ttu-id="e645f-144">El método [IApplicationDocumentLists:: getList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) se puede usar para recuperar la lista MRU de Shell de Windows para la aplicación de cinta.</span><span class="sxs-lookup"><span data-stu-id="e645f-144">The [IApplicationDocumentLists::GetList](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-getlist) method can be used to retrieve the Windows Shell MRU list for the Ribbon application.</span></span> <span data-ttu-id="e645f-145">A continuación, la aplicación puede usar el objeto recuperado por este método para crear los datos que requiere el marco de cinta para rellenar la lista de **elementos recientes** del menú de la [aplicación](windowsribbon-controls-applicationmenu.md).</span><span class="sxs-lookup"><span data-stu-id="e645f-145">The object retrieved by this method can then be used by the application to create the data required by the Ribbon framework to populate the **Recent items** list of the [Application Menu](windowsribbon-controls-applicationmenu.md).</span></span>

> [!Note]  
> <span data-ttu-id="e645f-146">Cuando se usa este método, *ListType* debe tener el valor `ADLT_RECENT` .</span><span class="sxs-lookup"><span data-stu-id="e645f-146">When using this method, *listtype* should have the value `ADLT_RECENT`.</span></span>

 

<span data-ttu-id="e645f-147">Para obtener un ejemplo de cómo implementar una lista de elementos MRU en una aplicación de marco de cinta, vea el [ejemplo HTMLEditRibbon](windowsribbon-htmleditribbonsample.md).</span><span class="sxs-lookup"><span data-stu-id="e645f-147">For an example of how to implement an MRU items list in a Ribbon framework application, see the [HTMLEditRibbon Sample](windowsribbon-htmleditribbonsample.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e645f-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e645f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e645f-149">Biblioteca de controles de Windows Ribbon Framework</span><span class="sxs-lookup"><span data-stu-id="e645f-149">Windows Ribbon Framework Control Library</span></span>](windowsribbon-controls-entry.md)
</dt> <dt>

[<span data-ttu-id="e645f-150">**Elemento de marcado de elementos recientes**</span><span class="sxs-lookup"><span data-stu-id="e645f-150">**Recent items markup element**</span></span>](windowsribbon-element-recentitems.md)
</dt> </dl>

 

 