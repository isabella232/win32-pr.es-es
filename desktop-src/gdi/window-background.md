---
description: El fondo de la ventana es el color o el patrón que se usa para rellenar el área de cliente antes de que se inicie el dibujo de una ventana.
ms.assetid: d0613f9b-e65b-4de2-887d-2b642d36b22d
title: Fondo de la ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32d567b0bdc38866cd9332ff8ed399bfb23f53c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908938"
---
# <a name="window-background"></a>Fondo de la ventana

El fondo de la ventana es el color o el patrón que se usa para rellenar el área de cliente antes de que se inicie el dibujo de una ventana. El fondo de la ventana cubre lo que estaba en la pantalla antes de que la ventana se moviera allí, borrando las imágenes existentes e impidiendo que la nueva salida de la aplicación se mezcle con información no relacionada.

El sistema pinta el fondo de una ventana o le da la oportunidad de hacerlo mediante el envío de un mensaje de [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) cuando la aplicación llama a [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint). Si una aplicación no procesa el mensaje pero lo pasa a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), el sistema borra el fondo rellenándolo con el patrón del pincel de fondo especificado por la clase de la ventana. Si el pincel no es válido o la clase no tiene un pincel de fondo, el sistema establece el miembro **fErase** de la estructura [**paintstruct (**](/windows/win32/api/winuser/ns-winuser-paintstruct) que se devuelve **BeginPaint** , pero no realiza ninguna otra acción. A continuación, la aplicación tiene una segunda oportunidad para dibujar el fondo de la ventana, si es necesario.

Si procesa [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md), la aplicación debe utilizar el parámetro *wParam* del mensaje para dibujar el fondo. Este parámetro contiene un identificador para mostrar el contexto de dispositivo para la ventana. Después de dibujar el fondo, la aplicación debe devolver un valor distinto de cero. Esto garantiza que [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) no establezca erróneamente el miembro **fErase** de la estructura [**paintstruct (**](/windows/win32/api/winuser/ns-winuser-paintstruct) en un valor distinto de cero (lo que indica que se debe borrar el fondo) cuando la aplicación procese el mensaje de [**\_ dibujo de WM**](wm-paint.md) subsiguiente.

Una aplicación puede definir un pincel de fondo de clase asignando un identificador de pincel o un valor de color del sistema al miembro **hbrBackground** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) al registrar la clase con la función [**RegisterClass**](/windows/win32/api/winuser/nf-winuser-registerclassa) . La función [**GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) o [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush) se puede usar para crear un controlador de pincel. Un valor de color del sistema puede ser uno de los definidos para la función [**SetSysColors**](/windows/win32/api/winuser/nf-winuser-setsyscolors) . (El valor debe aumentarse en uno antes de que se asigne al miembro).

Una aplicación puede procesar el mensaje de [**\_ ERASEBKGND de WM**](../winmsg/wm-erasebkgnd.md) aunque se haya definido un pincel de fondo de clase. Esto es típico en aplicaciones que permiten al usuario cambiar el color de fondo o el patrón de una ventana especificada sin afectar a otras ventanas de la clase. En tales casos, la aplicación no debe pasar el mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

No es necesario que una aplicación Alinee los pinceles, ya que el sistema dibuja el pincel mediante el origen de la ventana como punto de referencia. Dado esto, el usuario puede desplace la ventana sin que ello afecte a la alineación de los pinceles de patrón.

 

 
