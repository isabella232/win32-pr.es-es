---
title: Control de barra de estado (referencia de elementos de interfaz de usuario de MSAA)
description: Las barras de estado muestran información de estado en una ventana horizontal en la parte inferior de una ventana de la aplicación.
ms.assetid: e910a5c6-84d5-4ade-abf5-792ff1915021
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81bddf2898b9b7eca5385d86d6dabc6a50d3d4df
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357661"
---
# <a name="status-bar-control-msaa-ui-element-reference"></a><span data-ttu-id="26150-103">Control de barra de estado (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="26150-103">Status Bar Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="26150-104">En este tema se describen los objetos de **control de barra de estado** para fines de referencia de elementos de interfaz de usuario de MSAA.</span><span class="sxs-lookup"><span data-stu-id="26150-104">This topic describes **Status Bar Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="26150-105">La forma de crear objetos de **control de barra de estado** en varios marcos de interfaz de usuario no se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="26150-105">How to create **Status Bar Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="26150-106">Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.</span><span class="sxs-lookup"><span data-stu-id="26150-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="26150-107">Las barras de estado muestran información de estado en una ventana horizontal en la parte inferior de una ventana de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="26150-107">Status bars display status information in a horizontal window at the bottom of an application window.</span></span> <span data-ttu-id="26150-108">Las barras de Estado suelen dividirse en partes, denominadas paneles, y cada panel muestra información de estado diferente.</span><span class="sxs-lookup"><span data-stu-id="26150-108">Status bars are often divided into parts, called panes, and each pane displays different status information.</span></span> <span data-ttu-id="26150-109">Además, las barras de estado pueden contener objetos de diferentes tipos, incluidos botones y barras de progreso.</span><span class="sxs-lookup"><span data-stu-id="26150-109">Additionally, status bars can contain objects of different types, including buttons and progress bars.</span></span> <span data-ttu-id="26150-110">El nombre de clase de ventana de un control de barra de estado es STATUSCLASSNAME, que se define como "msctls \_ statusbar32" en commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="26150-110">The window class name for a status bar control is STATUSCLASSNAME, which is defined as "msctls\_statusbar32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="26150-111">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="26150-111">IAccessible Methods</span></span>

<span data-ttu-id="26150-112">Las barras de estado admiten los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="26150-112">Status bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="26150-113">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="26150-113">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="26150-114">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="26150-114">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="26150-115">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="26150-115">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="26150-116">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="26150-116">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="26150-117">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="26150-117">IAccessible Properties</span></span>

<span data-ttu-id="26150-118">Las barras de estado admiten las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="26150-118">Status bars support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="26150-119">Propiedad</span><span class="sxs-lookup"><span data-stu-id="26150-119">Property</span></span>                                                                 | <span data-ttu-id="26150-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="26150-120">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="26150-121">**obtener \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="26150-121">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="26150-122">La propiedad **ChildCount** es el número de paneles de la barra de estado.</span><span class="sxs-lookup"><span data-stu-id="26150-122">The **ChildCount** property is the number of panes in the status bar.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="26150-123">**obtener \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="26150-123">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="26150-124">**obtener \_ accName**</span><span class="sxs-lookup"><span data-stu-id="26150-124">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="26150-125">El propio objeto de barra de estado no tiene una propiedad **nombre** .</span><span class="sxs-lookup"><span data-stu-id="26150-125">The status bar object itself does not have a **Name** property.</span></span> <span data-ttu-id="26150-126">La propiedad **nombre** de cada panel de la barra de estado es igual que el texto mostrado.</span><span class="sxs-lookup"><span data-stu-id="26150-126">The **Name** property of each pane in the status bar is the same as the displayed text.</span></span>                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="26150-127">**obtener \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="26150-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="26150-128">La propiedad **primaria** del objeto de barra de estado es una ventana [**( \_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene el mismo nombre de clase de ventana que el control.</span><span class="sxs-lookup"><span data-stu-id="26150-128">The **Parent** property of the status bar object is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same window class name as the control.</span></span> <span data-ttu-id="26150-129">La propiedad **primaria** de los paneles en la barra de estado es el objeto de barra de estado.</span><span class="sxs-lookup"><span data-stu-id="26150-129">The **Parent** property of the panes in the status bar is the status bar object.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="26150-130">**obtener \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="26150-130">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="26150-131">La propiedad de **rol** para el propio objeto de barra de estado es la barra de estado [**\_ del sistema \_ de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="26150-131">The **Role** property for the status bar object itself is [**ROLE\_SYSTEM\_STATUSBAR**](object-roles.md).</span></span> <span data-ttu-id="26150-132">El texto que se muestra en una barra de Estado tiene el [**\_ sistema de \_ STATICTEXT de rol**](object-roles.md) como su propiedad de **rol** .</span><span class="sxs-lookup"><span data-stu-id="26150-132">The text displayed in a status bar has [**ROLE\_SYSTEM\_STATICTEXT**](object-roles.md) as its **Role** property.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="26150-133">**obtener \_ accState**</span><span class="sxs-lookup"><span data-stu-id="26150-133">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="26150-134">La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md): [**sistema de estado \_ \_ invisible**](object-state-constants.md) \| [**estado \_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_ centrado**](object-state-constants.md) en \| [**\_ \_**](object-state-constants.md) sistema enfocable</span><span class="sxs-lookup"><span data-stu-id="26150-134">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="notes"></a><span data-ttu-id="26150-135">Notas</span><span class="sxs-lookup"><span data-stu-id="26150-135">Notes</span></span>

<span data-ttu-id="26150-136">Dado que los métodos abreviados de teclado no se admiten para los controles de barra de estado o las áreas de texto en las barras de estado, no se admite [**Get \_ accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) .</span><span class="sxs-lookup"><span data-stu-id="26150-136">Because keyboard shortcuts are not supported for status bar controls or text areas on status bars, [**get\_accKeyboardShortcut**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) is not supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26150-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="26150-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26150-138">IAccessible (interfaz)</span><span class="sxs-lookup"><span data-stu-id="26150-138">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





