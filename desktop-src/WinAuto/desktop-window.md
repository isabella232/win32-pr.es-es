---
title: Ventana de escritorio (referencia de elementos de interfaz de usuario de MSAA)
description: La ventana escritorio muestra la vista de lista de escritorio (que contiene iconos como Mi PC) y la barra de tareas que contiene el botón Inicio.
ms.assetid: 3668c26e-6462-4219-95d3-507811ed7f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d58208b3993964a367d093174d58d705beda23d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418456"
---
# <a name="desktop-window-msaa-ui-element-reference"></a><span data-ttu-id="4d337-103">Ventana de escritorio (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="4d337-103">Desktop Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="4d337-104">La ventana escritorio muestra la vista de lista de escritorio (que contiene iconos como Mi PC) y la barra de tareas que contiene el botón **Inicio** .</span><span class="sxs-lookup"><span data-stu-id="4d337-104">The desktop window displays the desktop list view (which contains icons such as My Computer) and the taskbar that contains the **Start** button.</span></span>

<span data-ttu-id="4d337-105">Los clientes raramente consultan este objeto porque la vista de lista y la barra de tareas cubren todo el escritorio.</span><span class="sxs-lookup"><span data-stu-id="4d337-105">This object is rarely queried by clients because the list view and the taskbar cover the entire desktop.</span></span> <span data-ttu-id="4d337-106">El objeto de escritorio se recupera al iniciar sesión, antes de que el Shell del sistema operativo muestre la vista de lista y la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="4d337-106">The desktop object is retrieved when you log on, before the operating system shell displays the list view and taskbar.</span></span> <span data-ttu-id="4d337-107">En algunos casos, el escritorio se obtiene al navegar desde otros objetos.</span><span class="sxs-lookup"><span data-stu-id="4d337-107">In some cases, the desktop is obtained when navigating from other objects.</span></span>

<span data-ttu-id="4d337-108">El nombre de la clase de ventana de la ventana de escritorio es " \# 32769".</span><span class="sxs-lookup"><span data-stu-id="4d337-108">The window class name for the desktop window is "\#32769".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="4d337-109">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="4d337-109">IAccessible Methods</span></span>

<span data-ttu-id="4d337-110">La ventana de escritorio admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="4d337-110">The desktop window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="4d337-111">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="4d337-111">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="4d337-112">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="4d337-112">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="4d337-113">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="4d337-113">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="4d337-114">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="4d337-114">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="4d337-115">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="4d337-115">IAccessible Properties</span></span>

<span data-ttu-id="4d337-116">La ventana de escritorio admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="4d337-116">The desktop window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="4d337-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="4d337-117">Property</span></span>                                                                 | <span data-ttu-id="4d337-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="4d337-118">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d337-119">**obtener \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="4d337-119">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="4d337-120">**obtener \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="4d337-120">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="4d337-121">**obtener \_ accName**</span><span class="sxs-lookup"><span data-stu-id="4d337-121">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="4d337-122">La propiedad de nombre es "escritorio".</span><span class="sxs-lookup"><span data-stu-id="4d337-122">The Name property is "Desktop".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="4d337-123">**obtener \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="4d337-123">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="4d337-124">La propiedad **role** es [**el \_ \_ cliente del sistema de roles**](object-roles.md).</span><span class="sxs-lookup"><span data-stu-id="4d337-124">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="4d337-125">**obtener \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="4d337-125">**get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="4d337-126">**obtener \_ accState**</span><span class="sxs-lookup"><span data-stu-id="4d337-126">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="4d337-127">La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md):[**sistema de estado \_ \_ invisible**](object-state-constants.md) \| [**estado \_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_ centrado**](object-state-constants.md) en \| [**\_ \_**](object-state-constants.md) sistema enfocable</span><span class="sxs-lookup"><span data-stu-id="4d337-127">The **State** property is a combination of one or more of the following [values](object-state-constants.md):[**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="4d337-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4d337-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d337-129">IAccessible (interfaz)</span><span class="sxs-lookup"><span data-stu-id="4d337-129">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





