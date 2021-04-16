---
title: Escalado de pantalla de Active Accessibility y Windows Vista
description: Windows Vista permite a los usuarios cambiar la configuración de puntos por pulgada (PPP) para que la mayoría de los elementos de la interfaz de usuario de la pantalla parezcan más grandes.
ms.assetid: c781fefd-09f0-4340-b3d3-f4e57308f392
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db8e192dc01d4c7d75f19741cdfac7b3b08d22c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488055"
---
# <a name="active-accessibility-and-windows-vista-screen-scaling"></a>Escalado de pantalla de Active Accessibility y Windows Vista

Windows Vista permite a los usuarios cambiar la configuración de puntos por pulgada (PPP) para que la mayoría de los elementos de la interfaz de usuario de la pantalla parezcan más grandes. Aunque esta característica ha estado disponible durante mucho tiempo en Microsoft Windows, en versiones anteriores, el escalado debía ser implementado por aplicaciones. En Windows Vista, el Administrador de ventanas de escritorio realiza el escalado predeterminado para todas las aplicaciones que no controlan su propia escala. Las aplicaciones cliente de Microsoft Active Accessibility deben tener en cuenta esta característica.

## <a name="scaling-in-windows-vista"></a>Escalado en Windows Vista

La configuración de PPP predeterminada es 96, lo que significa que 96 píxeles ocupan el ancho o el alto de una pulgada teórica. La medida exacta de una "pulgada" depende del tamaño y de la resolución física del monitor. Por ejemplo, en un monitor de 12 pulgadas de ancho, con una resolución horizontal de 1280 píxeles, una línea horizontal de 96 píxeles se amplía aproximadamente 9/10 de una pulgada.

Cambiar la configuración de PPP no es lo mismo que cambiar la resolución de pantalla. Con el ajuste de escala de PPP, el número de píxeles físicos de la pantalla sigue siendo el mismo. Sin embargo, el escalado se aplica al tamaño y la ubicación de los elementos de la interfaz de usuario. Este ajuste de escala se puede realizar automáticamente mediante el Administrador de ventanas de escritorio (DWM) para el escritorio y para las aplicaciones que no solicitan explícitamente para cambiar de escala.

En efecto, cuando el usuario establece el factor de escala en 120 ppp, una pulgada vertical u horizontal en la pantalla aumenta en un 25 por ciento. Todas las dimensiones se escalan en consecuencia. El desplazamiento de una ventana desde los bordes superior e izquierdo de la pantalla aumenta en un 25 por ciento. El tamaño de la ventana aumenta en la misma proporción, junto con los desplazamientos y los tamaños de todos los elementos de la interfaz de usuario que contiene.

De forma predeterminada, el DWM no realiza el escalado para las aplicaciones no compatibles con PPP cuando el usuario establece el PPP en 120, pero lo realiza cuando el valor de PPP se establece en un valor personalizado de 144 o superior. Sin embargo, el usuario puede invalidar el comportamiento predeterminado.

El escalado de pantalla crea nuevos desafíos para las aplicaciones a las que les preocupa de cualquier manera las coordenadas de pantalla. La pantalla contiene ahora dos sistemas de coordenadas: físico y lógico. Las coordenadas físicas de un punto son el desplazamiento real en píxeles desde la parte superior izquierda del origen. Las coordenadas lógicas son los desplazamientos de la manera que serían si se escalaran los propios píxeles.

Supongamos que diseña un cuadro de diálogo con un botón en las coordenadas (100, 48). Cuando se muestra este cuadro de diálogo con el valor predeterminado de 96 PPP, el botón se encuentra en las coordenadas físicas de (100, 48). En 120 ppp, se encuentra en las coordenadas físicas de (125, 60). Sin embargo, las coordenadas lógicas son las mismas en cualquier configuración de PPP: (100, 48).

Las coordenadas lógicas son importantes porque hacen que el comportamiento del sistema operativo y las aplicaciones sean coherentes, independientemente de la configuración de PPP. Por ejemplo, **System. Windows. Forms. cursor. Position** devuelve normalmente las coordenadas lógicas. Si mueve el cursor sobre un elemento en un cuadro de diálogo, se devuelven las mismas coordenadas independientemente del valor de PPP. Si dibuja un control en (100, 100), se dibuja en esas coordenadas lógicas y ocupará la misma posición relativa en cualquier valor de PPP.

## <a name="scaling-in-active-accessibility-clients"></a>Escalado en clientes de Active Accessibility

Microsoft Active Accessibility no usa coordenadas lógicas. Los métodos y funciones siguientes devuelven coordenadas físicas o las toman como parámetros.

-   [**IAccessible:: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)

De forma predeterminada, una aplicación cliente de Microsoft Active Accessibility que se ejecute en un entorno que no sea de 96 PPP no podrá obtener resultados correctos de estas llamadas. Por ejemplo, dado que la posición del cursor se encuentra en coordenadas lógicas, el cliente no puede pasar simplemente estas coordenadas a [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) para obtener el elemento que se encuentra debajo del cursor.

Además, una aplicación que crea una ventana fuera de su área de cliente, como una aplicación de accesibilidad que resalta elementos de interfaz de usuario centrados, no creará la ventana en la ubicación de pantalla correcta, porque la ventana se colocará en las coordenadas lógicas, no las coordenadas físicas devueltas por [**IAccessible:: accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).

La solución se encuentra en dos partes:

-   Haga que la aplicación cliente sea "compatible con PPP". Para ello, llame a la función [**SetProcessDPIAware**](/windows/win32/api/winuser/nf-winuser-setprocessdpiaware) en el inicio. Esta función hace que todo el proceso sea compatible con PPP, lo que significa que todas las ventanas que pertenecen al proceso no se escalan.
-   Usar funciones que son compatibles con PPP. Por ejemplo, para obtener coordenadas de cursor, llame a la función [**GetPhysicalCursorPos**](/windows/win32/api/winuser/nf-winuser-getphysicalcursorpos) . No use [**GetCursorPos**](/windows/win32/api/winuser/nf-winuser-getcursorpos); su comportamiento en aplicaciones con reconocimiento de PPP es indefinido.

Si la aplicación realiza una comunicación directa entre procesos con aplicaciones que no reconocen los valores de PPP, puede que tenga que convertir entre las coordenadas lógicas y físicas mediante las funciones [**PhysicalToLogicalPoint**](/windows/win32/api/winuser/nf-winuser-physicaltologicalpoint) y [**LogicalToPhysicalPoint**](/windows/win32/api/winuser/nf-winuser-logicaltophysicalpoint) .

 

 