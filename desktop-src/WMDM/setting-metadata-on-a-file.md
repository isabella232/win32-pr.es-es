---
title: Establecer metadatos en un archivo
description: Establecer metadatos en un archivo
ms.assetid: 478a5412-e8b4-41c8-802f-9c2748dbaeae
keywords:
- Windows Media Administrador de dispositivos,metadata
- Administrador de dispositivos,metadata
- guía de programación, metadatos
- aplicaciones de escritorio, metadatos
- crear Windows aplicaciones Administrador de dispositivos multimedia, metadatos
- escribir archivos en dispositivos, metadatos
- metadata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a6fa7002d4fafffe0793ef91b00dd3f1f0e20c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242013"
---
# <a name="setting-metadata-on-a-file"></a>Establecer metadatos en un archivo

Puede establecer metadatos en un archivo antes de escribirlo en el dispositivo (cuando se usa [**IWMDMStorageControl3::Insert3)**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)o en un almacenamiento existente (llamando a [**IWMDMStorage3::SetMetadata).**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) Solo puede establecer atributos en un almacenamiento existente (llamando a [**IWMDMStorage::SetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-setattributes) o [**IWMDMStorage2::SetAttributes2).**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-setattributes2)

Para establecer los metadatos, se crea y rellena una [**interfaz IWMDMMetaData**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmmetadata) que se pasa a [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3). Sin embargo, este método puede borrar todos los metadatos existentes en el archivo, aparte de los metadatos codificados de forma segura almacenados en el propio sistema de archivos, como el nombre de archivo o el tamaño. Por lo tanto, debe copiar todos los metadatos existentes que desee conservar en la interfaz IWMDMMetaData que envíe. Dado Windows no Administrador de dispositivos se pueden usar para recuperar metadatos de archivos locales, debe usar el SDK de formato multimedia de Windows (o alguna otra herramienta) para recuperar dichos metadatos.

Para usar el SDK Windows Media Format para recuperar las propiedades del archivo ASF, siga estos pasos:

1.  Cree un objeto del editor de metadatos llamando a **WMCreateEditor** y solicitando una **interfaz IWMMetadataEditor.**
2.  Abra el archivo para leer los metadatos mediante una **llamada a IWMMetadataEditor::Open**.
3.  Si el archivo es un archivo ASF válido y se puede abrir, consulte el editor para la **interfaz IWMHeaderInfo.**
4.  Recupere las propiedades del archivo mediante una llamada **a IWMHeaderInfo::GetAttributeByName**, pasando la constante de propiedad del SDK Windows formato multimedia deseado. En la tabla siguiente se proporciona una lista de constantes del SDK de formato con Windows media Administrador de dispositivos SDK equivalentes.



| Windows Constante del SDK de formato multimedia    | Windows Media Administrador de dispositivos SDK Constant      |
|--------------------------------------|------------------------------------------------|
| g \_ wszWMTitle                        | g \_ wszWMDMTitle                                |
| g \_ wszWMAuthor                       | g \_ wszWMDMAuthor                               |
| g \_ wszWMAlbumTitle                   | g \_ wszWMDMAlbumTitle                           |
| g \_ wszWMGenre                        | g \_ wszWMDMGenre                                |
| g \_ wszWMYear                         | g \_ wszWMDMYear                                 |
| g \_ wszWMTrackNumber o g \_ wszWMTrack | g \_ wszWMDMTrack                                |
| g \_ wszWMComposer                     | g \_ wszWMDMComposer                             |
| g \_ wszWMDuration                     | g \_ wszWMDMDuration                             |
| g \_ wszWMCopyright                    | g \_ wszWMDMProviderCopyright                    |
| g \_ wszWMDescription                  | g \_ wszWMDMDescription                          |
| g \_ wszWMBitrate                      | g \_ wszWMDMBitrate                              |
| g \_ wszWMRating                       | g \_ wszWMDMUserRating                           |
| g \_ wszWMAlbumArtist                  | g \_ wszWMDMAlbumArtist                          |
| g \_ wszWMParentalRating               | g \_ wszWMDMParentalRating                       |
| g \_ wszWMRadioStationName             | g \_ wszWMDMMediaStationName                     |
| g \_ wszWMSubTitle                     | g \_ wszWMDMSubTitle                             |
| g \_ wszWMVideoWidth                   | g \_ wszWMDMWidth                                |
| g \_ wszWMVideoHeight                  | g \_ wszWMDMHeight                               |
| g \_ wszWMMood                         | g \_ wszWMDMTrackMood                            |
| g \_ wszWMCodec                        | g \_ wszAudioWAVECodec o g \_ wszVideoFourCCCodec |



 

En el siguiente código de ejemplo de C++ se muestra cómo recuperar varias propiedades de metadatos de un archivo ASF mediante el SDK de formato multimedia de Windows y convertirlos a los valores Windows Media Administrador de dispositivos equivalentes.


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



La siguiente función de ejemplo de C++ muestra cómo usar DirectShow para obtener información de archivo y agregarla a los metadatos.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escribir archivos en el dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




