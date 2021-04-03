---
title: Ventana conmutador (referencia de elementos de interfaz de usuario de MSAA)
description: La ventana conmutador aparece siempre que un usuario presiona ALT + TAB para cambiar a otra aplicación. La ventana conmutador contiene un icono para cada aplicación que se está ejecutando.
ms.assetid: 77b32eb1-7722-410b-b141-ac09fc7fdffb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eead618e23f8a56c90b37eae2386f16a90f6dd67
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779663"
---
# <a name="switch-window-msaa-ui-element-reference"></a><span data-ttu-id="f36e1-104">Ventana conmutador (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="f36e1-104">Switch Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="f36e1-105">La ventana conmutador aparece siempre que un usuario presiona ALT + TAB para cambiar a otra aplicación.</span><span class="sxs-lookup"><span data-stu-id="f36e1-105">The switch window displays whenever a user presses ALT+TAB to switch to a different application.</span></span> <span data-ttu-id="f36e1-106">La ventana conmutador contiene un icono para cada aplicación que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="f36e1-106">The switch window contains an icon for each application currently running.</span></span>

<span data-ttu-id="f36e1-107">El nombre de la clase de ventana de la ventana de conmutador es " \# 32771".</span><span class="sxs-lookup"><span data-stu-id="f36e1-107">The window class name for the switch window is "\#32771".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="f36e1-108">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="f36e1-108">IAccessible Methods</span></span>

<span data-ttu-id="f36e1-109">La ventana switch admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="f36e1-109">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>



| <span data-ttu-id="f36e1-110">Método</span><span class="sxs-lookup"><span data-stu-id="f36e1-110">Method</span></span>                                                                    | <span data-ttu-id="f36e1-111">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f36e1-111">Comments</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f36e1-112">**accDoDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="f36e1-112">**accDoDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) | <span data-ttu-id="f36e1-113">El propio objeto de ventana modificador no tiene una propiedad **DEFAULTACTION** .</span><span class="sxs-lookup"><span data-stu-id="f36e1-113">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="f36e1-114">El método [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) de cada elemento de la ventana switch activa el elemento especificado.</span><span class="sxs-lookup"><span data-stu-id="f36e1-114">The [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) method for each item in the switch window activates the specified item.</span></span> |
| [<span data-ttu-id="f36e1-115">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="f36e1-115">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)                 |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="f36e1-116">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="f36e1-116">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="f36e1-117">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="f36e1-117">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)               |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="f36e1-118">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="f36e1-118">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)                   |                                                                                                                                                                                                                                   |



 

## <a name="iaccessible-properties"></a><span data-ttu-id="f36e1-119">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="f36e1-119">IAccessible Properties</span></span>

<span data-ttu-id="f36e1-120">La ventana switch admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="f36e1-120">The switch window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



|                                                                                |                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f36e1-121">**obtener \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="f36e1-121">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount)       | <span data-ttu-id="f36e1-122">La propiedad **ChildCount** es cero.</span><span class="sxs-lookup"><span data-stu-id="f36e1-122">The **ChildCount** property is zero.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="f36e1-123">**obtener \_ accDefaultAction**</span><span class="sxs-lookup"><span data-stu-id="f36e1-123">**get\_accDefaultAction**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) | <span data-ttu-id="f36e1-124">El propio objeto de ventana modificador no tiene una propiedad **DEFAULTACTION** .</span><span class="sxs-lookup"><span data-stu-id="f36e1-124">The switch window object itself does not have a **DefaultAction** property.</span></span> <span data-ttu-id="f36e1-125">La propiedad **DEFAULTACTION** de cada elemento de la ventana switch es "switch".</span><span class="sxs-lookup"><span data-stu-id="f36e1-125">The **DefaultAction** property for each item in the switch window is "Switch".</span></span>                                                                     |
| [<span data-ttu-id="f36e1-126">**obtener \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="f36e1-126">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)                 | <span data-ttu-id="f36e1-127">El objeto primario de la ventana de conmutador no puede recibir el foco; solo los elementos secundarios individuales pueden recibir el foco.</span><span class="sxs-lookup"><span data-stu-id="f36e1-127">The switch window parent object cannot receive focus; only the individual children can receive focus.</span></span>                                                                                                                          |
| [<span data-ttu-id="f36e1-128">**obtener \_ accName**</span><span class="sxs-lookup"><span data-stu-id="f36e1-128">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)                   | <span data-ttu-id="f36e1-129">El propio objeto de ventana conmutador no tiene una propiedad **nombre** .</span><span class="sxs-lookup"><span data-stu-id="f36e1-129">The switch window object itself does not have a **Name** property.</span></span> <span data-ttu-id="f36e1-130">La propiedad **Name** de cada icono de la aplicación en la ventana de conmutador es igual que el nombre de aplicación mostrado.</span><span class="sxs-lookup"><span data-stu-id="f36e1-130">The **Name** property for each application icon in the switch window is the same as the displayed application name.</span></span>                                         |
| [<span data-ttu-id="f36e1-131">**obtener \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="f36e1-131">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)                   | <span data-ttu-id="f36e1-132">El propio objeto de ventana conmutador tiene una propiedad **role** de "Window \[ 32771 \] ".</span><span class="sxs-lookup"><span data-stu-id="f36e1-132">The switch window object itself has a **Role** property of "window \[32771\]".</span></span> <span data-ttu-id="f36e1-133">Además, cada icono de aplicación de la ventana de conmutador tiene la propiedad de **rol** [**\_ \_ ListItem del sistema de rol**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="f36e1-133">Also, each application icon in the switch window has the **Role** property [**ROLE\_SYSTEM\_LISTITEM**](object-roles.md).</span></span> |
| [<span data-ttu-id="f36e1-134">**obtener \_ accState**</span><span class="sxs-lookup"><span data-stu-id="f36e1-134">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)                 | <span data-ttu-id="f36e1-135">El propio objeto de ventana modificador no admite la propiedad **State** .</span><span class="sxs-lookup"><span data-stu-id="f36e1-135">The switch window object itself does not support the **State** property.</span></span> <span data-ttu-id="f36e1-136">El valor de **Estado** de los elementos de la vista de lista es el [**sistema de estado \_ \_ enfocable**](object-state-constants.md).</span><span class="sxs-lookup"><span data-stu-id="f36e1-136">The **State** value for the list view items is [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md).</span></span>                     |



 

## <a name="related-topics"></a><span data-ttu-id="f36e1-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f36e1-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f36e1-138">IAccessible (interfaz)</span><span class="sxs-lookup"><span data-stu-id="f36e1-138">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




