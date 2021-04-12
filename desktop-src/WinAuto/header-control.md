---
title: Control header (referencia de elementos de interfaz de usuario de MSAA)
description: Un control de encabezado muestra los encabezados en la parte superior de las columnas de información y permite que el usuario ordene la información haciendo clic en los encabezados. El explorador de Windows utiliza un control de encabezado cuando se selecciona la vista de detalles.
ms.assetid: 669d6bb8-7bc4-4e6f-bf4f-207887f44b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6d069770b14ad3ba58022af28ad07fc78cb8c5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357463"
---
# <a name="header-control-msaa-ui-element-reference"></a><span data-ttu-id="409bc-104">Control header (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="409bc-104">Header Control (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="409bc-105">En este tema se describen los objetos de **control de encabezado** para la referencia de elementos de interfaz de usuario de MSAA.</span><span class="sxs-lookup"><span data-stu-id="409bc-105">This topic describes **Header Control** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="409bc-106">Cómo crear objetos de **control de encabezado** en varios marcos de interfaz de usuario no se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="409bc-106">How to create **Header Control** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="409bc-107">Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.</span><span class="sxs-lookup"><span data-stu-id="409bc-107">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="409bc-108">Un control de encabezado muestra los encabezados en la parte superior de las columnas de información y permite que el usuario ordene la información haciendo clic en los encabezados.</span><span class="sxs-lookup"><span data-stu-id="409bc-108">A header control displays headings at the top of columns of information and lets the user sort the information by clicking the headings.</span></span> <span data-ttu-id="409bc-109">El explorador de Windows utiliza un control de encabezado cuando se selecciona la vista de detalles.</span><span class="sxs-lookup"><span data-stu-id="409bc-109">Windows Explorer uses a header control when the Details view is selected.</span></span>

<span data-ttu-id="409bc-110">El nombre de clase de ventana de un control de encabezado es WC \_ header, que se define como "SysHeader32" en commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="409bc-110">The window class name for a header control is WC\_HEADER, which is defined as "SysHeader32" in Commctrl.h.</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="409bc-111">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="409bc-111">IAccessible Methods</span></span>

<span data-ttu-id="409bc-112">Un control de encabezado admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="409bc-112">A header control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="409bc-113">Método</span><span class="sxs-lookup"><span data-stu-id="409bc-113">Method</span></span>                                                                    | <span data-ttu-id="409bc-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="409bc-114">Comments</span></span>                                                        |
|---------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="409bc-115">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="409bc-115">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="409bc-116">Este método realiza la acción predeterminada haciendo clic en el encabezado.</span><span class="sxs-lookup"><span data-stu-id="409bc-116">This method performs the default action by clicking the header.</span></span> |
| [<span data-ttu-id="409bc-117">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="409bc-117">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                 |
| [<span data-ttu-id="409bc-118">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="409bc-118">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                 |
| [<span data-ttu-id="409bc-119">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="409bc-119">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                 |
| [<span data-ttu-id="409bc-120">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="409bc-120">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                 |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="409bc-121">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="409bc-121">IAccessible Properties</span></span>

<span data-ttu-id="409bc-122">Un control de encabezado admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="409bc-122">A header control supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="409bc-123">Propiedad</span><span class="sxs-lookup"><span data-stu-id="409bc-123">Property</span></span>                                                                       | <span data-ttu-id="409bc-124">Comentarios</span><span class="sxs-lookup"><span data-stu-id="409bc-124">Comments</span></span>                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="409bc-125">**obtener \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="409bc-125">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="409bc-126">La propiedad **ChildCount** es cero.</span><span class="sxs-lookup"><span data-stu-id="409bc-126">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                                   |
| [<span data-ttu-id="409bc-127">**obtener \_ accDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="409bc-127">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="409bc-128">La propiedad **DEFAULTACTION** es "click".</span><span class="sxs-lookup"><span data-stu-id="409bc-128">The **DefaultAction** property is "Click".</span></span>                                                                                                                                                                                             |
| [<span data-ttu-id="409bc-129">**obtener \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="409bc-129">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 |                                                                                                                                                                                                                                        |
| [<span data-ttu-id="409bc-130">**obtener \_ accName**</span><span class="sxs-lookup"><span data-stu-id="409bc-130">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="409bc-131">La propiedad **Name** es igual que el nombre del encabezado de columna.</span><span class="sxs-lookup"><span data-stu-id="409bc-131">The **Name** property is the same as the name of the column header.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="409bc-132">**obtener \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="409bc-132">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)               | <span data-ttu-id="409bc-133">La propiedad **primaria** es una ventana ( [**\_ \_ lista de sistema de roles**](object-roles.md) ) que rodea el control y tiene el mismo nombre de clase de ventana que el control.</span><span class="sxs-lookup"><span data-stu-id="409bc-133">The **Parent** property is a window ( [**ROLE\_SYSTEM\_LIST**](object-roles.md) ) that surrounds the control and has the same window class name as the control.</span></span>                                                      |
| [<span data-ttu-id="409bc-134">**obtener \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="409bc-134">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="409bc-135">La propiedad **role** es el [**sistema de rol \_ \_ COLUMNHEADER**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="409bc-135">The **Role** property is [**ROLE\_SYSTEM\_COLUMNHEADER**](object-roles.md).</span></span>                                                                                                                                  |
| [<span data-ttu-id="409bc-136">**obtener \_ accState**</span><span class="sxs-lookup"><span data-stu-id="409bc-136">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="409bc-137">El valor de la propiedad **State** es siempre [**el \_ estado \_ ReadOnly del sistema**](object-state-constants.md) y también puede incluir el [**sistema de estado \_ \_ invisible**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="409bc-137">The value for the **State** property is always [**STATE\_SYSTEM\_READONLY**](object-state-constants.md) and can also include [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="409bc-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="409bc-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="409bc-139">IAccessible (interfaz)</span><span class="sxs-lookup"><span data-stu-id="409bc-139">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




