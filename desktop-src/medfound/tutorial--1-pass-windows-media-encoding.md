---
description: La codificación hace referencia al proceso de conversión de medios digitales de un formato a otro. Por ejemplo, convertir el audio MP3 Windows formato de audio multimedia tal como se define en la especificación del formato de sistemas avanzados (ASF).
ms.assetid: 4fe202d8-c8f5-4e9a-ad40-1aea8f767362
title: 'Tutorial: Codificación multimedia de Windows paso 1'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d670b107f315966a048a2f847183431f9a57bd4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268663"
---
# <a name="tutorial-1-pass-windows-media-encoding"></a>Tutorial: Codificación multimedia de Windows paso 1

La codificación hace referencia al proceso de conversión de medios digitales de un formato a otro. Por ejemplo, convertir el audio MP3 Windows formato de audio multimedia tal como se define en la especificación del formato de sistemas avanzados (ASF).

**Nota**  La especificación ASF define un tipo de contenedor para el archivo de salida (.wma o .wmv) que puede contener datos multimedia en cualquier formato, comprimidos o sin comprimir. Por ejemplo, un contenedor de ASF como un archivo .wma puede contener datos multimedia en formato MP3. El proceso de codificación convierte el formato real de los datos contenidos en el archivo.

En este tutorial se muestra cómo codificar el origen de entrada de contenido claro (no protegido por DRM) en el contenido multimedia de Windows y escribir los datos en un nuevo archivo ASF (.wm) mediante los componentes de ASF de la capa de \* canalización. Estos componentes se usarán para crear una topología de codificación parcial, que se controlará mediante una instancia de la sesión multimedia.

En este tutorial, creará una aplicación de consola que toma los nombres de archivo de entrada y salida, y el modo de codificación como argumentos. El archivo de entrada puede estar en un formato de medio comprimido o sin comprimir. Los modos de codificación válidos son "CBR" (velocidad de bits constante) o "VBR" (velocidad de bits variable). La aplicación crea un origen multimedia para representar el origen especificado por el nombre de archivo de entrada y el receptor del archivo ASF para archivar el contenido codificado del archivo de origen en un archivo ASF. Para que el escenario sea sencillo de implementar, el archivo de salida solo tendrá una secuencia de audio y una secuencia de vídeo. La aplicación inserta el códec Professional Media Audio 9.1 de Windows para la conversión de formato de secuencia de audio y el códec Windows Media Video 9 para la secuencia de vídeo.

Para la codificación de velocidad de bits constante, antes de que comience la sesión de codificación, el codificador debe conocer la velocidad de bits de destino que debe lograr. En este tutorial, para el modo "CBR", la aplicación usa la velocidad de bits disponible con el primer tipo de medio de salida que se recupera del codificador durante la negociación del tipo de medio como velocidad de bits de destino. Para la codificación de velocidad de bits variable, en este tutorial se muestra la codificación con velocidad de bits variable estableciendo un nivel de calidad. Las secuencias de audio se codifican en el nivel de calidad de 98 y las secuencias de vídeo en el nivel de calidad de 95.

En el procedimiento siguiente se resumen los pasos para codificar Windows contenido multimedia en un contenedor de ASF mediante un modo de codificación de 1 paso.

1.  Cree un origen de medios para el especificado mediante el solucionador de origen.
2.  Enumerar las secuencias en el origen de medios.
3.  Cree el receptor de medios de ASF y agregue receptores de flujo en función de las secuencias del origen de medios que deba codificarse.
4.  Configure el receptor de medios con las propiedades de codificación necesarias.
5.  Cree el Windows codificadores multimedia para las secuencias del archivo de salida.
6.  Configure los codificadores con las propiedades que se establecen en el receptor de medios.
7.  Cree una topología de codificación parcial.
8.  Cree una instancia de la sesión multimedia y establezca la topología en la sesión multimedia.
9.  Inicie la sesión de codificación controlando la sesión multimedia y obteniendo todos los eventos pertinentes de la sesión multimedia.
10. Para la codificación de VBR, obtenga los valores de propiedad de codificación del codificador y esta establezca en el receptor de medios.
11. Cierre y cierre la sesión de codificación.

Este tutorial contiene las secciones siguientes:

-   [Requisitos previos](#prerequisites)
-   [Configurar el Project](#set-up-the-project)
-   [Creación del origen multimedia](#create-the-media-source)
-   [Creación del receptor de archivos ASF](#create-the-asf-file-sink)
    -   [Creación del objeto de perfil de ASF](#create-the-asf-profile-object)
    -   [Crear un tipo de medio de audio comprimido](#create-a-compressed-audio-media-type)
    -   [Crear un tipo de medio de vídeo comprimido](#create-a-compressed-video-media-type)
    -   [Creación del objeto ContentInfo de ASF](#create-the-asf-contentinfo-object)
    -   [Creación del receptor de archivos ASF](#create-the-asf-file-sink)
-   [Compilación de la topología de codificación parcial](#build-the-partial-encoding-topology)
    -   [Creación del nodo de topología de origen para el origen multimedia](#create-the-source-topology-node-for-the-media-source)
    -   [Crear instancias de los codificadores necesarios y crear los nodos de transformación](#instantiate-the-required-encoders-and-create-the-transform-nodes)
    -   [Creación de los nodos de topología de salida para el receptor de archivos](#create-the-output-topology-nodes-for-the-file-sink)
    -   [Conectar nodos de origen, transformación y receptor](#connect-the-source-transform-and-sink-nodes)
-   [Control de la sesión de codificación](#handling-the-encoding-session)
-   [Actualizar las propiedades de codificación en el receptor de archivos](#update-encoding-properties-in-the-file-sink)
-   [Implementar Main](#implement-main)
-   [Probar el archivo de salida](#test-the-output-file)
-   [Códigos de error comunes y depuración Sugerencias](#common-error-codes-and-debugging-tips)
-   [Temas relacionados](#related-topics)

## <a name="prerequisites"></a>Prerrequisitos

En este tutorial se da por hecho lo siguiente:

-   Está familiarizado con la estructura de [archivos asf](asf-file-structure.md), los componentes de [ASF](pipeline-layer-asf-components.md) de la capa de canalización proporcionados por Media Foundation para trabajar con objetos de ASF. Estos componentes incluyen los siguientes objetos:
    -   [Orígenes multimedia](media-sources.md)

        **Nota**  Si va a realizar la transratación (convertir un archivo de velocidad de bits mayor en un archivo de velocidad de bits inferior sin cambiar los formatos), usará el origen [multimedia de ASF](asf-media-source.md).

    -   [Windows Codificadores multimedia](windows-media-encoders.md)
    -   [Receptores multimedia de ASF](asf-media-sinks.md)
    -   [Objeto ContentInfo de ASF](asf-contentinfo-object.md)
    -   [Perfil de ASF](asf-profile.md)

-   Está familiarizado con los Windows multimedia y los distintos tipos [](constant-bit-rate-encoding.md) de codificación, especialmente la codificación de velocidad de bits constante y la codificación de velocidad de bits variable basada en [calidad.](quality-based-variable-bit-rate--vbr--encoding.md)
-   Está familiarizado con las operaciones MFT del codificador. En concreto, crear una instancia del codificador y establecer los tipos de entrada y salida en el codificador.
-   Está familiarizado con los objetos de topología y cómo crear una topología de codificación. Para obtener más información sobre topologías y nodos de topología, vea [Crear topologías](creating-topologies.md).
-   Está familiarizado con el [modelo de eventos](media-session.md)de Media Session y las operaciones de control de flujo. Para obtener información, vea [Eventos de sesión multimedia](media-session-events.md).

## <a name="set-up-the-project"></a>Configurar el Project

1.  Incluya los siguientes encabezados en el archivo de código fuente:

    ```C++
    #include <new>
    #include <mfidl.h>            // Media Foundation interfaces
    #include <mfapi.h>            // Media Foundation platform APIs
    #include <mferror.h>        // Media Foundation error codes
    #include <wmcontainer.h>    // ASF-specific components
    #include <wmcodecdsp.h>        // Windows Media DSP interfaces
    #include <Dmo.h>            // DMO objects
    #include <uuids.h>            // Definition for FORMAT_VideoInfo
    #include <propvarutil.h>
    
    ```

    

2.  Vínculo a los siguientes archivos de biblioteca:

    ```C++
    // The required link libraries 
    #pragma comment(lib, "mfplat")
    #pragma comment(lib, "mf")
    #pragma comment(lib, "mfuuid")
    #pragma comment(lib, "msdmo")
    #pragma comment(lib, "strmiids")
    #pragma comment(lib, "propsys")
    
    ```

    

3.  Declare la [función SafeRelease.](saferelease.md)

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

    

4.  Declare la enumeración ENCODING \_ MODE para definir los tipos de codificación CBR y VBR.

    ```C++
    // Encoding mode
    typedef enum ENCODING_MODE {
      NONE  = 0x00000000,
      CBR   = 0x00000001,
      VBR   = 0x00000002,
    } ;
    
    ```

    

5.  Defina una constante para la ventana de búfer para una secuencia de vídeo.

    ```C++
    // Video buffer window
    const INT32 VIDEO_WINDOW_MSEC = 3000;
    
    ```

    

## <a name="create-the-media-source"></a>Creación del origen multimedia

Cree un origen multimedia para el origen de entrada. Media Foundation proporciona orígenes de medios integrados para varios formatos multimedia: MP3, MP4/3GP, AVI/WAVE. Para obtener información sobre los formatos admitidos por Media Foundation, vea [Supported Media Formats in Media Foundation](supported-media-formats-in-media-foundation.md).

Para crear el origen de medios, use el [solucionador de origen](source-resolver.md). Este objeto analiza la dirección URL especificada para el archivo de origen y crea el origen multimedia adecuado.

Realice las siguientes llamadas:

-   [**MFCreateSourceResolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)
-   [**IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)

    Para obtener más información sobre estas llamadas, vea [Usar el solucionador de origen](using-the-source-resolver.md).

    Si el archivo de entrada está en formato ASF y desea convertirlo en un archivo de velocidad de bits diferente sin cambiar los formatos, el solucionador de origen crea una instancia del origen multimedia [de ASF](asf-media-source.md).

En el ejemplo de código siguiente se muestra una función CreateMediaSource que crea un origen multimedia para el archivo especificado.


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="create-the-asf-file-sink"></a>Creación del receptor de archivos ASF

Cree una instancia del receptor de archivos ASF que archivará los datos multimedia codificados en un archivo ASF al final de la sesión de codificación.

En este tutorial, creará un objeto de activación para el receptor de archivos ASF. El receptor de archivos necesita la siguiente información para crear los receptores de flujo necesarios.

-   Secuencias que se codificarán y escribirán en el archivo final.
-   Las propiedades de codificación que se usan para codificar el contenido multimedia, como el tipo de codificación, el número de pases de codificación y las propiedades relacionadas.
-   Propiedades de archivo global que indican al receptor de medios si debe ajustar automáticamente los parámetros del cubo de fugas (velocidad de bits y tamaño de búfer).

La información de secuencia se configura en el objeto ASF Profile y las propiedades de codificación y global se establecen en un almacén de propiedades administrado por el objeto ContentInfo de ASF.

Para obtener información general sobre el receptor de archivos ASF, vea [Receptores multimedia de ASF.](asf-media-sinks.md)

### <a name="create-the-asf-profile-object"></a>Creación del objeto de perfil de ASF

Para que el receptor de archivos ASF escriba datos multimedia codificados en un archivo ASF, el receptor debe conocer el número de secuencias y el tipo de secuencias para las que crear receptores de flujo. En este tutorial extraerá esa información del origen de medios y creará los flujos de salida correspondientes. Restrinja los flujos de salida a una secuencia de audio y una secuencia de vídeo. Para cada secuencia seleccionada en el origen, cree una secuencia de destino y agrégréla al perfil.

Para implementar este paso, necesita los siguientes objetos.

-   [Perfil de ASF](asf-profile.md)
-   Descriptor de presentación para el origen multimedia
-   Descriptores de secuencia para las secuencias seleccionadas en el origen de medios.
-   Tipos de medios para las secuencias seleccionadas.

En los pasos siguientes se describe el proceso de creación del perfil de ASF y las secuencias de destino.

**Para crear el perfil de ASF**

1.  Llame [**a MFCreateASFProfile para**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) crear un objeto de perfil vacío.
2.  Llame [**a IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) para crear el descriptor de presentación para el origen multimedia creado en el paso descrito en la sección "Crear el origen multimedia" de este tutorial.
3.  Llame [**a IMFPresentationDescriptor::GetStreamDescriptorCount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) para obtener el número de secuencias en el origen multimedia.
4.  Llame [**a IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para cada secuencia del origen multimedia y obtenga el descriptor de secuencia de la secuencia.
5.  Llame [**a IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) seguido de [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) y obtenga el primer tipo de medio para la secuencia.

    **Nota**   Para evitar llamadas complejas, suponga que solo existe un tipo de medio por secuencia y seleccione el primer tipo de medio de la secuencia. En el caso de las secuencias complejas, debe enumerar cada tipo de medio del controlador de tipo de medio y elegir el tipo de medio que desea codificar.

6.  Llame a I [**IMFMediaType::GetMajorType para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) obtener el tipo principal de la secuencia para determinar si la secuencia contiene audio o vídeo.
7.  En función del tipo principal de la secuencia, cree tipos de medios de destino. Estos tipos de medios contendrán información de formato que el codificador usará durante la sesión de codificación. En las secciones siguientes de este tutorial se describe el proceso de creación de los tipos de medios de destino.
    -   Crear un tipo de medio de audio comprimido
    -   Crear un tipo de medio de vídeo comprimido
8.  Cree una secuencia basada en el tipo de medio de destino, configúrela según los requisitos de la aplicación y agregue la secuencia al perfil. Para obtener más información, vea [Adding Stream Information to the ASF File Sink](adding-stream-information-to-the-asf-file-sink.md).

    1.  Llame [**a IMFASFProfile::CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) y pase el tipo de medio de destino para crear el flujo de salida. El método recupera la interfaz IMFASFStreamConfig del objeto de secuencia.
    2.  Configure la secuencia.
        -   Llame [**a IMFASFStreamConfig::SetStreamNumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) para asignar un número a la secuencia. Esta configuración es obligatoria.
        -   Opcionalmente, configure los parámetros del cubo de pérdidas, la extensión de carga, la exclusión mutua en cada secuencia mediante una llamada a los métodos [**DEFISFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) y los atributos de configuración de flujo pertinentes.
    3.  Agregue las propiedades de codificación de nivel de flujo mediante el objeto ContentInfo de ASF. Para obtener más información sobre este paso, vea la sección "Creación del objeto ContentInfo de ASF" en este tutorial.
    4.  Llame [**a IMFASFProfile::SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) para agregar la secuencia al perfil.

    En el ejemplo de código siguiente se crea una secuencia de audio de salida.

    ```C++
    //-------------------------------------------------------------------
    //  CreateAudioStream
    //  Create an audio stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //-------------------------------------------------------------------

    HRESULT CreateAudioStream(IMFASFProfile* pProfile, WORD wStreamNumber)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        IMFMediaType* pAudioType = NULL;
        IMFASFStreamConfig* pAudioStream = NULL;
        
        //Create an output type from the encoder
        HRESULT hr = GetOutputTypeFromWMAEncoder(&pAudioType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Create a new stream with the audio type
        hr = pProfile->CreateStream(pAudioType, &pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set stream number
        hr = pAudioStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Add the stream to the profile
        hr = pProfile->SetStream(pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Audio Stream created. Stream Number: %d.\n", wStreamNumber);

    done:
        SafeRelease(&pAudioStream);
        SafeRelease(&pAudioType);
        return hr;
    }
    ```

    

    En el ejemplo de código siguiente se crea una secuencia de vídeo de salida.

    ```C++
    //-------------------------------------------------------------------
    //  CreateVideoStream
    //  Create an video stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //    pType: A pointer to the source's video media type.
    //-------------------------------------------------------------------

    HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        HRESULT hr = S_OK;

        
        IMFMediaType* pVideoType = NULL;
        IMFASFStreamConfig* pVideoStream = NULL;

        UINT32 dwBitRate = 0;
            
        //Create a new video type from the source type
        hr = CreateCompressedVideoType(pType, &pVideoType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Create a new stream with the video type
        hr = pProfile->CreateStream(pVideoType, &pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }
        

        //Set a valid stream number
        hr = pVideoStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }

        //Add the stream to the profile
        hr = pProfile->SetStream(pVideoStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

    done:

        SafeRelease(&pVideoStream);
        SafeRelease(&pVideoType);

        return hr;
    }
    ```

    

En el ejemplo de código siguiente se crean secuencias de salida en función de las secuencias del origen.


```C++
    //For each stream in the source, add target stream information in the profile
    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        //Get the media type handler
        hr = pStreamDesc->GetMediaTypeHandler(&pHandler);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the first media type 
        hr = pHandler->GetMediaTypeByIndex(0, &pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the major type
        hr = pMediaType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        // If this is a video stream, create the target video stream
        if (guidMajor == MFMediaType_Video)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateVideoStream(pProfile, wStreamID, pMediaType);

            if (FAILED(hr))
            {
                goto done;
            }
        }
        
        // If this is an audio stream, create the target audio stream
        if (guidMajor == MFMediaType_Audio)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateAudioStream(pProfile, wStreamID);

            if (FAILED(hr))
            {
                goto done;
            }
        }

        //Get stream's encoding property
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set the stream-level encoding properties
        hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
        if (FAILED(hr))
        {
            goto done;
        }


        SafeRelease(&pMediaType);
        SafeRelease(&pStreamDesc);
        SafeRelease(&pContentInfoProps);
        wStreamID++;
    }
```



### <a name="create-a-compressed-audio-media-type"></a>Crear un tipo de medio de audio comprimido

Si desea incluir una secuencia de audio en el archivo de salida, cree un tipo de audio especificando las características del tipo codificado estableciendo los atributos necesarios. Para asegurarse de que el tipo de audio es compatible con el codificador de audio multimedia de Windows, cree una instancia del codificador MFT, establezca las propiedades de codificación y obtenga un tipo de medio mediante una llamada a [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Para obtener el tipo de salida necesario, recorre en bucle todos los tipos disponibles, obtiene los atributos de cada tipo de medio y selecciona el tipo más cercano a sus requisitos. En este tutorial, obtenga el primer tipo disponible de la lista de tipos de medios de salida admitidos por el codificador.

**Nota**  Para Windows 7, Media Foundation proporciona una nueva función, [**MFTranscodeGetAudioOutputAvailableTypes,**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) que recupera una lista de los tipos de audio compatibles. Esta función solo obtiene los tipos de medios para la codificación CBR.

Un tipo de audio completo debe tener los siguientes atributos establecidos:

-   [**TIPO \_ PRINCIPAL DE MT \_ DE \_ MF**](mf-mt-major-type-attribute.md)
-   [**\_SUBTIPO DE MT DE MF \_**](mf-mt-subtype-attribute.md)
-   [**CANALES \_ NUM DE AUDIO MF \_ \_ \_ MT**](mf-mt-audio-num-channels-attribute.md)
-   [**MUESTRAS \_ DE AUDIO MF MT POR \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-samples-per-second-attribute.md)
-   [**ALINEACIÓN \_ DE \_ BLOQUES DE AUDIO MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)
-   [**PROMEDIO DE BYTES PROMEDIO DE AUDIO DE MF \_ MT \_ POR \_ \_ \_ \_ SEGUNDO**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**BITS \_ DE AUDIO MF MT POR \_ \_ \_ \_ MUESTRA**](mf-mt-audio-bits-per-sample-attribute.md)

En el ejemplo de código siguiente se crea un tipo de audio comprimido obteniendo un tipo compatible del codificador Windows Media Audio. La implementación de SetEncodingProperties se muestra en la sección "Crear el objeto ContentInfo de ASF" de este tutorial.


```C++
//-------------------------------------------------------------------
//  GetOutputTypeFromWMAEncoder
//  Gets a compatible output type from the Windows Media audio encoder.
//
//  ppAudioType: Receives a pointer to the media type.
//-------------------------------------------------------------------

HRESULT GetOutputTypeFromWMAEncoder(IMFMediaType** ppAudioType)
{
    if (!ppAudioType)
    {
        return E_POINTER;
    }

    IMFTransform* pMFT = NULL;
    IMFMediaType* pType = NULL;
    IPropertyStore* pProps = NULL;

    //We need to find a suitable output media type
    //We need to create the encoder to get the available output types
    //and discard the instance.

    CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cCLSID = 0;            // Size of the array.

    MFT_REGISTER_TYPE_INFO tinfo;
    
    tinfo.guidMajorType = MFMediaType_Audio;
    tinfo.guidSubtype = MFAudioFormat_WMAudioV9;

    // Look for an encoder.
    HRESULT hr = MFTEnum(
        MFT_CATEGORY_AUDIO_ENCODER,
        0,                  // Reserved
        NULL,                // Input type to match. None.
        &tinfo,             // WMV encoded type.
        NULL,               // Attributes to match. (None.)
        &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
        &cCLSID             // Receives the size of the array.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // MFTEnum can return zero matches.
    if (cCLSID == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
        goto done;
    }
    else
    {
        // Create the MFT decoder
        hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));

        if (FAILED(hr))
        {
            goto done;
        }

    }

    // Get the encoder's property store

    hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Set encoding properties
    hr = SetEncodingProperties(MFMediaType_Audio, pProps);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get the first output type
    //You can loop through the available output types to choose 
    //the one that meets your target requirements
    hr = pMFT->GetOutputAvailableType(0, 0, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return to the caller
    *ppAudioType = pType;
    (*ppAudioType)->AddRef();
    
done:
    SafeRelease(&pProps);
    SafeRelease(&pType);
    SafeRelease(&pMFT);
    CoTaskMemFree(pMFTCLSIDs);
    return hr;
}
```



### <a name="create-a-compressed-video-media-type"></a>Crear un tipo de medio de vídeo comprimido

Si desea incluir una secuencia de vídeo en el archivo de salida, cree un tipo de vídeo codificado por completo. El tipo de medio completo debe incluir la velocidad de bits deseada y los datos privados de códec.

Hay dos maneras de crear un tipo de medio de vídeo completo.

-   Cree un tipo de medio vacío y copie los atributos del tipo de medio del tipo de vídeo de origen y sobrescriba el atributo [**\_ MF MT \_ SUBTYPE**](mf-mt-subtype-attribute.md) con la constante GUID MFVideoFormat \_ WMV3.

    Un tipo de vídeo completo debe tener los siguientes atributos establecidos:

    -   TIPO \_ PRINCIPAL DE MT \_ DE \_ MF
    -   \_SUBTIPO DE MT DE MF \_
    -   MF \_ MT \_ FRAME \_ RATE
    -   TAMAÑO \_ DEL MARCO DE MT \_ \_ DE MF
    -   MODO \_ DE \_ INTERLACE MF \_ MT
    -   RELACIÓN DE \_ ASPECTO \_ DE PÍXELES DE MT \_ DE \_ MF
    -   MF \_ MT \_ AVG \_ BITRATE
    -   DATOS \_ DE USUARIO DE MF MT \_ \_

    En el ejemplo de código siguiente se crea un tipo de vídeo comprimido a partir del tipo de vídeo del origen.

    ```C++
    //-------------------------------------------------------------------
    //  CreateCompressedVideoType
    //  Creates an output type from source's video media type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateCompressedVideoType(
            IMFMediaType* pType, 
            IMFMediaType** ppVideoType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppVideoType)
        {
            return E_POINTER;
        }
        
        HRESULT hr = S_OK;
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 fSamplesIndependent = 0;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->CopyAllItems(pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Fill the missing attributes
        //1. Frame rate
        hr = MFGetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

            hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////2. Frame size
        hr = MFGetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;
                
            hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////3. Interlace mode
        
        if (FAILED(pMediaType->GetUINT32(MF_MT_INTERLACE_MODE, &interlace)))
        {
            hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        ////4. Pixel aspect Ratio
        hr = MFGetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            par.Numerator = par.Denominator = 1;
            hr = MFSetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32)par.Numerator, (UINT32)par.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        //6. bit rate
        if (FAILED(pMediaType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate)))
        {
            hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, 1000000);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_WMV3);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppVideoType = pMediaType;
        (*ppVideoType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    
    ```

    

-   Obtenga un tipo de medio compatible del codificador de vídeo Windows Media estableciendo las propiedades de codificación y, a continuación, llamando a [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Este método devuelve el tipo parcial. Asegúrese de convertir el tipo parcial en un tipo completo agregando la siguiente información:

    -   Establezca la velocidad de bits de vídeo en el atributo [**\_ AVG \_ \_ BITRATE de MF MT.**](mf-mt-avg-bitrate-attribute.md)
    -   Agregue datos privados de códec estableciendo el atributo [**MF \_ MT USER \_ \_ DATA.**](mf-mt-user-data-attribute.md) Para obtener instrucciones detalladas, vea "Datos de códecs privados" en [Configuración de un codificador WMV.](configuring-a-wmv-encoder.md)

    Dado [**que IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) comprueba la velocidad de bits antes de devolver los datos privados del códec, asegúrese de establecer la velocidad de bits antes de obtener los datos privados del códec.

    En el ejemplo de código siguiente se crea un tipo de vídeo comprimido obteniendo un tipo compatible del codificador Windows Media Video. También crea un tipo de vídeo sin comprimir y lo establece como entrada del codificador. Esto se implementa en la función auxiliar CreateUncompressedVideoType. GetOutputTypeFromWMVEncoder convierte el tipo parcial devuelto en un tipo completo agregando datos privados de códec. La implementación de SetEncodingProperties se muestra en la sección "Crear el objeto ContentInfo de ASF" de este tutorial.

    ```C++
    //-------------------------------------------------------------------
    //  GetOutputTypeFromWMVEncoder
    //  Gets a compatible output type from the Windows Media video encoder.
    //
    //  pType: A pointer to the source video stream's media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT GetOutputTypeFromWMVEncoder(IMFMediaType* pType, IMFMediaType** ppVideoType)
    {
        if (!ppVideoType)
        {
            return E_POINTER;
        }

        IMFTransform* pMFT = NULL;
        IPropertyStore* pProps = NULL;
        IMFMediaType* pInputType = NULL;
        IMFMediaType* pOutputType = NULL;
        
        UINT32 cBitrate = 0;

        //We need to find a suitable output media type
        //We need to create the encoder to get the available output types
        //and discard the instance.

        CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
        UINT32 cCLSID = 0;          // Size of the array.

        MFT_REGISTER_TYPE_INFO tinfo;
        
        tinfo.guidMajorType = MFMediaType_Video;
        tinfo.guidSubtype = MFVideoFormat_WMV3;

        // Look for an encoder.
        HRESULT hr = MFTEnum(
            MFT_CATEGORY_VIDEO_ENCODER,
            0,                  // Reserved
            NULL,               // Input type to match. None.
            &tinfo,             // WMV encoded type.
            NULL,               // Attributes to match. (None.)
            &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
            &cCLSID             // Receives the size of the array.
            );
        if (FAILED(hr))
        {
            goto done;
        }

        // MFTEnum can return zero matches.
        if (cCLSID == 0)
        {
            hr = MF_E_TOPO_CODEC_NOT_FOUND;
            goto done;
        }
        else
        {
            //Create the MFT decoder
            hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
                CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));
            if (FAILED(hr))
            {
                goto done;
            }

        }
        
        //Get the video encoder property store
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
        if (FAILED(hr))
        {
            goto done;
        }

        //Set encoding properties
        hr = SetEncodingProperties(MFMediaType_Video, pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = CreateUncompressedVideoType(pType, &pInputType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMFT->SetInputType(0, pInputType, 0);

        //Get the first output type
        //You can loop through the available output types to choose 
        //the one that meets your target requirements
        hr =  pMFT->GetOutputAvailableType(0, 0, &pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        //Now set the bit rate
        hr = pOutputType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddPrivateData(pMFT, pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Return to the caller
        *ppVideoType = pOutputType;
        (*ppVideoType)->AddRef();
        
    done:
        SafeRelease(&pProps);
        SafeRelease(&pOutputType);
        SafeRelease(&pInputType);
        SafeRelease(&pMFT);
        CoTaskMemFree(pMFTCLSIDs);
        return hr;
    }
    ```

    

    En el ejemplo de código siguiente se crea un tipo de vídeo sin comprimir.

    ```C++
    //-------------------------------------------------------------------
    //  CreateUncompressedVideoType
    //  Creates an uncompressed video type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateUncompressedVideoType(IMFMediaType* pType, IMFMediaType** ppMediaType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppMediaType)
        {
            return E_POINTER;
        }
        
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        HRESULT hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFGetAttributeRatio(pType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

        }
        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;

        }

        interlace = MFGetAttributeUINT32(pType, MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);

        hr = MFGetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (FAILED(hr))
        {
            par.Numerator = par.Denominator = 1;
        }

        cBitrate = MFGetAttributeUINT32(pType, MF_MT_AVG_BITRATE, 1000000);

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_MAJOR_TYPE, guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_RGB32);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, 2);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppMediaType = pMediaType;
        (*ppMediaType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    ```

    

    En el ejemplo de código siguiente se agregan datos privados de códec al tipo de medio de vídeo especificado.

    ```C++
    //
    // AddPrivateData
    // Appends the private codec data to a media type.
    //
    // pMFT: The video encoder
    // pTypeOut: A video type from the encoder's type list.
    //
    // The function modifies pTypeOut by adding the codec data.
    //

    HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
    {
        HRESULT hr = S_OK;
        ULONG cbData = 0;
        BYTE *pData = NULL;

        IWMCodecPrivateData *pPrivData = NULL;

        DMO_MEDIA_TYPE mtOut = { 0 };

        // Convert the type to a DMO type.
        hr = MFInitAMMediaTypeFromMFMediaType(
            pTypeOut, 
            FORMAT_VideoInfo, 
            (AM_MEDIA_TYPE*)&mtOut
            );
        
        if (SUCCEEDED(hr))
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
        }

        if (SUCCEEDED(hr))
        {
            hr = pPrivData->SetPartialOutputType(&mtOut);
        }

        //
        // Get the private codec data
        //

        // First get the buffer size.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(NULL, &cbData);
        }

        if (SUCCEEDED(hr))
        {
            pData = new BYTE[cbData];

            if (pData == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        // Now get the data.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(pData, &cbData);
        }

        // Add the data to the media type.
        if (SUCCEEDED(hr))
        {
            hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
        }

        delete [] pData;
        MoFreeMediaType(&mtOut);
        SafeRelease(&pPrivData);
        return hr;
    }
    ```

    

### <a name="create-the-asf-contentinfo-object"></a>Creación del objeto ContentInfo de ASF

El objeto ContentInfo de ASF es un componente de nivel WMContainer diseñado principalmente para almacenar la información del objeto de encabezado de ASF. El receptor de archivos ASF implementa el objeto ContentInfo con el fin de almacenar información (en un almacén de propiedades) que se usará para escribir el objeto de encabezado ASF del archivo codificado. Para ello, debe crear y configurar el siguiente conjunto de información en el objeto ContentInfo antes de iniciar la sesión de codificación.

1.  Llame [**a MFCreateASFContentInfo para**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) crear un objeto ContentInfo vacío.

    En el ejemplo de código siguiente se crea un objeto ContentInfo vacío.

    ```C++
        // Create an empty ContentInfo object
        hr = MFCreateASFContentInfo(&pContentInfo);
        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  Llame [**a IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) para obtener el almacén de propiedades de nivel de flujo del receptor de archivos. En esta llamada, debe pasar el número de secuencia que asignó para la secuencia al crear el perfil de ASF.
3.  Establezca las propiedades de codificación [de nivel de flujo](configuring-the-encoder.md) en el almacén de propiedades de secuencia del receptor de archivos. Para obtener más información, vea "Propiedades de codificación de secuencias" en [Establecer propiedades en el receptor de archivos](setting-properties-in-the-file-sink.md).

    En el ejemplo de código siguiente se establecen las propiedades de nivel de flujo en el almacén de propiedades del receptor de archivos.

    ```C++
            //Get stream's encoding property
            hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
            if (FAILED(hr))
            {
                goto done;
            }

            //Set the stream-level encoding properties
            hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
            if (FAILED(hr))
            {
                goto done;
            }

    
    ```

    

    En el ejemplo de código siguiente se muestra la implementación de SetEncodingProperties. Esta función establece las propiedades de codificación de nivel de flujo para CBR y VBR.

    ```C++
    //-------------------------------------------------------------------
    //  SetEncodingProperties
    //  Create a media source from a URL.
    //
    //  guidMT:  Major type of the stream, audio or video
    //  pProps:  A pointer to the property store in which 
    //           to set the required encoding properties.
    //-------------------------------------------------------------------

    HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
    {
        if (!pProps)
        {
            return E_INVALIDARG;
        }

        if (EncodingMode == NONE)
        {
            return MF_E_NOT_INITIALIZED;
        }
       
        HRESULT hr = S_OK;

        PROPVARIANT var;

        switch (EncodingMode)
        {
            case CBR:
                // Set VBR to false.
                hr = InitPropVariantFromBoolean(FALSE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the video buffer window.
                if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            case VBR:
                //Set VBR to true.
                hr = InitPropVariantFromBoolean(TRUE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Number of encoding passes is 1.

                hr = InitPropVariantFromInt32(1, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the quality level.

                if (guidMT == MFMediaType_Audio)
                {
                    hr = InitPropVariantFromUInt32(98, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                else if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromUInt32(95, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            default:
                hr = E_UNEXPECTED;
                break;
        }    

    done:
        PropVariantClear(&var);
        return hr;
    }
    ```

    

4.  Llame [**a IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) para obtener el almacén de propiedades global del receptor de archivos. En esta llamada, debe pasar 0 en el primer parámetro. Para obtener más información, vea "Propiedades globales del receptor de archivos" en [Establecer propiedades en el receptor de archivos](setting-properties-in-the-file-sink.md).
5.  Establezca [**MFPKEY \_ ASFMEDIASINK \_ AUTOADJUST \_ BITRATE**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) en VARIANT TRUE para asegurarse de que los valores del cubo con fugas en el \_ multiplexor de ASF se ajusten correctamente. Para obtener información sobre esta propiedad, vea "Multiplexer Initialization and Leaky Bucket Configuración" en [Creating the Multiplexer Object](creating-the-multiplexer-object.md).

    En el ejemplo de código siguiente se establecen las propiedades de nivel de flujo en el almacén de propiedades del receptor de archivos.

    ```C++
        //Now we need to set global properties that will be set on the media sink
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(0, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Auto adjust Bitrate
        var.vt = VT_BOOL;
        var.boolVal = VARIANT_TRUE;

        hr = pContentInfoProps->SetValue(MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE, var);
        
        //Initialize with the profile
        hr = pContentInfo->SetProfile(pProfile);
        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

    > [!Note]  
    > Hay otras propiedades que puede establecer en el nivel global para el receptor de archivos. Para obtener más información, vea "Configuring the ContentInfo Object with Encoder Configuración" en [Setting Properties in the ContentInfo Object](setting-properties-in-the-contentinfo-object.md).

     

Usará el elemento ContentInfo de ASF configurado para crear un objeto de activación para el receptor de archivos de ASF (que se describe en la sección siguiente).

Si va a crear un receptor de archivos fuera de proceso [**(MFCreateASFMediaSinkActivate),**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)es decir, mediante un objeto de activación, puede usar el objeto ContentInfo configurado para crear una instancia del receptor de medios de ASF (que se describe en la sección siguiente). Si va a crear un receptor de archivos en proceso [**(MFCreateASFMediaSink),**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)en lugar de crear el objeto ContentInfo vacío tal y como se describe en el paso 1, obtenga una referencia a la interfaz [**MFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) mediante una llamada a **MFMediaSink::QueryInterface** en el receptor de archivos. A continuación, debe configurar el objeto ContentInfo como se describe en esta sección.

### <a name="create-the-asf-file-sink"></a>Creación del receptor de archivos de ASF

En este paso del tutorial, usará la función ContentInfo de ASF configurada, que creó en el paso anterior, para crear un objeto de activación para el receptor de archivos de ASF mediante una llamada a la función [**MFCreateASFMediaSinkActivate.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) Para obtener más información, vea [Creating the ASF File Sink](creating-the-asf-file-sink.md).

En el ejemplo de código siguiente se crea el objeto de activación para el receptor de archivos.


```C++
    //Create the activation object for the  file sink
    hr = MFCreateASFMediaSinkActivate(sURL, pContentInfo, &pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

```



## <a name="build-the-partial-encoding-topology"></a>Compilación de la topología de codificación parcial

A continuación, compilará una topología de codificación parcial mediante la creación de nodos de topología para el origen de medios, los codificadores Windows media necesarios y el receptor de archivos ASF. Después de agregar los nodos de topología, conectará los nodos de origen, transformación y receptor. Antes de agregar nodos de topología, debe crear un objeto de topología vacío llamando a [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).

### <a name="create-the-source-topology-node-for-the-media-source"></a>Creación del nodo de topología de origen para el origen de medios

En este paso, creará el nodo de topología de origen para el origen de medios.

Para crear este nodo, necesita las siguientes referencias:

-   Puntero al origen de medios que creó en el paso descrito en la sección "Crear el origen de medios" de este tutorial.
-   Puntero al descriptor de presentación para el origen multimedia. Puede obtener una referencia a la interfaz IMFPresentationDescriptor del origen multimedia llamando a [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).
-   Puntero al descriptor de flujo para cada secuencia del origen multimedia para el que ha creado una secuencia de destino en el paso descrito en la sección "Crear el objeto de perfil de ASF" de este tutorial.

Para obtener más información sobre cómo crear nodos de origen y ejemplos de código, vea [Crear nodos de origen.](creating-source-nodes.md)

En el ejemplo de código siguiente se crea una topología parcial agregando el nodo de origen y los nodos de transformación necesarios. Este código llama a las funciones auxiliares AddSourceNode y AddTransformOutputNodes. Estas funciones se incluyen más adelante en este tutorial.


```C++
//-------------------------------------------------------------------
//  BuildPartialTopology
//  Create a partial encoding topology by adding the source and the sink.
//
//  pSource:  A pointer to the media source to enumerate the source streams.
//  pSinkActivate: A pointer to the activation object for ASF file sink.
//  ppTopology:  Receives a pointer to the topology.
//-------------------------------------------------------------------

HRESULT BuildPartialTopology(
       IMFMediaSource *pSource, 
       IMFActivate* pSinkActivate,
       IMFTopology** ppTopology)
{
    if (!pSource || !pSinkActivate)
    {
        return E_INVALIDARG;
    }
    if (!ppTopology)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    IMFPresentationDescriptor* pPD = NULL;
    IMFStreamDescriptor *pStreamDesc = NULL;
    IMFMediaTypeHandler* pMediaTypeHandler = NULL;
    IMFMediaType* pSrcType = NULL;

    IMFTopology* pTopology = NULL;
    IMFTopologyNode* pSrcNode = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;


    DWORD cElems = 0;
    DWORD dwSrcStream = 0;
    DWORD StreamID = 0;
    GUID guidMajor = GUID_NULL;
    BOOL fSelected = FALSE;


    //Create the topology that represents the encoding pipeline
    hr = MFCreateTopology (&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

        
    hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPD->GetStreamDescriptorCount(&dwSrcStream);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        hr = AddSourceNode(pTopology, pSource, pPD, pStreamDesc, &pSrcNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamDesc->GetMediaTypeHandler (&pMediaTypeHandler);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pStreamDesc->GetStreamIdentifier(&StreamID);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaTypeHandler->GetMediaTypeByIndex(0, &pSrcType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSrcType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddTransformOutputNodes(pTopology, pSinkActivate, pSrcType, &pEncoderNode);
        if (FAILED(hr))
        {
            goto done;
        }

        //now we have the transform node, connect it to the source node
        hr = pSrcNode->ConnectOutput(0, pEncoderNode, 0);
        if (FAILED(hr))
        {
            goto done;
        }
                

        SafeRelease(&pStreamDesc);
        SafeRelease(&pMediaTypeHandler);
        SafeRelease(&pSrcType);
        SafeRelease(&pEncoderNode);
        SafeRelease(&pOutputNode);
        guidMajor = GUID_NULL;
    }

    *ppTopology = pTopology;
   (*ppTopology)->AddRef();


    wprintf_s(L"Partial Topology Built.\n");

done:
    SafeRelease(&pStreamDesc);
    SafeRelease(&pMediaTypeHandler);
    SafeRelease(&pSrcType);
    SafeRelease(&pEncoderNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pTopology);

    return hr;
}
```



En el ejemplo de código siguiente se crea y agrega el nodo de topología de origen a la topología de codificación. Toma punteros a un objeto de topología anterior, el origen de medios para enumerar las secuencias de origen, el descriptor de presentación del origen de medios y el descriptor de flujo del origen multimedia. El autor de la llamada recibe un puntero al nodo de topología de origen.


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



### <a name="instantiate-the-required-encoders-and-create-the-transform-nodes"></a>Crear instancias de los codificadores necesarios y crear los nodos de transformación

La Media Foundation de datos no inserta automáticamente los codificadores Windows media necesarios para las secuencias que debe codificar. La aplicación debe agregar los codificadores manualmente. Para ello, enumere las secuencias del perfil de ASF que creó en el paso descrito en la sección "Crear el objeto de perfil de ASF" de este tutorial. Para cada secuencia del origen y la secuencia correspondiente del perfil, cree una instancia de los codificadores necesarios. Para este paso, necesita un puntero al objeto de activación para el receptor de archivos que creó en el paso descrito en la sección "Crear el receptor de archivos ASF" de este tutorial.

Para obtener información general sobre la creación de codificadores a través de objetos de activación, vea [Using an Encoder's Activation Objects](using-an-encoder-s-activation-objects.md).

En el procedimiento siguiente se describen los pasos necesarios para crear instancias de los codificadores necesarios.

1.  Para obtener una referencia al objeto ContentInfo del receptor, llame a [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) en el receptor de archivos activate y, a continuación, consulte [**ELFFContentInfo desde**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) el receptor de archivos mediante una llamada a **QueryInterface**.
2.  Obtenga el perfil de ASF asociado al objeto ContentInfo llamando a [**IMFASFContentInfo::GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile).
3.  Enumerar las secuencias del perfil. Para ello, necesitará el número de secuencias y una referencia a la interfaz [**DEFSTREAMConfig de cada**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) secuencia.

    Llame a los métodos siguientes:

    -   [**IMFASFProfile::GetStreamCount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)
    -   [**IMFASFProfile::GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)

4.  Para cada secuencia, obtenga el tipo principal y las propiedades de codificación de la secuencia del objeto ContentInfo.

    Llame a los métodos siguientes:

    -   [**IMFASFStreamConfig::GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype)
    -   [**IMFMediaType::GetMajorType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)
    -   [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)

        Para esta llamada, necesita el número de secuencia recuperado por la [**llamada a IMFASFProfile::GetStream.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)

5.  En función del tipo de secuencia, audio o vídeo, cree una instancia del objeto de activación para el codificador mediante una llamada a [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) o [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate).

    Para llamar a estas funciones, necesita las siguientes referencias:

    -   Puntero al tipo de medio de la secuencia recuperado por [**IMFASFStreamConfig::GetMediaType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) en el paso anterior.
    -   Puntero al almacén de propiedades de codificación de la secuencia recuperado por [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore). Al pasar un puntero al almacén de propiedades, las propiedades de secuencia establecidas en el receptor de archivos se copian en el MFT del codificador.

6.  Actualice el parámetro de cubo de fugas para la secuencia de audio.

    [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) establece el tipo de salida en el codificador subyacente MFT para el códec de audio Windows Media. Una vez establecido el tipo de medio de salida, el codificador obtiene la velocidad de bits media del tipo de medio de salida, calcula la velocidad de bits de la ventana de búfer y establece los valores del cubo de pérdidas que se usarán durante la sesión de codificación. Puede actualizar estos valores en el receptor de archivos consultando el codificador o estableciendo valores personalizados. Para actualizar los valores, necesita el siguiente conjunto de información:

    -   Velocidad de bits media: obtenga la velocidad de bits media del atributo [**AVG \_ BYTES PER \_ \_ \_ \_ \_ SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) de MF MT AUDIO establecido en el tipo de medio de salida seleccionado durante la negociación del tipo de medio.
    -   Ventana búfer: puede recuperarla llamando a [**IWMCodecLeakyBucket::GetBufferSizeBits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md).
    -   Tamaño inicial del búfer: se establece en 0.

    Cree una matriz de DWORD y establezca el valor en la propiedad [**\_ MFPKEY ASFSTREAMSINK \_ \_ CORRECTED LEAKYBUCKET**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) del receptor de secuencia de audio. Si no proporciona los valores actualizados, la sesión multimedia los establece correctamente.

    Para obtener más información, vea [The Leaky Bucket Buffer Model](the-leaky-bucket-buffer-model.md).

Los objetos de activación creados en el paso 5 deben agregarse a la topología como nodos de topología de transformación. Para obtener más información y código de ejemplo, vea "Creating a Transform Node from an Activation Object" (Crear un nodo de transformación a partir de un objeto de activación) en [Creating Transform Nodes](creating-transform-nodes.md).

En el ejemplo de código siguiente se crea y se agrega el codificador necesario. Toma punteros a un objeto de topología creado previamente, el objeto de activación del receptor del archivo y el tipo de medio del flujo de origen. También llama a AddOutputNode (vea el ejemplo de código siguiente) que crea y agrega el nodo receptor a la topología de codificación. It El autor de la llamada recibe un puntero al nodo de topología de origen.


```C++
//-------------------------------------------------------------------
//  AddTransformOutputNodes
//  Creates and adds the sink node to the encoding topology.
//  Creates and adds the required encoder activates.

//  pTopology:  A pointer to the topology.
//  pSinkActivate:  A pointer to the file sink's activation object.
//  pSourceType: A pointer to the source stream's media type.
//  ppNode:  Receives a pointer to the topology node.
//-------------------------------------------------------------------

HRESULT AddTransformOutputNodes(
    IMFTopology* pTopology,
    IMFActivate* pSinkActivate,
    IMFMediaType* pSourceType,
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    if (!pTopology || !pSinkActivate || !pSourceType)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNode* pEncNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFProfile* pProfile = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFMediaType* pMediaType = NULL;
    IPropertyStore* pProps = NULL;
    IMFActivate *pEncoderActivate = NULL;
    IMFMediaSink *pSink = NULL; 

    GUID guidMT = GUID_NULL;
    GUID guidMajor = GUID_NULL;

    DWORD cStreams = 0;
    WORD wStreamNumber = 0;

    HRESULT hr = S_OK;
        
    hr = pSourceType->GetMajorType(&guidMajor);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Activate the sink
    hr = pSinkActivate->ActivateObject(__uuidof(IMFMediaSink), (void**)&pSink);
    if (FAILED(hr))
    {
        goto done;
    }
    //find the media type in the sink
    //Get content info from the sink
    hr = pSink->QueryInterface(__uuidof(IMFASFContentInfo), (void**)&pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }
    

    hr = pContentInfo->GetProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->GetStreamCount(&cStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreams ; index++)
    {
        hr = pProfile->GetStream(index, &wStreamNumber, &pStream);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pStream->GetMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->GetMajorType(&guidMT);
        if (FAILED(hr))
        {
            goto done;
        }
        if (guidMT!=guidMajor)
        {
            SafeRelease(&pStream);
            SafeRelease(&pMediaType);
            guidMT = GUID_NULL;

            continue;
        }
        //We need to activate the encoder
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamNumber, &pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMT == MFMediaType_Audio)
        {
             hr = MFCreateWMAEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Audio Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
        if (guidMT == MFMediaType_Video)
        {
            hr = MFCreateWMVEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Video Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
    }

    // Set the object pointer.
    hr = pEncNode->SetObject(pEncoderActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output node to this node.
    hr = AddOutputNode(pTopology, pSinkActivate, wStreamNumber, &pOutputNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //now we have the output node, connect it to the transform node
    hr = pEncNode->ConnectOutput(0, pOutputNode, 0);
    if (FAILED(hr))
    {
        goto done;
    }

   // Return the pointer to the caller.
    *ppNode = pEncNode;
    (*ppNode)->AddRef();


done:
    SafeRelease(&pEncNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pEncoderActivate);
    SafeRelease(&pMediaType);
    SafeRelease(&pProps);
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    SafeRelease(&pContentInfo);
    SafeRelease(&pSink);
    return hr;
}
```



### <a name="create-the-output-topology-nodes-for-the-file-sink"></a>Creación de los nodos de topología de salida para el receptor de archivos

En este paso, creará el nodo de topología de salida para el receptor de archivos de ASF.

Para crear este nodo, necesita las siguientes referencias:

-   Puntero al objeto de activación que creó en el paso descrito en la sección "Creación del receptor de archivos de ASF" de este tutorial.
-   Números de secuencia para identificar los receptores de flujo agregados al receptor de archivos. Los números de secuencia coinciden con la identificación de la secuencia que se estableció durante la creación de la secuencia.

Para obtener más información sobre la creación de nodos de salida y el ejemplo de código, vea "Crear un nodo de salida a partir de un objeto de activación" en [Creación de nodos de salida.](creating-output-nodes.md)

Si no usa el objeto de activación para el receptor de archivos, debe enumerar los receptores de flujo en el receptor de archivos de ASF y establecer cada receptor de flujo como el nodo de salida de la topología. Para obtener información sobre la enumeración de receptores de flujo, vea "Enumerating Stream Sinks" (Enumeración de receptores de flujo) en Adding Stream Information to the ASF File Sink (Agregar información de flujo [al receptor de archivos de ASF).](adding-stream-information-to-the-asf-file-sink.md)

En el ejemplo de código siguiente se crea y agrega el nodo receptor a la topología de codificación. Toma punteros a un objeto de topología creado previamente, el objeto de activación del receptor del archivo y el número de identificación de la secuencia. It El autor de la llamada recibe un puntero al nodo de topología de origen.


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



En el ejemplo de código siguiente se enumeran los receptores de flujo para un receptor multimedia determinado.


```C++
//-------------------------------------------------------------------
//  EnumerateStreamSinks
//  Enumerates the stream sinks within the specified media sink.
//
//  pSink:  A pointer to the media sink.
//-------------------------------------------------------------------
HRESULT EnumerateStreamSinks (IMFMediaSink* pSink)
{
    if (!pSink)
    {
        return E_INVALIDARG;
    }
    
    IMFStreamSink* pStreamSink = NULL;
    DWORD cStreamSinks = 0;

    HRESULT hr = pSink->GetStreamSinkCount(&cStreamSinks);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreamSinks; index++)
    {
        hr = pSink->GetStreamSinkByIndex (index, &pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        //Use the stream sink
        //Not shown.
    }
done:
    SafeRelease(&pStreamSink);

    return hr;
}
```



### <a name="connect-the-source-transform-and-sink-nodes"></a>Conectar los nodos de origen, transformación y receptor

En este paso, conectará el nodo de origen al nodo de transformación que hace referencia a las activaciones de codificación que creó en el paso descrito en la sección "Creación de instancias de los codificadores necesarios y creación de los nodos de transformación" de este tutorial. El nodo de transformación se conectará al nodo de salida que contiene el objeto de activación para el receptor de archivos.

## <a name="handling-the-encoding-session"></a>Control de la sesión de codificación

En el paso , realizará los pasos siguientes:

1.  Llame [**a MFCreateMediaSession para**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) crear una sesión de codificación.
2.  Llame [**a IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) para establecer la topología de codificación en la sesión. Si se completa la llamada, la sesión multimedia evalúa los nodos de topología e inserta objetos de transformación adicionales, como un descodificador que convierte el origen comprimido especificado en muestras sin comprimir para introducirlos como entrada en el codificador.
3.  Llame [**a IMFMediaSession::GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) para solicitar los eventos que genera la sesión multimedia.

    En el bucle de eventos, iniciará y cerrará la sesión de codificación en función de los eventos que genera la sesión multimedia. La [**llamada a MFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) da como resultado que la sesión multimedia genera el evento [MESessionTopologyStatus](mesessiontopologystatus.md) con la marca MF \_ TOPOSTATUS \_ READY establecida. Todos los eventos se generan de forma asincrónica y una aplicación puede recuperar estos eventos de forma sincrónica o asincrónica. Dado que la aplicación de este tutorial es una aplicación de consola y el bloqueo de subprocesos de la interfaz de usuario no es un problema, se obtienen los eventos de la sesión multimedia de forma sincrónica.

    Para obtener los eventos de forma asincrónica, la aplicación debe implementar la [**interfaz IMFAsyncCallback.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) Para obtener más información y una implementación de ejemplo de esta interfaz, vea "Control de eventos de sesión" en Cómo reproducir archivos [multimedia con Media Foundation](how-to-play-unprotected-media-files.md).

En el bucle de eventos para obtener los eventos de sesión multimedia, espere al evento [MESessionTopologyStatus](mesessiontopologystatus.md) que se genera cuando se completa [**LANSESIÓNMEDIA::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) y se resuelve la topología. Al obtener el evento MESessionTopologyStatus, inicie la sesión de codificación mediante una llamada [**a IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start). La sesión multimedia genera el [evento MEEndOfPresentation](meendofpresentation.md) cuando se completan todas las operaciones de codificación. Este evento debe controlarse para la codificación VBR y se describe en la sección siguiente "Actualizar propiedades de codificación en el receptor de archivos para la codificación VBR" de este tutorial.

La sesión multimedia genera el objeto de encabezado ASF y finaliza el archivo cuando se completa la sesión de codificación y, a continuación, genera el [evento MESessionClosed.](mesessionclosed.md) Este evento debe controlarse realizando las operaciones de apagado adecuadas en la sesión multimedia. Para comenzar las operaciones de apagado, llame [**a LAMEMEDIASession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown). Una vez cerrada la sesión de codificación, no se puede establecer otra topología para codificar en la misma instancia de sesión multimedia. Para codificar otro archivo, la sesión multimedia actual debe cerrarse y liberarse, y la nueva topología debe establecerse en una sesión multimedia recién creada. En el ejemplo de código siguiente se crea la sesión multimedia, se establece la topología de codificación y se administran los eventos de sesión multimedia.

En el ejemplo de código siguiente se crea la sesión multimedia, se establece la topología de codificación y se controla la sesión de codificación mediante el control de eventos de la sesión multimedia.


```C++
//-------------------------------------------------------------------
//  Encode
//  Controls the encoding session and handles events from the media session.
//
//  pTopology:  A pointer to the encoding topology.
//-------------------------------------------------------------------

HRESULT Encode(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }
    
    IMFMediaSession *pSession = NULL;
    IMFMediaEvent* pEvent = NULL;
    IMFTopology* pFullTopology = NULL;
    IUnknown* pTopoUnk = NULL;


    MediaEventType meType = MEUnknown;  // Event type

    HRESULT hr = S_OK;
    HRESULT hrStatus = S_OK;            // Event status
                
    MF_TOPOSTATUS TopoStatus = MF_TOPOSTATUS_INVALID; // Used with MESessionTopologyStatus event.    
        

    hr = MFCreateMediaSession(NULL, &pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->SetTopology(MFSESSION_SETTOPOLOGY_IMMEDIATE, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get media session events synchronously
    while (1)
    {
        hr = pSession->GetEvent(0, &pEvent);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetType(&meType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetStatus(&hrStatus);
        if (FAILED(hr))
        {
            goto done;
        }
        if (FAILED(hrStatus))
        {
            hr = hrStatus;
            goto done;
        }

       switch(meType)
        {
            case MESessionTopologyStatus:
                {
                    // Get the status code.
                    MF_TOPOSTATUS status = (MF_TOPOSTATUS)MFGetAttributeUINT32(
                                             pEvent, MF_EVENT_TOPOLOGY_STATUS, MF_TOPOSTATUS_INVALID);

                    if (status == MF_TOPOSTATUS_READY)
                    {
                        PROPVARIANT var;
                        PropVariantInit(&var);
                        wprintf_s(L"Topology resolved and set on the media session.\n");

                        hr = pSession->Start(NULL, &var);
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                    }
                    if (status == MF_TOPOSTATUS_STARTED_SOURCE)
                    {
                        wprintf_s(L"Encoding started.\n");
                        break;
                    }
                    if (status == MF_TOPOSTATUS_ENDED)
                    {
                        wprintf_s(L"Encoding complete.\n");
                        hr = pSession->Close();
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                        break;
                    }
                }
                break;


            case MESessionEnded:
                wprintf_s(L"Encoding complete.\n");
                hr = pSession->Close();
                if (FAILED(hr))
                {
                    goto done;
                }
                break;

            case MEEndOfPresentation:
                {
                    if (EncodingMode == VBR)
                    {
                        hr = pSession->GetFullTopology(MFSESSION_GETFULLTOPOLOGY_CURRENT, 0, &pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        hr = PostEncodingUpdate(pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        wprintf_s(L"Updated sinks for VBR. \n");
                    }
                }
                break;

            case MESessionClosed:
                wprintf_s(L"Encoding session closed.\n");

                hr = pSession->Shutdown();
                goto done;
        }
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pEvent);

    }
done:
    SafeRelease(&pEvent);
    SafeRelease(&pSession);
    SafeRelease(&pFullTopology);
    SafeRelease(&pTopoUnk);
    return hr;
}
```



## <a name="update-encoding-properties-in-the-file-sink"></a>Actualizar las propiedades de codificación en el receptor de archivos

Ciertas propiedades de codificación, como la velocidad de bits de codificación y los valores precisos del depósito de fugas, no se conocen hasta que se completa la codificación, especialmente para la codificación VBR. Para obtener los valores correctos, la aplicación debe esperar al evento [MEEndOfPresentation](meendofpresentation.md) que indica que la sesión de codificación se ha completado. Los valores del cubo de pérdida deben actualizarse en el receptor para que el objeto de encabezado de ASF pueda reflejar los valores precisos.

En el procedimiento siguiente se describen los pasos necesarios para atravesar los nodos de la topología de codificación para obtener el nodo receptor de archivos y establecer las propiedades de cubo de pérdida necesarias.

**Para actualizar los valores de propiedad posteriores a la codificación en el receptor de archivos ASF**

1.  Llame [**a IMFTopology::GetOutputNodeCollection para**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) obtener la colección de nodos de salida de la topología de codificación.
2.  Para cada nodo, obtenga un puntero al receptor de flujo en el nodo mediante una llamada a [**IMFTopologyNode::GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject). Consulta de la [**interfaz IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) en el [**puntero IUnknown devuelto**](/windows/win32/api/unknwn/nn-unknwn-iunknown) por **LADETOPOLOGYNode::GetObject**.
3.  Para cada receptor de flujo, obtenga el nodo de bajada (codificador) mediante una llamada [**a IMFTopologyNode::GetInput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput).
4.  Consulte el nodo para obtener el puntero [**DETRANSFORMTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) del nodo del codificador.
5.  Consulte el codificador para el puntero [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para obtener el almacén de propiedades de codificación del codificador.
6.  Consulte el receptor de secuencias para el [**puntero IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para obtener el almacén de propiedades del receptor del flujo.
7.  Llame [**a IPropertyStore::GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) para obtener los valores de propiedad necesarios del almacén de propiedades del codificador y cópielos en el almacén de propiedades del receptor de secuencias llamando a **IPropertyStore::SetValue**.

En la tabla siguiente se muestran los valores de propiedad posteriores a la codificación que se deben establecer en el receptor de secuencias para la secuencia de vídeo.



| Tipo de codificación                                                                                  | Nombre de propiedad (GetValue)                                                                        | Nombre de propiedad (SetValue)                                                                                                |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Codificación de velocidad de bits constante](constant-bit-rate-encoding.md)                                   | MFPKEY \_ BAVG<br/> MFPKEY \_ ESTOG<br/>                                                 | MFPKEY \_ STAT \_ BAVG<br/> MFPKEY \_ STAT \_ STAT STATG<br/>                                                             |
| [Codificación de velocidad de bits variable basada en calidad](quality-based-variable-bit-rate--vbr--encoding.md) | MFPKEY \_ BAVG<br/> MFPKEY \_ ESTOG<br/> MFPKEY \_ BMAX<br/> MFPKEY \_ RMAX<br/> | MFPKEY \_ STAT \_ BAVG<br/> MFPKEY \_ STAT \_ STAT STATG<br/> MFPKEY \_ STAT \_ BMAX<br/> MFPKEY \_ STAT \_ RMAX<br/> |



 

En el ejemplo de código siguiente se establecen los valores de propiedad posteriores a la codificación.


```C++
//-------------------------------------------------------------------
//  PostEncodingUpdate
//  Updates the file sink with encoding properties set on the encoder
//  during the encoding session.
    //1. Get the output nodes
    //2. For each node, get the downstream node
    //3. For the downstream node, get the MFT
    //4. Get the property store
    //5. Get the required values
    //6. Set them on the stream sink
//
//  pTopology: A pointer to the full topology retrieved from the media session.
//-------------------------------------------------------------------

HRESULT PostEncodingUpdate(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFCollection* pOutputColl = NULL;
    IUnknown* pNodeUnk = NULL;
    IMFMediaType* pType = NULL;
    IMFTopologyNode* pNode = NULL;
    IUnknown* pSinkUnk = NULL;
    IMFStreamSink* pStreamSink = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IUnknown* pEncoderUnk = NULL;
    IMFTransform* pEncoder = NULL;
    IPropertyStore* pStreamSinkProps = NULL;
    IPropertyStore* pEncoderProps = NULL;

    GUID guidMajorType = GUID_NULL;

    PROPVARIANT var;
    PropVariantInit( &var );

    DWORD cElements = 0;

    hr = pTopology->GetOutputNodeCollection( &pOutputColl);
    if (FAILED(hr))
    {
        goto done;
    }


    hr = pOutputColl->GetElementCount(&cElements);
    if (FAILED(hr))
    {
        goto done;
    }


    for(DWORD index = 0; index < cElements; index++)
    {
        hr = pOutputColl->GetElement(index, &pNodeUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNodeUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInputPrefType(0, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->GetMajorType( &guidMajorType );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetObject(&pSinkUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSinkUnk->QueryInterface(IID_IMFStreamSink, (void**)&pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInput( 0, &pEncoderNode, NULL );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderNode->GetObject(&pEncoderUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderUnk->QueryInterface(IID_IMFTransform, (void**)&pEncoder);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamSink->QueryInterface(IID_IPropertyStore, (void**)&pStreamSinkProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoder->QueryInterface(IID_IPropertyStore, (void**)&pEncoderProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if( guidMajorType == MFMediaType_Video )
        {            
            hr = pEncoderProps->GetValue( MFPKEY_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_BMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else if( guidMajorType == MFMediaType_Audio )
        {      
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BMAX, &var);
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var );         
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, var );         
            if (FAILED(hr))
            {
                goto done;
            }
        } 
        PropVariantClear( &var ); 
   }
done:
    SafeRelease (&pOutputColl);
    SafeRelease (&pNodeUnk);
    SafeRelease (&pType);
    SafeRelease (&pNode);
    SafeRelease (&pSinkUnk);
    SafeRelease (&pStreamSink);
    SafeRelease (&pEncoderNode);
    SafeRelease (&pEncoderUnk);
    SafeRelease (&pEncoder);
    SafeRelease (&pStreamSinkProps);
    SafeRelease (&pEncoderProps);

    return hr;
   
}
```



## <a name="implement-main"></a>Implementar Main

En el ejemplo de código siguiente se muestra la función principal de la aplicación de consola.


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 4)
    {
        wprintf_s(L"Usage: %s inputaudio.mp3, %s output.wm*, %Encoding Type: CBR, VBR\n");
        return 0;
    }


    HRESULT             hr = S_OK;

    IMFMediaSource* pSource = NULL;
    IMFTopology* pTopology = NULL;
    IMFActivate* pFileSinkActivate = NULL;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the requested encoding mode
    if (wcscmp(argv[3], L"CBR")==0)
    {
        EncodingMode = CBR;
    }
    else if (wcscmp(argv[3], L"VBR")==0)
    {
        EncodingMode = VBR;
    }
    else
    {
        EncodingMode = CBR;
    }

    // Start up Media Foundation platform.
    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the media source
    hr = CreateMediaSource(argv[1], &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the file sink activate
    hr = CreateMediaSink(argv[2], pSource, &pFileSinkActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    //Build the encoding topology.
    hr = BuildPartialTopology(pSource, pFileSinkActivate, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Instantiate the media session and start encoding
    hr = Encode(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }


done:
    // Clean up.
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    SafeRelease(&pFileSinkActivate);

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the output file due to 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="test-the-output-file"></a>Probar el archivo de salida

En la lista siguiente se describe una lista de comprobación para probar el archivo codificado. Estos valores se pueden activar en el cuadro de diálogo propiedades del archivo  que puede mostrar haciendo clic con el botón derecho en el archivo codificado y seleccionando Propiedades en el menú contextual.

-   La ruta de acceso del archivo codificado es precisa.
-   El tamaño del archivo es superior a cero KB y la duración de reproducción coincide con la duración del archivo de origen.
-   Para la secuencia de vídeo, compruebe el ancho y el alto del fotograma, la velocidad de fotogramas. Estos valores deben coincidir con los valores especificados en el perfil de ASF que creó en el paso descrito en la sección "Crear el objeto de perfil de ASF".
-   Para la secuencia de audio, la velocidad de bits debe estar cerca del valor especificado en el tipo de medio de destino.
-   Abra el archivo en Reproductor de Windows Media compruebe la calidad de la codificación.
-   Abra el archivo ASF en ASFViewer para ver la estructura de un archivo ASF. Esta herramienta se puede descargar desde este sitio [web de Microsoft.](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea)

## <a name="common-error-codes-and-debugging-tips"></a>Códigos de error comunes y depuración Sugerencias

En la lista siguiente se describen los códigos de error comunes que podría recibir y las sugerencias de depuración.

-   La llamada [**a IMFSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) detiene la aplicación.

    Asegúrese de que ha inicializado la plataforma Media Foundation mediante una llamada a [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup). Esta función configura internamente la plataforma asincrónica que usan todos los métodos que inician operaciones asincrónicas, como [**IMFSourceResolver::CreateObjectFromURL.**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)

-   [**CARDINALSourceResolver::CreateObjectFromURL**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) devuelve HRESULT 0x80070002 "El sistema no puede encontrar el archivo especificado.

    Asegúrese de que existe el nombre de archivo de entrada especificado por el usuario en el primer argumento.

-   HRESULT 0x80070020 "El proceso no puede tener acceso al archivo porque otro proceso lo está utilizando. "

    Asegúrese de que los archivos de entrada y salida no están actualmente en uso por otro recurso del sistema.

-   Las llamadas [**a los métodos DETRANSFORMTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) devuelven MF \_ E \_ INVALIDMEDIATYPE.

    Asegúrese de que se cumplen las condiciones siguientes:

    -   El tipo de entrada o el tipo de salida que especificó es compatible con los tipos de medios que admite el codificador.
    -   Los tipos de medios especificados están completos. Para que los tipos de medios se completen, consulte los atributos necesarios en las secciones "Crear un tipo de medio de audio comprimido" y "Crear un tipo de medio de vídeo comprimido" de este tutorial.
    -   Asegúrese de que ha establecido la velocidad de bits de destino en el tipo de medio parcial al que va a agregar los datos privados del códec.

-   La sesión multimedia devuelve MF \_ E \_ UNSUPPORTED \_ D3D \_ TYPE en el estado del evento.

    Este error se devuelve cuando el tipo de medio del origen indica un modo de intercalación mixto que no es compatible con Windows codificador de Vídeo multimedia. Si el tipo de medio de vídeo comprimido está establecido para usar el modo progresiva, la canalización debe usar una transformación de desenlazado. Dado que la canalización no encuentra una coincidencia (indicada por este código de error), debe insertar manualmente un desenlace (procesador de vídeo transcodificador) entre el descodificador y los nodos del codificador.

-   La sesión multimedia devuelve E \_ INVALIDARG en el estado del evento.

    Este error se devuelve cuando los atributos de tipo multimedia del origen no son compatibles con los atributos del tipo de medio de salida establecido en Windows codificador multimedia.

-   [**IWMCodecPrivateData::GetPrivateData**](../wmformat/iwmcodecprivatedata-getprivatedata.md) devuelve HRESULT 0x80040203 "Error de sintaxis al intentar evaluar una cadena de consulta"

    Asegúrese de que el tipo de entrada está establecido en el MFT del codificador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Componentes de ASF de capa de canalización](pipeline-layer-asf-components.md)
</dt> </dl>

 

 
