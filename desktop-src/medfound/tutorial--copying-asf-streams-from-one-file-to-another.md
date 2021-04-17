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
# <a name="tutorial-copying-asf-streams-by-using-wmcontainer-objects"></a>Tutorial: copiar secuencias ASF mediante objetos WMContainer

Una manera de crear un archivo ASF es copiar secuencias ASF desde un archivo existente. Para ello, puede recuperar los datos multimedia del archivo de origen y escribir en el archivo de salida. Si el archivo de origen es un archivo ASF, puede copiar ejemplos de secuencias sin descomprimirlos y volver a comprimirlos.

En este tutorial se muestra este escenario mediante la extracción de la primera secuencia de audio de un archivo de audio y vídeo ASF (. wmv) y su copia en un nuevo archivo de audio ASF (. WMA). En este tutorial, creará una aplicación de consola que toma los nombres de archivo de entrada y salida como argumentos. La aplicación utiliza el divisor ASF para analizar los ejemplos de flujo de entrada y, a continuación, los envía al multiplexor ASF para escribir los paquetes de datos ASF para la secuencia de audio.

Este tutorial contiene los siguientes pasos:

-   [Requisitos previos](#prerequisites)
-   [Terminología](#terminology)
-   [1. configurar el proyecto](#1-set-up-the-project)
-   [2. declarar funciones auxiliares](#2-declare-helper-functions)
-   [3. abrir el archivo ASF de entrada](#3-open-the-input-asf-file)
-   [4. inicializar objetos para el archivo de entrada](#4-initialize-objects-for-the-input-file)
-   [5. crear un perfil de audio](#5-create-an-audio-profile)
-   [6. inicializar los objetos para el archivo de salida](#6-initialize-objects-for-the-output-file)
-   [7. generar nuevos paquetes de datos ASF](#7-generate-new-asf-data-packets)
-   [8. escribir los objetos ASF en el nuevo archivo](#8-write-the-asf-objects-in-the-new-file)
-   [9 escribir la función Entry-Point](#9-write-the-entry-point-function)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Requisitos previos

En este tutorial se da por hecho lo siguiente:

-   Está familiarizado con la estructura de un archivo ASF y los componentes proporcionados por Media Foundation para trabajar con objetos ASF. Estos componentes incluyen los objetos ContentInfo, Splitter, multiplexor y Profile. Para obtener más información, consulte [WMCONTAINER ASF Components](wmcontainer-asf-components.md).
-   Está familiarizado con el proceso de analizar el objeto de encabezado ASF y los paquetes de datos ASF de un archivo existente y generar ejemplos de secuencias comprimidas mediante el divisor. Para obtener más información, consulte [Tutorial: leer un archivo ASF](tutorial--reading-an-asf-file.md).
-   Está familiarizado con los búferes multimedia y los flujos de bytes: en concreto, las operaciones de archivo que usan un flujo de bytes y la escritura del contenido de un búfer multimedia en una secuencia de bytes. (Consulte [2. Declare las funciones auxiliares](#2-declare-helper-functions)).

## <a name="terminology"></a>Terminología

En este tutorial se usan los siguientes términos:

-   Secuencia de bytes de origen: objeto de secuencia de bytes, expone la interfaz [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que incluye el contenido del archivo de entrada.
-   Source ContentInfo Object: ContentInfo Object, expone la interfaz [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , que representa el objeto de encabezado ASF del archivo de entrada.
-   Perfil de audio: objeto de perfil, expone la interfaz [**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) , que solo contiene secuencias de audio del archivo de entrada.
-   Stream Sample: ejemplo multimedia, expone la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , generada por el divisor representa los datos multimedia del flujo seleccionado obtenidos del archivo de entrada en estado comprimido.
-   OUTPUT ContentInfo Object: ContentInfo Object, expone la interfaz [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) , que representa el objeto de encabezado ASF del archivo de salida.
-   Secuencia de bytes de datos: objeto de secuencia de bytes, expone la interfaz [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que representa la parte del objeto de datos ASF completa del archivo de salida.
-   Paquete de datos: el ejemplo multimedia, expone la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , generada por el multiplexor representa un paquete de datos ASF que se escribirá en la secuencia de bytes de datos.
-   Secuencia de bytes de salida: objeto de flujo de bytes, expone la interfaz [**IMFByteStream**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) , que incluye el contenido del archivo de salida.

## <a name="1-set-up-the-project"></a>1. configurar el proyecto

Incluya los siguientes encabezados en el archivo de código fuente:


```C++
#include <stdio.h>       // Standard I/O
#include <windows.h>     // Windows headers
#include <mfapi.h>       // Media Foundation platform
#include <wmcontainer.h> // ASF interfaces
#include <mferror.h>     // Media Foundation error codes
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



## <a name="2-declare-helper-functions"></a>2. declarar funciones auxiliares

En este tutorial se usan las siguientes funciones auxiliares para leer y escribir en una secuencia de bytes.

La `AllocReadFromByteStream` función Lee los datos de una secuencia de bytes y asigna un nuevo búfer multimedia para contener los datos. Para obtener más información, vea [**IMFByteStream:: Read**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-read).


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



La `WriteBufferToByteStream` función escribe datos de un búfer multimedia en una secuencia de bytes. Para obtener más información, vea [**IMFByteStream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write).


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



La `AppendToByteStream` función anexa el contenido de un flujo de bytes a otro:


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



## <a name="3-open-the-input-asf-file"></a>3. abrir el archivo ASF de entrada

Abra el archivo de entrada mediante una llamada a la función [**MFCreateFile**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatefile) . El método devuelve un puntero al objeto de flujo de bytes que incluye el contenido del archivo. El nombre de archivo lo especifica el usuario a través de los argumentos de línea de comandos de la aplicación.

El siguiente código de ejemplo toma un nombre de archivo y devuelve un puntero a un objeto de flujo de bytes que se puede usar para leer el archivo.


```C++
        // Open the file.
        hr = MFCreateFile(MF_ACCESSMODE_READ, MF_OPENMODE_FAIL_IF_NOT_EXIST, 
            MF_FILEFLAGS_NONE, pszFileName, &pStream);
```



## <a name="4-initialize-objects-for-the-input-file"></a>4. inicializar objetos para el archivo de entrada

A continuación, creará e inicializará el objeto ContentInfo de origen y el divisor para generar ejemplos de secuencias.

Esta secuencia de bytes de origen creada en el paso 2 se usará para analizar el objeto de encabezado ASF y rellenar el objeto ContentInfo de origen. Este objeto se usará para inicializar el divisor y facilitar el análisis de los paquetes de datos ASF para la secuencia de audio en el archivo de entrada. También recuperará la longitud del objeto de datos ASF en el archivo de entrada y el desplazamiento al primer paquete de datos ASF con respecto al inicio del archivo. El divisor usará estos atributos para generar ejemplos de secuencias de audio.

Para crear e inicializar los componentes ASF para el archivo de entrada:

1.  Llame a [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) para crear el objeto ContentInfo. Esta función devuelve un puntero a la interfaz [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) .
2.  Llame a [**IMFASFContentInfo::P arseheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) para analizar el encabezado ASF. Para obtener más información acerca de este paso, vea [leer el objeto de encabezado ASF de un archivo existente](reading-the-asf-header-object-of-an-existing-file.md).
3.  Llame a [**MFCreateASFSplitter**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfsplitter) para crear el objeto divisor de ASF. Esta función devuelve un puntero a la interfaz [**IMFASFSplitter**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfsplitter) .
4.  Llame a [**IMFASFSplitter:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-initialize), pasando el puntero [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo). Para obtener más información acerca de este paso, consulte [crear el objeto divisor de ASF](creating-the-asf-splitter-object.md).
5.  Llame a [**IMFASFContentInfo:: GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) para obtener un descriptor de presentación para el archivo ASF.
6.  Obtiene el valor del atributo [**de \_ \_ desplazamiento de \_ \_ Inicio de \_ datos ASF de MF PD**](mf-pd-asf-data-start-offset-attribute.md) del descriptor de presentación. Este valor es la ubicación del objeto de datos ASF en el archivo, como un desplazamiento de bytes desde el inicio del archivo.
7.  Obtiene el valor del atributo [**de \_ \_ longitud de \_ datos \_ ASF de MF PD**](mf-pd-asf-data-length-attribute.md) del descriptor de presentación. Este valor es el tamaño total del objeto de datos ASF, en bytes. Para obtener más información, vea [obtener información de los objetos de encabezado ASF](getting-information-from-asf-header-objects.md).

En el ejemplo de código siguiente se muestra una función que consolida todos los pasos. Esta función toma un puntero a la secuencia de bytes de origen y devuelve punteros al objeto ContentInfo de origen y al divisor. Además, recibe la longitud y los desplazamientos al objeto de datos ASF.


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



## <a name="5-create-an-audio-profile"></a>5. crear un perfil de audio

A continuación, creará un objeto de perfil para el archivo de entrada mediante su obtención del objeto ContentInfo de origen. Después, configurará el perfil para que contenga solo las secuencias de audio del archivo de entrada. Para ello, enumere las secuencias y quite las secuencias que no sean de audio del perfil. El objeto de Perfil de audio se usará más adelante en este tutorial para inicializar el objeto ContentInfo de salida.

Para crear un perfil de audio

1.  Obtiene el objeto de perfil para el archivo de entrada del objeto ContentInfo de origen llamando a [**IMFASFContentInfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile). El método devuelve un puntero a un objeto de perfil que contiene todas las secuencias del archivo de entrada. Para obtener más información, consulte [crear un perfil ASF](creating-an-asf-profile.md).
2.  Quite todos los objetos de exclusión mutua del perfil. Este paso es necesario porque los flujos que no son de audio se quitarán del perfil, lo que podría invalidar los objetos de exclusión mutua.
3.  Quite todas las secuencias que no sean de audio del perfil, como se indica a continuación:
    -   Llame a [**IMFASFProfile:: GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount) para obtener el número de secuencias.
    -   En un bucle, llame a [**IMFASFProfile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) para obtener cada flujo por índice.
    -   Llame a [**IMFASFStreamConfig:: GetStreamType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getstreamtype) para obtener el tipo de flujo.
    -   En el caso de las secuencias que no son de audio, llame a [**IMFASFProfile:: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) para quitar el flujo.
4.  Almacene el número de secuencia de la primera secuencia de audio. Se seleccionará en el divisor para generar ejemplos de secuencias. Si el número de secuencia es cero, el llamador puede suponer que no había ningún archivo de secuencias de audio.

En el siguiente código se indican estos pasos:


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



La `RemoveMutexes` función quita todos los objetos de exclusión mutua del perfil:


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



## <a name="6-initialize-objects-for-the-output-file"></a>6. inicializar los objetos para el archivo de salida

A continuación, creará el objeto ContentInfo de salida y el multiplexor para generar paquetes de datos para el archivo de salida.

El perfil de audio creado en el paso 4 se usará para rellenar el objeto ContentInfo de salida. Este objeto contiene información como atributos de archivo global y propiedades de secuencia. El objeto ContentInfo de salida se usará para inicializar el multiplexor que generará paquetes de datos para el archivo de salida. Una vez generados los paquetes de datos, el objeto ContentInfo debe actualizarse para reflejar los nuevos valores.

Para crear e inicializar componentes ASF para el archivo de salida

1.  Cree un objeto ContentInfo vacío llamando a [**MFCreateASFContentInfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) y rellénelo con información del perfil de audio creado en el paso 3 llamando a [**IMFASFContentInfo:: SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile). Para obtener más información, consulte [inicializar el objeto ContentInfo de un nuevo archivo ASF](initializing-the-contentinfo-object-of-a-new-asf-file.md).
2.  Cree e inicialice el objeto multiplexor usando el objeto ContentInfo de salida. Para obtener más información, vea [crear el objeto multiplexor](creating-the-multiplexer-object.md).

En el ejemplo de código siguiente se muestra una función que consolida los pasos. Esta función toma un puntero a un objeto de perfil y devuelve punteros al objeto ContentInfo de salida y al multiplexor.


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



## <a name="7-generate-new-asf-data-packets"></a>7. generar nuevos paquetes de datos ASF

A continuación, generará ejemplos de secuencias de audio a partir de la secuencia de bytes de origen mediante el divisor y los enviará al multiplexor para crear paquetes de datos ASF. Estos paquetes de datos constituirán el último objeto de datos ASF del nuevo archivo.

Para generar ejemplos de secuencias de audio

1.  Seleccione la primera secuencia de audio en el divisor llamando a [**IMFASFSplitter:: SelectStreams**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-selectstreams).
2.  Leer bloques de tamaño fijo de los datos multimedia de la secuencia de bytes de origen en un búfer multimedia.
3.  Recopile los ejemplos de secuencias como muestras de medios del divisor llamando a [**IMFASFSplitter:: GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) en un bucle siempre que reciba la \_ marca ASF STATUSFLAGS \_ incompleta en el parámetro *pdwStatusFlags* . Para obtener más información, vea generar ejemplos de paquetes de datos ASF en generación de ejemplos de [secuencias a partir de un objeto de datos ASF existente](generating-stream-samples-from-an-existing-asf-data-object.md).
4.  Para cada ejemplo de medio, llame a [**IMFASFMultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) para enviar el ejemplo multimedia al multiplexor. El multiplexor genera los paquetes de datos para el objeto de datos ASF.
5.  Escriba el paquete de datos generado por el multiplexor en la secuencia de bytes de datos.
6.  Una vez generados todos los paquetes de datos, llame a [**IMFASFMultiplexer:: end**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) para actualizar el objeto ContentInfo de salida con la información recopilada durante la generación de paquetes de datos ASF.

El siguiente código de ejemplo genera ejemplos de secuencias del divisor de ASF y los envía al multiplexor. El multiplexor genera paquetes de datos ASF y los escribe en una secuencia.


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



Para obtener paquetes del divisor de ASF, el código anterior llama a la `GetPacketsFromSplitter` función, que se muestra aquí:


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



La `GenerateDataPackets` función obtiene los paquetes de datos del multiplexor. Para obtener más información, vea [obtener paquetes de datos ASF](generating-new-asf-data-packets.md).


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



## <a name="8-write-the-asf-objects-in-the-new-file"></a>8. escribir los objetos ASF en el nuevo archivo

A continuación, escribirá el contenido del objeto ContentInfo de salida en un búfer multimedia mediante una llamada a [**IMFASFContentInfo:: GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader). Este método convierte los datos almacenados en el objeto ContentInfo en datos binarios en formato de objeto de encabezado ASF. Para obtener más información, vea [generar un nuevo objeto de encabezado ASF](generating-a-new-asf-header-object.md).

Una vez generado el nuevo objeto de encabezado ASF, escriba el archivo de salida escribiendo primero el objeto de encabezado en la secuencia de bytes de salida creada en el paso 2 mediante una llamada a la función auxiliar WriteBufferToByteStream. Siga el objeto de encabezado con el objeto de datos contenido en la secuencia de bytes de datos. En el código de ejemplo se muestra una función que transfiere el contenido de la secuencia de bytes de datos a la secuencia de bytes de salida.


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



## <a name="9-write-the-entry-point-function"></a>9 escribir la función Entry-Point

Ahora puede poner los pasos anteriores juntos en una aplicación completa. Antes de usar cualquiera de los objetos Media Foundation, inicialice la plataforma de Media Foundation mediante una llamada a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Cuando haya terminado, llame a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown). Para obtener más información, vea [inicializar Media Foundation](initializing-media-foundation.md).

En el código siguiente se muestra la aplicación de consola completa. El argumento de línea de comandos especifica el nombre del archivo que se va a convertir y el nombre del nuevo archivo de audio.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de WMContainer ASF](wmcontainer-asf-components.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



