---
description: En este tutorial se muestra cómo escribir un nuevo archivo de audio (.wma) extrayendo contenido multimedia de un archivo de audio sin comprimir (.wav) y comprima en formato ASF.
ms.assetid: f310c6ed-52e7-4828-9d4c-2f7ced9080c5
title: 'Tutorial: Escritura de un archivo WMA mediante objetos WMContainer'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aed89eb9ef656fe9240a1ed56e712f92209ba5c7e6d5bea2cca3d909d4315ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972774"
---
# <a name="tutorial-writing-a-wma-file-by-using-wmcontainer-objects"></a>Tutorial: Escritura de un archivo WMA mediante objetos WMContainer

En este tutorial se muestra cómo escribir un nuevo archivo de audio (.wma) extrayendo contenido multimedia de un archivo de audio sin comprimir (.wav) y comprima en formato ASF. El modo de codificación utilizado para la conversión es [Codificación de velocidad de bits constante](constant-bit-rate-encoding.md) (CBR). En este modo, antes de la sesión de codificación, la aplicación especifica una velocidad de bits de destino que el codificador debe lograr.

En este tutorial, creará una aplicación de consola que toma los nombres de archivo de entrada y salida como argumentos. La aplicación obtiene los ejemplos de medios sin comprimir de una aplicación de análisis de archivos de onda, que se proporciona con este tutorial. Estos ejemplos se envían al codificador para su conversión Windows formato De audio multimedia 9. El codificador está configurado para la codificación CBR y usa la primera velocidad de bits disponible durante la negociación del tipo de medio como velocidad de bits de destino. Los ejemplos codificados se envían al multiplexor para la aplicación de paquetes en formato de datos ASF. Estos paquetes se escribirán en una secuencia de bytes que representa el objeto de datos de ASF. Una vez que la sección de datos esté lista, creará un archivo de audio ASF y escribirá el nuevo objeto de encabezado ASF que consolida toda la información de encabezado y, a continuación, anexará el flujo de bytes del objeto de datos de ASF.

Este tutorial contiene las secciones siguientes:

-   [Requisitos previos](#prerequisites)
-   [Terminología](#terminology)
-   [1. Configure el Project](#1-set-up-the-project)
-   [2. Declarar funciones auxiliares](#2-declare-helper-functions)
-   [3. Abrir un archivo de audio](#3-open-an-audio-file)
-   [4. Configuración del codificador](#4-configure-the-encoder)
-   [5. Cree el objeto ContentInfo de ASF.](#5-create-the-asf-contentinfo-object)
-   [6. Creación del multiplexor de ASF](#6-create-the-asf-multiplexer)
-   [7. Generar nuevos paquetes de datos de ASF](#7-generate-new-asf-data-packets)
-   [8. Escribir el archivo ASF](#8-write-the-asf-file)
-   [9. Definición de la Entry-Point función](#9-define-the-entry-point-function)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Prerrequisitos

En este tutorial se da por hecho lo siguiente:

-   Está familiarizado con la estructura de un archivo ASF y los componentes proporcionados por Media Foundation para trabajar con objetos de ASF. Estos componentes incluyen ContentInfo, splitter, multiplexor y objetos de perfil. Para obtener más información, vea [WmContainer ASF Components](wmcontainer-asf-components.md).
-   Está familiarizado con los Windows multimedia y los distintos tipos de codificación, especialmente CBR. Para obtener más información, [vea Windows Media Encoders](windows-media-encoders.md) .
-   Está familiarizado con los búferes multimedia y las [secuencias](media-buffers.md) de bytes: en concreto, las operaciones de archivo mediante una secuencia de bytes y la escritura del contenido de un búfer multimedia en una secuencia de bytes.

## <a name="terminology"></a>Terminología

En este tutorial se usan los términos siguientes:

-   Tipo de medio de origen: objeto de tipo de medio, expone la interfaz [**IMFMediaType,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que describe el contenido del archivo de entrada.
-   Perfil de audio: objeto de perfil, expone la interfaz [**RECORDSETASFProfile,**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) que solo contiene secuencias de audio del archivo de salida.
-   Ejemplo de secuencia: muestra multimedia, expone la interfaz [**DE PRUEBASEJEMPLO,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) representa los datos multimedia del archivo de entrada obtenidos del codificador en un estado comprimido.
-   Objeto ContentInfo: [objeto ContentInfo](asf-contentinfo-object.md)de ASF , expone la interfaz [**DEFFContentInfo,**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) que representa el objeto de encabezado ASF del archivo de salida.
-   Flujo de bytes de datos: objeto de secuencia de bytes, expone la interfaz [**BYTEByteStream,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) que representa toda la parte del objeto de datos ASF del archivo de salida.
-   Paquete de datos: ejemplo de medios, expone [**la interfaz DESAMPLESAMPLE,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) generada por el [multiplexor de ASF](asf-multiplexer.md); representa un paquete de datos de ASF que se escribirá en el flujo de bytes de datos.
-   Secuencia de bytes de salida: objeto de secuencia de bytes, expone la interfaz [**BYTEByteStream,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream) que contiene el contenido del archivo de salida.

## <a name="1-set-up-the-project"></a>1. Configure el Project

1.  Incluya los siguientes encabezados en el archivo de código fuente:

    ```C++
    #include <new>
    #include <stdio.h>       // Standard I/O
    #include <windows.h>     // Windows headers
    #include <mfapi.h>       // Media Foundation platform
    #include <wmcontainer.h> // ASF interfaces
    #include <mferror.h>     // Media Foundation error codes
    ```

    

2.  Vínculo a los siguientes archivos de biblioteca:

    -   mfplat.lib
    -   mf.lib
    -   mfuuid.lib

3.  Declare la [función SafeRelease.](saferelease.md)
4.  Incluya la clase CWmaEncoder en el proyecto. Para obtener el código fuente completo de esta clase, vea [Código de ejemplo de codificador](encoder-example-code.md).

## <a name="2-declare-helper-functions"></a>2. Declarar funciones auxiliares

En este tutorial se usan las siguientes funciones auxiliares para leer y escribir desde una secuencia de bytes.

-   `AppendToByteStream`: anexa el contenido de una secuencia de bytes a otra secuencia de bytes.
-   WriteBufferToByteStream: escribe datos de un búfer multimedia en una secuencia de bytes.

Para obtener más información, [**vea IMFByteStream::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write). El código siguiente muestra estas funciones auxiliares:


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



## <a name="3-open-an-audio-file"></a>3. Abrir un archivo de audio

En este tutorial se da por supuesto que la aplicación generará audio sin comprimir para la codificación. Para ello, en este tutorial se declaran dos funciones:


```C++
HRESULT OpenAudioFile(PCWSTR pszURL, IMFMediaType **ppAudioFormat);
HRESULT GetNextAudioSample(BOOL *pbEOS, IMFSample **ppSample);
```



La implementación de estas funciones se deja al lector.

-   La función debe abrir el archivo multimedia especificado por pszURL y devolver un puntero a un tipo de medio que `OpenAudioFile` describa una secuencia de audio. 
-   La `GetNextAudioSample` función debe leer el audio PCM sin comprimir del archivo abierto por `OpenAudioFile` . Cuando se alcanza el final del archivo, *pbEOS* recibe el valor **TRUE**. De lo contrario, *ppSample* recibe un ejemplo multimedia que contiene el búfer de audio.

## <a name="4-configure-the-encoder"></a>4. Configuración del codificador

A continuación, cree el codificador, configúrelo para generar ejemplos de secuencias codificadas con CBR y negocie los tipos de medios de entrada y salida.

En Media Foundation, los codificadores (exponen la interfaz [**DETRANSFORMTRANSFORM)**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) se implementan [como Media Foundation transforms](media-foundation-transforms.md) (MFT).

En este tutorial, el codificador se implementa en la `CWmaEncoder` clase que proporciona un contenedor para MFT. Para obtener el código fuente completo de esta clase, vea [Código de ejemplo de codificador](encoder-example-code.md).

> [!Note]  
> Opcionalmente, puede especificar el tipo de codificación como CBR. De forma predeterminada, el codificador está configurado para usar la codificación CBR. Para obtener más información, vea [Codificación de velocidad de bits constante.](constant-bit-rate-encoding.md) Puede establecer propiedades adicionales en función del tipo de codificación, para obtener información sobre las propiedades específicas de un modo de codificación, vea Codificación de velocidad de bits [variable](quality-based-variable-bit-rate--vbr--encoding.md)basada en calidad, Codificación de velocidad de bits variable sin [restricciones](unconstrained-variable-bit-rate--vbr--encoding.md)y Codificación de velocidad de bits [variable](peak-constrained-variable-bit-rate--vbr--encoding.md)limitada por pico.

 


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



## <a name="5-create-the-asf-contentinfo-object"></a>5. Cree el objeto ContentInfo de ASF.

El [objeto ContentInfo de ASF](asf-contentinfo-object.md) contiene información sobre los distintos objetos de encabezado del archivo de salida.

En primer lugar, cree un perfil de ASF para la secuencia de audio:

1.  Llame [**a MFCreateASFProfile para**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) crear un objeto de perfil de ASF vacío. El perfil de ASF expone la [**interfaz IMFASFProfile.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) Para obtener más información, [vea Creating and Configuring ASF Secuencias](creating-and-configuring-asf-streams.md).
2.  Obtenga el formato de audio codificado del `CWmaEncoder` objeto .
3.  Llame [**a IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) para crear una nueva secuencia para el perfil de ASF. Pase un puntero a la interfaz [**IMFMediaType,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) que representa el formato de secuencia.
4.  Llame [**a IMFASFStreamConfig::SetStreamNumber para**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) asignar un identificador de secuencia.
5.  Establezca los parámetros "leaky bucket" estableciendo el atributo [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) en el objeto de secuencia.
6.  Llame [**a IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) para agregar la nueva secuencia al perfil.

Ahora cree el objeto ContentInfo de ASF como se muestra a continuación:

1.  Llame [**a MFCreateASFContentInfo para**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) crear un objeto ContentInfo vacío.
2.  Llame [**a IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile) para establecer el perfil de ASF.

El siguiente código muestra estos pasos:


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



## <a name="6-create-the-asf-multiplexer"></a>6. Creación del multiplexor de ASF

El [multiplexor de ASF](asf-multiplexer.md) genera paquetes de datos de ASF.

1.  Llame [**a MFCreateASFMultiplexer para**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmultiplexer) crear el multiplexor de ASF.
2.  Llame [**a IMFASFMultiplexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-initialize) para inicializar el multiplexor. Pase un puntero al objeto De información de contenido de ASF, que se creó en la sección anterior.
3.  Llame [**a IMFASFMultiplexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-setflags) para establecer la marca **MFASF \_ MULTIPLEXER \_ AUTOADJUST \_ BITRATE.** Cuando se usa esta configuración, el multiplexor ajusta automáticamente la velocidad de bits del contenido de ASF para que coincida con las características de las secuencias que se multiplexa.


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



## <a name="7-generate-new-asf-data-packets"></a>7. Generar nuevos paquetes de datos de ASF

A continuación, genere paquetes de datos de ASF para el nuevo archivo. Estos paquetes de datos constituyen el objeto de datos de ASF final para el nuevo archivo. Para generar nuevos paquetes de datos de ASF:

1.  Llame [**a MFCreateTempFile para**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatetempfile) crear una secuencia de bytes temporal para contener los paquetes de datos de ASF.
2.  Llame a la función definida por la aplicación para obtener datos de audio sin `GetNextAudioSample` comprimir para el codificador.
3.  Pase el audio sin comprimir al codificador para la compresión. Para más información, consulte [Procesamiento de datos en el codificador.](processing-data-in-the-encoder.md)
4.  Llame [**a IMFASFMultiplexer::P rocessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) para enviar las muestras de audio comprimido al multiplexor de ASF para la aplicación de paquetes.
5.  Obtenga los paquetes ASF del multiplexor y escríbalos en la secuencia de bytes temporal. Para obtener más información, vea [Generar nuevos paquetes de datos de ASF.](generating-new-asf-data-packets.md)
6.  Cuando llegue al final de la secuencia de origen, escurra el codificador y extrae las muestras comprimidas restantes del codificador. Para obtener más información sobre cómo purgar un MFT, vea [Basic MFT Processing Model](basic-mft-processing-model.md).
7.  Una vez que se envíen todas las muestras al multiplexor, llame a [**MULTICASTASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) y extraiga los paquetes ASF restantes del multiplexor.
8.  Llame [**a IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end).

El código siguiente genera paquetes de datos de ASF. La función devuelve un puntero a una secuencia de bytes que contiene el objeto de datos ASF.


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



El código de `GenerateASFDataPackets` la función se muestra en el tema [Generating New ASF Data Packets](generating-new-asf-data-packets.md).

## <a name="8-write-the-asf-file"></a>8. Escribir el archivo ASF

A continuación, escriba el encabezado ASF en un búfer multimedia mediante una llamada a [**IMFASFContentInfo::GenerateHeader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generateheader). Este método convierte los datos almacenados en el objeto ContentInfo en datos binarios en formato de objeto de encabezado ASF. Para obtener más información, vea [Generar un nuevo objeto de encabezado ASF](generating-a-new-asf-header-object.md).

Una vez generado el nuevo objeto de encabezado ASF, cree una secuencia de bytes para el archivo de salida. En primer lugar, escriba el objeto de encabezado en el flujo de bytes de salida. Siga el objeto de encabezado con el objeto de datos incluido en la secuencia de bytes de datos.


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



## <a name="9-define-the-entry-point-function"></a>9. Definición de la Entry-Point función

Ahora puede colocar los pasos anteriores en una aplicación completa. Antes de usar cualquiera de los Media Foundation, inicialice la plataforma Media Foundation mediante una llamada [**a MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Cuando haya terminado, llame a [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown). Para obtener más información, vea [Inicializar Media Foundation](initializing-media-foundation.md).

El código siguiente muestra la aplicación de consola completa. El argumento de línea de comandos especifica el nombre del archivo que se convertirá y el nombre del nuevo archivo de audio.


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



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de ASF de WMContainer](wmcontainer-asf-components.md)
</dt> <dt>

[Compatibilidad con ASF en Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



