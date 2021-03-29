---
title: Para la compatibilidad con varios idiomas
description: Para la compatibilidad con varios idiomas
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- SDK de Windows Media Format, compatible con varios idiomas
- SDK de Windows Media Format, compatibilidad con varios idiomas
- SDK de Windows Media Format, compatibilidad con idiomas
- Advanced Systems Format (ASF), compatible con varios idiomas
- ASF (formato de sistemas avanzados), compatible con varios idiomas
- Advanced Systems Format (ASF), compatibilidad con varios idiomas
- ASF (formato de sistemas avanzados), compatibilidad con varios idiomas
- Advanced Systems Format (ASF), compatibilidad con idiomas
- ASF (formato de sistemas avanzados), compatibilidad con idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc070bda1cc25c6b7fd0fa583a8ac63a55fa603
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103995022"
---
# <a name="to-support-multiple-languages"></a><span data-ttu-id="eb3e1-112">Para la compatibilidad con varios idiomas</span><span class="sxs-lookup"><span data-stu-id="eb3e1-112">To Support Multiple Languages</span></span>

<span data-ttu-id="eb3e1-113">Puede admitir varios lenguajes en streams y en metadatos.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-113">You can support multiple languages both in streams and in metadata.</span></span> <span data-ttu-id="eb3e1-114">El núcleo de la compatibilidad con varios idiomas en el SDK de Windows Media Format es la interfaz [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) , que mantiene una lista de los idiomas admitidos.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-114">The core of multiple language support in the Windows Media Format SDK is the [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) interface, which maintains a list of the languages supported.</span></span> <span data-ttu-id="eb3e1-115">La lista de idiomas proporciona a cada idioma compatible un índice, que se usa en varios objetos del SDK cuando se trabaja con varios idiomas.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-115">The language list gives each supported language an index, which is used in various objects in the SDK when dealing with the multiple languages.</span></span>

<span data-ttu-id="eb3e1-116">El método [**IWMLanguageList:: AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) agrega un idioma a la lista.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-116">The [**IWMLanguageList::AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) method adds a language to the list.</span></span> <span data-ttu-id="eb3e1-117">Puede identificar los idiomas que ya están en la lista obteniendo el número total de idiomas con [**IWMLanguageList:: GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) y, a continuación, recorrer en bucle los lenguajes que llaman a [**IWMLanguageList:: GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) para cada uno.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-117">You can identify the languages already in the list by obtaining the total number of languages with [**IWMLanguageList::GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) and then looping through the languages calling [**IWMLanguageList::GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) for each.</span></span> <span data-ttu-id="eb3e1-118">El índice de idioma está basado en cero.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-118">The language index is zero based.</span></span>

## <a name="to-configure-mutual-exclusion-by-language"></a><span data-ttu-id="eb3e1-119">Para configurar la exclusión mutua por idioma</span><span class="sxs-lookup"><span data-stu-id="eb3e1-119">To Configure Mutual Exclusion by Language</span></span>

<span data-ttu-id="eb3e1-120">La configuración de un objeto de exclusión mutua simple por lenguaje es muy simple.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-120">Configuring a simple mutual exclusion object by language is very simple.</span></span> <span data-ttu-id="eb3e1-121">Cada flujo está asociado ahora a un lenguaje.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-121">Each stream is now associated with a language.</span></span> <span data-ttu-id="eb3e1-122">El lenguaje asociado a una secuencia se puede establecer mediante [**IWMStreamConfig3:: SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage).</span><span class="sxs-lookup"><span data-stu-id="eb3e1-122">The language associated with a stream can be set using [**IWMStreamConfig3::SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage).</span></span> <span data-ttu-id="eb3e1-123">Una vez configurados todos los flujos mutuamente excluyentes, basta con crear un objeto de exclusión mutua como haría con cualquier otro tipo.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-123">After all of the mutually exclusive streams are configured, simply create a mutual exclusion object as you would for any other type.</span></span> <span data-ttu-id="eb3e1-124">A continuación, llame a [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) pasando \_ \_ el lenguaje CLSID WMMUTEX para el tipo.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-124">Then call [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) passing CLSID\_WMMUTEX\_Language for the type.</span></span>

<span data-ttu-id="eb3e1-125">Las secuencias que se excluyen mutuamente por el lenguaje se vuelven más complicadas cuando las secuencias exclusivas también se excluyen mutuamente a través de la velocidad de bits.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-125">Streams that are mutually exclusive by language become more complicated when the exclusive streams are also mutually exclusive by bit rate.</span></span> <span data-ttu-id="eb3e1-126">En este caso, debe realizar los siguientes pasos para usar registros mutuamente excluyentes:</span><span class="sxs-lookup"><span data-stu-id="eb3e1-126">In this case you must use mutually exclusive records, by performing the following steps:</span></span>

1.  <span data-ttu-id="eb3e1-127">Cree un objeto de exclusión mutua para las secuencias de velocidades de bits diferentes en cada idioma.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-127">Create a mutual exclusion object for the streams of differing bit rates in each language.</span></span> <span data-ttu-id="eb3e1-128">Para obtener más información sobre cómo crear un objeto de exclusión mutua por velocidad de bits, vea [usar la exclusión mutua de velocidad de bits múltiple](using-multiple-bit-rate-mutual-exclusion.md).</span><span class="sxs-lookup"><span data-stu-id="eb3e1-128">For more information about creating a mutual exclusion object by bit rate, see [Using Multiple Bit Rate Mutual Exclusion](using-multiple-bit-rate-mutual-exclusion.md).</span></span>
2.  <span data-ttu-id="eb3e1-129">Cree un objeto de exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-129">Create a mutual exclusion object.</span></span> <span data-ttu-id="eb3e1-130">Llame a [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) y pase el \_ lenguaje CLSID WMMUTEX \_ para especificar la exclusividad por lenguaje.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-130">Call [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) and pass CLSID\_WMMUTEX\_Language to specify exclusivity by language.</span></span>
3.  <span data-ttu-id="eb3e1-131">Obtenga un puntero a la interfaz [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) del objeto de exclusión mutua creado en el paso 2 llamando al método **QueryInterface** de [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="eb3e1-131">Obtain a pointer to the [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) interface of the mutual exclusion object created in step 2 by calling the **QueryInterface** method of [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).</span></span>
4.  <span data-ttu-id="eb3e1-132">Llame al método [**IWMMutualExclusion2:: AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) una vez para cada lenguaje, para crear registros de secuencia que se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-132">Call the [**IWMMutualExclusion2::AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) method once for each language, to create stream records that will be mutually exclusive.</span></span>
5.  <span data-ttu-id="eb3e1-133">Para cada registro creado en el paso 4, agregue las secuencias del lenguaje adecuado con llamadas a [**IWMMutualExclusion2:: AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).</span><span class="sxs-lookup"><span data-stu-id="eb3e1-133">For each record created in step 4, add the streams of the appropriate language with calls to [**IWMMutualExclusion2::AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).</span></span>

## <a name="to-read-files-with-multiple-languages"></a><span data-ttu-id="eb3e1-134">Para leer archivos con varios idiomas</span><span class="sxs-lookup"><span data-stu-id="eb3e1-134">To Read Files with Multiple Languages</span></span>

<span data-ttu-id="eb3e1-135">El objeto de lector proporciona métodos para identificar los idiomas disponibles de las secuencias en un archivo.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-135">The reader object provides methods to identify the available languages of streams in a file.</span></span> <span data-ttu-id="eb3e1-136">Puede recuperar el número de idiomas admitidos para una salida mediante una llamada a [**IWMReaderAdvanced4:: GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount).</span><span class="sxs-lookup"><span data-stu-id="eb3e1-136">You can retrieve the number of supported languages for an output by calling [**IWMReaderAdvanced4::GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount).</span></span> <span data-ttu-id="eb3e1-137">A continuación, puede recuperar los detalles de cada idioma con llamadas a [**IWMReaderAdvanced4:: GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).</span><span class="sxs-lookup"><span data-stu-id="eb3e1-137">You can then retrieve details about each language with calls to [**IWMReaderAdvanced4::GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).</span></span>

<span data-ttu-id="eb3e1-138">Puede especificar el idioma que se va a reproducir pasando el índice de ese idioma al lector con una llamada a [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span><span class="sxs-lookup"><span data-stu-id="eb3e1-138">You can specify the language to play by passing the index of that language to the reader with a call to [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span></span> <span data-ttu-id="eb3e1-139">Se seleccionará el idioma especificado al mismo tiempo que se mantiene la selección de secuencias automática para cualquier otro objeto de exclusión mutua del archivo.</span><span class="sxs-lookup"><span data-stu-id="eb3e1-139">This will select the specified language while maintaining automatic stream selection for any other mutual exclusion objects in the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eb3e1-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eb3e1-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb3e1-141">**Temas avanzados**</span><span class="sxs-lookup"><span data-stu-id="eb3e1-141">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="eb3e1-142">**Interfaz IWMLanguageList**</span><span class="sxs-lookup"><span data-stu-id="eb3e1-142">**IWMLanguageList Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[<span data-ttu-id="eb3e1-143">**Interfaz IWMMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="eb3e1-143">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="eb3e1-144">**Interfaz IWMMutualExclusion2**</span><span class="sxs-lookup"><span data-stu-id="eb3e1-144">**IWMMutualExclusion2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[<span data-ttu-id="eb3e1-145">**Interfaz IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="eb3e1-145">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="eb3e1-146">**Interfaz IWMReaderAdvanced4**</span><span class="sxs-lookup"><span data-stu-id="eb3e1-146">**IWMReaderAdvanced4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[<span data-ttu-id="eb3e1-147">**Interfaz IWMStreamConfig3**</span><span class="sxs-lookup"><span data-stu-id="eb3e1-147">**IWMStreamConfig3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




