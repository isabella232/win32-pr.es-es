---
title: Funcionalidades de dibujo de hardware
description: Funcionalidades de dibujo de hardware
ms.assetid: 3a26de73-cb9e-41a0-8c33-a7cca7d6058e
keywords:
- administrador de compresión de vídeo (VCM), dibujo
- VCM (administrador de compresión de vídeo), dibujo
- Función ICGetInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba7d3af8beb7c4ac676e421fe10d427322470d14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062913"
---
# <a name="hardware-drawing-capabilities"></a>Funcionalidades de dibujo de hardware

Algunos representadores pueden dibujar directamente en el hardware de vídeo a medida que descomprimen fotogramas de vídeo. Estos representadores devuelven la marca VIDCF \_ DRAW en respuesta a la función [**ICGetInfo.**](/windows/desktop/api/Vfw/nf-vfw-icgetinfo) Cuando se usa este tipo de representador, la aplicación no tiene que controlar los datos descomprimidos. Permite al representador conservar los datos descomprimidos para dibujar.

Si la aplicación usa un representador con funcionalidades de dibujo, debe controlar las siguientes tareas:

-   Seleccione un representador.
-   Especifique formatos de imagen.
-   Inicialice el representador.
-   Dibuje los datos.
-   Controlar parámetros de dibujo.

## <a name="renderer-selection"></a>Selección del representador

La [**macro ICDrawOpen**](/windows/desktop/api/Vfw/nf-vfw-icdrawopen) abre un representador que puede dibujar imágenes con el formato especificado. Devuelve un identificador de un representador si se realiza correctamente o cero en caso contrario. Esta macro usa la [**función ICLocate**](/windows/desktop/api/Vfw/nf-vfw-iclocate) para abrir el representador.

## <a name="specifying-image-formats"></a>Especificar formatos de imagen

Dado que la aplicación no necesita dibujar los datos descomprimidos, no requiere un formato de salida específico. Sin embargo, debe asegurarse de que el representador puede dibujar con el formato de entrada mediante el ICM [**\_ DRAW \_ QUERY**](icm-draw-query.md) (o usar la macro [**ICDrawQuery).**](/windows/desktop/api/Vfw/nf-vfw-icdrawquery) Este mensaje no puede determinar si un representador puede dibujar un mapa de bits. Si la aplicación debe determinar si el representador puede dibujar el mapa de bits, use este mensaje con la [**función ICDrawBegin.**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin)

La aplicación puede hacer que un representador sugiera un formato de entrada mediante [**la función ICDrawSuggestFormat.**](/windows/desktop/api/Vfw/nf-vfw-icdrawsuggestformat) Esta función se usa cuando un representador separa las funcionalidades de dibujo de las funcionalidades de descompresión. La mayoría de las aplicaciones que usan las funciones de dibujo no tendrán que determinar el formato de salida.

## <a name="renderer-initialization"></a>Inicialización del representador

La [**función ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) inicializa un representador y le indica el destino del dibujo. Esta función también puede realizar las siguientes tareas:

-   Determine si el representador admite un formato de entrada específico.
-   Especifique si la operación de dibujo ocupa una ventana o toda la pantalla.
-   Especifique la parte de la imagen que se mostrará mediante el rectángulo de origen.
-   Defina la velocidad de reproducción de la secuencia de imágenes.

Algunos representadores almacena en búfer los datos comprimidos para que funcionen de forma más eficaz. La aplicación puede enviar el [**mensaje \_ ICM GETBUFFERSWANTED**](icm-getbufferswanted.md) (o usar la macro [**ICGetBuffersWanted)**](/windows/desktop/api/Vfw/nf-vfw-icgetbufferswanted) para determinar el número de búferes que solicita el representador. La aplicación debe cargar previamente estos búferes y enviarlos al representador antes de dibujarlos.

## <a name="drawing-the-data"></a>Dibujar los datos

Puede usar la función [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) para descomprimir los datos para dibujar. Sin embargo, el representador no inicia el dibujo de datos hasta que la aplicación envía el ICM [**\_ DRAW \_ START**](icm-draw-start.md) (o usa la macro [**ICDrawStart).**](/windows/desktop/api/Vfw/nf-vfw-icdrawstart) Cuando la aplicación llama a esta función, el representador comienza a dibujar los fotogramas a la velocidad especificada por el *parámetro dwRate* dividido por el *parámetro dwScale;* Estos parámetros se proporcionaron cuando la aplicación inicializó el representador mediante la [**función ICDrawBegin.**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) El dibujo continúa hasta que la aplicación [**envía el ICM DRAW \_ \_ STOP**](icm-draw-stop.md) (o usa la macro [**ICDrawStop).**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop)

> [!Note]  
> Si un representador almacena en búfer los datos antes del dibujo, la aplicación no debe usar la macro **ICDrawStart** hasta que haya enviado el número de fotogramas devueltos por el representador para la macro **ICGetBuffersWanted.**

 

El *parámetro lTime* de [**ICDraw**](/windows/desktop/api/Vfw/nf-vfw-icdraw) especifica el tiempo para dibujar un marco. El representador divide este entero por la escala de tiempo especificada con [**ICDrawBegin**](/windows/desktop/api/Vfw/nf-vfw-icdrawbegin) para obtener la hora real. Los tiempos **de las funciones ICDraw** son relativos **a ICDrawStart.** **ICDrawStart establece** el reloj en cero. Por ejemplo, si la aplicación especifica 1000 para la escala de tiempo y 75 para *lTime*, el representador dibuja el marco 75 milisegundos en la secuencia.

## <a name="controlling-drawing-parameters"></a>Controlar parámetros de dibujo

Puede supervisar el reloj de un representador enviando el mensaje [**\_ DRAW \_ GETTIME**](icm-draw-gettime.md) de ICM (o usar la macro [**ICDrawGetTime)**](/windows/desktop/api/Vfw/nf-vfw-icdrawgettime) y puede establecer el reloj de un representador que puede dibujar datos enviando el mensaje [**DRAW \_ \_ SETTIME**](icm-draw-settime.md) de ICM (o use la macro [**ICDrawSetTime).**](/windows/desktop/api/Vfw/nf-vfw-icdrawsettime)

Para cambiar la posición actual mientras se dibuja un representador, la aplicación puede enviar el mensaje [**ICM \_ DRAW \_ WINDOW**](icm-draw-window.md) (o usar la macro [**ICDrawWindow)**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) para cambiar la posición de la ventana. Las aplicaciones suelen usar este mensaje cada vez que cambia la ventana.

Si la ventana de reproducción recibe un mensaje de la paleta de resultados, la aplicación debe enviar el mensaje [**\_ ICM DRAW \_ REALIZE**](icm-draw-realize.md) (o usar la macro [**ICDrawRealize)**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) para que el representador se dé cuenta de la paleta de nuevo para la reproducción. Las aplicaciones pueden cambiar la paleta enviando el mensaje [**\_ DRAW \_ CHANGEPALETTE**](icm-draw-changepalette.md) de ICM (o usar la macro [**ICDrawChangePalette)**](/windows/desktop/api/Vfw/nf-vfw-icdrawchangepalette) y obtener la paleta actual mediante el envío del ICM [**DRAW GET \_ \_ \_ PALETTE.**](icm-draw-get-palette.md)

Se debe indicar específicamente a algunos representadores que muestren los fotogramas pasados a ellos. El envío [**del ICM \_ DRAW \_ RENDERBUFFER**](icm-draw-renderbuffer.md) (o usar la macro [**ICDrawRenderBuffer)**](/windows/desktop/api/Vfw/nf-vfw-icdrawrenderbuffer) hace que estos representadores dibujen el marco.

 

 




