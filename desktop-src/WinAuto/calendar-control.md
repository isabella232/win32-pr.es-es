---
title: Control de calendario (referencia de elementos de interfaz de usuario de MSAA)
description: Los controles de calendario proporcionan una forma sencilla e intuitiva de que un usuario pueda seleccionar una fecha de una interfaz conocida.
ms.assetid: cfb1e420-bb8f-4100-9c83-304d11573c0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63acb3ca83f6b7e71740acee4232e081e11594e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903292"
---
# <a name="calendar-control-msaa-ui-element-reference"></a><span data-ttu-id="31cd5-103">Control de calendario (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="31cd5-103">Calendar Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="31cd5-104">En este tema se describen los objetos de **control de calendario** para la referencia de elementos de interfaz de usuario de MSAA.</span><span class="sxs-lookup"><span data-stu-id="31cd5-104">This topic describes **Calendar Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="31cd5-105">La forma de crear objetos de **control de calendario** en varios marcos de interfaz de usuario no se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="31cd5-105">How to create **Calendar Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="31cd5-106">Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.</span><span class="sxs-lookup"><span data-stu-id="31cd5-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="31cd5-107">Los controles de calendario proporcionan una forma sencilla e intuitiva de que un usuario pueda seleccionar una fecha de una interfaz conocida.</span><span class="sxs-lookup"><span data-stu-id="31cd5-107">Calendar controls provide a simple and intuitive way for a user to select a date from a familiar interface.</span></span>

<span data-ttu-id="31cd5-108">El nombre de clase de ventana de un control de calendario mensual es MONTHCAL \_ Class, que se define como "SysMonthCal32" en commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="31cd5-108">The window class name for a month calendar control is MONTHCAL\_CLASS, which is defined as "SysMonthCal32" in Commctrl.h.</span></span> <span data-ttu-id="31cd5-109">La información de este tema se aplica al control de calendario mensual de la versión 5 de commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="31cd5-109">Information in this topic applies to the month calendar control in version 5 of Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="31cd5-110">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="31cd5-110">IAccessible Methods</span></span>

<span data-ttu-id="31cd5-111">Los controles de calendario admiten los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="31cd5-111">Calendar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="31cd5-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="31cd5-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="31cd5-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="31cd5-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="31cd5-114">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="31cd5-114">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="31cd5-115">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="31cd5-115">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="31cd5-116">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="31cd5-116">IAccessible Properties</span></span>

<span data-ttu-id="31cd5-117">Los controles de calendario admiten las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="31cd5-117">Calendar controls support the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="31cd5-118">Propiedad</span><span class="sxs-lookup"><span data-stu-id="31cd5-118">Property</span></span>                                                                 | <span data-ttu-id="31cd5-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="31cd5-119">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31cd5-120">**obtener \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="31cd5-120">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="31cd5-121">La propiedad **ChildCount** es cero.</span><span class="sxs-lookup"><span data-stu-id="31cd5-121">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="31cd5-122">**obtener \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="31cd5-122">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="31cd5-123">**obtener \_ accName**</span><span class="sxs-lookup"><span data-stu-id="31cd5-123">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="31cd5-124">La propiedad **Name** se obtiene del control de texto estático que etiqueta el control Calendar.</span><span class="sxs-lookup"><span data-stu-id="31cd5-124">The **Name** property is obtained from the static text control that labels the calendar control.</span></span> <span data-ttu-id="31cd5-125">Al crear controles, los programadores de servidor deben asegurarse de que un control de texto estático precede inmediatamente al control que etiqueta dentro del orden de tabulación.</span><span class="sxs-lookup"><span data-stu-id="31cd5-125">When creating controls, server developers must ensure that a static text control immediately precedes the control that it labels within the tab order.</span></span>                                                                                                                                                                                                                 |
| [<span data-ttu-id="31cd5-126">**obtener \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="31cd5-126">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="31cd5-127">La propiedad **primaria** es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el control.</span><span class="sxs-lookup"><span data-stu-id="31cd5-127">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="31cd5-128">**obtener \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="31cd5-128">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="31cd5-129">La propiedad **role** es [**el \_ \_ cliente del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="31cd5-129">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="31cd5-130">**obtener \_ accState**</span><span class="sxs-lookup"><span data-stu-id="31cd5-130">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="31cd5-131">La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md)de estado invisible del sistema de estado [**\_ \_ invisible**](object-state-constants.md) del sistema de estado \| [**\_ \_ no disponible**](object-state-constants.md) \| [**\_ \_**](object-state-constants.md) sistema enfocable \| [**\_ \_**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="31cd5-131">The **State** property is a combination of one or more of the following [values](object-state-constants.md)[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="31cd5-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="31cd5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31cd5-133">IAccessible (interfaz)</span><span class="sxs-lookup"><span data-stu-id="31cd5-133">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





