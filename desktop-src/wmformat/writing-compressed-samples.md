---
title: Escribir ejemplos comprimidos
description: Escribir ejemplos comprimidos
ms.assetid: f85ca719-1b9d-404f-b2b1-c9e3524e4bc6
keywords:
- Advanced Systems Format (ASF), escribir ejemplos comprimidos
- ASF (formato de sistemas avanzados), escribir ejemplos comprimidos
- Advanced Systems Format (ASF), pasar ejemplos comprimidos
- ASF (formato de sistemas avanzados), pasar ejemplos comprimidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c43fed30aa89e83c157479257e78fbab4acd98
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104487287"
---
# <a name="writing-compressed-samples"></a><span data-ttu-id="138be-107">Escribir ejemplos comprimidos</span><span class="sxs-lookup"><span data-stu-id="138be-107">Writing Compressed Samples</span></span>

<span data-ttu-id="138be-108">En el caso de algunas secuencias de audio o vídeo, es posible que desee pasar muestras que ya estén comprimidas en lugar de pasar datos sin procesar.</span><span class="sxs-lookup"><span data-stu-id="138be-108">For some audio or video streams, you may want to pass samples that are already compressed instead of passing raw data.</span></span> <span data-ttu-id="138be-109">Esta característica se usa para copiar un flujo existente o escribir ejemplos comprimidos con un códec de terceros.</span><span class="sxs-lookup"><span data-stu-id="138be-109">This feature is used to copy an existing stream or to write samples compressed with a third-party codec.</span></span> <span data-ttu-id="138be-110">El proceso de escritura de un ejemplo comprimido es idéntico al de escribir un ejemplo sin comprimir, salvo que se usa [**IWMWriterAdvanced:: WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) en lugar de [**IWMWriter:: WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span><span class="sxs-lookup"><span data-stu-id="138be-110">The process of writing a compressed sample is identical to writing an uncompressed sample, except that you use [**IWMWriterAdvanced::WriteStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) instead of [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span></span> <span data-ttu-id="138be-111">Para obtener más información sobre cómo escribir ejemplos sin comprimir, vea [para escribir ejemplos](to-write-samples.md).</span><span class="sxs-lookup"><span data-stu-id="138be-111">For more information about writing uncompressed samples, see [To Write Samples](to-write-samples.md).</span></span>

<span data-ttu-id="138be-112">Al escribir ejemplos comprimidos, para perfiles CBR, el escritor quitará algunos ejemplos, si es necesario, para mantener el contenido dentro de la velocidad de bits y los valores de la ventana de búfer especificados.</span><span class="sxs-lookup"><span data-stu-id="138be-112">When you write compressed samples, for CBR profiles, the writer will drop some samples, if necessary, to keep the content within the specified bit rate and buffer window values.</span></span> <span data-ttu-id="138be-113">En el caso de VBR, el sistema de escritura no quitará los ejemplos, pero no hay ninguna manera de asegurarse de que los valores de velocidad de bits y de la ventana de búfer serán correctos.</span><span class="sxs-lookup"><span data-stu-id="138be-113">For VBR, the writer will not drop samples, but there is no way to be sure that the bit rate and buffer window values will be correct.</span></span>

<span data-ttu-id="138be-114">Si va a copiar una secuencia de un archivo a otro, debe copiar siempre el objeto de configuración de secuencia del perfil del archivo original en el perfil del nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="138be-114">If you are copying a stream from one file to another, you should always copy the stream configuration object from the profile of the original file to the profile of the new file.</span></span> <span data-ttu-id="138be-115">Esto garantiza que tenga la información de la ventana de búfer y la velocidad de bits correcta.</span><span class="sxs-lookup"><span data-stu-id="138be-115">This ensures that you have the correct bit rate and buffer window information.</span></span> <span data-ttu-id="138be-116">Si copia un flujo comprimido en una secuencia que tiene un conjunto de ventanas de búfer inferior, se quitarán los ejemplos durante la escritura del archivo.</span><span class="sxs-lookup"><span data-stu-id="138be-116">If you copy a compressed stream to a stream that has a lower buffer window set, samples will be dropped during file writing.</span></span>

## <a name="related-topics"></a><span data-ttu-id="138be-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="138be-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="138be-118">**Escribir archivos ASF**</span><span class="sxs-lookup"><span data-stu-id="138be-118">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




