---
description: Procesamiento de entrada y salida de MFT de códecs
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: Procesamiento de entrada y salida de MFT de códecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af3a16fa1855574f1b7618bc0d41bf85c15412f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275823"
---
# <a name="processing-codec-mft-input-and-output"></a><span data-ttu-id="c02b8-103">Procesamiento de entrada y salida de MFT de códecs</span><span class="sxs-lookup"><span data-stu-id="c02b8-103">Processing Codec MFT Input and Output</span></span>

<span data-ttu-id="c02b8-104">Cuando haya configurado el tipo de entrada y el tipo de salida de una MFT, puede empezar a procesar las muestras de datos.</span><span class="sxs-lookup"><span data-stu-id="c02b8-104">When you have configured the input type and output type for an MFT, you can begin processing data samples.</span></span> <span data-ttu-id="c02b8-105">Pase ejemplos a la MFT para su procesamiento mediante el método [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) y, a continuación, recupere el ejemplo procesado llamando a [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="c02b8-105">You pass samples to the MFT for processing by using the [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method, and then retrieve the processed sample by calling [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="c02b8-106">Debe establecer las marcas de tiempo y duraciones precisas para todos los ejemplos de entrada pasados.</span><span class="sxs-lookup"><span data-stu-id="c02b8-106">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="c02b8-107">Las marcas de tiempo no son estrictamente necesarias pero ayudan a mantener la sincronización de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="c02b8-107">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="c02b8-108">Si no dispone de las marcas de tiempo para los ejemplos, es mejor dejarlas de usar valores inciertos.</span><span class="sxs-lookup"><span data-stu-id="c02b8-108">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c02b8-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c02b8-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c02b8-110">Trabajar con códec MFTs</span><span class="sxs-lookup"><span data-stu-id="c02b8-110">Working with Codec MFTs</span></span>](workingwithcodecmfts.md)
</dt> </dl>

 

 



