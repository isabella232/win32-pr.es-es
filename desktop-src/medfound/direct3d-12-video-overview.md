---
description: Este artículo contiene instrucciones generales para usar las API de vídeo de Direct3D 12.
ms.assetid: ''
title: Información general sobre vídeo de Direct3D 12
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: b21587f2784b34131da9c050655b6f3fbe43582d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539574"
---
# <a name="direct3d-12-video-overview"></a>Información general sobre vídeo de Direct3D 12

Este artículo contiene instrucciones generales para usar las API de vídeo de Direct3D 12.

## <a name="about-direct3d-12-video"></a>Vídeo acerca de Direct3D 12

La interfaz de vídeo de Direct3D 12 proporciona una nueva forma para que las aplicaciones implementen la descodificación y el proceso de vídeo. La interfaz de Direct3D 12 es diferente de la interfaz de Direct3D 11 anterior porque se diseñó para ser coherente con los principios y el estilo de Direct3D 12, que incluye lo siguiente:

- Ofrezca más control a los desarrolladores
 - Asignación de memoria accesible desde hardware
 - Subprocesos de CPU utilizados para generar & enviar comandos
   - Generación y envío independientes
   - Sin bloqueo
 - Programación de trabajo de hardware
- Cubre la funcionalidad existente, incluida la mayoría de la funcionalidad de vídeo de Direct3D 11, pero al mismo tiempo, tiene en cuenta la simplicidad y la facilidad de uso.
- Eficacia y rendimiento de las aplicaciones de Direct3D 12 principales iguales o superiores a Direct3D 11
- Coherencia con otras API de Direct3D 12
- Interoperabilidad con las API de gráficos existentes


## <a name="video-decoding"></a>Descodificación de vídeo

En las secciones siguientes se describen algunas de las tareas necesarias para implementar la descodificación de vídeo de Direct3D 12.

### <a name="query-for-decoding-capabilities"></a>Consulta de funcionalidades de descodificación

Llame a [ID3D12VideoDevice:: CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) para comprobar los detalles de compatibilidad de las operaciones de descodificación de vídeo de Direct3D 12. Pase un valor de la enumeración [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) para especificar la característica a la que solicita información de soporte técnico.

### <a name="create-the-video-decoder"></a>Crear el descodificador de vídeo

Llame a [ID3D12VideoDevice:: CreateVideoDecoder](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder) para crear una instancia de la interfaz [ID3D12VideoDecoder](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoder) . El descodificador contiene el estado de una sesión de descodificación, incluidos los datos relacionados con las referencias como vectores de movimiento.  En el caso de un cambio de resolución o un cambio de [MaxDecodePictureBufferCount](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc) , se vuelve a crear el objeto descodificador. El ancho y el alto de descodificación especifican la resolución de flujo nativo antes de cualquier escala.  El número máximo de búferes de descodificación de imágenes (DPB) especifica el recuento de DPB más grande que se puede usar sin volver a crear el descodificador de vídeo.

El descodificador se puede usar para grabar comandos desde varias listas de comandos, pero solo se puede asociar a una lista de comandos a la vez.  La aplicación es responsable de sincronizar el acceso al descodificador.

### <a name="create-the-video-decoder-heap"></a>Crear el montón del descodificador de vídeo 

Llame a [ID3D12VideoDevice:: CreateVideoDecoderHeap](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) para crear una instancia de la interfaz [ID3D12VideoDecoderHeap](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoderheap) . Este objeto contiene los recursos de controlador dependientes de la resolución y el estado.

### <a name="decoding-a-frame"></a>Descodificar un marco

Todos los parámetros de entrada y salida de las operaciones de procesamiento de vídeo se organizan en una estructura de parámetros de entrada, [D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)y una estructura de parámetros de salida, [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments).
La aplicación administra los fotogramas de referencia y, como tal, debe establecer los fotogramas de referencia para cada operación de descodificación.
Cuando se grabe correctamente la lista de comandos, llame a [ID3D12CommandQueue:: ExecuteCommandLists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) en la cola de comandos de vídeo para enviar la descodificación de fotogramas a la GPU.


### <a name="enabling-decoder-output-conversions"></a>Habilitar las conversiones de salida del descodificador
Si el descodificador admite la conversión, habilite las conversiones deseadas rellenando correctamente la estructura de [D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) . El formato y las resoluciones de la salida deseada en lugar de la salida nativa del descodificador se comunican a través de la diferencia en el espacio de colores y las resoluciones especificadas en los parámetros de conversión.

##  <a name="querying-decoding-status"></a>Consulta del estado de descodificación 
Use los métodos [ID3D12VideoDecodeCommandList:: BeginQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery) y [ID3D12VideoDecodeCommandList:: EndQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery) para consultar el estado de la operación de descodificación.

La estructura de [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics) se usa para describir las estadísticas de descodificación de vídeo. Para obtener una instancia de esta estructura, llame a [ID3D12VideoDecodeCommandList:: EndQuery](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery), pasando el valor de tipo de consulta heap de [D3D12_QUERY_TYPE_VIDEO_DECODE_STATISTIC](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Tenga en cuenta que esta consulta no usa [ID3D12VideoDecodeCommandList:: BeginQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery).

## <a name="video-processing"></a>Procesamiento de vídeo

Las API de vídeo de Direct3D 12 tienen un enfoque simplificado para el procesamiento de vídeo, con lo que se eliminan las características de Direct3D 11 que no se usaron ampliamente y se quitan las comprobaciones de funcionalidad de las características que son obligatorias en Se elimina el proceso de enumeración para el procesamiento de vídeo. En su lugar, llame a [ID3D12VideoDevice:: CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) , que permite que una aplicación identifique las capacidades del procesador de vídeo. Los formatos y las tasas de vídeo, entrelazado y estéreo deseados se proporcionan como entrada para **CheckFeatureSupport**.

### <a name="removed-capabilities"></a>Funcionalidades eliminadas

Las siguientes funcionalidades de Direct3D 11 no se admiten en el procesamiento de vídeo de Direct3D 12:
- Tasas personalizadas.  En su lugar, se proporciona una velocidad de entrada y salida durante la grabación de comandos [ID3D12VideoProcessCommandList::P rocessframes](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) .
- Ahora solo hay dos modos de desentrelazado disponibles: [Bob](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags) y [Custom](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags). Se han eliminado otros modos. PERSONALIZADO es un modo de desentrelazado de alta calidad proporcionado por el fabricante del hardware.
- Ya no se admiten todos los formatos estéreo opcionales de [D3D11_VIDEO_PROCESSOR_STEREO_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_caps) . En su lugar, [Nono](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format), [horizontal](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format), [vertical](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format)y [independiente](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) son obligatorios para todos los dispositivos de hardware Si se admite estéreo.
- No hay ningún equivalente para [D3D11_VIDEO_PROCESSOR_FORMAT_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_format_caps) o [D3D11_VIDEO_PROCESSOR_AUTO_STREAM_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_auto_stream_caps). En su lugar, los formatos de entrada y salida son argumentos para la creación del procesador de vídeo y, en ese momento, se debe conocer si el procesador de vídeo puede o no puede realizar la operación con el formato especificado. El [D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_auto_processing_flags) se utiliza para indicar si las características de procesamiento automático están disponibles.
- No hay ningún equivalente para [D3D11_VIDEO_PROCESSOR_CAPS_LEGACY](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps).
- No hay ningún equivalente para [D3D11_VIDEO_PROCESSOR_CAPS_CONSTRICTION](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps).
- Al convertir de estéreo a mono, asumimos que la vista de línea base es 0.
- El procesamiento de vídeo de Direct3D 12 no admite la conversión de mono a estéreo y no se admite el desplazamiento mono. 


### <a name="creating-a-video-processor"></a>Creación de un procesador de vídeo

Llame a [ID3D12VideoDevice:: CreateVideoProcessor](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor) para crear una instancia de [ID3D12VideoProcessor](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoprocessor). El procesador de vídeo contiene el estado de una sesión de procesamiento de vídeo, incluida la memoria intermedia necesaria, los datos de procesamiento en caché u otro espacio de trabajo temporal. Los argumentos de creación del procesador de vídeo especifican qué operaciones se realizan o están disponibles en [ID3D12VideoProcessCommandList1::P rocessframes1](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1) Time.  Las asignaciones de controladores para realizar la operación de proceso de vídeo (por ejemplo, los intermedios) se asignan en el momento de la creación del procesador de vídeo.  Use [D3D12_FEATURE_VIDEO_PROCESSOR_SIZE](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) para determinar el tamaño de asignación del procesador de vídeo de antemano.

El procesador de vídeo solo se puede usar para grabar comandos desde varias listas de comandos, pero solo se puede asociar a una lista de comandos a la vez.  La aplicación es responsable de sincronizar el acceso al procesador de vídeo.  La aplicación también debe grabar comandos de procesamiento de vídeo en el vídeo procoessor en el orden en que se ejecutan en la GPU.

Todos los argumentos de entrada y salida de las operaciones de procesamiento de vídeo se organizan en una estructura de argumentos de entrada, [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)y una estructura de argumentos de salida, [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments). La aplicación debe llamar a [ID3D12VideoProcessCommandList::P rocessframes](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) para registrar la operación de procesamiento de vídeo que desea ejecutar. 

Cuando se grabe la lista de comandos, llame a [ID3D12CommandQueue:: ExecuteCommandLists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) en la cola de comandos de vídeo para enviar el procesamiento de fotogramas a la GPU.


## <a name="tiers"></a>Niveles

El vídeo de Direct3D 12 define los niveles que agrupan las capacidades de los dispositivos de hardware, de modo que la aplicación puede tener menos rutas de acceso de código para satisfacer la variedad de hardware. Los niveles se especifican con la enumeración [D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier) .

En todos los niveles, estará disponible lo siguiente:

- No es necesario volver a realizar el descodificador en los cambios de resolución. Solo es necesario volver a crear el montón del descodificador en el cambio de resolución.
- Todos los fotogramas de referencia serán administrados por la aplicación. Esto permite que el sistema Ahorre memoria, ya que no es necesario asignar el número máximo de DPBs en el momento de la creación del descodificador en algunos niveles, y proporciona flexibilidad a las aplicaciones en los escenarios de cambio de resolución.

Tenga en cuenta que los niveles son superconjuntos. Una aplicación puede decidir realizar el nivel 1 y no usar las características de nivel superior, lo que se permite, pero es posible que no proporcione un rendimiento óptimo. Para obtener más información sobre las capacidades asociadas a los distintos niveles de nivel, vea [D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier).

## <a name="reference-frames"></a>Fotogramas de referencia

Con el vídeo de Direct3D 12, los fotogramas de referencia se pasan explícitamente. Esto permite un uso claro de la matriz de texturas o matrices de texturas al descodificar fotogramas. No es necesario que la aplicación pase exactamente el mismo identificador de recurso cuando se usa como referencia. por ejemplo, puede optar por copiar un recurso en otro y, a continuación, pasar la copia en lugar de la original. El controlador sigue usando los índices de *RefFrameList* y *CurrPic* de DXVA para almacenar los datos pertinentes de cada fotograma descodificado.


## <a name="directx-12-fences"></a>Barreras de DirectX 12

En DirectX 12, la aplicación es responsable de sincronizar el acceso a sus búferes. En el caso de la descodificación, habrá que agregar barreras a los búferes de entrada y a los búferes de salida. Cada barrera tiene un valor asociado y se usa para la sincronización de la CPU y los motores de hardware. Para obtener más información, vea [uso de barreras de recursos para sincronizar los Estados de los recursos en Direct3D 12](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12).

Una implementación típica tendrá una barrera para cada búfer de entrada. En el caso de los búferes de entrada, es posible que el búfer esté disponible antes de que se realice todo el proceso de descodificación. El sistema omitirá este caso y asumirá que el búfer de entrada está disponible cuando se realiza la descodificación.
Normalmente, una implementación también tendrá una barrera para cada búfer de salida. En el caso de enviar la salida al compositor, por ejemplo, se necesita una barrera que se señaliza cuando la presentación de ese fotograma se realiza finalmente, lo que indica que la salida está de nuevo disponible para el descodificador.


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>API de vídeo de 
[Direct3D 12](direct3d-12-video-apis.md) 
 [Guía de programación de Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 
