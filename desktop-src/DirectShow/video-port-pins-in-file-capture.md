---
description: Anclar puertos de vídeo en la captura de archivos
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: Anclar puertos de vídeo en la captura de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab348c7e378f4130b43eef45f2cf4ddd079b0e85a77397b767cadddde5a7d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049385"
---
# <a name="video-port-pins-in-file-capture"></a>Anclar puertos de vídeo en la captura de archivos

Si el dispositivo de captura tiene un puerto de vídeo, el pin de puerto de vídeo debe estar conectado a un representador de vídeo, incluso si solo desea capturar en un archivo.

Si llama a [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con el valor **PIN CATEGORY \_ \_ CAPTURE** y el dispositivo tiene un pin de puerto de vídeo, Capture Graph Builder conecta automáticamente el pin de puerto de vídeo al filtro [Overlay Mixer](overlay-mixer-filter.md) y conecta el Mixer de superposición al representador de vídeo. El Generador Graph captura oculta la ventana de vídeo mediante una llamada a [**IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con el valor **OAFALSE**. Si la aplicación llama posteriormente a **RenderStream** con **PIN CATEGORY \_ \_ PREVIEW**, las llamadas a Capture Graph Builder ponen **\_ AutoShow** con el valor **OATRUE** para mostrar la ventana de vídeo.

Después de llamar a **RenderStream** con **PIN CATEGORY \_ \_ CAPTURE**, puede comprobar si ha agregado el representador de vídeo consultando el Administrador de filtros Graph para la [**interfaz IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Captura de vídeo en un archivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



