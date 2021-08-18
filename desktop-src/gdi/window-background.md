---
description: El fondo de la ventana es el color o el patrón que se usa para rellenar el área de cliente antes de que una ventana comience a dibujarse.
ms.assetid: d0613f9b-e65b-4de2-887d-2b642d36b22d
title: Fondo de la ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 819f3bf333728909bdd0e374d41b7665f0517bcc17666b88c58f610e0127d942
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848945"
---
# <a name="window-background"></a>Fondo de la ventana

El fondo de la ventana es el color o el patrón que se usa para rellenar el área de cliente antes de que una ventana comience a dibujarse. El fondo de la ventana cubre todo lo que estaba en la pantalla antes de que la ventana se moviera allí, borrando las imágenes existentes e impidiendo que la nueva salida de la aplicación se mezclase con información no relacionada.

El sistema pinta el fondo de una ventana o ofrece a la ventana la oportunidad de hacerlo enviándole un mensaje [**\_ WM ERASEBNDND**](../winmsg/wm-erasebkgnd.md) cuando la aplicación llama a [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint). Si una aplicación no procesa el mensaje, pero lo pasa a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), el sistema borra el fondo rellenando con el patrón en el pincel de fondo especificado por la clase de la ventana. Si el pincel no es válido o la clase no tiene pincel de fondo, el sistema establece el miembro **fErase** en la estructura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) que **beginPaint** devuelve, pero no realiza ninguna otra acción. A continuación, la aplicación tiene una segunda oportunidad de dibujar el fondo de la ventana, si es necesario.

Si procesa [**WM \_ ERASEB DOMAINND,**](../winmsg/wm-erasebkgnd.md)la aplicación debe usar el parámetro *wParam* del mensaje para dibujar el fondo. Este parámetro contiene un identificador para el contexto del dispositivo de presentación de la ventana. Después de dibujar el fondo, la aplicación debe devolver un valor distinto de cero. Esto garantiza que [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) no establece erróneamente el miembro **fErase** de la estructura [**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) en un valor distinto de cero (lo que indica que se debe borrar el fondo) cuando la aplicación procesa el mensaje [**WM \_ PAINT**](wm-paint.md) posterior.

Una aplicación puede definir un pincel de fondo de clase asignando un identificador de pincel o un valor de color del sistema al **miembro hbrBackground** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) al registrar la clase con la [**función RegisterClass.**](/windows/win32/api/winuser/nf-winuser-registerclassa) La [**función GetStockObject**](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) [**o CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush) se puede usar para crear un identificador de pincel. Un valor de color del sistema puede ser uno de los definidos para la [**función SetSysColors.**](/windows/win32/api/winuser/nf-winuser-setsyscolors) (El valor debe aumentarse en uno antes de que se asigne al miembro).

Una aplicación puede procesar el [**mensaje \_ ERASEB DOMAINND de WM**](../winmsg/wm-erasebkgnd.md) aunque se defina un pincel de fondo de clase. Esto es habitual en las aplicaciones que permiten al usuario cambiar el color de fondo o el patrón de la ventana para una ventana especificada sin afectar a otras ventanas de la clase . En tales casos, la aplicación no debe pasar el mensaje [**a DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

No es necesario que una aplicación alinee los pinceles, ya que el sistema dibuja el pincel utilizando el origen de la ventana como punto de referencia. Dado esto, el usuario puede mover la ventana sin afectar a la alineación de los pinceles de patrón.

 

 
