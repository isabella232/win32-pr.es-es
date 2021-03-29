---
title: Tamaño de índice
description: Tamaño de índice
ms.assetid: 7902589d-5e08-4c0c-9a22-82d28ad2677e
keywords:
- Mensaje WM_CAP_GET_SEQUENCE_SETUP
- capCaptureGetSetup (macro)
- Mensaje WM_CAP_SET_SEQUENCE_SETUP
- capCaptureSetSetup (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cd9e59c23376a7aa201673ef71743c8a192b60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777119"
---
# <a name="index-size"></a><span data-ttu-id="cc372-107">Tamaño de índice</span><span class="sxs-lookup"><span data-stu-id="cc372-107">Index Size</span></span>

<span data-ttu-id="cc372-108">Cada archivo AVI utiliza un índice de un tamaño especificado para buscar fragmentos de datos de vídeo y audio dentro del archivo.</span><span class="sxs-lookup"><span data-stu-id="cc372-108">Each AVI file uses an index of a specified size to locate video and audio data chunks within the file.</span></span> <span data-ttu-id="cc372-109">Una entrada en el índice busca un fotograma de vídeo o un búfer de audio de onda.</span><span class="sxs-lookup"><span data-stu-id="cc372-109">An entry in the index locates one video frame or waveform-audio buffer.</span></span> <span data-ttu-id="cc372-110">Por consiguiente, el valor del tamaño del índice establece indirectamente el límite superior del número de fotogramas que se pueden capturar en un archivo.</span><span class="sxs-lookup"><span data-stu-id="cc372-110">Consequently, the value of the index size indirectly sets the upper limit on the number of frames that can be captured in a file.</span></span>

<span data-ttu-id="cc372-111">Puede recuperar el tamaño del índice actual mediante el mensaje de configuración de la [**\_ \_ \_ \_ secuencia Get Cap de WM**](wm-cap-get-sequence-setup.md) (o la macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="cc372-111">You can retrieve the current index size by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="cc372-112">El tamaño actual del índice se almacena en el miembro **dwIndexSize** de la estructura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="cc372-112">The current index size is stored in the **dwIndexSize** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="cc372-113">Puede especificar un nuevo tamaño de índice como el valor de **dwIndexSize** y, a continuación, enviar la estructura **CAPTUREPARMS** actualizada a la ventana de captura mediante el mensaje de configuración de la secuencia del conjunto de límites de WM (o la macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ). [**\_ \_ \_ \_**](wm-cap-set-sequence-setup.md)</span><span class="sxs-lookup"><span data-stu-id="cc372-113">You can specify a new index size as the value of **dwIndexSize** and then send the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="cc372-114">El tamaño de índice predeterminado es 34.952 entradas (que permiten fotogramas de 32 KB y un número proporcional de búferes de audio).</span><span class="sxs-lookup"><span data-stu-id="cc372-114">The default index size is 34,952 entries (allowing 32K frames and a proportional number of audio buffers).</span></span>

 

 




