---
description: En este tema se describe cómo implementar un origen multimedia personalizado en Microsoft Media Foundation.
ms.assetid: 82db6f32-ad94-4563-b8bd-8a5072c5b221
title: Escritura de un origen de medios personalizado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8769fa16d4dcbfd3438b66f9a9e78c34274735a5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "105707563"
---
# <a name="writing-a-custom-media-source"></a>Escritura de un origen de medios personalizado

En este tema se describe cómo implementar un origen multimedia personalizado en Microsoft Media Foundation. Contiene las secciones siguientes:

-   [Crear el descriptor de presentación](#creating-the-presentation-descriptor)
-   [Inicio del origen del medio](#starting-the-media-source)
    -   [Invoca](#seeking)
-   [Pausar el origen de medios](#pausing-the-media-source)
-   [Generar datos de origen](#generating-source-data)
    -   [Solicitudes de ejemplo](#sample-requests)
    -   [Asignar ejemplos](#allocating-samples)
    -   [Espacios en la secuencia](#gaps-in-the-stream)
-   [Apagar el origen del medio](#shutting-down-the-media-source)
-   [Orígenes en directo](#live-sources)
-   [Temas relacionados](#related-topics)

## <a name="creating-the-presentation-descriptor"></a>Crear el descriptor de presentación

El método [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) devuelve una copia del descriptor de presentación del origen. Para crear el descriptor de presentación, debe conocer el número de flujos en el contenido de origen y los posibles formatos de cada flujo. Para cada flujo, cree un descriptor de secuencia como se indica a continuación:

1.  Cree una matriz de tipos de medios. Cada tipo de medio de la matriz representa un posible formato para la secuencia. Para obtener más información sobre la creación de tipos de medios, consulte [tipos de medios](media-types.md).
2.  Llame a [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) para crear el descriptor de flujo. Pase la matriz de tipos de medios. La función devuelve un puntero [**IMFStreamDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor) .
3.  Llame a [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) para obtener el controlador de tipo de medio del descriptor de flujo.
4.  Llame a [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) para establecer el formato de flujo predeterminado. Use uno de los tipos de medios que creó en el paso 1. Por lo general, debe usar el formato con la máxima calidad.
5.  Opcionalmente, establezca atributos en el descriptor de flujo. Para obtener una lista de los atributos que se aplican a los descriptores de flujo, vea [los atributos del descriptor de flujo](stream-descriptor-attributes.md).

Ahora cree el descriptor de presentación:

1.  Llame a [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) y pase la matriz de descriptores de flujo. La función devuelve un puntero [**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) .
2.  Elija la selección de flujo predeterminada llamando a [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) para seleccionar una o más secuencias. Se debe seleccionar al menos un flujo en la configuración predeterminada.
3.  Opcionalmente, establezca los atributos del descriptor de presentación. Para obtener una lista de los atributos que se aplican a los descriptores de flujo, vea [atributos de descriptor de presentación](presentation-descriptor-attributes.md).

Debe crear el descriptor de presentación una vez, ya sea en el inicio o después de que el origen haya analizado lo suficiente de los datos de origen para determinar el contenido. El método [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) debe devolver una copia del descriptor de presentación. Para crear la copia, llame a [**IMFPresentationDescriptor:: Clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone). Al devolver una copia, se evita que el cliente modifique el estado del descriptor de la presentación original, como los atributos o la selección de la secuencia. Sin embargo, tenga en cuenta que **Clone** crea una copia superficial, por lo que el cliente puede modificar potencialmente los descriptores de flujo subyacentes.

## <a name="starting-the-media-source"></a>Inicio del origen del medio

El método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) inicia el origen del medio o busca en una nueva posición. Una llamada a **Start** produce una *búsqueda* cuando el estado anterior estaba en pausa o en ejecución y se especifica una nueva hora de inicio. De lo contrario, el método **Start** produce un *Inicio*. Cuando se complete la operación de **Inicio** , envíe los siguientes eventos.

1.  Envíe un evento [MENewStream](menewstream.md) para cada nuevo flujo, es decir, cada secuencia que se canceló previamente y que ahora está seleccionada. Los datos de evento son un puntero a la secuencia.
2.  Envíe un evento [MEUpdatedStream](meupdatedstream.md) para cada flujo que se seleccionó previamente y que todavía está seleccionado. Los datos de evento son un puntero a la secuencia. (No envía un evento para secuencias no seleccionadas).
3.  Si el origen está buscando, envíe un evento [MESourceSeeked](mesourceseeked.md) . De lo contrario, envíe un evento [MESourceStarted](mesourcestarted.md) . Los datos de evento son la hora de inicio que se especificó en el método de [**Inicio**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) . En el caso del evento MESourceStarted, si la hora de inicio es VT \_ vacío, establezca el atributo de [**\_ \_ \_ \_ Inicio real del origen de eventos MF**](mf-event-source-actual-start-attribute.md) en el evento. El valor del atributo es la hora de inicio real.
4.  En cada flujo, si el origen está buscando, envíe un evento [MEStreamSeeked](mestreamseeked.md) . De lo contrario, envíe un evento [MEStreamStarted](mestreamstarted.md) . Los datos del evento son la hora de inicio. (El origen multimedia puede poner en cola un evento en la secuencia llamando al método [**IMFMediaEventGenerator:: QueueEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-queueevent) del flujo).

Cuando se anule la selección de una secuencia, ciérrela. La secuencia no debe poner en cola más eventos en ese momento.

El formato de hora para el método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) se proporciona en el parámetro *pguidTimeFormat* . El formato de hora estándar, indicado por el **GUID \_ null**, es de 100 a nanosegundos. Un origen multimedia debe admitir este formato de hora.

### <a name="seeking"></a>Invoca

Al buscar, la posición de inicio solicitada podría no estar en un límite de ejemplo exacto. Además, para el contenido comprimido, la posición inicial puede estar entre fotogramas clave. Un flujo debe proporcionar ejemplos del primer punto necesario para generar un ejemplo sin comprimir en la posición de inicio solicitada. En el caso de vídeo, eso significa que se inicia desde el fotograma clave anterior. La canalización es responsable de quitar los fotogramas adicionales del descodificador, de modo que la reproducción se inicia a la hora solicitada.

La hora de inicio dada en los eventos de origen ([MESourceStarted](mesourcestarted.md), [MESourceSeeked](mesourceseeked.md), [MEStreamStarted](mestreamstarted.md)y [MEStreamSeeked](mestreamseeked.md)) es la hora de inicio solicitada (el valor proporcionado en el método de [**Inicio**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) ), independientemente de la posición inicial real.

Por ejemplo, supongamos que los primeros fotogramas de un flujo de vídeo tienen las siguientes características:



| Muestra     | 1       | 2       | 3        | 4        |
|------------|---------|---------|----------|----------|
| Time       | 33 MS | 66 MS | 100 ms | 133 MS |
| ¿Fotograma clave? | Sí     | No      | No       | Sí      |



 

Si se llama al método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) con un valor de 100 milisegundos, el origen debe generar el vídeo a partir del fotograma 1, el primer fotograma clave antes de este tiempo. El evento de inicio seguirá indicando 100 milisegundos en los datos de evento.

## <a name="pausing-the-media-source"></a>Pausar el origen de medios

El método [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) pone en pausa el origen del medio.

Mientras el origen está en pausa, una secuencia puede crear muestras nuevas y almacenarlas en una cola, pero la secuencia no entrega los ejemplos. Estas son algunas excepciones a esta regla:

-   Los orígenes en directo deben quitar los datos mientras están en pausa.
-   Si el origen obtiene datos de una red, es posible que PAUSE el servidor.

Si el cliente llama a [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) mientras el origen está en pausa, la solicitud también se pone en cola hasta que se inicia de nuevo el origen. No se deben quitar las solicitudes.

Solo se permite pausar desde el estado Iniciado. De lo contrario, [**PAUSE**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) debe devolver la **\_ \_ \_ \_ transición de estado no válida MF E**.

## <a name="generating-source-data"></a>Generar datos de origen

Media Foundation usa un *modelo de extracción*, lo que significa que las secuencias generan y proporcionan ejemplos en respuesta a las solicitudes de la canalización. Un flujo puede proporcionar ejemplos cuando se está ejecutando el origen multimedia y se selecciona la secuencia. Un flujo solo entrega datos cuando el cliente solicita un nuevo ejemplo.

### <a name="sample-requests"></a>Solicitudes de ejemplo

El cliente solicita un nuevo ejemplo llamando a [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample). Esta es la secuencia de operaciones:

1.  El cliente llama a [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample). El argumento es un puntero a un objeto de *token* opcional que el cliente utiliza para realizar el seguimiento de la solicitud. El cliente implementa el token. Los tokens deben exponer la interfaz **IUnknown** . El cliente también puede pasar un puntero NULL en lugar de un token.
2.  Si el cliente proporcionó un token, el flujo multimedia llama a **AddRef** en el token y coloca el token en una cola de primero en salir, primero en salir. El método devuelve y el resto de los pasos se producen de forma asincrónica.

3.  Cuando hay más datos disponibles, el flujo multimedia crea un nuevo ejemplo. (Este paso se describe con más detalle en la sección siguiente).
4.  El flujo multimedia extrae el primer token de la cola.
5.  Si el token no es **null**, el flujo de medios establece el atributo de [**\_ token MFSampleExtension**](mfsampleextension-token-attribute.md) en el ejemplo multimedia. El valor del atributo es un puntero al token.
6.  El flujo multimedia envía un evento [MEMediaSample](memediasample.md) . Los datos de evento son un puntero a la interfaz [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) del ejemplo.
7.  Si el cliente proporcionó un token, el flujo multimedia llama a **Release** en el objeto de token.

Si el flujo multimedia no puede satisfacer la solicitud de [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) del cliente, extrae el token de la cola y llama a **Release** en el token, pero no envía un evento [MEMediaSample](memediasample.md) .

El cliente puede usar el token para hacer un seguimiento del estado de la solicitud. Cuando el cliente recibe el evento [MEMediaSample](memediasample.md) , puede obtener el token del ejemplo y hacer coincidir con la solicitud original. El cliente también puede usar el token para detectar si el origen de medios ha quitado la solicitud. Si el recuento de referencias del token es cero y el flujo multimedia no envía un evento MEMediaSample, significa que la solicitud se ha quitado.

En los pasos que se enumeran aquí se supone que el método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) se implementa como una operación asincrónica. Si el método es sincrónico, no es necesario colocar el token de solicitud en una cola. Sin embargo, si la generación de datos tarda bastante tiempo, se recomienda un enfoque asincrónico, por ejemplo, si el origen lee datos de un flujo de bytes.

La secuencia es responsable del almacenamiento en búfer de los datos que se acumulan entre las llamadas a [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample).

Cuando el flujo multimedia alcanza el final de la secuencia, envía un evento [MEEndOfStream](meendofstream.md) después del último ejemplo. Una vez finalizada cada secuencia, el origen del medio envía un evento [MEEndOfPresentation](meendofpresentation.md) . Después de que una secuencia de medios envíe el evento MEEndOfStream, el método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) devuelve el **\_ \_ fin \_ de la \_ secuencia MF E** hasta que se reinicia el origen.

### <a name="allocating-samples"></a>Asignar ejemplos

Cuando el flujo está listo para rellenar una solicitud de ejemplo pendiente, crea un nuevo ejemplo y agrega uno o más búferes multimedia al ejemplo. Para obtener más información sobre la creación de búferes multimedia, consulte [búferes multimedia](media-buffers.md).

La secuencia debe establecer la marca de tiempo y la duración, si se conoce. La marca de tiempo es relativa al origen. En la mayoría de los casos, el inicio del contenido corresponde a una marca de tiempo de cero. Por ejemplo, si el origen lee desde un archivo multimedia, el inicio del archivo tendría una marca de tiempo de cero.

La marca de tiempo en el ejemplo no es necesariamente igual al tiempo de presentación. La sesión multimedia se traduce del tiempo de origen al tiempo de presentación. En el caso de los datos comprimidos, el flujo debe generar datos a partir del fotograma clave más cercano antes de la hora de inicio. Esto permite que el descodificador entregue el marco que aparece en la hora de inicio solicitada. (De lo contrario, el descodificador debe esperar hasta el siguiente fotograma clave).

Si la velocidad de reproducción es mayor o menor que 1,0, la canalización ajusta la velocidad del reloj de la presentación. El origen no ajusta las marcas de tiempo en las muestras.

El origen puede establecer información adicional sobre el ejemplo mediante el establecimiento de atributos. Para obtener una lista de los atributos de ejemplo, vea [atributos de ejemplo](sample-attributes.md).

### <a name="gaps-in-the-stream"></a>Espacios en la secuencia

Si una secuencia contiene un intervalo de longitud significativa, se recomienda que el flujo envíe un evento [MEStreamTick](mestreamtick.md) . Este evento notifica al cliente que falta un ejemplo. Los datos de evento son la marca de tiempo de la muestra que falta, en unidades de 100-nanosegundos (**VT \_ i8**). Este evento puede guardar los componentes de nivel inferior desde la espera de las muestras que no llegarán. El flujo puede enviar tantos eventos MEStreamTick como sea necesario para abarcar la brecha en la secuencia.

## <a name="shutting-down-the-media-source"></a>Apagar el origen del medio

Cuando el cliente se realiza mediante el origen de medios, llama a [**IMFMediaSource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown). Dentro de este método, el origen de medios debe romper cualquier recuento de referencias circulares. Normalmente, habrá referencias circulares entre el origen multimedia y los flujos multimedia.

Si usa la cola de eventos para implementar [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator), llame a [**IMFMediaEventQueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) en la cola de eventos. Este método cierra la cola de eventos y señala cualquier llamador que esté esperando actualmente un evento.

Después del apagado, todos los métodos del origen devuelven el **\_ \_ cierre de MF E**, con la excepción de los métodos **IUnknown** .

## <a name="live-sources"></a>Orígenes en directo

A partir de Windows 7, Media Foundation admite automáticamente dispositivos de captura de audio y vídeo. En el caso de vídeo, el dispositivo debe proporcionar un minicontrolador de streaming de kernel (KS) en la categoría captura de vídeo. Media Foundation usa la ruta de acceso de PnP para enumerar el dispositivo. En el caso de audio, Media Foundation usa la API de dispositivo multimedia de Windows (MMDevice) para enumerar los dispositivos de punto de conexión de audio. Si el dispositivo cumple estos criterios, no es necesario implementar un origen de medios personalizado.

Sin embargo, es posible que desee implementar un origen de medios personalizado para algún otro tipo de dispositivo u otro origen de datos en directo. Solo hay algunas diferencias entre un origen en directo y otros orígenes multimedia:

-   En el método [**IMFMediaSource:: GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics) , devuelve **MFMEDIASOURCE \_ es \_ Live** Flag.
-   El primer ejemplo debe tener una marca de tiempo de cero.
-   Los eventos y los Estados de streaming se administran igual que los orígenes de medios, con la excepción del estado de pausa.
-   Mientras está en pausa, no poner en cola ejemplos. Quitar los datos que se generan mientras están en pausa.
-   Los orígenes en directo normalmente no admiten la búsqueda, la reproducción inversa o el control de velocidad.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Orígenes multimedia](media-sources.md)
</dt> <dt>

[Tutorial: escribir un origen de medios personalizado](tutorial--writing-a-custom-media-source.md)
</dt> </dl>

 

 



