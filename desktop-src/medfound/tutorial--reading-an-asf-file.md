---
description: En este tutorial se muestra cómo obtener paquetes de datos de un archivo de formato de sistema avanzado (ASF) mediante el divisor de ASF.
ms.assetid: e3a55275-e8f0-4ab7-98db-a2f2c54d5a51
title: 'Tutorial: lectura de un archivo ASF mediante objetos WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0225f434f650f0423771122e6fc345022e69ec1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696872"
---
# <a name="tutorial-reading-an-asf-file-by-using-wmcontainer-objects"></a><span data-ttu-id="e7d3f-103">Tutorial: lectura de un archivo ASF mediante objetos WMContainer</span><span class="sxs-lookup"><span data-stu-id="e7d3f-103">Tutorial: Reading an ASF File by Using WMContainer Objects</span></span>

<span data-ttu-id="e7d3f-104">En este tutorial se muestra cómo obtener paquetes de datos de un archivo de formato de sistema avanzado (ASF) mediante el [divisor de ASF](asf-splitter.md).</span><span class="sxs-lookup"><span data-stu-id="e7d3f-104">This tutorial shows how to get data packets from an Advanced Systems Format (ASF) file using the [ASF Splitter](asf-splitter.md).</span></span> <span data-ttu-id="e7d3f-105">En este tutorial, creará una aplicación de consola simple que lee un archivo ASF y genera ejemplos de medios comprimidos para la primera secuencia de vídeo del archivo.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-105">In this tutorial, you will create a simple console application that reads an ASF file and generates compressed media samples for the first video stream in the file.</span></span> <span data-ttu-id="e7d3f-106">La aplicación muestra información sobre los fotogramas clave en el flujo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-106">The application displays information about the key frames in the video stream.</span></span>

<span data-ttu-id="e7d3f-107">Este tutorial contiene los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="e7d3f-107">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="e7d3f-108">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e7d3f-108">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="e7d3f-109">1. configurar el proyecto</span><span class="sxs-lookup"><span data-stu-id="e7d3f-109">1. Set up the Project</span></span>](#1-set-up-the-project)
-   [<span data-ttu-id="e7d3f-110">2. abrir un archivo ASF</span><span class="sxs-lookup"><span data-stu-id="e7d3f-110">2. Open an ASF File</span></span>](#2-open-an-asf-file)
-   [<span data-ttu-id="e7d3f-111">3. leer el objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="e7d3f-111">3. Read the ASF Header Object</span></span>](#3-read-the-asf-header-object)
-   [<span data-ttu-id="e7d3f-112">4. crear el divisor de ASF</span><span class="sxs-lookup"><span data-stu-id="e7d3f-112">4. Create the ASF Splitter</span></span>](#4-create-the-asf-splitter)
-   [<span data-ttu-id="e7d3f-113">5. seleccionar una secuencia para el análisis</span><span class="sxs-lookup"><span data-stu-id="e7d3f-113">5. Select a Stream for Parsing</span></span>](#5-select-a-stream-for-parsing)
-   [<span data-ttu-id="e7d3f-114">6. generar ejemplos de medios comprimidos</span><span class="sxs-lookup"><span data-stu-id="e7d3f-114">6. Generate Compressed Media Samples</span></span>](#6-generate-compressed-media-samples)
-   [<span data-ttu-id="e7d3f-115">7. escribir la función Entry-Point</span><span class="sxs-lookup"><span data-stu-id="e7d3f-115">7. Write the Entry-Point Function</span></span>](#7-write-the-entry-point-function)
-   [<span data-ttu-id="e7d3f-116">Lista de programas</span><span class="sxs-lookup"><span data-stu-id="e7d3f-116">Program Listing</span></span>](#program-listing)
-   [<span data-ttu-id="e7d3f-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e7d3f-117">Related topics</span></span>](#related-topics)

<span data-ttu-id="e7d3f-118">En el tutorial no se explica cómo descodificar los datos comprimidos que la aplicación obtiene del divisor de ASF.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-118">The tutorial does not cover how to decode the compressed data that the application gets from the ASF splitter.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e7d3f-119">Requisitos previos</span><span class="sxs-lookup"><span data-stu-id="e7d3f-119">Prerequisites</span></span>

<span data-ttu-id="e7d3f-120">En este tutorial se da por hecho lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e7d3f-120">This tutorial assumes the following:</span></span>

-   <span data-ttu-id="e7d3f-121">Está familiarizado con la estructura de un archivo ASF y los componentes proporcionados por Media Foundation para trabajar con objetos ASF.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-121">You are familiar with the structure of an ASF file and the components provided by Media Foundation to work with ASF Objects.</span></span> <span data-ttu-id="e7d3f-122">Estos componentes incluyen el objeto ContentInfo, el divisor, el multiplexor y el perfil.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-122">These components include the ContentInfo object, splitter, multiplexer, and profile.</span></span> <span data-ttu-id="e7d3f-123">Para obtener más información, consulte [WMCONTAINER ASF Components](wmcontainer-asf-components.md).</span><span class="sxs-lookup"><span data-stu-id="e7d3f-123">For more information, see [WMContainer ASF Components](wmcontainer-asf-components.md).</span></span>
-   <span data-ttu-id="e7d3f-124">Está familiarizado con los [búferes multimedia](media-buffers.md) y los flujos de bytes: en concreto, las operaciones de archivo que utilizan un flujo de bytes, la lectura de una secuencia de bytes en un búfer multimedia y la escritura de contenido de un búfer multimedia en una secuencia de bytes.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-124">You are familiar with [Media Buffers](media-buffers.md) and byte streams: Specifically, file operations using a byte stream, reading from a byte stream into a media buffer, and writing the contents of a media buffer to a byte stream.</span></span>

## <a name="1-set-up-the-project"></a><span data-ttu-id="e7d3f-125">1. configurar el proyecto</span><span class="sxs-lookup"><span data-stu-id="e7d3f-125">1. Set up the Project</span></span>

<span data-ttu-id="e7d3f-126">Incluya los siguientes encabezados en el archivo de código fuente:</span><span class="sxs-lookup"><span data-stu-id="e7d3f-126">Include the following headers in your source file:</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>
```



<span data-ttu-id="e7d3f-127">Vínculo a los siguientes archivos de biblioteca:</span><span class="sxs-lookup"><span data-stu-id="e7d3f-127">Link to the following library files:</span></span>

-   <span data-ttu-id="e7d3f-128">mfplat. lib</span><span class="sxs-lookup"><span data-stu-id="e7d3f-128">mfplat.lib</span></span>
-   <span data-ttu-id="e7d3f-129">MF. lib</span><span class="sxs-lookup"><span data-stu-id="e7d3f-129">mf.lib</span></span>
-   <span data-ttu-id="e7d3f-130">mfuuid. lib</span><span class="sxs-lookup"><span data-stu-id="e7d3f-130">mfuuid.lib</span></span>

<span data-ttu-id="e7d3f-131">Declare la función [SafeRelease](saferelease.md) :</span><span class="sxs-lookup"><span data-stu-id="e7d3f-131">Declare the [SafeRelease](saferelease.md) function:</span></span>


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



## <a name="2-open-an-asf-file"></a><span data-ttu-id="e7d3f-132">2. abrir un archivo ASF</span><span class="sxs-lookup"><span data-stu-id="e7d3f-132">2. Open an ASF File</span></span>

<span data-ttu-id="e7d3f-133">A continuación, abra el archivo especificado mediante una llamada a la función [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) .</span><span class="sxs-lookup"><span data-stu-id="e7d3f-133">Next, open the specified file by calling the [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) function.</span></span> <span data-ttu-id="e7d3f-134">El método devuelve un puntero al objeto de flujo de bytes que incluye el contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-134">The method returns a pointer to the byte stream object that contains the contents of the file.</span></span> <span data-ttu-id="e7d3f-135">El nombre de archivo lo especifica el usuario a través de los argumentos de línea de comandos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-135">The filename is specified by the user through command line arguments of the application.</span></span>

<span data-ttu-id="e7d3f-136">El siguiente código de ejemplo toma un nombre de archivo y devuelve un puntero a un objeto de flujo de bytes que se puede usar para leer el archivo.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-136">The following example code takes a file name and returns a pointer to a byte stream object that can be used to read the file.</span></span>


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="3-read-the-asf-header-object"></a><span data-ttu-id="e7d3f-137">3. leer el objeto de encabezado ASF</span><span class="sxs-lookup"><span data-stu-id="e7d3f-137">3. Read the ASF Header Object</span></span>

<span data-ttu-id="e7d3f-138">A continuación, cree el [objeto ASF ContentInfo](asf-contentinfo-object.md) y úselo para analizar el objeto de encabezado ASF del archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-138">Next, create the [ASF ContentInfo Object](asf-contentinfo-object.md) and use it to parse the ASF Header Object of the specified file.</span></span> <span data-ttu-id="e7d3f-139">El objeto ContentInfo almacena información del encabezado ASF, incluidos los atributos de archivo globales e información sobre cada secuencia.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-139">The ContentInfo object stores information from the ASF header, including global file attributes and information about each stream.</span></span> <span data-ttu-id="e7d3f-140">Usará el objeto ContentInfo más adelante en el tutorial para inicializar el divisor de ASF y obtener el número de flujo de la secuencia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-140">You will use the ContentInfo object later in the tutorial to initialize the ASF splitter and get the stream number of the video stream.</span></span>

<span data-ttu-id="e7d3f-141">Para crear el objeto ContentInfo de ASF:</span><span class="sxs-lookup"><span data-stu-id="e7d3f-141">To create the ASF ContentInfo object:</span></span>

1.  <span data-ttu-id="e7d3f-142">Llame a la función [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para crear un objeto ContentInfo.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-142">Call the [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) function to create a ContentInfo object.</span></span> <span data-ttu-id="e7d3f-143">El método devuelve un puntero a la interfaz [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .</span><span class="sxs-lookup"><span data-stu-id="e7d3f-143">The method returns a pointer to the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) interface.</span></span>
2.  <span data-ttu-id="e7d3f-144">Lea los primeros 30 bytes de datos del archivo ASF en un búfer multimedia.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-144">Read the first 30 bytes of data from the ASF file into a media buffer.</span></span>
3.  <span data-ttu-id="e7d3f-145">Pase el búfer del medio al método [**IMFASFContentInfo:: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) .</span><span class="sxs-lookup"><span data-stu-id="e7d3f-145">Pass the media buffer to the [**IMFASFContentInfo::GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) method.</span></span> <span data-ttu-id="e7d3f-146">Este método devuelve el tamaño total del objeto de encabezado en el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-146">This method returns the total size of the Header Object in the ASF file.</span></span>
4.  <span data-ttu-id="e7d3f-147">Pase el mismo búfer multimedia al método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="e7d3f-147">Pass the same media buffer to the [**IMFASFContentInfo::ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span>
5.  <span data-ttu-id="e7d3f-148">Lea el resto del objeto de encabezado en un nuevo búfer multimedia.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-148">Read the remainder of the Header Object into a new media buffer.</span></span>
6.  <span data-ttu-id="e7d3f-149">Pase el segundo búfer al método [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .</span><span class="sxs-lookup"><span data-stu-id="e7d3f-149">Pass the second buffer to the [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) method.</span></span> <span data-ttu-id="e7d3f-150">Especifique el desplazamiento de 30 bytes en el parámetro *cbOffsetWithinHeader* de **ParseHeader**.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-150">Specify the 30-byte offset in the *cbOffsetWithinHeader* parameter of **ParseHeader**.</span></span> <span data-ttu-id="e7d3f-151">El método **ParseHeader** inicializa el objeto ContentInfo con la información recopilada de los distintos objetos ASF contenidos en el objeto de encabezado.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-151">The **ParseHeader** method initializes the ContentInfo object with information gathered from the various ASF objects contained in the Header Object.</span></span>


```C++
// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 
```



<span data-ttu-id="e7d3f-152">Esta función usa la `ReadFromByteStream` función para leer de una secuencia de bytes en un búfer multimedia:</span><span class="sxs-lookup"><span data-stu-id="e7d3f-152">This function uses the `ReadFromByteStream` function to read from a byte stream into a media buffer:</span></span>


```C++
// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size size of the 
// buffer, whichever is smaller. If the end of the byte stream is reached, the 
// actual amount of data read might be less than either of these values.
//
// To find out how much data was read, call IMFMediaBuffer::GetCurrentLength.

HRESULT ReadFromByteStream(
    IMFByteStream *pStream,     // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,    // Pointer to the media buffer.
    DWORD cbMax                 // Maximum amount to read.
    )
{
    DWORD cbBufferMax = 0;
    DWORD cbRead = 0;
    BYTE *pData= NULL;

    HRESULT hr = pBuffer->Lock(&pData, &cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax > cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream->Read(pData, cbMax, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer->Unlock();
    }
    return hr;
}
```



## <a name="4-create-the-asf-splitter"></a><span data-ttu-id="e7d3f-153">4. crear el divisor de ASF</span><span class="sxs-lookup"><span data-stu-id="e7d3f-153">4. Create the ASF Splitter</span></span>

<span data-ttu-id="e7d3f-154">A continuación, cree el objeto de [divisor de ASF](asf-splitter.md) .</span><span class="sxs-lookup"><span data-stu-id="e7d3f-154">Next, create the [ASF Splitter](asf-splitter.md) object.</span></span> <span data-ttu-id="e7d3f-155">Usará el divisor de ASF para analizar el objeto de datos ASF, que contiene datos multimedia de paquetes para el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-155">You will use the ASF splitter to parse the ASF Data Object, which contains packetized media data for the ASF file.</span></span>

<span data-ttu-id="e7d3f-156">Para crear un objeto divisor para el archivo ASF:</span><span class="sxs-lookup"><span data-stu-id="e7d3f-156">To create a splitter object for the ASF File:</span></span>

1.  <span data-ttu-id="e7d3f-157">Llame a la función [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) para crear el divisor de ASF.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-157">Call the [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) function to create the ASF splitter.</span></span> <span data-ttu-id="e7d3f-158">La función devuelve un puntero a la interfaz [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .</span><span class="sxs-lookup"><span data-stu-id="e7d3f-158">The function returns a pointer to the [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) interface.</span></span>
2.  <span data-ttu-id="e7d3f-159">Llame a [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) para inicializar el divisor de ASF.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-159">Call [**IMFASFSplitter::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) to initialize the ASF splitter.</span></span> <span data-ttu-id="e7d3f-160">Este método toma un puntero al objeto ContentInfo, que se creó en el procedimiento 3.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-160">This method takes a pointer to the ContentInfo object, which was created in procedure 3.</span></span>


```C++
// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}
```



## <a name="5-select-a-stream-for-parsing"></a><span data-ttu-id="e7d3f-161">5. seleccionar una secuencia para el análisis</span><span class="sxs-lookup"><span data-stu-id="e7d3f-161">5. Select a Stream for Parsing</span></span>

<span data-ttu-id="e7d3f-162">A continuación, enumere las secuencias del archivo ASF y seleccione la primera secuencia de vídeo para el análisis.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-162">Next, enumerate the streams in the ASF file and select the first video stream for parsing.</span></span> <span data-ttu-id="e7d3f-163">Para enumerar las secuencias, usará un objeto de perfil ASF y buscará secuencias que tengan un tipo de medio de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-163">To enumerate the streams, you will use an ASF profile object and search for streams that have a video media type.</span></span>

<span data-ttu-id="e7d3f-164">Para seleccionar la secuencia de vídeo:</span><span class="sxs-lookup"><span data-stu-id="e7d3f-164">To select the video stream:</span></span>

1.  <span data-ttu-id="e7d3f-165">Llame a [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) en el objeto ContentInfo para crear un perfil ASF.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-165">Call [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) on the ContentInfo object to create an ASF profile.</span></span> <span data-ttu-id="e7d3f-166">Entre otras informaciones, el perfil describe las secuencias del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-166">Among other information, the profile describes the streams in the ASF file.</span></span>
2.  <span data-ttu-id="e7d3f-167">Llame a [**IMFASFProfile:: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) para obtener el número de secuencias del archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-167">Call [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) to get the number of streams in the ASF file.</span></span>
3.  <span data-ttu-id="e7d3f-168">Llame a [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) en un bucle para enumerar las secuencias.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-168">Call [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) in a loop to enumerate the streams.</span></span> <span data-ttu-id="e7d3f-169">El método devuelve un puntero a la interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .</span><span class="sxs-lookup"><span data-stu-id="e7d3f-169">The method returns a pointer to the [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) interface.</span></span> <span data-ttu-id="e7d3f-170">También devuelve el identificador del flujo.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-170">It also returns the stream identifier.</span></span>
4.  <span data-ttu-id="e7d3f-171">Llame a [**IMFASFStreamConfig:: GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) para obtener el GUID de tipo principal de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-171">Call [**IMFASFStreamConfig::GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) to get the major type GUID for the stream.</span></span> <span data-ttu-id="e7d3f-172">Si el GUID de tipo principal es MFMediaType \_ video, el flujo contiene vídeo.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-172">If the major type GUID is MFMediaType\_Video, the stream contains video.</span></span>
5.  <span data-ttu-id="e7d3f-173">Si encuentra una secuencia de vídeo en el paso 4, llame a [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) para seleccionar la secuencia.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-173">If you found a video stream in step 4, call [**IMFASFSplitter::SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) to select the stream.</span></span> <span data-ttu-id="e7d3f-174">Este método toma una matriz de identificadores de secuencia.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-174">This method takes an array of stream identifiers.</span></span> <span data-ttu-id="e7d3f-175">En este tutorial, el tamaño de la matriz es 1 porque la aplicación analizará un solo flujo.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-175">For this tutorial, the array size is 1 because the application will parse a single stream.</span></span>

<span data-ttu-id="e7d3f-176">En el código de ejemplo siguiente se enumeran las secuencias del archivo ASF y se selecciona la primera secuencia de vídeo en el divisor ASF:</span><span class="sxs-lookup"><span data-stu-id="e7d3f-176">The following example code enumerates the streams in the ASF file and selects the first video stream on the ASF splitter:</span></span>


```C++
// Select the first video stream for parsing with the ASF splitter.

HRESULT SelectVideoStream(IMFASFContentInfo *pContentInfo, 
    IMFASFSplitter *pSplitter, BOOL *pbHasVideo)
{
    DWORD   cStreams = 0;
    WORD    wStreamID = 0;

    IMFASFProfile *pProfile = NULL;
    IMFASFStreamConfig *pStream = NULL;

    // Get the ASF profile from the ContentInfo object.
    HRESULT hr = pContentInfo->GetProfile(&pProfile);

    // Loop through all of the streams in the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&cStreams);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            GUID    streamType = GUID_NULL;

            // Get the stream type and stream identifier.
            hr = pProfile->GetStream(i, &wStreamID, &pStream);
            if (FAILED(hr)) 
            {
                break;
            }

            hr = pStream->GetStreamType(&streamType);
            if (FAILED(hr)) 
            {
                break;
            }

            if (streamType == MFMediaType_Video)
            {
                *pbHasVideo = TRUE;
                break;
            }
            SafeRelease(&pStream);
        }
    }

    // Select the video stream, if found.
    if (SUCCEEDED(hr))
    {
        if (*pbHasVideo)
        {
            // SelectStreams takes an array of stream identifiers.
            hr = pSplitter->SelectStreams(&wStreamID, 1);
        }
    }
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    return hr;
}
```



## <a name="6-generate-compressed-media-samples"></a><span data-ttu-id="e7d3f-177">6. generar ejemplos de medios comprimidos</span><span class="sxs-lookup"><span data-stu-id="e7d3f-177">6. Generate Compressed Media Samples</span></span>

<span data-ttu-id="e7d3f-178">A continuación, use el divisor de ASF para analizar el objeto de datos ASF y obtener los paquetes de datos de la secuencia de vídeo seleccionada.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-178">Next, use the ASF splitter to parse the ASF Data Object and get the data packets for the selected video stream.</span></span> <span data-ttu-id="e7d3f-179">La aplicación Lee los datos del archivo ASF en bloques de tamaño fijo y pasa los datos al divisor de ASF.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-179">The application reads data from the ASF file in fixed-size blocks and passes the data to the ASF splitter.</span></span> <span data-ttu-id="e7d3f-180">El divisor analiza los datos y genera [ejemplos de medios](media-samples.md) que contienen los datos de vídeo comprimidos.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-180">The splitter parses the data and generates [Media Samples](media-samples.md) that contain the compressed video data.</span></span> <span data-ttu-id="e7d3f-181">La aplicación comprueba si cada ejemplo representa un fotograma clave.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-181">The application checks whether each sample represents a key frame.</span></span> <span data-ttu-id="e7d3f-182">Si es así, la aplicación muestra información básica sobre el ejemplo:</span><span class="sxs-lookup"><span data-stu-id="e7d3f-182">If so, the application displays some basic information about the sample:</span></span>

-   <span data-ttu-id="e7d3f-183">Número de búferes multimedia</span><span class="sxs-lookup"><span data-stu-id="e7d3f-183">Number of media buffers</span></span>
-   <span data-ttu-id="e7d3f-184">Tamaño total de los datos</span><span class="sxs-lookup"><span data-stu-id="e7d3f-184">Total size of the data</span></span>
-   <span data-ttu-id="e7d3f-185">Marca de tiempo</span><span class="sxs-lookup"><span data-stu-id="e7d3f-185">Time stamp</span></span>

<span data-ttu-id="e7d3f-186">Para generar ejemplos de medios comprimidos:</span><span class="sxs-lookup"><span data-stu-id="e7d3f-186">To generate compressed media samples:</span></span>

1.  <span data-ttu-id="e7d3f-187">Asigne un nuevo búfer multimedia.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-187">Allocate a new media buffer.</span></span>
2.  <span data-ttu-id="e7d3f-188">Leer datos de la secuencia de bytes en el búfer multimedia.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-188">Read data from the byte stream into the media buffer.</span></span>
3.  <span data-ttu-id="e7d3f-189">Pase el búfer multimedia al método [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) .</span><span class="sxs-lookup"><span data-stu-id="e7d3f-189">Pass the media buffer to the [**IMFASFSplitter::ParseData**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) method.</span></span> <span data-ttu-id="e7d3f-190">El método analiza los datos ASF en el búfer.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-190">The method parses the ASF data in the buffer.</span></span>
4.  <span data-ttu-id="e7d3f-191">En un bucle, obtenga ejemplos de medios del divisor llamando a [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="e7d3f-191">In a loop, get media samples from the splitter by calling [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample).</span></span> <span data-ttu-id="e7d3f-192">Si el parámetro *ppISample* recibe un puntero [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) válido, significa que el divisor de ASF ha analizado uno o varios paquetes de datos.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-192">If the *ppISample* parameter receives a valid [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) pointer, it means the ASF splitter has parsed one or more data packets.</span></span> <span data-ttu-id="e7d3f-193">Si *ppISample* recibe el valor **null**, interrumpa el bucle y vuelva al paso 1.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-193">If *ppISample* receives the value **NULL**, break from the loop and go back to step 1.</span></span>
5.  <span data-ttu-id="e7d3f-194">Muestra información sobre el ejemplo.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-194">Display information about the sample.</span></span>
6.  <span data-ttu-id="e7d3f-195">Interrumpa el bucle en las siguientes condiciones:</span><span class="sxs-lookup"><span data-stu-id="e7d3f-195">Break from the loop in the following conditions:</span></span>
    -   <span data-ttu-id="e7d3f-196">El parámetro *ppISample* recibe el valor **null**.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-196">The *ppISample* parameter receives the value **NULL**.</span></span>
    -   <span data-ttu-id="e7d3f-197">El parámetro *pdwStatusFlags* no recibe la marca **ASF \_ STATUSFLAGS \_ incompleta** .</span><span class="sxs-lookup"><span data-stu-id="e7d3f-197">The *pdwStatusFlags* parameter does not receive the **ASF\_STATUSFLAGS\_INCOMPLETE** flag.</span></span>

<span data-ttu-id="e7d3f-198">Repita estos pasos hasta que llegue al final del archivo.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-198">Repeat these steps until you reach the end of the file.</span></span> <span data-ttu-id="e7d3f-199">El siguiente código muestra estos pasos:</span><span class="sxs-lookup"><span data-stu-id="e7d3f-199">The following code shows these steps:</span></span>


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



<span data-ttu-id="e7d3f-200">La función IsKeyFrame comprueba si un ejemplo es un fotograma clave, obteniendo el valor del atributo [**\_ CleanPoint de MFSampleExtension**](mfsampleextension-cleanpoint-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="e7d3f-200">The IsKeyFrame function tests whether a sample is a key frame, by getting the value of the [**MFSampleExtension\_CleanPoint**](mfsampleextension-cleanpoint-attribute.md) attribute.</span></span>


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



<span data-ttu-id="e7d3f-201">A efectos de Ilustración, en este tutorial se muestra información sobre cada fotograma clave de vídeo llamando a la siguiente función:</span><span class="sxs-lookup"><span data-stu-id="e7d3f-201">For illustration purposes, this tutorial displays some information for each video key frame, by calling the following function:</span></span>


```C++
void DisplayKeyFrame(IMFSample *pSample)
{
    DWORD   cBuffers = 0;           // Buffer count
    DWORD   cbTotalLength = 0;      // Buffer length
    MFTIME  hnsTime = 0;            // Time stamp

    // Print various information about the key frame.
    if (SUCCEEDED(pSample->GetBufferCount(&cBuffers)))
    {
        wprintf_s(L"Buffer count: %d\n", cBuffers);
    }
    if (SUCCEEDED(pSample->GetTotalLength(&cbTotalLength)))
    {
        wprintf_s(L"Length: %d bytes\n", cbTotalLength);
    }
    if (SUCCEEDED(pSample->GetSampleTime(&hnsTime)))
    {
        // Convert the time stamp to seconds.
        double sec = static_cast<double>(hnsTime / 10000) / 1000;
        wprintf_s(L"Time stamp: %f sec.\n", sec);
    }
    wprintf_s(L"\n");
}
```



<span data-ttu-id="e7d3f-202">Una aplicación típica usaría los paquetes de datos para la descodificación, remuxing, el envío a través de la red o alguna otra tarea.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-202">A typical application would use the data packets for decoding, remuxing, sending over the network, or some other task.</span></span>

## <a name="7-write-the-entry-point-function"></a><span data-ttu-id="e7d3f-203">7. escribir la función Entry-Point</span><span class="sxs-lookup"><span data-stu-id="e7d3f-203">7. Write the Entry-Point Function</span></span>

<span data-ttu-id="e7d3f-204">Ahora puede poner los pasos anteriores juntos en una aplicación completa.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-204">Now you can put the previous steps together into a complete application.</span></span> <span data-ttu-id="e7d3f-205">Antes de usar cualquiera de los objetos Media Foundation, inicialice la plataforma de Media Foundation mediante una llamada a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span><span class="sxs-lookup"><span data-stu-id="e7d3f-205">Before using any of the Media Foundation objects, initialize the Media Foundation platform by calling [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup).</span></span> <span data-ttu-id="e7d3f-206">Cuando haya terminado, llame a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span><span class="sxs-lookup"><span data-stu-id="e7d3f-206">When you are done, call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).</span></span> <span data-ttu-id="e7d3f-207">Para obtener más información, [inicializar Media Foundation](initializing-media-foundation.md).</span><span class="sxs-lookup"><span data-stu-id="e7d3f-207">For more information, [Initializing Media Foundation](initializing-media-foundation.md).</span></span>


```C++
int wmain(int argc, WCHAR* argv[])
{
    if (argc != 2)
    {
        _s(L"Usage: %s input.wmv");
        return 0;
    }

    // Start the Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        PCWSTR pszFileName = argv[1]; 
        BOOL   bHasVideo = FALSE;

        IMFByteStream       *pStream = NULL;
        IMFASFContentInfo   *pContentInfo = NULL;
        IMFASFSplitter      *pSplitter = NULL;

        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);

        // Read the ASF header.
        if (SUCCEEDED(hr))
        {
            hr = CreateContentInfo(pStream, &pContentInfo);
        }

        // Create the ASF splitter.
        if (SUCCEEDED(hr))
        {
            hr = CreateASFSplitter(pContentInfo, &pSplitter);
        }

        // Select the first video stream.
        if (SUCCEEDED(hr))
        {
            hr = SelectVideoStream(pContentInfo, pSplitter, &bHasVideo);
        }

        // Parse the ASF file.
        if (SUCCEEDED(hr))
        {
            if (bHasVideo)
            {
                hr = DisplayKeyFrames(pStream, pSplitter);
            }
            else
            {
                wprintf_s(L"No video stream.\n");
            }
        }
        SafeRelease(&pSplitter);
        SafeRelease(&pContentInfo);
        SafeRelease(&pStream);
    
        // Shut down the Media Foundation platform.
        MFShutdown();
    }
    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="program-listing"></a><span data-ttu-id="e7d3f-208">Lista de programas</span><span class="sxs-lookup"><span data-stu-id="e7d3f-208">Program Listing</span></span>

<span data-ttu-id="e7d3f-209">En el código siguiente se muestra la lista completa del tutorial.</span><span class="sxs-lookup"><span data-stu-id="e7d3f-209">The following code shows the complete listing for the tutorial.</span></span>


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>

#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// Read data from a byte stream into a media buffer.
//
// This function reads a maximum of cbMax bytes, or up to the size size of the 
// buffer, whichever is smaller. If the end of the byte stream is reached, the 
// actual amount of data read might be less than either of these values.
//
// To find out how much data was read, call IMFMediaBuffer::GetCurrentLength.

HRESULT ReadFromByteStream(
    IMFByteStream *pStream,     // Pointer to the byte stream.
    IMFMediaBuffer *pBuffer,    // Pointer to the media buffer.
    DWORD cbMax                 // Maximum amount to read.
    )
{
    DWORD cbBufferMax = 0;
    DWORD cbRead = 0;
    BYTE *pData= NULL;

    HRESULT hr = pBuffer->Lock(&pData, &cbBufferMax, NULL);

    // Do not exceed the maximum size of the buffer.
    if (SUCCEEDED(hr))
    {
        if (cbMax > cbBufferMax)
        {
            cbMax = cbBufferMax;
        }

        // Read up to cbMax bytes.
        hr = pStream->Read(pData, cbMax, &cbRead);
    }

    // Update the size of the valid data in the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbRead);
    }
    if (pData)
    {
        pBuffer->Unlock();
    }
    return hr;
}


// Read the ASF Header Object from a byte stream and return a pointer to the 
// populated ASF ContentInfo object.
//
// The current read position of the byte stream must be at the start of the
// ASF Header Object.

HRESULT CreateContentInfo(IMFByteStream *pStream, 
    IMFASFContentInfo **ppContentInfo)
{
    const DWORD MIN_ASF_HEADER_SIZE = 30;
    
    QWORD cbHeader = 0;
    DWORD cbBuffer = 0;

    IMFASFContentInfo *pContentInfo = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    // Create the ASF ContentInfo object.
    HRESULT hr = MFCreateASFContentInfo(&pContentInfo);
    
    // Read the first 30 bytes to find the total header size.

    if (SUCCEEDED(hr))
    {
        hr = MFCreateMemoryBuffer(MIN_ASF_HEADER_SIZE, &pBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer,MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->GetHeaderSize(pBuffer, &cbHeader);
    }

    // Pass the first 30 bytes to the ContentInfo object.
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, 0);
    }

    SafeRelease(&pBuffer);

    if (SUCCEEDED(hr))
    {
        cbBuffer = (DWORD)(cbHeader - MIN_ASF_HEADER_SIZE);

        hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);
    }

    // Read the rest of the header and finish parsing the header.
    if (SUCCEEDED(hr))
    {
        hr = ReadFromByteStream(pStream, pBuffer, cbBuffer);
    }
    if (SUCCEEDED(hr))
    {
        hr = pContentInfo->ParseHeader(pBuffer, MIN_ASF_HEADER_SIZE);
    }
    if (SUCCEEDED(hr))
    {
        // Return the pointer to the caller.
        *ppContentInfo = pContentInfo;
        (*ppContentInfo)->AddRef();
    }
    SafeRelease(&pBuffer);
    SafeRelease(&pContentInfo);
    return hr;
} 

// Create and initialize the ASF splitter.

HRESULT CreateASFSplitter (IMFASFContentInfo* pContentInfo, 
    IMFASFSplitter** ppSplitter)
{
    IMFASFSplitter *pSplitter = NULL;

    // Create the splitter object.
    HRESULT hr = MFCreateASFSplitter(&pSplitter);

    // Initialize the splitter to work with specific ASF data.
    if (SUCCEEDED(hr))
    {
        hr = pSplitter->Initialize(pContentInfo);
    }
    if (SUCCEEDED(hr))
    {
        // Return the object to the caller.
        *ppSplitter = pSplitter;
        (*ppSplitter)->AddRef();
    }
    SafeRelease(&pSplitter);
    return hr;
}


// Select the first video stream for parsing with the ASF splitter.

HRESULT SelectVideoStream(IMFASFContentInfo *pContentInfo, 
    IMFASFSplitter *pSplitter, BOOL *pbHasVideo)
{
    DWORD   cStreams = 0;
    WORD    wStreamID = 0;

    IMFASFProfile *pProfile = NULL;
    IMFASFStreamConfig *pStream = NULL;

    // Get the ASF profile from the ContentInfo object.
    HRESULT hr = pContentInfo->GetProfile(&pProfile);

    // Loop through all of the streams in the profile.
    if (SUCCEEDED(hr))
    {
        hr = pProfile->GetStreamCount(&cStreams);
    }

    if (SUCCEEDED(hr))
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            GUID    streamType = GUID_NULL;

            // Get the stream type and stream identifier.
            hr = pProfile->GetStream(i, &wStreamID, &pStream);
            if (FAILED(hr)) 
            {
                break;
            }

            hr = pStream->GetStreamType(&streamType);
            if (FAILED(hr)) 
            {
                break;
            }

            if (streamType == MFMediaType_Video)
            {
                *pbHasVideo = TRUE;
                break;
            }
            SafeRelease(&pStream);
        }
    }

    // Select the video stream, if found.
    if (SUCCEEDED(hr))
    {
        if (*pbHasVideo)
        {
            // SelectStreams takes an array of stream identifiers.
            hr = pSplitter->SelectStreams(&wStreamID, 1);
        }
    }
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    return hr;
}

inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}

void DisplayKeyFrame(IMFSample *pSample)
{
    DWORD   cBuffers = 0;           // Buffer count
    DWORD   cbTotalLength = 0;      // Buffer length
    MFTIME  hnsTime = 0;            // Time stamp

    // Print various information about the key frame.
    if (SUCCEEDED(pSample->GetBufferCount(&cBuffers)))
    {
        wprintf_s(L"Buffer count: %d\n", cBuffers);
    }
    if (SUCCEEDED(pSample->GetTotalLength(&cbTotalLength)))
    {
        wprintf_s(L"Length: %d bytes\n", cbTotalLength);
    }
    if (SUCCEEDED(pSample->GetSampleTime(&hnsTime)))
    {
        // Convert the time stamp to seconds.
        double sec = static_cast<double>(hnsTime / 10000) / 1000;
        wprintf_s(L"Time stamp: %f sec.\n", sec);
    }
    wprintf_s(L"\n");
}


// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}

int wmain(int argc, WCHAR* argv[])
{
    if (argc != 2)
    {
        _s(L"Usage: %s input.wmv");
        return 0;
    }

    // Start the Media Foundation platform.
    HRESULT hr = MFStartup(MF_VERSION);
    if (SUCCEEDED(hr))
    {
        PCWSTR pszFileName = argv[1]; 
        BOOL   bHasVideo = FALSE;

        IMFByteStream       *pStream = NULL;
        IMFASFContentInfo   *pContentInfo = NULL;
        IMFASFSplitter      *pSplitter = NULL;

        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);

        // Read the ASF header.
        if (SUCCEEDED(hr))
        {
            hr = CreateContentInfo(pStream, &pContentInfo);
        }

        // Create the ASF splitter.
        if (SUCCEEDED(hr))
        {
            hr = CreateASFSplitter(pContentInfo, &pSplitter);
        }

        // Select the first video stream.
        if (SUCCEEDED(hr))
        {
            hr = SelectVideoStream(pContentInfo, pSplitter, &bHasVideo);
        }

        // Parse the ASF file.
        if (SUCCEEDED(hr))
        {
            if (bHasVideo)
            {
                hr = DisplayKeyFrames(pStream, pSplitter);
            }
            else
            {
                wprintf_s(L"No video stream.\n");
            }
        }
        SafeRelease(&pSplitter);
        SafeRelease(&pContentInfo);
        SafeRelease(&pStream);
    
        // Shut down the Media Foundation platform.
        MFShutdown();
    }
    if (FAILED(hr))
    {
        wprintf_s(L"Error: 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="related-topics"></a><span data-ttu-id="e7d3f-210">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e7d3f-210">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7d3f-211">Componentes de WMContainer ASF</span><span class="sxs-lookup"><span data-stu-id="e7d3f-211">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="e7d3f-212">Compatibilidad con ASF en Media Foundation</span><span class="sxs-lookup"><span data-stu-id="e7d3f-212">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



