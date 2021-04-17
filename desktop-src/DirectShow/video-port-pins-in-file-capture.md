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
# <a name="video-port-pins-in-file-capture"></a><span data-ttu-id="052c3-103">PIN de puerto de vídeo en la captura de archivos</span><span class="sxs-lookup"><span data-stu-id="052c3-103">Video Port Pins in File Capture</span></span>

<span data-ttu-id="052c3-104">Si el dispositivo de captura tiene un puerto de vídeo, el PIN del puerto de vídeo debe estar conectado a un representador de vídeo, incluso si solo desea capturar en un archivo.</span><span class="sxs-lookup"><span data-stu-id="052c3-104">If the capture device has a video port, the video port pin must be connected to a video renderer, even if you only want to capture to a file.</span></span>

<span data-ttu-id="052c3-105">Si llama a [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) con la **captura de \_ categoría \_** de valor PIN y el dispositivo tiene un PIN de puerto de vídeo, el generador de gráficos de captura conecta automáticamente el PIN del puerto de vídeo al filtro de [mezclador de superposición](overlay-mixer-filter.md) y conecta el mezclador de superposición al representador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="052c3-105">If you call [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) with the value **PIN\_CATEGORY\_CAPTURE** and the device has a video port pin, the Capture Graph Builder automatically connects the video port pin to the [Overlay Mixer](overlay-mixer-filter.md) filter and connects the Overlay Mixer to the Video Renderer.</span></span> <span data-ttu-id="052c3-106">El generador de gráficos de captura oculta la ventana de vídeo llamando a [**IVideoWindow::p UT \_ Show**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) con el valor **OAFALSE**.</span><span class="sxs-lookup"><span data-stu-id="052c3-106">The Capture Graph Builder hides the video window by calling [**IVideoWindow::put\_AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) with the value **OAFALSE**.</span></span> <span data-ttu-id="052c3-107">Si posteriormente la aplicación llama a **RenderStream** con la **\_ \_ versión preliminar de la categoría PIN**, el generador de gráficos de captura llama a **Put \_ Autoshow** con el valor **OATRUE** para mostrar la ventana de vídeo.</span><span class="sxs-lookup"><span data-stu-id="052c3-107">If the application later calls **RenderStream** with **PIN\_CATEGORY\_PREVIEW**, the Capture Graph Builder calls **put\_AutoShow** with the value **OATRUE**, in order to show the video window.</span></span>

<span data-ttu-id="052c3-108">Después de llamar a **RenderStream** con la **\_ \_ captura de categoría de PIN**, puede comprobar si se ha agregado el representador de vídeo consultando el administrador de gráficos de filtros para la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) .</span><span class="sxs-lookup"><span data-stu-id="052c3-108">After you call **RenderStream** with **PIN\_CATEGORY\_CAPTURE**, you can check whether it has added the Video Renderer by querying the Filter Graph Manager for the [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="052c3-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="052c3-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="052c3-110">Capturar vídeo en un archivo</span><span class="sxs-lookup"><span data-stu-id="052c3-110">Capturing Video to a File</span></span>](capturing-video-to-a-file.md)
</dt> </dl>

 

 



