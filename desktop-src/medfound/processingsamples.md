---
description: Procesamiento de entradas y salidas de códecs DMO
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: Procesamiento de entradas y salidas de códecs DMO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c6781d877f4c863161537fcc5b6a746691cfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360481"
---
# <a name="processing-codec-dmo-input-and-output"></a><span data-ttu-id="da20c-103">Procesamiento de entradas y salidas de códecs DMO</span><span class="sxs-lookup"><span data-stu-id="da20c-103">Processing Codec DMO Input and Output</span></span>

<span data-ttu-id="da20c-104">Cuando haya configurado el tipo de entrada y de salida para un DMO, puede empezar a procesar los ejemplos de datos.</span><span class="sxs-lookup"><span data-stu-id="da20c-104">When you have configured the input type and output type for a DMO, you can begin processing data samples.</span></span> <span data-ttu-id="da20c-105">Pase ejemplos a DMO para su procesamiento mediante el método **IMediaObject::P rocessinput** y, a continuación, recupere el ejemplo procesado llamando a **IMediaObject::P rocessoutput**.</span><span class="sxs-lookup"><span data-stu-id="da20c-105">You pass samples to the DMO for processing using the **IMediaObject::ProcessInput** method, and then retrieve the processed sample by calling **IMediaObject::ProcessOutput**.</span></span> <span data-ttu-id="da20c-106">Debe establecer las marcas de tiempo y duraciones precisas para todos los ejemplos de entrada pasados.</span><span class="sxs-lookup"><span data-stu-id="da20c-106">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="da20c-107">Las marcas de tiempo no son estrictamente necesarias pero ayudan a mantener la sincronización de audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="da20c-107">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="da20c-108">Si no dispone de las marcas de tiempo para los ejemplos, es mejor dejarlas de usar valores inciertos.</span><span class="sxs-lookup"><span data-stu-id="da20c-108">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="related-topics"></a><span data-ttu-id="da20c-109">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="da20c-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da20c-110">Trabajar con códec DMOs</span><span class="sxs-lookup"><span data-stu-id="da20c-110">Working with Codec DMOs</span></span>](workingwithcodecdmos.md)
</dt> </dl>

 

 



