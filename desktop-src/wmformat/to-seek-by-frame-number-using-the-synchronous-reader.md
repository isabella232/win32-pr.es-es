---
title: Para buscar por número de marco mediante el lector sincrónico
description: Para buscar por número de marco mediante el lector sincrónico
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- Advanced Systems Format (ASF), búsqueda por números de fotogramas
- ASF (formato de sistemas avanzados), búsqueda por números de fotogramas
- Advanced Systems Format (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- lectores sincrónicos, búsquedas por números de fotogramas
- secuencias de vídeo, búsqueda por números de fotogramas
- secuencias de vídeo, lectores sincrónicos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c26711d2d839e47279e7e52a50f5dc82c6e81da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104358684"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a><span data-ttu-id="2d8f2-110">Para buscar por número de marco mediante el lector sincrónico</span><span class="sxs-lookup"><span data-stu-id="2d8f2-110">To Seek By Frame Number Using the Synchronous Reader</span></span>

<span data-ttu-id="2d8f2-111">Para buscar datos por número de marco mediante el lector sincrónico, especifique un intervalo para la reproducción.</span><span class="sxs-lookup"><span data-stu-id="2d8f2-111">To seek for data by frame number using the synchronous reader, you specify a range for playback.</span></span> <span data-ttu-id="2d8f2-112">Un intervalo se define mediante un número de fotograma inicial en un flujo de vídeo específico y un número de fotogramas que se van a reproducir.</span><span class="sxs-lookup"><span data-stu-id="2d8f2-112">A range is defined by a starting frame number in a specific video stream and a number of frames to play.</span></span>

<span data-ttu-id="2d8f2-113">Para buscar datos en un archivo ASF por número de marco mediante el lector sincrónico, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="2d8f2-113">To seek data in an ASF file by frame number using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="2d8f2-114">Establezca el número de fotograma inicial y el número de fotogramas que se van a leer para la entrega de ejemplo llamando a [**IWMSyncReader:: SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span><span class="sxs-lookup"><span data-stu-id="2d8f2-114">Set the starting frame number and number of frames to read for sample delivery by calling [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span></span> <span data-ttu-id="2d8f2-115">Debe especificar el número de secuencia de una secuencia de vídeo indexada por fotogramas.</span><span class="sxs-lookup"><span data-stu-id="2d8f2-115">You must specify the stream number of a frame-indexed video stream.</span></span> <span data-ttu-id="2d8f2-116">El lector sincronizará el resto de los resultados con el tiempo de presentación del marco especificado de la secuencia especificada y comenzará a entregar ejemplos de salida.</span><span class="sxs-lookup"><span data-stu-id="2d8f2-116">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
2.  <span data-ttu-id="2d8f2-117">Comience a recuperar ejemplos con llamadas a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="2d8f2-117">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="2d8f2-118">Continúe como lo haría normalmente con el lector sincrónico.</span><span class="sxs-lookup"><span data-stu-id="2d8f2-118">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d8f2-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d8f2-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d8f2-120">**Interfaz IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="2d8f2-120">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="2d8f2-121">**Leer archivos con el lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="2d8f2-121">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




