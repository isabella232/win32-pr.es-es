---
description: Normalmente, una aplicación se dibuja en una ventana en respuesta a un mensaje \_ WM PAINT.
ms.assetid: b2317ce9-e775-450e-91f5-00f735f256a3
title: El WM_PAINT mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 138913771621699abb27d4f5648e732b21a607ff5466ec4766726ab278d46fed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965185"
---
# <a name="the-wm_paint-message"></a>El mensaje PAINT de WM \_

Normalmente, una aplicación se dibuja en una ventana en respuesta a un [**mensaje \_ WM PAINT.**](wm-paint.md) El sistema envía este mensaje a un procedimiento de ventana cuando los cambios en la ventana han modificado el contenido del área de cliente. El sistema envía el mensaje solo si no hay ningún otro mensaje en la cola de mensajes de la aplicación.

Al recibir un [**mensaje \_ WM PAINT,**](wm-paint.md) una aplicación puede llamar a [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) para recuperar el contexto del dispositivo de presentación del área de cliente y usarlo en llamadas a funciones GDI para llevar a cabo las operaciones de dibujo necesarias para actualizar el área de cliente. Después de completar las operaciones de dibujo, la aplicación llama a [**la función EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) para liberar el contexto del dispositivo de presentación.

Antes [**de que BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) devuelva el contexto del dispositivo de presentación, el sistema prepara el contexto del dispositivo para la ventana especificada. En primer lugar, establece la región de recorte para que el contexto del dispositivo sea igual a la intersección de la parte de la ventana que necesita actualizarse y la parte visible para el usuario. Solo se dibujan las partes de la ventana que han cambiado. Los intentos de dibujar fuera de esta región se recortan y no aparecen en la pantalla.

El sistema también puede enviar [**mensajes \_ WM NCPAINT**](wm-ncpaint.md) y [**WM \_ ERASEB SPAMND**](../winmsg/wm-erasebkgnd.md) al procedimiento de ventana antes de [**que se devuelva BeginPaint.**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) Estos mensajes dirigen a la aplicación para dibujar el área no cliente y el fondo de la ventana. El *área no cliente* es la parte de una ventana que está fuera del área de cliente. El área incluye características como la barra de título, el menú de la ventana (también conocido como menú **Sistema)** y las barras de desplazamiento. La mayoría de las aplicaciones se basan en la función de ventana [**predeterminada, DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), para dibujar esta área y, por tanto, pasar el **mensaje WM \_ NCPAINT** a esta función. El *fondo de la* ventana es el color o el patrón con el que se rellena una ventana antes de que comiencen otras operaciones de dibujo. El fondo cubre las imágenes que se han hecho anteriormente en la ventana o en la pantalla debajo de la ventana. Si una ventana pertenece a una clase de ventana que tiene un pincel de fondo de clase, la función **DefWindowProc** dibuja automáticamente el fondo de la ventana.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) rellena una [**estructura PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) con información como las dimensiones de la parte de la ventana que se va a actualizar y una marca que indica si se ha dibujado el fondo de la ventana. La aplicación puede usar esta información para optimizar el dibujo. Por ejemplo, puede usar las dimensiones de la región de actualización, especificadas por el **miembro rcPaint,** para limitar el dibujo solo a las partes de la ventana que necesitan actualizarse. Si una aplicación tiene una salida muy sencilla, puede omitir la región de actualización y dibujar en toda la ventana, dependiendo del sistema para descartar (recortar) cualquier salida innecesario. Dado que el dibujo de clips del sistema que se extiende fuera de la región de recorte, solo está visible el dibujo que se encuentra en la región de actualización.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) establece la región de actualización de una ventana en **NULL.** Esto borra la región, lo que impide que genere mensajes [**WM \_ PAINT posteriores.**](wm-paint.md) Si una aplicación procesa un mensaje **WM \_ PAINT** pero no llama a **BeginPaint** o borra la región de actualización, la aplicación seguirá recibiendo mensajes **WM \_ PAINT** mientras la región no esté vacía. En todos los casos, una aplicación debe borrar la región de actualización antes de volver del **mensaje \_ WM PAINT.**

Cuando la aplicación termine de dibujar, debe llamar a [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint). Para la mayoría de las ventanas, **EndPaint** libera el contexto del dispositivo para mostrar, lo que lo hace disponible para otras ventanas. **EndPaint** también muestra el caret, si beginPaint lo ha ocultado [**previamente.**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) **BeginPaint** oculta el centro de referencia para evitar que las operaciones de dibujo la dañan.

-   [Región de actualización](the-update-region.md)
-   [Invalidar y validar la región de actualización](invalidating-and-validating-the-update-region.md)
-   [Recuperar la región de actualización](retrieving-the-update-region.md)
-   [Exclusión de la región de actualización](excluding-the-update-region.md)
-   [Dibujo sincrónico y asincrónico](synchronous-and-asynchronous-drawing.md)

 

 
