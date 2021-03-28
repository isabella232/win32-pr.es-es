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
# <a name="multiple-monitor-system-metrics"></a>Varias métricas del sistema de supervisión

La función [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) devuelve valores para el monitor principal, excepto SM \_ CXMAXTRACK y SM \_ CYMAXTRACK, que hacen referencia a todo el escritorio. Las siguientes métricas son las mismas para todos los controladores de dispositivo: SM \_ CXCURSOR, SM \_ CYCURSOR, SM \_ CXICON, SMCYICON. Las siguientes funcionalidades de visualización son las mismas para todos los monitores: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.

[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) también tiene constantes que hacen referencia solo a un sistema de varios monitores. SM \_ XVIRTUALSCREEN y SM \_ YVIRTUALSCREEN identifican la esquina superior izquierda de la pantalla virtual, SM \_ CXVIRTUALSCREEN y SM \_ CYVIRTUALSCREEN son las medidas verticales y horizontales de la pantalla virtual, SM \_ CMONITORS es el número de monitores conectados al escritorio y SM \_ SAMEDISPLAYFORMAT indica si todos los monitores del escritorio tienen el mismo formato de color.

Para obtener información acerca de un solo monitor de pantalla o todos los monitores de pantalla de un escritorio, use EnumDisplayMonitors. El rectángulo de la ventana del escritorio devuelto por [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) o [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) siempre es igual al rectángulo del monitor principal, por compatibilidad con las aplicaciones existentes. Por lo tanto, el resultado de


```C++
GetWindowRect(GetDesktopWindow(), &rc);
```



será:


```C++
rc.left = 0; 
rc.top = 0; 
rc.right = GetSystemMetrics (SM_CXSCREEN); 
rc.bottom = GetSystemMetrics (SM_CYSCREEN);
```



Para cambiar el área de trabajo de un monitor, llame a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ SETWORKAREA y *pvParam* que señalen a una estructura [**Rect**](/previous-versions//dd162897(v=vs.85)) que esté en el monitor deseado. Si *pvParam* es **null**, se modifica el área de trabajo del monitor principal. El uso \_ de SPI GETWORKAREA siempre devuelve el área de trabajo del monitor principal. Para obtener el área de trabajo de un monitor que no sea el monitor principal, llame a [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).

 

 
