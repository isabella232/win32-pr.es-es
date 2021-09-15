---
description: Este artículo contiene instrucciones generales para usar las API de vídeo de Direct3D 12.
ms.assetid: ''
title: Introducción al vídeo de Direct3D 12
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: b21587f2784b34131da9c050655b6f3fbe43582d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127573420"
---
# <a name="direct3d-12-video-overview"></a>Introducción al vídeo de Direct3D 12

Este artículo contiene instrucciones generales para usar las API de vídeo de Direct3D 12.

## <a name="about-direct3d-12-video"></a>Acerca de Direct3D 12 Video

La interfaz de vídeo de Direct3D 12 proporciona una nueva manera de que las aplicaciones implementen lacodización y el proceso de vídeo. La interfaz de Direct3D 12 es diferente de la interfaz anterior de Direct3D 11 porque se diseñó para ser coherente con los principios y el estilo de Direct3D 12, que incluye lo siguiente:

- Proporcionar a los desarrolladores más control
 - Asignación de memoria accesible por hardware
 - Subprocesos de CPU usados para generar & enviar comandos
   - Generación y envío independientes
   - Sin bloqueo
 - Programación del trabajo de hardware
- Abarca la funcionalidad existente, incluida la mayoría de las funcionalidades de vídeo de Direct3D 11, pero al mismo tiempo, tiene en cuenta la simplicidad y la facilidad de uso.
- Potencia y rendimiento de las aplicaciones principales de Direct3D 12 iguales o superiores a Direct3D 11
- Coherencia con otras API de Direct3D 12
- Interoperabilidad con las API de gráficos existentes


## <a name="video-decoding"></a>Video decoding

En las secciones siguientes se describen algunas de las tareas implicadas en la implementación de lacoding de vídeo de Direct3D 12.

### <a name="query-for-decoding-capabilities"></a>Consulta de funcionalidades de decoding

Llame [a ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) para comprobar los detalles de soporte técnico de las operaciones de decodificación de vídeo de Direct3D 12. Pase un valor de la [enumeración D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) para especificar la característica para la que solicita información de soporte técnico.

### <a name="create-the-video-decoder"></a>Creación del descodificador de vídeo

Llame [a ID3D12VideoDevice::CreateVideoDecoder](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder) para crear una instancia de la interfaz [ID3D12VideoDecoder.](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoder) El descodificador contiene el estado de una sesión de descodificación, incluidos los datos relacionados con la referencia, como los vectores de movimiento.  En caso de un cambio de resolución o un [cambio MaxDecodePictureBufferCount,](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc) se vuelve a crear el objeto descodificador. El ancho y alto de descodificación especifican la resolución de secuencia nativa antes de cualquier escala.  El número máximo de búferes de imagen de descodificación (DPB) especifica el mayor número de DPB que se puede usar sin volver a crear el descodificador de vídeo.

El descodificador se puede usar para registrar comandos de varias listas de comandos, pero solo se puede asociar a una lista de comandos a la vez.  La aplicación es responsable de sincronizar el acceso al descodificador.

### <a name="create-the-video-decoder-heap"></a>Creación del montón de descodificador de vídeo 

Llame [a ID3D12VideoDevice::CreateVideoDecoderHeap](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) para crear una instancia de la interfaz [ID3D12VideoDecoderHeap.](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoderheap) Este objeto contiene el estado y los recursos del controlador dependientes de la resolución.

### <a name="decoding-a-frame"></a>Decoding a frame

Todos los parámetros de entrada y salida para las operaciones de procesamiento de vídeo se organizan en una estructura de parámetros de [entrada,](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS y una estructura de parámetros de [salida, D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments).
La aplicación administra los marcos de referencia y, como tal, debe establecer los fotogramas de referencia para cada operación de decodificación.
Cuando la lista de comandos se grabe correctamente, llame a [ID3D12CommandQueue::ExecuteCommandLists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) en la cola de comandos de vídeo para enviar lacoding de fotogramas a la GPU.


### <a name="enabling-decoder-output-conversions"></a>Habilitación de conversiones de salida del descodificador
Si el descodificador admite la conversión, habilite las conversiones deseadas rellenando correctamente [la D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) estructura. El formato y las resoluciones de la salida deseada frente a la salida nativa del descodificador se comunican a través de la diferencia en el espacio de colores y las resoluciones especificadas en los parámetros de conversión.

##  <a name="querying-decoding-status"></a>Consulta del estado de lacoding 
Use los métodos [ID3D12VideoDecodeCommandList::BeginQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery) e [ID3D12VideoDecodeCommandList::EndQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery) para consultar el estado de la operación de descodificación.

La [D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics) se usa para describir las estadísticas de descodificación de vídeo. Para obtener una instancia de esta estructura, llame a [ID3D12VideoDecodeCommandList::EndQuery](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery), pasando el valor de tipo de consulta del [montón D3D12_QUERY_TYPE_VIDEO_DECODE_STATISTIC](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Tenga en cuenta que esta consulta no [usa ID3D12VideoDecodeCommandList::BeginQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery).

## <a name="video-processing"></a>Procesamiento de vídeo

Las API de vídeo de Direct3D 12 toman un enfoque simplificado para el procesamiento de vídeo, lo que elimina las características de Direct3D 11 que no se usaron ampliamente y elimina las comprobaciones de funcionalidad para las características que son obligatorias en todos los dispositivos. Se elimina el proceso de enumeración para el procesamiento de vídeo. En su lugar, llame a [ID3D12VideoDevice::CheckFeatureSupport,](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) lo que permite a una aplicación identificar las funcionalidades del procesador de vídeo. El vídeo deseado, el entrelazmiento, los formatos estéreo y las velocidades se proporcionan como entrada para **CheckFeatureSupport.**

### <a name="removed-capabilities"></a>Funcionalidades eliminadas

Las siguientes funcionalidades de Direct3D 11 no se admiten en el procesamiento de vídeo de Direct3D 12:
- Tarifas personalizadas.  En su lugar, hay una velocidad de entrada y salida dada durante la grabación del comando [ID3D12VideoProcessCommandList::P rocessFrames.](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes)
- Ahora solo hay dos modos de desinteresado disponibles: [BOB](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags) y [CUSTOM.](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags) Se han eliminado otros modos. CUSTOM es un modo de desinterlazado de alta calidad proporcionado por el proveedor de hardware.
- Todos los formatos estéreo opcionales [de D3D11_VIDEO_PROCESSOR_STEREO_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_caps) ya no se admiten. En su lugar, [nono](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format), [horizontal,](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) [vertical](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format)y [independiente](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) son obligatorios para todos los dispositivos de hardware si se admite estéreo.
- No hay ningún equivalente para [D3D11_VIDEO_PROCESSOR_FORMAT_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_format_caps) o [D3D11_VIDEO_PROCESSOR_AUTO_STREAM_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_auto_stream_caps). En su lugar, los formatos de entrada y salida son argumentos para la creación del procesador de vídeo y, en ese momento, se debe saber si el procesador de vídeo puede o no puede realizar la operación con el formato especificado. El [D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_auto_processing_flags) se usa para indicar si las características de procesamiento automático están disponibles.
- No hay ningún equivalente para [D3D11_VIDEO_PROCESSOR_CAPS_LEGACY](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps).
- No hay ningún equivalente para [D3D11_VIDEO_PROCESSOR_CAPS_CONSTRICTION](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps).
- Al convertir de estéreo a mono, se supone que la vista de línea base es 0.
- El procesamiento de vídeo de Direct3D 12 no admite la conversión de mono a estéreo y no se admite el desplazamiento mono. 


### <a name="creating-a-video-processor"></a>Creación de un procesador de vídeo

Llame [a ID3D12VideoDevice::CreateVideoProcessor](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor) para crear una instancia de [ID3D12VideoProcessor](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoprocessor). El procesador de vídeo contiene el estado de una sesión de procesamiento de vídeo, incluida la memoria intermedia necesaria, los datos de procesamiento almacenados en caché u otro espacio de trabajo temporal. Los argumentos de creación del procesador de vídeo especifican qué operaciones se realizan o están disponibles en la hora [ID3D12VideoProcessCommandList1::P rocessFrames1.](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1)  Las asignaciones de controladores para realizar la operación de proceso de vídeo (por ejemplo, los intermedios) se asignan en el momento de la creación del procesador de vídeo.  Use [D3D12_FEATURE_VIDEO_PROCESSOR_SIZE](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) para determinar el tamaño de asignación del procesador de vídeo de antemano.

El procesador de vídeo solo se puede usar para grabar comandos de varias listas de comandos, pero solo se puede asociar a una lista de comandos a la vez.  La aplicación es responsable de sincronizar el acceso al procesador de vídeo.  La aplicación también debe grabar comandos de procesamiento de vídeo en el procoesor de vídeo en el orden en que se ejecutan en la GPU.

Todos los argumentos de entrada y salida para las operaciones de procesamiento de vídeo se organizan en una estructura de argumentos de entrada, [D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)y una estructura de argumentos de [salida, D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments). La aplicación debe llamar a [ID3D12VideoProcessCommandList::P rocessFrames](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) para grabar la operación de procesamiento de vídeo que quiere ejecutar. 

Cuando se registra la lista de comandos, llame a [ID3D12CommandQueue::ExecuteCommandLists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) en la cola de comandos de vídeo para enviar el procesamiento de fotogramas a la GPU.


## <a name="tiers"></a>Niveles

El vídeo de Direct3D 12 define niveles que agrupan las funcionalidades de los dispositivos de hardware, de modo que la aplicación pueda tener menos rutas de acceso de código para satisfacer la variedad de hardware. Los niveles se especifican con la enumeración [D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier) datos.

En todos los niveles, estará disponible lo siguiente:

- No es necesario recrear el descodificador en los cambios de resolución. Solo es necesario volver a crear el montón del descodificador al cambiar la resolución.
- La aplicación administrará todos los fotogramas de referencia. Esto permite al sistema ahorrar memoria, ya que no es necesario asignar el número máximo de DPB en el momento de la creación del descodificador en algunos niveles, y proporciona flexibilidad a las aplicaciones en escenarios de cambio de resolución.

Tenga en cuenta que los niveles son superconjuntos. Una aplicación puede decidir realizar el nivel 1 y no usar las características de nivel superior, lo que se permite, pero puede que no proporcione un rendimiento óptimo. Para obtener más información sobre las funcionalidades asociadas a diferentes niveles, [consulte D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier).

## <a name="reference-frames"></a>Marcos de referencia

Con el vídeo de Direct3D 12, los fotogramas de referencia se pasan explícitamente. Esto permite un uso claro de la matriz de texturas o matrices de texturas al decodificar fotogramas. No es necesario que la aplicación pase exactamente el mismo identificador de recursos cuando se usa como referencia; Por ejemplo, puede decidir copiar un recurso en otro y, a continuación, pasar la copia en lugar del original. El controlador sigue utilizando los índices *RefFrameList* y *CurrPic* de DXVA para almacenar los datos pertinentes para cada fotograma descodificado.


## <a name="directx-12-fences"></a>Barreras de DirectX 12

En DirectX 12, la aplicación es responsable de sincronizar el acceso a sus búferes. En el caso de la decodificación, será necesario agregar barreras a los búferes de entrada y a los búferes de salida. Cada barrera tiene un valor asociado y se usa para la sincronización de la CPU y los motores de hardware. Para obtener más información, [vea Using Resource Barriers to Synchronize Resource States in Direct3D 12 ( Uso de barreras de recursos para sincronizar estados de recursos en Direct3D 12).](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12)

Una implementación típica tendrá una barrera para cada búfer de entrada. En el caso de los búferes de entrada, es posible que el búfer esté disponible antes de que se haga todo el proceso de descodización. El sistema omitirá este caso y asumirá que el búfer de entrada está disponible cuando se realiza lacoding.
Una implementación también normalmente tendrá una barrera para cada búfer de salida. En el caso de enviar la salida al compositor, por ejemplo, se necesita una barrera que se señale cuando finalmente se realiza esa presentación de ese marco, lo que indica que la salida está de nuevo disponible para el descodificador.


## <a name="related-topics"></a>Temas relacionados

<dl> <dt>API de vídeo 
[de Direct3D 12](direct3d-12-video-apis.md) 
 [Media Foundation de programación](media-foundation-programming-guide.md)
</dt> </dl>

 

 
