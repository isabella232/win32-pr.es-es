---
description: La función GetSystemMetrics devuelve valores para el monitor principal, excepto SM \_ CXMAXTRACK y SM \_ CYMAXTRACK, que hacen referencia a todo el escritorio.
ms.assetid: d0105363-1895-4e10-8a33-648a6fc4c20a
title: Varias métricas del sistema de supervisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 149f4da5c687df28817105e1ec3876ffd1ab5649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155601"
---
# <a name="multiple-monitor-system-metrics"></a><span data-ttu-id="c53e7-103">Varias métricas del sistema de supervisión</span><span class="sxs-lookup"><span data-stu-id="c53e7-103">Multiple Monitor System Metrics</span></span>

<span data-ttu-id="c53e7-104">La función [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) devuelve valores para el monitor principal, excepto SM \_ CXMAXTRACK y SM \_ CYMAXTRACK, que hacen referencia a todo el escritorio.</span><span class="sxs-lookup"><span data-stu-id="c53e7-104">The [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function returns values for the primary monitor, except for SM\_CXMAXTRACK and SM\_CYMAXTRACK, which refer to the entire desktop.</span></span> <span data-ttu-id="c53e7-105">Las siguientes métricas son las mismas para todos los controladores de dispositivo: SM \_ CXCURSOR, SM \_ CYCURSOR, SM \_ CXICON, SMCYICON.</span><span class="sxs-lookup"><span data-stu-id="c53e7-105">The following metrics are the same for all device drivers: SM\_CXCURSOR, SM\_CYCURSOR, SM\_CXICON, SMCYICON.</span></span> <span data-ttu-id="c53e7-106">Las siguientes funcionalidades de visualización son las mismas para todos los monitores: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.</span><span class="sxs-lookup"><span data-stu-id="c53e7-106">The following display capabilities are the same for all monitors: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.</span></span>

<span data-ttu-id="c53e7-107">[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) también tiene constantes que hacen referencia solo a un sistema de varios monitores.</span><span class="sxs-lookup"><span data-stu-id="c53e7-107">[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) also has constants that refer only to a Multiple Monitor system.</span></span> <span data-ttu-id="c53e7-108">SM \_ XVIRTUALSCREEN y SM \_ YVIRTUALSCREEN identifican la esquina superior izquierda de la pantalla virtual, SM \_ CXVIRTUALSCREEN y SM \_ CYVIRTUALSCREEN son las medidas verticales y horizontales de la pantalla virtual, SM \_ CMONITORS es el número de monitores conectados al escritorio y SM \_ SAMEDISPLAYFORMAT indica si todos los monitores del escritorio tienen el mismo formato de color.</span><span class="sxs-lookup"><span data-stu-id="c53e7-108">SM\_XVIRTUALSCREEN and SM\_YVIRTUALSCREEN identify the upper-left corner of the virtual screen, SM\_CXVIRTUALSCREEN and SM\_CYVIRTUALSCREEN are the vertical and horizontal measurements of the virtual screen, SM\_CMONITORS is the number of monitors attached to the desktop, and SM\_SAMEDISPLAYFORMAT indicates whether all the monitors on the desktop have the same color format.</span></span>

<span data-ttu-id="c53e7-109">Para obtener información acerca de un solo monitor de pantalla o todos los monitores de pantalla de un escritorio, use EnumDisplayMonitors.</span><span class="sxs-lookup"><span data-stu-id="c53e7-109">To get information about a single display monitor or all of the display monitors in a desktop, use EnumDisplayMonitors.</span></span> <span data-ttu-id="c53e7-110">El rectángulo de la ventana del escritorio devuelto por [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) o [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) siempre es igual al rectángulo del monitor principal, por compatibilidad con las aplicaciones existentes.</span><span class="sxs-lookup"><span data-stu-id="c53e7-110">The rectangle of the desktop window returned by [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) or [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) is always equal to the rectangle of the primary monitor, for compatibility with existing applications.</span></span> <span data-ttu-id="c53e7-111">Por lo tanto, el resultado de</span><span class="sxs-lookup"><span data-stu-id="c53e7-111">Thus, the result of</span></span>


```C++
GetWindowRect(GetDesktopWindow(), &rc);
```



<span data-ttu-id="c53e7-112">será:</span><span class="sxs-lookup"><span data-stu-id="c53e7-112">will be:</span></span>


```C++
rc.left = 0; 
rc.top = 0; 
rc.right = GetSystemMetrics (SM_CXSCREEN); 
rc.bottom = GetSystemMetrics (SM_CYSCREEN);
```



<span data-ttu-id="c53e7-113">Para cambiar el área de trabajo de un monitor, llame a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ SETWORKAREA y *pvParam* que señalen a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que esté en el monitor deseado.</span><span class="sxs-lookup"><span data-stu-id="c53e7-113">To change the work area of a monitor, call [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) with SPI\_SETWORKAREA and *pvParam* pointing to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that is on the desired monitor.</span></span> <span data-ttu-id="c53e7-114">Si *pvParam* es **null**, se modifica el área de trabajo del monitor principal.</span><span class="sxs-lookup"><span data-stu-id="c53e7-114">If *pvParam* is **NULL**, the work area of the primary monitor is modified.</span></span> <span data-ttu-id="c53e7-115">El uso \_ de SPI GETWORKAREA siempre devuelve el área de trabajo del monitor principal.</span><span class="sxs-lookup"><span data-stu-id="c53e7-115">Using SPI\_GETWORKAREA always returns the work area of the primary monitor.</span></span> <span data-ttu-id="c53e7-116">Para obtener el área de trabajo de un monitor que no sea el monitor principal, llame a [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span><span class="sxs-lookup"><span data-stu-id="c53e7-116">To get the work area of a monitor other than the primary monitor, call [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span></span>

 

 
