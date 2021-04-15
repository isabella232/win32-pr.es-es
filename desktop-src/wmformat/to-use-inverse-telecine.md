---
title: Para el uso de telecine inverso
description: Para el uso de telecine inverso
ms.assetid: 7752d1ac-34b1-446a-a69c-29463c9e10f7
keywords:
- Windows Media Format SDK, Telecine inverso
- SDK de Windows Media Format, telecine
- Advanced Systems Format (ASF), Telecine inverso
- ASF (formato de sistemas avanzados), Telecine inverso
- Advanced Systems Format (ASF), telecine
- ASF (formato de sistemas avanzados), telecine
- Telecine inverso
- Telecine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4f4e3ae34c2a9efcaa4fe8e5ce7256474404
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "105695572"
---
# <a name="to-use-inverse-telecine"></a><span data-ttu-id="4249a-111">Para el uso de telecine inverso</span><span class="sxs-lookup"><span data-stu-id="4249a-111">To Use Inverse Telecine</span></span>

<span data-ttu-id="4249a-112">Telecine es el proceso de convertir película, que tiene 24 fotogramas por segundo, en vídeo, que tiene 60 campos (medio fotogramas) por segundo.</span><span class="sxs-lookup"><span data-stu-id="4249a-112">Telecine is the process of converting film, which has 24 frames per second, to video, which has 60 fields (half frames) per second.</span></span> <span data-ttu-id="4249a-113">Este proceso coloca las imágenes de cada fotograma de la película en varios campos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="4249a-113">This process puts images from each film frame in multiple video fields.</span></span>

<span data-ttu-id="4249a-114">Al codificar digitalmente un vídeo que se creó a partir de una película mediante telecine, el proceso de compresión puede producir artefactos de movimiento y otras disminuciones de calidad.</span><span class="sxs-lookup"><span data-stu-id="4249a-114">When you digitally encode a video that was created from film by using telecine, the compression process can cause motion artifacts and other degradations in quality.</span></span> <span data-ttu-id="4249a-115">Para evitar que afecte a la calidad de la salida digital, el códec de Windows Media Video 9 admite telecine inversa.</span><span class="sxs-lookup"><span data-stu-id="4249a-115">To avoid affecting the quality of the digital output, the Windows Media Video 9 codec supports inverse telecine.</span></span> <span data-ttu-id="4249a-116">Cuando se usa Telecine inverso, el códec reconstruye los fotogramas de la película 24 originales por segundo del vídeo de entrada antes de codificar el contenido.</span><span class="sxs-lookup"><span data-stu-id="4249a-116">When using inverse telecine, the codec reconstructs the original 24 film frames per second from the input video before encoding the content.</span></span>

<span data-ttu-id="4249a-117">Para usar telecine inversa, debe:</span><span class="sxs-lookup"><span data-stu-id="4249a-117">To use inverse telecine, you must:</span></span>

-   <span data-ttu-id="4249a-118">Use un perfil con una secuencia de vídeo establecida en 24 fotogramas por segundo.</span><span class="sxs-lookup"><span data-stu-id="4249a-118">Use a profile with a video stream set to 24 frames per second.</span></span>
-   <span data-ttu-id="4249a-119">Conozca la configuración de campo del vídeo de entrada.</span><span class="sxs-lookup"><span data-stu-id="4249a-119">Know the field configuration of the input video.</span></span>

<span data-ttu-id="4249a-120">Para usar telecine inversa para una entrada al escritor, realice los pasos siguientes.</span><span class="sxs-lookup"><span data-stu-id="4249a-120">To use inverse telecine for an input to the writer, perform the following steps.</span></span>

1.  <span data-ttu-id="4249a-121">Configure el escritor como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="4249a-121">Set up the writer as usual.</span></span> <span data-ttu-id="4249a-122">Para obtener más información, consulte [Writing ASF files](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="4249a-122">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="4249a-123">Antes de empezar a escribir ejemplos, obtenga un puntero a la interfaz [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) llamando a **IWMWriter:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="4249a-123">Before beginning to write samples, obtain a pointer to the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface by calling **IWMWriter::QueryInterface**.</span></span>
3.  <span data-ttu-id="4249a-124">Identifique la secuencia que se va a reconstruir mediante una llamada a [**IWMWriterAdvanced2:: SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) para el número de entrada deseado.</span><span class="sxs-lookup"><span data-stu-id="4249a-124">Identify the stream to be reconstructed by calling [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) for the desired input number.</span></span> <span data-ttu-id="4249a-125">Pase g \_ wszDeinterlaceMode como la configuración y WM \_ DM \_ desentrelazado \_ INVERSETELECINE como valor.</span><span class="sxs-lookup"><span data-stu-id="4249a-125">Pass g\_wszDeinterlaceMode as the setting and WM\_DM\_DEINTERLACE\_INVERSETELECINE as the value.</span></span>
4.  <span data-ttu-id="4249a-126">Vuelva a llamar a **SetInputSetting** para establecer g \_ wszInitialPatternForInverseTelecine.</span><span class="sxs-lookup"><span data-stu-id="4249a-126">Call **SetInputSetting** again to set g\_wszInitialPatternForInverseTelecine.</span></span>
5.  <span data-ttu-id="4249a-127">Escriba el archivo como de costumbre.</span><span class="sxs-lookup"><span data-stu-id="4249a-127">Write the file as usual.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4249a-128">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4249a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4249a-129">**Temas avanzados**</span><span class="sxs-lookup"><span data-stu-id="4249a-129">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="4249a-130">**Interfaz IWMWriter**</span><span class="sxs-lookup"><span data-stu-id="4249a-130">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="4249a-131">**Interfaz IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="4249a-131">**IWMWriterAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2)
</dt> </dl>

 

 




