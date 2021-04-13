---
title: Usar OBJID \_ NATIVEOM para exponer una interfaz nativa para una ventana
description: Esta técnica permite a los clientes obtener un objeto personalizado para una ventana. Los servidores pueden utilizar esto para exponer un puntero a un objeto de documento personalizado para una ventana.
ms.assetid: 91713fe5-f03f-464e-88ee-9d8d66d5b19d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2c5c6ec194ca643475444feb5839c02d3fa890
ms.sourcegitcommit: 2e9db3c7d9a3dbea15196b03c883846fad6f32be
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "104419862"
---
# <a name="use-objid_nativeom-to-expose-a-native-interface-for-a-window"></a><span data-ttu-id="f78fb-104">Usar OBJID \_ NATIVEOM para exponer una interfaz nativa para una ventana</span><span class="sxs-lookup"><span data-stu-id="f78fb-104">Use OBJID\_NATIVEOM to expose a native interface for a window</span></span>

<span data-ttu-id="f78fb-105">Esta técnica permite a los clientes obtener un objeto personalizado para una ventana.</span><span class="sxs-lookup"><span data-stu-id="f78fb-105">This technique allows clients to get a custom object for a window.</span></span> <span data-ttu-id="f78fb-106">Los servidores pueden utilizar esto para exponer un puntero a un objeto de documento personalizado para una ventana.</span><span class="sxs-lookup"><span data-stu-id="f78fb-106">Servers can use this to expose a pointer to a custom document object for a window.</span></span>

<span data-ttu-id="f78fb-107">**Para exponer una interfaz nativa del modelo de objetos para una ventana (servidores)**</span><span class="sxs-lookup"><span data-stu-id="f78fb-107">**To expose a native object model interface for a window (servers)**</span></span>

1.  <span data-ttu-id="f78fb-108">Controle el mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) en el procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="f78fb-108">Handle the [**WM\_GETOBJECT**](wm-getobject.md) message in the window procedure.</span></span> <span data-ttu-id="f78fb-109">Cuando el valor *lParam* es [**OBJID \_ NATIVEOM**](object-identifiers.md), devuelve un puntero de interfaz al objeto personalizado mediante [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span><span class="sxs-lookup"><span data-stu-id="f78fb-109">When the *lParam* value is [**OBJID\_NATIVEOM**](object-identifiers.md), return an interface pointer to the custom object using [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject).</span></span>
2.  <span data-ttu-id="f78fb-110">Libere el puntero de interfaz después de llamar a [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), si es necesario.</span><span class="sxs-lookup"><span data-stu-id="f78fb-110">Release your interface pointer after calling [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject), if appropriate.</span></span> <span data-ttu-id="f78fb-111">Para obtener más información, vea **LresultFromObject**.</span><span class="sxs-lookup"><span data-stu-id="f78fb-111">For more information, see **LresultFromObject**.</span></span>

<span data-ttu-id="f78fb-112">Los clientes pueden obtener un puntero a este objeto personalizado.</span><span class="sxs-lookup"><span data-stu-id="f78fb-112">Clients can obtain a pointer to this custom object.</span></span>

<span data-ttu-id="f78fb-113">**Para obtener un puntero para un objeto personalizado para una ventana (clientes)**</span><span class="sxs-lookup"><span data-stu-id="f78fb-113">**To obtain a pointer for a custom object for a window (clients)**</span></span>

-   <span data-ttu-id="f78fb-114">Llame a [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) y pase [**OBJID \_ NATIVEOM**](object-identifiers.md) como segundo parámetro.</span><span class="sxs-lookup"><span data-stu-id="f78fb-114">Call [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) and pass [**OBJID\_NATIVEOM**](object-identifiers.md) as the second parameter.</span></span>

<span data-ttu-id="f78fb-115">Tenga en cuenta los siguientes problemas para esta técnica:</span><span class="sxs-lookup"><span data-stu-id="f78fb-115">Note the following issues for this technique:</span></span>

-   <span data-ttu-id="f78fb-116">Esta técnica es similar a devolver un puntero de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , excepto para el identificador de objeto utilizado y el hecho de que [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) devuelve un objeto personalizado en lugar de **IAccessible**.</span><span class="sxs-lookup"><span data-stu-id="f78fb-116">This technique is similar to returning an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer except for the object ID used and the fact that [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) returns a custom object instead of **IAccessible**.</span></span>
-   <span data-ttu-id="f78fb-117">Los desarrolladores de servidores pueden necesitar publicar información que permita a los clientes identificar de forma única el **hWnd** para que puedan encontrarlo antes de llamar a [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) en su identificador de ventana.</span><span class="sxs-lookup"><span data-stu-id="f78fb-117">Server developers may need to publish information that allows clients to uniquely identify the **HWND** so that they can find it before calling [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) on its window handle.</span></span>
-   <span data-ttu-id="f78fb-118">No implemente la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en el objeto personalizado que se devuelve.</span><span class="sxs-lookup"><span data-stu-id="f78fb-118">Do not implement the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface on the custom object that is returned.</span></span> <span data-ttu-id="f78fb-119">Si lo hace, OLEACC lo tratará como un **IAccessible** estándar y puede impedir que se usen interfaces personalizadas.</span><span class="sxs-lookup"><span data-stu-id="f78fb-119">If you do, OLEACC will treat it is as a standard **IAccessible** and may prevent the custom interfaces from being used.</span></span>
-   <span data-ttu-id="f78fb-120">Para poder usarlos en los procesos, es posible que sea necesario registrar las interfaces del objeto devuelto con el modelo de objetos componentes (COM).</span><span class="sxs-lookup"><span data-stu-id="f78fb-120">In order to be used across processes, the interfaces on the returned object may need to be registered with Component Object Model (COM).</span></span>

<span data-ttu-id="f78fb-121">Esta técnica es compatible con varios componentes de Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="f78fb-121">This technique is supported by several Microsoft Office components.</span></span> <span data-ttu-id="f78fb-122">Para obtener más información, vea [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span><span class="sxs-lookup"><span data-stu-id="f78fb-122">For more information, see [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow).</span></span>

 

 




