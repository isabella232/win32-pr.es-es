---
description: Un contexto de dispositivo privado permite que una aplicación evite recuperar e inicializar un contexto de dispositivo de presentación cada vez que la aplicación debe dibujarse en una ventana.
ms.assetid: 8de5a14b-a8b3-42a5-81f3-bf3c357052cb
title: Contextos de dispositivo de pantalla privada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce63fddbc2e351b166308c9ca3ce674be1a0026851af7bb1192c49cc961cdee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092885"
---
# <a name="private-display-device-contexts"></a>Contextos de dispositivo de pantalla privada

Un *contexto de dispositivo privado* permite que una aplicación evite recuperar e inicializar un contexto de dispositivo de presentación cada vez que la aplicación debe dibujarse en una ventana. Los contextos de dispositivo privado son útiles para las ventanas que requieren muchos cambios en los valores de los atributos del contexto del dispositivo para prepararlo para dibujar. Los contextos de dispositivo privado reducen el tiempo necesario para preparar el contexto del dispositivo y, por tanto, el tiempo necesario para llevar a cabo el dibujo en la ventana.

Una aplicación dirige al sistema para crear un contexto de dispositivo privado para una ventana especificando el estilo OWNDC de CS \_ en la clase window. El sistema crea un contexto de dispositivo privado único cada vez que crea una nueva ventana que pertenece a la clase . Inicialmente, el contexto de dispositivo privado tiene los mismos valores predeterminados para los atributos que un contexto de dispositivo común, pero la aplicación puede modificarlos en cualquier momento. El sistema conserva los cambios en el contexto del dispositivo durante la vida útil de la ventana o hasta que la aplicación realiza cambios adicionales.

Una aplicación puede recuperar un identificador en el contexto del dispositivo privado mediante la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) en cualquier momento después de crear la ventana. La aplicación solo debe recuperar el identificador una vez. A partir de ese momento, puede mantener y usar el identificador de cualquier número de veces. Dado que un contexto de dispositivo privado no forma parte de la caché de contexto del dispositivo de presentación, una aplicación nunca necesita liberar el contexto del dispositivo mediante la [**función ReleaseDC.**](/windows/desktop/api/Winuser/nf-winuser-releasedc)

El sistema ajusta automáticamente el contexto del dispositivo para reflejar los cambios en la ventana, como mover o ajustar el tamaño. Esto garantiza que las ventanas superpuestas siempre se recortan correctamente; es decir, la aplicación no requiere ninguna acción para garantizar el recorte. Sin embargo, el sistema no revisa el contexto del dispositivo para incluir la región de actualización. Por lo tanto, al procesar un [**mensaje \_ WM PAINT,**](wm-paint.md) la aplicación debe incorporar la región de actualización llamando a [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) o recuperando la región de actualización e intersecando con la región de recorte actual. Si la aplicación no llama a **BeginPaint**, debe validar explícitamente la región de actualización mediante la [**función ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) [**o ValidateRgn.**](/windows/desktop/api/Winuser/nf-winuser-validatergn) Si la aplicación no valida la región de actualización, la ventana recibe una serie infinita de **mensajes WM \_ PAINT.**

Dado [**que BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) oculta el signo de diálogo si una ventana lo muestra, una aplicación que llama a **BeginPaint** también debe llamar a la función [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) para restaurar el signo de diálogo. **EndPaint** no tiene ningún otro efecto en un contexto de dispositivo privado.

Aunque un contexto de dispositivo privado es práctico de usar, consume mucha memoria en términos de recursos del sistema, lo que requiere 800 o más bytes para almacenar. Se recomiendan contextos de dispositivo privado cuando las consideraciones de rendimiento superan los costos de almacenamiento.

El sistema incluye el contexto de dispositivo privado al enviar el [**mensaje \_ ERASEBND de WM**](../winmsg/wm-erasebkgnd.md) a la aplicación. Las selecciones actuales del contexto del dispositivo privado, incluido el modo de asignación, están en vigor cuando la aplicación o el sistema procesa estos mensajes. Para evitar efectos no deseados, el sistema usa coordenadas lógicas al borrar el fondo; Por ejemplo, usa la función [**GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox) para recuperar las coordenadas lógicas del área que se va a borrar y pasa estas coordenadas a la [**función FillRect.**](/windows/desktop/api/Winuser/nf-winuser-fillrect) Las aplicaciones que procesan estos mensajes pueden usar técnicas similares.

Una aplicación puede usar la [**función GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) para forzar al sistema a devolver un contexto de dispositivo común para la ventana que tiene un contexto de dispositivo privado. Esto resulta útil para realizar cambios rápidos en una ventana sin cambiar los valores actuales de los atributos del contexto del dispositivo privado.

 

 
