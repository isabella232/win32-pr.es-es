---
title: Captura de fotogramas manual
description: Captura de fotogramas manual
ms.assetid: 7c5576ff-2694-4f44-a386-03bbc6f9c2ed
keywords:
- Mensaje WM_CAP_SINGLE_FRAME_OPEN
- Mensaje WM_CAP_SINGLE_FRAME
- Mensaje WM_CAP_SINGLE_FRAME_CLOSE
- capCaptureSingleFrameOpen (macro)
- capCaptureSingleFrame (macro)
- capCaptureSingleFrameClose (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26899032d8e81be437e8f29acf36f0a37703c560
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903335"
---
# <a name="manual-frame-capture"></a><span data-ttu-id="e60d9-109">Captura de fotogramas manual</span><span class="sxs-lookup"><span data-stu-id="e60d9-109">Manual Frame Capture</span></span>

<span data-ttu-id="e60d9-110">Si desea especificar de forma individual los fotogramas que se van a capturar en una secuencia de vídeo, puede controlar la secuencia mediante el uso de los mensajes de cierre de fotograma único de [**Cap de WM \_ \_ \_ \_ abierto**](wm-cap-single-frame-open.md), de [](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) [**\_ límite \_ único \_**](wm-cap-single-frame.md)de la Cap de WM y de [**\_ \_ \_ \_ cierre de trama único**](wm-cap-single-frame-close.md) de la Cap de WM (o las macros capCaptureSingleFrameOpen, [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe)y [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) ).</span><span class="sxs-lookup"><span data-stu-id="e60d9-110">If you want to individually specify the frames to capture in a video stream, you can control the sequence by using the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md), [**WM\_CAP\_SINGLE\_FRAME**](wm-cap-single-frame.md), and [**WM\_CAP\_SINGLE\_FRAME\_CLOSE**](wm-cap-single-frame-close.md) messages (or the [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen), [**capCaptureSingleFrame**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe), and [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) macros).</span></span> <span data-ttu-id="e60d9-111">Normalmente, estos mensajes se utilizan para crear la animación anexando fotogramas individuales al archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="e60d9-111">Typically, these messages are used to create animation by appending individual frames to the capture file.</span></span> <span data-ttu-id="e60d9-112">\_ \_ \_ \_ La apertura de un fotograma de Cap de WM abre un archivo para una operación de captura controlada manualmente.</span><span class="sxs-lookup"><span data-stu-id="e60d9-112">WM\_CAP\_SINGLE\_FRAME\_OPEN opens a file for a manually driven capture operation.</span></span> <span data-ttu-id="e60d9-113">\_El marco único de Cap de WM \_ \_ captura un fotograma individual y lo anexa al archivo de captura.</span><span class="sxs-lookup"><span data-stu-id="e60d9-113">WM\_CAP\_SINGLE\_FRAME captures an individual frame and appends it to the capture file.</span></span> <span data-ttu-id="e60d9-114">\_ \_ \_ Cierre de trama único \_ de Cap de WM cierra el archivo que se usa para la captura de fotogramas manual.</span><span class="sxs-lookup"><span data-stu-id="e60d9-114">WM\_CAP\_SINGLE\_FRAME\_CLOSE closes the file used for manual frame capture.</span></span>

> [!Note]  
> <span data-ttu-id="e60d9-115">Este método de captura no admite la captura de audio simultánea con la captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e60d9-115">This capture method does not support simultaneous audio capture with video capture.</span></span>

 

 

 




