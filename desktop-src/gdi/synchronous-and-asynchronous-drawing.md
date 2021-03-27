---
description: La mayoría del dibujo que se lleva a cabo durante el procesamiento del mensaje de pintura de WM \_ es asincrónico; es decir, hay un retraso entre el momento en que se invalida una parte de la ventana y la hora en que \_ se envía la pintura de WM.
ms.assetid: c4eac615-6526-4ca6-854b-b4a598da13a4
title: Dibujo sincrónico y asincrónico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a80dd5d5d63cbe10d19ec98e9f5dc9ae9163c18a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002806"
---
# <a name="synchronous-and-asynchronous-drawing"></a>Dibujo sincrónico y asincrónico

La mayoría del dibujo que se lleva a cabo durante el procesamiento del mensaje de [**\_ pintura de WM**](wm-paint.md) es asincrónico; es decir, hay un retraso entre el momento en que se invalida una parte de la ventana y la hora en que \_ se envía la pintura de WM. Durante el retraso, la aplicación normalmente recupera mensajes de la cola y realiza otras tareas. El motivo del retraso es que el sistema trata normalmente el dibujo en una ventana como una operación de prioridad baja y funciona como si los mensajes de entrada del usuario y los mensajes que pueden afectar a la posición o el tamaño de una ventana se procesarán antes de la pintura de WM \_ .

En algunos casos, es necesario que una aplicación dibuje sincrónicamente, dibujando en la ventana inmediatamente después de invalidar una parte de la ventana. Una aplicación típica dibuja su ventana principal inmediatamente después de crear la ventana para indicar al usuario que la aplicación se ha iniciado correctamente. El sistema dibuja algunas ventanas de control sincrónicamente, como los botones, ya que estas ventanas sirven como el foco de los datos proporcionados por el usuario. Aunque cualquier ventana con una rutina de dibujo simple se puede dibujar sincrónicamente, todo el dibujo debe realizarse rápidamente y no debe interferir con la capacidad de la aplicación para responder a los datos proporcionados por el usuario.

Las funciones [**UpdateWindow**](/windows/desktop/api/Winuser/nf-winuser-updatewindow) y [**RedrawWindow**](/windows/desktop/api/Winuser/nf-winuser-redrawwindow) permiten dibujar sincrónicamente. **UpdateWindow** envía un mensaje de [**\_ dibujo de WM**](wm-paint.md) directamente a la ventana si la región de actualización no está vacía. **RedrawWindow** también envía un mensaje de **\_ dibujo de WM** , pero proporciona a la aplicación un mayor control sobre cómo dibujar la ventana, por ejemplo, si se debe dibujar el área no cliente y el fondo de la ventana, o si se debe enviar el mensaje independientemente de si la región de actualización está vacía. Estas funciones envían el mensaje de **\_ dibujo de WM** directamente a la ventana, independientemente del número de otros mensajes en la cola de mensajes de la aplicación.

Cualquier ventana que requiera operaciones de dibujo que consumen mucho tiempo debe dibujarse de forma asincrónica para evitar que los mensajes pendientes se bloqueen mientras se dibuja la ventana. Además, cualquier aplicación que invalide con frecuencia pequeñas partes de una ventana debe permitir que estas partes no válidas se consoliden en un solo mensaje de [**\_ dibujo de WM**](wm-paint.md) asincrónico, en lugar de una serie de mensajes de **\_ dibujo de WM** sincrónicos.

 

 



