---
description: Para que la aplicación de varios monitoraware funcione en sistemas con y sin compatibilidad con monitores múltiples, vincule la aplicación con MultiMon. h.
ms.assetid: 8667305e-ca76-49cb-878e-07814431e6db
title: Varias aplicaciones de supervisión en diferentes sistemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5d470861136ac9362d986b8647c86abee7021b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984923"
---
# <a name="multiple-monitor-applications-on-different-systems"></a>Varias aplicaciones de supervisión en diferentes sistemas

Para que la aplicación de varios monitoraware funcione en sistemas con y sin compatibilidad con monitores múltiples, vincule la aplicación con MultiMon. h. También debe definir \_ \_ stubs de MULTIMON de compilación en exactamente un archivo de C. Si el sistema no admite varios monitores, devuelve los valores predeterminados de [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) y las funciones de varios monitores actúan como si solo hubiera una pantalla. En varios sistemas de supervisión, la aplicación funcionará con normalidad.

Dado que las coordenadas negativas pueden producirse fácilmente en un sistema de un solo monitor, debe recuperar las coordenadas empaquetadas en lParam mediante las macros **Get \_ X \_ lParam** y **Get \_ y \_ lParam** .

No use coordenadas negativas ni coordenadas mayores que SM \_ CXSCREEN y SM \_ CYSCREEN para ocultar una ventana. Las ventanas que usan estos límites para ocultar pueden aparecer en otro monitor. Del mismo modo, no use estos límites para mantener visible una ventana, ya que esto puede hacer que una ventana se ajuste al monitor principal. Es mejor volver a examinar las aplicaciones existentes para estos problemas. Sin embargo, puede minimizar los problemas de las aplicaciones existentes ejecutando la aplicación en el monitor principal o manteniendo el monitor principal en la esquina superior izquierda de la pantalla virtual.

Tenga en cuenta que SM \_ CXMAXTRACK y SM \_ CYMAXTRACK se definen para el escritorio, no solo un monitor. Es posible que sea necesario redefinir Windows con estos límites.

Es posible que una ventana primaria o relacionada no esté en el mismo monitor que una ventana secundaria. Para buscar el monitor de una ventana, las aplicaciones deben usar la función [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) .

Para que se muestre un protector de pantalla en todos los monitores, vincule con la versión más reciente de Scrnsave. lib. De lo contrario, el protector de pantalla solo puede aparecer en el monitor principal y dejar los otros monitores intactos. Los protectores de pantalla vinculados con la versión más reciente de Scrnsave. lib funcionarán en sistemas de varios monitores. Para tener un protector de pantalla diferente en cada monitor, utilice las funciones de varios monitores para controlar cada monitor por separado.

Los dispositivos de entrada que proporcionan coordenadas al sistema en coordenadas absolutas, como tabletas, tienen la entrada de cursor restringida al monitor principal. Para cambiar la entrada de Tablet PC entre monitores, consulte las instrucciones del OEM.

Para asignar la entrada del mouse que se envía en coordenadas absolutas a toda la pantalla virtual, use la estructura de [**entrada**](/windows/win32/api/winuser/ns-winuser-input) con MOUSEEVENTF \_ Absolute y MOUSEEVENTF \_ VIRTUALDESKTOP.

La función [**bitblt**](/windows/desktop/api/Wingdi/nf-wingdi-bitblt) funciona bien en varios sistemas de supervisión. Sin embargo, se producirá un error en las funciones [**MaskBlt**](/windows/desktop/api/Wingdi/nf-wingdi-maskblt), [**PlgBlt**](/windows/desktop/api/Wingdi/nf-wingdi-plgblt), [**StretchBlt**](/windows/desktop/api/Wingdi/nf-wingdi-stretchblt)y [**TransparentBlt**](/windows/desktop/api/WinGdi/nf-wingdi-transparentblt) si los contextos de dispositivo de origen y de destino son diferentes.

 

 
