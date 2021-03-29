---
title: Cuadro de grupo (referencia de elementos de interfaz de usuario de MSAA)
description: Un cuadro de grupo es un rectángulo que rodea un conjunto de controles, como las casillas o los botones de radio, y contiene un texto definido por la aplicación (etiqueta).
ms.assetid: c6cd81a1-76c0-41c5-bb7f-4796ea7e3114
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a105242aabd49d87241a2a49bdaca5c19edd350b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778108"
---
# <a name="group-box-msaa-ui-element-reference"></a><span data-ttu-id="46027-103">Cuadro de grupo (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="46027-103">Group Box (MSAA UI Element Reference)</span></span>

> [!Note]  
> <span data-ttu-id="46027-104">En este tema se describen los objetos de **cuadro de grupo** para la referencia de elementos de interfaz de usuario de MSAA.</span><span class="sxs-lookup"><span data-stu-id="46027-104">This topic describes **Group Box** objects for purposes of MSAA UI Element Reference.</span></span> <span data-ttu-id="46027-105">La forma de crear objetos de **cuadro de grupo** en varios marcos de interfaz de usuario no se describe aquí.</span><span class="sxs-lookup"><span data-stu-id="46027-105">How to create **Group Box** objects in various UI frameworks is not described here.</span></span> <span data-ttu-id="46027-106">Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.</span><span class="sxs-lookup"><span data-stu-id="46027-106">See the API reference documentation for the UI framework you're using.</span></span>

 

<span data-ttu-id="46027-107">Un cuadro de grupo es un rectángulo que rodea un conjunto de controles, como las casillas o los botones de radio, y contiene un texto definido por la aplicación (etiqueta).</span><span class="sxs-lookup"><span data-stu-id="46027-107">A group box is a rectangle that surrounds a set of controls, such as check boxes or radio buttons, and contains an application-defined text (label).</span></span>

<span data-ttu-id="46027-108">El único propósito de un cuadro de grupo es organizar los controles relacionados con un propósito común, indicado por la etiqueta.</span><span class="sxs-lookup"><span data-stu-id="46027-108">The sole purpose of a group box is to organize controls related by a common purpose, indicated by the label.</span></span>

<span data-ttu-id="46027-109">El nombre de clase de ventana de un cuadro de grupo es "BUTTON".</span><span class="sxs-lookup"><span data-stu-id="46027-109">The window class name for a group box is "BUTTON".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="46027-110">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="46027-110">IAccessible Methods</span></span>

<span data-ttu-id="46027-111">Un cuadro de grupo admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="46027-111">A group box supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="46027-112">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="46027-112">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="46027-113">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="46027-113">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="46027-114">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="46027-114">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)

## <a name="iaccessible-properties"></a><span data-ttu-id="46027-115">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="46027-115">IAccessible Properties</span></span>

<span data-ttu-id="46027-116">Un cuadro de grupo admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="46027-116">A group box supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="46027-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="46027-117">Property</span></span>                                                                             | <span data-ttu-id="46027-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="46027-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="46027-119">**obtener \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="46027-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)             | <span data-ttu-id="46027-120">La propiedad **ChildCount** siempre es cero.</span><span class="sxs-lookup"><span data-stu-id="46027-120">The **ChildCount** property is always zero.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="46027-121">**obtener \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="46027-121">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="46027-122">**obtener \_ accKeyboardShortcut**</span><span class="sxs-lookup"><span data-stu-id="46027-122">**get\_accKeyboardShortcut**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_acckeyboardshortcut) | <span data-ttu-id="46027-123">Los cuadros de grupo no tienen métodos abreviados de teclado.</span><span class="sxs-lookup"><span data-stu-id="46027-123">Group boxes do not have keyboard shortcuts.</span></span> <span data-ttu-id="46027-124">Sin embargo, si el texto de la ventana del cuadro de grupo contiene un carácter de y comercial (&), Microsoft Active Accessibility devuelve una cadena que no es NULL como la propiedad **KeyboardShortcut** .</span><span class="sxs-lookup"><span data-stu-id="46027-124">However, if the window text for the group box contains an ampersand (&) character, Microsoft Active Accessibility returns a non-Null string as the **KeyboardShortcut** property.</span></span>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="46027-125">**obtener \_ accName**</span><span class="sxs-lookup"><span data-stu-id="46027-125">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                         | <span data-ttu-id="46027-126">La propiedad **Name** se obtiene del texto (o título) de la ventana del control, que se muestra con el cuadro de grupo.</span><span class="sxs-lookup"><span data-stu-id="46027-126">The **Name** property is obtained from the control's window text (or caption), which is displayed with the group box.</span></span>                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="46027-127">**obtener \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="46027-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)                     | <span data-ttu-id="46027-128">La propiedad **primaria** es una ventana ( [**\_ \_ ventana del sistema de roles**](object-roles.md) ) que rodea el control y tiene la misma propiedad de **nombre** y el mismo nombre de clase de ventana que el control.</span><span class="sxs-lookup"><span data-stu-id="46027-128">The **Parent** property is a window ( [**ROLE\_SYSTEM\_WINDOW**](object-roles.md) ) that surrounds the control and has the same **Name** property and window class name as the control.</span></span>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="46027-129">**obtener \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="46027-129">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                         | <span data-ttu-id="46027-130">La propiedad **role** es [**la \_ \_ agrupación del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="46027-130">The **Role** property is [**ROLE\_SYSTEM\_GROUPING**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="46027-131">**obtener \_ accState**</span><span class="sxs-lookup"><span data-stu-id="46027-131">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                       | <span data-ttu-id="46027-132">La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md):[**sistema de estado \_ \_ invisible**](object-state-constants.md) \| [**estado \_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_ centrado**](object-state-constants.md) en \| [**\_ \_**](object-state-constants.md) sistema enfocable</span><span class="sxs-lookup"><span data-stu-id="46027-132">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="46027-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="46027-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46027-134">IAccessible (interfaz)</span><span class="sxs-lookup"><span data-stu-id="46027-134">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





