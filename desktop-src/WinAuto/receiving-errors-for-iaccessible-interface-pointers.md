---
title: Recibir errores de punteros de interfaz IAccessible
description: En este tema se describen situaciones en las que podría recibir un error de un puntero de interfaz IAccessible.
ms.assetid: 408bfa47-fda0-4a25-89c1-da41d967ad61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d3bd9e39dae9c5de9ad1644e5955bd5fb90d2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903675"
---
# <a name="receiving-errors-for-iaccessible-interface-pointers"></a><span data-ttu-id="09b10-103">Recibir errores de punteros de interfaz IAccessible</span><span class="sxs-lookup"><span data-stu-id="09b10-103">Receiving Errors for IAccessible Interface Pointers</span></span>

<span data-ttu-id="09b10-104">En este tema se describen situaciones en las que podría recibir un error de un puntero de interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="09b10-104">This topic describes situations in which you might receive an error for an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span> <span data-ttu-id="09b10-105">Las funciones **IAccessible** pueden devolver errores para los punteros de interfaz **IAccessible** cuando un usuario cierra una aplicación a la que pertenece el objeto, o si un usuario descarta un control a través de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="09b10-105">**IAccessible** functions can return errors for **IAccessible** interface pointers when a user closes an application that the object belongs to, or if a user dismisses a control through the user interface.</span></span>

## <a name="user-closes-an-application"></a><span data-ttu-id="09b10-106">El usuario cierra una aplicación</span><span class="sxs-lookup"><span data-stu-id="09b10-106">User Closes an Application</span></span>

<span data-ttu-id="09b10-107">Si un usuario cierra la aplicación que contiene un objeto al que señala el puntero de la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) , todas las llamadas futuras a ese objeto devolverán un código de error.</span><span class="sxs-lookup"><span data-stu-id="09b10-107">If a user closes the application that contains an object to which the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer was pointing, then all future calls to that object will return an error code.</span></span> <span data-ttu-id="09b10-108">El error, como **Co \_ E \_ OBJNOTCONNECTED**, indicará que el objeto ya no existe.</span><span class="sxs-lookup"><span data-stu-id="09b10-108">The error, such as **CO\_E\_OBJNOTCONNECTED**, will indicate that the object does not exist anymore.</span></span> <span data-ttu-id="09b10-109">Esto se aplica a todos los punteros de interfaz **IAccessible** .</span><span class="sxs-lookup"><span data-stu-id="09b10-109">This applies to all **IAccessible** interface pointers.</span></span>

## <a name="user-dismisses-a-control"></a><span data-ttu-id="09b10-110">El usuario descarta un control</span><span class="sxs-lookup"><span data-stu-id="09b10-110">User Dismisses a Control</span></span>

<span data-ttu-id="09b10-111">Si un usuario descarta un control (por ejemplo, presionando un botón de método de presionado), los clientes pueden seguir llamando a métodos y propiedades de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en este objeto porque el objeto no se ha liberado.</span><span class="sxs-lookup"><span data-stu-id="09b10-111">If a user dismisses a control (for example, by pressing a push button), clients can still call [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) methods and properties on this object because the object has not been released.</span></span> <span data-ttu-id="09b10-112">Sin embargo, las llamadas futuras recibirán mensajes de error.</span><span class="sxs-lookup"><span data-stu-id="09b10-112">However, future calls will receive error messages.</span></span>

<span data-ttu-id="09b10-113">Esta situación se aplica a las siguientes funciones y métodos:</span><span class="sxs-lookup"><span data-stu-id="09b10-113">This situation applies to the following functions and methods:</span></span>

-   [<span data-ttu-id="09b10-114">**AccessibleObjectFromEvent**</span><span class="sxs-lookup"><span data-stu-id="09b10-114">**AccessibleObjectFromEvent**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)
-   [<span data-ttu-id="09b10-115">**AccessibleObjectFromPoint**</span><span class="sxs-lookup"><span data-stu-id="09b10-115">**AccessibleObjectFromPoint**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)
-   [<span data-ttu-id="09b10-116">**AccessibleObjectFromWindow**</span><span class="sxs-lookup"><span data-stu-id="09b10-116">**AccessibleObjectFromWindow**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow)
-   [<span data-ttu-id="09b10-117">**IAccessible:: accHitTest**</span><span class="sxs-lookup"><span data-stu-id="09b10-117">**IAccessible::accHitTest**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [<span data-ttu-id="09b10-118">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="09b10-118">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [<span data-ttu-id="09b10-119">**IAccessible:: get \_ accFocus**</span><span class="sxs-lookup"><span data-stu-id="09b10-119">**IAccessible::get\_accFocus**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accfocus)
-   [<span data-ttu-id="09b10-120">**IAccessible:: get \_ accSelection**</span><span class="sxs-lookup"><span data-stu-id="09b10-120">**IAccessible::get\_accSelection**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accselection)

 

 




