---
title: Comunicación entre cliente y servidor
description: El mecanismo WinEvents proporciona una manera para que los servidores se comuniquen fácilmente con los clientes de Microsoft Active Accessibility.
ms.assetid: 992fe603-dcfe-4afd-88db-6d258a7a5f64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95b29170d5a903493977af130ef6d48bb3b896b6
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "105704885"
---
# <a name="clientserver-communication"></a><span data-ttu-id="e0d01-103">Comunicación entre cliente y servidor</span><span class="sxs-lookup"><span data-stu-id="e0d01-103">Client/Server Communication</span></span>

<span data-ttu-id="e0d01-104">El mecanismo [WinEvents](winevents-overview.md) proporciona una manera para que los servidores se comuniquen fácilmente con los clientes de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="e0d01-104">The [WinEvents](winevents-overview.md) mechanism provides a way for servers to communicate easily with Microsoft Active Accessibility clients.</span></span> <span data-ttu-id="e0d01-105">A menudo, los clientes recopilan información al reaccionar a WinEvents (por ejemplo, el siguiente enfoque), pero pueden solicitar información de un servidor en cualquier momento.</span><span class="sxs-lookup"><span data-stu-id="e0d01-105">Clients often collect information by reacting to WinEvents (for example, following focus), but they are free to request information from a server at any time.</span></span>

<span data-ttu-id="e0d01-106">Para solicitar información para un objeto accesible que genera un WinEvent, un cliente debe procesar el evento y establecer una conexión con el objeto accesible pertinente.</span><span class="sxs-lookup"><span data-stu-id="e0d01-106">To request information for an accessible object that generates a WinEvent, a client must process the event and establish a connection with the relevant accessible object.</span></span> <span data-ttu-id="e0d01-107">Para ello, el cliente realiza los seis pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="e0d01-107">To do this, the client performs the following six steps:</span></span>

-   <span data-ttu-id="e0d01-108">Un servidor llama a [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) para generar una notificación WinEvent para cada cambio en sus elementos de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e0d01-108">A server calls [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) to generate a WinEvent notification for each change to its user interface elements.</span></span>
-   <span data-ttu-id="e0d01-109">El código de administración de WinEvent en el usuario determina si alguna aplicación cliente ha registrado una [*función de enlace*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) WinEvent mediante [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) y llama a la función de devolución de llamada registrada.</span><span class="sxs-lookup"><span data-stu-id="e0d01-109">The WinEvent management code in USER determines if any client applications have registered a WinEvent [*hook function*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) using [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) and calls the registered callback function.</span></span>
-   <span data-ttu-id="e0d01-110">En su función de devolución de llamada, el cliente solicita acceso al objeto que generó el evento llamando a [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) u otras funciones de recuperación de objetos accesibles.</span><span class="sxs-lookup"><span data-stu-id="e0d01-110">In its callback function, the client requests access to the object that generated the event by calling [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) or other accessible object retrieval functions.</span></span> <span data-ttu-id="e0d01-111">Para obtener más información, vea [recuperar un objeto IAccessible](retrieving-an-iaccessible-object.md).</span><span class="sxs-lookup"><span data-stu-id="e0d01-111">For more information, see [Retrieving an IAccessible Object](retrieving-an-iaccessible-object.md).</span></span>
-   <span data-ttu-id="e0d01-112">Esta API de Microsoft Active Accessibility envía la aplicación de servidor a un mensaje de [**WM \_ GETOBJECT**](wm-getobject.md) para recuperar el objeto accesible.</span><span class="sxs-lookup"><span data-stu-id="e0d01-112">This Microsoft Active Accessibility API sends the server application a [**WM\_GETOBJECT**](wm-getobject.md) message to retrieve the accessible object.</span></span>
-   <span data-ttu-id="e0d01-113">En respuesta a [**WM \_ GETOBJECT**](wm-getobject.md), la aplicación de servidor devuelve cero o devuelve un valor que actúa como una referencia de una sola vez al objeto que generó el evento.</span><span class="sxs-lookup"><span data-stu-id="e0d01-113">In response to [**WM\_GETOBJECT**](wm-getobject.md), the server application either returns zero or returns a value that acts as a one-time reference to the object that generated the event.</span></span>
-   <span data-ttu-id="e0d01-114">Si el servidor devuelve cero, Microsoft Active Accessibility crea un objeto proxy y proporciona su dirección al cliente.</span><span class="sxs-lookup"><span data-stu-id="e0d01-114">If the server returns zero, Microsoft Active Accessibility creates a proxy object and gives its address to the client.</span></span> <span data-ttu-id="e0d01-115">De lo contrario, Microsoft Active Accessibility usa esta referencia para recuperar la dirección de una interfaz de objeto como [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) o [**IDispatch**](idispatch-interface.md)y proporciona esa dirección al cliente.</span><span class="sxs-lookup"><span data-stu-id="e0d01-115">Otherwise, Microsoft Active Accessibility uses this reference to retrieve the address of an object interface such as [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) or [**IDispatch**](idispatch-interface.md), and gives that address to the client.</span></span>

<span data-ttu-id="e0d01-116">Una vez que el cliente tiene una dirección de interfaz, puede llamar a las propiedades y métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) del objeto accesible para recuperar la información.</span><span class="sxs-lookup"><span data-stu-id="e0d01-116">Once the client has an interface address, it can call the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods of the accessible object to retrieve information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e0d01-117">En esta sección</span><span class="sxs-lookup"><span data-stu-id="e0d01-117">In this section</span></span>

-   [<span data-ttu-id="e0d01-118">WinEvents y Active Accessibility</span><span class="sxs-lookup"><span data-stu-id="e0d01-118">WinEvents and Active Accessibility</span></span>](winevents-overview.md)
-   [<span data-ttu-id="e0d01-119">Cómo \_ funciona WM GETOBJECT</span><span class="sxs-lookup"><span data-stu-id="e0d01-119">How WM\_GETOBJECT Works</span></span>](how-wm-getobject-works.md)
-   [<span data-ttu-id="e0d01-120">Recuperar un objeto IAccessible</span><span class="sxs-lookup"><span data-stu-id="e0d01-120">Retrieving an IAccessible Object</span></span>](retrieving-an-iaccessible-object.md)

 

 




