---
description: Usar los controles de presentación de vídeo
ms.assetid: 09501d67-effb-41ce-a7b7-d2415acdf3ac
title: Usar los controles de presentación de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbb9c83485faebc873b3e92502122c5497b4bb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811521"
---
# <a name="using-the-video-display-controls"></a>Usar los controles de presentación de vídeo

La interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) controla cómo el representador de vídeo mejorado (EVR) muestra el vídeo en una ventana de la aplicación. Esta interfaz se puede usar en DirectShow o en Media Foundation. Internamente, el presentador predeterminado de EVR proporciona los controles de presentación de vídeo. Si escribe un presentador personalizado, puede proporcionar la misma interfaz o definir una interfaz personalizada.

La manera correcta de obtener un puntero a la interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) depende de si está usando la versión DIRECTSHOW de EVR o la versión media Foundation. En el Media Foundation EVR, también depende de si usa el EVR directamente o lo usa a través de la sesión multimedia (que es más habitual).

Para obtener un puntero a la interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) , haga lo siguiente:

1.  Obtiene un puntero a la interfaz [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .

    -   Si usa el filtro EVR de DirectShow, llame a **QueryInterface** en el filtro.

    -   Si usa el receptor de medios EVR directamente, llame a **QueryInterface** en el receptor de medios.

    -   Si usa la sesión multimedia, llame a **QueryInterface** en la sesión multimedia.

2.  Si usa la sesión multimedia, espere a que la sesión multimedia envíe el evento [MESessionTopologyStatus](mesessiontopologystatus.md) con el valor de estado MF \_ TOPOSTATUS \_ listo. (En caso contrario, omita este paso).

3.  Llame a [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obtener la interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) . El identificador de servicio es el \_ servicio de representación de vídeo Mr \_ \_ .

Puede usar la interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) para realizar las siguientes tareas:

-   Establezca la ventana de recorte.

-   Establezca los rectángulos de origen y de destino.

-   Actualice la ventana de vídeo en respuesta a los mensajes de ventana.

-   Habilitar o deshabilitar el modo de pantalla completa.

## <a name="clipping-window"></a>Ventana de recorte

La aplicación debe proporcionar una ventana en la que EVR dibuje el vídeo. Para establecer la ventana de recorte, llame a [**IMFVideoDisplayControl:: SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) con un identificador a la ventana de la aplicación.

Si crea el receptor de medios de EVR a través de su objeto de activación, este paso no es necesario. El objeto de activación llama automáticamente a [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow), mediante el identificador de ventana que proporcionó en la función [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .

## <a name="source-and-destination-rectangles"></a>Rectángulos de origen y de destino

Durante la reproducción, el presentador toma una parte de la imagen de vídeo compuesta y la dibuja en un área de la ventana de vídeo. La parte de la imagen compuesta es el *rectángulo de origen* y el área de la ventana de vídeo es el *rectángulo de destino*.

El rectángulo de origen se define mediante coordenadas normalizadas en las que el punto (0,0, 0,0) corresponde a la esquina superior izquierda del vídeo y (1,0, 1,0) corresponde a la esquina inferior derecha del vídeo. El rectángulo de origen puede ser cualquier región de este rectángulo. El rectángulo de destino se especifica en píxeles, en relación con el área cliente de la ventana. El rectángulo de origen predeterminado es la imagen completa y el rectángulo de destino predeterminado es un rectángulo vacío.

Para establecer los rectángulos de origen y de destino, llame a [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Si crea el receptor de medios de EVR a través de su objeto de activación, este paso no es necesario. El objeto de activación establece automáticamente el rectángulo de destino igual a todo el área cliente de la ventana. Sin embargo, debe llamar a [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) si desea cambiar el rectángulo de origen o establecer un rectángulo de destino diferente.

## <a name="window-messages"></a>Mensajes de ventana

Durante la reproducción, la aplicación debe responder a ciertos mensajes de ventana, como se indica a continuación:

-   WM \_ Paint: llame a [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) para volver a dibujar el vídeo. Además, evite pintar el rectángulo de destino mientras se reproduce el vídeo, ya que esto puede provocar parpadeos.

-   \_Tamaño de WM: puede que tenga que llamar a [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) para cambiar el tamaño del rectángulo de destino.

A diferencia del filtro del procesador de mezcla de vídeo (VMR) de DirectShow, no es necesario notificar a EVR cuando recibe un mensaje de DISPLAYCHANGE de WM \_ .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> </dl>

 

 



