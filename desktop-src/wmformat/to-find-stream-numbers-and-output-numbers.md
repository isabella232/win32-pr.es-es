---
title: Para buscar números de secuencia y números de salida
description: Para buscar números de secuencia y números de salida
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- Advanced Systems Format (ASF), números de secuencia
- ASF (formato de sistemas avanzados), crear números
- Advanced Systems Format (ASF), buscar números de salida
- ASF (formato de sistemas avanzados), buscar números de salida
- lectores sincrónicos, números de secuencia
- lectores sincrónicos, buscar números de salida
- flujos, buscar números
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4bdf10eaeb95f981ab2972ba56ad09b867cd99
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788739"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a><span data-ttu-id="e9235-110">Para buscar números de secuencia y números de salida</span><span class="sxs-lookup"><span data-stu-id="e9235-110">To Find Stream Numbers and Output Numbers</span></span>

<span data-ttu-id="e9235-111">El lector sincrónico admite el cambio más simplificado entre los números de flujo y de salida para la reproducción que el lector asincrónico.</span><span class="sxs-lookup"><span data-stu-id="e9235-111">The synchronous reader supports more simplified switching between stream and output numbers for playback than the asynchronous reader.</span></span> <span data-ttu-id="e9235-112">Por lo tanto, es más importante poder encontrar qué números de secuencia son equivalentes a los números de salida, o viceversa.</span><span class="sxs-lookup"><span data-stu-id="e9235-112">It is therefore more important to be able to find which stream numbers equate to which output numbers, or the other way around.</span></span>

<span data-ttu-id="e9235-113">Para buscar el número de salida que corresponde a un número de secuencia, llame a [**IWMSyncReader:: GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).</span><span class="sxs-lookup"><span data-stu-id="e9235-113">To find the output number that corresponds to a stream number, call [**IWMSyncReader::GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).</span></span>

<span data-ttu-id="e9235-114">Para buscar el número de secuencia que corresponde a un número de salida, llame a [ **IWMSyncReader:: GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)</span><span class="sxs-lookup"><span data-stu-id="e9235-114">To find the stream number that corresponds to an output number, call [**IWMSyncReader::GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)</span></span>

## <a name="related-topics"></a><span data-ttu-id="e9235-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e9235-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e9235-116">**Interfaz IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="e9235-116">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="e9235-117">**Entradas, secuencias y salidas**</span><span class="sxs-lookup"><span data-stu-id="e9235-117">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="e9235-118">**Leer archivos con el lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="e9235-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




