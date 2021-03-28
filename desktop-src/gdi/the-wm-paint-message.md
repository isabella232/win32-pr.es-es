---
description: Normalmente, una aplicación se dibuja en una ventana en respuesta a un \_ mensaje de dibujo de WM.
ms.assetid: b2317ce9-e775-450e-91f5-00f735f256a3
title: El mensaje WM_PAINT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69f7dab736972d8b7226890144efd8763de856a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997928"
---
# <a name="the-wm_paint-message"></a>Mensaje de \_ dibujo de WM

Normalmente, una aplicación se dibuja en una ventana en respuesta a un mensaje de [**\_ dibujo de WM**](wm-paint.md) . El sistema envía este mensaje a un procedimiento de ventana cuando los cambios en la ventana han alterado el contenido del área cliente. El sistema solo envía el mensaje si no hay ningún otro mensaje en la cola de mensajes de la aplicación.

Al recibir un mensaje de [**\_ dibujo de WM**](wm-paint.md) , una aplicación puede llamar a [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) para recuperar el contexto de dispositivo de pantalla para el área cliente y usarlo en llamadas a funciones GDI para realizar cualquier operación de dibujo necesaria para actualizar el área cliente. Después de completar las operaciones de dibujo, la aplicación llama a la función [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) para liberar el contexto de dispositivo de pantalla.

Antes de que [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) devuelva el contexto de dispositivo de pantalla, el sistema prepara el contexto de dispositivo para la ventana especificada. Primero establece la región de recorte para que el contexto del dispositivo sea igual a la intersección de la parte de la ventana que necesita actualizar y la parte que es visible para el usuario. Solo se vuelven a dibujar las partes de la ventana que han cambiado. Los intentos de dibujar fuera de esta región se recortan y no aparecen en la pantalla.

El sistema también puede enviar mensajes de [**WM \_ NCPAINT**](wm-ncpaint.md) y [**WM \_ ERASEBKGND**](../winmsg/wm-erasebkgnd.md) al procedimiento de ventana antes de que se devuelva [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) . Estos mensajes dirigen a la aplicación para que dibuje el área no cliente y el fondo de la ventana. El *área no cliente* es la parte de una ventana que está fuera del área cliente. El área incluye características como la barra de título, el menú ventana (también conocido como menú **del sistema** ) y las barras de desplazamiento. La mayoría de las aplicaciones se basan en la función de ventana predeterminada, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca), para dibujar esta área y, por tanto, pasar el mensaje de **WM \_ NCPAINT** a esta función. El *fondo* de la ventana es el color o el patrón con el que se rellena una ventana antes de que empiecen otras operaciones de dibujo. El fondo cubre todas las imágenes previamente en la ventana o en la pantalla en la ventana. Si una ventana pertenece a una clase de ventana que tiene un pincel de fondo de clase, la función **DefWindowProc** dibuja automáticamente el fondo de la ventana.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) rellena una estructura [**paintstruct (**](/windows/win32/api/winuser/ns-winuser-paintstruct) con información como las dimensiones de la parte de la ventana que se va a actualizar y una marca que indica si se ha dibujado el fondo de la ventana. La aplicación puede usar esta información para optimizar el dibujo. Por ejemplo, puede usar las dimensiones de la región de actualización, especificada por el miembro **rcPaint** , para limitar el dibujo solo a las partes de la ventana que necesiten actualizarse. Si una aplicación tiene una salida muy simple, puede omitir la región de actualización y dibujarla en toda la ventana, basándose en el sistema para descartar (recortar) cualquier salida innecesaria. Dado que el sistema recorta el dibujo que se extiende fuera de la región de recorte, solo está visible el dibujo que está en la región de actualización.

[**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) establece la región de actualización de una ventana en **null**. Esto borra la región, lo que impide que genere mensajes [**de \_ pintura de WM**](wm-paint.md) posteriores. Si una aplicación procesa un mensaje de **\_ dibujo de WM** pero no llama a **BeginPaint** ni borra la región de actualización, la aplicación continúa recibiendo mensajes de **WM \_ Paint** siempre y cuando la región no esté vacía. En todos los casos, una aplicación debe borrar la región de actualización antes de volver del mensaje de **\_ dibujo de WM** .

Una vez que la aplicación finaliza el dibujo, debe llamar a [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint). Para la mayoría de las ventanas, **EndPaint** libera el contexto de dispositivo de pantalla, lo que lo pone a disposición de otras ventanas. **EndPaint** también muestra el símbolo de intercalación, si se ocultó previamente por [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint). **BeginPaint** oculta el símbolo de intercalación para evitar que las operaciones de dibujo lo dañen.

-   [La región de actualización](the-update-region.md)
-   [Invalidación y validación de la región de actualización](invalidating-and-validating-the-update-region.md)
-   [Recuperación de la región de actualización](retrieving-the-update-region.md)
-   [Exclusión de la región de actualización](excluding-the-update-region.md)
-   [Dibujo sincrónico y asincrónico](synchronous-and-asynchronous-drawing.md)

 

 
