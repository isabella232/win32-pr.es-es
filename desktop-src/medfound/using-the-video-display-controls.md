---
description: Uso de los controles de visualización de vídeo
ms.assetid: 09501d67-effb-41ce-a7b7-d2415acdf3ac
title: Uso de los controles de visualización de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbb9c83485faebc873b3e92502122c5497b4bb1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363691"
---
# <a name="using-the-video-display-controls"></a>Uso de los controles de visualización de vídeo

La [**interfaz IMFVideoDisplayControl controla**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) cómo el representador de vídeo mejorado (EVR) muestra el vídeo dentro de una ventana de la aplicación. Esta interfaz se puede usar en DirectShow o Media Foundation. Internamente, el presentador predeterminado de EVR proporciona los controles de visualización de vídeo. Si escribe un presentador personalizado, puede proporcionar la misma interfaz o definir una interfaz personalizada.

La manera correcta de obtener un puntero a la interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) depende de si usa la versión DirectShow del EVR o la versión Media Foundation. Para la Media Foundation EVR, también depende de si usa la EVR directamente o a través de la sesión multimedia (que es más habitual).

Para obtener un puntero a la [**interfaz IMFVideoDisplayControl,**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) haga lo siguiente:

1.  Obtenga un puntero a la [**interfaz IMFGetService.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)

    -   Si usa el filtro DirectShow EVR, llame a **QueryInterface** en el filtro.

    -   Si usa el receptor de medios EVR directamente, llame a **QueryInterface** en el receptor de medios.

    -   Si usa la sesión multimedia, llame a **QueryInterface** en la sesión multimedia.

2.  Si usa la sesión multimedia, espere a que la sesión multimedia envíe el evento [MESessionTopologyStatus](mesessiontopologystatus.md) con un valor de estado DE MF \_ TOPOSTATUS \_ READY. (Omita este paso en caso contrario).

3.  Llame [**a IMFGetService::GetService para**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) obtener la interfaz [**IMFVideoDisplayControl.**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) El identificador de servicio es MR \_ VIDEO \_ RENDER \_ SERVICE.

Puede usar la interfaz [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) para realizar las siguientes tareas:

-   Establezca la ventana de recorte.

-   Establezca los rectángulos de origen y destino.

-   Actualice la ventana de vídeo en respuesta a los mensajes de la ventana.

-   Habilite o deshabilite el modo de pantalla completa.

## <a name="clipping-window"></a>Ventana de recorte

La aplicación debe proporcionar una ventana donde la EVR dibuje el vídeo. Para establecer la ventana de recorte, llame a [**IMFVideoDisplayControl::SetVideoWindow con**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) un identificador para la ventana de la aplicación.

Si crea el receptor de medios EVR a través de su objeto de activación, este paso no es necesario. El objeto de activación llama automáticamente [**a SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow)mediante el identificador de ventana que proporcionó en la [**función MFCreateVideoRendererActivate.**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate)

## <a name="source-and-destination-rectangles"></a>Rectángulos de origen y destino

Durante la reproducción, el presentador toma una parte de la imagen de vídeo compuesta y la dibuja en un área de la ventana de vídeo. La parte de la imagen compuesta es el rectángulo *de origen* y el área de la ventana de vídeo es el rectángulo *de destino.*

El rectángulo de origen se define mediante coordenadas normalizadas donde el punto (0.0, 0.0) corresponde a la esquina superior izquierda del vídeo y (1.0, 1.0) corresponde a la esquina inferior derecha del vídeo. El rectángulo de origen puede ser cualquier región dentro de este rectángulo. El rectángulo de destino se especifica en píxeles, en relación con el área de cliente de la ventana. El rectángulo de origen predeterminado es toda la imagen y el rectángulo de destino predeterminado es un rectángulo vacío.

Para establecer los rectángulos de origen y destino, llame [**a IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Si crea el receptor de medios EVR a través de su objeto de activación, este paso no es necesario. El objeto de activación establece automáticamente el rectángulo de destino igual al área de cliente completa de la ventana. Sin embargo, debe llamar a [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) si desea cambiar el rectángulo de origen o establecer otro rectángulo de destino.

## <a name="window-messages"></a>Mensajes de ventana

Durante la reproducción, la aplicación debe responder a determinados mensajes de ventana, como se muestra a continuación:

-   WM \_ PAINT: llame [**a IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) para volver a dibujar el vídeo. Además, evite pintar sobre el rectángulo de destino mientras se reproduce el vídeo, ya que esto puede provocar parpadeo.

-   WM \_ SIZE: es posible que tenga que llamar a [**SetVideoPosition para**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) cambiar el tamaño del rectángulo de destino.

A diferencia del filtro Representador de mezcla de vídeo (VMR) de DirectShow, no es necesario notificar a evr cuando recibe un mensaje \_ DISPLAYCHANGE de WM.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Representador de vídeo mejorado](enhanced-video-renderer.md)
</dt> </dl>

 

 



