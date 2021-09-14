---
description: En este tutorial se usa sink writer para codificar un archivo de vídeo.
ms.assetid: 3E297366-0863-4E89-A0D5-438CD1FC5AF9
title: 'Tutorial: Uso del escritor de receptores para codificar vídeo'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3e6095355e18db6c8335cadcbc4afc56b35406
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127268620"
---
# <a name="tutorial-using-the-sink-writer-to-encode-video"></a>Tutorial: Uso del escritor de receptores para codificar vídeo

En este tutorial se usa [sink writer para](sink-writer.md) codificar un archivo de vídeo.

## <a name="define-the-video-format"></a>Definir el formato de vídeo

Para simplificar, en este tutorial se usa un formato de vídeo fijo, definido por las siguientes constantes:


```C++
// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;
```



Estas constantes especifican los parámetros siguientes del formato de vídeo:

-   Tamaño del marco (ancho y alto)
-   Fotogramas por segundo.
-   Velocidad de bits codificada.
-   Formato de codificación, Windows Media Video 9 (**MFVideoFormat \_ WMV3**).
-   Formato de entrada, que es RGB de 32 bits.
-   Duración del archivo de salida.

El programa usa estas constantes para crear los tipos de medios que describen el formato. En una aplicación real, normalmente admitiría una variedad de perfiles de codificación.

## <a name="create-an-uncompressed-video-frame"></a>Creación de un fotograma de vídeo sin comprimir

Además, para simplificar, en este tutorial se usa un fotograma de vídeo estático como entrada. El marco de vídeo contiene un rectángulo verde sólido y se genera mediante programación. El fotograma de vídeo se almacena en una variable global como una matriz de **DWORD:**


```C++
// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];
```



El código siguiente establece cada píxel del marco en verde:


```C++
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }
```



## <a name="initialize-the-sink-writer"></a>Inicializar el escritor de receptores

Para inicializar el escritor de receptores, realice los pasos siguientes.

1.  Llame [**a MFCreateSinkWriterFromURL para**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-mfcreatesinkwriterfromurl) crear una nueva instancia del escritor receptor.
2.  Cree un tipo de medio que describa el vídeo codificado.
3.  Pase este tipo de medio al [**método IMFSinkWriter::AddStream.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-addstream)
4.  Cree un segundo tipo de medio que describa la entrada sin comprimir.
5.  Pase el tipo de medio sin comprimir al [**método IMFSinkWriter::SetInputMediaType.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-setinputmediatype)
6.  Llame al [**método IMFSinkWriter::BeginWriting.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-beginwriting)
7.  El escritor de receptores ya está listo para aceptar ejemplos de entrada.

En el código siguiente se muestran estos pasos.


```C++
HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}
```



La mayoría de los pasos del ejemplo de código anterior son establecer los atributos de tipo de medio para los dos tipos de medios. Los detalles de los tipos de medios dependerán del contenido de origen y del perfil de codificación deseado.

## <a name="send-video-frames-to-the-sink-writer"></a>Envío de fotogramas de vídeo al escritor receptor

Para enviar un fotograma de vídeo al escritor del receptor, llame al método [**IMFSinkWriter::WriteSample.**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) El **método WriteSample** toma un puntero a la [**interfaz IMFSample,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) que representa un *objeto de ejemplo multimedia.* El ejemplo de medios contiene un *objeto de búfer multimedia,* que a su vez contiene un puntero al marco de vídeo. Para obtener más información sobre los ejemplos de medios y el búfer, vea los temas siguientes.

-   [Ejemplos de medios](media-samples.md)
-   [Búferes multimedia](media-buffers.md)

Dependiendo de la aplicación, es posible que obtenga los ejemplos multimedia del Lector [de origen.](source-reader.md) Como alternativa, puede crear los ejemplos de medios y manipular directamente los datos en el búfer. El código siguiente muestra el segundo enfoque. Crea un búfer de memoria y escribe un único fotograma de vídeo en el búfer. A continuación, agrega ese búfer a un ejemplo multimedia y envía el ejemplo multimedia al sistema de escritura del receptor.


```C++
HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



Este código realiza los pasos siguientes.

1.  Llame a [**MFCreateMemoryBuffer para**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatememorybuffer) crear un objeto de búfer multimedia. Esta función asigna la memoria para el búfer.
2.  Llame [**a IMFMediaBuffer::Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) para bloquear el búfer y obtener un puntero a la memoria.
3.  Llame [**a MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) para copiar el fotograma de vídeo en el búfer.
    > [!Note]  
    > En este ejemplo concreto, el **uso de memcpy** también funcionaría. Sin embargo, [**la función MFCopyImage**](/windows/desktop/api/mfapi/nf-mfapi-mfcopyimage) controla correctamente el caso en el que el paso de la imagen de origen no coincide con el búfer de destino. Para obtener más información, vea [Image Stride](image-stride.md).

     

4.  Llame [**a IMFMediaBuffer::Unlock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-unlock) para desbloquear el búfer.
5.  Llame [**aBUFFERMediaBuffer::SetCurrentLength para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-setcurrentlength) actualizar la longitud de los datos válidos en el búfer. (De lo contrario, este valor tiene como valor predeterminado cero).
6.  Llame [**a MFCreateSample**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatesample) para crear un objeto de ejemplo multimedia.
7.  Llame [**a IMFSample::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer) para agregar el búfer multimedia al ejemplo de medios.
8.  Llame [**aSAMPLESample::SetSampleTime para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime) establecer la marca de tiempo del fotograma de vídeo.
9.  Llame [**aSAMPLESample::SetSampleDuration para**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration) establecer la duración del fotograma de vídeo.
10. Llame [**a IMFSinkWriter::WriteSample**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-writesample) para enviar el ejemplo multimedia al escritor receptor.

## <a name="write-the-main-function"></a>Escritura de la función main

Dentro de `main` la función , realice los pasos siguientes.

1.  Llame [**a CoInitializeEx para**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) inicializar la biblioteca COM.
2.  Llame [**a MFStartup para**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) inicializar Microsoft Media Foundation.
3.  Cree el escritor del receptor.
4.  Enviar fotogramas de vídeo al escritor receptor.
5.  Llame [**a IMFSinkWriter::Finalize para**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsinkwriter-finalize) finalizar el archivo de salida.
6.  Suelte el puntero al sistema de escritura del receptor.
7.  Llame [**a MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown).
8.  Llame [**a CoUninitialize.**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)


```C++
void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="example-code"></a>Código de ejemplo

El código siguiente muestra el programa completo.


```C++
#include <Windows.h>
#include <mfapi.h>
#include <mfidl.h>
#include <Mfreadwrite.h>
#include <mferror.h>

#pragma comment(lib, "mfreadwrite")
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mfuuid")

template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

// Format constants
const UINT32 VIDEO_WIDTH = 640;
const UINT32 VIDEO_HEIGHT = 480;
const UINT32 VIDEO_FPS = 30;
const UINT64 VIDEO_FRAME_DURATION = 10 * 1000 * 1000 / VIDEO_FPS;
const UINT32 VIDEO_BIT_RATE = 800000;
const GUID   VIDEO_ENCODING_FORMAT = MFVideoFormat_WMV3;
const GUID   VIDEO_INPUT_FORMAT = MFVideoFormat_RGB32;
const UINT32 VIDEO_PELS = VIDEO_WIDTH * VIDEO_HEIGHT;
const UINT32 VIDEO_FRAME_COUNT = 20 * VIDEO_FPS;

// Buffer to hold the video frame data.
DWORD videoFrameBuffer[VIDEO_PELS];

HRESULT InitializeSinkWriter(IMFSinkWriter **ppWriter, DWORD *pStreamIndex)
{
    *ppWriter = NULL;
    *pStreamIndex = NULL;

    IMFSinkWriter   *pSinkWriter = NULL;
    IMFMediaType    *pMediaTypeOut = NULL;   
    IMFMediaType    *pMediaTypeIn = NULL;   
    DWORD           streamIndex;     

    HRESULT hr = MFCreateSinkWriterFromURL(L"output.wmv", NULL, NULL, &pSinkWriter);

    // Set the output media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeOut);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetGUID(MF_MT_SUBTYPE, VIDEO_ENCODING_FORMAT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_AVG_BITRATE, VIDEO_BIT_RATE);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeOut->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeOut, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeOut, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->AddStream(pMediaTypeOut, &streamIndex);   
    }

    // Set the input media type.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateMediaType(&pMediaTypeIn);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_MAJOR_TYPE, MFMediaType_Video);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetGUID(MF_MT_SUBTYPE, VIDEO_INPUT_FORMAT);     
    }
    if (SUCCEEDED(hr))
    {
        hr = pMediaTypeIn->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(pMediaTypeIn, MF_MT_FRAME_SIZE, VIDEO_WIDTH, VIDEO_HEIGHT);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_FRAME_RATE, VIDEO_FPS, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(pMediaTypeIn, MF_MT_PIXEL_ASPECT_RATIO, 1, 1);   
    }
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->SetInputMediaType(streamIndex, pMediaTypeIn, NULL);   
    }

    // Tell the sink writer to start accepting data.
    if (SUCCEEDED(hr))
    {
        hr = pSinkWriter->BeginWriting();
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppWriter = pSinkWriter;
        (*ppWriter)->AddRef();
        *pStreamIndex = streamIndex;
    }

    SafeRelease(&pSinkWriter);
    SafeRelease(&pMediaTypeOut);
    SafeRelease(&pMediaTypeIn);
    return hr;
}

HRESULT WriteFrame(
    IMFSinkWriter *pWriter, 
    DWORD streamIndex, 
    const LONGLONG& rtStart        // Time stamp.
    )
{
    IMFSample *pSample = NULL;
    IMFMediaBuffer *pBuffer = NULL;

    const LONG cbWidth = 4 * VIDEO_WIDTH;
    const DWORD cbBuffer = cbWidth * VIDEO_HEIGHT;

    BYTE *pData = NULL;

    // Create a new memory buffer.
    HRESULT hr = MFCreateMemoryBuffer(cbBuffer, &pBuffer);

    // Lock the buffer and copy the video frame to the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->Lock(&pData, NULL, NULL);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCopyImage(
            pData,                      // Destination buffer.
            cbWidth,                    // Destination stride.
            (BYTE*)videoFrameBuffer,    // First row in source image.
            cbWidth,                    // Source stride.
            cbWidth,                    // Image width in bytes.
            VIDEO_HEIGHT                // Image height in pixels.
            );
    }
    if (pBuffer)
    {
        pBuffer->Unlock();
    }

    // Set the data length of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pBuffer->SetCurrentLength(cbBuffer);
    }

    // Create a media sample and add the buffer to the sample.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateSample(&pSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->AddBuffer(pBuffer);
    }

    // Set the time stamp and the duration.
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleTime(rtStart);
    }
    if (SUCCEEDED(hr))
    {
        hr = pSample->SetSampleDuration(VIDEO_FRAME_DURATION);
    }

    // Send the sample to the Sink Writer.
    if (SUCCEEDED(hr))
    {
        hr = pWriter->WriteSample(streamIndex, pSample);
    }

    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}

void main()
{
    // Set all pixels to green
    for (DWORD i = 0; i < VIDEO_PELS; ++i)
    {
        videoFrameBuffer[i] = 0x0000FF00;
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            IMFSinkWriter *pSinkWriter = NULL;
            DWORD stream;

            hr = InitializeSinkWriter(&pSinkWriter, &stream);
            if (SUCCEEDED(hr))
            {
                // Send frames to the sink writer.
                LONGLONG rtStart = 0;


                for (DWORD i = 0; i < VIDEO_FRAME_COUNT; ++i)
                {
                    hr = WriteFrame(pSinkWriter, stream, rtStart);
                    if (FAILED(hr))
                    {
                        break;
                    }
                    rtStart += VIDEO_FRAME_DURATION;
                }
            }
            if (SUCCEEDED(hr))
            {
                hr = pSinkWriter->Finalize();
            }
            SafeRelease(&pSinkWriter);
            MFShutdown();
        }
        CoUninitialize();
    }
}
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Escritor de receptores](sink-writer.md)
</dt> </dl>

 

 
