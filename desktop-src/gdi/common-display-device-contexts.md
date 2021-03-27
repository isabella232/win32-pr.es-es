---
description: Un contexto de dispositivo común se usa para dibujar en el área de cliente de la ventana.
ms.assetid: 63c4f775-b1a3-4f7c-808b-81c596f26353
title: Contextos de dispositivo de pantalla comunes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 890b0235784ec1ed11c8ce3a553244629a008d75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001525"
---
# <a name="common-display-device-contexts"></a>Contextos de dispositivo de pantalla comunes

Un *contexto de dispositivo común* se usa para dibujar en el área de cliente de la ventana. El sistema proporciona un contexto de dispositivo común de forma predeterminada para cualquier ventana cuya clase de ventana no especifique explícitamente un estilo de contexto de dispositivo de pantalla. Normalmente, los contextos de dispositivo comunes se utilizan con ventanas que se pueden dibujar sin cambios profundos en los atributos de contexto del dispositivo. Los contextos de dispositivo comunes son prácticos porque no requieren memoria adicional ni recursos del sistema, pero pueden ser inconvenientes si la aplicación debe configurar muchos atributos antes de usarlos.

El sistema recupera todos los contextos de dispositivo comunes de la memoria caché de contexto de dispositivo de pantalla. Una aplicación puede recuperar un contexto de dispositivo común inmediatamente después de crear la ventana. Dado que el contexto de dispositivo común es de la memoria caché, la aplicación siempre debe liberar el contexto del dispositivo tan pronto como sea posible después del dibujo. Una vez que se libera el contexto de dispositivo común, ya no es válido y la aplicación no debe intentar dibujar con él. Para volver a dibujar, la aplicación debe recuperar un nuevo contexto de dispositivo común y seguir recuperando y liberando un contexto de dispositivo común cada vez que se dibuja en la ventana. Si la aplicación recupera el identificador de contexto del dispositivo mediante la función [**GetDC**](/windows/desktop/api/Winuser/nf-winuser-getdc) , debe usar la función [**ReleaseDC**](/windows/desktop/api/Winuser/nf-winuser-releasedc) para liberar el identificador. Del mismo modo, para cada función [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint) , la aplicación debe usar una función [**EndPaint**](/windows/desktop/api/Winuser/nf-winuser-endpaint) correspondiente.

Cuando la aplicación recupera el contexto del dispositivo, el sistema ajusta el origen para que se alinee con la esquina superior izquierda del área cliente. También establece la región de recorte para que el resultado en el contexto del dispositivo se recorte en el área cliente. Cualquier salida que de otro modo aparecería fuera del área cliente se recorta. Si la aplicación recupera el contexto de dispositivo común mediante [**BeginPaint**](/windows/desktop/api/Winuser/nf-winuser-beginpaint), el sistema también incluye la región de actualización en la región de recorte para restringir aún más la salida.

Cuando una aplicación libera un contexto de dispositivo común, el sistema restaura los valores predeterminados de los atributos del contexto del dispositivo. Una aplicación que modifica los valores de atributo debe hacerlo cada vez que recupera un contexto de dispositivo común. La liberación del contexto del dispositivo libera cualquier objeto de dibujo que la aplicación haya seleccionado en él, por lo que la aplicación no necesita liberar estos objetos antes de liberar el contexto del dispositivo. En todos los casos, una aplicación nunca debe asumir que el contexto de dispositivo común conserva las selecciones no predeterminadas después de su lanzamiento.

 

 



