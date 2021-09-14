---
description: Anclar puertos de vídeo en la captura de archivos
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: Anclar puertos de vídeo en la captura de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2361c5a7cdaa7640ece9724000963f39f3f77ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127272911"
---
# <a name="video-port-pins-in-file-capture"></a>Anclar puertos de vídeo en la captura de archivos

Si el dispositivo de captura tiene un puerto de vídeo, el pin de puerto de vídeo debe estar conectado a un representador de vídeo, incluso si solo desea capturar en un archivo.

Si llama a [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con el valor **PIN CATEGORY \_ \_ CAPTURE** y el dispositivo tiene un pin de puerto de vídeo, Capture Graph Builder conecta automáticamente el pin de puerto de vídeo al filtro [Overlay Mixer](overlay-mixer-filter.md) y conecta el Mixer overlay al representador de vídeo. El Generador de Graph captura oculta la ventana de vídeo mediante una llamada a [**IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con el valor **OAFALSE**. Si la aplicación llama más adelante a **RenderStream** con **PIN CATEGORY \_ \_ PREVIEW**, las llamadas a Capture Graph Builder ponen **\_ AutoShow** con el valor **OATRUE** para mostrar la ventana de vídeo.

Después de llamar a **RenderStream** con **PIN CATEGORY \_ \_ CAPTURE**, puede comprobar si ha agregado el representador de vídeo consultando el Administrador de filtros Graph para la [**interfaz IVideoWindow.**](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Capturar vídeo en un archivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



