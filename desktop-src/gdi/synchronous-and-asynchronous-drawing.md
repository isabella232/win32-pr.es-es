---
description: La mayoría de los dibujos realizados durante el procesamiento del mensaje WM PAINT son asincrónicos; es decir, hay un retraso entre el momento en que se invalida una parte de la ventana y el momento en que se envía \_ WM \_ PAINT.
ms.assetid: c4eac615-6526-4ca6-854b-b4a598da13a4
title: Dibujo sincrónico y asincrónico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80dd5d5d63cbe10d19ec98e9f5dc9ae9163c18a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474316"
---
# <a name="synchronous-and-asynchronous-drawing"></a>Dibujo sincrónico y asincrónico

La mayoría de los dibujos realizados durante el procesamiento del mensaje [**\_ WM PAINT**](wm-paint.md) son asincrónicos; es decir, hay un retraso entre el momento en que se invalida una parte de la ventana y el momento en que se envía WM \_ PAINT. Durante el retraso, la aplicación normalmente recupera mensajes de la cola y lleva a cabo otras tareas. El motivo del retraso es que el sistema suele tratar el dibujo en una ventana como una operación de prioridad baja y funciona como si los mensajes y mensajes de entrada del usuario que pueden afectar a la posición o tamaño de una ventana se procesarán antes que WM \_ PAINT.

En algunos casos, es necesario que una aplicación dibuje sincrónicamente, es decir, dibuje en la ventana inmediatamente después de invalidar una parte de la ventana. Una aplicación típica dibuja su ventana principal inmediatamente después de crear la ventana para indicar al usuario que la aplicación se ha iniciado correctamente. El sistema dibuja algunas ventanas de control de forma sincrónica, como botones, porque dichas ventanas sirven como foco para la entrada del usuario. Aunque cualquier ventana con una rutina de dibujo simple se puede dibujar sincrónicamente, todo este dibujo debe realizarse rápidamente y no debe interferir con la capacidad de la aplicación para responder a la entrada del usuario.

Las [**funciones UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) [**y RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) permiten el dibujo sincrónico. **UpdateWindow** envía un [**mensaje \_ WM PAINT**](wm-paint.md) directamente a la ventana si la región de actualización no está vacía. **RedrawWindow también** envía un mensaje **WM \_ PAINT,** pero proporciona a la aplicación un mayor control sobre cómo dibujar la ventana, por ejemplo, si se va a dibujar el área no cliente y el fondo de la ventana o si se va a enviar el mensaje independientemente de si la región de actualización está vacía. Estas funciones envían el **mensaje \_ WM PAINT** directamente a la ventana, independientemente del número de otros mensajes de la cola de mensajes de la aplicación.

Cualquier ventana que requiera operaciones de dibujo lentas debe dibujarse de forma asincrónica para evitar que los mensajes pendientes se bloqueen a medida que se dibuja la ventana. Además, cualquier aplicación que invalide con frecuencia pequeñas partes de una ventana debe permitir que estas partes no válidas se consolide en un único mensaje [**DE WM \_ PAINT**](wm-paint.md) asincrónico, en lugar de una serie de mensajes **WM PAINT sincrónicos. \_**

 

 



