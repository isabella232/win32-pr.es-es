---
title: Cómo controlar WM_GETOBJECT
description: Cuando recibe un mensaje de WM \_ GETOBJECT que contiene \_ el cliente de OBJID, el servidor debe devolver un puntero al objeto que implementa IAccessible.
ms.assetid: 455398b7-f748-4ab0-8953-3f74439e44f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6223d75339f537ccf1939f9c9af46a42aa47bfdb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777251"
---
# <a name="how-to-handle-wm_getobject"></a><span data-ttu-id="4a678-103">Cómo administrar WM \_ GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="4a678-103">How to Handle WM\_GETOBJECT</span></span>

<span data-ttu-id="4a678-104">Cuando recibe un mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) que contiene [**el \_ cliente de OBJID**](object-identifiers.md), el servidor debe devolver un puntero al objeto que implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span><span class="sxs-lookup"><span data-stu-id="4a678-104">When it receives a [**WM\_GETOBJECT**](wm-getobject.md) message that contains [**OBJID\_CLIENT**](object-identifiers.md), the server must return a pointer to the object that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible).</span></span> <span data-ttu-id="4a678-105">Este puntero es un LRESULT que se obtiene llamando a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span><span class="sxs-lookup"><span data-stu-id="4a678-105">This pointer is an LRESULT that is obtained by calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span></span> <span data-ttu-id="4a678-106">Microsoft Active Accessibility, junto con la biblioteca del modelo de objetos componentes (COM), realiza el cálculo de referencias adecuado y pasa el puntero de interfaz **IAccessible** del servidor al cliente.</span><span class="sxs-lookup"><span data-stu-id="4a678-106">Microsoft Active Accessibility, in conjunction with the Component Object Model (COM) library, performs the appropriate marshaling and passes the **IAccessible** interface pointer from the server to the client.</span></span>

<span data-ttu-id="4a678-107">Los servidores deben controlar correctamente el recuento de referencias en el objeto accesible.</span><span class="sxs-lookup"><span data-stu-id="4a678-107">Servers must correctly handle reference counting on the accessible object.</span></span> <span data-ttu-id="4a678-108">Recuerde que cuando se crea un objeto COM, el recuento de referencias es 1.</span><span class="sxs-lookup"><span data-stu-id="4a678-108">Remember that when you create a COM object, the reference count is 1.</span></span> <span data-ttu-id="4a678-109">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) después incrementa el recuento de referencias varias veces.</span><span class="sxs-lookup"><span data-stu-id="4a678-109">[**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) then further increments the reference count several times.</span></span> <span data-ttu-id="4a678-110">Todas las referencias creadas por **LresultFromObject** se liberan automáticamente cuando el objeto ya no se necesita, pero el servidor es responsable de liberar la referencia inicial y, a menos que lo haga, el objeto nunca se destruirá.</span><span class="sxs-lookup"><span data-stu-id="4a678-110">All the references created by **LresultFromObject** are automatically released when the object is no longer needed, but the server is responsible for releasing the initial reference, and unless it does so, the object will never be destroyed.</span></span> <span data-ttu-id="4a678-111">En los ejemplos de las secciones siguientes se muestra cómo liberar referencias a objetos accesibles.</span><span class="sxs-lookup"><span data-stu-id="4a678-111">The examples in the following sections show how to release references to accessible objects.</span></span>

<span data-ttu-id="4a678-112">Normalmente, los servidores controlan [**WM \_ GETOBJECT**](wm-getobject.md) de una de las siguientes maneras:</span><span class="sxs-lookup"><span data-stu-id="4a678-112">Servers typically handle [**WM\_GETOBJECT**](wm-getobject.md) in one of the following ways:</span></span>

-   [<span data-ttu-id="4a678-113">Crear nuevos objetos accesibles</span><span class="sxs-lookup"><span data-stu-id="4a678-113">Create New Accessible Objects</span></span>](create-new-accessible-objects.md)
-   [<span data-ttu-id="4a678-114">Reutilizar punteros existentes a objetos</span><span class="sxs-lookup"><span data-stu-id="4a678-114">Reuse Existing Pointers to Objects</span></span>](reuse-existing-pointers-to-objects.md)
-   [<span data-ttu-id="4a678-115">Crear nuevas interfaces para el mismo objeto</span><span class="sxs-lookup"><span data-stu-id="4a678-115">Create New Interfaces to the Same Object</span></span>](create-new-interfaces-to-the-same-object.md)

> [!Note]  
> <span data-ttu-id="4a678-116">En esta sección, como en el resto de la documentación, cuando se analiza un puntero a una interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , este puntero puede ser realmente un puntero a un objeto proxy que contiene la interfaz **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="4a678-116">In this section as in the rest of the documentation, when a pointer to an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is discussed, this pointer may actually be a pointer to a proxy object that wraps the **IAccessible** interface.</span></span> <span data-ttu-id="4a678-117">Para obtener más información acerca de los objetos proxy, consulte [crear objetos proxy](creating-proxy-objects.md).</span><span class="sxs-lookup"><span data-stu-id="4a678-117">For more information about proxy objects, see [Creating Proxy Objects](creating-proxy-objects.md).</span></span>

 

<span data-ttu-id="4a678-118">Para obtener información general de [**WM \_ GetObject**](wm-getobject.md), consulte [how \_ GetObject Works](how-wm-getobject-works.md).</span><span class="sxs-lookup"><span data-stu-id="4a678-118">For an overview of [**WM\_GETOBJECT**](wm-getobject.md), see [How WM\_GETOBJECT Works](how-wm-getobject-works.md).</span></span>

 

 




