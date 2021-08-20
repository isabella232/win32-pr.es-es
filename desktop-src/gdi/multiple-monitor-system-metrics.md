---
description: La función GetSystemMetrics devuelve valores para el monitor principal, excepto SM \_ CXMAXTRACK y SM CYMAXTRACK, que hacen referencia a \_ todo el escritorio.
ms.assetid: d0105363-1895-4e10-8a33-648a6fc4c20a
title: Varias métricas del sistema de supervisión
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3143562116561bb220bc6f0b5ecfa4ad8f5103c3e4532cab639c4c2b37f59467
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037713"
---
# <a name="multiple-monitor-system-metrics"></a>Varias métricas del sistema de supervisión

La [**función GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) devuelve valores para el monitor principal, excepto SM \_ CXMAXTRACK y SM CYMAXTRACK, que hacen referencia a \_ todo el escritorio. Las métricas siguientes son las mismas para todos los controladores de dispositivo: SM \_ CXCURSOR, SM \_ CYCURSOR, SM \_ CXICON, SMCYICON. Las siguientes funcionalidades de visualización son las mismas para todos los monitores: LOGPIXELSX, LOGPIXELSY, DESTOPHORZRES, DESKTOPVERTRES.

[**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) también tiene constantes que hacen referencia solo a un sistema de varios monitores. SMMONITORALSCREEN y SM YVIRTUALSCREEN identifican la esquina superior izquierda de la pantalla \_ \_ virtual, SM \_ CXVIRTUALSCREEN y SM CYVIRTUALSCREEN son las medidas vertical y horizontal de la pantalla \_ virtual, SM CMONITORS es el número de monitores conectados al escritorio y \_ SM \_ SAMEDISPLAYFORMAT indica si todos los monitores del escritorio tienen el mismo formato de color.

Para obtener información sobre un único monitor de pantalla o todos los monitores de pantalla de un escritorio, use EnumDisplayMonitors. El rectángulo de la ventana de escritorio devuelto por [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect) o [**GetClientRect**](/windows/win32/api/winuser/nf-winuser-getclientrect) siempre es igual al rectángulo del monitor principal, por compatibilidad con las aplicaciones existentes. Por lo tanto, el resultado de


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



Para cambiar el área de trabajo de un monitor, llame a [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) con SPI \_ SETWORKAREA y *pvParam* que apunte a una [**estructura RECT**](/previous-versions//dd162897(v=vs.85)) que se encuentra en el monitor deseado. Si *pvParam* es **NULL,** se modifica el área de trabajo del monitor principal. El uso de SPI \_ GETWORKAREA siempre devuelve el área de trabajo del monitor principal. Para obtener el área de trabajo de un monitor que no sea el principal, llame a [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).

 

 
