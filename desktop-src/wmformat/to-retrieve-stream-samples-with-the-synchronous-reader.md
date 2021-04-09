---
title: Para recuperar ejemplos de secuencias con el lector sincrónico
description: Para recuperar ejemplos de secuencias con el lector sincrónico
ms.assetid: d5cc4bb7-5fcf-4e1e-80dc-f03feed4dc8a
keywords:
- Advanced Systems Format (ASF), recuperar ejemplos de secuencias
- ASF (formato de sistemas avanzados), recuperar ejemplos de secuencias
- Advanced Systems Format (ASF), lectores sincrónicos
- ASF (formato de sistemas avanzados), lectores sincrónicos
- lectores sincrónicos, recuperar ejemplos de secuencias
- flujos, recuperar ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fd641dc08387606d1fdf04602e46cb9e9cbc2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104149080"
---
# <a name="to-retrieve-stream-samples-with-the-synchronous-reader"></a><span data-ttu-id="cdb4a-109">Para recuperar ejemplos de secuencias con el lector sincrónico</span><span class="sxs-lookup"><span data-stu-id="cdb4a-109">To Retrieve Stream Samples with the Synchronous Reader</span></span>

<span data-ttu-id="cdb4a-110">Al igual que el lector asincrónico, el lector sincrónico puede recuperar muestras por número de secuencia.</span><span class="sxs-lookup"><span data-stu-id="cdb4a-110">Like the asynchronous reader, the synchronous reader can retrieve samples by stream number.</span></span> <span data-ttu-id="cdb4a-111">A diferencia del lector asincrónico, el lector sincrónico puede proporcionar ejemplos de secuencias comprimidos o sin comprimir.</span><span class="sxs-lookup"><span data-stu-id="cdb4a-111">Unlike the asynchronous reader, the synchronous reader can deliver stream samples either compressed or uncompressed.</span></span>

<span data-ttu-id="cdb4a-112">Para recibir ejemplos de secuencias, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="cdb4a-112">To receive stream samples, perform the following steps.</span></span>

1.  <span data-ttu-id="cdb4a-113">En cualquier momento antes o durante la reproducción, llame a [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) pasando el número de flujo deseado.</span><span class="sxs-lookup"><span data-stu-id="cdb4a-113">Any time before or during playback, call [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) passing the desired stream number.</span></span>
2.  <span data-ttu-id="cdb4a-114">Recupere ejemplos con llamadas continuas a [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="cdb4a-114">Retrieve samples with continued calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span>

<span data-ttu-id="cdb4a-115">Puede comprobar si se ha seleccionado una secuencia para la entrega de ejemplo llamando a [**IWMSyncReader:: GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).</span><span class="sxs-lookup"><span data-stu-id="cdb4a-115">You can check whether a stream is selected for sample delivery by calling [**IWMSyncReader::GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cdb4a-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cdb4a-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cdb4a-117">**Interfaz IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="cdb4a-117">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="cdb4a-118">**Leer archivos con el lector sincrónico**</span><span class="sxs-lookup"><span data-stu-id="cdb4a-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




