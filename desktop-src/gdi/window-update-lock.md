---
description: Un bloqueo de actualización de ventana es una suspensión temporal del dibujo en una ventana.
ms.assetid: 92b1ba04-ff79-4a37-9633-99412cdafe95
title: Bloqueo de actualización de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4897915020134387947c7a77009c4bdbd63cfdd6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241269"
---
# <a name="window-update-lock"></a>Bloqueo de actualización de ventana

Un *bloqueo de actualización de* ventana es una suspensión temporal del dibujo en una ventana. El sistema usa el bloqueo para evitar que otras ventanas arrojen sobre el rectángulo de seguimiento cada vez que el usuario mueve o cambia el tamaño de una ventana. Las aplicaciones pueden usar el bloqueo para evitar el dibujo si realizan operaciones similares de movimiento o tamaño con sus propias ventanas.

Una aplicación usa la [**función LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) para establecer o borrar un bloqueo de actualización de ventana, especificando la ventana que se bloqueará. El bloqueo se aplica a la ventana especificada y a todas sus ventanas secundarias. Cuando se establece el bloqueo, las funciones [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) y [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) devuelven un contexto de dispositivo para mostrar con una región visible que está vacía. Dado esto, la aplicación puede seguir dibujando en la ventana, pero se recorta toda la salida. El bloqueo persiste hasta que la aplicación lo borra mediante una llamada a **LockWindowUpdate**, **especificando NULL** para la ventana. Aunque **LockWindowUpdate fuerza** que la región visible de una ventana esté vacía, la función no hace que la ventana especificada sea invisible y no borra el bit de estilo VISIBLE de WS. \_

Una vez establecido el bloqueo, la aplicación puede usar la función [**GetDCEx,**](/windows/desktop/api/Winuser/nf-winuser-getdcex) con el valor LOCKWINDOWUPDATE de DCX, para recuperar un contexto de dispositivo de presentación para dibujar sobre la \_ ventana bloqueada. Esto permite a la aplicación dibujar un rectángulo de seguimiento al procesar mensajes de teclado o mouse. El sistema usa este método cuando el usuario mueve y cambia el tamaño de las ventanas. **GetDCEx recupera** el contexto del dispositivo de presentación de la caché de contexto del dispositivo para mostrar, por lo que la aplicación debe liberar el contexto del dispositivo tan pronto como sea posible después del dibujo.

Mientras se establece un bloqueo de actualización de ventana, el sistema crea un rectángulo delimitador acumulado para cada ventana bloqueada. Cuando se borra el bloqueo, el sistema usa este rectángulo delimitador para establecer la región de actualización de la ventana y sus ventanas secundarias, lo que fuerza un mensaje [**WM \_ PAINT**](wm-paint.md) final. Si el rectángulo delimitador acumulado está vacío (es decir, si no se ha producido ningún dibujo mientras se estableció el bloqueo), no se establece la región de actualización.

 

 



