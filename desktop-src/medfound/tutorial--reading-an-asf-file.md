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
# <a name="tutorial-reading-an-asf-file-by-using-wmcontainer-objects"></a>Tutorial: lectura de un archivo ASF mediante objetos WMContainer

En este tutorial se muestra cómo obtener paquetes de datos de un archivo de formato de sistema avanzado (ASF) mediante el [divisor de ASF](asf-splitter.md). En este tutorial, creará una aplicación de consola simple que lee un archivo ASF y genera ejemplos de medios comprimidos para la primera secuencia de vídeo del archivo. La aplicación muestra información sobre los fotogramas clave en el flujo de vídeo.

Este tutorial contiene los siguientes pasos:

-   [Requisitos previos](#prerequisites)
-   [1. configurar el proyecto](#1-set-up-the-project)
-   [2. abrir un archivo ASF](#2-open-an-asf-file)
-   [3. leer el objeto de encabezado ASF](#3-read-the-asf-header-object)
-   [4. crear el divisor de ASF](#4-create-the-asf-splitter)
-   [5. seleccionar una secuencia para el análisis](#5-select-a-stream-for-parsing)
-   [6. generar ejemplos de medios comprimidos](#6-generate-compressed-media-samples)
-   [7. escribir la función Entry-Point](#7-write-the-entry-point-function)
-   [Lista de programas](#program-listing)
-   [Temas relacionados](#related-topics)

En el tutorial no se explica cómo descodificar los datos comprimidos que la aplicación obtiene del divisor de ASF.

## <a name="prerequisites"></a>Requisitos previos

En este tutorial se da por hecho lo siguiente:

-   Está familiarizado con la estructura de un archivo ASF y los componentes proporcionados por Media Foundation para trabajar con objetos ASF. Estos componentes incluyen el objeto ContentInfo, el divisor, el multiplexor y el perfil. Para obtener más información, consulte [WMCONTAINER ASF Components](wmcontainer-asf-components.md).
-   Está familiarizado con los [búferes multimedia](media-buffers.md) y los flujos de bytes: en concreto, las operaciones de archivo que utilizan un flujo de bytes, la lectura de una secuencia de bytes en un búfer multimedia y la escritura de contenido de un búfer multimedia en una secuencia de bytes.

## <a name="1-set-up-the-project"></a>1. configurar el proyecto

Incluya los siguientes encabezados en el archivo de código fuente:


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <Mferror.h>
```



Vínculo a los siguientes archivos de biblioteca:

-   mfplat. lib
-   MF. lib
-   mfuuid. lib

Declare la función [SafeRelease](saferelease.md) :


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



## <a name="2-open-an-asf-file"></a>2. abrir un archivo ASF

A continuación, abra el archivo especificado mediante una llamada a la función [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) . El método devuelve un puntero al objeto de flujo de bytes que incluye el contenido del archivo. El nombre de archivo lo especifica el usuario a través de los argumentos de línea de comandos de la aplicación.

El siguiente código de ejemplo toma un nombre de archivo y devuelve un puntero a un objeto de flujo de bytes que se puede usar para leer el archivo.


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="3-read-the-asf-header-object"></a>3. leer el objeto de encabezado ASF

A continuación, cree el [objeto ASF ContentInfo](asf-contentinfo-object.md) y úselo para analizar el objeto de encabezado ASF del archivo especificado. El objeto ContentInfo almacena información del encabezado ASF, incluidos los atributos de archivo globales e información sobre cada secuencia. Usará el objeto ContentInfo más adelante en el tutorial para inicializar el divisor de ASF y obtener el número de flujo de la secuencia de vídeo.

Para crear el objeto ContentInfo de ASF:

1.  Llame a la función [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para crear un objeto ContentInfo. El método devuelve un puntero a la interfaz [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .
2.  Lea los primeros 30 bytes de datos del archivo ASF en un búfer multimedia.
3.  Pase el búfer del medio al método [**IMFASFContentInfo:: GetHeaderSize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) . Este método devuelve el tamaño total del objeto de encabezado en el archivo ASF.
4.  Pase el mismo búfer multimedia al método [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) .
5.  Lea el resto del objeto de encabezado en un nuevo búfer multimedia.
6.  Pase el segundo búfer al método [**ParseHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) . Especifique el desplazamiento de 30 bytes en el parámetro *cbOffsetWithinHeader* de **ParseHeader**. El método **ParseHeader** inicializa el objeto ContentInfo con la información recopilada de los distintos objetos ASF contenidos en el objeto de encabezado.


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



Esta función usa la `ReadFromByteStream` función para leer de una secuencia de bytes en un búfer multimedia:


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



## <a name="4-create-the-asf-splitter"></a>4. crear el divisor de ASF

A continuación, cree el objeto de [divisor de ASF](asf-splitter.md) . Usará el divisor de ASF para analizar el objeto de datos ASF, que contiene datos multimedia de paquetes para el archivo ASF.

Para crear un objeto divisor para el archivo ASF:

1.  Llame a la función [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) para crear el divisor de ASF. La función devuelve un puntero a la interfaz [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .
2.  Llame a [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize) para inicializar el divisor de ASF. Este método toma un puntero al objeto ContentInfo, que se creó en el procedimiento 3.


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



## <a name="5-select-a-stream-for-parsing"></a>5. seleccionar una secuencia para el análisis

A continuación, enumere las secuencias del archivo ASF y seleccione la primera secuencia de vídeo para el análisis. Para enumerar las secuencias, usará un objeto de perfil ASF y buscará secuencias que tengan un tipo de medio de vídeo.

Para seleccionar la secuencia de vídeo:

1.  Llame a [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile) en el objeto ContentInfo para crear un perfil ASF. Entre otras informaciones, el perfil describe las secuencias del archivo ASF.
2.  Llame a [**IMFASFProfile:: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) para obtener el número de secuencias del archivo ASF.
3.  Llame a [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) en un bucle para enumerar las secuencias. El método devuelve un puntero a la interfaz [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) . También devuelve el identificador del flujo.
4.  Llame a [**IMFASFStreamConfig:: GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) para obtener el GUID de tipo principal de la secuencia. Si el GUID de tipo principal es MFMediaType \_ video, el flujo contiene vídeo.
5.  Si encuentra una secuencia de vídeo en el paso 4, llame a [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams) para seleccionar la secuencia. Este método toma una matriz de identificadores de secuencia. En este tutorial, el tamaño de la matriz es 1 porque la aplicación analizará un solo flujo.

En el código de ejemplo siguiente se enumeran las secuencias del archivo ASF y se selecciona la primera secuencia de vídeo en el divisor ASF:


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



## <a name="6-generate-compressed-media-samples"></a>6. generar ejemplos de medios comprimidos

A continuación, use el divisor de ASF para analizar el objeto de datos ASF y obtener los paquetes de datos de la secuencia de vídeo seleccionada. La aplicación Lee los datos del archivo ASF en bloques de tamaño fijo y pasa los datos al divisor de ASF. El divisor analiza los datos y genera [ejemplos de medios](media-samples.md) que contienen los datos de vídeo comprimidos. La aplicación comprueba si cada ejemplo representa un fotograma clave. Si es así, la aplicación muestra información básica sobre el ejemplo:

-   Número de búferes multimedia
-   Tamaño total de los datos
-   Marca de tiempo

Para generar ejemplos de medios comprimidos:

1.  Asigne un nuevo búfer multimedia.
2.  Leer datos de la secuencia de bytes en el búfer multimedia.
3.  Pase el búfer multimedia al método [**IMFASFSplitter::P arsedata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) . El método analiza los datos ASF en el búfer.
4.  En un bucle, obtenga ejemplos de medios del divisor llamando a [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample). Si el parámetro *ppISample* recibe un puntero [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) válido, significa que el divisor de ASF ha analizado uno o varios paquetes de datos. Si *ppISample* recibe el valor **null**, interrumpa el bucle y vuelva al paso 1.
5.  Muestra información sobre el ejemplo.
6.  Interrumpa el bucle en las siguientes condiciones:
    -   El parámetro *ppISample* recibe el valor **null**.
    -   El parámetro *pdwStatusFlags* no recibe la marca **ASF \_ STATUSFLAGS \_ incompleta** .

Repita estos pasos hasta que llegue al final del archivo. El siguiente código muestra estos pasos:


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



La función IsKeyFrame comprueba si un ejemplo es un fotograma clave, obteniendo el valor del atributo [**\_ CleanPoint de MFSampleExtension**](mfsampleextension-cleanpoint-attribute.md) .


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



A efectos de Ilustración, en este tutorial se muestra información sobre cada fotograma clave de vídeo llamando a la siguiente función:


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



Una aplicación típica usaría los paquetes de datos para la descodificación, remuxing, el envío a través de la red o alguna otra tarea.

## <a name="7-write-the-entry-point-function"></a>7. escribir la función Entry-Point

Ahora puede poner los pasos anteriores juntos en una aplicación completa. Antes de usar cualquiera de los objetos Media Foundation, inicialice la plataforma de Media Foundation mediante una llamada a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Cuando haya terminado, llame a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown). Para obtener más información, [inicializar Media Foundation](initializing-media-foundation.md).


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



## <a name="program-listing"></a>Lista de programas

En el código siguiente se muestra la lista completa del tutorial.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de WMContainer ASF](wmcontainer-asf-components.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



