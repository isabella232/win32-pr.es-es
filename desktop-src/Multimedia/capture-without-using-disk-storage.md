---
title: Capturar sin usar Disk Storage
description: Capturar sin usar Disk Storage
ms.assetid: 2e2f1b67-69be-424c-8a6f-d9db5eeb6088
keywords:
- Mensaje WM_CAP_SEQUENCE_NOFILE
- capCaptureSequenceNoFile (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76fa69fa8a827117dbc110a410cb40084614559
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105651294"
---
# <a name="capture-without-using-disk-storage"></a><span data-ttu-id="8a079-105">Capturar sin usar Disk Storage</span><span class="sxs-lookup"><span data-stu-id="8a079-105">Capture Without Using Disk Storage</span></span>

<span data-ttu-id="8a079-106">Puede usar los servicios de captura sin escribir los datos en un archivo de disco mediante el mensaje [**\_ \_ \_ nofile Sequence**](wm-cap-sequence-nofile.md) de la secuencia de Cap de WM (o la macro [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) ).</span><span class="sxs-lookup"><span data-stu-id="8a079-106">You can use capture services without writing the data to a disk file by using the [**WM\_CAP\_SEQUENCE\_NOFILE**](wm-cap-sequence-nofile.md) message (or the [**capCaptureSequenceNoFile**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequencenofile) macro).</span></span> <span data-ttu-id="8a079-107">Este mensaje solo es útil junto con las funciones de devolución de llamada que permiten que la aplicación use los datos de vídeo y audio directamente.</span><span class="sxs-lookup"><span data-stu-id="8a079-107">This message is useful only in conjunction with callback functions that allow your application to use the video and audio data directly.</span></span> <span data-ttu-id="8a079-108">Por ejemplo, las aplicaciones de videoconferencia podrían usar este mensaje para obtener fotogramas de vídeo en streaming.</span><span class="sxs-lookup"><span data-stu-id="8a079-108">For example, videoconferencing applications might use this message to obtain streaming video frames.</span></span> <span data-ttu-id="8a079-109">Las funciones de devolución de llamada transferirían las imágenes capturadas al equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="8a079-109">The callback functions would transfer the captured images to the remote computer.</span></span>

 

 




