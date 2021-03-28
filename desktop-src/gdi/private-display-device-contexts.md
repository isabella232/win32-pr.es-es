---
description: Un contexto de dispositivo privado permite a una aplicación evitar la recuperación y la inicialización de un contexto de dispositivo de pantalla cada vez que la aplicación debe dibujarse en una ventana.
ms.assetid: 8de5a14b-a8b3-42a5-81f3-bf3c357052cb
title: Contextos de dispositivo de pantalla privada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451dbd3c0a232610026740d0ea0fa817ea2034b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544406"
---
# <a name="private-display-device-contexts"></a>Contextos de dispositivo de pantalla privada

Un *contexto de dispositivo privado* permite a una aplicación evitar la recuperación y la inicialización de un contexto de dispositivo de pantalla cada vez que la aplicación debe dibujarse en una ventana. Los contextos de dispositivo privados son útiles para las ventanas que requieren muchos cambios en los valores de los atributos del contexto del dispositivo para prepararlos para el dibujo. Los contextos de dispositivo privados reducen el tiempo necesario para preparar el contexto del dispositivo y, por lo tanto, el tiempo necesario para realizar el dibujo en la ventana.

Una aplicación dirige el sistema para crear un contexto de dispositivo privado para una ventana especificando el estilo CS \_ OWNDC en la clase Window. El sistema crea un contexto de dispositivo privado único cada vez que crea una nueva ventana que pertenece a la clase. Inicialmente, el contexto de dispositivo privado tiene los mismos valores predeterminados para los atributos que un contexto de dispositivo común, pero la aplicación puede modificarlos en cualquier momento. El sistema conserva los cambios en el contexto de dispositivo durante la vida de la ventana o hasta que la aplicación realiza cambios adicionales.

Una aplicación puede recuperar un identificador para el contexto de dispositivo privado mediante la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) en cualquier momento después de crear la ventana. La aplicación debe recuperar el identificador una sola vez. A partir de ese momento, puede mantener y usar el identificador cualquier número de veces. Dado que un contexto de dispositivo privado no forma parte de la memoria caché de contexto de dispositivo de pantalla, una aplicación no necesita liberar nunca el contexto de dispositivo mediante la función [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) .

El sistema ajusta automáticamente el contexto de dispositivo para reflejar los cambios en la ventana, como mover o cambiar el tamaño. Esto garantiza que todas las ventanas superpuestas siempre se recortan correctamente; es decir, la aplicación no requiere ninguna acción para garantizar el recorte. Sin embargo, el sistema no revisa el contexto del dispositivo para incluir la región de actualización. Por lo tanto, al procesar un mensaje de [**\_ dibujo de WM**](wm-paint.md) , la aplicación debe incorporar la región de actualización mediante una llamada a [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) o mediante la recuperación de la región de actualización y la intersección con la región de recorte actual. Si la aplicación no llama a **BeginPaint**, debe validar explícitamente la región de actualización mediante el uso de la función [**ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) o [**ValidateRgn**](/windows/desktop/api/Winuser/nf-winuser-validatergn) . Si la aplicación no valida la región de actualización, la ventana recibe una serie infinita de mensajes de **\_ dibujo de WM** .

Dado que [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) oculta el símbolo de intercalación si se muestra una ventana, una aplicación que llama a **BeginPaint** también debe llamar a la función [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) para restaurar el símbolo de intercalación. **EndPaint** no tiene ningún efecto en un contexto de dispositivo privado.

Aunque es conveniente usar un contexto de dispositivo privado, el uso de memoria es intensivo en cuanto a recursos del sistema, lo que requiere que se almacenen 800 o más bytes. Los contextos de dispositivo privados se recomiendan cuando las consideraciones de rendimiento superan los costos de almacenamiento.

El sistema incluye el contexto de dispositivo privado al enviar el mensaje de [**\_ ERASEBKGND de WM**](../winmsg/wm-erasebkgnd.md) a la aplicación. Las selecciones actuales del contexto de dispositivo privado, incluido el modo de asignación, están en vigor cuando la aplicación o el sistema procesa estos mensajes. Para evitar efectos no deseados, el sistema utiliza coordenadas lógicas al borrar el fondo; por ejemplo, usa la función [**GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox) para recuperar las coordenadas lógicas del área que se va a borrar y pasa estas coordenadas a la función [**FillRect**](/windows/desktop/api/Winuser/nf-winuser-fillrect) . Las aplicaciones que procesan estos mensajes pueden utilizar técnicas similares.

Una aplicación puede usar la función [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) para obligar al sistema a devolver un contexto de dispositivo común para la ventana que tiene un contexto de dispositivo privado. Esto resulta útil para llevar a cabo un toque rápido en una ventana sin cambiar los valores actuales de los atributos del contexto de dispositivo privado.

 

 
