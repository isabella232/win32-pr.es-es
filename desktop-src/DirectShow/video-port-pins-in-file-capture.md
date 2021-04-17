---
description: PIN de puerto de vídeo en la captura de archivos
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: PIN de puerto de vídeo en la captura de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2361c5a7cdaa7640ece9724000963f39f3f77ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677541"
---
# <a name="video-port-pins-in-file-capture"></a>PIN de puerto de vídeo en la captura de archivos

Si el dispositivo de captura tiene un puerto de vídeo, el PIN del puerto de vídeo debe estar conectado a un representador de vídeo, incluso si solo desea capturar en un archivo.

Si llama a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con la **captura de \_ categoría \_** de valor PIN y el dispositivo tiene un PIN de puerto de vídeo, el generador de gráficos de captura conecta automáticamente el PIN del puerto de vídeo al filtro de [mezclador de superposición](overlay-mixer-filter.md) y conecta el mezclador de superposición al representador de vídeo. El generador de gráficos de captura oculta la ventana de vídeo llamando a [**IVideoWindow::p UT \_ Show**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con el valor **OAFALSE**. Si posteriormente la aplicación llama a **RenderStream** con la **\_ \_ versión preliminar de la categoría PIN**, el generador de gráficos de captura llama a **Put \_ Autoshow** con el valor **OATRUE** para mostrar la ventana de vídeo.

Después de llamar a **RenderStream** con la **\_ \_ captura de categoría de PIN**, puede comprobar si se ha agregado el representador de vídeo consultando el administrador de gráficos de filtros para la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Capturar vídeo en un archivo](capturing-video-to-a-file.md)
</dt> </dl>

 

 



