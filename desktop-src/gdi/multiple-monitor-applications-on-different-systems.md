---
description: Para que la aplicación monitoraware múltiple funcione en sistemas con y sin compatibilidad con varios monitores, vincule la aplicación con Multimon.h.
ms.assetid: 8667305e-ca76-49cb-878e-07814431e6db
title: Varias aplicaciones de supervisión en sistemas diferentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4c597261063f49b6e6856576e3528698291348afb2b8478d854a824b92d2cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037723"
---
# <a name="multiple-monitor-applications-on-different-systems"></a>Varias aplicaciones de supervisión en sistemas diferentes

Para que la aplicación monitoraware múltiple funcione en sistemas con y sin compatibilidad con varios monitores, vincule la aplicación con Multimon.h. También debe definir COMPILE \_ MULTIMON \_ STUBS en exactamente un archivo C. Si el sistema no admite varios monitores, devuelve los valores predeterminados de [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) y las funciones de supervisión múltiples actúan como si solo hubiera una pantalla. En varios sistemas de supervisión, la aplicación funcionará con normalidad.

Dado que las coordenadas negativas pueden ocurrir fácilmente en un sistema multimonitor, debe recuperar las coordenadas empaquetadas en lParam mediante las macros **GET \_ X \_ LPARAM** y **GET Y \_ \_ LPARAM.**

No use coordenadas negativas o coordenadas mayores que SM \_ CXSCREEN y SM \_ CYSCREEN para ocultar una ventana. Windows que usan estos límites para ocultar pueden aparecer en otro monitor. Del mismo modo, no use estos límites para mantener visible una ventana, ya que esto puede hacer que una ventana se ajuste al monitor principal. Es mejor volver a examinar las aplicaciones existentes para estos problemas. Sin embargo, puede minimizar los problemas en las aplicaciones existentes ejecutando la aplicación en el monitor principal o manteniendo el monitor principal en la esquina superior izquierda de la pantalla virtual.

Tenga en cuenta que SM \_ CXMAXTRACK y SM CYMAXTRACK están definidos para el \_ escritorio, no solo para un monitor. Windows estos límites es posible que deba volver a definirse.

Es posible que una ventana primaria o relacionada no esté en el mismo monitor que una ventana secundaria. Para buscar el monitor de una ventana, las aplicaciones deben usar la [**función MonitorFromWindow.**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)

Para que se muestre un protector de pantalla en todos los monitores, vincule con la versión más reciente de Scrnsave.lib. De lo contrario, el protector de pantalla solo puede aparecer en el monitor principal y dejar los demás monitores intactos. Los protectores de pantalla vinculados con la versión más reciente de Scrnsave.lib funcionarán tanto en sistemas de supervisión únicos como en varios. Para tener un protector de pantalla diferente en cada monitor, use las varias funciones de supervisión para controlar cada monitor por separado.

Los dispositivos de entrada que entregan coordenadas al sistema en coordenadas absolutas, como tabletas, tienen su entrada de cursor restringida al monitor principal. Para cambiar la entrada de tableta entre monitores, consulte las instrucciones del OEM.

Para asignar la entrada del mouse que se envía en coordenadas absolutas a toda la pantalla virtual, use la estructura [**INPUT**](/windows/win32/api/winuser/ns-winuser-input) con MOUSEEVENTF ABSOLUTE y \_ MOUSEEVENTF \_ VIRTUALDESKTOP.

La [**función BitBlt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) funciona bien para varios sistemas de supervisión. Sin embargo, las [**funciones MaskBlt,**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt) [**PlgBlt,**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt) [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)y [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) producirán un error si los contextos de dispositivo de origen y destino son diferentes.

 

 
