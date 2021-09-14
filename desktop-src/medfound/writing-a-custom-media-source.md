---
description: En este tema se describe cómo implementar un origen multimedia personalizado en Microsoft Media Foundation.
ms.assetid: 82db6f32-ad94-4563-b8bd-8a5072c5b221
title: Escribir un origen multimedia personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8769fa16d4dcbfd3438b66f9a9e78c34274735a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127363539"
---
# <a name="writing-a-custom-media-source"></a>Escribir un origen multimedia personalizado

En este tema se describe cómo implementar un origen multimedia personalizado en Microsoft Media Foundation. Contiene las secciones siguientes:

-   [Crear el descriptor de presentación](#creating-the-presentation-descriptor)
-   [Iniciar el origen de medios](#starting-the-media-source)
    -   [Buscando](#seeking)
-   [Pausar el origen multimedia](#pausing-the-media-source)
-   [Generar datos de origen](#generating-source-data)
    -   [Solicitudes de ejemplo](#sample-requests)
    -   [Asignación de ejemplos](#allocating-samples)
    -   [Brechas en la secuencia](#gaps-in-the-stream)
-   [Apagar el origen de medios](#shutting-down-the-media-source)
-   [Orígenes en directo](#live-sources)
-   [Temas relacionados](#related-topics)

## <a name="creating-the-presentation-descriptor"></a>Crear el descriptor de presentación

El [**método IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) devuelve una copia del descriptor de presentación del origen. Para crear el descriptor de presentación, debe conocer el número de secuencias del contenido de origen y los posibles formatos de cada secuencia. Para cada secuencia, cree un descriptor de flujo como se muestra a continuación:

1.  Cree una matriz de tipos de medios. Cada tipo de medio de la matriz representa un formato posible para la secuencia. Para obtener más información sobre cómo crear tipos de medios, vea [Tipos de medios](media-types.md).
2.  Llame [**a MFCreateStreamDescriptor para**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) crear el descriptor de flujo. Pase la matriz de tipos de medios. La función devuelve un [**puntero IMFStreamDescriptor.**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)
3.  Llame [**a IMFStreamDescriptor::GetMediaTypeHandler para**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) obtener el controlador de tipo de medio del descriptor de secuencia.
4.  Llame [**a IMFMediaTypeHandler::SetCurrentMediaType para**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) establecer el formato de secuencia predeterminado. Use uno de los tipos de medios que creó en el paso 1. Por lo general, debe usar el formato con la máxima calidad.
5.  Opcionalmente, establezca atributos en el descriptor de flujo. Para obtener una lista de atributos que se aplican a los descriptores de secuencia, vea [Atributos de descriptor de flujo.](stream-descriptor-attributes.md)

Ahora cree el descriptor de presentación:

1.  Llame [**a MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) y pase la matriz de descriptores de flujo. La función devuelve un [**puntero IMFPresentationDescriptor.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
2.  Elija la selección de secuencia predeterminada mediante una llamada [**a IMFPresentationDescriptor::SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) para seleccionar una o varias secuencias. Se debe seleccionar al menos una secuencia en la configuración predeterminada.
3.  Opcionalmente, establezca atributos en el descriptor de presentación. Para obtener una lista de los atributos que se aplican a los descriptores de flujo, vea [Atributos del descriptor de presentación](presentation-descriptor-attributes.md).

Debe crear el descriptor de presentación una vez, ya sea al inicio o después de que el origen haya analizando suficientemente los datos de origen para determinar el contenido. El [**método CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) debe devolver una copia del descriptor de presentación. Para crear la copia, llame [**a IMFPresentationDescriptor::Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone). Devolver una copia impide que el cliente modifique el estado del descriptor de presentación original, como los atributos o la selección de secuencia. Sin embargo, tenga en cuenta que **Clone** crea una copia superficial, por lo que el cliente puede modificar potencialmente los descriptores de flujo subyacentes.

## <a name="starting-the-media-source"></a>Iniciar el origen de medios

El [**método IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) inicia el origen multimedia o busca una nueva posición. Una llamada a **Start provoca** una *búsqueda* cuando el estado anterior estaba en pausa o en ejecución, y se especifica una nueva hora de inicio. De lo contrario, **el método Start** produce un *inicio*. Cuando se **complete la** operación De inicio, envíe los siguientes eventos.

1.  Envíe un [evento MENewStream](menewstream.md) para cada nueva secuencia, es decir, cada secuencia que se deseleccionó previamente y ahora está seleccionada. Los datos del evento son un puntero a la secuencia.
2.  Envíe un [evento MEUpdatedStream](meupdatedstream.md) para cada secuencia que se seleccionó previamente y aún está seleccionada. Los datos del evento son un puntero a la secuencia. (No envíe un evento para secuencias deseleccionada).
3.  Si el origen está buscando, envíe un [evento MESourceSeeked.](mesourceseeked.md) De lo contrario, envíe [un evento MESourceStarted.](mesourcestarted.md) Los datos del evento son la hora de inicio especificada en el [**método**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) Start. Para el evento MESourceStarted, si la hora de inicio es VT EMPTY, establezca el atributo \_ MF EVENT SOURCE ACTUAL [**\_ \_ \_ \_ START**](mf-event-source-actual-start-attribute.md) en el evento. El valor del atributo es la hora de inicio real.
4.  Para cada secuencia, si el origen está buscando, envíe un [evento MEStreamSeeked.](mestreamseeked.md) De lo contrario, envíe [un evento MEStreamStarted.](mestreamstarted.md) Los datos del evento son la hora de inicio. (El origen multimedia puede poner en cola un evento en la secuencia mediante una llamada al método [**IMFMediaEventGenerator::QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent) de la secuencia).

Cuando se deseleccione una secuencia, apague la secuencia. La secuencia no debe poner en cola más eventos en ese momento.

El formato de hora del [**método Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) se especifica en el *parámetro pguidTimeFormat.* El formato de hora estándar, indicado por **GUID \_ NULL,** es unidades de 100 nanosegundos. Un origen de medios debe admitir este formato de hora.

### <a name="seeking"></a>Buscando

Al buscar, es posible que la posición inicial solicitada no esté en un límite de muestra exacto. Además, para el contenido comprimido, la posición inicial puede estar entre fotogramas clave. Una secuencia debe entregar muestras desde el punto más antiguo necesario para generar una muestra sin comprimir en la posición inicial solicitada. En el caso del vídeo, esto significa empezar desde el fotograma clave anterior. La canalización es responsable de quitar los fotogramas adicionales del descodificador, de modo que la reproducción se inicie en el momento solicitado.

La hora de inicio dada en los eventos de origen [(MESourceStarted,](mesourcestarted.md) [MESourceSeeked,](mesourceseeked.md) [MEStreamStarted](mestreamstarted.md)y [MEStreamSeeked)](mestreamseeked.md)es la hora de inicio solicitada (el valor especificado en el [**método Start),**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) independientemente de la posición de inicio real.

Por ejemplo, supongamos que los primeros fotogramas de una secuencia de vídeo tienen las siguientes características:



| Muestra     | 1       | 2       | 3        | 4        |
|------------|---------|---------|----------|----------|
| Time       | 33 ms | 66 ms | 100 ms | 133 ms |
| ¿Fotograma clave? | Sí     | No      | No       | Sí      |



 

Si se llama al método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) con un valor de 100 milisegundos, el origen debe generar vídeo a partir del fotograma 1, el primer fotograma clave antes de este tiempo. El evento de inicio seguirá indicando 100 milisegundos en los datos del evento.

## <a name="pausing-the-media-source"></a>Pausar el origen multimedia

El [**método IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) pausa el origen multimedia.

Mientras el origen está en pausa, una secuencia puede crear nuevos ejemplos y almacenarlos en una cola, pero la secuencia no entrega los ejemplos. Estas son algunas excepciones a esta regla:

-   Los orígenes en directo deben quitar los datos mientras están en pausa.
-   Si el origen obtiene datos de una red, podría pausar el servidor.

Si el cliente llama [**a IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) mientras el origen está en pausa, la solicitud también se pone en cola hasta que el origen se inicia de nuevo. No se deben descartar las solicitudes.

La pausa solo se permite desde el estado iniciado. De lo contrario, [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) debe devolver **MF E INVALID STATE \_ \_ \_ \_ TRANSITION**.

## <a name="generating-source-data"></a>Generar datos de origen

Media Foundation un modelo *de extracción*, lo que significa que las secuencias generan y entregan ejemplos en respuesta a las solicitudes de la canalización. Una secuencia puede entregar ejemplos cuando el origen multimedia se está ejecutando y la secuencia está seleccionada. Una secuencia entrega datos solo cuando el cliente solicita un nuevo ejemplo.

### <a name="sample-requests"></a>Solicitudes de ejemplo

El cliente solicita un nuevo ejemplo mediante una llamada [**a IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample). Esta es la secuencia de operaciones:

1.  El cliente llama [**a IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample). El argumento es un puntero a un objeto *de token* opcional que el cliente usa para realizar el seguimiento de la solicitud. El cliente implementa el token. Los tokens deben exponer **la interfaz IUnknown.** El cliente también puede pasar un puntero NULL en lugar de un token.
2.  Si el cliente proporcionó un token, el flujo multimedia llama a **AddRef** en el token y coloca el token en una cola de entrada y salida. El método devuelve y los pasos restantes se producen de forma asincrónica.

3.  Cuando hay más datos disponibles, la secuencia multimedia crea un nuevo ejemplo. (Este paso se describe con más detalle en la sección siguiente).
4.  El flujo multimedia extrae el primer token de la cola.
5.  Si el token no es **NULL,** la secuencia de medios establece el atributo [**MFSampleExtension \_ Token**](mfsampleextension-token-attribute.md) en el ejemplo multimedia. El valor del atributo es un puntero al token.
6.  La secuencia multimedia envía un [evento MEMediaSample.](memediasample.md) Los datos del evento son un puntero a la interfaz [**DESEJEMPLOEJEMPLO Del**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) ejemplo.
7.  Si el cliente proporcionó un token, el flujo multimedia llama **a Release en** el objeto de token.

Si el flujo multimedia no puede satisfacer la solicitud [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) del cliente, extrae el token de la cola y llama a **Release** en el token, pero no envía un evento [MEMediaSample.](memediasample.md)

El cliente puede usar el token para realizar un seguimiento del estado de la solicitud. Cuando el cliente recibe el [evento MEMediaSample,](memediasample.md) puede obtener el token del ejemplo y hacer coincidirlo con la solicitud original. El cliente también puede usar el token para detectar si el origen multimedia ha eliminado la solicitud. Si el recuento de referencias del token cae a cero y el flujo multimedia no envía un evento MEMediaSample, significa que se ha eliminado la solicitud.

En los pasos enumerados aquí se supone [**que el método RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) se implementa como una operación asincrónica. Si el método es sincrónico, no es necesario colocar el token de solicitud en una cola. Sin embargo, si la generación de datos tarda una cantidad significativa de tiempo, se recomienda un enfoque asincrónico, por ejemplo, si el origen lee datos de una secuencia de bytes.

La secuencia es responsable de almacenar en búfer los datos que se acumulan entre las llamadas a [**RequestSample.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)

Cuando el flujo multimedia llega al final de la secuencia, envía un [evento MEEndOfStream](meendofstream.md) después del último ejemplo. Una vez finalizada cada secuencia, el origen multimedia envía un [evento MEEndOfPresentation.](meendofpresentation.md) Una vez que una secuencia multimedia envía el evento MEEndOfStream, el [**método RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) devuelve **MF E END OF \_ \_ \_ \_ STREAM** hasta que se reinicia el origen.

### <a name="allocating-samples"></a>Asignación de ejemplos

Cuando la secuencia está lista para rellenar una solicitud de ejemplo pendiente, crea un nuevo ejemplo y agrega uno o varios búferes multimedia al ejemplo. Para obtener más información sobre cómo crear búferes multimedia, vea [Búferes multimedia](media-buffers.md).

La secuencia debe establecer la marca de tiempo y la duración, si se conoce. La marca de tiempo es relativa al origen. En la mayoría de los casos, el inicio del contenido corresponde a una marca de tiempo de cero. Por ejemplo, si el origen lee de un archivo multimedia, el inicio del archivo tendría una marca de tiempo de cero.

La marca de tiempo del ejemplo no es necesariamente igual al tiempo de presentación. La sesión multimedia se traduce del tiempo de origen al tiempo de presentación. En el caso de los datos comprimidos, la secuencia debe generar datos a partir del fotograma clave más cercano antes de la hora de inicio. Esto permite que el descodificador entregue el fotograma que aparece en la hora de inicio solicitada. (De lo contrario, el descodificador tendría que esperar hasta el siguiente fotograma clave).

Si la velocidad de reproducción es más rápida o más lenta que 1.0, la canalización ajusta la velocidad del reloj de presentación. El origen no ajusta las marcas de tiempo en los ejemplos.

El origen puede establecer información adicional sobre el ejemplo estableciendo atributos. Para obtener una lista de atributos de ejemplo, vea [Atributos de ejemplo.](sample-attributes.md)

### <a name="gaps-in-the-stream"></a>Espacios en la secuencia

Si una secuencia contiene un intervalo de longitud significativa, se recomienda que la secuencia envíe un [evento MEStreamTick.](mestreamtick.md) Este evento notifica al cliente que falta un ejemplo. Los datos del evento son la marca de tiempo de la muestra que falta, en unidades de 100 nanosegundos **(VT \_ I8).** Este evento puede hacer que los componentes de nivel inferior no tengan que esperar muestras que no lleguen. La secuencia puede enviar tantos eventos MEStreamTick como sea necesario para abarcar la brecha en la secuencia.

## <a name="shutting-down-the-media-source"></a>Apagar el origen multimedia

Cuando el cliente se ha terminado con el origen de medios, llama a [**ALMEDIASOURCE::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown). Dentro de este método, el origen de medios debe interrumpir los recuentos de referencias circulares. Normalmente, habrá referencias circulares entre el origen de medios y las secuencias multimedia.

Si usa la cola de eventos para implementar [**ELERMEDIAEventGenerator,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)llame a [**LA COLA DE EVENTOS DE LA COLA DE EVENTOS.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) Este método cierra la cola de eventos y señala a cualquier llamador que esté esperando un evento.

Después del cierre, todos los métodos del origen **devuelven MF \_ E \_ SHUTDOWN**, a excepción de **los métodos IUnknown.**

## <a name="live-sources"></a>Orígenes en directo

A partir Windows 7, Media Foundation automáticamente admite dispositivos de captura de audio y vídeo. En el caso del vídeo, el dispositivo debe proporcionar un minidriver de streaming de kernel (KS) en la categoría de captura de vídeo. Media Foundation la ruta de acceso pnP para enumerar el dispositivo. Para el audio, Media Foundation la API Windows multimedia (MMDevice) para enumerar los dispositivos de punto de conexión de audio. Si el dispositivo cumple estos criterios, no es necesario implementar un origen multimedia personalizado.

Sin embargo, es posible que desee implementar un origen multimedia personalizado para algún otro tipo de dispositivo u otro origen de datos en directo. Solo hay algunas diferencias entre un origen en directo y otros orígenes multimedia:

-   En el [**método MFMediaSource::GetCharacteristics,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics) devuelva la **marca MFMEDIASOURCE \_ IS \_ LIVE.**
-   El primer ejemplo debe tener una marca de tiempo de cero.
-   Los eventos y los estados de streaming se controlan igual que los orígenes multimedia, a excepción del estado en pausa.
-   Mientras esté en pausa, no ponga en cola ejemplos. Quitar los datos que se generan mientras están en pausa.
-   Normalmente, los orígenes en directo no admiten la búsqueda, el juego inverso ni el control de velocidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Orígenes multimedia](media-sources.md)
</dt> <dt>

[Tutorial: Escritura de un origen multimedia personalizado](tutorial--writing-a-custom-media-source.md)
</dt> </dl>

 

 



