---
title: Ventana de cliente MDI (referencia de elementos de interfaz de usuario de MSAA)
description: La interfaz de múltiples documentos (MDI) es una especificación que define la interfaz de usuario estándar para las aplicaciones escritas para Windows. Una aplicación MDI permite a un usuario trabajar con más de un documento a la vez.
ms.assetid: ede2dd19-e4c6-43e8-8f22-f807621dfa0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1557176752d29b7d429a0c434554df09b69a8e6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994184"
---
# <a name="mdi-client-window-msaa-ui-element-reference"></a><span data-ttu-id="5e51a-104">Ventana de cliente MDI (referencia de elementos de interfaz de usuario de MSAA)</span><span class="sxs-lookup"><span data-stu-id="5e51a-104">MDI Client Window (MSAA UI Element Reference)</span></span>

<span data-ttu-id="5e51a-105">La interfaz de múltiples documentos (MDI) es una especificación que define la interfaz de usuario estándar para las aplicaciones escritas para Windows.</span><span class="sxs-lookup"><span data-stu-id="5e51a-105">The multiple document interface (MDI) is a specification that defines the standard user interface for applications written for Windows.</span></span> <span data-ttu-id="5e51a-106">Una aplicación MDI permite a un usuario trabajar con más de un documento a la vez.</span><span class="sxs-lookup"><span data-stu-id="5e51a-106">An MDI application enables a user to work with more than one document at a time.</span></span>

<span data-ttu-id="5e51a-107">Una aplicación MDI tiene tres tipos de ventanas: una ventana de marco, una ventana de cliente y un número de ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="5e51a-107">An MDI application has three kinds of windows: a frame window, a client window, and a number of child windows.</span></span> <span data-ttu-id="5e51a-108">La ventana de marco es similar a la ventana principal de una aplicación y se rodea a la ventana de cliente.</span><span class="sxs-lookup"><span data-stu-id="5e51a-108">The frame window is like the main window of an application, and it surrounds the client window.</span></span> <span data-ttu-id="5e51a-109">La ventana de cliente es un elemento secundario de la ventana de marco y sirve de fondo para las ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="5e51a-109">The client window is a child of the frame window and serves as the background for the child windows.</span></span> <span data-ttu-id="5e51a-110">La ventana de cliente también proporciona compatibilidad para crear y manipular las ventanas secundarias en las que se muestran los documentos.</span><span class="sxs-lookup"><span data-stu-id="5e51a-110">The client window also provides support for creating and manipulating the child windows in which documents are displayed.</span></span>

<span data-ttu-id="5e51a-111">El nombre de la clase de ventana de una ventana de cliente MDI es "MDIClient".</span><span class="sxs-lookup"><span data-stu-id="5e51a-111">The window class name for an MDI client window is "MDIClient".</span></span>

## <a name="iaccessible-methods"></a><span data-ttu-id="5e51a-112">Métodos IAccessible</span><span class="sxs-lookup"><span data-stu-id="5e51a-112">IAccessible Methods</span></span>

<span data-ttu-id="5e51a-113">Una ventana de cliente MDI admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="5e51a-113">An MDI client window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods:</span></span>

-   [<span data-ttu-id="5e51a-114">**accHitTest**</span><span class="sxs-lookup"><span data-stu-id="5e51a-114">**accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="5e51a-115">**accLocation**</span><span class="sxs-lookup"><span data-stu-id="5e51a-115">**accLocation**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [<span data-ttu-id="5e51a-116">**accNavigate**</span><span class="sxs-lookup"><span data-stu-id="5e51a-116">**accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="5e51a-117">**accSelect**</span><span class="sxs-lookup"><span data-stu-id="5e51a-117">**accSelect**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a><span data-ttu-id="5e51a-118">Propiedades de IAccessible</span><span class="sxs-lookup"><span data-stu-id="5e51a-118">IAccessible Properties</span></span>

<span data-ttu-id="5e51a-119">Una ventana de cliente MDI admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :</span><span class="sxs-lookup"><span data-stu-id="5e51a-119">An MDI client window supports the following [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties:</span></span>



| <span data-ttu-id="5e51a-120">Propiedad</span><span class="sxs-lookup"><span data-stu-id="5e51a-120">Property</span></span>                                                                 | <span data-ttu-id="5e51a-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5e51a-121">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e51a-122">**obtener \_ accChildCount**</span><span class="sxs-lookup"><span data-stu-id="5e51a-122">**get\_accChildCount**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount) | <span data-ttu-id="5e51a-123">La propiedad **ChildCount** es el número de ventanas secundarias en las que se muestran los documentos.</span><span class="sxs-lookup"><span data-stu-id="5e51a-123">The **ChildCount** property is the number of child windows in which documents are displayed.</span></span>                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="5e51a-124">**obtener \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="5e51a-124">**get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)           |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="5e51a-125">**obtener \_ accName**</span><span class="sxs-lookup"><span data-stu-id="5e51a-125">**get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)             | <span data-ttu-id="5e51a-126">La propiedad **Name** es "Workspace".</span><span class="sxs-lookup"><span data-stu-id="5e51a-126">The **Name** property is "Workspace".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="5e51a-127">**obtener \_ accParent**</span><span class="sxs-lookup"><span data-stu-id="5e51a-127">**get\_accParent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accparent)         | <span data-ttu-id="5e51a-128">La propiedad **primaria** es la ventana de marco MDI.</span><span class="sxs-lookup"><span data-stu-id="5e51a-128">The **Parent** property is the MDI frame window.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="5e51a-129">**obtener \_ accRole**</span><span class="sxs-lookup"><span data-stu-id="5e51a-129">**get\_accRole**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)             | <span data-ttu-id="5e51a-130">La propiedad **role** es [**el \_ \_ cliente del sistema de roles**](object-roles.md)</span><span class="sxs-lookup"><span data-stu-id="5e51a-130">The **Role** property is [**ROLE\_SYSTEM\_CLIENT**](object-roles.md)</span></span>                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="5e51a-131">**obtener \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="5e51a-131">**get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="5e51a-132">**obtener \_ accState**</span><span class="sxs-lookup"><span data-stu-id="5e51a-132">**get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)           | <span data-ttu-id="5e51a-133">La propiedad **Estado** es una combinación de uno o varios de los siguientes [valores](object-state-constants.md): [**sistema de estado \_ \_ invisible**](object-state-constants.md) \| [**estado \_ \_ no disponible**](object-state-constants.md) del sistema de estado \| [**\_ \_ centrado**](object-state-constants.md) en \| [**\_ \_**](object-state-constants.md) sistema enfocable</span><span class="sxs-lookup"><span data-stu-id="5e51a-133">The **State** property is a combination of one or more of the following [values](object-state-constants.md): [**STATE\_SYSTEM\_INVISIBLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_UNAVAILABLE**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSED**](object-state-constants.md) \| [**STATE\_SYSTEM\_FOCUSABLE**](object-state-constants.md)</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5e51a-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5e51a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5e51a-135">IAccessible (interfaz)</span><span class="sxs-lookup"><span data-stu-id="5e51a-135">IAccessible Interface</span></span>](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





