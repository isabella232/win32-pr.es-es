---
description: Una manera de crear un archivo ASF es copiar secuencias ASF desde un archivo existente.
ms.assetid: 158fe3a1-42e6-461d-b56b-5419cd961fca
title: 'Tutorial: copiar secuencias ASF mediante objetos WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44bac13626a8c80f474eeb029db4eb1351273910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696874"
---
# <a name="tutorial-copying-asf-streams-by-using-wmcontainer-objects"></a><span data-ttu-id="8c67b-103">Tutorial: copiar secuencias ASF mediante objetos WMContainer</span><span class="sxs-lookup"><span data-stu-id="8c67b-103">Tutorial: Copying ASF Streams by Using WMContainer Objects</span></span>

<span data-ttu-id="8c67b-104">Una manera de crear un archivo ASF es copiar secuencias ASF desde un archivo existente.</span><span class="sxs-lookup"><span data-stu-id="8c67b-104">One way to create an ASF file is to copy ASF streams from an existing file.</span></span> <span data-ttu-id="8c67b-105">Para ello, puede recuperar los datos multimedia del archivo de origen y escribir en el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="8c67b-105">To do this, you can retrieve the media data from the source file and write to the output file.</span></span> <span data-ttu-id="8c67b-106">Si el archivo de origen es un archivo ASF, puede copiar ejemplos de secuencias sin descomprimirlos y volver a comprimirlos.</span><span class="sxs-lookup"><span data-stu-id="8c67b-106">If the source file is an ASF file, you can copy stream samples without decompressing and recompressing them.</span></span>

<span data-ttu-id="8c67b-107">En este tutorial se muestra este escenario mediante la extracción de la primera secuencia de audio de un archivo de audio y vídeo ASF (. wmv) y su copia en un nuevo archivo de audio ASF (. WMA).</span><span class="sxs-lookup"><span data-stu-id="8c67b-107">This tutorial demonstrates this scenario by extracting the first audio stream from an ASF audio-video file (.wmv) and copying it to a new ASF audio file (.wma).</span></span> <span data-ttu-id="8c67b-108">En este tutorial, creará una aplicación de consola que toma los nombres de archivo de entrada y salida como argumentos.</span><span class="sxs-lookup"><span data-stu-id="8c67b-108">In this tutorial, you will create a console application that takes the input and output filenames as arguments.</span></span> <span data-ttu-id="8c67b-109">La aplicación utiliza el divisor ASF para analizar los ejemplos de flujo de entrada y, a continuación, los envía al multiplexor ASF para escribir los paquetes de datos ASF para la secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="8c67b-109">The application uses the ASF Splitter to parse the input stream samples and then sends them to the ASF Multiplexer to write the ASF data packets for the audio stream.</span></span>

<span data-ttu-id="8c67b-110">Este tutorial contiene los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="8c67b-110">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="8c67b-111">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8c67b-111">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="8c67b-112">Terminología</span><span class="sxs-lookup"><span data-stu-id="8c67b-112">Terminology</span></span>](#terminology)
-   [<span data-ttu-id="8c67b-113">1. configurar el proyecto</span><span class="sxs-lookup"><span data-stu-id="8c67b-113">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="8c67b-114">2. declarar funciones auxiliares</span><span class="sxs-lookup"><span data-stu-id="8c67b-114">2. Declare Helper Functions</span></span>](#2-declare-helper-functions)
-   [<span data-ttu-id="8c67b-115">3. abrir el archivo ASF de entrada</span><span class="sxs-lookup"><span data-stu-id="8c67b-115">3. Open the Input ASF File</span></span>](#3-open-the-input-asf-file)
-   [<span data-ttu-id="8c67b-116">4. inicializar objetos para el archivo de entrada</span><span class="sxs-lookup"><span data-stu-id="8c67b-116">4. Initialize Objects for the Input File</span></span>](#4-initialize-objects-for-the-input-file)
-   [<span data-ttu-id="8c67b-117">5. crear un perfil de audio</span><span class="sxs-lookup"><span data-stu-id="8c67b-117">5. Create an Audio Profile</span></span>](#5-create-an-audio-profile)
-   [<span data-ttu-id="8c67b-118">6. inicializar los objetos para el archivo de salida</span><span class="sxs-lookup"><span data-stu-id="8c67b-118">6. Initialize Objects for the Output File</span></span>](#6-initialize-objects-for-the-output-file)
-   [<span data-ttu-id="8c67b-119">7. generar nuevos paquetes de datos ASF</span><span class="sxs-lookup"><span data-stu-id="8c67b-119">7. Generate New ASF Data Packets</span></span>](#7-generate-new-asf-data-packets)
-   [<span data-ttu-id="8c67b-120">8. escribir los objetos ASF en el nuevo archivo</span><span class="sxs-lookup"><span data-stu-id="8c67b-120">8. Write the ASF Objects in the New File</span></span>](#8-write-the-asf-objects-in-the-new-file)
-   [<span data-ttu-id="8c67b-121">9 escribir la función Entry-Point</span><span class="sxs-lookup"><span data-stu-id="8c67b-121">9 Write the Entry-Point Function</span></span>](#9-write-the-entry-point-function)
-   [<span data-ttu-id="8c67b-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c67b-122">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="8c67b-123">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="8c67b-123">Prerequisites</span></span>

<span data-ttu-id="8c67b-124">En este tutorial se da por hecho lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="8c67b-124">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="8c67b-125">Está familiarizado con la estructura de un archivo ASF y los componentes proporcionados por Media Foundation para trabajar con objetos ASF.</span><span class="sxs-lookup"><span data-stu-id="8c67b-125">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="8c67b-126">Estos componentes incluyen los objetos ContentInfo, Splitter, multiplexor y Profile.</span><span class="sxs-lookup"><span data-stu-id="8c67b-126">These components include ContentInfo, splitter, multiplexer, and profile objects.</span></span> <span data-ttu-id="8c67b-127">Para obtener más información, consulte [WMCONTAINER ASF Components](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="8c67b-127">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="8c67b-128">Está familiarizado con el proceso de analizar el objeto de encabezado ASF y los paquetes de datos ASF de un archivo existente y generar ejemplos de secuencias comprimidas mediante el divisor.</span><span class="sxs-lookup"><span data-stu-id="8c67b-128">You are familiar with the process of parsing the ASF Header Object and the ASF data packets of an existing file and generating compressed stream samples by using the splitter.</span></span> <span data-ttu-id="8c67b-129">Para obtener más información, consulte [Tutorial: leer un archivo ASF](tutorial--reading-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="8c67b-129">For more information see [Tutorial: Reading an ASF File](tutorial--reading-an-asf-file.md).</span></span>
-   <span data-ttu-id="8c67b-130">Está familiarizado con los búferes multimedia y los flujos de bytes: en concreto, las operaciones de archivo que usan un flujo de bytes y la escritura del contenido de un búfer multimedia en una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="8c67b-130">You are familiar with media buffers and byte streams: Specifically, file operations using a byte stream, and writing the contents of a media buffer into a byte stream.</span></span> <span data-ttu-id="8c67b-131">(Consulte [2. Declare las funciones auxiliares](#2-declare-helper-functions)).</span><span class="sxs-lookup"><span data-stu-id="8c67b-131">(See [2. Declare Helper Functions](#2-declare-helper-functions).)</span></span>

## <a name="terminology"></a><span data-ttu-id="8c67b-132">Terminología</span><span class="sxs-lookup"><span data-stu-id="8c67b-132">Terminology</span></span>

<span data-ttu-id="8c67b-133">En este tutorial se usan los siguientes términos:</span><span class="sxs-lookup"><span data-stu-id="8c67b-133">This tutorial uses the following terms:</span></span>

-   <span data-ttu-id="8c67b-134">Secuencia de bytes de origen: objeto de secuencia de bytes, expone la interfaz [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que incluye el contenido del archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="8c67b-134">Source byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the input file.</span></span>
-   <span data-ttu-id="8c67b-135">Source ContentInfo Object: ContentInfo Object, expone la interfaz [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , que representa el objeto de encabezado ASF del archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="8c67b-135">Source ContentInfo object: ContentInfo object, exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the input file.</span></span>
-   <span data-ttu-id="8c67b-136">Perfil de audio: objeto de perfil, expone la interfaz [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , que solo contiene secuencias de audio del archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="8c67b-136">Audio profile: Profile object, exposes [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) interface, which contains only audio streams of the input file.</span></span>
-   <span data-ttu-id="8c67b-137">Stream Sample: ejemplo multimedia, expone la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , generada por el divisor representa los datos multimedia del flujo seleccionado obtenidos del archivo de entrada en estado comprimido.</span><span class="sxs-lookup"><span data-stu-id="8c67b-137">Stream sample: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the splitter represents the selected stream's media data obtained from the input file in compressed state.</span></span>
-   <span data-ttu-id="8c67b-138">OUTPUT ContentInfo Object: ContentInfo Object, expone la interfaz [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , que representa el objeto de encabezado ASF del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="8c67b-138">Output ContentInfo object: ContentInfo object, exposes [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface, which represents the ASF Header Object of the output file.</span></span>
-   <span data-ttu-id="8c67b-139">Secuencia de bytes de datos: objeto de secuencia de bytes, expone la interfaz [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que representa la parte del objeto de datos ASF completa del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="8c67b-139">Data byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which represents the entire ASF Data Object portion of the output file.</span></span>
-   <span data-ttu-id="8c67b-140">Paquete de datos: el ejemplo multimedia, expone la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , generada por el multiplexor representa un paquete de datos ASF que se escribirá en la secuencia de bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="8c67b-140">Data packet: Media sample, exposes [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface, generated by the multiplexer represents an ASF data packet that will be written to the data byte stream.</span></span>
-   <span data-ttu-id="8c67b-141">Secuencia de bytes de salida: objeto de flujo de bytes, expone la interfaz [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que incluye el contenido del archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="8c67b-141">Output byte stream: Byte stream object, exposes [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) interface, which contains the contents of the output file.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="8c67b-142">1. configurar el proyecto</span><span class="sxs-lookup"><span data-stu-id="8c67b-142">1. Set up the Project</span></span>

<span data-ttu-id="8c67b-143">Incluya los siguientes encabezados en el archivo de código fuente:</span><span class="sxs-lookup"><span data-stu-id="8c67b-143">Include the following headers in your source file:</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <mferror.h>     // Media Foundation error codes
```



<span data-ttu-id="8c67b-144">Vínculo a los siguientes archivos de biblioteca:</span><span class="sxs-lookup"><span data-stu-id="8c67b-144">Link to the following library files:</span></span>

-   <span data-ttu-id="8c67b-145">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="8c67b-145">mfplat.lib</span></span>
-   <span data-ttu-id="8c67b-146">MF. lib</span><span class="sxs-lookup"><span data-stu-id="8c67b-146">mf.lib</span></span>
-   <span data-ttu-id="8c67b-147">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="8c67b-147">mfuuid.lib</span></span>

<span data-ttu-id="8c67b-148">Declare la función [SafeRelease](saferelease.md) :</span><span class="sxs-lookup"><span data-stu-id="8c67b-148">Declare the [SafeRelease](saferelease.md) function:</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



## <a name="2-declare-helper-functions"></a><span data-ttu-id="8c67b-149">2. declarar funciones auxiliares</span><span class="sxs-lookup"><span data-stu-id="8c67b-149">2. Declare Helper Functions</span></span>

<span data-ttu-id="8c67b-150">En este tutorial se usan las siguientes funciones auxiliares para leer y escribir en una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="8c67b-150">This tutorial uses the following helper functions to read and write from a byte stream.</span></span>

<span data-ttu-id="8c67b-151">La `AllocReadFromByteStream` función Lee los datos de una secuencia de bytes y asigna un nuevo búfer multimedia para contener los datos.</span><span class="sxs-lookup"><span data-stu-id="8c67b-151">The `AllocReadFromByteStream` function reads data from a byte stream and allocates a new media buffer to hold the data.</span></span> <span data-ttu-id="8c67b-152">Para obtener más información, vea [**IMFByteStream:: Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).</span><span class="sxs-lookup"><span data-stu-id="8c67b-152">For more information, see [**IMFByteStream::Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).</span></span>


```C++
//-------------------------------------------------------------------
// AllocReadFromByteStream
//
// Reads data from a byte stream and returns a media buffer that
// contains the data.
//-------------------------------------------------------------------

HRESULT AllocReadFromByteStream(
    IMFByteStream *pStream,         // Pointer to the byte stream.
    DWORD cbToRead,                 // Number of bytes to read.
    IMFMediaBuffer **ppBuffer       // Receives a pointer to the media buffer. 
    )
{
    HRESULT hr = S_OK;
    BYTE *pData = NULL;
    DWORD cbRead = 0;   // Actual amount of data read.

    IMFMediaBuffer *pBuffer = NULL;

    // Create the media buffer. 
    // This function allocates the memory for the buffer.
    hr = MFCreateMemoryBuffer(cbToRead, &pBuffer);

    // Get a pointer to the memory buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }

    // Read the data from the byte stream.
    if (SUCCEEDED(hr))
    {
        hr = pStream->Read(pData, cbToRead, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pBuffer;
        (*ppBuffer)->AddRef();
    }

    if (pData)
    {
        pBuffer->Unlock();
    }
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="8c67b-153">La `WriteBufferToByteStream` función escribe datos de un búfer multimedia en una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="8c67b-153">The `WriteBufferToByteStream` function writes data from a media buffer to a byte stream.</span></span> <span data-ttu-id="8c67b-154">Para obtener más información, vea [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span><span class="sxs-lookup"><span data-stu-id="8c67b-154">For more information, see [**IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).</span></span>


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



<span data-ttu-id="8c67b-155">La `AppendToByteStream` función anexa el contenido de un flujo de bytes a otro:</span><span class="sxs-lookup"><span data-stu-id="8c67b-155">The `AppendToByteStream` function appends the contents of one byte stream to another:</span></span>


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



## <a name="3-open-the-input-asf-file"></a><span data-ttu-id="8c67b-156">3. abrir el archivo ASF de entrada</span><span class="sxs-lookup"><span data-stu-id="8c67b-156">3. Open the Input ASF File</span></span>

<span data-ttu-id="8c67b-157">Abra el archivo de entrada mediante una llamada a la función [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="8c67b-157">Open the input file by calling the [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) function.</span></span> <span data-ttu-id="8c67b-158">El método devuelve un puntero al objeto de flujo de bytes que incluye el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="8c67b-158">The method returns a pointer to the byte stream object that contains the contents of the file.</span></span> <span data-ttu-id="8c67b-159">El nombre de archivo lo especifica el usuario a través de los argumentos de línea de comandos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="8c67b-159">The filename is specified by the user through command line arguments of the application.</span></span>

<span data-ttu-id="8c67b-160">El siguiente código de ejemplo toma un nombre de archivo y devuelve un puntero a un objeto de flujo de bytes que se puede usar para leer el archivo.</span><span class="sxs-lookup"><span data-stu-id="8c67b-160">The following example code takes a file name and returns a pointer to a byte stream object that can be used to read the file.</span></span>


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="4-initialize-objects-for-the-input-file"></a><span data-ttu-id="8c67b-161">4. inicializar objetos para el archivo de entrada</span><span class="sxs-lookup"><span data-stu-id="8c67b-161">4. Initialize Objects for the Input File</span></span>

<span data-ttu-id="8c67b-162">A continuación, creará e inicializará el objeto ContentInfo de origen y el divisor para generar ejemplos de secuencias.</span><span class="sxs-lookup"><span data-stu-id="8c67b-162">Next, you will create and initialize the source ContentInfo object and the splitter for generating stream samples.</span></span>

<span data-ttu-id="8c67b-163">Esta secuencia de bytes de origen creada en el paso 2 se usará para analizar el objeto de encabezado ASF y rellenar el objeto ContentInfo de origen.</span><span class="sxs-lookup"><span data-stu-id="8c67b-163">This source byte stream created in step 2 will be used to parse the ASF Header Object and populate the source ContentInfo object.</span></span> <span data-ttu-id="8c67b-164">Este objeto se usará para inicializar el divisor y facilitar el análisis de los paquetes de datos ASF para la secuencia de audio en el archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="8c67b-164">This object will be used to initialize the splitter to facilitate the parsing of the ASF data packets for the audio stream in the input file.</span></span> <span data-ttu-id="8c67b-165">También recuperará la longitud del objeto de datos ASF en el archivo de entrada y el desplazamiento al primer paquete de datos ASF con respecto al inicio del archivo.</span><span class="sxs-lookup"><span data-stu-id="8c67b-165">You will also retrieve the length of the ASF Data Object in the input file and the offset to the first ASF data packet relative to the start of the file.</span></span> <span data-ttu-id="8c67b-166">El divisor usará estos atributos para generar ejemplos de secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="8c67b-166">These attributes will be used by the splitter to generate audio stream samples.</span></span>

<span data-ttu-id="8c67b-167">Para crear e inicializar los componentes ASF para el archivo de entrada:</span><span class="sxs-lookup"><span data-stu-id="8c67b-167">To create and initialize ASF components for the input file:</span></span>

1.  <span data-ttu-id="8c67b-168">Llame a [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para crear el objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="8c67b-168">Call [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) to create the ContentInfo object.</span></span> <span data-ttu-id="8c67b-169">Esta función devuelve un puntero a la interfaz [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .</span><span class="sxs-lookup"><span data-stu-id="8c67b-169">This function returns a pointer to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface.</span></span>
2.  <span data-ttu-id="8c67b-170">Llame a [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) para analizar el encabezado ASF.</span><span class="sxs-lookup"><span data-stu-id="8c67b-170">Call [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) to parse the ASF Header.</span></span> <span data-ttu-id="8c67b-171">Para obtener más información acerca de este paso, vea [leer el objeto de encabezado ASF de un archivo existente](reading-the-asf-header-object-of-an-existing-file.md).</span><span class="sxs-lookup"><span data-stu-id="8c67b-171">For more information about this step, see [Reading the ASF Header Object of an Existing File](reading-the-asf-header-object-of-an-existing-file.md).</span></span>
3.  <span data-ttu-id="8c67b-172">Llame a [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) para crear el objeto divisor de ASF.</span><span class="sxs-lookup"><span data-stu-id="8c67b-172">Call [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) to create the ASF splitter object.</span></span> <span data-ttu-id="8c67b-173">Esta función devuelve un puntero a la interfaz [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="8c67b-173">This function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span>
4.  <span data-ttu-id="8c67b-174">Llame a [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), pasando el puntero [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo).</span><span class="sxs-lookup"><span data-stu-id="8c67b-174">Call [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), passing in the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo)pointer.</span></span> <span data-ttu-id="8c67b-175">Para obtener más información acerca de este paso, consulte [crear el objeto divisor de ASF](creating-the-asf-splitter-object.md).</span><span class="sxs-lookup"><span data-stu-id="8c67b-175">For more information about this step, see [Creating the ASF Splitter Object](creating-the-asf-splitter-object.md).</span></span>
5.  <span data-ttu-id="8c67b-176">Llame a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) para obtener un descriptor de presentación para el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="8c67b-176">Call [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) to get a presentation descriptor for the ASF file.</span></span>
6.  <span data-ttu-id="8c67b-177">Obtiene el valor del atributo [**de \_ \_ desplazamiento de \_ \_ Inicio de \_ datos ASF de MF PD**](mf-pd-asf-data-start-offset-attribute.md) del descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="8c67b-177">Get the value of the [**MF\_PD\_ASF\_DATA\_START\_OFFSET**](mf-pd-asf-data-start-offset-attribute.md) attribute from the presentation descriptor.</span></span> <span data-ttu-id="8c67b-178">Este valor es la ubicación del objeto de datos ASF en el archivo, como un desplazamiento de bytes desde el inicio del archivo.</span><span class="sxs-lookup"><span data-stu-id="8c67b-178">This value is the location of the ASF Data Object in the file, as a byte offset from the start of the file.</span></span>
7.  <span data-ttu-id="8c67b-179">Obtiene el valor del atributo [**de \_ \_ longitud de \_ datos \_ ASF de MF PD**](mf-pd-asf-data-length-attribute.md) del descriptor de presentación.</span><span class="sxs-lookup"><span data-stu-id="8c67b-179">Get the value of the [**MF\_PD\_ASF\_DATA\_LENGTH**](mf-pd-asf-data-length-attribute.md) attribute from the presentation descriptor.</span></span> <span data-ttu-id="8c67b-180">Este valor es el tamaño total del objeto de datos ASF, en bytes.</span><span class="sxs-lookup"><span data-stu-id="8c67b-180">This value is the total size of the ASF Data Object, in bytes.</span></span> <span data-ttu-id="8c67b-181">Para obtener más información, vea [obtener información de los objetos de encabezado ASF](getting-information-from-asf-header-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8c67b-181">For more information, see [Getting Information from ASF Header Objects](getting-information-from-asf-header-objects.md).</span></span>

<span data-ttu-id="8c67b-182">En el ejemplo de código siguiente se muestra una función que consolida todos los pasos.</span><span class="sxs-lookup"><span data-stu-id="8c67b-182">The following example code shows a function that consolidates all of the steps.</span></span> <span data-ttu-id="8c67b-183">Esta función toma un puntero a la secuencia de bytes de origen y devuelve punteros al objeto ContentInfo de origen y al divisor.</span><span class="sxs-lookup"><span data-stu-id="8c67b-183">This function takes a pointer to the source byte stream and returns pointers to the source ContentInfo object and the splitter.</span></span> <span data-ttu-id="8c67b-184">Además, recibe la longitud y los desplazamientos al objeto de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="8c67b-184">Also, it receives the length and offsets to the ASF Data Object.</span></span>


```C++
//-------------------------------------------------------------------
// CreateSourceParsers
//
// Creates the ASF splitter and the ASF Content Info object for the 
// source file.
// 
// This function also calulates the offset and length of the ASF 
// Data Object.
//-------------------------------------------------------------------

HRESULT CreateSourceParsers(
    IMFByteStream *pSourceStream,
    IMFASFContentInfo **ppSourceContentInfo,
    IMFASFSplitter **ppSplitter,
    UINT64 *pcbDataOffset,
    UINT64 *pcbDataLength
    )
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;

    IMFMediaBuffer *pBuffer = NULL;
    IMFPresentationDescriptor *pPD = NULL;
    IMFASFContentInfo *pSourceContentInfo = NULL;
    IMFASFSplitter *pSplitter = NULL;

    QWORD cbHeader = 0;

    /*------- Parse the ASF header. -------*/

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pSourceContentInfo);
    
    // Read the first 30 bytes to find the total header size.
    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            MIN_ASF_HEADER_SIZE, 
            &pBuffer
            );
    }

    // Get the header size.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Release the buffer; we will reuse it.
    SafeRelease(&pBuffer);
    
    // Read the entire header into a buffer.
    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(0);
    }

    if (SUCCEEDED(hr))
    {
        hr = AllocReadFromByteStream(
            pSourceStream, 
            (DWORD)cbHeader, 
            &pBuffer
            );
    }

    // Parse the buffer and populate the header object.
    if (SUCCEEDED(hr))
    {
        hr = pSourceContentInfo->ParseHeader(pBuffer, 0);
    }

    /*------- Initialize the ASF splitter. -------*/

    // Create the splitter.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFSplitter(&pSplitter);
    }
    
    // initialize the splitter with the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pSourceContentInfo);
    }


    /*------- Get the offset and size of the ASF Data Object. -------*/

    // Generate the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr =  pSourceContentInfo->GeneratePresentationDescriptor(&pPD);
    }

    // Get the offset to the start of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_START_OFFSET, pcbDataOffset);
    }

    // Get the length of the Data Object.
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_DATA_LENGTH, pcbDataLength);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppSourceContentInfo = pSourceContentInfo;
        (*ppSourceContentInfo)->AddRef();

        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();

    }

    SafeRelease(&pPD);
    SafeRelease(&pBuffer);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSplitter);

    return S_OK;
}
```



## <a name="5-create-an-audio-profile"></a><span data-ttu-id="8c67b-185">5. crear un perfil de audio</span><span class="sxs-lookup"><span data-stu-id="8c67b-185">5. Create an Audio Profile</span></span>

<span data-ttu-id="8c67b-186">A continuación, creará un objeto de perfil para el archivo de entrada mediante su obtención del objeto ContentInfo de origen.</span><span class="sxs-lookup"><span data-stu-id="8c67b-186">Next, you will create a profile object for the input file by obtaining it from the source ContentInfo object.</span></span> <span data-ttu-id="8c67b-187">Después, configurará el perfil para que contenga solo las secuencias de audio del archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="8c67b-187">You will then configure the profile so that it contains only the audio streams of the input file.</span></span> <span data-ttu-id="8c67b-188">Para ello, enumere las secuencias y quite las secuencias que no sean de audio del perfil.</span><span class="sxs-lookup"><span data-stu-id="8c67b-188">To do this, enumerate the streams and remove non-audio streams from the profile.</span></span> <span data-ttu-id="8c67b-189">El objeto de Perfil de audio se usará más adelante en este tutorial para inicializar el objeto ContentInfo de salida.</span><span class="sxs-lookup"><span data-stu-id="8c67b-189">The audio profile object will be used later in this tutorial to initialize the output ContentInfo object.</span></span>

<span data-ttu-id="8c67b-190">Para crear un perfil de audio</span><span class="sxs-lookup"><span data-stu-id="8c67b-190">To create an audio profile</span></span>

1.  <span data-ttu-id="8c67b-191">Obtiene el objeto de perfil para el archivo de entrada del objeto ContentInfo de origen llamando a [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span><span class="sxs-lookup"><span data-stu-id="8c67b-191">Get the profile object for the input file from the source ContentInfo object by calling [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).</span></span> <span data-ttu-id="8c67b-192">El método devuelve un puntero a un objeto de perfil que contiene todas las secuencias del archivo de entrada.</span><span class="sxs-lookup"><span data-stu-id="8c67b-192">The method returns a pointer to a profile object that contains all of the streams in the input file.</span></span> <span data-ttu-id="8c67b-193">Para obtener más información, consulte [crear un perfil ASF](creating-an-asf-profile.md).</span><span class="sxs-lookup"><span data-stu-id="8c67b-193">For more information see [Creating an ASF Profile](creating-an-asf-profile.md).</span></span>
2.  <span data-ttu-id="8c67b-194">Quite todos los objetos de exclusión mutua del perfil.</span><span class="sxs-lookup"><span data-stu-id="8c67b-194">Remove any mutual exclusion objects from the profile.</span></span> <span data-ttu-id="8c67b-195">Este paso es necesario porque los flujos que no son de audio se quitarán del perfil, lo que podría invalidar los objetos de exclusión mutua.</span><span class="sxs-lookup"><span data-stu-id="8c67b-195">This step is required because non-audio streams will be removed from the profile, which could invalidate the mutual exclusion objects.</span></span>
3.  <span data-ttu-id="8c67b-196">Quite todas las secuencias que no sean de audio del perfil, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="8c67b-196">Remove all non-audio streams from the profile, as follows:</span></span>
    -   <span data-ttu-id="8c67b-197">Llame a [**IMFASFProfile:: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) para obtener el número de secuencias.</span><span class="sxs-lookup"><span data-stu-id="8c67b-197">Call [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) to get the number of streams.</span></span>
    -   <span data-ttu-id="8c67b-198">En un bucle, llame a [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) para obtener cada flujo por índice.</span><span class="sxs-lookup"><span data-stu-id="8c67b-198">In a loop, call [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) to get each stream by index.</span></span>
    -   <span data-ttu-id="8c67b-199">Llame a [**IMFASFStreamConfig:: GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) para obtener el tipo de flujo.</span><span class="sxs-lookup"><span data-stu-id="8c67b-199">Call [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) to get the stream type.</span></span>
    -   <span data-ttu-id="8c67b-200">En el caso de las secuencias que no son de audio, llame a [**IMFASFProfile:: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) para quitar el flujo.</span><span class="sxs-lookup"><span data-stu-id="8c67b-200">For non-audio streams, call [**IMFASFProfile::RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) to remove the stream.</span></span>
4.  <span data-ttu-id="8c67b-201">Almacene el número de secuencia de la primera secuencia de audio.</span><span class="sxs-lookup"><span data-stu-id="8c67b-201">Store the stream number of the first audio stream.</span></span> <span data-ttu-id="8c67b-202">Se seleccionará en el divisor para generar ejemplos de secuencias.</span><span class="sxs-lookup"><span data-stu-id="8c67b-202">This will be selected on the splitter to generate stream samples.</span></span> <span data-ttu-id="8c67b-203">Si el número de secuencia es cero, el llamador puede suponer que no había ningún archivo de secuencias de audio.</span><span class="sxs-lookup"><span data-stu-id="8c67b-203">If the stream number is zero, the caller can assume that there were no audio streams file.</span></span>

<span data-ttu-id="8c67b-204">En el siguiente código se indican estos pasos:</span><span class="sxs-lookup"><span data-stu-id="8c67b-204">The following code these steps:</span></span>


```C++
//-------------------------------------------------------------------
// GetAudioProfile
//
// Gets the ASF profile from the source file and removes any video
// streams from the profile.
//-------------------------------------------------------------------

HRESULT GetAudioProfile(
    IMFASFContentInfo *pSourceContentInfo, 
    IMFASFProfile **ppAudioProfile, 
    WORD *pwSelectStreamNumber
    )
{
    IMFASFStreamConfig *pStream = NULL;
    IMFASFProfile *pProfile = NULL;

    DWORD dwTotalStreams = 0;
    WORD  wStreamNumber = 0; 
    GUID guidMajorType = GUID_NULL;
    
    // Get the profile object from the source ContentInfo object.
    HRESULT hr = pSourceContentInfo->GetProfile(&pProfile);

    // Remove mutexes from the profile
    if (SUCCEEDED(hr))
    {
        hr = RemoveMutexes(pProfile);
    }

    // Get the total number of streams on the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&dwTotalStreams);
    }

    // Enumerate the streams and remove the non-audio streams.
    if (SUCCEEDED(hr))
    {
        for (DWORD index = 0; index < dwTotalStreams; )
        {
            hr = pProfile->GetStream(index, &wStreamNumber, &pStream);

            if (FAILED(hr)) { break; }

            hr = pStream->GetStreamType(&guidMajorType);

            SafeRelease(&pStream);

            if (FAILED(hr)) { break; }

            if (guidMajorType != MFMediaType_Audio)
            {
                hr = pProfile->RemoveStream(wStreamNumber);
    
                if (FAILED(hr)) { break; }

                index = 0;
                dwTotalStreams--;
            }
            else
            {
                // Store the first audio stream number. 
                // This will be selected on the splitter.

                if (*pwSelectStreamNumber == 0)
                {
                    *pwSelectStreamNumber = wStreamNumber;
                }

                index++;
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        *ppAudioProfile = pProfile;
        (*ppAudioProfile)->AddRef();
    }

    SafeRelease(&pStream);
    SafeRelease(&pProfile);

    return S_OK;
}
```



<span data-ttu-id="8c67b-205">La `RemoveMutexes` función quita todos los objetos de exclusión mutua del perfil:</span><span class="sxs-lookup"><span data-stu-id="8c67b-205">The `RemoveMutexes` function removes any mutual exclusion objects from the profile:</span></span>


```C++
HRESULT RemoveMutexes(IMFASFProfile *pProfile)
{
    DWORD cMutex = 0;
    HRESULT hr = pProfile->GetMutualExclusionCount(&cMutex);

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cMutex; i++)
        {
            hr = pProfile->RemoveMutualExclusion(0);

            if (FAILED(hr))
            {
                break;
            }
        }
    }

    return hr;
}
```



## <a name="6-initialize-objects-for-the-output-file"></a><span data-ttu-id="8c67b-206">6. inicializar los objetos para el archivo de salida</span><span class="sxs-lookup"><span data-stu-id="8c67b-206">6. Initialize Objects for the Output File</span></span>

<span data-ttu-id="8c67b-207">A continuación, creará el objeto ContentInfo de salida y el multiplexor para generar paquetes de datos para el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="8c67b-207">Next, you will create the output ContentInfo object and the multiplexer for generating data packets for the output file.</span></span>

<span data-ttu-id="8c67b-208">El perfil de audio creado en el paso 4 se usará para rellenar el objeto ContentInfo de salida.</span><span class="sxs-lookup"><span data-stu-id="8c67b-208">The audio profile created in step 4 will be used to populate the output ContentInfo object.</span></span> <span data-ttu-id="8c67b-209">Este objeto contiene información como atributos de archivo global y propiedades de secuencia.</span><span class="sxs-lookup"><span data-stu-id="8c67b-209">This object contains information such as global file attributes and stream properties.</span></span> <span data-ttu-id="8c67b-210">El objeto ContentInfo de salida se usará para inicializar el multiplexor que generará paquetes de datos para el archivo de salida.</span><span class="sxs-lookup"><span data-stu-id="8c67b-210">The output ContentInfo object will be used to initialize the multiplexer that will generate data packets for the output file.</span></span> <span data-ttu-id="8c67b-211">Una vez generados los paquetes de datos, el objeto ContentInfo debe actualizarse para reflejar los nuevos valores.</span><span class="sxs-lookup"><span data-stu-id="8c67b-211">After the data packets are generated, the ContentInfo object must be updated to reflect the new values.</span></span>

<span data-ttu-id="8c67b-212">Para crear e inicializar componentes ASF para el archivo de salida</span><span class="sxs-lookup"><span data-stu-id="8c67b-212">To create and initialize ASF components for the output file</span></span>

1.  <span data-ttu-id="8c67b-213">Cree un objeto ContentInfo vacío llamando a [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) y rellénelo con información del perfil de audio creado en el paso 3 llamando a [**IMFASFContentInfo:: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span><span class="sxs-lookup"><span data-stu-id="8c67b-213">Create an empty ContentInfo object by calling [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) and populate it with information from the audio profile created in step 3 by calling [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).</span></span> <span data-ttu-id="8c67b-214">Para obtener más información, consulte [inicializar el objeto ContentInfo de un nuevo archivo ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="8c67b-214">For more information, see [Initializing the ContentInfo Object of a New ASF File](initializing-the-contentinfo-object-of-a-new-asf-file.md).</span></span>
2.  <span data-ttu-id="8c67b-215">Cree e inicialice el objeto multiplexor usando el objeto ContentInfo de salida.</span><span class="sxs-lookup"><span data-stu-id="8c67b-215">Create and initialize the multiplexer object by using the output ContentInfo object.</span></span> <span data-ttu-id="8c67b-216">Para obtener más información, vea [crear el objeto multiplexor](creating-the-multiplexer-object.md).</span><span class="sxs-lookup"><span data-stu-id="8c67b-216">For more information, see [Creating the Multiplexer Object](creating-the-multiplexer-object.md).</span></span>

<span data-ttu-id="8c67b-217">En el ejemplo de código siguiente se muestra una función que consolida los pasos.</span><span class="sxs-lookup"><span data-stu-id="8c67b-217">The following example code shows a function that consolidates the steps.</span></span> <span data-ttu-id="8c67b-218">Esta función toma un puntero a un objeto de perfil y devuelve punteros al objeto ContentInfo de salida y al multiplexor.</span><span class="sxs-lookup"><span data-stu-id="8c67b-218">This function takes a pointer to a profile object and returns pointers to the output ContentInfo object and the multiplexer.</span></span>


```C++
//-------------------------------------------------------------------
// CreateOutputGenerators
//
// Creates the ASF mux and the ASF Content Info object for the 
// output file.
//-------------------------------------------------------------------

HRESULT CreateOutputGenerators(
    IMFASFProfile *pProfile, 
    IMFASFContentInfo **ppContentInfo, 
    IMFASFMultiplexer **ppMux
    )
{
    IMFASFContentInfo *pContentInfo = NULL;
    IMFASFMultiplexer *pMux = NULL;

    // Use the ASF profile to create the ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);

    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->SetProfile(pProfile);
    }

    // Create the ASF Multiplexer object.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFMultiplexer(&pMux);
    }
    
    // Initialize it using the new ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Initialize(pContentInfo);
    }

    // Return the pointers to the caller.
    if (SUCCEEDED(hr))
    {
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();

        *ppMux = pMux;
        (*ppMux)->AddRef();
    }

    SafeRelease(&pContentInfo);
    SafeRelease(&pMux);

    return hr;
}
```



## <a name="7-generate-new-asf-data-packets"></a><span data-ttu-id="8c67b-219">7. generar nuevos paquetes de datos ASF</span><span class="sxs-lookup"><span data-stu-id="8c67b-219">7. Generate New ASF Data Packets</span></span>

<span data-ttu-id="8c67b-220">A continuación, generará ejemplos de secuencias de audio a partir de la secuencia de bytes de origen mediante el divisor y los enviará al multiplexor para crear paquetes de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="8c67b-220">Next, you will generate audio stream samples from the source byte stream by using the splitter and send them to the multiplexer to create ASF data packets.</span></span> <span data-ttu-id="8c67b-221">Estos paquetes de datos constituirán el último objeto de datos ASF del nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="8c67b-221">These data packets will constitute the final ASF Data Object for the new file.</span></span>

<span data-ttu-id="8c67b-222">Para generar ejemplos de secuencias de audio</span><span class="sxs-lookup"><span data-stu-id="8c67b-222">To generate audio stream samples</span></span>

1.  <span data-ttu-id="8c67b-223">Seleccione la primera secuencia de audio en el divisor llamando a [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).</span><span class="sxs-lookup"><span data-stu-id="8c67b-223">Select the first audio stream on the splitter by calling [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).</span></span>
2.  <span data-ttu-id="8c67b-224">Leer bloques de tamaño fijo de los datos multimedia de la secuencia de bytes de origen en un búfer multimedia.</span><span class="sxs-lookup"><span data-stu-id="8c67b-224">Read fixed-size blocks of media data from the source byte stream into a media buffer.</span></span>
3.  <span data-ttu-id="8c67b-225">Recopile los ejemplos de secuencias como muestras de medios del divisor llamando a [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) en un bucle siempre que reciba la \_ marca ASF STATUSFLAGS \_ incompleta en el parámetro *pdwStatusFlags* .</span><span class="sxs-lookup"><span data-stu-id="8c67b-225">Collect the stream samples as media samples from the splitter by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in a loop as long as it receives the ASF\_STATUSFLAGS\_INCOMPLETE flag in the *pdwStatusFlags* parameter.</span></span> <span data-ttu-id="8c67b-226">Para obtener más información, vea generar ejemplos de paquetes de datos ASF en generación de ejemplos de [secuencias a partir de un objeto de datos ASF existente](generating-stream-samples-from-an-existing-asf-data-object.md).</span><span class="sxs-lookup"><span data-stu-id="8c67b-226">For more information, see Generating Samples for ASF Data Packets" in [Generating Stream Samples from an Existing ASF Data Object](generating-stream-samples-from-an-existing-asf-data-object.md).</span></span>
4.  <span data-ttu-id="8c67b-227">Para cada ejemplo de medio, llame a [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) para enviar el ejemplo multimedia al multiplexor.</span><span class="sxs-lookup"><span data-stu-id="8c67b-227">For each media sample, call [**IMFASFMultiplexer::ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) to send the media sample to the multiplexer.</span></span> <span data-ttu-id="8c67b-228">El multiplexor genera los paquetes de datos para el objeto de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="8c67b-228">The multiplexer generates the data packets for the ASF Data Object.</span></span>
5.  <span data-ttu-id="8c67b-229">Escriba el paquete de datos generado por el multiplexor en la secuencia de bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="8c67b-229">Write the data packet generated by the multiplexer to the data byte stream.</span></span>
6.  <span data-ttu-id="8c67b-230">Una vez generados todos los paquetes de datos, llame a [**IMFASFMultiplexer:: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) para actualizar el objeto ContentInfo de salida con la información recopilada durante la generación de paquetes de datos ASF.</span><span class="sxs-lookup"><span data-stu-id="8c67b-230">After all the data packets have been generated, call [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) to update the output ContentInfo object with information collected during ASF data packet generation.</span></span>

<span data-ttu-id="8c67b-231">El siguiente código de ejemplo genera ejemplos de secuencias del divisor de ASF y los envía al multiplexor.</span><span class="sxs-lookup"><span data-stu-id="8c67b-231">The following example code generates stream samples from the ASF splitter and sends them to the multiplexer.</span></span> <span data-ttu-id="8c67b-232">El multiplexor genera paquetes de datos ASF y los escribe en una secuencia.</span><span class="sxs-lookup"><span data-stu-id="8c67b-232">The multiplexer generates ASF data packets and writes it to a stream.</span></span>


```C++
//-------------------------------------------------------------------
// GenerateASFDataObject
// 
// Creates a byte stream that contains the ASF Data Object for the
// output file.
//-------------------------------------------------------------------

HRESULT GenerateASFDataObject(
    IMFByteStream *pSourceStream, 
    IMFASFSplitter *pSplitter, 
    IMFASFMultiplexer *pMux, 
    UINT64   cbDataOffset,
    UINT64   cbDataLength,
    IMFByteStream **ppDataStream
    )
{
    IMFMediaBuffer *pBuffer = NULL;
    IMFByteStream *pDataStream = NULL;
    
    const DWORD READ_SIZE = 1024 * 4;

    // Flush the splitter to remove any pending samples.
    HRESULT hr = pSplitter->Flush();

    if (SUCCEEDED(hr))
    {
        hr = MFCreateTempFile(
            MF_ACCESSMODE_READWRITE, 
            MF_OPENMODE_DELETE_IF_EXIST,
            MF_FILEFLAGS_NONE,
            &pDataStream
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = pSourceStream->SetCurrentPosition(cbDataOffset);
    }

    if (SUCCEEDED(hr))
    {
        while (cbDataLength > 0)
        {
            DWORD cbRead = min(READ_SIZE, (DWORD)cbDataLength);

            hr = AllocReadFromByteStream(
                pSourceStream, 
                cbRead, 
                &pBuffer
                );

            if (FAILED(hr)) 
            { 
                break; 
            }

            cbDataLength -= cbRead;

            // Push data on the splitter.
            hr =  pSplitter->ParseData(pBuffer, 0, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            // Get ASF packets from the splitter and feed them to the mux.
            hr = GetPacketsFromSplitter(pSplitter, pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }

            SafeRelease(&pBuffer);
        }
    }

    // Flush the mux and generate any remaining samples.
    if (SUCCEEDED(hr))
    {
        hr = pMux->Flush();
    }

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataPackets(pMux, pDataStream);
    }

     // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppDataStream = pDataStream;
        (*ppDataStream)->AddRef();
    }

    SafeRelease(&pBuffer);
    SafeRelease(&pDataStream);
    return hr;
}
```



<span data-ttu-id="8c67b-233">Para obtener paquetes del divisor de ASF, el código anterior llama a la `GetPacketsFromSplitter` función, que se muestra aquí:</span><span class="sxs-lookup"><span data-stu-id="8c67b-233">To get packets from the ASF splitter, the previous code calls the `GetPacketsFromSplitter` function, shown here:</span></span>


```C++
//-------------------------------------------------------------------
// GetPacketsFromSplitter
//
// Gets samples from the ASF splitter.
//
// This function is called after calling IMFASFSplitter::ParseData.
//-------------------------------------------------------------------

HRESULT GetPacketsFromSplitter(
    IMFASFSplitter *pSplitter,
    IMFASFMultiplexer *pMux,
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;
    DWORD   dwStatus = ASF_STATUSFLAGS_INCOMPLETE;
    WORD    wStreamNum = 0;

    IMFSample *pSample = NULL;

    while (dwStatus & ASF_STATUSFLAGS_INCOMPLETE) 
    {
        hr = pSplitter->GetNextSample(&dwStatus, &wStreamNum, &pSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pSample)
        {
            //Send to the multiplexer to convert it into ASF format
            hr = pMux->ProcessSample(wStreamNum, pSample, 0);

            if (FAILED(hr)) 
            { 
                break; 
            }

            hr = GenerateASFDataPackets(pMux, pDataStream);

            if (FAILED(hr)) 
            { 
                break; 
            }
        }

        SafeRelease(&pSample);
    }

    SafeRelease(&pSample);
    return hr;
}
```



<span data-ttu-id="8c67b-234">La `GenerateDataPackets` función obtiene los paquetes de datos del multiplexor.</span><span class="sxs-lookup"><span data-stu-id="8c67b-234">The `GenerateDataPackets` function gets data packets from multiplexer.</span></span> <span data-ttu-id="8c67b-235">Para obtener más información, vea [obtener paquetes de datos ASF](generating-new-asf-data-packets.md).</span><span class="sxs-lookup"><span data-stu-id="8c67b-235">For more information, see [Getting ASF Data Packets](generating-new-asf-data-packets.md).</span></span>


```C++
//-------------------------------------------------------------------
// GenerateASFDataPackets
// 
// Gets data packets from the mux. This function is called after 
// calling IMFASFMultiplexer::ProcessSample. 
//-------------------------------------------------------------------

HRESULT GenerateASFDataPackets( 
    IMFASFMultiplexer *pMux, 
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;

    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacketBuffer = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pOutputSample)
        {
            //Convert to contiguous buffer
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacketBuffer);
            
            if (FAILED(hr))
            {
                break;
            }

            //Write buffer to byte stream
            hr = WriteBufferToByteStream(pDataStream, pDataPacketBuffer, NULL);

            if (FAILED(hr))
            {
                break;
            }
        }

        SafeRelease(&pDataPacketBuffer);
        SafeRelease(&pOutputSample);
    }

    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacketBuffer);
    return hr;
}
```



## <a name="8-write-the-asf-objects-in-the-new-file"></a><span data-ttu-id="8c67b-236">8. escribir los objetos ASF en el nuevo archivo</span><span class="sxs-lookup"><span data-stu-id="8c67b-236">8. Write the ASF Objects in the New File</span></span>

<span data-ttu-id="8c67b-237">A continuación, escribirá el contenido del objeto ContentInfo de salida en un búfer multimedia mediante una llamada a [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span><span class="sxs-lookup"><span data-stu-id="8c67b-237">Next, you will write the contents of the output ContentInfo object to a media buffer by calling [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader).</span></span> <span data-ttu-id="8c67b-238">Este método convierte los datos almacenados en el objeto ContentInfo en datos binarios en formato de objeto de encabezado ASF.</span><span class="sxs-lookup"><span data-stu-id="8c67b-238">This method converts data stored in the ContentInfo object into binary data in ASF Header Object format.</span></span> <span data-ttu-id="8c67b-239">Para obtener más información, vea [generar un nuevo objeto de encabezado ASF](generating-a-new-asf-header-object.md).</span><span class="sxs-lookup"><span data-stu-id="8c67b-239">For more information, see [Generating a New ASF Header Object](generating-a-new-asf-header-object.md).</span></span>

<span data-ttu-id="8c67b-240">Una vez generado el nuevo objeto de encabezado ASF, escriba el archivo de salida escribiendo primero el objeto de encabezado en la secuencia de bytes de salida creada en el paso 2 mediante una llamada a la función auxiliar WriteBufferToByteStream.</span><span class="sxs-lookup"><span data-stu-id="8c67b-240">After the new ASF Header Object has been generated, write the output file by first writing the Header Object to the output byte stream created in step 2 by calling the helper function WriteBufferToByteStream.</span></span> <span data-ttu-id="8c67b-241">Siga el objeto de encabezado con el objeto de datos contenido en la secuencia de bytes de datos.</span><span class="sxs-lookup"><span data-stu-id="8c67b-241">Follow the Header Object with the Data Object contained in the data byte stream.</span></span> <span data-ttu-id="8c67b-242">En el código de ejemplo se muestra una función que transfiere el contenido de la secuencia de bytes de datos a la secuencia de bytes de salida.</span><span class="sxs-lookup"><span data-stu-id="8c67b-242">The example code shows a function that transfers contents of the data bytes stream to the output byte stream.</span></span>


```C++
//-------------------------------------------------------------------
// WriteASFFile
//
// Writes the complete ASF file.
//-------------------------------------------------------------------

HRESULT WriteASFFile( 
    IMFASFContentInfo *pContentInfo, // ASF Content Info for the output file.
    IMFByteStream *pDataStream,      // Data stream.
    PCWSTR pszFile                   // Output file name.
    )
{
    
    IMFMediaBuffer *pHeaderBuffer = NULL;
    IMFByteStream *pWmaStream = NULL;

    DWORD cbHeaderSize = 0;
    DWORD cbWritten = 0;

    // Create output file.
    HRESULT hr = MFCreateFile(
        MF_ACCESSMODE_WRITE, 
        MF_OPENMODE_DELETE_IF_EXIST,
        MF_FILEFLAGS_NONE,
        pszFile,
        &pWmaStream
        );

    // Get the size of the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(NULL, &cbHeaderSize);
    }

    // Create a media buffer.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(cbHeaderSize, &pHeaderBuffer);
    }

    // Populate the media buffer with the ASF Header Object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GenerateHeader(pHeaderBuffer, &cbHeaderSize);
    }
 
    // Write the header contents to the byte stream for the output file.
    if (SUCCEEDED(hr))
    {
        hr = WriteBufferToByteStream(pWmaStream, pHeaderBuffer, &cbWritten);
    }

    if (SUCCEEDED(hr))
    {
        hr = pDataStream->SetCurrentPosition(0);
    }

    // Append the data stream to the file.

    if (SUCCEEDED(hr))
    {
        hr = AppendToByteStream(pDataStream, pWmaStream);
    }

    SafeRelease(&pHeaderBuffer);
    SafeRelease(&pWmaStream);

    return hr;
}
```



## <a name="9-write-the-entry-point-function"></a><span data-ttu-id="8c67b-243">9 escribir la función Entry-Point</span><span class="sxs-lookup"><span data-stu-id="8c67b-243">9 Write the Entry-Point Function</span></span>

<span data-ttu-id="8c67b-244">Ahora puede poner los pasos anteriores juntos en una aplicación completa.</span><span class="sxs-lookup"><span data-stu-id="8c67b-244">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="8c67b-245">Antes de usar cualquiera de los objetos Media Foundation, inicialice la plataforma de Media Foundation mediante una llamada a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="8c67b-245">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="8c67b-246">Cuando haya terminado, llame a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="8c67b-246">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="8c67b-247">Para obtener más información, vea [inicializar Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="8c67b-247">For more information, see [Initializing Media Foundation](initializing-media-foundation.md).</span></span>

<span data-ttu-id="8c67b-248">En el código siguiente se muestra la aplicación de consola completa.</span><span class="sxs-lookup"><span data-stu-id="8c67b-248">The following code shows the complete console application.</span></span> <span data-ttu-id="8c67b-249">El argumento de línea de comandos especifica el nombre del archivo que se va a convertir y el nombre del nuevo archivo de audio.</span><span class="sxs-lookup"><span data-stu-id="8c67b-249">The command-line argument specifies the name of the file to convert and the name of the new audio file.</span></span>


```C++
int wmain(int argc, WCHAR* argv[])
{
    if (argc != 3)
    {
        wprintf_s(L"Usage: %s input.wmv, %s output.wma\n");
        return 0;
    }

    HRESULT hr = MFStartup(MF_VERSION);

    if (FAILED(hr))
    {
        wprintf_s(L"MFStartup failed: 0x%X\n", hr);
        return 0;
    }

    PCWSTR pszInputFile = argv[1];      
    PCWSTR pszOutputFile = argv[2];     
    
    IMFByteStream      *pSourceStream = NULL;       
    IMFASFContentInfo  *pSourceContentInfo = NULL;  
    IMFASFProfile      *pAudioProfile = NULL;       
    IMFASFContentInfo  *pOutputContentInfo = NULL;  
    IMFByteStream      *pDataStream = NULL;         
    IMFASFSplitter     *pSplitter = NULL;           
    IMFASFMultiplexer  *pMux = NULL;                

    UINT64  cbDataOffset = 0;           
    UINT64  cbDataLength = 0;           
    WORD    wSelectStreamNumber = 0;    

    // Open the input file.

    hr = OpenFile(pszInputFile, &pSourceStream);

    // Initialize the objects that will parse the source file.

    if (SUCCEEDED(hr))
    {
        hr = CreateSourceParsers(
            pSourceStream, 
            &pSourceContentInfo,    // ASF Header for the source file.
            &pSplitter,             // Generates audio samples.
            &cbDataOffset,          // Offset to the first data packet.
            &cbDataLength           // Length of the ASF Data Object.
            );
    }

    // Create a profile object for the audio streams in the source file.

    if (SUCCEEDED(hr))
    {
        hr = GetAudioProfile(
            pSourceContentInfo, 
            &pAudioProfile,         // ASF profile for the audio stream.
            &wSelectStreamNumber    // Stream number of the first audio stream.
            );
    }

    // Initialize the objects that will generate the output data.

    if (SUCCEEDED(hr))
    {
        hr = CreateOutputGenerators(
            pAudioProfile, 
            &pOutputContentInfo,    // ASF Header for the output file.
            &pMux                   // Generates ASF data packets.
            );
    }

    // Set up the splitter to generate samples for the first
    // audio stream in the source media.

    if (SUCCEEDED(hr))
    {
        hr = pSplitter->SelectStreams(&wSelectStreamNumber, 1);
    }
    
    // Generate ASF Data Packets and store them in a byte stream.

    if (SUCCEEDED(hr))
    {
        hr = GenerateASFDataObject(
               pSourceStream, 
               pSplitter, 
               pMux, 
               cbDataOffset, 
               cbDataLength, 
               &pDataStream    // Byte stream for the ASF data packets.    
               );
    }

    // Update the header with new information if any.

    if (SUCCEEDED(hr))
    {
        hr = pMux->End(pOutputContentInfo);
    }

    //Write the ASF objects to the output file
    if (SUCCEEDED(hr))
    {
        hr = WriteASFFile(pOutputContentInfo, pDataStream, pszOutputFile);
    }

    // Clean up.
    SafeRelease(&pMux);
    SafeRelease(&pSplitter);
    SafeRelease(&pDataStream);
    SafeRelease(&pOutputContentInfo);
    SafeRelease(&pAudioProfile);
    SafeRelease(&pSourceContentInfo);
    SafeRelease(&pSourceStream);

    MFShutdown();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the audio file: 0x%X\n", hr);
    }

    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="8c67b-250">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8c67b-250">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c67b-251">Componentes de WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="8c67b-251">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="8c67b-252">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8c67b-252">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



