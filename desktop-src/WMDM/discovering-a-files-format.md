---
title: Detección del formato de un archivo
description: Detección del formato de un archivo
ms.assetid: f1b3f811-8161-41ca-a92c-2735c0bec2e8
keywords:
- Administrador de dispositivos de Windows Media, formatos de archivo
- Administrador de dispositivos, formatos de archivo
- Guía de programación, formatos de archivo
- aplicaciones de escritorio, formatos de archivo
- crear aplicaciones de Windows Media Administrador de dispositivos, formatos de archivo
- escribir archivos en dispositivos, formatos de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b06c963b01e3b681fd078d8685e1c788c73352e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775240"
---
# <a name="discovering-a-files-format"></a><span data-ttu-id="05b46-109">Detección del formato de un archivo</span><span class="sxs-lookup"><span data-stu-id="05b46-109">Discovering a File's Format</span></span>

<span data-ttu-id="05b46-110">Antes de enviar un archivo al dispositivo, una aplicación debe determinar si el dispositivo admite ese formato de archivo.</span><span class="sxs-lookup"><span data-stu-id="05b46-110">Before sending a file to the device, an application should determine whether the device supports that file format.</span></span>

<span data-ttu-id="05b46-111">Detectar el formato de un archivo puede ser complejo.</span><span class="sxs-lookup"><span data-stu-id="05b46-111">Discovering the format of a file can be complex.</span></span> <span data-ttu-id="05b46-112">La manera más sencilla consiste en crear una lista de extensiones de archivo asignadas a \_ valores de enumeración de FORMATCODE de WMDM específicos.</span><span class="sxs-lookup"><span data-stu-id="05b46-112">The simplest way is to create a list of file extensions mapped to specific WMDM\_FORMATCODE enumeration values.</span></span> <span data-ttu-id="05b46-113">Sin embargo, hay algunos problemas con este sistema: uno es que un único formato puede tener varias extensiones (por ejemplo,. jpg,. jpe y. JPEG para imágenes JPEG).</span><span class="sxs-lookup"><span data-stu-id="05b46-113">However, there are a few problems with this system: one is that a single format can have multiple extensions (such as .jpg, .jpe, and .jpeg for JPEG images).</span></span> <span data-ttu-id="05b46-114">Además, los distintos programas pueden usar la misma extensión de archivo para distintos formatos.</span><span class="sxs-lookup"><span data-stu-id="05b46-114">Also, the same file extension can be used by different programs for different formats.</span></span>

<span data-ttu-id="05b46-115">Para superar las limitaciones de una asignación estricta, es mejor que una aplicación Compruebe que el formato coincide con la extensión.</span><span class="sxs-lookup"><span data-stu-id="05b46-115">To overcome the limitations of a strict mapping, it is best for an application to verify that the format matches the extension.</span></span> <span data-ttu-id="05b46-116">El SDK de DirectShow proporciona herramientas que permiten a una aplicación detectar un conjunto limitado de detalles sobre la mayoría de los tipos de archivos multimedia.</span><span class="sxs-lookup"><span data-stu-id="05b46-116">The DirectShow SDK provides tools that enable an application to discover a limited set of details about most media file types.</span></span> <span data-ttu-id="05b46-117">El SDK de Windows Media Format expone un gran número de detalles, pero solo sobre archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="05b46-117">The Windows Media Format SDK exposes a large number of details, but only about ASF files.</span></span> <span data-ttu-id="05b46-118">Dado que todos los tipos de archivo deben tener su código de formato comprobado si es posible, por lo tanto, es mejor usar DirectShow para detectar o comprobar el código de formato básico y usar el SDK de Windows Media Format para detectar los metadatos adicionales deseados sobre los archivos ASF.</span><span class="sxs-lookup"><span data-stu-id="05b46-118">Because all file types should have their format code verified if possible, it is therefore best to use DirectShow to discover or verify the basic format code, and use the Windows Media Format SDK to discover any additional metadata desired about ASF files.</span></span> <span data-ttu-id="05b46-119">DirectShow también se puede usar para detectar metadatos básicos para archivos no ASF.</span><span class="sxs-lookup"><span data-stu-id="05b46-119">DirectShow can also be used to discover basic metadata for non-ASF files.</span></span>

<span data-ttu-id="05b46-120">A continuación se facilita una manera de detectar un formato de archivo mediante la asignación de extensiones y DirectShow.</span><span class="sxs-lookup"><span data-stu-id="05b46-120">The following is one way to discover a file format using extension mapping and DirectShow.</span></span>

<span data-ttu-id="05b46-121">En primer lugar, compare la extensión de nombre de archivo con una lista de extensiones conocidas.</span><span class="sxs-lookup"><span data-stu-id="05b46-121">First, compare the file name extension to a list of known extensions.</span></span> <span data-ttu-id="05b46-122">Asegúrese de hacer que la comparación no distinga mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="05b46-122">Be sure to make your comparison case-insensitive.</span></span> <span data-ttu-id="05b46-123">Si la extensión no está asignada, establezca el formato en WMDM \_ FORMATCODE sin \_ definir.</span><span class="sxs-lookup"><span data-stu-id="05b46-123">If the extension is not mapped, set the format to WMDM\_FORMATCODE\_UNDEFINED.</span></span>

-   <span data-ttu-id="05b46-124">Si no se encuentra el código de formato (o si desea comprobar que un archivo es un archivo multimedia), puede realizar los pasos siguientes:</span><span class="sxs-lookup"><span data-stu-id="05b46-124">If the format code was not found (or you want to verify that a file is a media file), you can perform the following steps:</span></span>
    1.  <span data-ttu-id="05b46-125">Cree un objeto de detector de medios de DirectShow mediante **CoCreateInstance**(CLSID \_ MediaDet) y recupere la interfaz **IMediaDet** .</span><span class="sxs-lookup"><span data-stu-id="05b46-125">Create a DirectShow Media Detector object using **CoCreateInstance**(CLSID\_MediaDet), and retrieving the **IMediaDet** interface.</span></span>
    2.  <span data-ttu-id="05b46-126">Abra el archivo mediante una llamada a **IMediaDet::p UT \_ nombreDeArchivo**.</span><span class="sxs-lookup"><span data-stu-id="05b46-126">Open the file by calling **IMediaDet::put\_Filename**.</span></span> <span data-ttu-id="05b46-127">Esta llamada producirá un error si el archivo está protegido.</span><span class="sxs-lookup"><span data-stu-id="05b46-127">This call will fail if the file is protected.</span></span>
    3.  <span data-ttu-id="05b46-128">Obtiene el tipo de medio del flujo predeterminado mediante una llamada a **IMediaDet:: get \_ StreamMediaType**, que devuelve un **\_ \_ tipo de medio am**.</span><span class="sxs-lookup"><span data-stu-id="05b46-128">Get the media type of the default stream by calling **IMediaDet::get\_StreamMediaType**, which returns an **AM\_MEDIA\_TYPE**.</span></span>
    4.  <span data-ttu-id="05b46-129">Obtiene el número de secuencias mediante una llamada a **IMediaDet:: get \_ OutputStreams**.</span><span class="sxs-lookup"><span data-stu-id="05b46-129">Get the number of streams by calling **IMediaDet::get\_OutputStreams**.</span></span>
        -   <span data-ttu-id="05b46-130">Si solo hay una secuencia y es audio, el tipo de archivo es WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO</span><span class="sxs-lookup"><span data-stu-id="05b46-130">If there is only one stream and it is audio, the file type is WMDM\_FORMATCODE\_UNDEFINEDAUDIO</span></span>
        -   <span data-ttu-id="05b46-131">Si solo hay una secuencia y se trata de un vídeo, el tipo de archivo es WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO</span><span class="sxs-lookup"><span data-stu-id="05b46-131">If there is only one stream and it is video, the file type is WMDM\_FORMATCODE\_UNDEFINEDVIDEO</span></span>
        -   <span data-ttu-id="05b46-132">Si solo hay una secuencia y se trata de un vídeo y la velocidad de bits es cero, el tipo de archivo es WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT.</span><span class="sxs-lookup"><span data-stu-id="05b46-132">If there is only one stream and it is video and the bit rate is zero, the file type is WMDM\_FORMATCODE\_WINDOWSIMAGEFORMAT.</span></span>

<span data-ttu-id="05b46-133">También puede intentar hacer coincidir códecs de audio o vídeo con los miembros **VIDEOINFOHEADER** o **WAVEFORMATEX** recuperados de **Get \_ StreamMediaType**.</span><span class="sxs-lookup"><span data-stu-id="05b46-133">You could also try matching audio or video codecs from the **VIDEOINFOHEADER** or **WAVEFORMATEX** members retrieved from **get\_StreamMediaType**.</span></span>

<span data-ttu-id="05b46-134">La siguiente función de C++ muestra la coincidencia de la extensión de archivo y el uso de DirectShow para intentar analizar archivos desconocidos.</span><span class="sxs-lookup"><span data-stu-id="05b46-134">The following C++ function demonstrates file extension matching and using DirectShow to try to analyze unknown files.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="05b46-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="05b46-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05b46-136">**Escribir archivos en el dispositivo**</span><span class="sxs-lookup"><span data-stu-id="05b46-136">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




