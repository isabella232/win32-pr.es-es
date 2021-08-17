---
title: Active Accessibility y Windows de pantalla de Vista
description: Windows Vista permite a los usuarios cambiar la configuración de puntos por pulgada (ppp) para que la mayoría de los elementos de la interfaz de usuario de la pantalla parezcan más grandes.
ms.assetid: c781fefd-09f0-4340-b3d3-f4e57308f392
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acf9c1ff6755507541c08b34e183dd751e0941fc646a1f691e4488884e572c79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327065"
---
# <a name="active-accessibility-and-windows-vista-screen-scaling"></a>Active Accessibility y Windows de pantalla de Vista

Windows Vista permite a los usuarios cambiar la configuración de puntos por pulgada (ppp) para que la mayoría de los elementos de la interfaz de usuario de la pantalla parezcan más grandes. Aunque esta característica lleva mucho tiempo disponible en Microsoft Windows, en versiones anteriores, las aplicaciones tenían que implementar el escalado. En Windows Vista, el Administrador de ventanas de escritorio realiza el escalado predeterminado para todas las aplicaciones que no controlan su propio escalado. Microsoft Active Accessibility aplicaciones cliente deben tener en cuenta esta característica.

## <a name="scaling-in-windows-vista"></a>Escalado en Windows Vista

El valor de ppp predeterminado es 96, lo que significa que 96 píxeles ocupan un ancho o alto de una pulgada notional. La medida exacta de una "pulgada" depende del tamaño y de la resolución física del monitor. Por ejemplo, en un monitor de 12 pulgadas de ancho, con una resolución horizontal de 1280 píxeles, una línea horizontal de 96 píxeles se amplía aproximadamente 9/10 de una pulgada.

Cambiar la configuración de ppp no es lo mismo que cambiar la resolución de pantalla. Con el escalado de ppp, el número de píxeles físicos en la pantalla sigue siendo el mismo. Sin embargo, el escalado se aplica al tamaño y la ubicación de los elementos de la interfaz de usuario. Este ajuste de escala se puede realizar automáticamente mediante el Administrador de ventanas de escritorio (DWM) para el escritorio y para las aplicaciones que no solicitan explícitamente para cambiar de escala.

De hecho, cuando el usuario establece el factor de escala en 120 ppp, una pulgada vertical u horizontal en la pantalla se hace más grande en un 25 %. Todas las dimensiones se escalan en consecuencia. El desplazamiento de una ventana de los bordes superior e izquierdo de la pantalla aumenta un 25 %. El tamaño de la ventana aumenta en la misma proporción, junto con los desplazamientos y tamaños de todos los elementos de la interfaz de usuario que contiene.

De forma predeterminada, dwm no realiza el escalado para aplicaciones que no tienen en cuenta ppp cuando el usuario establece el valor de ppp en 120, pero lo hace cuando el valor de ppp se establece en un valor personalizado de 144 o superior. Sin embargo, el usuario puede invalidar el comportamiento predeterminado.

El escalado de pantalla crea nuevos desafíos para las aplicaciones a las que les preocupa de cualquier manera las coordenadas de pantalla. La pantalla contiene ahora dos sistemas de coordenadas: físico y lógico. Las coordenadas físicas de un punto son el desplazamiento real en píxeles desde la parte superior izquierda del origen. Las coordenadas lógicas son los desplazamientos de la manera que serían si se escalaran los propios píxeles.

Supongamos que diseña un cuadro de diálogo con un botón en las coordenadas (100, 48). Cuando este cuadro de diálogo se muestra con el valor predeterminado de 96 ppp, el botón se encuentra en coordenadas físicas de (100, 48). A 120 ppp, se encuentra en coordenadas físicas de (125, 60). Pero las coordenadas lógicas son las mismas en cualquier configuración de ppp: (100, 48).

Las coordenadas lógicas son importantes, ya que hacen que el comportamiento del sistema operativo y las aplicaciones sea coherente independientemente de la configuración de ppp. Por ejemplo, **System.Windows. Forms.Cursor.Position** normalmente devuelve las coordenadas lógicas. Si mueve el cursor sobre un elemento de un cuadro de diálogo, se devuelven las mismas coordenadas independientemente de la configuración de ppp. Si dibuja un control en (100, 100), se dibuja en esas coordenadas lógicas y ocupará la misma posición relativa en cualquier configuración de ppp.

## <a name="scaling-in-active-accessibility-clients"></a>Escalado en Active Accessibility clientes

Microsoft Active Accessibility no usa coordenadas lógicas. Los siguientes métodos y funciones devuelven coordenadas físicas o las toman como parámetros.

-   [**IAccessible::accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint)

De forma predeterminada, Microsoft Active Accessibility aplicación cliente que se ejecuta en un entorno que no sea de 96 ppp no podrá obtener los resultados correctos de estas llamadas. Por ejemplo, como la posición del cursor está en coordenadas lógicas, el cliente no puede pasar simplemente estas coordenadas a [**AccessibleObjectFromPoint**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfrompoint) para obtener el elemento que está debajo del cursor.

Además, una aplicación que crea una ventana fuera de su área cliente, como una aplicación de accesibilidad que resalta los elementos de la interfaz de usuario centrados, no creará la ventana en la ubicación de pantalla correcta, ya que la ventana se colocará en las coordenadas lógicas, no en las coordenadas físicas devueltas por [**IAccessible::accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation).

La solución se encuentra en dos partes:

-   Haga que la aplicación cliente tenga en cuenta ppp. Para ello, llame a la [**función SetProcessDPIAware en**](/windows/win32/api/winuser/nf-winuser-setprocessdpiaware) el inicio. Esta función hace que todo el proceso tenga en cuenta los valores de ppp, lo que significa que todas las ventanas que pertenecen al proceso no se escalan.
-   Use funciones que tienen en cuenta ppp. Por ejemplo, para obtener coordenadas de cursor, llame a la [**función GetPhysicalCursorPos.**](/windows/win32/api/winuser/nf-winuser-getphysicalcursorpos) No use [**GetCursorPos**](/windows/win32/api/winuser/nf-winuser-getcursorpos); su comportamiento en aplicaciones con reconocimiento de ppp no está definido.

Si la aplicación realiza una comunicación directa entre procesos con aplicaciones que no tienen en cuenta ppp, es posible que haya convertido entre coordenadas lógicas y físicas mediante las funciones [**PhysicalToLogicalPoint**](/windows/win32/api/winuser/nf-winuser-physicaltologicalpoint) y [**LogicalToPhysicalPoint.**](/windows/win32/api/winuser/nf-winuser-logicaltophysicalpoint)

 

 