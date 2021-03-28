---
description: Una ventana o un menú que se encuentra en más de un monitor produce una interrupción visual de un visor. Para minimizar este problema, el sistema muestra menús y ventanas nuevas y maximizadas en un monitor. En la tabla siguiente se muestra cómo se elige el monitor.
ms.assetid: 9316c8dd-c9b7-49e2-a987-5949a87b0cfc
title: Colocar objetos en varios monitores de pantalla
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77149291737482fa0f3e7fe19ee4f350ee6521d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984855"
---
# <a name="positioning-objects-on-multiple-display-monitors"></a>Colocar objetos en varios monitores de pantalla

Una ventana o un menú que se encuentra en más de un monitor produce una interrupción visual de un visor. Para minimizar este problema, el sistema muestra menús y ventanas nuevas y maximizadas en un monitor. En la tabla siguiente se muestra cómo se elige el monitor.



| Object         | Ubicación                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| periodo         | [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)(ex) muestra una ventana en el monitor que contiene la parte más grande de la ventana. Maximiza el monitor que contiene la parte más grande de la ventana antes de que se minimice.<br/> La combinación de teclas ALT-TAB muestra una ventana en el monitor que tiene la ventana activa actualmente.<br/>                                                                                                                                          |
| ventana propiedad   | en el mismo monitor que su propietario.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| submenú        | Aparece en el monitor que contiene la parte más grande del elemento de menú correspondiente.                                                                                                                                                                                                                                                                                                                                                                                                          |
| menú contextual   | Aparece en el monitor en el que se hizo clic con el botón derecho.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| lista desplegable | Aparece en el monitor que contiene el rectángulo del cuadro combinado.                                                                                                                                                                                                                                                                                                                                                                                                                           |
| cuadro de diálogo     | Aparece en el monitor de la ventana que lo posee. Si se define con \_ el estilo CENTERMOUSE de DS, aparecerá en el monitor con el mouse.<br/> Si no tiene ningún propietario y la ventana activa y el cuadro de diálogo se encuentran en la misma aplicación, el cuadro de diálogo aparece en el monitor de la ventana activa actualmente.<br/> Si el cuadro de diálogo no tiene ningún propietario y la ventana activa no está en la misma aplicación que el cuadro de diálogo, el cuadro de diálogo aparece en el monitor principal.<br/> |
| cuadro de mensaje    | Aparece en el monitor de la ventana que lo posee.                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

Si una ventana ocupa dos monitores y uno de los monitores se cambia de posición, el sistema coloca la ventana en el monitor que contiene la parte más grande de la ventana original.

Normalmente, una aplicación también necesitará colocar objetos. Por ejemplo, puede que sea necesario crear una ventana en el mismo monitor que otra ventana.

**Para colocar un objeto en un sistema de varios monitores**

1.  Determine el monitor adecuado.
2.  Obtiene las coordenadas del monitor.
3.  Coloque el objeto con las coordenadas.

Normalmente, se coloca un objeto en el monitor principal o en un monitor que ya tiene un objeto en él. Para identificar el monitor de un punto, un rectángulo o una ventana determinados, use [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint), [**MonitorFromRect**](/windows/desktop/api/Winuser/nf-winuser-monitorfromrect)y [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow).

Para obtener las coordenadas del monitor, use [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa), que proporciona tanto el área de trabajo como el rectángulo del monitor completo. Tenga en cuenta que SM \_ CXSCREEN y SM \_ CYSCREEN siempre hacen referencia al monitor principal, no necesariamente al monitor que muestra la aplicación. Además, evite el SM \_ xxVIRTUALSCREEN porque se centra la ventana en la pantalla virtual, no en un monitor.

Para centrar los cuadros de diálogo en el área de trabajo de una ventana, use el estilo de centro de DS \_ . Para centrar el cuadro de diálogo en una ventana de la aplicación, use [**GetWindowRect**](/windows/win32/api/winuser/nf-winuser-getwindowrect). Windows restringe automáticamente los menús y los cuadros de diálogo a un monitor. Sin embargo, puede haber un problema en los menús personalizados, en los cuadros desplegables personalizados, en las paletas de herramientas personalizadas y en la posición de aplicación guardada.

Para obtener un ejemplo de cómo colocar objetos correctamente, vea [colocar objetos en una configuración de pantalla múltiple](positioning-objects-on-a-multiple-display-setup.md).

El uso \_ de SM CXSCREEN y SM \_ CYSCREEN para determinar la ubicación de una barra de herramientas del escritorio de la aplicación (también denominada *Appbar*) restringe el Appbar al monitor principal. Para permitir que una Appbar esté en cualquier borde de cualquier monitor, use las métricas del sistema adecuadas para calcular los bordes de los monitores. Además, use las macros **Get \_ X \_ lParam** y **Get \_ y \_ lParam** para extraer las coordenadas; de lo contrario, el signo de las coordenadas puede ser incorrecto. Estas macros se incluyen en windowsx. h.

El tamaño de una ventana de pantalla completa debe cambiar a medida que se mueve entre monitores con distintas resoluciones. Para ello, la aplicación debe comprobar la ventana en la que se encuentra, el uso de [**MonitorFromWindow**](/windows/desktop/api/Winuser/nf-winuser-monitorfromwindow) o [**MonitorFromPoint**](/windows/desktop/api/Winuser/nf-winuser-monitorfrompoint) y, a continuación, usar [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa) para obtener el tamaño del monitor. Como alternativa, puede usar **HMONITOR** desde la función **DirectDrawEnumerateEx** de DirectX. A continuación, use [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) para colocar y ajustar el tamaño de la ventana para cubrir el monitor.

Una ventana maximizada no cubre una barra de tareas que tenga la propiedad "AlwaysOn Top". Sin embargo, una ventana de pantalla completa cubre la barra de tareas, por ejemplo, en presentaciones y juegos de diapositivas de Microsoft PowerPoint.

Para guardar y restaurar posteriormente la posición de una ventana cuando se cierra una aplicación, use las funciones [**GetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-getwindowplacement) y [**SetWindowPlacement**](/windows/win32/api/winuser/nf-winuser-setwindowplacement) . Sin embargo, compruebe que la posición sigue siendo válida antes de usarla, ya que el monitor podría haberse cambiado o quitado del sistema. La aplicación muestra la ventana en el monitor principal si el **HMONITOR** de una ventana no es válido.

El sistema intenta iniciar una aplicación en el monitor que contiene el acceso directo. Por lo tanto, una manera de colocar una aplicación es tener su acceso directo en el monitor deseado.

Si utiliza [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) o [**ShellExecuteEx**](/windows/win32/api/shellapi/nf-shellapi-shellexecuteexa) , suministre un *hWnd* para que el sistema abra las ventanas nuevas en el mismo monitor que la aplicación que realiza la llamada.

Tenga en cuenta que los valores de la estructura [**minmaxinfo (**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) se modifican ligeramente para un sistema con varios monitores.

 

 
