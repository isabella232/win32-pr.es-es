---
description: Cuando se usan varios monitores como pantallas independientes, el escritorio contiene una pantalla o un conjunto de pantallas.
ms.assetid: fbc88c91-3209-4b59-bdbb-0f5ba009a312
title: Usar varios monitores como pantallas independientes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4761e0e04ae1adaa197b06f04fa36c61ccda3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985914"
---
# <a name="using-multiple-monitors-as-independent-displays"></a><span data-ttu-id="b8811-103">Usar varios monitores como pantallas independientes</span><span class="sxs-lookup"><span data-stu-id="b8811-103">Using Multiple Monitors as Independent Displays</span></span>

<span data-ttu-id="b8811-104">Cuando se usan varios monitores como pantallas independientes, el escritorio contiene una pantalla o un conjunto de pantallas.</span><span class="sxs-lookup"><span data-stu-id="b8811-104">When using multiple monitors as independent displays, the desktop contains one display or set of displays.</span></span> <span data-ttu-id="b8811-105">Este conjunto de pantallas incluye siempre el monitor principal y se comporta como se mencionó en las otras secciones de este tema.</span><span class="sxs-lookup"><span data-stu-id="b8811-105">This set of displays always includes the primary monitor and behaves as mentioned in the other sections of this topic.</span></span> <span data-ttu-id="b8811-106">Una aplicación puede utilizar cualquier otro monitor como una pantalla independiente.</span><span class="sxs-lookup"><span data-stu-id="b8811-106">An application can use any other monitor as an independent display.</span></span>

> [!Note]  
> <span data-ttu-id="b8811-107">No se admite el uso de otros monitores como pantallas independientes en los controladores que se implementan en el modelo de controladores de pantalla de Windows (WDDM).</span><span class="sxs-lookup"><span data-stu-id="b8811-107">Using other monitors as independent displays isn't supported on drivers that are implemented to the Windows Display Driver Model (WDDM).</span></span>

 

<span data-ttu-id="b8811-108">El administrador de ventanas no sabe nada acerca de las pantallas independientes.</span><span class="sxs-lookup"><span data-stu-id="b8811-108">The window manager knows nothing about the independent displays.</span></span> <span data-ttu-id="b8811-109">Están completamente controlados por la aplicación y no hay ninguna función de administrador de ventanas disponible para la aplicación (todas las llamadas del administrador de ventanas pasan automáticamente a la pantalla principal).</span><span class="sxs-lookup"><span data-stu-id="b8811-109">They are completely controlled by the application, and no window manager functions are available to the application (all window manager calls automatically go to the primary display).</span></span> <span data-ttu-id="b8811-110">Cada pantalla independiente tiene su propio origen y coordenadas horizontales y verticales, y se obtiene acceso a ellas a través de las funciones GDI como [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) o las funciones de DirectX como **DirectDrawCreate**.</span><span class="sxs-lookup"><span data-stu-id="b8811-110">Each independent display has its own origin and horizontal and vertical coordinates, and is accessed through the GDI functions such as [**CreateDC**](/windows/desktop/api/Wingdi/nf-wingdi-createdca) or the DirectX functions such as **DirectDrawCreate**.</span></span>

<span data-ttu-id="b8811-111">Para buscar las pantallas independientes, llame a [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) y busque las pantallas que no tienen el \_ dispositivo de pantalla \_ conectado \_ a \_ la marca de escritorio en la estructura de [**pantalla del \_ dispositivo**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) .</span><span class="sxs-lookup"><span data-stu-id="b8811-111">To locate the independent displays, call [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) and look for the displays that do not have DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP flag in the [**DISPLAY\_DEVICE**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) structure.</span></span>

<span data-ttu-id="b8811-112">Una aplicación puede abrir una pantalla llamando a</span><span class="sxs-lookup"><span data-stu-id="b8811-112">An application can open a display by calling</span></span>


```C++
hdc = CreateDC(lpszDisplayName, NULL, NULL, lpDevMode);
```



<span data-ttu-id="b8811-113">En esta llamada, el parámetro *lpszDisplayName* es uno de los nombres de dispositivo devueltos por [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) y *lpDevMode* es una descripción del modo gráficos para este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8811-113">In this call, the *lpszDisplayName* parameter is one of the device names returned by [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) and *lpDevMode* is a description of the graphics mode for this device.</span></span> <span data-ttu-id="b8811-114">La HDC resultante se puede usar para realizar cualquier operación de gráficos en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b8811-114">The resulting hdc can be used to perform any graphics operation to the device.</span></span>

 

 



