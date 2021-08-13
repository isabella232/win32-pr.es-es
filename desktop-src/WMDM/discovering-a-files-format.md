---
title: Detectar el formato de un archivo
description: Detectar el formato de un archivo
ms.assetid: f1b3f811-8161-41ca-a92c-2735c0bec2e8
keywords:
- Windows Formatos Administrador de dispositivos,file
- Administrador de dispositivos,formatos de archivo
- guía de programación, formatos de archivo
- aplicaciones de escritorio, formatos de archivo
- crear aplicaciones Windows multimedia Administrador de dispositivos, formatos de archivo
- escribir archivos en dispositivos, formatos de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83706a3026968a694d3629551d310db9021b7f8c8118f3d98621751a95af26b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118585334"
---
# <a name="discovering-a-files-format"></a>Detectar el formato de un archivo

Antes de enviar un archivo al dispositivo, una aplicación debe determinar si el dispositivo admite ese formato de archivo.

Detectar el formato de un archivo puede ser complejo. La manera más sencilla es crear una lista de extensiones de archivo asignadas a valores de enumeración FORMATCODE de WMDM \_ específicos. Sin embargo, hay algunos problemas con este sistema: uno es que un solo formato puede tener varias extensiones (como .jpg, .jpe y .jpeg para imágenes JPEG). Además, diferentes programas pueden usar la misma extensión de archivo para distintos formatos.

Para superar las limitaciones de una asignación estricta, es mejor que una aplicación compruebe que el formato coincide con la extensión. El SDK DirectShow proporciona herramientas que permiten a una aplicación detectar un conjunto limitado de detalles sobre la mayoría de los tipos de archivo multimedia. El SDK Windows media format expone un gran número de detalles, pero solo sobre los archivos ASF. Dado que todos los tipos de archivo deben tener comprobado su código de formato si es posible, es mejor usar DirectShow para detectar o comprobar el código de formato básico y usar el SDK de formato multimedia de Windows para detectar los metadatos adicionales deseados sobre los archivos ASF. DirectShow también se puede usar para detectar metadatos básicos para archivos que no son ASF.

La siguiente es una manera de detectar un formato de archivo mediante la asignación de extensiones DirectShow.

En primer lugar, compare la extensión de nombre de archivo con una lista de extensiones conocidas. Asegúrese de que la comparación no tiene en cuenta mayúsculas de minúsculas. Si la extensión no está asignada, establezca el formato en WMDM \_ FORMATCODE \_ UNDEFINED.

-   Si no se encontró el código de formato (o desea comprobar que un archivo es un archivo multimedia), puede realizar los pasos siguientes:
    1.  Cree un DirectShow Detección multimedia mediante **CoCreateInstance**(CLSID \_ MediaDet) y recuperando la **interfaz IMediaDet.**
    2.  Abra el archivo llamando a **IMediaDet::p ut \_ Filename**. Se producirá un error en esta llamada si el archivo está protegido.
    3.  Obtenga el tipo de medio de la secuencia predeterminada mediante una llamada **a IMediaDet::get \_ StreamMediaType**, que devuelve un **TIPO DE MEDIO DE \_ \_ AM**.
    4.  Para obtener el número de secuencias, llame a **IMediaDet::get \_ OutputStreams.**
        -   Si solo hay una secuencia y es audio, el tipo de archivo es WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO.
        -   Si solo hay una secuencia y es vídeo, el tipo de archivo es WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO.
        -   Si solo hay una secuencia y es vídeo y la velocidad de bits es cero, el tipo de archivo es WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT.

También puede intentar hacer coincidir códecs de audio o vídeo de los miembros **VIDEOINFOHEADER** o **MPEGATEX** recuperados de **get \_ StreamMediaType.**

La siguiente función de C++ muestra la coincidencia de la extensión de archivo y DirectShow para intentar analizar archivos desconocidos.


```C++
// For IMediaDet, you must link to strmiids.lib. Also include the following:
//#include <Qedit.h>  // for IMediaDet declaration.
//#include <Dshow.h>  // for VIDEOINFOHEADER declaration.
WMDM_FORMATCODE CWMDMController::myGetWMDM_FORMATCODE(LPCWSTR pFileName)
{
    HRESULT hr = S_OK;

    // Declare the variable to hold the WMDM format code.
    WMDM_FORMATCODE fmt = WMDM_FORMATCODE_UNDEFINED;
    
    // Get the file extension.
    wstring ext = pFileName;
    ext = ext.substr(ext.find_last_of(L".") + 1);

    // This is not an exhaustive list. 
    // It is also case-sensitive.
    if (ext == L"js" || ext == L"vb")
        fmt = WMDM_FORMATCODE_SCRIPT;
    else if (ext == L".exe")
        fmt = WMDM_FORMATCODE_EXECUTABLE;
    else if (ext == L"txt")
        fmt = WMDM_FORMATCODE_TEXT;
    else if (ext == L"html" || ext == L"htm" || ext == L"shtm")
        fmt = WMDM_FORMATCODE_HTML;
    else if (ext == L"aiff")
        fmt = WMDM_FORMATCODE_AIFF;
    else if (ext == L"wav")
        fmt = WMDM_FORMATCODE_WAVE;
    else if (ext == L"mp3")
        fmt = WMDM_FORMATCODE_MP3;
    else if (ext == L"mpg" || ext == L"mpeg" || ext == L"mp2")
        fmt = WMDM_FORMATCODE_MPEG;
    else if (ext == L"bmp")
        fmt = WMDM_FORMATCODE_IMAGE_BMP;
    else if (ext == L"avi")
        fmt = WMDM_FORMATCODE_AVI;
    else if (ext == L"asf")
        fmt = WMDM_FORMATCODE_ASF;
    else if (ext == L"tif")
        fmt = WMDM_FORMATCODE_IMAGE_TIFF;
    else if (ext == L"gif")
        fmt = WMDM_FORMATCODE_IMAGE_GIF;
    else if (ext == L"pct")
        fmt = WMDM_FORMATCODE_IMAGE_PICT;
    else if (ext == L"png")
        fmt = WMDM_FORMATCODE_IMAGE_PNG;
    else if (ext == L"wma")
        fmt = WMDM_FORMATCODE_WMA;
    else if (ext == L"wpl")
        fmt = WMDM_FORMATCODE_WPLPLAYLIST;
    else if (ext == L"asx")
        fmt = WMDM_FORMATCODE_ASXPLAYLIST;
    else if (ext == L"m3u")
        fmt = WMDM_FORMATCODE_M3UPLAYLIST;
    else if (ext == L"wmv")
        fmt = WMDM_FORMATCODE_WMV;
    else if (ext == L"jpg" || ext == L"jpeg" || ext == L"jpe")
        fmt = WMDM_FORMATCODE_IMAGE_EXIF;
    else if (ext == L"jp2")
        fmt = WMDM_FORMATCODE_IMAGE_JP2;
    else if (ext == L"jpx" || ext == L"jpf")
        fmt = WMDM_FORMATCODE_IMAGE_JPX;

    // If we couldn't get the type from the extension, perhaps DirectShow 
    // can determine the type. You could also modify this to verify that 
    // the major media type matches the file extension (for example, that 
    // a .gif file has a video image stream with a bit rate of zero).
    if (fmt == WMDM_FORMATCODE_UNDEFINED)
    {
        CComPtr<IMediaDet> pIMediaDet;
        hr = pIMediaDet.CoCreateInstance(CLSID_MediaDet, NULL);
        if (hr == S_OK && pIMediaDet != NULL)
        {
            hr = pIMediaDet->put_Filename(BSTR(pFileName));
            if (FAILED(hr)) return WMDM_FORMATCODE_UNDEFINED;

            AM_MEDIA_TYPE mediaType;
            if (hr == S_OK)
            {
                hr = pIMediaDet->get_StreamMediaType(&mediaType);
                CHECK_HR(hr, 
                  "get_StreamMediaType succeeded in myGetWMDM_FORMATCODE.", 
                  "get_StreamMediaType failed in myGetWMDM_FORMATCODE.");
            }

            if (hr == S_OK)
            {
                LONG numStreams = 0;
                hr = pIMediaDet->get_OutputStreams(&numStreams);

                // If there is at least one video stream, the file is video. 
                // If there are only audio streams, it is audio.
                // Loop through all streams or until first video stream is found.
                for (int i = 0; i < numStreams; i++)
                {
                    // Choices are either VIDEOINFOHEADER or WAVEFORMATEX. 
                    // VIDEOINFOHEADER2 is not supported.
                    if (IsEqualGUID(mediaType.formattype, 
                        FORMAT_VideoInfo))
                    {
                        VIDEOINFOHEADER* data = 
                            (VIDEOINFOHEADER*) mediaType.pbFormat;

                        // If only one stream and there was no matching 
                        // extension, it is undefined video. If no 
                        // bit rate, it's a still image.
                        if (data->dwBitRate == 0) fmt = 
                            WMDM_FORMATCODE_WINDOWSIMAGEFORMAT;
                        else fmt = WMDM_FORMATCODE_UNDEFINEDVIDEO;
                        break; // Found video--any additional streams are soundtracks.
                    }
                    if (IsEqualGUID(mediaType.formattype, FORMAT_WaveFormatEx))
                    {
                        // If only one stream and there was no matching 
                        // extension, it is undefined audio. 
                        if (fmt == WMDM_FORMATCODE_UNDEFINED)
                        {
                            fmt = WMDM_FORMATCODE_UNDEFINEDAUDIO;
                        }
                        WAVEFORMATEX* data = 
                            (WAVEFORMATEX*) mediaType.pbFormat;
                    }
                } // Loop through streams.
            }     // Got a stream media type.
        }         // Created a media detector object.
    }
    return fmt;
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Escribir archivos en el dispositivo**](writing-files-to-the-device.md)
</dt> </dl>

 

 




