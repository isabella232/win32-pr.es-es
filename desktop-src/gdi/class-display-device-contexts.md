---
description: Mediante el uso de un contexto de dispositivo de clase, una aplicación puede usar un único contexto de dispositivo de pantalla para cada ventana que pertenece a una clase especificada.
ms.assetid: fc76abbf-68da-47f2-8145-4fad806297b4
title: La clase muestra contextos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e5a4cc0268d948e1a6f95050409698217e3f13e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985051"
---
# <a name="class-display-device-contexts"></a>La clase muestra contextos de dispositivo

Mediante el uso de un *contexto de dispositivo de clase*, una aplicación puede usar un único contexto de dispositivo de pantalla para cada ventana que pertenece a una clase especificada. Los contextos de dispositivo de clase se suelen usar con ventanas de control que se dibujan con los mismos valores de atributo. Al igual que los contextos de dispositivos privados, los contextos de dispositivo de clase minimizan el tiempo necesario para preparar un contexto de dispositivo para el dibujo.

El sistema proporciona un contexto de dispositivo de clase para una ventana si pertenece a una clase de ventana con el \_ estilo CS CLASSDC. El sistema crea el contexto de dispositivo al crear la primera ventana que pertenece a la clase y, a continuación, usa el mismo contexto de dispositivo para todas las ventanas creadas posteriormente en la clase. Inicialmente, el contexto de dispositivo de clase tiene los mismos valores predeterminados para los atributos que un contexto de dispositivo común, pero la aplicación puede modificarlos en cualquier momento. El sistema conserva todos los cambios, excepto la región de recorte y el origen del dispositivo, hasta que se destruya la última ventana de la clase. Un cambio realizado en una ventana se aplica a todas las ventanas de esa clase.

Una aplicación puede recuperar el identificador del contexto de dispositivo de clase usando la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) en cualquier momento después de crear la primera ventana. La aplicación puede mantener y usar el identificador sin liberarlo porque el contexto de dispositivo de clase no forma parte de la memoria caché de contexto del dispositivo de pantalla. Si la aplicación crea otra ventana en la misma clase de ventana, la aplicación debe recuperar de nuevo el contexto de dispositivo de clase. Al recuperar el contexto de dispositivo, se establece el origen de dispositivo y la región de recorte correctos para la nueva ventana. Una vez que la aplicación recupera el contexto de dispositivo de clase para una nueva ventana en la clase, el contexto de dispositivo ya no se puede usar para dibujar en la ventana original sin recuperarlo de nuevo para esa ventana. En general, cada vez que se debe dibujar en una ventana, una aplicación debe recuperar explícitamente el contexto de dispositivo de clase para la ventana.

Las aplicaciones que usan contextos de dispositivo de clase siempre deben llamar a [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) al procesar un mensaje de [**\_ pintura de WM**](wm-paint.md) . La función establece el origen de dispositivo y la región de recorte correctos para la ventana e incorpora la región de actualización. La aplicación también debe llamar a [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) para restaurar el símbolo de intercalación si **BeginPaint** lo HID. **EndPaint** no tiene ningún efecto en un contexto de dispositivo de clase.

El sistema pasa el contexto de dispositivo de clase al enviar el mensaje de [**\_ ERASEBKGND de WM**](../winmsg/wm-erasebkgnd.md) a la aplicación, lo que permite que los valores de atributo actuales afecten a cualquier dibujo realizado por la aplicación o el sistema al procesar este mensaje. Como podría tener una ventana con un contexto de dispositivo privado, una aplicación puede usar [**GetDCEx**](/windows/desktop/api/Winuser/nf-winuser-getdcex) para obligar al sistema a devolver un contexto de dispositivo común para la ventana que tiene un contexto de dispositivo de clase.

No se recomienda usar contextos de dispositivo de clase.

 

 
