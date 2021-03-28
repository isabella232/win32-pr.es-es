---
description: Un bloqueo de actualización de ventana es una suspensión temporal del dibujo en una ventana.
ms.assetid: 92b1ba04-ff79-4a37-9633-99412cdafe95
title: Bloqueo de actualización de ventana
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4897915020134387947c7a77009c4bdbd63cfdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276449"
---
# <a name="window-update-lock"></a>Bloqueo de actualización de ventana

Un *bloqueo de actualización de ventana* es una suspensión temporal del dibujo en una ventana. El sistema utiliza el bloqueo para evitar que otras ventanas dibujen el rectángulo de seguimiento cada vez que el usuario mueve o cambia el tamaño de una ventana. Las aplicaciones pueden utilizar el bloqueo para evitar el dibujo si realizan operaciones de movimiento o cambio de tamaño similares con sus propias ventanas.

Una aplicación utiliza la función [**LockWindowUpdate**](/windows/desktop/api/Winuser/nf-winuser-lockwindowupdate) para establecer o borrar un bloqueo de actualización de ventana, especificando la ventana que se va a bloquear. El bloqueo se aplica a la ventana especificada y a todas sus ventanas secundarias. Cuando se establece el bloqueo, las funciones [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) y [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) devuelven un contexto de dispositivo de pantalla con un área visible que está vacía. Dado esto, la aplicación puede continuar dibujando en la ventana, pero todos los resultados se recortan. El bloqueo se conserva hasta que la aplicación lo borra llamando a **LockWindowUpdate**, especificando **null** para la ventana. Aunque **LockWindowUpdate** fuerza que el área visible de una ventana esté vacía, la función no hace que la ventana especificada sea invisible y no borra el \_ bit de estilo visible de WS.

Una vez establecido el bloqueo, la aplicación puede usar la función [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) , con el \_ valor LOCKWINDOWUPDATE de DCX, para recuperar un contexto de dispositivo de pantalla que se va a dibujar en la ventana bloqueada. Esto permite que la aplicación dibuje un rectángulo de seguimiento al procesar los mensajes del teclado o del mouse. El sistema utiliza este método cuando el usuario mueve y cambia el tamaño de las ventanas. **GetDCEx** recupera el contexto de dispositivo de pantalla de la memoria caché de contexto de dispositivo de pantalla, por lo que la aplicación debe liberar el contexto de dispositivo lo antes posible después de dibujar.

Mientras se establece un bloqueo de actualización de ventana, el sistema crea un rectángulo delimitador acumulado para cada ventana bloqueada. Cuando se borra el bloqueo, el sistema usa este rectángulo delimitador para establecer la región de actualización de la ventana y sus ventanas secundarias, lo que fuerza un mensaje de [**\_ pintura de WM**](wm-paint.md) eventual. Si el rectángulo delimitador acumulado está vacío (es decir, si no se ha producido ningún dibujo mientras se estableció el bloqueo), no se establece la región de actualización.

 

 



