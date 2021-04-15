---
title: DoProcessOutput en el complemento DSP de vídeo de ejemplo
description: DoProcessOutput en el complemento DSP de vídeo de ejemplo
ms.assetid: 67536e35-a049-49c8-bd89-fad1fab37e6c
keywords:
- Complementos de Windows Media Player, DSP de vídeo
- complementos, DSP de vídeo
- Complementos de procesamiento de señal digital, DoProcessOutput
- Complementos DSP, DoProcessOutput
- Complementos de DSP de vídeo, DoProcessOutput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff3bc844890930209a1c6007213d3c466f0cd15b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695248"
---
# <a name="doprocessoutput-in-the-sample-video-dsp-plug-in"></a><span data-ttu-id="7ea90-108">DoProcessOutput en el complemento DSP de vídeo de ejemplo</span><span class="sxs-lookup"><span data-stu-id="7ea90-108">DoProcessOutput in the Sample Video DSP Plug-in</span></span>

<span data-ttu-id="7ea90-109">Dado que un complemento de DSP de vídeo suele admitir varios formatos de vídeo, es conveniente separar el código de implementación de procesamiento en una función independiente para cada formato.</span><span class="sxs-lookup"><span data-stu-id="7ea90-109">Because a video DSP plug-in typically supports several video formats, it is convenient to separate the processing implementation code into a separate function for each format.</span></span> <span data-ttu-id="7ea90-110">Esto significa que la implementación de **DoProcessOutput** para complementos de DSP de vídeo es relativamente sencilla.</span><span class="sxs-lookup"><span data-stu-id="7ea90-110">This means that the implementation of **DoProcessOutput** for video DSP plug-ins is relatively simple.</span></span>

<span data-ttu-id="7ea90-111">La implementación en el complemento de ejemplo comprueba primero si el usuario ha habilitado el complemento.</span><span class="sxs-lookup"><span data-stu-id="7ea90-111">The implementation in the sample plug-in first tests whether the user has enabled the plug-in.</span></span> <span data-ttu-id="7ea90-112">Si el complemento está deshabilitado, el código copia los datos proporcionados en el búfer de entrada en el búfer de salida sin cambiarlo, como se muestra en el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="7ea90-112">If the plug-in is disabled, the code copies the data provided in the input buffer to the output buffer without changing it, as the following code demonstrates:</span></span>


```C++
// Test whether the plug-in has been disabled by the user.
if (!m_bEnabled)
{
    // Just copy the data without changing it. You should
    // also do any necessary format conversion here.
    memcpy(pbOutputData, pbInputData, m_dwBufferSize);
    *cbBytesProcessed = m_dwBufferSize;

    return S_OK;
}

```



<span data-ttu-id="7ea90-113">Si el complemento está habilitado, el código simplemente realiza una serie de comprobaciones en el miembro de **subtipo** de tipo de medio de entrada para determinar el formato de vídeo actual.</span><span class="sxs-lookup"><span data-stu-id="7ea90-113">If the plug-in is enabled, the code simply performs a series of checks on the input media type **subtype** member to determine the current video format.</span></span> <span data-ttu-id="7ea90-114">Cuando se encuentra una coincidencia, el código llama a la función de procesamiento adecuada.</span><span class="sxs-lookup"><span data-stu-id="7ea90-114">When a match is found, the code calls the appropriate processing function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ea90-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7ea90-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ea90-116">**Implementación de un complemento DSP de vídeo**</span><span class="sxs-lookup"><span data-stu-id="7ea90-116">**Implementing a Video DSP Plug-in**</span></span>](implementing-a-video-dsp-plug-in.md)
</dt> </dl>

 

 




