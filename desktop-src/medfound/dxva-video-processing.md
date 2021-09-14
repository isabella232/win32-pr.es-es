---
description: El procesamiento de vídeo DXVA encapsula las funciones del hardware gráfico dedicado al procesamiento de imágenes de vídeo sin comprimir. Los servicios de procesamiento de vídeo incluyen desinterlazado y combinación de vídeo.
ms.assetid: bd688f81-4b7c-4016-b0bd-e40782131f8e
title: Procesamiento de vídeo DXVA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5058d93ddd7c506a501eb6ca07c4661755fc8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252495"
---
# <a name="dxva-video-processing"></a>Procesamiento de vídeo DXVA

El procesamiento de vídeo DXVA encapsula las funciones del hardware gráfico dedicado al procesamiento de imágenes de vídeo sin comprimir. Los servicios de procesamiento de vídeo incluyen desinterlazado y combinación de vídeo.

Este tema contiene las siguientes secciones:

-   [Información general](#overview)
-   [Creación de un dispositivo de procesamiento de vídeo](#creating-a-video-processing-device)
    -   [Obtener el puntero IDirectXVideoProcessorService](#get-the-idirectxvideoprocessorservice-pointer)
    -   [Enumerar los dispositivos de procesamiento de vídeo](#enumerate-the-video-processing-devices)
    -   [Enumerar Render-Target formatos](#enumerate-render-target-formats)
    -   [Consulta de las funcionalidades del dispositivo](#query-the-device-capabilities)
    -   [Creación del dispositivo](#create-the-device)
-   [Vídeo proceso Blit](#video-process-blit)
    -   [Parámetros de Blit](#blit-parameters)
    -   [Ejemplos de entrada](#input-samples)
-   [Composición de imágenes](#image-composition)
    -   [Ejemplo 1: Letterboxing](#example-1-letterboxing)
    -   [Ejemplo 2: Stretching Substream Images](#example-2-stretching-substream-images)
    -   [Ejemplo 3: Alturas de flujo no coincidentes](#example-3-mismatched-stream-heights)
    -   [Ejemplo 4: Rectángulo de destino menor que la superficie de destino](#example-4-target-rectangle-smaller-than-destination-surface)
    -   [Ejemplo 5: Rectángulos de origen](#example-5-source-rectangles)
    -   [Ejemplo 6: Intersección de rectángulos de destino](#example-6-intersecting-destination-rectangles)
    -   [Ejemplo 7: Stretching and Cropping Video](#example-7-stretching-and-cropping-video)
-   [Orden de ejemplo de entrada](#input-sample-order)
    -   [Ejemplo 1](#example-1-letterboxing)
    -   [Ejemplo 2](#example-2-stretching-substream-images)
    -   [Ejemplo 3](#example-3-mismatched-stream-heights)
    -   [Ejemplo 4](#example-4-target-rectangle-smaller-than-destination-surface)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

El hardware gráfico puede usar la unidad de procesamiento gráfico (GPU) para procesar imágenes de vídeo sin comprimir. Un *dispositivo de procesamiento* de vídeo es un componente de software que encapsula estas funciones. Las aplicaciones pueden usar un dispositivo de procesamiento de vídeo para realizar funciones como:

-   Desinterlazado y televisa inversa
-   Mezcla de subproyecciones de vídeo en la imagen de vídeo principal
-   Ajuste de color (ProcAmp) y filtrado de imágenes
-   Escalado de imagen
-   Conversión de espacio de color
-   Combinación alfa

En el diagrama siguiente se muestran las fases de la canalización de procesamiento de vídeo. El diagrama no está diseñado para mostrar una implementación real. Por ejemplo, el controlador de gráficos podría combinar varias fases en una sola operación. Todas estas operaciones se pueden realizar en una sola llamada al dispositivo de procesamiento de vídeo. Es posible que algunas fases que se muestran aquí, como el filtrado de ruido y detalles, no sean compatibles con el controlador.

![diagrama que muestra las fases del procesamiento de vídeo dxva.](images/8581554e-a1bc-4cab-9ae1-99a6537e2a84.gif)

La entrada a la canalización de procesamiento de vídeo siempre incluye una *secuencia de* vídeo principal, que contiene los datos de la imagen principal. La secuencia de vídeo principal determina la velocidad de fotogramas del vídeo de salida. Cada fotograma del vídeo de salida se calcula en relación con los datos de entrada de la secuencia de vídeo principal. Los píxeles de la secuencia principal siempre son opacos, sin datos alfa por píxel. La secuencia de vídeo principal puede ser progresiva o entrelazada.

Opcionalmente, la canalización de procesamiento de vídeo puede recibir hasta 15 subproducciones de vídeo. Una sub secuencia contiene datos de imagen auxiliares, como subtítulos o subapicciones de DVD. Estas imágenes se muestran a través de la secuencia de vídeo principal y, por lo general, no están pensadas para mostrarse por sí mismas. Las imágenes de subtransmisión pueden contener datos alfa por píxel y siempre son fotogramas progresivas. El dispositivo de procesamiento de vídeo combina alfa las imágenes de subtransmisión con el marco desenlazado actual de la secuencia de vídeo principal.

En el resto de este tema, el término *imagen* se usa para los datos de entrada en un dispositivo de procesamiento de vídeo. Una imagen puede constar de un marco progresiva, un solo campo o dos campos intercalados. La salida siempre es un marco desenlazado.

Un controlador de vídeo puede implementar más de un dispositivo de procesamiento de vídeo para proporcionar diferentes conjuntos de funcionalidades de procesamiento de vídeo. Los dispositivos se identifican mediante GUID. Los siguientes GUID están predefinidos:

-   **DXVA2 \_ VideoProcBobDevice**. Este dispositivo realiza el desinterlazado bob.
-   **DXVA2 \_ VideoProcProgressiveDevice**. Este dispositivo se usa si el vídeo solo contiene fotogramas progresivas, sin fotogramas entrelazados. (Algunos contenidos de vídeo contienen una combinación de fotogramas progresivas e entrelazados. El dispositivo progresiva no se puede usar para este tipo de contenido de vídeo "mixto", porque se requiere un paso de desenlazado para los fotogramas entrelazados).

Todos los controladores gráficos que admiten el procesamiento de vídeo DXVA deben implementar al menos estos dos dispositivos. El controlador de gráficos también puede proporcionar otros dispositivos, que se identifican mediante GUID específicos del controlador. Por ejemplo, un controlador podría implementar un algoritmo de desinterlazado propietario que genera una salida de mejor calidad que el desinterlazado bob. Algunos algoritmos de desinteresado pueden requerir imágenes de referencia hacia delante o hacia atrás de la secuencia principal. Si es así, el autor de la llamada debe proporcionar estas imágenes al controlador en la secuencia correcta, como se describe más adelante en esta sección.

También se proporciona un dispositivo de software de referencia. El dispositivo de software está optimizado para la calidad en lugar de la velocidad y puede que no sea adecuado para el procesamiento de vídeo en tiempo real. El dispositivo de software de referencia usa el valor GUID DXVA2 \_ VideoProcSoftwareDevice.

## <a name="creating-a-video-processing-device"></a>Creación de un dispositivo de procesamiento de vídeo

Antes de usar el procesamiento de vídeo DXVA, la aplicación debe crear un dispositivo de procesamiento de vídeo. Este es un breve esquema de los pasos, que se explican con más detalle en el resto de esta sección:

1.  Obtenga un puntero a la [**interfaz IDirectXVideoProcessorService.**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
2.  Cree una descripción del formato de vídeo para la secuencia de vídeo principal. Use esta descripción para obtener una lista de los dispositivos de procesamiento de vídeo que admiten el formato de vídeo. Los dispositivos se identifican mediante GUID.
3.  Para un dispositivo determinado, obtenga una lista de formatos de destino de representación admitidos por el dispositivo. Los formatos se devuelven como una lista de **valores D3DFORMAT.** Si tiene previsto mezclar substreams, obtenga también una lista de los formatos de subtransmisión admitidos.
4.  Consulte las funcionalidades de cada dispositivo.
5.  Cree el dispositivo de procesamiento de vídeo.

A veces puede omitir algunos de estos pasos. Por ejemplo, en lugar de obtener la lista de formatos de destino de representación, simplemente podría intentar crear el dispositivo de procesamiento de vídeo con el formato que prefiera y ver si se realiza correctamente. Es probable que un formato común, como D3DFMT \_ X8R8G8B8, tenga éxito.

En el resto de esta sección se describen estos pasos en detalle.

### <a name="get-the-idirectxvideoprocessorservice-pointer"></a>Obtener el puntero IDirectXVideoProcessorService

La [**interfaz IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) se obtiene del dispositivo Direct3D. Hay dos maneras de obtener un puntero a esta interfaz:

-   Desde un dispositivo Direct3D.
-   Desde la [Administrador de dispositivos Direct3D.](direct3d-device-manager.md)

Si tiene un puntero a un dispositivo Direct3D, puede obtener un puntero [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) llamando a la [**función DXVA2CreateVideoService.**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) Pase un puntero a la interfaz **IDirect3DDevice9** del dispositivo y especifique **\_ IID IDirectXVideoProcessorService** para el *parámetro riid,* como se muestra en el código siguiente:


```C++
    // Create the DXVA-2 Video Processor service.
    hr = DXVA2CreateVideoService(g_pD3DD9, IID_PPV_ARGS(&g_pDXVAVPS));
```



n algunos casos, un objeto crea el dispositivo Direct3D y, a continuación, lo comparte con otros objetos a través del Administrador de dispositivos [.](direct3d-device-manager.md) En esta situación, puede llamar a [**IDirect3DDeviceManager9::GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) en el administrador de dispositivos para obtener el puntero [**IDirectXVideoProcessorService,**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) como se muestra en el código siguiente:


```C++
HRESULT GetVideoProcessorService(
    IDirect3DDeviceManager9 *pDeviceManager,
    IDirectXVideoProcessorService **ppVPService
    )
{
    *ppVPService = NULL;

    HANDLE hDevice;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    if (SUCCEEDED(hr))
    {
        // Get the video processor service 
        HRESULT hr2 = pDeviceManager->GetVideoService(
            hDevice, 
            IID_PPV_ARGS(ppVPService)
            );

        // Close the device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (FAILED(hr2))
        {
            hr = hr2;
        }
    }

    if (FAILED(hr))
    {
        SafeRelease(ppVPService);
    }

    return hr;
}
```



### <a name="enumerate-the-video-processing-devices"></a>Enumerar los dispositivos de procesamiento de vídeo

Para obtener una lista de dispositivos de procesamiento de vídeo, rellene una estructura [**\_ DXVA2 VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) con el formato de la secuencia de vídeo principal y pase esta estructura al método [**IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) El método devuelve una matriz de GUID, una para cada dispositivo de procesamiento de vídeo que se puede usar con este formato de vídeo.

Considere una aplicación que representa una secuencia de vídeo en formato YUY2, mediante la definición BT.709 del color YUV, con una velocidad de fotogramas de 29,97 fotogramas por segundo. Suponga que el contenido del vídeo consta completamente de fotogramas progresivas. El siguiente fragmento de código muestra cómo rellenar la descripción del formato y obtener los GUID del dispositivo:


```C++
    // Initialize the video descriptor.

    g_VideoDesc.SampleWidth                         = VIDEO_MAIN_WIDTH;
    g_VideoDesc.SampleHeight                        = VIDEO_MAIN_HEIGHT;
    g_VideoDesc.SampleFormat.VideoChromaSubsampling = DXVA2_VideoChromaSubsampling_MPEG2;
    g_VideoDesc.SampleFormat.NominalRange           = DXVA2_NominalRange_16_235;
    g_VideoDesc.SampleFormat.VideoTransferMatrix    = EX_COLOR_INFO[g_ExColorInfo][0];
    g_VideoDesc.SampleFormat.VideoLighting          = DXVA2_VideoLighting_dim;
    g_VideoDesc.SampleFormat.VideoPrimaries         = DXVA2_VideoPrimaries_BT709;
    g_VideoDesc.SampleFormat.VideoTransferFunction  = DXVA2_VideoTransFunc_709;
    g_VideoDesc.SampleFormat.SampleFormat           = DXVA2_SampleProgressiveFrame;
    g_VideoDesc.Format                              = VIDEO_MAIN_FORMAT;
    g_VideoDesc.InputSampleFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.InputSampleFreq.Denominator         = 1;
    g_VideoDesc.OutputFrameFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.OutputFrameFreq.Denominator         = 1;

    // Query the video processor GUID.

    UINT count;
    GUID* guids = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorDeviceGuids(&g_VideoDesc, &count, &guids);
```



El código de este ejemplo se toma del ejemplo del SDK [de \_ VideoProc de DXVA2.](dxva2-videoproc-sample.md)

El método [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) asigna la matriz *pGuids* de este ejemplo, por lo que la aplicación debe liberar la matriz llamando a [**CoTaskMemFree.**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) Los pasos restantes se pueden realizar mediante cualquiera de los GUID de dispositivo devueltos por este método.

### <a name="enumerate-render-target-formats"></a>Enumerar Render-Target formatos

Para obtener la lista de formatos de destino de representación admitidos por el dispositivo, pase el GUID del dispositivo y la estructura [**\_ VideoDesc de DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) al método [**IDirectXVideoProcessorService::GetVideoProcessorRenderTargets,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) como se muestra en el código siguiente:


```C++
    // Query the supported render-target formats.

    UINT i, count;
    D3DFORMAT* formats = NULL;

    HRESULT hr = g_pDXVAVPS->GetVideoProcessorRenderTargets(
        guid, &g_VideoDesc, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorRenderTargets failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_RENDER_TARGET_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the render-target format.\n"));
        return FALSE;
    }
```



El método devuelve una matriz de **valores D3DFORMAT.** En este ejemplo, donde el tipo de entrada es YUY2, una lista típica de formatos podría ser D3DFMT \_ X8R8G8B8 (RGB de 32 bits) y D3DMFT \_ YUY2 (el formato de entrada). Sin embargo, la lista exacta dependerá del controlador.

La lista de formatos disponibles para las sub secuencias puede variar en función del formato de destino de representación y el formato de entrada. Para obtener la lista de formatos de subtransmisión, pase el GUID del dispositivo, la estructura de formato y el formato de destino de representación al método [**IDirectXVideoProcessorService::GetVideoProcessorSubStreamFormats,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) como se muestra en el código siguiente:


```C++
    // Query the supported substream formats.

    formats = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorSubStreamFormats(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorSubStreamFormats failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_SUB_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the substream format.\n"));
        return FALSE;
    }
```



Este método devuelve otra matriz de **valores D3DFORMAT.** Los formatos típicos de substream son AYUV y AI44.

### <a name="query-the-device-capabilities"></a>Consulta de las funcionalidades del dispositivo

Para obtener las funcionalidades de un dispositivo determinado, pase el GUID del dispositivo, la estructura de formato y un formato de destino de representación al método [**IDirectXVideoProcessorService::GetVideoProcessorCaps.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) El método rellena una estructura [**DxVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) con las funcionalidades del dispositivo.


```C++
    // Query video processor capabilities.

    hr = g_pDXVAVPS->GetVideoProcessorCaps(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &g_VPCaps);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorCaps failed: 0x%x.\n", hr));
        return FALSE;
    }
```



### <a name="create-the-device"></a>Creación del dispositivo

Para crear el dispositivo de procesamiento de vídeo, llame a [**IDirectXVideoProcessorService::CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor). La entrada a este método es el GUID del dispositivo, la descripción del formato, el formato render-target y el número máximo de substreams que planea mezclar. El método devuelve un puntero a la [**interfaz IDirectXVideoProcessor,**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) que representa el dispositivo de procesamiento de vídeo.


```C++
    // Finally create a video processor device.

    hr = g_pDXVAVPS->CreateVideoProcessor(
        guid,
        &g_VideoDesc,
        VIDEO_RENDER_TARGET_FORMAT,
        SUB_STREAM_COUNT,
        &g_pDXVAVPD
        );
```



## <a name="video-process-blit"></a>Vídeo proceso Blit

La operación principal de procesamiento de vídeo es el *procesamiento de vídeo blit*. (Una *blit es* cualquier operación que combina dos o más mapas de bits en un solo mapa de bits. Un archivo blit de procesamiento de vídeo combina imágenes de entrada para crear un marco de salida). Para realizar un procesamiento de vídeo blit, llame a [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt). Este método pasa un conjunto de ejemplos de vídeo al dispositivo de procesamiento de vídeo. En respuesta, el dispositivo de procesamiento de vídeo procesa las imágenes de entrada y genera un fotograma de salida. El procesamiento puede incluir desinteresado, conversión de espacio de color y combinación de substream. La salida se escribe en una superficie de destino proporcionada por el autor de la llamada.

El [**método VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) toma los parámetros siguientes:

-   *pRT* apunta a una superficie de destino de representación **IDirect3DSurface9** que recibirá el fotograma de vídeo procesado.
-   *pBltParams apunta* a una estructura [**\_ VideoProcessBltParams de DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) que especifica los parámetros para la blit.
-   *pSamples es* la dirección de una matriz de [**estructuras de DXVA2 \_ VideoSample.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) Estas estructuras contienen los ejemplos de entrada para la blit.
-   *NumSamples proporciona* el tamaño de la *matriz pSamples.*
-   El *parámetro Reservado* está reservado y debe establecerse en **NULL.**

En la *matriz pSamples,* el autor de la llamada debe proporcionar los siguientes ejemplos de entrada:

-   Imagen actual de la secuencia de vídeo principal.
-   Las imágenes de referencia hacia delante y hacia atrás, si lo requiere el algoritmo de desinterlazado.
-   Cero o más imágenes de substream, hasta un máximo de 15 substreams.

El controlador espera que esta matriz esté en un orden determinado, como se describe en Input [Sample Order](#input-sample-order).

### <a name="blit-parameters"></a>Parámetros de Blit

La [**estructura \_ VideoProcessBltParams de DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) contiene parámetros generales para blit. Los parámetros más importantes se almacenan en los siguientes miembros de la estructura :

-   **TargetFrame** es el tiempo de presentación del marco de salida. Para el contenido progresiva, esta hora debe ser igual a la hora de inicio del fotograma actual de la secuencia de vídeo principal. Esta hora se especifica en el miembro **Start** de la [**estructura DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) para ese ejemplo de entrada.

    Para el contenido entrelazado, un marco con dos campos intercalados genera dos marcos de salida desenlazados. En el primer fotograma de salida, el tiempo de presentación debe ser igual a la hora de inicio de la imagen actual en la secuencia de vídeo principal, igual que el contenido progresiva. En el segundo marco de salida, la hora de inicio debe ser igual al punto medio entre la hora de inicio de la imagen actual en la secuencia de vídeo principal y la hora de inicio de la siguiente imagen de la secuencia. Por ejemplo, si el vídeo de entrada es de 25 fotogramas por segundo (50 campos por segundo), los fotogramas de salida tendrán las marcas de tiempo que se muestran en la tabla siguiente. Las marcas de tiempo se muestran en unidades de 100 nanosegundos.

    

    | Imagen de entrada | **TargetFrame** (1) | **TargetFrame** (2) |
    |---------------|---------------------|---------------------|
    | 0             | 0                   | 200000              |
    | 400000        | 0                   | 600000              |
    | 800000        | 800000              | 1000000             |
    | 1200000       | 1200000             | 1400000             |

    

     

    Si el contenido entrelazado consta de campos individuales en lugar de campos intercalados, las horas de salida siempre coinciden con los tiempos de entrada, como con el contenido progresiva.

-   **TargetRect define** una región rectangular dentro de la superficie de destino. La blit escribirá la salida en esta región. En concreto, cada píxel dentro de **TargetRect** se modificará y no se modificará ningún píxel fuera de **TargetRect.** El rectángulo de destino define el rectángulo delimitador para todas las secuencias de vídeo de entrada. La colocación de secuencias individuales dentro de ese rectángulo se controla mediante el *parámetro pSamples* de [**IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).
-   **BackgroundColor** proporciona el color del fondo siempre que no aparezca ninguna imagen de vídeo. Por ejemplo, cuando se muestra una imagen de vídeo de 16 x 9 dentro de un área de 4 x 3 (letterboxing), las regiones con cuadro de letras se muestran con el color de fondo. El color de fondo solo se aplica dentro del rectángulo de destino (**TargetRect**). Los píxeles fuera **de TargetRect** no se modifican.
-   **DestFormat** describe el espacio de color del vídeo de salida, por ejemplo, si se usa el color BT.709 o BT.601 de ITU-R. Esta información puede afectar a cómo se muestra la imagen. Para obtener más información, vea [Información de color extendida](extended-color-information.md).

En la página de referencia de la estructura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) se describen otros parámetros.

### <a name="input-samples"></a>Ejemplos de entrada

El *parámetro pSamples* [**de IDirectXVideoProcessor::VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) apunta a una matriz de estructuras [**DXVA2 \_ VideoSample.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) Cada una de estas estructuras contiene información sobre una muestra de entrada y un puntero a la superficie de Direct3D que contiene la muestra. Cada ejemplo es uno de los siguientes:

-   Imagen actual de la secuencia principal.
-   Imagen de referencia hacia delante o hacia atrás de la secuencia principal, que se usa para desenlazar.
-   Imagen de substream.

El orden exacto en el que los ejemplos deben aparecer en la matriz se describe más adelante, en la sección [Input Sample Order](#input-sample-order).

Se pueden proporcionar hasta 15 imágenes de subtransmisión, aunque la mayoría de las aplicaciones de vídeo solo necesitan una subtransmisión, como máximo. El número de substreams puede cambiar con cada llamada a [**VideoProcessBlt.**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) Las imágenes de subtransmisión se indican estableciendo el miembro **SampleFormat.SampleFormat** de la estructura [**\_ DXVA2 VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) igual a DXVA2 \_ SampleSubStream. Para la secuencia de vídeo principal, este miembro describe el entrelazado del vídeo de entrada. Para obtener más información, vea [**Enumeración \_ SampleFormat de DXVA2.**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat)

Para la secuencia de vídeo principal, los miembros **Start** y **End** de la estructura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) dan las horas de inicio y finalización del ejemplo de entrada. Para las imágenes de subtransmisión, establezca estos valores en cero, ya que el tiempo de presentación siempre se calcula a partir de la secuencia principal. La aplicación es responsable de realizar un seguimiento de cuándo se debe presentar cada imagen de subtransmisión y enviarla a [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) en el momento adecuado.

Dos rectángulos definen cómo se coloca el vídeo de origen para cada secuencia:

-   El **miembro SrcRect** de la estructura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) especifica el rectángulo de origen *,* una región rectangular de la imagen de origen que aparecerá en el marco de salida compuesto. Para recortar la imagen, establezca esta opción en un valor menor que el tamaño del marco. De lo contrario, estar debe ser igual al tamaño del marco.
-   El **miembro DstRect** de la misma estructura especifica el rectángulo de destino *,* una región rectangular de la superficie de destino donde aparecerá el marco de vídeo.

El controlador divide los píxeles del rectángulo de origen en el rectángulo de destino. Los dos rectángulos pueden tener diferentes tamaños o relaciones de aspecto; el controlador escalará la imagen según sea necesario. Además, cada flujo de entrada puede usar un factor de escalado diferente. De hecho, el escalado puede ser necesario para generar la relación de aspecto correcta en el marco de salida. El controlador no tiene en cuenta la relación de aspecto de píxeles del origen, por lo que si la imagen de origen usa píxeles no cuadrados, es responsabilidad de la aplicación calcular el rectángulo de destino correcto.

Los formatos de substream preferidos son AYUV y AI44. El último es un formato de paleta con 16 colores. Las entradas de paleta se especifican en el **miembro Pal** de la [**estructura DXVA2 \_ VideoSample.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) (Si el formato de vídeo de origen se expresa originalmente como un tipo Media Foundation multimedia, las entradas de la paleta se almacenan en el atributo [**MF \_ MT \_ PALETTE).**](mf-mt-palette-attribute.md) En el caso de los formatos sin paleta, desactive esta matriz en cero.

## <a name="image-composition"></a>Composición de imágenes

Cada operación blit se define mediante los tres rectángulos siguientes:

-   El *rectángulo de* destino **(TargetRect)** define la región dentro de la superficie de destino donde aparecerá la salida. La imagen de salida se recorta a este rectángulo.
-   El *rectángulo* de destino para cada secuencia (**DstRect**) define dónde aparece el flujo de entrada en la imagen compuesta.
-   El *rectángulo* de origen de cada secuencia (**SrcRect**) define qué parte de la imagen de origen aparece.

Los rectángulos de destino y destino se especifican en relación con la superficie de destino. El rectángulo de origen se especifica en relación con la imagen de origen. Todos los rectángulos se especifican en píxeles.

![diagrama que muestra rectángulos de origen, destino y destino](images/dxva-vp-rects.gif)

El dispositivo de procesamiento de vídeo alfa combina las imágenes de entrada con cualquiera de los siguientes orígenes de datos alfa:

-   Datos alfa por píxel de substreams.
-   Valor alfa planar para cada secuencia de vídeo, especificado en el **miembro PlanarAlpha** de la [**estructura \_ DXVA2 VideoSample.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample)
-   Valor alfa planar de la imagen compuesta, especificado en el **miembro Alpha** de la estructura [**\_ DXVA2 VideoProcessBltParams.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) Este valor se usa para combinar toda la imagen compuesta con el color de fondo.

En esta sección se proporciona una serie de ejemplos que muestran cómo el dispositivo de procesamiento de vídeo crea la imagen de salida.

### <a name="example-1-letterboxing"></a>Ejemplo 1: Letterboxing

En este ejemplo se muestra cómo crear una caja de letras de la imagen de origen estableciendo el rectángulo de destino en menor que el rectángulo de destino. La secuencia de vídeo principal de este ejemplo es una imagen de 720 × 480 y está pensada para mostrarse con una relación de aspecto de 16:9. La superficie de destino es de 640 × 480 píxeles (relación de aspecto de 4:3). Para lograr la relación de aspecto correcta, el rectángulo de destino debe ser 640 × 360. Por motivos de simplicidad, este ejemplo no incluye una substream. En el diagrama siguiente se muestran los rectángulos de origen y destino.

![diagrama en el que se muestra la creación de letterboxing.](images/428105fa-a26b-48a6-991d-44d24ab786b1.gif)

En el diagrama anterior se muestran los rectángulos siguientes:

-   Rectángulo de destino: { 0, 0, 640, 480 }
-   Vídeo principal:

    -   Rectángulo de origen: { 0, 0, 720, 480 }
    -   Rectángulo de destino: { 0, 60, 640, 420 }

El controlador desinterlará el vídeo, reducirá el marco desenlazado a 640 × 360 y cortará el marco en el rectángulo de destino. El rectángulo de destino es mayor que el rectángulo de destino, por lo que el controlador usará el color de fondo para rellenar las barras horizontales encima y debajo del marco. El color de fondo se especifica en la [**estructura \_ DXVA2 VideoProcessBltParams.**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams)

### <a name="example-2-stretching-substream-images"></a>Ejemplo 2: Stretching Substream Images

Las imágenes de subtransmisión pueden extenderse más allá de la imagen de vídeo principal. En el vídeo de DVD, por ejemplo, la secuencia de vídeo principal puede tener una relación de aspecto 4:3, mientras que la subtransmisión es 16:9. En este ejemplo, ambas secuencias de vídeo tienen las mismas dimensiones de origen (720 × 480), pero la subtransmisión está pensada para mostrarse en una relación de aspecto de 16:9. Para lograr esta relación de aspecto, la imagen de subtransmisión se extiende horizontalmente. Los rectángulos de origen y destino se muestran en el diagrama siguiente.

![diagrama que muestra el stretch de la imagen de substream.](images/7ab31c65-06b9-4843-90b8-2f9fb6f6b20e.gif)

En el diagrama anterior se muestran los rectángulos siguientes:

-   Rectángulo de destino: { 0, 0, 854, 480 }
-   Vídeo principal:

    -   Rectángulo de origen: { 0, 0, 720, 480 }
    -   Rectángulo de destino: { 0, 107, 474, 480 }

-   Substream:
    -   Rectángulo de origen: { 0, 0, 720, 480 }
    -   Rectángulo de destino: { 0, 0, 854, 480 }

Estos valores conservan el alto de la imagen y escalan ambas imágenes horizontalmente. En las regiones donde aparecen ambas imágenes, se mezclan alfa. Cuando la imagen de substream se encuentra más allá del vídeo de las primarias, la subtransmisión se mezcla alfa con el color de fondo. Esta combinación alfa tiene en cuenta los colores modificados en el lado derecho del diagrama.

### <a name="example-3-mismatched-stream-heights"></a>Ejemplo 3: Alturas de flujo no coincidentes

En el ejemplo anterior, la subtransmisión y la secuencia principal tienen el mismo alto. Secuencias también pueden tener alturas no coincidentes, como se muestra en este ejemplo. Las áreas dentro del rectángulo de destino donde no aparece ningún vídeo se dibujan con el color de fondo( negro en este ejemplo). Los rectángulos de origen y destino se muestran en el diagrama siguiente.

![diagrama que muestra alturas de flujo no coincidentes,](images/0190a15a-d971-450f-90ed-ce5633e1069c.gif)

En el diagrama anterior se muestran los rectángulos siguientes:

-   Rectángulo de destino: { 0, 0, 150, 85 }
-   Vídeo principal:
    -   Rectángulo de origen: { 0, 0, 150, 50 }
    -   Rectángulo de destino: { 0, 17, 150, 67 }
-   Substream:
    -   Rectángulo de origen: { 0, 0, 100, 85 }
    -   Rectángulo de destino: { 25, 0, 125, 85 }

### <a name="example-4-target-rectangle-smaller-than-destination-surface"></a>Ejemplo 4: Rectángulo de destino menor que la superficie de destino

En este ejemplo se muestra un caso en el que el rectángulo de destino es menor que la superficie de destino.

![diagrama que muestra un blit en un rectángulo de destino.](images/360a85a3-333c-4b32-b8f7-1beb1e805921.gif)

En el diagrama anterior se muestran los rectángulos siguientes:

-   Superficie de destino: { 0, 0, 300, 200 }
-   Rectángulo de destino: { 0, 0, 150, 85 }
-   Vídeo principal:
    -   Rectángulo de origen: { 0, 0, 150, 50 }
    -   Rectángulo de destino: { 0, 17, 150, 67 }
-   Substream:
    -   Rectángulo de origen: { 0, 0, 100, 85 }
    -   Rectángulo de destino: { 25, 0, 125, 85 }

Los píxeles fuera del rectángulo de destino no se modifican, por lo que el color de fondo solo aparece dentro del rectángulo de destino. El área de puntos indica partes de la superficie de destino que no se ven afectadas por la blit.

### <a name="example-5-source-rectangles"></a>Ejemplo 5: Rectángulos de origen

Si especifica un rectángulo de origen más pequeño que la imagen de origen, el controlador cortará solo esa parte de la imagen. En este ejemplo, los rectángulos de origen especifican el cuadrante inferior derecho de la secuencia de vídeo principal y el cuadrante inferior izquierdo de la subdifusión (que se indica mediante marcas hash en el diagrama). Los rectángulos de destino tienen los mismos tamaños que los rectángulos de origen, por lo que el vídeo no se extiende. Los rectángulos de origen y destino se muestran en el diagrama siguiente.

![diagrama que muestra un blit de dos rectángulos de origen.](images/b1de4cc3-0155-40be-acac-b486e2af8c0d.gif)

En el diagrama anterior se muestran los rectángulos siguientes:

-   Rectángulo de destino: { 0, 0, 720, 576 }
-   Vídeo principal:
    -   Tamaño de la superficie de origen: { 0, 0, 720, 480 }
    -   Rectángulo de origen: { 360, 240, 720, 480 }
    -   Rectángulo de destino: { 0, 0, 360, 240 }
-   Substream:
    -   Tamaño de la superficie de origen: { 0, 0, 640, 576 }
    -   Rectángulo de origen: { 0, 288, 320, 576 }
    -   Rectángulo de destino: { 400, 0, 720, 288 }

### <a name="example-6-intersecting-destination-rectangles"></a>Ejemplo 6: Intersección de rectángulos de destino

Este ejemplo es similar al anterior, pero los rectángulos de destino se intersecan. Las dimensiones de superficie son las mismas que en el ejemplo anterior, pero los rectángulos de origen y destino no lo son. De nuevo, el vídeo se recorta pero no se extiende. Los rectángulos de origen y destino se muestran en el diagrama siguiente.

![diagrama que muestra rectángulos de destino en intersección.](images/fbe450cb-c84d-4110-9515-00f27601528e.gif)

En el diagrama anterior se muestran los rectángulos siguientes:

-   Rectángulo de destino: { 0, 0, 720, 576 }
-   Vídeo principal:
    -   Tamaño de la superficie de origen: { 0, 0, 720, 480 }
    -   Rectángulo de origen: { 260, 92, 720, 480 }
    -   Rectángulo de destino: { 0, 0, 460, 388 }
-   Substream:
    -   Tamaño de la superficie de origen: { 0, 0, 640, 576 }
    -   Rectángulo de origen: { 0, 0, 460, 388 }
    -   Rectángulo de destino: { 260, 188, 720, 576 }

### <a name="example-7-stretching-and-cropping-video"></a>Ejemplo 7: Stretching and Cropping Video

En este ejemplo, el vídeo se extiende y se recorta. Una región de 180 × 120 de cada secuencia se extiende para cubrir un área de 360 × 240 en el rectángulo de destino.

![diagrama que muestra la extensión y el recorte.](images/ce83529c-8545-492c-9d3e-ef221c30e326.gif)

En el diagrama anterior se muestran los rectángulos siguientes:

-   Rectángulo de destino: { 0, 0, 720, 480 }
-   Vídeo principal:
    -   Tamaño de la superficie de origen: { 0, 0, 360, 240 }
    -   Rectángulo de origen: { 180, 120, 360, 240 }
    -   Rectángulo de destino: { 0, 0, 360, 240 }
-   Substream:
    -   Tamaño de la superficie de origen: { 0, 0, 360, 240 }
    -   Rectángulo de origen: { 0, 0, 180, 120 }
    -   Rectángulo de destino: { 360, 240, 720, 480 }

## <a name="input-sample-order"></a>Orden de ejemplo de entrada

El *parámetro pSamples* del [**método VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) es un puntero a una matriz de ejemplos de entrada. Los ejemplos de la secuencia de vídeo principal aparecen primero, seguidos de imágenes de subtransmisión en orden Z. Los ejemplos deben colocarse en la matriz en el orden siguiente:

-   Los ejemplos de la secuencia de vídeo principal aparecen primero en la matriz, en orden temporal. Según el modo de desinteresado, el controlador puede requerir uno o varios ejemplos de referencia de la secuencia de vídeo principal. Los **miembros NumForwardRefSamples** y **NumBackwardRefSamples** de la estructura [**\_ VideoProcessorCaps de DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) especifican cuántos ejemplos de referencia hacia delante y hacia atrás se necesitan. El autor de la llamada debe proporcionar estos ejemplos de referencia incluso si el contenido del vídeo es progresiva y no requiere desenlazado. (Esto puede ocurrir cuando se entregan fotogramas progresivas a un dispositivo de desenlazado, por ejemplo, cuando el origen contiene una combinación de fotogramas entrelazados y progresivas).
-   Después de los ejemplos de la secuencia de vídeo principal, la matriz puede contener hasta 15 muestras de subtransmisión, organizadas en orden Z, de abajo a arriba. Las subrecciones siempre son progresivas y no requieren imágenes de referencia.

En cualquier momento, la secuencia de vídeo principal puede cambiar entre contenido entrelazado y progresiva, y el número de substreams puede cambiar.

El **miembro SampleFormat.SampleFormat** de la [**estructura DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) indica el tipo de imagen. Para las imágenes de substream, establezca este valor en DXVA2 \_ SampleSubStream. Para las imágenes progresivas, el valor es DXVA2 \_ SampleProgressiveFrame. Para las imágenes entrelazadas, el valor depende del diseño del campo.

Si el controlador requiere ejemplos de referencia hacia delante y hacia atrás, es posible que el número completo de muestras no esté disponible al principio de la secuencia de vídeo. En ese caso, incluya entradas para ellas en la matriz *pSamples,* pero marque los ejemplos que faltan como con el tipo DXVA2 \_ SampleUnknown.

Los **miembros Start** y **End** de la estructura VideoSample de [**DXVA2 \_**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) dan la ubicación temporal de cada ejemplo. Estos valores solo se usan para ejemplos de la secuencia de vídeo principal. En el caso de las imágenes de subtransmisión, establezca ambos miembros en cero.

Los ejemplos siguientes pueden ayudar a aclarar estos requisitos.

### <a name="example-1"></a>Ejemplo 1

El caso más sencillo se produce cuando no hay substreams y el algoritmo de desinterlazado no requiere ejemplos de referencia **(NumForwardRefSamples** y **NumBackwardRefSamples** son cero). El desenlace de Bob es un ejemplo de este tipo de algoritmo. En este caso, la *matriz pSamples* debe contener una sola superficie de entrada, como se muestra en la tabla siguiente.



| Índice           | Tipo de superficie        | Ubicación temporal |
|-----------------|---------------------|-------------------|
| *pSamples* \[ 0\] | Imagen entrelazada. | *T*               |



 

Se supone que *el valor de hora T* es la hora de inicio del fotograma de vídeo actual.

### <a name="example-2"></a>Ejemplo 2

En este ejemplo, la aplicación combina dos substreams con la secuencia principal. El algoritmo de desenlazado no requiere ejemplos de referencia. En la tabla siguiente se muestra cómo se organizan estos ejemplos en la *matriz pSamples.*



| Índice           | Tipo de superficie       | Ubicación temporal | Orden Z |
|-----------------|--------------------|-------------------|---------|
| *pSamples* \[ 0\] | Imagen entrelazada | *T*               | 0       |
| *pSamples* \[ 1\] | Substream          | 0                 | 1       |
| *pSamples* \[ 2\] | Substream          | 0                 | 2       |



 

### <a name="example-3"></a>Ejemplo 3

Ahora supongamos que el algoritmo de desenlace requiere una muestra de referencia hacia atrás y una muestra de referencia hacia delante. Además, se proporcionan dos imágenes de subdisección, para un total de cinco superficies. La ordenación correcta se muestra en la tabla siguiente.



| Índice           | Tipo de superficie                   | Ubicación temporal | Orden Z        |
|-----------------|--------------------------------|-------------------|----------------|
| *pSamples* \[ 0\] | Imagen entrelazada (referencia) | *T* -1            | No aplicable |
| *pSamples* \[ 1\] | Imagen entrelazada             | *T*               | 0              |
| *pSamples* \[ 2\] | Imagen entrelazada (referencia) | *T* +1            | No aplicable |
| *pSamples* \[ 3\] | Substream                      | 0                 | 1              |
| *pSamples* \[ 4\] | Substream                      | 0                 | 2              |



 

La hora *T* -1 es la hora de inicio del fotograma antes del marco actual y *T* +1 es la hora de inicio del fotograma siguiente.

Si la secuencia de vídeo cambia a contenido progresiva, con el mismo modo de desenlazado, la aplicación debe proporcionar el mismo número de muestras, como se muestra en la tabla siguiente.



| Índice           | Tipo de superficie                    | Ubicación temporal | Orden Z        |
|-----------------|---------------------------------|-------------------|----------------|
| *pSamples* \[ 0\] | Imagen progresiva (referencia) | *T* -1            | No aplicable |
| *pSamples* \[ 1\] | Imagen progresiva             | *T*               | 0              |
| *pSamples* \[ 2\] | Imagen progresiva (referencia) | *T* +1            | No aplicable |
| *pSamples* \[ 3\] | Substream                       | 0                 | 1              |
| *pSamples* \[ 4\] | Substream                       | 0                 | 2              |



 

### <a name="example-4"></a>Ejemplo 4

Al principio de una secuencia de vídeo, es posible que los ejemplos de referencia hacia delante y hacia atrás no estén disponibles. Cuando esto sucede, las entradas de los ejemplos que faltan se incluyen en la matriz *pSamples,* con el tipo de ejemplo DXVA2 \_ SampleUnknown.

Suponiendo que el modo de desenlace necesita un ejemplo de referencia hacia delante y otro hacia atrás, las tres primeras llamadas a [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) tendrían las secuencias de entradas que se muestran en las tres tablas siguientes.



| Índice           | Tipo de superficie                   | Ubicación temporal |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[ 0\] | Unknown                        | 0                 |
| *pSamples* \[ 1\] | Unknown                        | 0                 |
| *pSamples* \[ 2\] | Imagen entrelazada (referencia) | *T* +1            |



 



| Índice           | Tipo de superficie                   | Ubicación temporal |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[ 0\] | Unknown                        | 0                 |
| *pSamples* \[ 1\] | Imagen entrelazada             | *T*               |
| *pSamples* \[ 2\] | Imagen entrelazada (referencia) | *T* +1            |



 



| Índice           | Tipo de superficie                   | Ubicación temporal |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[ 0\] | Imagen entrelazada             | *T* -1            |
| *pSamples* \[ 1\] | Imagen entrelazada             | *T*               |
| *pSamples* \[ 2\] | Imagen entrelazada (referencia) | *T* +1            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aceleración de vídeo de DirectX 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Ejemplo de VideoProc de DXVA2 \_](dxva2-videoproc-sample.md)
</dt> </dl>

 

 
