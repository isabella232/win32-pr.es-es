---
title: Consideraciones de diseño para objetos proxy
description: El diseño de objetos proxy y accesibles depende del diseño de los elementos de la interfaz de usuario del servidor. Independientemente del diseño, un elemento de la interfaz de usuario debe notificar a su objeto proxy justo antes de que se destruya para que el objeto proxy controle las llamadas de los clientes de forma adecuada.
ms.assetid: 83a9ff66-2fe6-4589-a187-cdaf207b02b8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9578c79f93f91834dec14808a1a1867f40b215a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075310"
---
# <a name="design-considerations-for-proxy-objects"></a><span data-ttu-id="8793e-104">Consideraciones de diseño para objetos proxy</span><span class="sxs-lookup"><span data-stu-id="8793e-104">Design Considerations for Proxy Objects</span></span>

<span data-ttu-id="8793e-105">El diseño de objetos proxy y accesibles depende del diseño de los elementos de la interfaz de usuario del servidor.</span><span class="sxs-lookup"><span data-stu-id="8793e-105">Proxy and accessible object design depends on the design of the server UI elements.</span></span> <span data-ttu-id="8793e-106">Independientemente del diseño, un elemento de la interfaz de usuario debe notificar a su objeto proxy justo antes de que se destruya para que el objeto proxy controle las llamadas de los clientes de forma adecuada.</span><span class="sxs-lookup"><span data-stu-id="8793e-106">Regardless of the design, a UI element must notify its proxy object right before it is destroyed so that the proxy object handles calls from clients appropriately.</span></span>

<span data-ttu-id="8793e-107">En la lista siguiente se describen dos posibilidades de diseño:</span><span class="sxs-lookup"><span data-stu-id="8793e-107">The following list describes two design possibilities:</span></span>

-   <span data-ttu-id="8793e-108">Coloque el código que implementa la interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en el mismo módulo que el código que implementa el elemento de la interfaz de usuario si el código de la interfaz de usuario es fácilmente extensible.</span><span class="sxs-lookup"><span data-stu-id="8793e-108">Place the code that implements the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface in the same module as the code that implements the user interface element if the user interface code is easily extensible.</span></span> <span data-ttu-id="8793e-109">En este caso, el proxy es "ligero" en el sentido de que todo lo que hace es supervisar la duración del objeto accesible, reenviar las llamadas al objeto accesible y devolver los resultados.</span><span class="sxs-lookup"><span data-stu-id="8793e-109">In this case, the proxy is "lightweight" in the sense that all it does is monitor the life span of the accessible object, forward calls to the accessible object, and return the results.</span></span>
-   <span data-ttu-id="8793e-110">Coloque el código que implementa [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) en el mismo módulo que el código que implementa el objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="8793e-110">Place the code that implements [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) in the same module as the code that implements the proxy object.</span></span> <span data-ttu-id="8793e-111">En este caso, el objeto accesible usa funciones internas para obtener información sobre el elemento de la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="8793e-111">In this case, the accessible object uses internal functions to obtain information about the UI element.</span></span>

## <a name="trackbar-controls"></a><span data-ttu-id="8793e-112">Controles TrackBar</span><span class="sxs-lookup"><span data-stu-id="8793e-112">Trackbar Controls</span></span>

<span data-ttu-id="8793e-113">Al implementar controles TrackBar, use el estilo de barra de control **TBS \_ invertido** para proporcionar información más significativa.</span><span class="sxs-lookup"><span data-stu-id="8793e-113">When implementing trackbar controls, use the trackbar style **TBS\_REVERSED** to provide more meaningful information.</span></span> <span data-ttu-id="8793e-114">Este estilo invierte la escala usada por [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span><span class="sxs-lookup"><span data-stu-id="8793e-114">This style reverses the scale used by [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue).</span></span>

<span data-ttu-id="8793e-115">En el caso de los trackbars verticales sin este estilo, [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) devuelve cero (0) cuando el control de posición de la barra de progreso está en la parte superior del control; los valores aumentan a medida que se desliza el dedo hacia la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="8793e-115">For vertical trackbars without this style, [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) returns zero (0) when the trackbar thumb is at the top of the control; the values increase as you slide the thumb toward the bottom.</span></span> <span data-ttu-id="8793e-116">Con el **estilo \_ invertido de TBS** , **IAccessible:: get \_ accValue** devuelve 100 (100) cuando el control de posición está en la parte superior; los números disminuyen a medida que se mueve el control de barra de desplazamiento hacia la parte inferior.</span><span class="sxs-lookup"><span data-stu-id="8793e-116">With the **TBS\_REVERSED** style, **IAccessible::get\_accValue** returns one hundred (100) when the trackbar thumb is at the top; the numbers decrease as you move the trackbar thumb toward the bottom.</span></span>

<span data-ttu-id="8793e-117">En el caso de trackbars horizontal sin este estilo, se devuelve cero (0) cuando el control de posición de la barra de desplazamiento está en el extremo izquierdo del control. los valores aumentan a medida que mueve el control de barra de desplazamiento hacia la derecha.</span><span class="sxs-lookup"><span data-stu-id="8793e-117">For horizontal trackbars without this style, zero (0) is returned when the trackbar thumb is at the left end of the control; the values increase as you move the trackbar thumb to the right.</span></span> <span data-ttu-id="8793e-118">Con el **estilo \_ invertido de TBS** , [**IAccessible:: get \_ accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) devuelve 100 (100) cuando el control de la barra de desplazamiento está a la izquierda; los valores disminuyen cuando se mueve el control de posición de la barra de desplazamiento a la derecha.</span><span class="sxs-lookup"><span data-stu-id="8793e-118">With the **TBS\_REVERSED** style, [**IAccessible::get\_accValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accvalue) returns one hundred (100) when the trackbar thumb is at the left; the values decrease as you move the trackbar thumb to the right.</span></span>

 

 




