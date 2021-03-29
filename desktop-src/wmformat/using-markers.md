---
title: Usar marcadores
description: Usar marcadores
ms.assetid: b801c985-4ec7-441e-9f8a-40c69b1299a9
keywords:
- Windows Media Format SDK, marcadores
- Advanced Systems Format (ASF), marcadores
- ASF (formato de sistemas avanzados), marcadores
- Advanced Systems Format (ASF), buscar marcadores
- ASF (formato de sistemas avanzados), buscar marcadores
- marcadores, acerca de
- marcadores, agregar
- marcadores, quitar
- marcadores, recuperar
- marcadores, buscar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cc585b8c71e3bfbae85953650809ad031d36a2
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "103789232"
---
# <a name="using-markers"></a><span data-ttu-id="c876a-113">Usar marcadores</span><span class="sxs-lookup"><span data-stu-id="c876a-113">Using Markers</span></span>

<span data-ttu-id="c876a-114">Un *marcador* es un punto con nombre dentro de un archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="c876a-114">A *marker* is a named point within an ASF file.</span></span> <span data-ttu-id="c876a-115">Cada marcador se compone de un nombre y un tiempo asociado, medido como un desplazamiento desde el inicio del archivo.</span><span class="sxs-lookup"><span data-stu-id="c876a-115">Each marker consists of a name and an associated time, measured as an offset from the start of the file.</span></span> <span data-ttu-id="c876a-116">Una aplicación puede usar marcadores para asignar nombres a varios puntos del contenido, Mostrar esos nombres al usuario y, a continuación, buscar las posiciones del marcador.</span><span class="sxs-lookup"><span data-stu-id="c876a-116">An application can use markers to assign names to various points within the content, display those names to the user, and then seek to the marker positions.</span></span> <span data-ttu-id="c876a-117">Una aplicación puede Agregar o quitar marcadores de un archivo ASF existente.</span><span class="sxs-lookup"><span data-stu-id="c876a-117">An application can add or remove markers from an existing ASF file.</span></span>

<span data-ttu-id="c876a-118">La interfaz [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) contiene métodos para trabajar con marcadores.</span><span class="sxs-lookup"><span data-stu-id="c876a-118">The [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface contains methods for working with markers.</span></span> <span data-ttu-id="c876a-119">El objeto editor de metadatos admite la adición y eliminación de marcadores.</span><span class="sxs-lookup"><span data-stu-id="c876a-119">The metadata editor object supports adding and removing markers.</span></span> <span data-ttu-id="c876a-120">Los objetos de lectura y escritura pueden recuperar marcadores, pero no pueden agregar o quitar marcadores.</span><span class="sxs-lookup"><span data-stu-id="c876a-120">The writer and reader objects can retrieve markers but cannot add or remove markers.</span></span>

## <a name="adding-markers"></a><span data-ttu-id="c876a-121">Agregar marcadores</span><span class="sxs-lookup"><span data-stu-id="c876a-121">Adding Markers</span></span>

<span data-ttu-id="c876a-122">Para agregar un marcador, consulte el editor de metadatos de la interfaz **IWMHeaderInfo** .</span><span class="sxs-lookup"><span data-stu-id="c876a-122">To add a marker, query the metadata editor for the **IWMHeaderInfo** interface.</span></span> <span data-ttu-id="c876a-123">A continuación, llame al método [**IWMHeaderInfo:: AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) , especificando el nombre del marcador como una cadena de caracteres anchos y el tiempo en unidades de 100-nanosegundos.</span><span class="sxs-lookup"><span data-stu-id="c876a-123">Then call the [**IWMHeaderInfo::AddMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addmarker) method, specifying the marker name as a wide-character string and the time in 100-nanosecond units.</span></span> <span data-ttu-id="c876a-124">El tiempo no debe superar la duración del archivo.</span><span class="sxs-lookup"><span data-stu-id="c876a-124">The time must not exceed the file duration.</span></span> <span data-ttu-id="c876a-125">Dos marcadores pueden tener la misma hora.</span><span class="sxs-lookup"><span data-stu-id="c876a-125">Two markers can have the same time.</span></span>

<span data-ttu-id="c876a-126">En el ejemplo siguiente se agregan varios marcadores a un archivo:</span><span class="sxs-lookup"><span data-stu-id="c876a-126">The following example adds several markers to a file:</span></span>


```C++
IWMMetadataEditor *pEdit = 0;
IWMHeaderInfo     *pInfo = 0;

// Create the metadata editor object.

WMCreateEditor(&pEdit);
pEdit->Open(L"C:\\example.wmv");
pEdit->QueryInterface(IID_IWMHeaderInfo, (void**)&pInfo);

// Add the markers. Note that we add the last ones first. Do this when possible
// for improved performance when writing the markers to the file.
hr = pInfo->AddMarker(L"End",  520000000);   // 52 sec.
hr = pInfo->AddMarker(L"Segue",  350000000); // 35 sec.
hr = pInfo->AddMarker(L"Intro",  15000000);  // 1.5 sec.

// Commit changes and clean up.

pEdit->Flush();
pEdit->Close(); 
pInfo->Release();
pEdit->Release();

```



## <a name="removing-markers"></a><span data-ttu-id="c876a-127">Quitar marcadores</span><span class="sxs-lookup"><span data-stu-id="c876a-127">Removing Markers</span></span>

<span data-ttu-id="c876a-128">Para quitar un marcador, llame a [**IWMHeaderInfo:: RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), especificando el índice del marcador que se va a quitar.</span><span class="sxs-lookup"><span data-stu-id="c876a-128">To remove a marker, call [**IWMHeaderInfo::RemoveMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removemarker), specifying the index of the marker to remove.</span></span> <span data-ttu-id="c876a-129">Los marcadores se ordenan automáticamente en orden de tiempo creciente, de modo que el índice 0 siempre es el primer marcador.</span><span class="sxs-lookup"><span data-stu-id="c876a-129">Markers are automatically sorted in increasing time order, so index 0 is always the first marker.</span></span> <span data-ttu-id="c876a-130">Tenga en cuenta que al llamar a **RemoveMarker** se cambian los números de índice de los marcadores siguientes.</span><span class="sxs-lookup"><span data-stu-id="c876a-130">Note that calling **RemoveMarker** changes the index numbers of any markers that follow.</span></span> <span data-ttu-id="c876a-131">El código siguiente, donde *Pinfo* es un puntero a una interfaz **IWMHeaderInfo** , quita todos los marcadores de un archivo:</span><span class="sxs-lookup"><span data-stu-id="c876a-131">The following code, where *pInfo* is a pointer to an **IWMHeaderInfo** interface, removes all the markers from a file:</span></span>


```C++
WORD count = 0;
pInfo->GetMarkerCount(&count);
while (count--)
{
    pInfo->RemoveMarker(0);
}

```



## <a name="retrieving-markers"></a><span data-ttu-id="c876a-132">Recuperar marcadores</span><span class="sxs-lookup"><span data-stu-id="c876a-132">Retrieving Markers</span></span>

<span data-ttu-id="c876a-133">Para recuperar el nombre y la hora de un marcador, realice los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="c876a-133">To retrieve the name and time of a marker, perform the following steps:</span></span>

1.  <span data-ttu-id="c876a-134">Llame al método [**IWMHeaderInfo:: GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) para determinar el número de marcadores que contiene el archivo.</span><span class="sxs-lookup"><span data-stu-id="c876a-134">Call the [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount) method to determine how many markers the file contains.</span></span>
2.  <span data-ttu-id="c876a-135">Recupere el tamaño de la cadena necesaria para contener el nombre del marcador.</span><span class="sxs-lookup"><span data-stu-id="c876a-135">Retrieve the size of the string needed to contain the marker name.</span></span> <span data-ttu-id="c876a-136">Para ello, llame al método [**IWMHeaderInfo:: GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) .</span><span class="sxs-lookup"><span data-stu-id="c876a-136">To do so, call the [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) method.</span></span> <span data-ttu-id="c876a-137">Especifique el índice del marcador que se va a recuperar y **null** para el búfer de cadena (el parámetro *pwszMarkerName* ).</span><span class="sxs-lookup"><span data-stu-id="c876a-137">Specify the index of the marker to retrieve, and **NULL** for the string buffer (the *pwszMarkerName* parameter).</span></span> <span data-ttu-id="c876a-138">El método devuelve la longitud de la cadena, incluido el carácter ' \\ 0 ' de terminación, en el parámetro *pcchMarkerNameLen* .</span><span class="sxs-lookup"><span data-stu-id="c876a-138">The method returns the length of the string, including the terminating '\\0' character, in the *pcchMarkerNameLen* parameter.</span></span>
3.  <span data-ttu-id="c876a-139">Asigne una cadena de caracteres anchos para recibir el nombre.</span><span class="sxs-lookup"><span data-stu-id="c876a-139">Allocate a wide-character string to receive the name.</span></span>
4.  <span data-ttu-id="c876a-140">Vuelva a llamar a **GetMarker** , pero esta vez pase la dirección de la cadena en el parámetro *pwszMarkerName* .</span><span class="sxs-lookup"><span data-stu-id="c876a-140">Call **GetMarker** again, but this time pass the address of the string in the *pwszMarkerName* parameter.</span></span> <span data-ttu-id="c876a-141">El método escribe el nombre del marcador en la cadena y devuelve la hora del marcador en el parámetro *pcnsMarkerTime* .</span><span class="sxs-lookup"><span data-stu-id="c876a-141">The method writes the marker name into the string, and returns the marker time in the *pcnsMarkerTime* parameter.</span></span>

<span data-ttu-id="c876a-142">El siguiente código recorre en bucle cada marcador en orden y recupera el nombre y la hora:</span><span class="sxs-lookup"><span data-stu-id="c876a-142">The following code loops through every marker in order and retrieves the name and time:</span></span>


```C++
WORD cMarkers = 0;
HRESULT hr = pInfo->GetMarkerCount(&cMarkers);

WCHAR *wszName = 0;
WORD  len = 0;
for (WORD iMarker = 0; iMarker < cMarkers; ++iMarker)
{
    QWORD rtTime = 0;
    WORD req_len = 0;
    hr = pInfo->GetMarker(iMarker, 0, &req_len, &rtTime);
    
    // Reallocate if necessary.
    if (len < req_len)
    {
        delete[] wszName;
        wszName = new WCHAR[req_len];
        len = req_len;
    }
    hr = pInfo->GetMarker(iMarker, wszName, &req_len, &rtTime);
    // Display the name...
}
delete[] wszName;

```



## <a name="seeking-to-a-marker"></a><span data-ttu-id="c876a-143">Buscar un marcador</span><span class="sxs-lookup"><span data-stu-id="c876a-143">Seeking to a Marker</span></span>

<span data-ttu-id="c876a-144">Para iniciar la reproducción desde una ubicación de marcador, llame al método [**IWMReaderAdvanced2:: StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) del objeto lector y especifique el índice del marcador.</span><span class="sxs-lookup"><span data-stu-id="c876a-144">To start playback from a marker location, call the reader object's [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker) method, specifying the index of the marker.</span></span> <span data-ttu-id="c876a-145">Los parámetros restantes son idénticos a los del método [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) .</span><span class="sxs-lookup"><span data-stu-id="c876a-145">The remaining parameters are identical to those for the [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start) method.</span></span> <span data-ttu-id="c876a-146">En el ejemplo siguiente se consulta el lector de la interfaz [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) y se busca el primer marcador.</span><span class="sxs-lookup"><span data-stu-id="c876a-146">The following example queries the reader for the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface and seeks to the first marker.</span></span>


```C++
IWMReaderAdvanced2 *pReader2 = 0
WORD iMarkerIndex = 0;
hr = pReader->QueryInterface(IID_IWMReaderAdvanced2, (void**)&pReader2);
if (SUCCEEDED(hr))
{
    hr = pPlayer2->StartAtMarker(iMarkerIndex, 0, 1.0, 0);
    pPlayer2->Release();
}

```



## <a name="related-topics"></a><span data-ttu-id="c876a-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c876a-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c876a-148">**Interfaz IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="c876a-148">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="c876a-149">**IWMReaderAdvanced2::StartAtMarker**</span><span class="sxs-lookup"><span data-stu-id="c876a-149">**IWMReaderAdvanced2::StartAtMarker**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)
</dt> <dt>

[<span data-ttu-id="c876a-150">**Trabajar con metadatos**</span><span class="sxs-lookup"><span data-stu-id="c876a-150">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




