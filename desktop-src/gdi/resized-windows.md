---
description: El sistema cambia el tamaño de una ventana cuando el usuario elige comandos de menú de la ventana, como size y Maximize, o cuando la aplicación llama a funciones, como la función SetWindowPos.
ms.assetid: 6f997cba-e4c9-4e27-8309-42b9892ec620
title: Ventanas cambiadas de tamaño
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88f740191f8b85038f17a687ebc547305f882383
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908479"
---
# <a name="resized-windows"></a><span data-ttu-id="3d2e0-103">Ventanas cambiadas de tamaño</span><span class="sxs-lookup"><span data-stu-id="3d2e0-103">Resized Windows</span></span>

<span data-ttu-id="3d2e0-104">El sistema cambia el tamaño de una ventana cuando el usuario elige comandos de menú de la ventana, como size y Maximize, o cuando la aplicación llama a funciones, como la función [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) .</span><span class="sxs-lookup"><span data-stu-id="3d2e0-104">The system changes the size of a window when the user chooses window menu commands, such as Size and Maximize, or when the application calls functions, such as the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function.</span></span> <span data-ttu-id="3d2e0-105">Cuando una ventana cambia de tamaño, el sistema supone que el contenido de la parte expuesta anteriormente de la ventana no se ve afectado y no es necesario volver a dibujarlo.</span><span class="sxs-lookup"><span data-stu-id="3d2e0-105">When a window changes size, the system assumes that the contents of the previously exposed portion of the window are not affected and need not be redrawn.</span></span> <span data-ttu-id="3d2e0-106">El sistema solo invalida la parte recién expuesta de la ventana, lo que ahorra tiempo cuando la aplicación procesa el mensaje de [**\_ pintura de WM**](wm-paint.md) eventual.</span><span class="sxs-lookup"><span data-stu-id="3d2e0-106">The system invalidates only the newly exposed portion of the window, which saves time when the eventual [**WM\_PAINT**](wm-paint.md) message is processed by the application.</span></span> <span data-ttu-id="3d2e0-107">En este caso, **la \_ pintura de WM** no se genera cuando se reduce el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="3d2e0-107">In this case, **WM\_PAINT** is not generated when the size of the window is reduced.</span></span>

<span data-ttu-id="3d2e0-108">En algunas ventanas, cualquier cambio en el tamaño de la ventana invalida el contenido.</span><span class="sxs-lookup"><span data-stu-id="3d2e0-108">For some windows, any change to the size of the window invalidates the contents.</span></span> <span data-ttu-id="3d2e0-109">Por ejemplo, una aplicación de reloj que adapte la superficie del reloj para ajustarse perfectamente dentro de su ventana debe volver a dibujar el reloj cada vez que la ventana cambie de tamaño.</span><span class="sxs-lookup"><span data-stu-id="3d2e0-109">For example, a clock application that adapts the face of the clock to fit neatly within its window must redraw the clock whenever the window changes size.</span></span> <span data-ttu-id="3d2e0-110">Para obligar al sistema a invalidar todo el área cliente de la ventana cuando se realiza un cambio vertical, horizontal o vertical y horizontal, una aplicación debe especificar el estilo CS \_ VREDRAW o CS \_ HREDRAW, o ambos, al registrar la clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="3d2e0-110">To force the system to invalidate the entire client area of the window when a vertical, horizontal, or both vertical and horizontal change is made, an application must specify the CS\_VREDRAW or CS\_HREDRAW style, or both, when registering the window class.</span></span> <span data-ttu-id="3d2e0-111">Cualquier ventana que pertenezca a una clase de ventana que tenga estos estilos se invalida cada vez que el usuario o la aplicación cambia el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="3d2e0-111">Any window belonging to a window class having these styles is invalidated each time the user or the application changes the size of the window.</span></span>

 

 
