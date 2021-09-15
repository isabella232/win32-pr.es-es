---
description: Un contexto de dispositivo privado permite que una aplicación evite recuperar e inicializar un contexto de dispositivo para mostrar cada vez que la aplicación debe dibujar en una ventana.
ms.assetid: 8de5a14b-a8b3-42a5-81f3-bf3c357052cb
title: Contextos de dispositivo de presentación privada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451dbd3c0a232610026740d0ea0fa817ea2034b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127360470"
---
# <a name="private-display-device-contexts"></a>Contextos de dispositivo de presentación privada

Un *contexto de dispositivo privado* permite que una aplicación evite recuperar e inicializar un contexto de dispositivo para mostrar cada vez que la aplicación debe dibujar en una ventana. Los contextos de dispositivo privado son útiles para ventanas que requieren muchos cambios en los valores de los atributos del contexto del dispositivo para prepararlo para dibujar. Los contextos de dispositivo privado reducen el tiempo necesario para preparar el contexto del dispositivo y, por tanto, el tiempo necesario para realizar el dibujo en la ventana.

Una aplicación dirige al sistema para crear un contexto de dispositivo privado para una ventana especificando el estilo OWNDC de CS \_ en la clase de ventana. El sistema crea un contexto de dispositivo privado único cada vez que crea una nueva ventana que pertenece a la clase . Inicialmente, el contexto de dispositivo privado tiene los mismos valores predeterminados para los atributos que un contexto de dispositivo común, pero la aplicación puede modificarlos en cualquier momento. El sistema conserva los cambios en el contexto del dispositivo durante la vida útil de la ventana o hasta que la aplicación realiza cambios adicionales.

Una aplicación puede recuperar un identificador en el contexto del dispositivo privado mediante la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) en cualquier momento después de crear la ventana. La aplicación solo debe recuperar el identificador una vez. A partir de entonces, puede mantener y usar el identificador de cualquier número de veces. Dado que un contexto de dispositivo privado no forma parte de la caché de contexto del dispositivo para mostrar, una aplicación nunca necesita liberar el contexto del dispositivo mediante la [**función ReleaseDC.**](/windows/desktop/api/Winuser/nf-winuser-releasedc)

El sistema ajusta automáticamente el contexto del dispositivo para reflejar los cambios en la ventana, como mover o ajustar el tamaño. Esto garantiza que las ventanas superpuestas siempre se recortan correctamente; es decir, la aplicación no requiere ninguna acción para garantizar el recorte. Sin embargo, el sistema no revisa el contexto del dispositivo para incluir la región de actualización. Por lo tanto, al procesar un [**mensaje \_ WM PAINT,**](wm-paint.md) la aplicación debe incorporar la región de actualización mediante una llamada a [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) o recuperando la región de actualización y formando una intersección con la región de recorte actual. Si la aplicación no llama a **BeginPaint**, debe validar explícitamente la región de actualización mediante la [**función ValidateRect**](/windows/desktop/api/Winuser/nf-winuser-validaterect) [**o ValidateRgn.**](/windows/desktop/api/Winuser/nf-winuser-validatergn) Si la aplicación no valida la región de actualización, la ventana recibe una serie infinita de **mensajes WM \_ PAINT.**

Dado [**que BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) oculta el caret si se muestra una ventana, una aplicación que llama a **BeginPaint** también debe llamar a la función [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) para restaurar el caret. **EndPaint** no tiene ningún otro efecto en un contexto de dispositivo privado.

Aunque un contexto de dispositivo privado es cómodo de usar, consume mucha memoria en términos de recursos del sistema, lo que requiere 800 bytes o más para almacenar. Se recomiendan contextos de dispositivo privado cuando las consideraciones de rendimiento superan los costos de almacenamiento.

El sistema incluye el contexto de dispositivo privado al enviar el [**mensaje \_ ERASEB DOMAINND**](../winmsg/wm-erasebkgnd.md) de WM a la aplicación. Las selecciones actuales del contexto del dispositivo privado, incluido el modo de asignación, están en vigor cuando la aplicación o el sistema procesa estos mensajes. Para evitar efectos no deseados, el sistema usa coordenadas lógicas al borrar el fondo; Por ejemplo, usa la función [**GetClipBox**](/windows/desktop/api/Wingdi/nf-wingdi-getclipbox) para recuperar las coordenadas lógicas del área que se va a borrar y pasa estas coordenadas a la [**función FillRect.**](/windows/desktop/api/Winuser/nf-winuser-fillrect) Las aplicaciones que procesan estos mensajes pueden usar técnicas similares.

Una aplicación puede usar la [**función GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) para forzar al sistema a devolver un contexto de dispositivo común para la ventana que tiene un contexto de dispositivo privado. Esto resulta útil para llevar a cabo cambios rápidos en una ventana sin cambiar los valores actuales de los atributos del contexto del dispositivo privado.

 

 
