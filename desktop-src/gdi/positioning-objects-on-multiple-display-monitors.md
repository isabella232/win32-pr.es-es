---
description: Una ventana o un menú que se encuentra en más de un monitor provoca una interrupción visual para un visor. Para minimizar este problema, el sistema muestra menús y ventanas nuevas y maximizadas en un monitor. En la tabla siguiente se muestra cómo se elige el monitor.
ms.assetid: 9316c8dd-c9b7-49e2-a987-5949a87b0cfc
title: Colocar objetos en varios monitores de pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb6581fbed64b6a8ac83e29410e9758c6dea7b2d145958c57fa187abf34985c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119602735"
---
# <a name="positioning-objects-on-multiple-display-monitors"></a>Colocar objetos en varios monitores de pantalla

Una ventana o un menú que se encuentra en más de un monitor provoca una interrupción visual para un visor. Para minimizar este problema, el sistema muestra menús y ventanas nuevas y maximizadas en un monitor. En la tabla siguiente se muestra cómo se elige el monitor.



| Object         | Location                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| periodo         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)(por ejemplo) muestra una ventana en el monitor que contiene la parte más grande de la ventana. Maximiza el monitor que contiene la parte más grande de la ventana antes de que se minimizara.<br/> La combinación de teclas ALT-TAB muestra una ventana en el monitor que tiene la ventana activa actualmente.<br/>                                                                                                                                          |
| ventana de propiedad   | en el mismo monitor que su propietario.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Submenú        | Aparece en el monitor que contiene la parte más grande del elemento de menú correspondiente.                                                                                                                                                                                                                                                                                                                                                                                                          |
| menú contextual   | Aparece en el monitor donde se produjo el clic con el botón derecho.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| lista desplegable | Aparece en el monitor que contiene el rectángulo del cuadro combinado.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| cuadro de diálogo     | Aparece en el monitor de la ventana que la posee. Si se define con el estilo DS \_ CENTERMOUSE, aparece en el monitor con el mouse.<br/> Si no tiene ningún propietario y la ventana activa y el cuadro de diálogo están en la misma aplicación, el cuadro de diálogo aparece en el monitor de la ventana activa actualmente.<br/> Si el cuadro de diálogo no tiene propietario y la ventana activa no está en la misma aplicación que el cuadro de diálogo, el cuadro de diálogo aparece en el monitor principal.<br/> |
| cuadro de mensaje    | Aparece en el monitor de la ventana que la posee.                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Si una ventana se aleja de dos monitores y se vuelve a colocar uno de ellos, el sistema coloca la ventana en el monitor que contiene la parte más grande de la ventana original.

Normalmente, una aplicación también necesitará colocar objetos. Por ejemplo, es posible que sea necesario crear una ventana en el mismo monitor que otra ventana.

**Para colocar un objeto en un sistema de varios monitores**

1.  Determine el monitor adecuado.
2.  Obtenga las coordenadas al monitor.
3.  Coloque el objeto utilizando las coordenadas.

Normalmente, colocará un objeto en el monitor principal o en un monitor que ya tenga un objeto en él. Para identificar el monitor de un punto, rectángulo o ventana determinados, use [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint), [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)y [**MonitorFromWindow.**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow)

Para obtener las coordenadas del monitor, use [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa), que proporciona el área de trabajo y todo el rectángulo del monitor. Tenga en cuenta que SM CXSCREEN y SM CYSCREEN siempre hacen referencia al monitor principal, no necesariamente al \_ monitor que muestra la \_ aplicación. Además, evite SM xxVIRTUALSCREEN porque esto centra la ventana en la pantalla \_ virtual, no en un monitor.

Para centrar los cuadros de diálogo en el área de trabajo de una ventana, use el estilo DS \_ CENTER. Para centrar el cuadro de diálogo en una ventana de aplicación, use [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect). Windows automáticamente los menús y cuadros de diálogo a un monitor. Sin embargo, puede haber un problema con los menús personalizados, los cuadros desplegables personalizados, las paletas de herramientas personalizadas y la posición de la aplicación guardada.

Para obtener un ejemplo de cómo colocar objetos correctamente, vea [Positioning Objects on a Multiple Display Setup](positioning-objects-on-a-multiple-display-setup.md).

El uso de SM CXSCREEN y SM CYSCREEN para determinar la ubicación de una barra de herramientas de escritorio de aplicaciones (también denominada barra de aplicaciones) restringe la barra de aplicaciones \_ \_ al monitor principal.  Para permitir que una barra de aplicaciones esté en cualquier borde de cualquier monitor, use las métricas del sistema adecuadas para calcular los bordes de los monitores. Además, use las macros **GET \_ X \_ LPARAM** y **GET Y \_ \_ LPARAM** para extraer las coordenadas; de lo contrario, el signo de las coordenadas puede ser incorrecto. Estas macros se incluyen en Windowsx.h.

El tamaño de una ventana de pantalla completa debe cambiar a medida que se mueve entre monitores con diferentes resoluciones. Para ello, la aplicación debe comprobar en qué ventana se encuentra, mediante [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) o [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint) y, a continuación, usar [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) para obtener el tamaño del monitor. Como alternativa, podría usar **HMONITOR** de la función **DirectDrawEnumerateEx de** DirectX. A [**continuación, use SetWindowPos para**](/windows/win32/api/winuser/nf-winuser-setwindowpos) colocar y cambiar el tamaño de la ventana para cubrir el monitor.

Una ventana maximizada no cubre una barra de tareas que tenga la propiedad "Siempre en la parte superior". Sin embargo, una ventana de pantalla completa cubre la barra de tareas, por ejemplo, en Microsoft PowerPoint diapositivas y juegos.

Para guardar y restaurar posteriormente la posición de una ventana cuando se cierra una aplicación, use las funciones [**GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) [**y SetWindowPlacement.**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) Sin embargo, compruebe que la posición sigue siendo válida antes de usarlo porque el monitor se podría haber movido o quitado del sistema. La aplicación muestra la ventana en el monitor principal si **el HMONITOR** de una ventana no es válido.

El sistema intenta iniciar una aplicación en el monitor que contiene su acceso directo. Por lo tanto, una manera de colocar una aplicación es tener su acceso directo en un monitor deseado.

Si usa [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx,**](/windows/win32/api/shellapi/nf-shellapi-shellexecuteexa) proporcione un *hWnd* para que el sistema abra nuevas ventanas en el mismo monitor que la aplicación que realiza la llamada.

Tenga en cuenta que los valores de la [**estructura MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) se modifican ligeramente para un sistema con varios monitores.

 

 
