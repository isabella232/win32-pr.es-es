---
description: Los receptores de medios son los objetos de canalización que reciben datos multimedia.
ms.assetid: a0fbce1b-0a16-4449-9eca-906fd9056a1c
title: Receptores de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9394cbfd49a631d59b9296202a2b6ca7a868869
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104361848"
---
# <a name="media-sinks"></a>Receptores de medios

Los *receptores de medios* son los objetos de canalización que reciben datos multimedia. Un receptor de medios es el destino de una o más secuencias de multimedia. Los receptores de medios se dividen en dos categorías generales:

-   Un *representador* es un receptor de medios que presenta los datos para la reproducción. El representador de vídeo mejorado (EVR) muestra fotogramas de vídeo y el representador de audio reproduce secuencias de audio a través de la tarjeta de sonido u otro dispositivo de audio.

-   Un *receptor de archivo* es un receptor de medios que escribe datos en un archivo u otro almacenamiento.

La diferencia principal entre ellos es que un receptor de archivo no utiliza los datos con una velocidad de reproducción fija. En su lugar, escribe los datos que recibe lo más rápido posible.

Los receptores de medios exponen la interfaz [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) . Cada receptor de medios contiene uno o varios *receptores de secuencias*. Cada receptor de la secuencia recibe los datos de una secuencia. Los receptores de flujo exponen la interfaz [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) . Normalmente, una aplicación no crea receptores de medios directamente. En su lugar, la aplicación crea uno o varios objetos de activación, que la sesión multimedia utiliza para crear el receptor. Todas las demás operaciones del receptor se controlan mediante la sesión de medios y la aplicación no llama a ningún método en el receptor de medios ni en ninguno de los receptores de flujo. Para obtener más información sobre los objetos de activación, vea [objetos de activación](activation-objects.md).

Lea el resto de este tema si está escribiendo un receptor de multimedia personalizado o si desea usar un receptor de medios directamente sin la sesión multimedia.

-   [Receptores de flujo](#stream-sinks)
-   [Reloj de presentación](#presentation-clock)
-   [Formatos de secuencia](#stream-formats)
-   [Flujo de datos](#data-flow)
-   [Marcadores](#markers)
-   [Cambios de estado](#state-changes)
-   [Finalizando](#finalizing)
-   [Apagar](#shutting-down)
-   [Interfaces del receptor de medios](#media-sink-interfaces)
-   [Interfaces del receptor de secuencias](#stream-sink-interfaces)
-   [Eventos de receptor de secuencias](#stream-sink-events)
-   [Temas relacionados](#related-topics)

## <a name="stream-sinks"></a>Receptores de flujo

Un receptor de medios puede tener un número fijo de receptores de secuencias, o puede admitir la adición y eliminación de receptores de flujo. Si tiene un número fijo de receptores de secuencias, el método [**IMFMediaSink:: GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) devuelve la marca de \_ secuencias fijas MEDIASINK \_ . De lo contrario, puede Agregar y quitar receptores de flujo. Para agregar un nuevo receptor de la secuencia, llame a [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink). Para quitar un receptor de flujo, llame a [**IMFMediaSink:: RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink). La \_ marca MEDIASINK Fixed \_ streams indica que el receptor multimedia no admite estos dos métodos. (Es posible que admita algún otro método para configurar el número de secuencias, por ejemplo, estableciendo los parámetros de inicialización cuando se crea el receptor). La lista de receptores de secuencia está ordenada. Para enumerarlos por valor de índice, llame al método [**IMFMediaSink:: GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) .

Los receptores de secuencias también tienen identificadores. Los identificadores de flujo son únicos en el receptor de medios, pero no tienen que ser consecutivos. Dependiendo del receptor de medios, los identificadores de flujo podrían tener algún significado relacionado con el contenido. Por ejemplo, un receptor de archivo podría escribir los identificadores de secuencia en el encabezado del archivo. De lo contrario, son arbitrarios. Para obtener un receptor de flujo mediante su identificador, llame a [**IMFMediaSink:: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid).

## <a name="presentation-clock"></a>Reloj de presentación

La velocidad a la que un receptor de medios consume muestras se controla mediante el reloj de la [presentación](presentation-clock.md). La sesión multimedia selecciona el reloj de la presentación y lo establece en el receptor de medios llamando al método [**IMFMediaSink:: SetPresentationClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-setpresentationclock) del receptor de medios. El reloj de la presentación debe establecerse en el receptor de medios antes de que pueda comenzar la transmisión por secuencias. Cada receptor de medios requiere un reloj de presentación para ejecutarse. El receptor de medios usa el reloj de presentación para dos propósitos:

-   Para recibir notificaciones cuando se inicia o se detiene el streaming. El receptor de medios recibe estas notificaciones a través de la interfaz [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) , que todos los receptores de medios deben implementar.

-   Para determinar cuándo debe representar los ejemplos. Cuando el receptor de medios recibe un nuevo ejemplo, obtiene la marca de tiempo del ejemplo e intenta representar el ejemplo en ese momento de presentación.

El reloj de la presentación deriva sus horas de reloj de otro objeto denominado *origen de tiempo de presentación*. Los orígenes de tiempo de presentación exponen la interfaz [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) . Algunos receptores de medios tienen acceso a un reloj preciso, de modo que exponen esta interfaz. Esto significa que un receptor de medios podría programar muestras con un tiempo proporcionado por su propio reloj. Sin embargo, el receptor de medios no puede suponer que este sea el caso. Siempre debe usar el tiempo desde el reloj de la presentación, independientemente de si el reloj de la presentación está controlado por el propio receptor de medios o por algún otro reloj.

Si un receptor de medios no puede coincidir con las tasas con un reloj que no sea el suyo propio, el método [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) devuelve MEDIASINK \_ no puede \_ coincidir con la \_ marca del reloj. Si esta marca está presente y el reloj de la presentación utiliza un origen de tiempo de presentación diferente, es probable que el receptor de medios funcione mal. Por ejemplo, podría producirse un problema durante la reproducción.

Un receptor sin *velocidad* es un receptor de medios que omite las marcas de tiempo de las muestras y consume datos en cuanto llega cada ejemplo. Un receptor de medios sin velocidad devuelve la \_ marca sin tasa de MEDIASINK del método [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) . Normalmente, esta marca se aplica a los receptores de archivo. Si cada receptor de medios de la canalización no tiene frecuencia, la sesión multimedia utiliza un reloj de presentación sin velocidad especial. Este reloj se ejecuta tan pronto como los receptores consumen ejemplos.

## <a name="stream-formats"></a>Formatos de secuencia

Antes de que el receptor de medios pueda recibir ejemplos, el cliente debe establecer el tipo de medio en los receptores de la secuencia. Para establecer el tipo de medio, llame al método [**IMFStreamSink:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-getmediatypehandler) del receptor de la secuencia. Este método devuelve un puntero a la interfaz [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) . Use esta interfaz para obtener la lista de tipos de medios preferidos, obtener el tipo de medio actual y establecer el tipo de medio.

Para obtener la lista de tipos de medios preferidos, llame a [**IMFMediaTypeHandler:: GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex). Los tipos preferidos se deben tomar como una sugerencia para el cliente. La lista puede estar incompleta o incluir tipos de medios parciales. Un tipo de medio parcial es aquél que no tiene todos los atributos necesarios para describir un formato válido. Por ejemplo, un tipo de vídeo parcial podría especificar el espacio de color y la profundidad de bits, pero no el ancho o el alto de la imagen. Un tipo de audio parcial puede especificar el formato de compresión y la velocidad de muestra, pero no el número de canales de audio.

Para obtener el tipo de medio actual del receptor de flujo, llame a [**IMFMediaTypeHandler:: GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype). Cuando se crea por primera vez un receptor de flujo, es posible que tenga un tipo de medio predeterminado ya establecido o que no tenga ningún tipo de medio hasta que el cliente establezca uno.

Para establecer el tipo de medio, llame a [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype). Es posible que algunos receptores de secuencias no admitan el cambio del tipo después de que se haya establecido. Por lo tanto, resulta útil probar los tipos de medios antes de establecerlos. Para probar si el receptor de medios aceptará un tipo de medio (sin establecer el tipo), llame a [**IMFMediaTypeHandler:: IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).

## <a name="data-flow"></a>Data Flow

Los receptores de medios usan un *modelo de extracción*, lo que significa que los receptores de la secuencia solicitan datos según lo necesiten. El cliente debe responder a tiempo para evitar los problemas.

Algunos receptores de *medios admiten* la reversión. La preprocesamiento es el proceso de asignar datos al receptor de medios antes de que se inicie el reloj de presentación. Si un receptor de medios admite la reversión, el receptor de medios expone la interfaz [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) y el método [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) devuelve la \_ marca de \_ preroll MEDIASINK. La garantiza que el receptor de medios está listo para presentar el primer ejemplo cuando se inicia el reloj de presentación. Se recomienda que el cliente siempre se previerta en caso de que el receptor de medios lo admita, ya que puede evitar problemas o interrupciones durante la reproducción.

El flujo de datos a un receptor de medios funciona de la siguiente manera:

1.  El cliente establece los tipos de medios y el reloj de la presentación. El receptor de medios se registra a sí mismo con el reloj de presentación para recibir notificaciones sobre los cambios de estado de reloj.
2.  Opcionalmente, el cliente consulta para [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll). Si el receptor de medios expone esta interfaz, el cliente llama a [**IMFMediaSinkPreroll:: NotifyPreroll**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasinkpreroll-notifypreroll). De lo contrario, el cliente omite el paso 5.
3.  Cada receptor de la secuencia envía uno o más eventos [MEStreamSinkRequestSample](mestreamsinkrequestsample.md) . En respuesta a cada uno de estos eventos, el cliente obtiene la siguiente muestra de datos para esa secuencia y llama a [**IMFStreamSink::P rocesssample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample).
4.  Cuando cada receptor de la secuencia recibe suficientes datos de prescrito, envía un evento [MEStreamSinkPrerolled](mestreamsinkprerolled.md) .
5.  El cliente llama a [**IMFPresentationClock:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) para iniciar el reloj de la presentación.
6.  El reloj de la presentación notifica al receptor de medios que se está iniciando el reloj llamando a [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart).
7.  Para obtener más datos, cada receptor de flujo envía eventos [MEStreamSinkRequestSample](mestreamsinkrequestsample.md) . En respuesta a cada uno de estos eventos, el cliente obtiene el ejemplo siguiente y llama a [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample). Este paso se repite hasta que finaliza la presentación.

La mayoría de los receptores de medios procesan ejemplos de forma asincrónica, por lo que los receptores de secuencias pueden enviar más de una solicitud de ejemplo a la vez.

Durante el streaming, el cliente puede llamar a [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) y [**IMFStreamSink:: Flush**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-flush) en cualquier momento. Los marcadores se describen en la sección siguiente. El vaciado hace que el receptor de la secuencia Quite cualquier ejemplo que haya puesto en cola pero que no se haya representado todavía.

## <a name="markers"></a>Marcadores

Los marcadores proporcionan una manera para que el cliente indique puntos específicos en la secuencia. Un marcador consta de la siguiente información:

-   El tipo de marcador, definido como miembro de la enumeración de [**\_ \_ tipo de marcador MFSTREAMSINK**](/windows/desktop/api/mfidl/ne-mfidl-mfstreamsink_marker_type) .
-   Datos asociados al marcador. El significado de los datos depende del tipo de marcador. Algunos tipos de marcador no tienen datos.
-   Datos opcionales para el propio uso del cliente.

Para colocar un marcador, el cliente llama a [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker). El receptor de la secuencia finaliza el procesamiento de cualquier ejemplo que haya recibido antes de la llamada a **PlaceMarker** y, a continuación, envía un evento [MEStreamSinkMarker](mestreamsinkmarker.md) .

La mayoría de los receptores de medios mantienen una cola de ejemplos pendientes, que se procesan de forma asincrónica. Los eventos de marcador se deben serializar con procesamiento de ejemplo, por lo que el receptor de medios debe colocar los marcadores en la misma cola. Por ejemplo, supongamos que el cliente realiza las llamadas a métodos siguientes:

1.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (ejemplo \# 1)
2.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (ejemplo \# 2)
3.  [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) (marcador \# 1)
4.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (ejemplo \# 3)
5.  [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) (marcador \# 2)

En este ejemplo, el receptor del flujo debe enviar el evento [MEStreamSinkMarker](mestreamsinkmarker.md) para el marcador \# 1 después de procesar el ejemplo \# 2 y el evento para el marcador \# 2 después de procesar el ejemplo \# 3.

Si el cliente vacía un receptor de flujo, el receptor de flujo procesa inmediatamente cualquier marcador que estuviera en la cola. Establece el código de estado en E \_ anular en estos eventos.

Algunos marcadores contienen información que es relevante para el receptor de medios:

-   **MFSTREAMSINK \_ \_Marca de marcador**: indica que hay un hueco en la secuencia. El ejemplo siguiente será una discontinuidad.
-   **MFSTREAMSINK \_ MARCADOR \_ ENDOFSEGMENT**: indica el final de un segmento o el final de una secuencia. El ejemplo siguiente (si existe) puede ser una discontinuidad.
-   **MFSTREAMSINK \_ \_Evento de marcador**: contiene un evento. Dependiendo del tipo de evento y la implementación del receptor de medios, el receptor de medios podría controlar el evento u omitirlo.

## <a name="state-changes"></a>Cambios de estado

A un receptor de medios se le notifican los cambios de estado en el reloj de la presentación a través de la interfaz [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) del receptor de medios. Cuando el cliente establece el reloj de la presentación, el receptor de medios llama a [**IMFPresentationClock:: AddClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) para registrarse para recibir notificaciones del reloj. En la tabla siguiente se resume cómo se comporta un receptor de medios en respuesta a los cambios de estado de reloj.



| Cambio de estado del reloj                                         | Procesamiento de ejemplo                                                                                                                                                                                                                                             | Procesamiento de marcadores                                                                                                                                                                                   |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | Los ejemplos de procesos cuya marca de tiempo es igual o posterior a la hora de inicio del reloj.                                                                                                                                                                              | Envíe el evento [MEStreamSinkMarker](mestreamsinkmarker.md) cuando se hayan procesado todos los ejemplos recibidos antes del marcador.                                                                 |
| [**OnClockPause**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause)     | El receptor de medios puede producir un error de [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) mientras está en pausa.<br/> Si el receptor de medios acepta ejemplos mientras está en pausa, debe ponerlos en cola hasta que se reinicie el reloj. No procese ningún ejemplo en cola mientras esté en pausa.<br/> | Si hay ejemplos en cola, coloque los marcadores en la misma cola. Envíe el evento de marcador cuando se reinicie el reloj.<br/> De lo contrario, envíe el evento de marcador inmediatamente.<br/>                    |
| [**OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | Procese cualquier ejemplo que se puso en cola mientras estaba en pausa y, a continuación, trate lo mismo que [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart).                                                                                                                         | Envíe eventos [MEStreamSinkMarker](mestreamsinkmarker.md) para marcadores en cola (serializados con procesamiento de ejemplo) y, a continuación, trate el mismo como [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart). |
| [**OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | Quitar todos los ejemplos en cola. Se puede producir un error en otras llamadas a [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) .                                                                                                                                                      | Enviar eventos de marcador en cola. En las llamadas posteriores a [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker), envíe el evento de marcador inmediatamente.                                                              |



 

Además, los receptores de secuencias deben enviar los eventos siguientes cuando hayan completado las transiciones de estado:

-   [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart), [**OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart): evento [MEStreamSinkStarted](mestreamsinkstarted.md)
-   [**OnClockPause**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause): evento [MEStreamSinkPaused](mestreamsinkpaused.md)
-   [**OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop): evento [MEStreamSinkStopped](mestreamsinkstopped.md)

## <a name="finalizing"></a>Finalizando

Algunos receptores de medios requieren un paso de procesamiento adicional después de que se entregue la última muestra. Normalmente, este requisito se aplica a los receptores de archivo, que deben escribir encabezados o índices en el archivo. Si un receptor de medios requiere un procesamiento final, expone la interfaz [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink) .

Después de que el cliente entregue el último ejemplo, el cliente consulta esta interfaz. Si el receptor de medios admite la interfaz, el cliente llama a [**IMFFinalizableMediaSink:: BeginFinalize**](/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-beginfinalize) para realizar el procesamiento final de forma asincrónica. Este método sigue el modelo asincrónico de Media Foundation estándar, que se describe en [métodos de devolución de llamada asincrónica](asynchronous-callback-methods.md). El receptor de medios puede suponer que el cliente llamará a **BeginFinalize**. Si no se llama a **BeginFinalize** , se puede producir un archivo creado incorrectamente.

## <a name="shutting-down"></a>Apagar

Cuando el cliente se realiza mediante el receptor de medios, el cliente llama a [**IMFMediaSink:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown). Dentro de este método, el receptor de medios debe romper cualquier recuento de referencias circulares. Normalmente, habrá referencias circulares entre el receptor de medios y los receptores de flujo.

Si está utilizando el objeto auxiliar de cola de eventos para implementar [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator), llame a [**IMFMediaEventQueue:: Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) en la cola de eventos. Este método cierra la cola de eventos y señala cualquier llamador que esté esperando actualmente un evento.

Después del apagado, todos los métodos del receptor multimedia devuelven \_ \_ el cierre de MF E, con la excepción de los métodos **IUnknown** .

## <a name="media-sink-interfaces"></a>Interfaces del receptor de medios

En la tabla siguiente se enumeran las interfaces estándar que los receptores de medios pueden exponer a través de **QueryInterface**. Los receptores de medios también pueden exponer interfaces personalizadas.



| Interfaz                                                      | Descripción                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                           | La interfaz principal para los receptores de medios. (Requerido)                                            |
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                 | Se usa para notificar al receptor de medios cuando el reloj de la presentación cambia de estado. (Requerido)              |
| [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)     | Implemente si el receptor de medios debe realizar un paso de procesamiento final. (Opcional).                 |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                         | Implemente si el receptor de medios expone cualquier interfaz de servicio. (Opcional).                       |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)       | Implemente si el receptor multimedia envía eventos. (Opcional).                                     |
| [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll)             | Implemente si el receptor de medios admite el prelanzamiento. (Opcional).                                     |
| [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) | Implemente si el receptor de medios puede proporcionar un origen de hora para el reloj de presentación. (Opcional). |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                   | Implemente si el receptor de medios puede ajustar la calidad de la reproducción. (Opcional).                          |



 

Opcionalmente, un receptor de medios puede implementar la siguiente interfaz como un servicio.



| Interfaz de servicio                        | Descripción                                    |
|------------------------------------------|------------------------------------------------|
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) | Informa del intervalo de velocidades de reproducción admitidas. |



 

Para obtener más información sobre las interfaces de servicio y [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), consulte [interfaces de servicio](service-interfaces.md).

## <a name="stream-sink-interfaces"></a>Interfaces del receptor de secuencias

Los receptores de secuencias deben exponer las siguientes interfaces a través de **QueryInterface**.



| Interfaz                                                | Descripción                                                                                              |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)                   | La interfaz principal para los receptores de flujo. (Requerido)                                                      |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Pone en cola los eventos. La interfaz [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) hereda esta interfaz. (Requerido) |



 

Actualmente no hay interfaces de servicio definidas para los receptores de flujo.

## <a name="stream-sink-events"></a>Eventos de receptor de secuencias

En la tabla siguiente se enumeran los eventos que se definen para los receptores de secuencias genéricos. Los receptores de secuencias también pueden enviar eventos personalizados que no se enumeran aquí.



| Evento                                                                  | Descripción                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [MEStreamSinkFormatChanged](mestreamsinkformatchanged.md)             | El tipo de medio del receptor de flujo ya no es válido. (Opcional). |
| [MEStreamSinkMarker](mestreamsinkmarker.md)                           | Se procesó un marcador. (Requerido)                          |
| [MEStreamSinkPaused](mestreamsinkpaused.md)                           | El receptor de flujo se ha pausado. (Requerido)                      |
| [MEStreamSinkPrerolled](mestreamsinkprerolled.md)                     | Se ha completado el prelanzamiento. (Opcional).                             |
| [MEStreamSinkRateChanged](mestreamsinkratechanged.md)                 | El receptor de la secuencia ha cambiado la velocidad de reproducción. (Opcional).       |
| [MEStreamSinkRequestSample](mestreamsinkrequestsample.md)             | Se solicita un nuevo ejemplo. (Requerido)                       |
| [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) | Se completó una solicitud de limpieza. (Opcional).                   |
| [MEStreamSinkStarted](mestreamsinkstarted.md)                         | El receptor de flujo se ha iniciado. (Requerido)                     |
| [MEStreamSinkStopped](mestreamsinkstopped.md)                         | El receptor de la secuencia se ha detenido. (Requerido)                     |



 

Actualmente no se definen eventos de uso general para los receptores de medios. Algunos receptores de medios podrían enviar eventos personalizados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Canalización de Media Foundation](media-foundation-pipeline.md)
</dt> <dt>

[Arquitectura de Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 




