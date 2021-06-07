---
title: Ventana Cambiar (Referencia del elemento de interfaz de usuario de MSAA)
description: La ventana de conmutador se muestra cada vez que un usuario presiona ALT+TAB para cambiar a otra aplicación. La ventana de conmutador contiene un icono para cada aplicación que se está ejecutando actualmente.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa12b5fa3bfb9e6207ddaff4133b030e6c233c3
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443986"
---
# <a name="switch-window-msaa-ui-element-reference"></a><span data-ttu-id="bcfa5-104">Ventana Cambiar (Referencia del elemento de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="bcfa5-104">Switch Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="bcfa5-105">La ventana de conmutador se muestra cada vez que un usuario presiona ALT+TAB para cambiar a otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="bcfa5-105">The switch window displays whenever a user presses ALT+TAB to switch to a different application.</span></span> <span data-ttu-id="bcfa5-106">La ventana de conmutador contiene un icono para cada aplicación que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="bcfa5-106">The switch window contains an icon for each application currently running.</span></span>

<span data-ttu-id="bcfa5-107">El nombre de clase de ventana para la ventana del conmutador es \# "32771".</span><span class="sxs-lookup"><span data-stu-id="bcfa5-107">The window class name for the switch window is "\#32771".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="bcfa5-108">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="bcfa5-108">IAccessible Methods</span></span>

<span data-ttu-id="bcfa5-109">La ventana switch admite los siguientes [**métodos IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)</span><span class="sxs-lookup"><span data-stu-id="bcfa5-109">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="bcfa5-110">Método</span><span class="sxs-lookup"><span data-stu-id="bcfa5-110">Method</span></span>                                                                    | <span data-ttu-id="bcfa5-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="bcfa5-111">Comments</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bcfa5-112">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="bcfa5-112">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="bcfa5-113">El propio objeto de ventana switch no tiene una **propiedad DefaultAction.**</span><span class="sxs-lookup"><span data-stu-id="bcfa5-113">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="bcfa5-114">El [**método accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) para cada elemento de la ventana de modificador activa el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="bcfa5-114">The [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) method for each item in the switch window activates the specified item.</span></span> |
| [<span data-ttu-id="bcfa5-115">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="bcfa5-115">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="bcfa5-116">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="bcfa5-116">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="bcfa5-117">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="bcfa5-117">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="bcfa5-118">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="bcfa5-118">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="bcfa5-119">Propiedades IAccessible</span><span class="sxs-lookup"><span data-stu-id="bcfa5-119">IAccessible Properties</span></span>

<span data-ttu-id="bcfa5-120">La ventana switch admite las siguientes [**propiedades IAccessible:**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)</span><span class="sxs-lookup"><span data-stu-id="bcfa5-120">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



|      <span data-ttu-id="bcfa5-121">Propiedad</span><span class="sxs-lookup"><span data-stu-id="bcfa5-121">Property</span></span>                                                                          |      <span data-ttu-id="bcfa5-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="bcfa5-122">Description</span></span>                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bcfa5-123">**get \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="bcfa5-123">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="bcfa5-124">La **propiedad ChildCount** es cero.</span><span class="sxs-lookup"><span data-stu-id="bcfa5-124">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="bcfa5-125">**get \_ accDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="bcfa5-125">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="bcfa5-126">El propio objeto de ventana switch no tiene una **propiedad DefaultAction.**</span><span class="sxs-lookup"><span data-stu-id="bcfa5-126">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="bcfa5-127">La **propiedad DefaultAction** para cada elemento de la ventana de modificador es "Switch".</span><span class="sxs-lookup"><span data-stu-id="bcfa5-127">The **DefaultAction** property for each item in the switch window is "Switch".</span></span>                                                                     |
| [<span data-ttu-id="bcfa5-128">**get \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="bcfa5-128">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | <span data-ttu-id="bcfa5-129">El objeto primario de la ventana de conmutador no puede recibir el foco; solo los elementos secundarios individuales pueden recibir el foco.</span><span class="sxs-lookup"><span data-stu-id="bcfa5-129">The switch window parent object cannot receive focus; only the individual children can receive focus.</span></span>                                                                                                                          |
| [<span data-ttu-id="bcfa5-130">**get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="bcfa5-130">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="bcfa5-131">El propio objeto de ventana de modificador no tiene una **propiedad Name.**</span><span class="sxs-lookup"><span data-stu-id="bcfa5-131">The switch window object itself does not have a **Name** property.</span></span> <span data-ttu-id="bcfa5-132">La **propiedad** Nombre de cada icono de aplicación de la ventana del conmutador es la misma que el nombre de la aplicación que se muestra.</span><span class="sxs-lookup"><span data-stu-id="bcfa5-132">The **Name** property for each application icon in the switch window is the same as the displayed application name.</span></span>                                         |
| [<span data-ttu-id="bcfa5-133">**get \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="bcfa5-133">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="bcfa5-134">El propio objeto de ventana de modificador tiene **una propiedad Role** de "ventana \[ 32771". \]</span><span class="sxs-lookup"><span data-stu-id="bcfa5-134">The switch window object itself has a **Role** property of "window \[32771\]".</span></span> <span data-ttu-id="bcfa5-135">Además, cada icono de aplicación de la ventana de modificador tiene **la** propiedad Role [**ROLE SYSTEM \_ \_ LISTITEM**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="bcfa5-135">Also, each application icon in the switch window has the **Role** property [**ROLE\_SYSTEM\_LISTITEM**](object-roles.md).</span></span> |
| [<span data-ttu-id="bcfa5-136">**get \_ accState**</span><span class="sxs-lookup"><span data-stu-id="bcfa5-136">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="bcfa5-137">El propio objeto de ventana de modificador no admite la **propiedad State.**</span><span class="sxs-lookup"><span data-stu-id="bcfa5-137">The switch window object itself does not support the **State** property.</span></span> <span data-ttu-id="bcfa5-138">El **valor de** Estado de los elementos de vista de lista es STATE SYSTEM [**\_ \_ FOCUSABLE.**](object-state-constants.md)</span><span class="sxs-lookup"><span data-stu-id="bcfa5-138">The **State** value for the list view items is [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md).</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="bcfa5-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bcfa5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bcfa5-140">Interfaz IAccessible</span><span class="sxs-lookup"><span data-stu-id="bcfa5-140">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




