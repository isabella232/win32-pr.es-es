---
title: Menú emergente (referencia de elementos de interfaz de usuario de MSAA)
description: Un menú emergente muestra una lista de comandos de menú.
ms.assetid: 9dbfa2d7-a086-4348-8b84-7e36d33e2d27
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 785fe8ac7a70352116b3a77cf30034092de04a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903650"
---
# <a name="pop-up-menu-msaa-ui-element-reference"></a><span data-ttu-id="2cb2b-103">Menú emergente (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="2cb2b-103">Pop-up Menu (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="2cb2b-104">En este tema se describen los objetos de **menú emergente** a efectos de la referencia de elementos de la interfaz de usuario de MSAA.</span><span class="sxs-lookup"><span data-stu-id="2cb2b-104">This topic describes **Pop-up Menu** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="2cb2b-105">La forma de crear objetos de **menú emergente** en varios marcos de interfaz de usuario no se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="2cb2b-105">How to create **Pop-up Menu** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="2cb2b-106">Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.</span><span class="sxs-lookup"><span data-stu-id="2cb2b-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="2cb2b-107">Un menú emergente muestra una lista de comandos de menú.</span><span class="sxs-lookup"><span data-stu-id="2cb2b-107">A pop-up menu displays a list of menu commands.</span></span> <span data-ttu-id="2cb2b-108">Microsoft Active Accessibility crea un objeto emergente de menú cuando se abre un elemento de menú en una barra de menús.</span><span class="sxs-lookup"><span data-stu-id="2cb2b-108">Microsoft Active Accessibility creates a menu pop-up object when a menu item in a menu bar is opened.</span></span> <span data-ttu-id="2cb2b-109">Microsoft Active Accessibility también crea objetos emergentes de menú para los menús contextuales, que se muestran cuando el usuario hace clic con el botón secundario en un elemento de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="2cb2b-109">Microsoft Active Accessibility also creates menu pop-up objects for context menus, which are displayed when the user right-clicks a user interface element.</span></span>

<span data-ttu-id="2cb2b-110">El nombre de la clase de ventana de un menú emergente es " \# 32768".</span><span class="sxs-lookup"><span data-stu-id="2cb2b-110">The window class name for a pop-up menu is "\#32768".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="2cb2b-111">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="2cb2b-111">IAccessible Methods</span></span>

<span data-ttu-id="2cb2b-112">Un menú emergente admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="2cb2b-112">A pop-up menu supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="2cb2b-113">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="2cb2b-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="2cb2b-114">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="2cb2b-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="2cb2b-115">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="2cb2b-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="2cb2b-116">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="2cb2b-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="2cb2b-117">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="2cb2b-117">IAccessible Properties</span></span>

<span data-ttu-id="2cb2b-118">Un menú emergente admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="2cb2b-118">A pop-up menu supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="2cb2b-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="2cb2b-119">Property</span></span>                                                                 | <span data-ttu-id="2cb2b-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2cb2b-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2cb2b-121">**obtener \_ accChild**</span><span class="sxs-lookup"><span data-stu-id="2cb2b-121">**get\_accChild**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild)           | <span data-ttu-id="2cb2b-122">Recupera [**IDispatch**](idispatch-interface.md) para el elemento de menú especificado.</span><span class="sxs-lookup"><span data-stu-id="2cb2b-122">Retrieves the [**IDispatch**](idispatch-interface.md) for the specified menu item.</span></span> <span data-ttu-id="2cb2b-123">Los identificadores secundarios de los elementos de menú se numeran secuencialmente de arriba abajo a partir de uno.</span><span class="sxs-lookup"><span data-stu-id="2cb2b-123">The child IDs for the menu items are numbered sequentially from top to bottom starting with one.</span></span>                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="2cb2b-124">**obtener \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="2cb2b-124">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="2cb2b-125">La propiedad **ChildCount** es el número de elementos de menú en el menú, incluidos los separadores de menús.</span><span class="sxs-lookup"><span data-stu-id="2cb2b-125">The **ChildCount** property is the number of menu items in the menu, including menu separators.</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="2cb2b-126">**obtener \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="2cb2b-126">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="2cb2b-127">**obtener \_ accName**</span><span class="sxs-lookup"><span data-stu-id="2cb2b-127">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="2cb2b-128">La propiedad **nombre** de un menú emergente es el mismo nombre que el menú.</span><span class="sxs-lookup"><span data-stu-id="2cb2b-128">The **Name** property for a pop-up menu is the same name as the menu.</span></span> <span data-ttu-id="2cb2b-129">La propiedad **Name** de un menú contextual es "context".</span><span class="sxs-lookup"><span data-stu-id="2cb2b-129">The **Name** property for a context menu is "Context".</span></span>                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="2cb2b-130">**obtener \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="2cb2b-130">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="2cb2b-131">La propiedad **primaria** es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el menú emergente y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el menú emergente.</span><span class="sxs-lookup"><span data-stu-id="2cb2b-131">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the pop-up menu and has the same **Name** property and window class name as the pop-up menu .</span></span>                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="2cb2b-132">**obtener \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="2cb2b-132">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="2cb2b-133">La propiedad **role** es [**\_ \_ MENUPOPUP del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="2cb2b-133">The **Role** property is [**ROLE\_SYSTEM\_MENUPOPUP**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="2cb2b-134">**obtener \_ accState**</span><span class="sxs-lookup"><span data-stu-id="2cb2b-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="2cb2b-135">La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md): [**sistema de estado \_ \_ invisible**](object-state-constants.md) \| [**estado \_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_ centrado**](object-state-constants.md) en \| [**\_ \_**](object-state-constants.md) sistema enfocable</span><span class="sxs-lookup"><span data-stu-id="2cb2b-135">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="2cb2b-136">Notas</span><span class="sxs-lookup"><span data-stu-id="2cb2b-136">Notes</span></span>

-   <span data-ttu-id="2cb2b-137">Los objetos de menú emergente no desencadenan eventos de [**\_ \_ creación**](event-constants.md) y [**\_ \_ destrucción**](event-constants.md) de objetos de eventos.</span><span class="sxs-lookup"><span data-stu-id="2cb2b-137">Pop-up menu objects do not trigger [**EVENT\_OBJECT\_CREATE**](event-constants.md) and [**EVENT\_OBJECT\_DESTROY**](event-constants.md) events.</span></span>
-   <span data-ttu-id="2cb2b-138">Los menús de varias columnas no admiten las marcas [**NAVDIR \_ left**](navigation-constants.md) o [**NAVDIR \_ right**](navigation-constants.md) del método [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) .</span><span class="sxs-lookup"><span data-stu-id="2cb2b-138">Multi-column menus do not support the [**NAVDIR\_LEFT**](navigation-constants.md) or [**NAVDIR\_RIGHT**](navigation-constants.md) flags of the [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) method.</span></span>
-   <span data-ttu-id="2cb2b-139">Los eventos [**Event \_ System \_ MENUPOPUPSTART**](event-constants.md) y [**Event \_ System \_ MENUPOPUPEND**](event-constants.md) no se envían de forma coherente.</span><span class="sxs-lookup"><span data-stu-id="2cb2b-139">The events [**EVENT\_SYSTEM\_MENUPOPUPSTART**](event-constants.md) and [**EVENT\_SYSTEM\_MENUPOPUPEND**](event-constants.md) are not sent consistently.</span></span> <span data-ttu-id="2cb2b-140">Se trata de un problema conocido y se está solucionando.</span><span class="sxs-lookup"><span data-stu-id="2cb2b-140">This is a known issue and is being addressed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cb2b-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2cb2b-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cb2b-142">IAccessible (interfaz)</span><span class="sxs-lookup"><span data-stu-id="2cb2b-142">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> <dt>

[<span data-ttu-id="2cb2b-143">**Barra de menús**</span><span class="sxs-lookup"><span data-stu-id="2cb2b-143">**Menu Bar**</span></span>](menu-bar.md)
</dt> <dt>

[<span data-ttu-id="2cb2b-144">**Elemento de menú**</span><span class="sxs-lookup"><span data-stu-id="2cb2b-144">**Menu Item**</span></span>](menu-item.md)
</dt> </dl>

 

 





