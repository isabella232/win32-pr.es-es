---
title: Capacidades de dibujo de hardware
description: Capacidades de dibujo de hardware
ms.assetid: 3a26de73-cb9e-41a0-8c33-a7cca7d6058e
keywords:
- Administrador de compresión de vídeo (VCM), dibujo
- VCM (Administrador de compresión de vídeo), dibujo
- ICGetInfo función)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7d3af8beb7c4ac676e421fe10d427322470d14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075823"
---
# <a name="hardware-drawing-capabilities"></a>Capacidades de dibujo de hardware

Algunos representadores pueden dibujar directamente en el hardware de vídeo a medida que descomprimen fotogramas de vídeo. Estos representadores devuelven la \_ marca VIDCF Draw en respuesta a la función [**ICGetInfo**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) . Cuando se usa este tipo de representador, la aplicación no tiene que controlar los datos descomprimidos. Permite que el representador retenga los datos descomprimidos para dibujar.

Si la aplicación usa un representador con funciones de dibujo, debe controlar las siguientes tareas:

-   Seleccione un representador.
-   Especificar formatos de imagen.
-   Inicialice el representador.
-   Dibuje los datos.
-   Controlan los parámetros de dibujo.

## <a name="renderer-selection"></a>Selección del representador

La macro [**ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) abre un representador que puede dibujar imágenes con el formato especificado. Devuelve un identificador de un representador si es correcto, o bien cero en caso contrario. Esta macro usa la función [**ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) para abrir el representador.

## <a name="specifying-image-formats"></a>Especificar formatos de imagen

Dado que la aplicación no necesita dibujar los datos descomprimidos, no requiere un formato de salida específico. Sin embargo, debe asegurarse de que el representador puede dibujar con el formato de entrada mediante el mensaje de [**\_ \_ consulta de dibujo ICM**](icm-draw-query.md) (o utilizar la macro [**ICDrawQuery**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) ). Este mensaje no puede determinar si un representador puede dibujar un mapa de bits. Si la aplicación debe determinar si el representador puede dibujar el mapa de bits, use este mensaje con la función [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) .

La aplicación puede tener un representador que sugiera un formato de entrada mediante la función [**ICDrawSuggestFormat**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat) . Esta función se usa cuando un representador separa las funciones de dibujo de las capacidades de descompresión. La mayoría de las aplicaciones que usan las funciones de dibujo no tendrán que determinar el formato de salida.

## <a name="renderer-initialization"></a>Inicialización del representador

La función [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) Inicializa un representador y le indica el destino del dibujo. Esta función también puede realizar las siguientes tareas:

-   Determinar si el representador admite un formato de entrada concreto.
-   Especifique si la operación de dibujo ocupa una ventana o toda la pantalla.
-   Especifique la parte de la imagen que se va a mostrar con el rectángulo de origen.
-   Defina la velocidad de reproducción de la secuencia de la imagen.

Algunos representadores almacenan en búfer los datos comprimidos para que funcionen de forma más eficaz. La aplicación puede enviar el [**mensaje \_ GETBUFFERSWANTED ICM**](icm-getbufferswanted.md) (o usar la macro [**ICGetBuffersWanted**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) ) para determinar el número de búferes que solicita el representador. La aplicación debe cargar previamente estos búferes y enviarlos al representador antes de dibujar.

## <a name="drawing-the-data"></a>Dibujar los datos

Puede usar la función [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) para descomprimir los datos para dibujar. El representador, sin embargo, no inicia el dibujo de datos hasta que la aplicación envíe el mensaje de [**\_ \_ Inicio de Draw de ICM**](icm-draw-start.md) (o use la macro [**ICDrawStart**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) ). Cuando la aplicación llama a esta función, el representador comienza a dibujar los fotogramas a la velocidad especificada por el parámetro *dwRate* dividido por el parámetro *dwScale* . Estos parámetros se proporcionaron cuando la aplicación inicializó el representador mediante la función [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) . El dibujo continúa hasta que la aplicación envía el mensaje de [**\_ \_ detención de Draw ICM**](icm-draw-stop.md) (o usa la macro [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) ).

> [!Note]  
> Si un representador almacena en búfer los datos antes del dibujo, la aplicación no debe utilizar la macro **ICDrawStart** hasta que haya enviado el número de fotogramas que el representador devolvió para la macro **ICGetBuffersWanted** .

 

El parámetro *lTime* de [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) especifica el tiempo de dibujo de un marco. El representador divide este entero según la escala de tiempo especificada con [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) para obtener la hora real. Las horas de las funciones **ICDraw** son relativas a **ICDrawStart**. **ICDrawStart** establece el reloj en cero. Por ejemplo, si la aplicación especifica 1000 para la escala de tiempo y 75 para *lTime*, el representador dibuja el fotograma 75 milisegundos en la secuencia.

## <a name="controlling-drawing-parameters"></a>Controlar los parámetros de dibujo

Para supervisar el reloj de un representador, envíe el [**mensaje \_ \_ GETTIME de Draw ICM**](icm-draw-gettime.md) (o use la macro [**ICDrawGetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) ), y puede establecer el reloj de un representador que puede dibujar datos mediante el envío del mensaje [**\_ \_ SETTIME de dibujo de ICM**](icm-draw-settime.md) (o use la macro [**ICDrawSetTime**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime) ).

Para cambiar la posición actual mientras se dibuja un representador, la aplicación puede enviar el mensaje de la [**\_ \_ ventana de dibujo ICM**](icm-draw-window.md) (o utilizar la macro [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) ) para cambiar la posición de la ventana. Normalmente, las aplicaciones usan este mensaje cada vez que cambia la ventana.

Si la ventana de reproducción obtiene un mensaje de la paleta de la presentación, la aplicación debe enviar el mensaje de error de envío de ICM (o usar la macro [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) ) para que el representador tenga en cuenta la paleta de nuevo para la reproducción. [**\_ \_**](icm-draw-realize.md) Las aplicaciones pueden cambiar la paleta enviando el [**mensaje \_ \_ CHANGEPALETTE de Draw ICM**](icm-draw-changepalette.md) (o usan la macro [**ICDrawChangePalette**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) ) y obtener la paleta actual mediante el envío del mensaje de la paleta de [**\_ \_ obtención \_ de dibujo ICM**](icm-draw-get-palette.md) .

Algunos representadores deben indicarse específicamente para mostrar los fotogramas que se le han pasado. El envío del mensaje de [**\_ \_ RENDERBUFFER ICM Draw**](icm-draw-renderbuffer.md) (o la utilización de la macro [**ICDrawRenderBuffer**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) ) hace que estos representadores dibujen el marco.

 

 




