---
title: Establecer los metadatos de un archivo
description: Establecer los metadatos de un archivo
ms.assetid: 478a5412-e8b4-41c8-802f-9c2748dbaeae
keywords:
- Administrador de dispositivos de Windows Media, metadatos
- Administrador de dispositivos, metadatos
- Guía de programación, metadatos
- aplicaciones de escritorio, metadatos
- crear aplicaciones de Windows Media Administrador de dispositivos, metadatos
- escribir archivos en dispositivos, metadatos
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a6fa7002d4fafffe0793ef91b00dd3f1f0e20c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695328"
---
# <a name="setting-metadata-on-a-file"></a><span data-ttu-id="358aa-110">Establecer los metadatos de un archivo</span><span class="sxs-lookup"><span data-stu-id="358aa-110">Setting Metadata on a File</span></span>

<span data-ttu-id="358aa-111">Puede establecer metadatos en un archivo antes de escribirlo en el dispositivo (cuando se usa [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)) o en un almacenamiento existente (llamando a [**IWMDMStorage3:: setMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)).</span><span class="sxs-lookup"><span data-stu-id="358aa-111">You can set metadata on a file before writing it to the device (when using [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)) or on an existing storage (by calling [**IWMDMStorage3::SetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)).</span></span> <span data-ttu-id="358aa-112">Solo puede establecer atributos en un almacenamiento existente (llamando a [**IWMDMStorage:: SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes) o [**IWMDMStorage2:: SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)).</span><span class="sxs-lookup"><span data-stu-id="358aa-112">You can set attributes only on an existing storage (by calling [**IWMDMStorage::SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes) or [**IWMDMStorage2::SetAttributes2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)).</span></span>

<span data-ttu-id="358aa-113">La configuración de los metadatos se realiza creando y rellenando una interfaz [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) que se pasa a [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span><span class="sxs-lookup"><span data-stu-id="358aa-113">Setting metadata is done by creating and filling an [**IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) interface that is passed into [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3).</span></span> <span data-ttu-id="358aa-114">Sin embargo, este método puede borrar todos los metadatos existentes en el archivo, excepto los metadatos codificados de forma rígida almacenados en el propio sistema de archivos, como el nombre o el tamaño del archivo.</span><span class="sxs-lookup"><span data-stu-id="358aa-114">However, this method can clear all existing metadata on the file, other than hard-coded metadata stored in the file system itself, such as file name or size.</span></span> <span data-ttu-id="358aa-115">Por lo tanto, debe copiar todos los metadatos existentes que desee conservar en la interfaz IWMDMMetaData que envíe.</span><span class="sxs-lookup"><span data-stu-id="358aa-115">Therefore, you must copy all existing metadata that you wish to retain into the IWMDMMetaData interface you submit.</span></span> <span data-ttu-id="358aa-116">Como Windows Media Administrador de dispositivos no se puede usar para recuperar metadatos de archivos locales, debe usar el SDK de Windows Media Format (o alguna otra herramienta) para recuperar dichos metadatos.</span><span class="sxs-lookup"><span data-stu-id="358aa-116">Because Windows Media Device Manager cannot be used to retrieve metadata from local files, you must use the Windows Media Format SDK (or some other tool) to retrieve such metadata.</span></span>

<span data-ttu-id="358aa-117">Para usar el SDK de Windows Media Format para recuperar las propiedades de archivo ASF, siga estos pasos:</span><span class="sxs-lookup"><span data-stu-id="358aa-117">To use the Windows Media Format SDK to retrieve ASF file properties, follow these steps:</span></span>

1.  <span data-ttu-id="358aa-118">Cree un objeto de editor de metadatos llamando a **WMCreateEditor** y solicitando una interfaz **IWMMetadataEditor** .</span><span class="sxs-lookup"><span data-stu-id="358aa-118">Create a metadata editor object by calling **WMCreateEditor** and requesting an **IWMMetadataEditor** interface.</span></span>
2.  <span data-ttu-id="358aa-119">Abra el archivo para la lectura de metadatos mediante una llamada a **IWMMetadataEditor:: Open**.</span><span class="sxs-lookup"><span data-stu-id="358aa-119">Open the file for metadata reading by calling **IWMMetadataEditor::Open**.</span></span>
3.  <span data-ttu-id="358aa-120">Si el archivo es un archivo ASF válido y se puede abrir, consulte en el editor la interfaz **IWMHeaderInfo** .</span><span class="sxs-lookup"><span data-stu-id="358aa-120">If the file is a valid ASF file and can be opened, query the editor for the **IWMHeaderInfo** interface.</span></span>
4.  <span data-ttu-id="358aa-121">Recupere las propiedades de archivo mediante una llamada a **IWMHeaderInfo:: GetAttributeByName**, pasando la constante de propiedad del SDK de Windows Media Format deseada.</span><span class="sxs-lookup"><span data-stu-id="358aa-121">Retrieve file properties by calling **IWMHeaderInfo::GetAttributeByName**, passing in the desired Windows Media Format SDK property constant.</span></span> <span data-ttu-id="358aa-122">En la tabla siguiente se proporciona una lista de constantes de SDK de formato con constantes de SDK de Windows Media Administrador de dispositivos equivalentes.</span><span class="sxs-lookup"><span data-stu-id="358aa-122">A list of Format SDK constants with equivalent Windows Media Device Manager SDK constants is given in the following table.</span></span>



| <span data-ttu-id="358aa-123">Windows Media Format (constante del SDK)</span><span class="sxs-lookup"><span data-stu-id="358aa-123">Windows Media Format SDK Constant</span></span>    | <span data-ttu-id="358aa-124">Constante del SDK de Administrador de dispositivos de Windows Media</span><span class="sxs-lookup"><span data-stu-id="358aa-124">Windows Media Device Manager SDK Constant</span></span>      |
|--------------------------------------|------------------------------------------------|
| <span data-ttu-id="358aa-125">g \_ wszWMTitle</span><span class="sxs-lookup"><span data-stu-id="358aa-125">g\_wszWMTitle</span></span>                        | <span data-ttu-id="358aa-126">g \_ wszWMDMTitle</span><span class="sxs-lookup"><span data-stu-id="358aa-126">g\_wszWMDMTitle</span></span>                                |
| <span data-ttu-id="358aa-127">g \_ wszWMAuthor</span><span class="sxs-lookup"><span data-stu-id="358aa-127">g\_wszWMAuthor</span></span>                       | <span data-ttu-id="358aa-128">g \_ wszWMDMAuthor</span><span class="sxs-lookup"><span data-stu-id="358aa-128">g\_wszWMDMAuthor</span></span>                               |
| <span data-ttu-id="358aa-129">g \_ wszWMAlbumTitle</span><span class="sxs-lookup"><span data-stu-id="358aa-129">g\_wszWMAlbumTitle</span></span>                   | <span data-ttu-id="358aa-130">g \_ wszWMDMAlbumTitle</span><span class="sxs-lookup"><span data-stu-id="358aa-130">g\_wszWMDMAlbumTitle</span></span>                           |
| <span data-ttu-id="358aa-131">g \_ wszWMGenre</span><span class="sxs-lookup"><span data-stu-id="358aa-131">g\_wszWMGenre</span></span>                        | <span data-ttu-id="358aa-132">g \_ wszWMDMGenre</span><span class="sxs-lookup"><span data-stu-id="358aa-132">g\_wszWMDMGenre</span></span>                                |
| <span data-ttu-id="358aa-133">g \_ wszWMYear</span><span class="sxs-lookup"><span data-stu-id="358aa-133">g\_wszWMYear</span></span>                         | <span data-ttu-id="358aa-134">g \_ wszWMDMYear</span><span class="sxs-lookup"><span data-stu-id="358aa-134">g\_wszWMDMYear</span></span>                                 |
| <span data-ttu-id="358aa-135">g \_ wszWMTrackNumber o g \_ wszWMTrack</span><span class="sxs-lookup"><span data-stu-id="358aa-135">g\_wszWMTrackNumber or g\_wszWMTrack</span></span> | <span data-ttu-id="358aa-136">g \_ wszWMDMTrack</span><span class="sxs-lookup"><span data-stu-id="358aa-136">g\_wszWMDMTrack</span></span>                                |
| <span data-ttu-id="358aa-137">g \_ wszWMComposer</span><span class="sxs-lookup"><span data-stu-id="358aa-137">g\_wszWMComposer</span></span>                     | <span data-ttu-id="358aa-138">g \_ wszWMDMComposer</span><span class="sxs-lookup"><span data-stu-id="358aa-138">g\_wszWMDMComposer</span></span>                             |
| <span data-ttu-id="358aa-139">g \_ wszWMDuration</span><span class="sxs-lookup"><span data-stu-id="358aa-139">g\_wszWMDuration</span></span>                     | <span data-ttu-id="358aa-140">g \_ wszWMDMDuration</span><span class="sxs-lookup"><span data-stu-id="358aa-140">g\_wszWMDMDuration</span></span>                             |
| <span data-ttu-id="358aa-141">g \_ wszWMCopyright</span><span class="sxs-lookup"><span data-stu-id="358aa-141">g\_wszWMCopyright</span></span>                    | <span data-ttu-id="358aa-142">g \_ wszWMDMProviderCopyright</span><span class="sxs-lookup"><span data-stu-id="358aa-142">g\_wszWMDMProviderCopyright</span></span>                    |
| <span data-ttu-id="358aa-143">g \_ wszWMDescription</span><span class="sxs-lookup"><span data-stu-id="358aa-143">g\_wszWMDescription</span></span>                  | <span data-ttu-id="358aa-144">g \_ wszWMDMDescription</span><span class="sxs-lookup"><span data-stu-id="358aa-144">g\_wszWMDMDescription</span></span>                          |
| <span data-ttu-id="358aa-145">g \_ wszWMBitrate</span><span class="sxs-lookup"><span data-stu-id="358aa-145">g\_wszWMBitrate</span></span>                      | <span data-ttu-id="358aa-146">g \_ wszWMDMBitrate</span><span class="sxs-lookup"><span data-stu-id="358aa-146">g\_wszWMDMBitrate</span></span>                              |
| <span data-ttu-id="358aa-147">g \_ wszWMRating</span><span class="sxs-lookup"><span data-stu-id="358aa-147">g\_wszWMRating</span></span>                       | <span data-ttu-id="358aa-148">g \_ wszWMDMUserRating</span><span class="sxs-lookup"><span data-stu-id="358aa-148">g\_wszWMDMUserRating</span></span>                           |
| <span data-ttu-id="358aa-149">g \_ wszWMAlbumArtist</span><span class="sxs-lookup"><span data-stu-id="358aa-149">g\_wszWMAlbumArtist</span></span>                  | <span data-ttu-id="358aa-150">g \_ wszWMDMAlbumArtist</span><span class="sxs-lookup"><span data-stu-id="358aa-150">g\_wszWMDMAlbumArtist</span></span>                          |
| <span data-ttu-id="358aa-151">g \_ wszWMParentalRating</span><span class="sxs-lookup"><span data-stu-id="358aa-151">g\_wszWMParentalRating</span></span>               | <span data-ttu-id="358aa-152">g \_ wszWMDMParentalRating</span><span class="sxs-lookup"><span data-stu-id="358aa-152">g\_wszWMDMParentalRating</span></span>                       |
| <span data-ttu-id="358aa-153">g \_ wszWMRadioStationName</span><span class="sxs-lookup"><span data-stu-id="358aa-153">g\_wszWMRadioStationName</span></span>             | <span data-ttu-id="358aa-154">g \_ wszWMDMMediaStationName</span><span class="sxs-lookup"><span data-stu-id="358aa-154">g\_wszWMDMMediaStationName</span></span>                     |
| <span data-ttu-id="358aa-155">g \_ wszWMSubTitle</span><span class="sxs-lookup"><span data-stu-id="358aa-155">g\_wszWMSubTitle</span></span>                     | <span data-ttu-id="358aa-156">g \_ wszWMDMSubTitle</span><span class="sxs-lookup"><span data-stu-id="358aa-156">g\_wszWMDMSubTitle</span></span>                             |
| <span data-ttu-id="358aa-157">g \_ wszWMVideoWidth</span><span class="sxs-lookup"><span data-stu-id="358aa-157">g\_wszWMVideoWidth</span></span>                   | <span data-ttu-id="358aa-158">g \_ wszWMDMWidth</span><span class="sxs-lookup"><span data-stu-id="358aa-158">g\_wszWMDMWidth</span></span>                                |
| <span data-ttu-id="358aa-159">g \_ wszWMVideoHeight</span><span class="sxs-lookup"><span data-stu-id="358aa-159">g\_wszWMVideoHeight</span></span>                  | <span data-ttu-id="358aa-160">g \_ wszWMDMHeight</span><span class="sxs-lookup"><span data-stu-id="358aa-160">g\_wszWMDMHeight</span></span>                               |
| <span data-ttu-id="358aa-161">g \_ wszWMMood</span><span class="sxs-lookup"><span data-stu-id="358aa-161">g\_wszWMMood</span></span>                         | <span data-ttu-id="358aa-162">g \_ wszWMDMTrackMood</span><span class="sxs-lookup"><span data-stu-id="358aa-162">g\_wszWMDMTrackMood</span></span>                            |
| <span data-ttu-id="358aa-163">g \_ wszWMCodec</span><span class="sxs-lookup"><span data-stu-id="358aa-163">g\_wszWMCodec</span></span>                        | <span data-ttu-id="358aa-164">g \_ wszAudioWAVECodec o g \_ wszVideoFourCCCodec</span><span class="sxs-lookup"><span data-stu-id="358aa-164">g\_wszAudioWAVECodec or g\_wszVideoFourCCCodec</span></span> |



 

<span data-ttu-id="358aa-165">En el siguiente código de ejemplo de C++ se muestra cómo recuperar una serie de propiedades de metadatos de un archivo ASF con el SDK de Windows Media Format y convertirlas en los valores equivalentes de Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="358aa-165">The following C++ example code demonstrates retrieving a number of metadata properties from an ASF file using the Windows Media Format SDK and converting them to the equivalent Windows Media Device Manager values.</span></span>


```C++
// Structure and array to hold equivalent Windows Media Format SDK 
// and Windows Media Device Manager SDK metadata property names.
struct EquivalentProperty
{
    LPCWSTR FormatSDKConst;
    LPCWSTR WMDMSDKConst;
};
EquivalentProperty EquivalentProperties []= 
{
    {g_wszWMTitle,        g_wszWMDMTitle},
    {g_wszWMAuthor,      g_wszWMDMAuthor},
    {g_wszWMAlbumTitle,  g_wszWMDMAlbumTitle},
    {g_wszWMGenre,       g_wszWMDMGenre},
    {g_wszWMYear,        g_wszWMDMYear},
    {g_wszWMTrackNumber, g_wszWMDMTrack},
    {g_wszWMTrack,       g_wszWMDMTrack},
    {g_wszWMComposer,    g_wszWMDMComposer},
    {g_wszWMBitrate,     g_wszWMDMBitrate},
    {g_wszWMDuration,    g_wszWMDMDuration},
    {g_wszWMCopyright,   g_wszWMDMProviderCopyright},
    {g_wszWMDescription, g_wszWMDMDescription},
    {g_wszWMRating,      g_wszWMDMUserRating},
    {g_wszWMAlbumArtist, g_wszWMDMAlbumArtist},
    {g_wszWMParentalRating,    g_wszWMDMParentalRating},
    {g_wszWMRadioStationName,  g_wszWMDMMediaStationName},
    {g_wszWMSubTitle,    g_wszWMDMSubTitle},
    {g_wszWMVideoWidth,  g_wszWMDMWidth},
    {g_wszWMVideoHeight, g_wszWMDMHeight},
    {g_wszWMMood,        g_wszWMDMTrackMood},
    {g_wszWMCodec,       g_wszAudioWAVECodec},
    {g_wszWMCodec,       g_wszVideoFourCCCodec}
};
// Function that tries to get metadata by using the Format SDK. 
// If it cannot open the file, it returns E_FAIL.
HRESULT GetFileMetadataFromFormatSDK(IWMDMMetaData* pMetadata, LPCWSTR file)
{
    if ((pMetaData == NULL) || (file == NULL)) return E_INVALIDPARAM;
    HRESULT hr = S_OK;
    CComPtr<IWMMetadataEditor> pEditor;

    // Do loop to allow easy error trapping. Even if there are no errors, 
    // the loop executes only once.
    do {
        hr = WMCreateEditor(&pEditor);
        if (FAILED(hr)) 
            break;

        // Open the file.
        hr = pEditor->Open(file);
        if (FAILED(hr)) 
            break;

        CComPtr<IWMHeaderInfo>pHeaderInfo;
        hr = pEditor->QueryInterface(__uuidof(IWMHeaderInfo), (void**)&pHeaderInfo);
        if (FAILED(hr))
            break;

        // Copy values from Format SDK to equivalent WMDM SDK metadata values.

        // Loop through all known values
        WORD stream = 0;
        WMT_ATTR_DATATYPE wmfType;
        WORD len = 0;
        BYTE* value = NULL;
        WMDM_TAG_DATATYPE wmdmType;
        for (int i = 0; i < sizeof(EquivalentProperties) / sizeof(EquivalentProperties[0]); i++)
        {
            // Request each value from our equivalency list by name.
            // The function is called twice: once to get the buffer size,
            // and once to get the value in the allocated buffer.
            if (FAILED(pHeaderInfo->GetAttributeByName(
                &stream, EquivalentProperties[i].FormatSDKConst, &wmfType, NULL, &len)))
            {
                continue;
            }

            value = new BYTE[len];
            if (value == NULL) continue;

            if (FAILED(pHeaderInfo->GetAttributeByName(&stream, EquivalentProperties[i].FormatSDKConst, &wmfType, value, &len)))
            {
                delete[] value;
                continue;
            }

            // Send the data to the equivalent WMDM metadata value.
            // First, find the equivalent WMDM type for the WMF type.
            switch(wmfType)
            {
            case WMT_TYPE_BINARY:
                wmdmType = WMDM_TYPE_BINARY;
                break;
            case WMT_TYPE_DWORD:
                wmdmType = WMDM_TYPE_DWORD;
                break;
            case WMT_TYPE_STRING:
                wmdmType = WMDM_TYPE_STRING;
                break;
            case WMT_TYPE_BOOL:
                wmdmType = WMDM_TYPE_BOOL;
                break;
            case WMT_TYPE_QWORD:
                wmdmType = WMDM_TYPE_QWORD;
                break;
            case WMT_TYPE_WORD:
                wmdmType = WMDM_TYPE_WORD;
                break;
            case WMT_TYPE_GUID:
                wmdmType = WMDM_TYPE_GUID;
                break;
            default:
                wmdmType = WMDM_TYPE_BINARY;
                break;
            }

            // Don't worry about trapping errors, because there's nothing 
            // we can do about it.
            pMetadata->AddItem(wmdmType, 
                EquivalentProperties[i].WMDMSDKConst, value, len);
            delete[] value;
        } // Add next value.
    } while (FALSE); // End Do loop error trap.

    // Close the file opened with IWMMetadataEditor.
    pEditor->Close();
    return hr;
}
```



<span data-ttu-id="358aa-166">La siguiente función de ejemplo de C++ muestra cómo usar DirectShow para obtener información de archivos y agregarla a los metadatos.</span><span class="sxs-lookup"><span data-stu-id="358aa-166">The following C++ example function shows how to use DirectShow to get some file information and add it to the metadata.</span></span>


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
HRESULT GetFileMetadataFromDShow(IWMDMMetaData* pMetadata, LPCWSTR file)
{
    HRESULT hr = S_OK;

    // Add file metadata properties from DirectShow. 
    // This is good for non-ASF files, or to add any information
    // that the Format SDK didn't get.

    // Do loop to allow easy error trapping. Even if there are no errors, 
    // the loop executes only once.
    do
    {
        // Create the Media Detector object.
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (FAILED(hr)) 
            break;

        // Open the file.
        hr = pIMediaDet->put_Filename(BSTR(file));
        if (FAILED(hr))
            break;

        // Get the media type for the default stream.
        AM_MEDIA_TYPE mediaType;
        hr = pIMediaDet->get_StreamMediaType(&mediaType);
        if (FAILED(hr))
            break;

        // We have the file open, so start requesting information from the 
        // Media Detector and adding it to the metadata. When adding 
        // individual metadata values, ignore the HRESULT, because failure 
        // to add these metadata values is not a breaking issue.

        // Get major and minor types.
        WCHAR strMediaType[64];
        ZeroMemory(strMediaType, 64);

        //Change the major type to a string, then add to IWMDMMetaData.
        StringFromGUID2(reinterpret_cast<GUID&>(mediaType.majortype),
            (LPOLESTR)strMediaType, 64);
        hr = pMetadata->AddItem(WMDM_TYPE_STRING, 
             g_wszWMDMediaClassPrimaryID, 
            (BYTE*) strMediaType, 
             sizeof(strMediaType) / sizeof(strMediaType[0]));

        // Clear local string, then retrieve subtype the same way.
        ZeroMemory(strMediaType, 64);
        StringFromGUID2(reinterpret_cast<GUID&>(mediaType.subtype),
            (LPOLESTR)strMediaType, 64);
        hr = pMetadata->AddItem(WMDM_TYPE_STRING, 
            g_wszWMDMMediaClassSecondaryID, (BYTE*) strMediaType,
            sizeof(strMediaType) / sizeof(strMediaType[0]));

        // Get the duration. Duration is retrieved in seconds, but set 
        // in 100-nanosecond units.
        double duration = 0;
        hr = pIMediaDet->get_StreamLength(&duration);
        if (duration > 0)
        {
            duration *= 10E7;
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMDuration, (BYTE*) &duration, sizeof(duration));
        }

        // Get the frame rate.
        double frameRate = 0;
        hr = pIMediaDet->get_FrameRate(&frameRate);
        if (frameRate > 0)
        {
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMFrameRate, 
                (BYTE*) &frameRate,
                sizeof(frameRate));
        }

        // Get the structure for the default stream's major type and 
        // fill in additional information.

        if (IsEqualGUID(mediaType.formattype, FORMAT_VideoInfo))
        {
            VIDEOINFOHEADER* data = (VIDEOINFOHEADER*) mediaType.pbFormat;
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMVideoBitrate, 
               (BYTE*) &data->dwBitRate, sizeof(DWORD));
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMHeight, 
               (BYTE*) &data->bmiHeader.biHeight, sizeof(LONG));
            hr = pMetadata->AddItem(WMDM_TYPE_DWORD, g_wszWMDMWidth, 
               (BYTE*) &data->bmiHeader.biWidth, sizeof(LONG));
        }

        if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
        {
            WAVEFORMATEX* data = (WAVEFORMATEX*) mediaType.pbFormat;
            hr = pMetadata->AddItem(WMDM_TYPE_WORD, g_wszWMDMBlockAlignment, 
                (BYTE*) &data->nBlockAlign, sizeof(WORD));
            hr = pMetadata->AddItem(WMDM_TYPE_WORD, g_wszWMDMNumChannels, 
               (BYTE*) &data->nChannels, sizeof(WORD));
        }
    } while (FALSE); // End of error loop.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="358aa-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="358aa-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="358aa-168">**Escribir archivos en el dispositivo**</span><span class="sxs-lookup"><span data-stu-id="358aa-168">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




