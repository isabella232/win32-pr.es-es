---
title: Recuperar un objeto IAccessible
description: Microsoft Active Accessibility proporciona funciones como AccessibleObjectFromWindow y AccessibleObjectFromPoint que permiten a los clientes recuperar objetos accesibles.
ms.assetid: 971cbead-128b-465a-8e77-2a20217f8d0f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89237916597f27c7179fce9516df1e0ecf43a6db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104356801"
---
# <a name="retrieving-an-iaccessible-object"></a><span data-ttu-id="661db-103">Recuperar un objeto IAccessible</span><span class="sxs-lookup"><span data-stu-id="661db-103">Retrieving an IAccessible Object</span></span>

<span data-ttu-id="661db-104">Microsoft Active Accessibility proporciona funciones como [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) y [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) que permiten a los clientes recuperar objetos accesibles.</span><span class="sxs-lookup"><span data-stu-id="661db-104">Microsoft Active Accessibility provides functions such as [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) and [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) that allow clients to retrieve accessible objects.</span></span> <span data-ttu-id="661db-105">Estas funciones devuelven un puntero de la interfaz [**IDispatch**](idispatch-interface.md) o [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) a través del cual los clientes obtienen información sobre el objeto accesible.</span><span class="sxs-lookup"><span data-stu-id="661db-105">These functions return either an [**IDispatch**](idispatch-interface.md) or [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer through which clients get information about the accessible object.</span></span>

<span data-ttu-id="661db-106">Cuando un cliente llama a [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) o a cualquiera de las otras funciones \**AccessibleObjectFrom \* \* \* X* que recuperan una interfaz en un objeto, Microsoft Active Accessibility envía el mensaje de ventana de la ventana de mensajes [**\_ GETOBJECT de WM**](wm-getobject.md) al procedimiento de ventana aplicable dentro de la aplicación correspondiente.</span><span class="sxs-lookup"><span data-stu-id="661db-106">When a client calls [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) or any of the other \**AccessibleObjectFrom\*\*\*X* functions that retrieve an interface to an object, Microsoft Active Accessibility sends the [**WM\_GETOBJECT**](wm-getobject.md) window message to the applicable window procedure within the appropriate application.</span></span> <span data-ttu-id="661db-107">Para proporcionar información a los clientes, los servidores deben responder al mensaje de la **\_ GETOBJECT de WM** .</span><span class="sxs-lookup"><span data-stu-id="661db-107">To provide information to clients, servers must respond to the **WM\_GETOBJECT** message.</span></span>

<span data-ttu-id="661db-108">Para recopilar información específica acerca de un elemento de la interfaz de usuario, los clientes deben recuperar primero una interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento.</span><span class="sxs-lookup"><span data-stu-id="661db-108">To collect specific information about a UI element, clients must first retrieve an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface for the element.</span></span> <span data-ttu-id="661db-109">Para recuperar el objeto **IAccessible** de un elemento, los clientes pueden utilizar una de las funciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="661db-109">To retrieve an element's **IAccessible** object, clients can use one of the following functions:</span></span>

-   [<span data-ttu-id="661db-110">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="661db-110">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [<span data-ttu-id="661db-111">**AccessibleObjectFromWindow**</span><span class="sxs-lookup"><span data-stu-id="661db-111">**AccessibleObjectFromWindow**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [<span data-ttu-id="661db-112">**AccessibleObjectFromEvent**</span><span class="sxs-lookup"><span data-stu-id="661db-112">**AccessibleObjectFromEvent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)

<span data-ttu-id="661db-113">**Para recuperar un puntero de interfaz IAccessible**</span><span class="sxs-lookup"><span data-stu-id="661db-113">**To retrieve an IAccessible Interface Pointer**</span></span>

1.  <span data-ttu-id="661db-114">El cliente llama a una de las funciones \**AccessibleObjectFrom \* \* \* X* .</span><span class="sxs-lookup"><span data-stu-id="661db-114">Client calls one of the \**AccessibleObjectFrom\*\*\*X* functions.</span></span>
2.  <span data-ttu-id="661db-115">Oleacc.dll envía un mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) al servidor.</span><span class="sxs-lookup"><span data-stu-id="661db-115">Oleacc.dll sends a [**WM\_GETOBJECT**](wm-getobject.md) message to server.</span></span>
3.  <span data-ttu-id="661db-116">El servidor determina qué elemento de la interfaz de usuario corresponde a la solicitud.</span><span class="sxs-lookup"><span data-stu-id="661db-116">The server determines which UI element corresponds to the request.</span></span>
4.  <span data-ttu-id="661db-117">El servidor devuelve cero para solicitar un proxy de Oleacc.dll,</span><span class="sxs-lookup"><span data-stu-id="661db-117">The server either returns zero to request an Oleacc.dll proxy,</span></span>

    <span data-ttu-id="661db-118">O bien</span><span class="sxs-lookup"><span data-stu-id="661db-118">Or</span></span>

    <span data-ttu-id="661db-119">Devuelve un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) (implementación nativa).</span><span class="sxs-lookup"><span data-stu-id="661db-119">Returns an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object (native implementation).</span></span> <span data-ttu-id="661db-120">Para ello, haga lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="661db-120">To do this, it:</span></span>

    -   <span data-ttu-id="661db-121">Construye un objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) para el elemento.</span><span class="sxs-lookup"><span data-stu-id="661db-121">Constructs an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object for the element.</span></span>
    -   <span data-ttu-id="661db-122">Llama a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) para calcular las referencias del puntero del objeto.</span><span class="sxs-lookup"><span data-stu-id="661db-122">Calls [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) to marshal the object's pointer.</span></span>
    -   <span data-ttu-id="661db-123">Devuelve LRESULT que se va a Oleacc.dll.</span><span class="sxs-lookup"><span data-stu-id="661db-123">Returns the LRESULT to Oleacc.dll.</span></span>

5.  <span data-ttu-id="661db-124">Oleacc.dll examina el valor devuelto de [**WM \_ GETOBJECT**](wm-getobject.md).</span><span class="sxs-lookup"><span data-stu-id="661db-124">Oleacc.dll examines the return value from [**WM\_GETOBJECT**](wm-getobject.md).</span></span>

    <span data-ttu-id="661db-125">Si es cero, Oleacc.dll crea un objeto proxy y lo devuelve al cliente.</span><span class="sxs-lookup"><span data-stu-id="661db-125">If it is zero, Oleacc.dll constructs a proxy object and returns it to the client.</span></span>

    <span data-ttu-id="661db-126">O bien</span><span class="sxs-lookup"><span data-stu-id="661db-126">Or</span></span>

    <span data-ttu-id="661db-127">Si es distinto de cero, Oleacc.dll llama a [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) para anular las referencias del puntero de objeto [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) nativo y lo devuelve al cliente.</span><span class="sxs-lookup"><span data-stu-id="661db-127">If it is nonzero, Oleacc.dll calls [**ObjectFromLresult**](/windows/desktop/api/Oleacc/nf-oleacc-objectfromlresult) to unmarshal the native [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object pointer and returns it to the client.</span></span>

 

 




