---
description: El procesamiento de vídeo de DXVA encapsula las funciones del hardware de gráficos que están dedicadas a procesar imágenes de vídeo sin comprimir. Los servicios de procesamiento de vídeo incluyen desentrelazado y combinación de vídeo.
ms.assetid: bd688f81-4b7c-4016-b0bd-e40782131f8e
title: Procesamiento de vídeo de DXVA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5058d93ddd7c506a501eb6ca07c4661755fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539561"
---
# <a name="dxva-video-processing"></a>Procesamiento de vídeo de DXVA

El procesamiento de vídeo de DXVA encapsula las funciones del hardware de gráficos que están dedicadas a procesar imágenes de vídeo sin comprimir. Los servicios de procesamiento de vídeo incluyen desentrelazado y combinación de vídeo.

Este tema contiene las siguientes secciones:

-   [Información general](#overview)
-   [Creación de un dispositivo de procesamiento de vídeo](#creating-a-video-processing-device)
    -   [Obtener el puntero IDirectXVideoProcessorService](#get-the-idirectxvideoprocessorservice-pointer)
    -   [Enumerar los dispositivos de procesamiento de vídeo](#enumerate-the-video-processing-devices)
    -   [Enumerar formatos de Render-Target](#enumerate-render-target-formats)
    -   [Consultar las capacidades del dispositivo](#query-the-device-capabilities)
    -   [Crear el dispositivo](#create-the-device)
-   [Proceso de vídeo blit](#video-process-blit)
    -   [Parámetros de blit](#blit-parameters)
    -   [Ejemplos de entrada](#input-samples)
-   [Composición de imagen](#image-composition)
    -   [Ejemplo 1: panorámica](#example-1-letterboxing)
    -   [Ejemplo 2: expandir imágenes de subflujo](#example-2-stretching-substream-images)
    -   [Ejemplo 3: alto de flujo no coincidente](#example-3-mismatched-stream-heights)
    -   [Ejemplo 4: rectángulo de destino menor que la superficie de destino](#example-4-target-rectangle-smaller-than-destination-surface)
    -   [Ejemplo 5: rectángulos de origen](#example-5-source-rectangles)
    -   [Ejemplo 6: intersección de rectángulos de destino](#example-6-intersecting-destination-rectangles)
    -   [Ejemplo 7: expandir y recortar vídeo](#example-7-stretching-and-cropping-video)
-   [Orden de ejemplo de entrada](#input-sample-order)
    -   [Ejemplo 1](#example-1-letterboxing)
    -   [Ejemplo 2](#example-2-stretching-substream-images)
    -   [Ejemplo 3](#example-3-mismatched-stream-heights)
    -   [Ejemplo 4](#example-4-target-rectangle-smaller-than-destination-surface)
-   [Temas relacionados](#related-topics)

## <a name="overview"></a>Información general

El hardware gráfico puede usar la unidad de procesamiento de gráficos (GPU) para procesar imágenes de vídeo sin comprimir. Un dispositivo de *procesamiento de vídeo* es un componente de software que encapsula estas funciones. Las aplicaciones pueden usar un dispositivo de procesamiento de vídeo para realizar funciones como las siguientes:

-   Desentrelazado y Telecine inverso
-   Combinación de subsecuencias de vídeo en la imagen de vídeo principal
-   Ajuste de color (ProcAmp) y filtrado de imágenes
-   Escalado de imágenes
-   Conversión de espacio de colores
-   Combinación alfa

En el diagrama siguiente se muestran las fases de la canalización de procesamiento de vídeo. El diagrama no está diseñado para mostrar una implementación real. Por ejemplo, el controlador de gráficos puede combinar varias fases en una sola operación. Todas estas operaciones se pueden realizar en una única llamada al dispositivo de procesamiento de vídeo. Algunas de las fases que se muestran aquí, como el filtrado de ruido y detalles, pueden no ser compatibles con el controlador.

![diagrama que muestra las fases del procesamiento de vídeo de DXVA.](images/8581554e-a1bc-4cab-9ae1-99a6537e2a84.gif)

La entrada de la canalización de procesamiento de vídeo siempre incluye una secuencia de vídeo *principal* , que contiene los datos de imagen principales. La secuencia de vídeo principal determina la velocidad de fotogramas del vídeo de salida. Cada fotograma del vídeo de salida se calcula en relación con los datos de entrada de la secuencia de vídeo principal. Los píxeles del flujo principal siempre son opacos, sin datos alfa por píxel. La secuencia de vídeo principal puede ser progresiva o entrelazada.

Opcionalmente, la canalización de procesamiento de vídeo puede recibir hasta 15 subsecuencias de vídeo. Un subflujo contiene datos de imagen auxiliares, como subtítulos (CC) o subimágenes de DVD. Estas imágenes se muestran en el flujo de vídeo principal y, por lo general, no están pensadas para que se muestren por sí mismas. Las imágenes de subflujo pueden contener datos alfa por píxel y siempre son fotogramas progresivos. El dispositivo de procesamiento de vídeo alfa combina las imágenes de subflujo con el fotograma desentrelazado actual de la secuencia de vídeo principal.

En el resto de este tema, el término *imagen* se usa para los datos de entrada en un dispositivo de procesamiento de vídeo. Una imagen puede constar de un fotograma progresivo, un solo campo o dos campos intercalados. La salida siempre es un marco desentrelazado.

Un controlador de vídeo puede implementar más de un dispositivo de procesamiento de vídeo para proporcionar diferentes conjuntos de capacidades de procesamiento de vídeo. Los dispositivos se identifican mediante un GUID. Los siguientes GUID están predefinidos:

-   **DXVA2 \_ VideoProcBobDevice**. Este dispositivo realiza el desentrelazado de Bob.
-   **DXVA2 \_ VideoProcProgressiveDevice**. Este dispositivo se usa si el vídeo solo contiene fotogramas progresivos, sin fotogramas entrelazados. (Algunos contenidos de vídeo contienen una mezcla de fotogramas progresivos y entrelazados. No se puede usar el dispositivo progresivo para este tipo de contenido de vídeo "mixto", ya que se requiere un paso de desentrelazado para los fotogramas entrelazados).

Cada controlador de gráficos que admite el procesamiento de vídeo de DXVA debe implementar al menos estos dos dispositivos. El controlador de gráficos también puede proporcionar otros dispositivos, que se identifican mediante GUID específicos del controlador. Por ejemplo, un controlador podría implementar un algoritmo de desentrelazado de propiedad que genera una salida de mejor calidad que el desentrelazado de Bob. Algunos algoritmos de desentrelazado pueden requerir imágenes de referencia hacia delante o hacia atrás desde el flujo principal. Si es así, el autor de la llamada debe proporcionar estas imágenes al controlador en la secuencia correcta, tal y como se describe más adelante en esta sección.

También se proporciona un dispositivo de software de referencia. El dispositivo de software está optimizado para la calidad en lugar de la velocidad y puede no ser adecuado para el procesamiento de vídeo en tiempo real. El dispositivo de software de referencia usa el valor de GUID DXVA2 \_ VideoProcSoftwareDevice.

## <a name="creating-a-video-processing-device"></a>Creación de un dispositivo de procesamiento de vídeo

Antes de usar el procesamiento de vídeo de DXVA, la aplicación debe crear un dispositivo de procesamiento de vídeo. Esta es una breve descripción de los pasos, que se explican con mayor detalle en el resto de esta sección:

1.  Obtiene un puntero a la interfaz [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) .
2.  Cree una descripción del formato de vídeo para la secuencia de vídeo principal. Use esta descripción para obtener una lista de los dispositivos de procesamiento de vídeo que admiten el formato de vídeo. Los dispositivos se identifican mediante un GUID.
3.  Para un dispositivo determinado, obtenga una lista de formatos de destino de representación admitidos por el dispositivo. Los formatos se devuelven como una lista de valores de **D3DFORMAT** . Si tiene previsto mezclar subsecuencias, obtenga también una lista de los formatos de subflujo admitidos.
4.  Consultar las capacidades de cada dispositivo.
5.  Cree el dispositivo de procesamiento de vídeo.

En ocasiones, puede omitir algunos de estos pasos. Por ejemplo, en lugar de obtener la lista de formatos de destino de representación, puede intentar simplemente crear el dispositivo de procesamiento de vídeo con el formato que prefiera y ver si se ejecuta correctamente. Un formato común, como D3DFMT \_ X8R8G8B8, es probable que se realice correctamente.

En el resto de esta sección se describen estos pasos con detalle.

### <a name="get-the-idirectxvideoprocessorservice-pointer"></a>Obtener el puntero IDirectXVideoProcessorService

La interfaz [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) se obtiene del dispositivo Direct3D. Hay dos maneras de obtener un puntero a esta interfaz:

-   Desde un dispositivo Direct3D.
-   Desde la [Administrador de dispositivos de Direct3D](direct3d-device-manager.md).

Si tiene un puntero a un dispositivo Direct3D, puede obtener un puntero [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) llamando a la función [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) . Pase un puntero a la interfaz **IDirect3DDevice9** del dispositivo y especifique **IID \_ IDirectXVideoProcessorService** para el parámetro *riid* , tal y como se muestra en el código siguiente:


```C++
    // Create the DXVA-2 Video Processor service.
    hr = DXVA2CreateVideoService(g_pD3DD9, IID_PPV_ARGS(&g_pDXVAVPS));
```



en algunos casos, un objeto crea el dispositivo Direct3D y, a continuación, lo comparte con otros objetos a través del [Administrador de dispositivos de Direct3D](direct3d-device-manager.md). En esta situación, puede llamar a [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) en el administrador de dispositivos para obtener el puntero [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) , como se muestra en el código siguiente:


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

Para obtener una lista de dispositivos de procesamiento de vídeo, rellene una estructura [**DXVA2 \_ videodesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) con el formato de la secuencia de vídeo principal y pase esta estructura al método [**IDirectXVideoProcessorService:: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) . El método devuelve una matriz de GUID, uno para cada dispositivo de procesamiento de vídeo que se puede usar con este formato de vídeo.

Considere una aplicación que representa una secuencia de vídeo en formato YUY2, con la definición BT. 709 del color YUV, con una velocidad de fotogramas de 29,97 fotogramas por segundo. Supongamos que el contenido de vídeo se compone exclusivamente de tramas progresivas. En el fragmento de código siguiente se muestra cómo rellenar la descripción del formato y obtener los GUID del dispositivo:


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



El código de este ejemplo se toma del ejemplo de SDK de [ \_ videoproc DXVA2](dxva2-videoproc-sample.md) .

La matriz *pGuids* de este ejemplo se asigna mediante el método [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) , por lo que la aplicación debe liberar la matriz llamando a [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree). El resto de los pasos se pueden realizar con cualquiera de los GUID de dispositivo devueltos por este método.

### <a name="enumerate-render-target-formats"></a>Enumerar formatos de Render-Target

Para obtener la lista de formatos de destino de representación admitidos por el dispositivo, pase el GUID del dispositivo y la estructura [**DXVA2 de \_ videodesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) al método [**IDirectXVideoProcessorService:: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) , tal y como se muestra en el código siguiente:


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



El método devuelve una matriz de valores **D3DFORMAT** . En este ejemplo, donde el tipo de entrada es YUY2, una lista típica de formatos podría ser D3DFMT \_ X8R8G8B8 (RGB de 32 bits) y D3DMFT \_ YUY2 (el formato de entrada). Sin embargo, la lista exacta dependerá del controlador.

La lista de formatos disponibles para las subsecuencias puede variar en función del formato de destino de representación y el formato de entrada. Para obtener la lista de formatos de subsecuencia, pase el GUID del dispositivo, la estructura de formato y el formato de representación-destino al método [**IDirectXVideoProcessorService:: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) , tal y como se muestra en el código siguiente:


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



Este método devuelve otra matriz de valores **D3DFORMAT** . Los formatos de subflujo típicos son AYUV y AI44.

### <a name="query-the-device-capabilities"></a>Consultar las capacidades del dispositivo

Para obtener las capacidades de un dispositivo determinado, pase el GUID del dispositivo, la estructura de formato y un formato de destino de representación al método [**IDirectXVideoProcessorService:: GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) . El método rellena una estructura de estructura de [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) con las funcionalidades del dispositivo.


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



### <a name="create-the-device"></a>Crear el dispositivo

Para crear el dispositivo de procesamiento de vídeo, llame a [**IDirectXVideoProcessorService:: CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor). La entrada a este método es el GUID del dispositivo, la descripción del formato, el formato del destino de representación y el número máximo de subflujos que se van a mezclar. El método devuelve un puntero a la interfaz [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) , que representa el dispositivo de procesamiento de vídeo.


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



## <a name="video-process-blit"></a>Proceso de vídeo blit

La operación principal de procesamiento de vídeo es el *procesamiento de vídeo*. (Un *blit* es cualquier operación que combina dos o más mapas de bits en un único mapa de bits. Un blit de procesamiento de vídeo combina imágenes de entrada para crear un fotograma de salida.) Para realizar una blit de procesamiento de vídeo, llame a [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt). Este método pasa un conjunto de muestras de vídeo al dispositivo de procesamiento de vídeo. En respuesta, el dispositivo de procesamiento de vídeo procesa las imágenes de entrada y genera un fotograma de salida. El procesamiento puede incluir desentrelazado, conversión de espacio de color y combinación de subflujo. La salida se escribe en una superficie de destino proporcionada por el autor de la llamada.

El método [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) toma los siguientes parámetros:

-   *pRT* apunta a una superficie de destino de representación de **IDirect3DSurface9** que recibirá el fotograma de vídeo procesado.
-   *pBltParams* apunta a una [**estructura \_ VideoProcessBltParams de DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) que especifica los parámetros para el blit.
-   *pSamples* es la dirección de una matriz de estructuras de [**\_ videoejemplo de DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) . Estas estructuras contienen los ejemplos de entrada para el blit.
-   *NumSamples* proporciona el tamaño de la matriz de *pSamples* .
-   El parámetro *Reserved* está reservado y debe establecerse en **null**.

En la matriz *pSamples* , el llamador debe proporcionar los siguientes ejemplos de entrada:

-   La imagen actual de la secuencia de vídeo principal.
-   Imágenes de referencia hacia delante y hacia atrás, si es necesario para el algoritmo de desentrelazado.
-   Cero o más imágenes de subsecuencia, hasta un máximo de 15 subsecuencias.

El controlador espera que esta matriz esté en un orden determinado, tal como se describe en [orden de ejemplo de entrada](#input-sample-order).

### <a name="blit-parameters"></a>Parámetros de blit

La estructura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) contiene parámetros generales para el blit. Los parámetros más importantes se almacenan en los siguientes miembros de la estructura:

-   **TargetFrame** es el tiempo de presentación del fotograma de salida. En el caso del contenido progresivo, esta hora debe ser igual a la hora de inicio del fotograma actual del flujo de vídeo principal. Esta vez se especifica en el miembro de **Inicio** de la estructura de [**\_ videomuestra DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) para ese ejemplo de entrada.

    En el caso de contenido entrelazado, un marco con dos campos intercalados genera dos fotogramas de salida desentrelazados. En el primer fotograma de salida, el tiempo de presentación debe ser igual a la hora de inicio de la imagen actual en el flujo de vídeo principal, al igual que el contenido progresivo. En el segundo fotograma de salida, la hora de inicio debe ser igual al punto medio entre la hora de inicio de la imagen actual en la secuencia de vídeo principal y la hora de inicio de la siguiente imagen de la secuencia. Por ejemplo, si el vídeo de entrada tiene 25 fotogramas por segundo (50 campos por segundo), los fotogramas de salida tendrán las marcas de tiempo que se muestran en la tabla siguiente. Las marcas de tiempo se muestran en unidades de 100 nanosegundos.

    

    | Imagen de entrada | **TargetFrame** (1) | **TargetFrame** (2) |
    |---------------|---------------------|---------------------|
    | 0             | 0                   | 200000              |
    | 400000        | 0                   | 600000              |
    | 800000        | 800000              | 1000000             |
    | 1,2 millones       | 1,2 millones             | 1,4 millones             |

    

     

    Si el contenido entrelazado consta de campos únicos en lugar de campos intercalados, los tiempos de salida siempre coinciden con los tiempos de entrada, como con el contenido progresivo.

-   **TargetRect** define una región rectangular dentro de la superficie de destino. El blit escribirá la salida en esta región. En concreto, se modificarán todos los píxeles dentro de **TargetRect** y no se modificará ningún píxel fuera de **TargetRect** . El rectángulo de destino define el rectángulo delimitador de todas las secuencias de vídeo de entrada. La colocación de flujos individuales dentro de ese rectángulo se controla mediante el parámetro *pSamples* de [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).
-   **BackgroundColor** proporciona el color del fondo siempre que no aparezca ninguna imagen de vídeo. Por ejemplo, cuando se muestra una imagen de 16 x 9 en una superficie de 4 x 3 (panorámica), se muestran las regiones con el color de fondo. El color de fondo solo se aplica dentro del rectángulo de destino (**TargetRect**). Los píxeles fuera de **TargetRect** no se modifican.
-   **DestFormat** describe el espacio de colores del vídeo de salida, por ejemplo, si se usa el color ITU-R BT. 709 o BT. 601. Esta información puede afectar al modo en que se muestra la imagen. Para obtener más información, vea [información de color extendido](extended-color-information.md).

Otros parámetros se describen en la página de referencia de la estructura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .

### <a name="input-samples"></a>Ejemplos de entrada

El parámetro *pSamples* de [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) apunta a una matriz de estructuras de [**\_ videoejemplo de DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) . Cada una de estas estructuras contiene información sobre un ejemplo de entrada y un puntero a la superficie de Direct3D que contiene el ejemplo. Cada ejemplo es uno de los siguientes:

-   La imagen actual del flujo principal.
-   Una imagen de referencia hacia delante o hacia atrás desde el flujo principal, que se usa para Desentrelazar.
-   Imagen de subsecuencia.

El orden exacto en el que las muestras deben aparecer en la matriz se describe más adelante, en la sección [orden de ejemplo de entrada](#input-sample-order).

Se pueden proporcionar hasta 15 imágenes de subflujo, aunque la mayoría de las aplicaciones de vídeo solo necesitan un subflujo, como máximo. El número de subsecuencias puede cambiar con cada llamada a [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt). Las imágenes de subflujo se indican estableciendo el miembro **SampleFormat. SampleFormat** de la estructura de [**\_ videomuestra DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) igual a DXVA2 \_ SampleSubStream. En el flujo de vídeo principal, este miembro describe el entrelazado del vídeo de entrada. Para obtener más información, consulte enumeración [**DXVA2 \_ SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) .

En el flujo de vídeo principal, los miembros **inicial** y **final** de la estructura de [**\_ videomuestra DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) proporcionan las horas de inicio y finalización de la muestra de entrada. En el caso de las imágenes de subflujo, establezca estos valores en cero, ya que el tiempo de presentación siempre se calcula a partir del flujo principal. La aplicación es responsable del seguimiento cuando se debe presentar cada imagen de subflujo y enviarla a [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) en el momento adecuado.

Dos rectángulos definen cómo se coloca el vídeo de origen para cada flujo:

-   El miembro **SrcRect** de la estructura de [**\_ videomuestra DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) especifica el *rectángulo de origen*, una región rectangular de la imagen de origen que aparecerá en el marco de salida compuesto. Para recortar la imagen, establézcalo en un valor menor que el tamaño del marco. En caso contrario, establézcalo igual al tamaño del marco.
-   El miembro **DstRect** de la misma estructura especifica el *rectángulo de destino*, una región rectangular de la superficie de destino donde aparecerá el fotograma de vídeo.

El controlador blits píxeles desde el rectángulo de origen al rectángulo de destino. Los dos rectángulos pueden tener diferentes tamaños o relaciones de aspecto. el controlador escalará la imagen según sea necesario. Además, cada flujo de entrada puede usar un factor de escala diferente. De hecho, es posible que sea necesario escalar para generar la relación de aspecto correcta en el marco de salida. El controlador no tiene en cuenta la proporción de aspecto de píxeles del origen, por lo que si la imagen de origen usa píxeles no cuadrados, depende de la aplicación calcular el rectángulo de destino correcto.

Los formatos de subflujo preferidos son AYUV y AI44. El último es un formato de paleta con 16 colores. Las entradas de la paleta se especifican en el miembro **PAL** de la estructura de [**\_ videomuestra DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) . (Si el formato de vídeo de origen se expresa originalmente como Media Foundation tipo de medio, las entradas de la paleta se almacenan en el atributo [**MF \_ MT \_ Palette**](mf-mt-palette-attribute.md) ). En el caso de los formatos no de paleta, borre esta matriz en cero.

## <a name="image-composition"></a>Composición de imagen

Cada operación de blit se define mediante los tres rectángulos siguientes:

-   El rectángulo de *destino* (**TargetRect**) define la región dentro de la superficie de destino en la que aparecerá la salida. La imagen de salida se recorta a este rectángulo.
-   El rectángulo de *destino* de cada secuencia (**DstRect**) define dónde aparece el flujo de entrada en la imagen compuesta.
-   El rectángulo de *origen* de cada flujo (**SrcRect**) define qué parte de la imagen de origen aparece.

Los rectángulos de destino y destino se especifican en relación con la superficie de destino. El rectángulo de origen se especifica en relación con la imagen de origen. Todos los rectángulos se especifican en píxeles.

![diagrama que muestra los rectángulos de origen, destino y destino](images/dxva-vp-rects.gif)

El dispositivo de procesamiento de vídeo alfa combina las imágenes de entrada con cualquiera de los siguientes orígenes de datos alfa:

-   Datos alfa por píxel de subsecuencias.
-   Un valor alfa plano para cada flujo de vídeo, especificado en el miembro **PlanarAlpha** de la estructura de [**\_ videoejemplo DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .
-   Valor alfa plano de la imagen compuesta, especificado en el miembro **alfa** de la estructura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) . Este valor se usa para fusionar toda la imagen compuesta con el color de fondo.

En esta sección se proporciona una serie de ejemplos que muestran cómo el dispositivo de procesamiento de vídeo crea la imagen de salida.

### <a name="example-1-letterboxing"></a>Ejemplo 1: panorámica

En este ejemplo se muestra cómo aplicar una panorámica a la imagen de origen, estableciendo el rectángulo de destino para que sea menor que el rectángulo de destino. La secuencia de vídeo principal de este ejemplo es una imagen 720 × 480 y está pensada para mostrarse con una relación de aspecto de 16:9. La superficie de destino es 640 × 480 píxeles (relación de aspecto de 4:3). Para lograr la relación de aspecto correcta, el rectángulo de destino debe ser 640 × 360. Para simplificar, en este ejemplo no se incluye un subflujo. En el diagrama siguiente se muestran los rectángulos de origen y de destino.

![diagrama que muestra la panorámica.](images/428105fa-a26b-48a6-991d-44d24ab786b1.gif)

En el diagrama anterior se muestran los siguientes rectángulos:

-   Rectángulo de destino: {0, 0, 640, 480}
-   Vídeo principal:

    -   Rectángulo de origen: {0, 0, 720, 480}
    -   Rectángulo de destino: {0, 60, 640, 420}

El controlador desentrelazará el vídeo, reducirá el fotograma desentrelazado a 640 × 360 y convertirá el marco en el rectángulo de destino. El rectángulo de destino es mayor que el rectángulo de destino, por lo que el controlador usará el color de fondo para rellenar las barras horizontales por encima y por debajo del marco. El color de fondo se especifica en la estructura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .

### <a name="example-2-stretching-substream-images"></a>Ejemplo 2: expandir imágenes de subflujo

Las imágenes de subflujo pueden extenderse más allá de la imagen de vídeo principal. En vídeo DVD, por ejemplo, la secuencia de vídeo principal puede tener una relación de aspecto 4:3 mientras que la subsecuencia es 16:9. En este ejemplo, ambos flujos de vídeo tienen las mismas dimensiones de origen (720 × 480), pero el subflujo está diseñado para mostrarse en una relación de aspecto de 16:9. Para lograr esta relación de aspecto, la imagen de subflujo se estira horizontalmente. Los rectángulos de origen y de destino se muestran en el diagrama siguiente.

![diagrama que muestra el ajuste de imagen de subflujo.](images/7ab31c65-06b9-4843-90b8-2f9fb6f6b20e.gif)

En el diagrama anterior se muestran los siguientes rectángulos:

-   Rectángulo de destino: {0, 0, 854, 480}
-   Vídeo principal:

    -   Rectángulo de origen: {0, 0, 720, 480}
    -   Rectángulo de destino: {0, 107, 474, 480}

-   Subtransmisiones
    -   Rectángulo de origen: {0, 0, 720, 480}
    -   Rectángulo de destino: {0, 0, 854, 480}

Estos valores conservan el alto de la imagen y escalan ambas imágenes horizontalmente. En las regiones en las que aparecen ambas imágenes, se combinan alfa. En el caso de que la imagen de subflujo se desacabe más allá del vídeo de la ubicación, el subflujo se mezcla alfa con el color de fondo. Esta mezcla alfa cuenta con los colores modificados en el lado derecho del diagrama.

### <a name="example-3-mismatched-stream-heights"></a>Ejemplo 3: alto de flujo no coincidente

En el ejemplo anterior, la subsecuencia y el flujo principal tienen el mismo alto. Los flujos también pueden tener un alto no coincidente, tal como se muestra en este ejemplo. Las áreas del rectángulo de destino donde no aparece ningún vídeo se dibujan con el color de fondo, en este ejemplo. Los rectángulos de origen y de destino se muestran en el diagrama siguiente.

![diagrama que muestra el alto de los flujos no coincidentes,](images/0190a15a-d971-450f-90ed-ce5633e1069c.gif)

En el diagrama anterior se muestran los siguientes rectángulos:

-   Rectángulo de destino: {0, 0, 150, 85}
-   Vídeo principal:
    -   Rectángulo de origen: {0, 0, 150, 50}
    -   Rectángulo de destino: {0, 17, 150, 67}
-   Subtransmisiones
    -   Rectángulo de origen: {0, 0, 100, 85}
    -   Rectángulo de destino: {25, 0, 125, 85}

### <a name="example-4-target-rectangle-smaller-than-destination-surface"></a>Ejemplo 4: rectángulo de destino menor que la superficie de destino

Este ejemplo muestra un caso en el que el rectángulo de destino es menor que la superficie de destino.

![diagrama que muestra un blit a un rectángulo de destino.](images/360a85a3-333c-4b32-b8f7-1beb1e805921.gif)

En el diagrama anterior se muestran los siguientes rectángulos:

-   Superficie de destino: {0, 0, 300, 200}
-   Rectángulo de destino: {0, 0, 150, 85}
-   Vídeo principal:
    -   Rectángulo de origen: {0, 0, 150, 50}
    -   Rectángulo de destino: {0, 17, 150, 67}
-   Subtransmisiones
    -   Rectángulo de origen: {0, 0, 100, 85}
    -   Rectángulo de destino: {25, 0, 125, 85}

Los píxeles que están fuera del rectángulo de destino no se modifican, por lo que el color de fondo solo aparece dentro del rectángulo de destino. El área de puntos indica partes de la superficie de destino que no se ven afectadas por el blit.

### <a name="example-5-source-rectangles"></a>Ejemplo 5: rectángulos de origen

Si especifica un rectángulo de origen menor que el de la imagen de origen, el controlador convertirá solo esa parte de la imagen. En este ejemplo, los rectángulos de origen especifican el cuadrante inferior derecho de la secuencia de vídeo principal y el cuadrante inferior izquierdo de la subsecuencia (indicado por marcas de hash en el diagrama). Los rectángulos de destino tienen el mismo tamaño que los rectángulos de origen, por lo que el vídeo no se ajusta. Los rectángulos de origen y de destino se muestran en el diagrama siguiente.

![diagrama que muestra un blit de dos rectángulos de origen.](images/b1de4cc3-0155-40be-acac-b486e2af8c0d.gif)

En el diagrama anterior se muestran los siguientes rectángulos:

-   Rectángulo de destino: {0, 0, 720, 576}
-   Vídeo principal:
    -   Tamaño de la superficie de origen: {0, 0, 720, 480}
    -   Rectángulo de origen: {360, 240, 720, 480}
    -   Rectángulo de destino: {0, 0, 360, 240}
-   Subtransmisiones
    -   Tamaño de la superficie de origen: {0, 0, 640, 576}
    -   Rectángulo de origen: {0, 288, 320, 576}
    -   Rectángulo de destino: {400, 0, 720, 288}

### <a name="example-6-intersecting-destination-rectangles"></a>Ejemplo 6: intersección de rectángulos de destino

Este ejemplo es similar al anterior, pero los rectángulos de destino forman una intersección. Las dimensiones de la superficie son las mismas que en el ejemplo anterior, pero los rectángulos de origen y de destino no. De nuevo, el vídeo se recorta pero no se ajusta. Los rectángulos de origen y de destino se muestran en el diagrama siguiente.

![diagrama que muestra los rectángulos de destino de intersección.](images/fbe450cb-c84d-4110-9515-00f27601528e.gif)

En el diagrama anterior se muestran los siguientes rectángulos:

-   Rectángulo de destino: {0, 0, 720, 576}
-   Vídeo principal:
    -   Tamaño de la superficie de origen: {0, 0, 720, 480}
    -   Rectángulo de origen: {260, 92, 720, 480}
    -   Rectángulo de destino: {0, 0, 460, 388}
-   Subtransmisiones
    -   Tamaño de la superficie de origen: {0, 0, 640, 576}
    -   Rectángulo de origen: {0, 0, 460, 388}
    -   Rectángulo de destino: {260, 188, 720, 576}

### <a name="example-7-stretching-and-cropping-video"></a>Ejemplo 7: expandir y recortar vídeo

En este ejemplo, el vídeo se estira y se recorta. Una región 180 × 120 de cada flujo se expande para abarcar un área de 360 × 240 en el rectángulo de destino.

![diagrama que muestra la expansión y el recorte.](images/ce83529c-8545-492c-9d3e-ef221c30e326.gif)

En el diagrama anterior se muestran los siguientes rectángulos:

-   Rectángulo de destino: {0, 0, 720, 480}
-   Vídeo principal:
    -   Tamaño de la superficie de origen: {0, 0, 360, 240}
    -   Rectángulo de origen: {180, 120, 360, 240}
    -   Rectángulo de destino: {0, 0, 360, 240}
-   Subtransmisiones
    -   Tamaño de la superficie de origen: {0, 0, 360, 240}
    -   Rectángulo de origen: {0, 0, 180, 120}
    -   Rectángulo de destino: {360, 240, 720, 480}

## <a name="input-sample-order"></a>Orden de ejemplo de entrada

El parámetro *pSamples* del método [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) es un puntero a una matriz de ejemplos de entrada. Los ejemplos del flujo de vídeo principal aparecen en primer lugar, seguidos de las imágenes de subsecuencia en orden Z. Los ejemplos se deben colocar en la matriz en el orden siguiente:

-   Los ejemplos de la secuencia de vídeo principal aparecen en primer lugar en la matriz, en orden temporal. Dependiendo del modo de desentrelazado, el controlador puede requerir uno o más ejemplos de referencia de la secuencia de vídeo principal. Los miembros **NumForwardRefSamples** y **NumBackwardRefSamples** de la estructura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) especifican el número de ejemplos de referencia hacia delante y hacia atrás que son necesarios. El autor de la llamada debe proporcionar estos ejemplos de referencia incluso si el contenido del vídeo es progresivo y no requiere desentrelazado. (Esto puede ocurrir cuando se proporcionan fotogramas progresivos a un dispositivo de desentrelazado, por ejemplo, cuando el origen contiene una mezcla de fotogramas entrelazados y progresivos).
-   Después de los ejemplos de la secuencia de vídeo principal, la matriz puede contener hasta 15 muestras de subflujo, organizadas en orden Z, de abajo a arriba. Las subsecuencias siempre son progresivas y no requieren imágenes de referencia.

En cualquier momento, la secuencia de vídeo principal puede cambiar entre el contenido entrelazado y progresivo, y el número de subflujos puede cambiar.

El miembro **SampleFormat. SampleFormat** de la estructura de [**\_ videomuestra DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) indica el tipo de imagen. En el caso de las imágenes de subflujo, establezca este valor en DXVA2 \_ SampleSubStream. En el caso de las imágenes progresivas, el valor es DXVA2 \_ SampleProgressiveFrame. En el caso de las imágenes entrelazadas, el valor depende del diseño del campo.

Si el controlador requiere ejemplos de referencia hacia delante y hacia atrás, es posible que el número total de muestras no esté disponible al principio de la secuencia de vídeo. En ese caso, incluya entradas para ellos en la matriz *pSamples* , pero marque los ejemplos que faltan como si tuvieran el tipo DXVA2 \_ SampleUnknown.

Los miembros **inicial** y **final** de la estructura de [**\_ videomuestra DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) proporcionan la ubicación temporal de cada ejemplo. Estos valores solo se usan para los ejemplos de la secuencia de vídeo principal. En el caso de las imágenes de subflujo, establezca ambos miembros en cero.

Los ejemplos siguientes pueden ayudarle a aclarar estos requisitos.

### <a name="example-1"></a>Ejemplo 1

El caso más simple se produce cuando no hay subsecuencias y el algoritmo de desentrelazado no requiere ejemplos de referencia (**NumForwardRefSamples** y **NumBackwardRefSamples** son cero). Bob desentrelazado es un ejemplo de este tipo de algoritmo. En este caso, la matriz *pSamples* debe contener una sola superficie de entrada, tal como se muestra en la tabla siguiente.



| Índice           | Tipo de superficie        | Ubicación temporal |
|-----------------|---------------------|-------------------|
| *pSamples* \[ 0,1\] | Imagen entrelazada. | *T*               |



 

Se supone que el valor de hora *T* es la hora de inicio del fotograma de vídeo actual.

### <a name="example-2"></a>Ejemplo 2

En este ejemplo, la aplicación mezcla dos subsecuencias con el flujo principal. El algoritmo de desentrelazado no requiere ejemplos de referencia. En la tabla siguiente se muestra cómo se organizan estos ejemplos en la matriz *pSamples* .



| Índice           | Tipo de superficie       | Ubicación temporal | Orden Z |
|-----------------|--------------------|-------------------|---------|
| *pSamples* \[ 0,1\] | Imagen entrelazada | *T*               | 0       |
| *pSamples* \[ dimensional\] | Subtransmisiones          | 0                 | 1       |
| *pSamples* \[ dos\] | Subtransmisiones          | 0                 | 2       |



 

### <a name="example-3"></a>Ejemplo 3

Ahora Supongamos que el algoritmo de desentrelazado requiere un ejemplo de referencia inversa y un ejemplo de referencia adelantada. Además, se proporcionan dos imágenes de subflujo, para un total de cinco superficies. En la tabla siguiente se muestra el orden correcto.



| Índice           | Tipo de superficie                   | Ubicación temporal | Orden Z        |
|-----------------|--------------------------------|-------------------|----------------|
| *pSamples* \[ 0,1\] | Imagen entrelazada (referencia) | *T* − 1            | No aplicable |
| *pSamples* \[ dimensional\] | Imagen entrelazada             | *T*               | 0              |
| *pSamples* \[ dos\] | Imagen entrelazada (referencia) | *T* + 1            | No aplicable |
| *pSamples* \[ 3\] | Subtransmisiones                      | 0                 | 1              |
| *pSamples* \[ 4\] | Subtransmisiones                      | 0                 | 2              |



 

El tiempo *T* − 1 es la hora de inicio del fotograma anterior al marco actual y *T* + 1 es la hora de inicio del siguiente fotograma.

Si la secuencia de vídeo cambia a contenido progresivo, utilizando el mismo modo de desentrelazado, la aplicación debe proporcionar el mismo número de ejemplos, como se muestra en la tabla siguiente.



| Índice           | Tipo de superficie                    | Ubicación temporal | Orden Z        |
|-----------------|---------------------------------|-------------------|----------------|
| *pSamples* \[ 0,1\] | Imagen progresiva (referencia) | *T* − 1            | No aplicable |
| *pSamples* \[ dimensional\] | Imagen progresiva             | *T*               | 0              |
| *pSamples* \[ dos\] | Imagen progresiva (referencia) | *T* + 1            | No aplicable |
| *pSamples* \[ 3\] | Subtransmisiones                       | 0                 | 1              |
| *pSamples* \[ 4\] | Subtransmisiones                       | 0                 | 2              |



 

### <a name="example-4"></a>Ejemplo 4

Al principio de una secuencia de vídeo, es posible que los ejemplos de referencia hacia delante y hacia atrás no estén disponibles. Cuando esto sucede, las entradas de los ejemplos que faltan se incluyen en la matriz *pSamples* , con el tipo de ejemplo DXVA2 \_ SampleUnknown.

Suponiendo que el modo de desentrelazado necesita una muestra de referencia hacia delante y una de referencias inversas, las tres primeras llamadas a [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) tendrían las secuencias de entradas que se muestran en las tres tablas siguientes.



| Índice           | Tipo de superficie                   | Ubicación temporal |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[ 0,1\] | Unknown                        | 0                 |
| *pSamples* \[ dimensional\] | Unknown                        | 0                 |
| *pSamples* \[ dos\] | Imagen entrelazada (referencia) | *T* + 1            |



 



| Índice           | Tipo de superficie                   | Ubicación temporal |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[ 0,1\] | Unknown                        | 0                 |
| *pSamples* \[ dimensional\] | Imagen entrelazada             | *T*               |
| *pSamples* \[ dos\] | Imagen entrelazada (referencia) | *T* + 1            |



 



| Índice           | Tipo de superficie                   | Ubicación temporal |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[ 0,1\] | Imagen entrelazada             | *T* − 1            |
| *pSamples* \[ dimensional\] | Imagen entrelazada             | *T*               |
| *pSamples* \[ dos\] | Imagen entrelazada (referencia) | *T* + 1            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Aceleración de vídeo de DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA2 \_ ejemplo de Videoproc](dxva2-videoproc-sample.md)
</dt> </dl>

 

 
