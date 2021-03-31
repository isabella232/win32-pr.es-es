---
title: Control ToolTip (referencia de elementos de interfaz de usuario de MSAA)
description: Un control de información sobre herramientas muestra una pequeña ventana emergente que contiene una línea de texto que describe el propósito de una herramienta, representada como un objeto gráfico, en una aplicación.
ms.assetid: d3a65d7b-b882-4a1a-bac2-6995b64cf4af
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37557fd116084fc9ac53e8567afc90eda339750d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903482"
---
# <a name="tooltip-control-msaa-ui-element-reference"></a><span data-ttu-id="4999b-103">Control ToolTip (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="4999b-103">ToolTip Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="4999b-104">En este tema se describen los objetos de **control de información sobre herramientas** para la referencia de elementos de interfaz de usuario de MSAA.</span><span class="sxs-lookup"><span data-stu-id="4999b-104">This topic describes **ToolTip Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="4999b-105">Cómo crear objetos de **control de información sobre herramientas** en varios marcos de interfaz de usuario no se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="4999b-105">How to create **ToolTip Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="4999b-106">Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.</span><span class="sxs-lookup"><span data-stu-id="4999b-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="4999b-107">Un control de información sobre herramientas muestra una pequeña ventana emergente que contiene una línea de texto que describe el propósito de una herramienta, representada como un objeto gráfico, en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="4999b-107">A tooltip control displays a small pop-up window that contains a line of text that describes the purpose of a tool, represented as a graphical object, in an application.</span></span>

<span data-ttu-id="4999b-108">El nombre de la clase de ventana para una información sobre herramientas es la clase TOOLTIPs \_ , que se define como "clase tooltips \_ " en commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="4999b-108">The window class name for a tooltip is TOOLTIPS\_CLASS, which is defined as "tooltips\_class" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="4999b-109">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="4999b-109">IAccessible Methods</span></span>

<span data-ttu-id="4999b-110">Un control ToolTip admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="4999b-110">A tooltip control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="4999b-111">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="4999b-111">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="4999b-112">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="4999b-112">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="4999b-113">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="4999b-113">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="4999b-114">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="4999b-114">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="4999b-115">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="4999b-115">IAccessible Properties</span></span>

<span data-ttu-id="4999b-116">Un control ToolTip admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="4999b-116">A tooltip control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="4999b-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4999b-117">Property</span></span>                                                                 | <span data-ttu-id="4999b-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4999b-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4999b-119">**obtener \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="4999b-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="4999b-120">La propiedad **ChildCount** es cero.</span><span class="sxs-lookup"><span data-stu-id="4999b-120">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="4999b-121">**obtener \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="4999b-121">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="4999b-122">**obtener \_ accName**</span><span class="sxs-lookup"><span data-stu-id="4999b-122">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="4999b-123">La propiedad **Name** es el texto contenido en el control ToolTip.</span><span class="sxs-lookup"><span data-stu-id="4999b-123">The **Name** property is the text contained in the tooltip control.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="4999b-124">**obtener \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="4999b-124">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="4999b-125">La propiedad **primaria** es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el control.</span><span class="sxs-lookup"><span data-stu-id="4999b-125">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="4999b-126">**obtener \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="4999b-126">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="4999b-127">La propiedad **role** es [**la \_ \_ información sobre herramientas del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4999b-127">The **Role** property is [**ROLE\_SYSTEM\_TOOLTIP**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="4999b-128">**obtener \_ accState**</span><span class="sxs-lookup"><span data-stu-id="4999b-128">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="4999b-129">La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md): [**sistema de estado \_ \_ invisible**](object-state-constants.md) \| [**estado \_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_ centrado**](object-state-constants.md) en \| [**\_ \_**](object-state-constants.md) sistema enfocable</span><span class="sxs-lookup"><span data-stu-id="4999b-129">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="4999b-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4999b-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4999b-131">IAccessible (interfaz)</span><span class="sxs-lookup"><span data-stu-id="4999b-131">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





