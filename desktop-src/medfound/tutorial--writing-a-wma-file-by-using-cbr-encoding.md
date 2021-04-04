---
description: En este tutorial se muestra cómo escribir un nuevo archivo de audio (. WMA) extrayendo contenido multimedia de un archivo de audio sin comprimir (. wav) y, a continuación, comprimirlo en formato ASF.
ms.assetid: f310c6ed-52e7-4828-9d4c-2f7ced9080c5
title: 'Tutorial: escribir un archivo WMA con objetos WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d156b75ced6cde2953ec90362ed13b0cc53bb83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908634"
---
# <a name="tutorial-writing-a-wma-file-by-using-wmcontainer-objects"></a><span data-ttu-id="6ace6-103">Tutorial: escribir un archivo WMA con objetos WMContainer</span><span class="sxs-lookup"><span data-stu-id="6ace6-103">Tutorial: Writing a WMA File by Using WMContainer Objects</span></span>

<span data-ttu-id="6ace6-104">En este tutorial se muestra cómo escribir un nuevo archivo de audio (. WMA) extrayendo contenido multimedia de un archivo de audio sin comprimir (. wav) y, a continuación, comprimirlo en formato ASF.</span><span class="sxs-lookup"><span data-stu-id="6ace6-104">This tutorial demonstrates writing a new audio file (.wma) by extracting media content from an uncompressed audio file (.wav) and then compressing it in ASF format.</span></span> <span data-ttu-id="6ace6-105">El modo de codificación utilizado para la conversión es la [codificación de velocidad de bits constante](constant-bit-rate-encoding.md) (CBR).</span><span class="sxs-lookup"><span data-stu-id="6ace6-105">The encoding mode used for the conversion is [Constant Bit Rate Encoding](constant-bit-rate-encoding.md) (CBR).</span></span> <span data-ttu-id="6ace6-106">En este modo, antes de la sesión de codificación, la aplicación especifica una velocidad de bits de destino que el codificador debe lograr.</span><span class="sxs-lookup"><span data-stu-id="6ace6-106">In this mode, before the encoding session, the application specifies a target bit rate that the encoder must achieve.</span></span>

<span data-ttu-id="6ace6-107">En este tutorial, creará una aplicación de consola que toma los nombres de archivo de entrada y salida como argumentos.</span><span class="sxs-lookup"><span data-stu-id="6ace6-107">In this tutorial, you will create a console application that takes the input and output filenames as arguments.</span></span> <span data-ttu-id="6ace6-108">La aplicación obtiene los ejemplos de medios sin comprimir de una aplicación de análisis de archivos de onda, que se proporciona con este tutorial.</span><span class="sxs-lookup"><span data-stu-id="6ace6-108">The application gets the uncompressed media samples from a wave file parsing application, which is provided with this tutorial.</span></span> <span data-ttu-id="6ace6-109">Estos ejemplos se envían al codificador para convertirlos al formato Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="6ace6-109">These samples are sent to the encoder for conversion to Windows Media Audio 9 format.</span></span> <span data-ttu-id="6ace6-110">El codificador está configurado para la codificación CBR y usa la primera velocidad de bits disponible durante la negociación de tipos de medios como la velocidad de bits de destino.</span><span class="sxs-lookup"><span data-stu-id="6ace6-110">The encoder is configured for CBR encoding and uses the first bit rate available during media type negotiation as the target bit rate.</span></span> <span data-ttu-id="6ace6-111">Los ejemplos codificados se envían al multiplexor para la packetización en formato de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="6ace6-111">The encoded samples are sent to the multiplexer for packetization in ASF data format.</span></span> <span data-ttu-id="6ace6-112">Estos paquetes se escribirán en una secuencia de bytes que representa el objeto de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="6ace6-112">These packets will be written to a byte stream that represents the ASF Data Object.</span></span> <span data-ttu-id="6ace6-113">Una vez que la sección de datos esté lista, creará un archivo de audio ASF y escribirá el nuevo objeto de encabezado ASF que consolida toda la información de encabezado y, a continuación, anexa la secuencia de bytes del objeto de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="6ace6-113">After the data section is ready, you will create an ASF audio file and write the new ASF Header Object that consolidates all the header information and then append the ASF Data Object byte stream.</span></span>

<span data-ttu-id="6ace6-114">Este tutorial contiene las siguientes secciones:</span><span class="sxs-lookup"><span data-stu-id="6ace6-114">This tutorial contains the following sections:</span></span>

-   [<span data-ttu-id="6ace6-115">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6ace6-115">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="6ace6-116">Terminología</span><span class="sxs-lookup"><span data-stu-id="6ace6-116">Terminology</span></span>](#terminology)
-   [<span data-ttu-id="6ace6-117">1. configurar el proyecto</span><span class="sxs-lookup"><span data-stu-id="6ace6-117">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="6ace6-118">2. declarar funciones auxiliares</span><span class="sxs-lookup"><span data-stu-id="6ace6-118">2. Declare Helper Functions</span></span>](#2-declare-helper-functions)
-   [<span data-ttu-id="6ace6-119">3. abrir un archivo de audio</span><span class="sxs-lookup"><span data-stu-id="6ace6-119">3. Open an Audio File</span></span>](#3-open-an-audio-file)
-   [<span data-ttu-id="6ace6-120">4. configurar el codificador</span><span class="sxs-lookup"><span data-stu-id="6ace6-120">4. Configure the Encoder</span></span>](#4-configure-the-encoder)
-   [<span data-ttu-id="6ace6-121">5. cree el objeto ContentInfo de ASF.</span><span class="sxs-lookup"><span data-stu-id="6ace6-121">5. Create the ASF ContentInfo object.</span></span>](#5-create-the-asf-contentinfo-object)
-   [<span data-ttu-id="6ace6-122">6. crear el multiplexor de ASF</span><span class="sxs-lookup"><span data-stu-id="6ace6-122">6. Create the ASF Multiplexer</span></span>](#6-create-the-asf-multiplexer)
-   [<span data-ttu-id="6ace6-123">7. generar nuevos paquetes de datos ASF</span><span class="sxs-lookup"><span data-stu-id="6ace6-123">7. Generate New ASF Data Packets</span></span>](#7-generate-new-asf-data-packets)
-   [<span data-ttu-id="6ace6-124">8. escribir el archivo ASF</span><span class="sxs-lookup"><span data-stu-id="6ace6-124">8. Write the ASF File</span></span>](#8-write-the-asf-file)
-   [<span data-ttu-id="6ace6-125">9. definir la función Entry-Point</span><span class="sxs-lookup"><span data-stu-id="6ace6-125">9. Define the Entry-Point Function</span></span>](#9-define-the-entry-point-function)
-   [<span data-ttu-id="6ace6-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ace6-126">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="6ace6-127">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="6ace6-127">Prerequisites</span></span>

<span data-ttu-id="6ace6-128">En este tutorial se da por hecho lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="6ace6-128">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="6ace6-129">Está familiarizado con la estructura de un archivo ASF y los componentes proporcionados por Media Foundation para trabajar con objetos ASF.</span><span class="sxs-lookup"><span data-stu-id="6ace6-129">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="6ace6-130">Estos componentes incluyen los objetos ContentInfo, Splitter, multiplexor y Profile.</span><span class="sxs-lookup"><span data-stu-id="6ace6-130">These components include ContentInfo, splitter, multiplexer, and profile objects.</span></span> <span data-ttu-id="6ace6-131">Para obtener más información, consulte [WMCONTAINER ASF Components](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="6ace6-131">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="6ace6-132">Está familiarizado con los codificadores de Windows Media y con los distintos tipos de codificación, especialmente CBR.</span><span class="sxs-lookup"><span data-stu-id="6ace6-132">You are familiar with Windows Media encoders, and the various encoding types, particularly CBR.</span></span> <span data-ttu-id="6ace6-133">Para obtener más información, consulte [codificadores de Windows Media](windows-media-encoders.md) .</span><span class="sxs-lookup"><span data-stu-id="6ace6-133">For more information, see [Windows Media Encoders](windows-media-encoders.md) .</span></span>
-   <span data-ttu-id="6ace6-134">Está familiarizado con los [búferes multimedia](media-buffers.md) y los flujos de bytes: en concreto, las operaciones de archivo que usan un flujo de bytes y la escritura del contenido de un búfer multimedia en una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="6ace6-134">You are familiar with [Media Buffers](media-buffers.md) and byte streams: Specifically, file operations using a byte stream, and writing the contents of a media buffer to a byte stream.</span></span>

## <a name="terminology"></a><span data-ttu-id="6ace6-135">Terminología</span><span class="sxs-lookup"><span data-stu-id="6ace6-135">Terminology</span></span>

<span data-ttu-id="6ace6-136">En este tutorial se usan los siguientes términos:</span><span class="sxs-lookup"><span data-stu-id="6ace6-136">This tutorial uses the following terms:</span></span>

-   <span data-ttu-id="6ace6-137">Tipo de medio de origen: objeto de tipo de medio, expone la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , que describe el contenido del archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="6ace6-137">Source media type: Media type object, exposes [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which describes the contents of the input file.</span></span>
-   <span data-ttu-id="6ace6-138">Perfil de audio: objeto de perfil, expone la interfaz [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , que solo contiene secuencias de audio del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="6ace6-138">Audio profile: Profile object, exposes [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface, which contains only audio streams of the output file.</span></span>
-   <span data-ttu-id="6ace6-139">Stream Sample: ejemplo multimedia, expone la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , representa los datos multimedia del archivo de entrada obtenidos del codificador en un estado comprimido.</span><span class="sxs-lookup"><span data-stu-id="6ace6-139">Stream sample: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, represents the input file's media data obtained from the encoder in a compressed state.</span></span>
-   <span data-ttu-id="6ace6-140">Objeto ContentInfo: el [objeto ContentInfo de ASF](asf-contentinfo-object.md), expone la interfaz [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , que representa el objeto de encabezado ASF del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="6ace6-140">ContentInfo object: [ASF ContentInfo Object](asf-contentinfo-object.md), exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the output file.</span></span>
-   <span data-ttu-id="6ace6-141">Secuencia de bytes de datos: objeto de secuencia de bytes, expone la interfaz [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que representa la parte del objeto de datos ASF completa del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="6ace6-141">Data byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which represents the entire ASF Data Object portion of the output file.</span></span>
-   <span data-ttu-id="6ace6-142">Paquete de datos: ejemplo multimedia, expone la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , generada por el [multiplexor ASF](asf-multiplexer.md); representa un paquete de datos ASF que se escribirá en la secuencia de bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="6ace6-142">Data packet: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the [ASF Multiplexer](asf-multiplexer.md); represents an ASF data packet that will be written to the data byte stream.</span></span>
-   <span data-ttu-id="6ace6-143">Secuencia de bytes de salida: objeto de flujo de bytes, expone la interfaz [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que incluye el contenido del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="6ace6-143">Output byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the output file.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="6ace6-144">1. configurar el proyecto</span><span class="sxs-lookup"><span data-stu-id="6ace6-144">1. Set up the Project</span></span>

1.  <span data-ttu-id="6ace6-145">Incluya los siguientes encabezados en el archivo de código fuente:</span><span class="sxs-lookup"><span data-stu-id="6ace6-145">Include the following headers in your source file:</span></span>

    ```C++
    #include <new>
    #include <stdio.h>       // Standard I/O
    #include <windows.h>     // Windows headers
    #include <mfapi.h>       // Media Foundation platform
    #include <wmcontainer.h> // ASF interfaces
    #include <mferror.h>     // Media Foundation error codes
    ```

    

2.  <span data-ttu-id="6ace6-146">Vínculo a los siguientes archivos de biblioteca:</span><span class="sxs-lookup"><span data-stu-id="6ace6-146">Link to the following library files:</span></span>

    -   <span data-ttu-id="6ace6-147">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="6ace6-147">mfplat.lib</span></span>
    -   <span data-ttu-id="6ace6-148">MF. lib</span><span class="sxs-lookup"><span data-stu-id="6ace6-148">mf.lib</span></span>
    -   <span data-ttu-id="6ace6-149">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="6ace6-149">mfuuid.lib</span></span>

3.  <span data-ttu-id="6ace6-150">Declare la función [SafeRelease](saferelease.md) .</span><span class="sxs-lookup"><span data-stu-id="6ace6-150">Declare the [SafeRelease](saferelease.md) function.</span></span>
4.  <span data-ttu-id="6ace6-151">Incluya la clase CWmaEncoder en el proyecto.</span><span class="sxs-lookup"><span data-stu-id="6ace6-151">Include the CWmaEncoder class in your project.</span></span> <span data-ttu-id="6ace6-152">Para obtener el código fuente completo de esta clase, vea [código de ejemplo del codificador](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="6ace6-152">For the complete source code of this class, see [Encoder Example Code](encoder-example-code.md).</span></span>

## <a name="2-declare-helper-functions"></a><span data-ttu-id="6ace6-153">2. declarar funciones auxiliares</span><span class="sxs-lookup"><span data-stu-id="6ace6-153">2. Declare Helper Functions</span></span>

<span data-ttu-id="6ace6-154">En este tutorial se usan las siguientes funciones auxiliares para leer y escribir en una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="6ace6-154">This tutorial uses the following helper functions to read and write from a byte stream.</span></span>

-   <span data-ttu-id="6ace6-155">`AppendToByteStream`: Anexa el contenido de una secuencia de bytes a otra secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="6ace6-155">`AppendToByteStream`: Appends the contents of one byte stream to another byte stream.</span></span>
-   <span data-ttu-id="6ace6-156">WriteBufferToByteStream: escribe datos de un búfer multimedia en una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="6ace6-156">WriteBufferToByteStream: Writes data from a media buffer to a byte stream.</span></span>

<span data-ttu-id="6ace6-157">Para obtener más información, vea [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="6ace6-157">For more information, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span> <span data-ttu-id="6ace6-158">En el código siguiente se muestran estas funciones auxiliares:</span><span class="sxs-lookup"><span data-stu-id="6ace6-158">The following code shows these helper functions:</span></span>


```C++
//-------------------------------------------------------------------
// AppendToByteStream
//
// Reads the contents of pSrc and writes them to pDest.
//-------------------------------------------------------------------

HRESULT AppendToByteStream(IMFByteStream *pSrc, IMFByteStream *pDest)
{
    HRESULT hr = S_OK;

    const DWORD READ_SIZE = 1024;

    BYTE buffer[READ_SIZE];

    while (1)
    {
        ULONG cbRead;

        hr = pSrc->Read(buffer, READ_SIZE, &cbRead);

        if (FAILED(hr)) { break; }

        if (cbRead == 0)
        {
            break;
        }

        hr = pDest->Write(buffer, cbRead, &cbRead);

        if (FAILED(hr)) { break; }
    }

    return hr;
}
```




```C++
//-------------------------------------------------------------------
// WriteBufferToByteStream
//
// Writes data from a media buffer to a byte stream.
//-------------------------------------------------------------------

HRESULT WriteBufferToByteStream(
    IMFByteStream *pStream,   // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,  // Pointer to the media buffer.
    DWORD *pcbWritten         // Receives the number of bytes written.
    )
{
    HRESULT hr = S_OK;
    DWORD cbData = 0;
    DWORD cbWritten = 0;
    BYTE *pMem = NULL;

    hr = pBuffer->Lock(&pMem, NULL, &cbData);

    if (SUCCEEDED(hr))
    {
        hr = pStream->Write(pMem, cbData, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        if (pcbWritten)
        {
            *pcbWritten = cbWritten;
        }
    }

    if (pMem)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



## <a name="3-open-an-audio-file"></a><span data-ttu-id="6ace6-159">3. abrir un archivo de audio</span><span class="sxs-lookup"><span data-stu-id="6ace6-159">3. Open an Audio File</span></span>

<span data-ttu-id="6ace6-160">En este tutorial se da por supuesto que la aplicación generará audio sin comprimir para la codificación.</span><span class="sxs-lookup"><span data-stu-id="6ace6-160">This tutorial assumes that your application will generate uncompressed audio for encoding.</span></span> <span data-ttu-id="6ace6-161">Para ello, se declaran dos funciones en este tutorial:</span><span class="sxs-lookup"><span data-stu-id="6ace6-161">For that purpose, two functions are declared in this tutorial:</span></span>


```C++
HRESULT OpenAudioFile(PCWSTR pszURL, IMFMediaType **ppAudioFormat);
HRESULT GetNextAudioSample(BOOL *pbEOS, IMFSample **ppSample);
```



<span data-ttu-id="6ace6-162">La implementación de estas funciones se deja al lector.</span><span class="sxs-lookup"><span data-stu-id="6ace6-162">The implementation of these functions is left to the reader.</span></span>

-   <span data-ttu-id="6ace6-163">La `OpenAudioFile` función debe abrir el archivo multimedia especificado por *pszURL* y devolver un puntero a un tipo de medio que describe una secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="6ace6-163">The `OpenAudioFile` function should open the media file specified by *pszURL* and return a pointer to a media type that describes an audio stream.</span></span>
-   <span data-ttu-id="6ace6-164">La `GetNextAudioSample` función debe leer el audio PCM sin comprimir del archivo que abrió `OpenAudioFile` .</span><span class="sxs-lookup"><span data-stu-id="6ace6-164">The `GetNextAudioSample` function should read uncompressed PCM audio from the file that was opened by `OpenAudioFile`.</span></span> <span data-ttu-id="6ace6-165">Cuando se alcanza el final del archivo, *pbEOS* recibe el valor **true**.</span><span class="sxs-lookup"><span data-stu-id="6ace6-165">When the end of the file is reached, *pbEOS* receives the value **TRUE**.</span></span> <span data-ttu-id="6ace6-166">De lo contrario, *ppSample* recibe un ejemplo multimedia que contiene el búfer de audio.</span><span class="sxs-lookup"><span data-stu-id="6ace6-166">Otherwise, *ppSample* receives a media sample that contains the audio buffer.</span></span>

## <a name="4-configure-the-encoder"></a><span data-ttu-id="6ace6-167">4. configurar el codificador</span><span class="sxs-lookup"><span data-stu-id="6ace6-167">4. Configure the Encoder</span></span>

<span data-ttu-id="6ace6-168">A continuación, cree el codificador, configúrelo para que genere ejemplos de secuencias con codificación CBR y negocie los tipos de medios de entrada y salida.</span><span class="sxs-lookup"><span data-stu-id="6ace6-168">Next, create the encoder, configure it to produce CBR-encoded stream samples, and negotiate the input and the output media types.</span></span>

<span data-ttu-id="6ace6-169">En Media Foundation, los codificadores (exponer la interfaz [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ) se implementan como [transformaciones Media Foundation](media-foundation-transforms.md) (MFT).</span><span class="sxs-lookup"><span data-stu-id="6ace6-169">In Media Foundation, encoders (expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface) are implemented as [Media Foundation Transforms](media-foundation-transforms.md) (MFT).</span></span>

<span data-ttu-id="6ace6-170">En este tutorial, el codificador se implementa en la `CWmaEncoder` clase que proporciona un contenedor para la MFT.</span><span class="sxs-lookup"><span data-stu-id="6ace6-170">In this tutorial, the encoder is implemented in the `CWmaEncoder` class that provides a wrapper for the MFT.</span></span> <span data-ttu-id="6ace6-171">Para obtener el código fuente completo de esta clase, vea [código de ejemplo del codificador](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="6ace6-171">For the complete source code of this class, see [Encoder Example Code](encoder-example-code.md).</span></span>

> [!Note]  
> <span data-ttu-id="6ace6-172">Opcionalmente, puede especificar el tipo de codificación como CBR.</span><span class="sxs-lookup"><span data-stu-id="6ace6-172">You can optionally specify the encoding type as CBR.</span></span> <span data-ttu-id="6ace6-173">De forma predeterminada, el codificador está configurado para usar codificación CBR.</span><span class="sxs-lookup"><span data-stu-id="6ace6-173">By default, the encoder is configured to use CBR encoding.</span></span> <span data-ttu-id="6ace6-174">Para obtener más información, consulte [codificación de velocidad de bits constante](constant-bit-rate-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="6ace6-174">For more information, see [Constant Bit Rate Encoding](constant-bit-rate-encoding.md).</span></span> <span data-ttu-id="6ace6-175">Puede establecer propiedades adicionales en función del tipo de codificación, para obtener información sobre las propiedades que son específicas de un modo de codificación, consulte codificación de [velocidad de bits variable basada en la calidad](quality-based-variable-bit-rate--vbr--encoding.md), [codificación de velocidad](unconstrained-variable-bit-rate--vbr--encoding.md)de bits variable sin restricciones y [codificación de velocidad de bits variable restringida](peak-constrained-variable-bit-rate--vbr--encoding.md).</span><span class="sxs-lookup"><span data-stu-id="6ace6-175">You can set additional properties depending on the type of encoding, for information about the properties that are specific to an encoding mode, see [Quality-Based Variable Bit Rate Encoding](quality-based-variable-bit-rate--vbr--encoding.md), [Unconstrained Variable Bit Rate Encoding](unconstrained-variable-bit-rate--vbr--encoding.md), and [Peak-Constrained Variable Bit Rate Encoding](peak-constrained-variable-bit-rate--vbr--encoding.md).</span></span>

 


```C++
    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }
```



## <a name="5-create-the-asf-contentinfo-object"></a><span data-ttu-id="6ace6-176">5. cree el objeto ContentInfo de ASF.</span><span class="sxs-lookup"><span data-stu-id="6ace6-176">5. Create the ASF ContentInfo object.</span></span>

<span data-ttu-id="6ace6-177">El [objeto ContentInfo de ASF](asf-contentinfo-object.md) contiene información sobre los distintos objetos de encabezado del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="6ace6-177">The [ASF ContentInfo Object](asf-contentinfo-object.md) contains information about the various header objects of the output file.</span></span>

<span data-ttu-id="6ace6-178">En primer lugar, cree un perfil ASF para la secuencia de audio:</span><span class="sxs-lookup"><span data-stu-id="6ace6-178">First, create an ASF profile for the audio stream:</span></span>

1.  <span data-ttu-id="6ace6-179">Llame a [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) para crear un objeto de perfil ASF vacío.</span><span class="sxs-lookup"><span data-stu-id="6ace6-179">Call [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) to create an empty ASF profile object.</span></span> <span data-ttu-id="6ace6-180">El perfil ASF expone la interfaz [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) .</span><span class="sxs-lookup"><span data-stu-id="6ace6-180">The ASF profile exposes the [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface.</span></span> <span data-ttu-id="6ace6-181">Para obtener más información, vea [crear y configurar secuencias ASF](creating-and-configuring-asf-streams.md).</span><span class="sxs-lookup"><span data-stu-id="6ace6-181">For more information, see [Creating and Configuring ASF Streams](creating-and-configuring-asf-streams.md).</span></span>
2.  <span data-ttu-id="6ace6-182">Obtiene el formato de audio codificado del `CWmaEncoder` objeto.</span><span class="sxs-lookup"><span data-stu-id="6ace6-182">Get the encoded audio format from the `CWmaEncoder` object.</span></span>
3.  <span data-ttu-id="6ace6-183">Llame a [**IMFASFProfile:: CreateStream (**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) para crear una nueva secuencia para el perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="6ace6-183">Call [**IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) to create a new stream for the ASF profile.</span></span> <span data-ttu-id="6ace6-184">Pase un puntero a la interfaz [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) , que representa el formato del flujo.</span><span class="sxs-lookup"><span data-stu-id="6ace6-184">Pass in a pointer to the [**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) interface, which represents the stream format.</span></span>
4.  <span data-ttu-id="6ace6-185">Llame a [**IMFASFStreamConfig:: SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) para asignar un identificador de flujo.</span><span class="sxs-lookup"><span data-stu-id="6ace6-185">Call [**IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) to assign a stream identifier.</span></span>
5.  <span data-ttu-id="6ace6-186">Establezca los parámetros de "depósito de fugas" estableciendo el atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) en el objeto de secuencia.</span><span class="sxs-lookup"><span data-stu-id="6ace6-186">Set the "leaky bucket" parameters by setting the [**MF\_ASFSTREAMCONFIG\_LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) attribute on the stream object.</span></span>
6.  <span data-ttu-id="6ace6-187">Llame a [**IMFASFProfile:: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) para agregar el nuevo flujo al perfil.</span><span class="sxs-lookup"><span data-stu-id="6ace6-187">Call [**IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) to add the new stream to the profile.</span></span>

<span data-ttu-id="6ace6-188">Ahora, cree el objeto ASF ContentInfo como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="6ace6-188">Now create the ASF ContentInfo object as follows:</span></span>

1.  <span data-ttu-id="6ace6-189">Llame a [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para crear un objeto ContentInfo vacío.</span><span class="sxs-lookup"><span data-stu-id="6ace6-189">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create an empty ContentInfo object.</span></span>
2.  <span data-ttu-id="6ace6-190">Llame a [**IMFASFContentInfo:: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para establecer el perfil de ASF.</span><span class="sxs-lookup"><span data-stu-id="6ace6-190">Call [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) to set the ASF profile.</span></span>

<span data-ttu-id="6ace6-191">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="6ace6-191">The following code shows these steps:</span></span>


```C++
HRESULT CreateASFContentInfo(
    CWmaEncoder* pEncoder,
    IMFASFContentInfo** ppContentInfo
    )
{
    HRESULT hr = S_OK;
    
    IMFASFProfile* pProfile = NULL;
    IMFMediaType* pMediaType = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFASFContentInfo* pContentInfo = NULL;

    // Create the ASF profile object.

    hr = MFCreateASFProfile(&pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a stream description for the encoded audio.

    hr = pEncoder->GetOutputType(&pMediaType); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->CreateStream(pMediaType, &pStream); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetStreamNumber(DEFAULT_STREAM_NUMBER); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Set "leaky bucket" values.

    LeakyBucket bucket;

    hr = pEncoder->GetLeakyBucket1(&bucket);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pStream->SetBlob(
        MF_ASFSTREAMCONFIG_LEAKYBUCKET1, 
        (UINT8*)&bucket, 
        sizeof(bucket)
        );

    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile

    hr = pProfile->SetStream(pStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the ASF ContentInfo object.

    hr = MFCreateASFContentInfo(&pContentInfo); 
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContentInfo->SetProfile(pProfile); 
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.

    *ppContentInfo = pContentInfo;
    (*ppContentInfo)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pStream);
    SafeRelease(&pMediaType);
    SafeRelease(&pContentInfo);
    return hr;
}
```



## <a name="6-create-the-asf-multiplexer"></a><span data-ttu-id="6ace6-192">6. crear el multiplexor de ASF</span><span class="sxs-lookup"><span data-stu-id="6ace6-192">6. Create the ASF Multiplexer</span></span>

<span data-ttu-id="6ace6-193">El [multiplexor de ASF](asf-multiplexer.md) genera paquetes de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="6ace6-193">The [ASF Multiplexer](asf-multiplexer.md) generates ASF data packets.</span></span>

1.  <span data-ttu-id="6ace6-194">Llame a [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) para crear el multiplexor de ASF.</span><span class="sxs-lookup"><span data-stu-id="6ace6-194">Call [**MFCreateASFMultiplexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) to create the ASF multiplexer.</span></span>
2.  <span data-ttu-id="6ace6-195">Llame a [**IMFASFMultiplexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) para inicializar el multiplexor.</span><span class="sxs-lookup"><span data-stu-id="6ace6-195">Call [**IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) to initialize the multiplexer.</span></span> <span data-ttu-id="6ace6-196">Pase un puntero al objeto de información de contenido ASF, que se creó en la sección anterior.</span><span class="sxs-lookup"><span data-stu-id="6ace6-196">Pass in a pointer to the ASF Content Info object, which was created in the previous section.</span></span>
3.  <span data-ttu-id="6ace6-197">Llame a [**IMFASFMultiplexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) para establecer la marca de **velocidad de \_ \_ \_ bits autoajuste del multiplexor de MFASF** .</span><span class="sxs-lookup"><span data-stu-id="6ace6-197">Call [**IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) to set the **MFASF\_MULTIPLEXER\_AUTOADJUST\_BITRATE** flag.</span></span> <span data-ttu-id="6ace6-198">Cuando se usa esta configuración, el multiplexor ajusta automáticamente la velocidad de bits del contenido ASF para que coincida con las características de las secuencias que se multiplexan.</span><span class="sxs-lookup"><span data-stu-id="6ace6-198">When this setting is used, the multiplexer automatically adjusts the bit rate of the ASF content to match the characteristics of the streams being multiplexed.</span></span>


```C++
HRESULT CreateASFMux( 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer** ppMultiplexer
    )
{
    HRESULT hr = S_OK;
    
    IMFMediaType* pMediaType = NULL;
    IMFASFMultiplexer *pMultiplexer = NULL;

    // Create and initialize the ASF Multiplexer object.

    hr = MFCreateASFMultiplexer(&pMultiplexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pMultiplexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Enable automatic bit-rate adjustment.

    hr = pMultiplexer->SetFlags(MFASF_MULTIPLEXER_AUTOADJUST_BITRATE);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppMultiplexer = pMultiplexer;
    (*ppMultiplexer)->AddRef();

done:
    SafeRelease(&pMultiplexer);
    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a><span data-ttu-id="6ace6-199">7. generar nuevos paquetes de datos ASF</span><span class="sxs-lookup"><span data-stu-id="6ace6-199">7. Generate New ASF Data Packets</span></span>

<span data-ttu-id="6ace6-200">A continuación, genere paquetes de datos ASF para el nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="6ace6-200">Next, generate ASF data packets for the new file.</span></span> <span data-ttu-id="6ace6-201">Estos paquetes de datos constituirán el último objeto de datos ASF del nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="6ace6-201">These data packets will constitute the final ASF Data Object for the new file.</span></span> <span data-ttu-id="6ace6-202">Para generar nuevos paquetes de datos ASF:</span><span class="sxs-lookup"><span data-stu-id="6ace6-202">To generate new ASF data packets:</span></span>

1.  <span data-ttu-id="6ace6-203">Llame a [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) para crear una secuencia de bytes temporal que contenga los paquetes de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="6ace6-203">Call [**MFCreateTempFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) to create a temporary byte stream to hold the ASF data packets.</span></span>
2.  <span data-ttu-id="6ace6-204">Llame a la función definida por la aplicación `GetNextAudioSample` para obtener datos de audio sin comprimir para el codificador.</span><span class="sxs-lookup"><span data-stu-id="6ace6-204">Call the application-defined `GetNextAudioSample` function to get uncompressed audio data for the encoder.</span></span>
3.  <span data-ttu-id="6ace6-205">Pase el audio sin comprimir al codificador para la compresión.</span><span class="sxs-lookup"><span data-stu-id="6ace6-205">Pass the uncompressed audio to the encoder for compression.</span></span> <span data-ttu-id="6ace6-206">Para obtener más información, vea [procesar datos en el codificador](processing-data-in-the-encoder.md)</span><span class="sxs-lookup"><span data-stu-id="6ace6-206">For more information, see [Processing Data in the Encoder](processing-data-in-the-encoder.md)</span></span>
4.  <span data-ttu-id="6ace6-207">Llame a [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) para enviar las muestras de audio comprimidas al multiplexor de ASF para la packetización.</span><span class="sxs-lookup"><span data-stu-id="6ace6-207">Call [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) to send the compressed audio samples to the ASF multiplexer for packetization.</span></span>
5.  <span data-ttu-id="6ace6-208">Obtenga los paquetes ASF del multiplexor y escríbalos en la secuencia de bytes temporal.</span><span class="sxs-lookup"><span data-stu-id="6ace6-208">Get the ASF packets from the multiplexer and write them to the temporary byte stream.</span></span> <span data-ttu-id="6ace6-209">Para obtener más información, consulte [generación de nuevos paquetes de datos ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="6ace6-209">For more information, see [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>
6.  <span data-ttu-id="6ace6-210">Cuando llegue al final de la secuencia de origen, vacíe el codificador y extraiga los ejemplos comprimidos restantes del codificador.</span><span class="sxs-lookup"><span data-stu-id="6ace6-210">When you reach the end of the source stream, drain the encoder and pull the remaining compressed samples from the encoder.</span></span> <span data-ttu-id="6ace6-211">Para obtener más información acerca de cómo purgar una MFT, vea [modelo de procesamiento de MFT básico](basic-mft-processing-model.md).</span><span class="sxs-lookup"><span data-stu-id="6ace6-211">For more information about draining an MFT, see [Basic MFT Processing Model](basic-mft-processing-model.md).</span></span>
7.  <span data-ttu-id="6ace6-212">Después de enviar todas las muestras al multiplexor, llame a [**IMFASFMultiplexer:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) y extraiga los paquetes ASF restantes del multiplexor.</span><span class="sxs-lookup"><span data-stu-id="6ace6-212">After all samples are sent to the multiplexer, call [**IMFASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) and pull the remaining ASF packets from the multiplexer.</span></span>
8.  <span data-ttu-id="6ace6-213">Llame a [**IMFASFMultiplexer:: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).</span><span class="sxs-lookup"><span data-stu-id="6ace6-213">Call [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).</span></span>

<span data-ttu-id="6ace6-214">El código siguiente genera paquetes de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="6ace6-214">The following code generates ASF data packets.</span></span> <span data-ttu-id="6ace6-215">La función devuelve un puntero a una secuencia de bytes que contiene el objeto de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="6ace6-215">The function returns a pointer to a byte stream that contains the ASF Data Object.</span></span>


```C++
HRESULT EncodeData(
    CWmaEncoder* pEncoder, 
    IMFASFContentInfo* pContentInfo,
    IMFASFMultiplexer* pMux, 
    IMFByteStream** ppDataStream) 
{
    HRESULT hr = S_OK;

    IMFByteStream* pStream = NULL;
    IMFSample* pInputSample = NULL;
    IMFSample* pWmaSample = NULL;

    BOOL bEOF = FALSE;

   // Create a temporary file to hold the data stream.
   hr = MFCreateTempFile(
        MF_ACCESSMODE_READWRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        &pStream
        );

   if (FAILED(hr))
   {
       goto done;
   }

    BOOL bNeedInput = TRUE;

    while (TRUE)
    {
        if (bNeedInput)
        {
            hr = GetNextAudioSample(&bEOF, &pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            if (bEOF)
            {
                // Reached the end of the input file.
                break;
            }

            // Encode the uncompressed audio sample.
            hr = pEncoder->ProcessInput(pInputSample);
            if (FAILED(hr))
            {
                goto done;
            }

            bNeedInput = FALSE;
        }

        if (bNeedInput == FALSE)
        {
            // Get data from the encoder.

            hr = pEncoder->ProcessOutput(&pWmaSample);
            if (FAILED(hr))
            {
                goto done;
            }

            // pWmaSample can be NULL if the encoder needs more input.

            if (pWmaSample)
            {
                hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
                if (FAILED(hr))
                {
                    goto done;
                }

                //Collect the data packets and write them to a stream
                hr = GenerateASFDataPackets(pMux, pStream);
                if (FAILED(hr))
                {
                    goto done;
                }
            }
            else
            {
                bNeedInput = TRUE;
            }
        }
        
        SafeRelease(&pInputSample);
        SafeRelease(&pWmaSample);
    }

    // Drain the MFT and pull any remaining samples from the encoder.

    hr = pEncoder->Drain();
    if (FAILED(hr))
    {
        goto done;
    }

    while (TRUE)
    {
        hr = pEncoder->ProcessOutput(&pWmaSample);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pWmaSample == NULL)
        {
            break;
        }

        hr = pMux->ProcessSample(DEFAULT_STREAM_NUMBER, pWmaSample, 0);
        if (FAILED(hr))
        {
            goto done;
        }

        //Collect the data packets and write them to a stream
        hr = GenerateASFDataPackets(pMux, pStream);
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pWmaSample);
    }

    // Flush the mux and get any pending ASF data packets.
    hr = pMux->Flush();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GenerateASFDataPackets(pMux, pStream);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Update the ContentInfo object
    hr = pMux->End(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return stream to the caller that contains the ASF encoded data.
    *ppDataStream = pStream;
    (*ppDataStream)->AddRef();

done:
    SafeRelease(&pStream);
    SafeRelease(&pInputSample);
    SafeRelease(&pWmaSample);
    return hr;
}
```



<span data-ttu-id="6ace6-216">El código de la `GenerateASFDataPackets` función se muestra en el tema [generar nuevos paquetes de datos ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="6ace6-216">Code for the `GenerateASFDataPackets` function is shown in the topic [Generating New ASF Data Packets](generating-new-asf-data-packets.md).</span></span>

## <a name="8-write-the-asf-file"></a><span data-ttu-id="6ace6-217">8. escribir el archivo ASF</span><span class="sxs-lookup"><span data-stu-id="6ace6-217">8. Write the ASF File</span></span>

<span data-ttu-id="6ace6-218">Después, escriba el encabezado ASF en un búfer multimedia mediante una llamada a [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span><span class="sxs-lookup"><span data-stu-id="6ace6-218">Next, write the ASF header to a media buffer by calling [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="6ace6-219">Este método convierte los datos almacenados en el objeto ContentInfo en datos binarios en formato de objeto de encabezado ASF.</span><span class="sxs-lookup"><span data-stu-id="6ace6-219">This method converts data stored in the ContentInfo object into binary data in ASF Header Object format.</span></span> <span data-ttu-id="6ace6-220">Para obtener más información, vea [generar un nuevo objeto de encabezado ASF](generating-a-new-asf-header-object.md).</span><span class="sxs-lookup"><span data-stu-id="6ace6-220">For more information, see [Generating a New ASF Header Object](generating-a-new-asf-header-object.md).</span></span>

<span data-ttu-id="6ace6-221">Una vez generado el nuevo objeto de encabezado ASF, cree una secuencia de bytes para el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="6ace6-221">After the new ASF Header Object has been generated, create a byte stream for the output file.</span></span> <span data-ttu-id="6ace6-222">En primer lugar, escriba el objeto de encabezado en la secuencia de bytes de salida.</span><span class="sxs-lookup"><span data-stu-id="6ace6-222">First write the Header Object to the output byte stream.</span></span> <span data-ttu-id="6ace6-223">Siga el objeto de encabezado con el objeto de datos contenido en la secuencia de bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="6ace6-223">Follow the Header Object with the Data Object contained in the data byte stream.</span></span>


```C++
HRESULT WriteASFFile( 
     IMFASFContentInfo *pContentInfo, 
     IMFByteStream *pDataStream,
     PCWSTR pszFile
     )
{
    HRESULT hr = S_OK;
    
    IMFMediaBuffer* pHeaderBuffer = NULL;
    IMFByteStream* pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    //Create output file
    hr = MFCreateFile(MF_ACCESSMODE_WRITE, MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE, pszFile, &pWmaStream);

    if (FAILED(hr))
    {
        goto done;
    }


    // Get the size of the ASF Header Object.
    hr = pContentInfo->GenerateHeader (NULL, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a media buffer.
    hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Populate the media buffer with the ASF Header Object.
    hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF header to the output file.
    hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    if (FAILED(hr))
    {
        goto done;
    }

    // Append the data stream to the file.

    hr = pDataStream->SetCurrentPosition(0);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = AppendToByteStream(pDataStream, pWmaStream);

done:
    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);
    return hr;
}
```



## <a name="9-define-the-entry-point-function"></a><span data-ttu-id="6ace6-224">9. definir la función Entry-Point</span><span class="sxs-lookup"><span data-stu-id="6ace6-224">9. Define the Entry-Point Function</span></span>

<span data-ttu-id="6ace6-225">Ahora puede poner los pasos anteriores juntos en una aplicación completa.</span><span class="sxs-lookup"><span data-stu-id="6ace6-225">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="6ace6-226">Antes de usar cualquiera de los objetos Media Foundation, inicialice la plataforma de Media Foundation mediante una llamada a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="6ace6-226">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="6ace6-227">Cuando haya terminado, llame a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="6ace6-227">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="6ace6-228">Para obtener más información, vea [inicializar Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="6ace6-228">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>

<span data-ttu-id="6ace6-229">En el código siguiente se muestra la aplicación de consola completa.</span><span class="sxs-lookup"><span data-stu-id="6ace6-229">The following code shows the complete console application.</span></span> <span data-ttu-id="6ace6-230">El argumento de línea de comandos especifica el nombre del archivo que se va a convertir y el nombre del nuevo archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="6ace6-230">The command-line argument specifies the name of the file to convert and the name of the new audio file.</span></span>


```C++
int wmain(int argc, WCHAR* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma");
        return 0;
    }

    const WCHAR* sInputFileName = argv[1];    // Source file name
    const WCHAR* sOutputFileName = argv[2];  // Output file name
    
    IMFMediaType* pInputType = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFMultiplexer* pMux = NULL;
    IMFByteStream* pDataStream = NULL;

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    HRESULT hr = CoInitializeEx(
        NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);

    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    CWmaEncoder* pEncoder = NULL; //Pointer to the Encoder object.

    hr = OpenAudioFile(sInputFileName, &pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Initialize the WMA encoder wrapper.

    pEncoder = new (std::nothrow) CWmaEncoder();
    if (pEncoder == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    hr = pEncoder->Initialize();
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetEncodingType(EncodeMode_CBR);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pEncoder->SetInputType(pInputType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the WMContainer objects.
    hr = CreateASFContentInfo(pEncoder, &pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateASFMux(pContentInfo, &pMux);
    if (FAILED(hr))
    {
        goto done;
    }

    // Convert uncompressed data to ASF format.
    hr = EncodeData(pEncoder, pContentInfo, pMux, &pDataStream);
    if (FAILED(hr))
    {
        goto done;
    }

    // Write the ASF objects to the output file.
    hr = WriteASFFile(pContentInfo, pDataStream, sOutputFileName);

done:
    SafeRelease(&pInputType);
    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);
    SafeRelease(&pDataStream);
    delete pEncoder;

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }

    return 0;
} 
```



## <a name="related-topics"></a><span data-ttu-id="6ace6-231">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ace6-231">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ace6-232">Componentes de WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="6ace6-232">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="6ace6-233">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="6ace6-233">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



