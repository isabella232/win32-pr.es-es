---
description: Los receptores multimedia son los objetos de canalización que reciben datos multimedia.
ms.assetid: a0fbce1b-0a16-4449-9eca-906fd9056a1c
title: Receptores multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9394cbfd49a631d59b9296202a2b6ca7a868869
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127580429"
---
# <a name="media-sinks"></a>Receptores multimedia

*Los receptores multimedia* son los objetos de canalización que reciben datos multimedia. Un receptor de medios es el destino de uno o varios flujos multimedia. Los receptores multimedia se divide en dos categorías generales:

-   Un *representador es* un receptor multimedia que presenta datos para la reproducción. El representador de vídeo mejorado (EVR) muestra fotogramas de vídeo y el representador de audio reproduce secuencias de audio a través de la tarjeta de sonido u otro dispositivo de audio.

-   Un *receptor de archivo* es un receptor multimedia que escribe datos en un archivo u otro almacenamiento.

La principal diferencia entre ellos es que un receptor de archivo no consume los datos a una velocidad de reproducción fija. En su lugar, escribe los datos que recibe lo antes posible.

Los receptores multimedia exponen la [**interfaz IMFMediaSink.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) Cada receptor de medios contiene uno o varios *receptores de secuencia.* Cada receptor de flujo recibe los datos de una secuencia. Los receptores de flujo exponen [**la interfaz DESTREAMSink.**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) Normalmente, una aplicación no crea receptores multimedia directamente. En su lugar, la aplicación crea uno o varios objetos de activación, que la sesión multimedia usa para crear el receptor. Todas las demás operaciones del receptor se controlan mediante la sesión multimedia y la aplicación no llama a ningún método en el receptor de medios ni en ninguno de los receptores de flujo. Para obtener más información sobre los objetos de activación, vea [Activation Objects](activation-objects.md).

Debe leer el resto de este tema si está escribiendo un receptor multimedia personalizado o si desea usar un receptor multimedia directamente sin la sesión multimedia.

-   [Receptores de flujo](#stream-sinks)
-   [Reloj de presentación](#presentation-clock)
-   [Formatos de secuencia](#stream-formats)
-   [Flujo de datos](#data-flow)
-   [Marcadores](#markers)
-   [Cambios de estado](#state-changes)
-   [Finalizando](#finalizing)
-   [Cerrando](#shutting-down)
-   [Interfaces de receptor multimedia](#media-sink-interfaces)
-   [Interfaces de receptor de flujo](#stream-sink-interfaces)
-   [Eventos de receptor de secuencias](#stream-sink-events)
-   [Temas relacionados](#related-topics)

## <a name="stream-sinks"></a>Receptores de flujo

Un receptor multimedia puede tener un número fijo de receptores de flujo, o puede admitir la adición y eliminación de receptores de flujo. Si tiene un número fijo de receptores de flujo, el método [**IMFMediaSink::GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) devuelve la marca MEDIASINK \_ FIXED \_ STREAMS. De lo contrario, puede agregar y quitar receptores de flujo. Para agregar un nuevo receptor de flujo, llame [**a IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink). Para quitar un receptor de flujo, llame [**a IMFMediaSink::RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink). La marca MEDIASINK FIXED STREAMS indica que el receptor de \_ medios no admite estos dos \_ métodos. (Es posible que admita alguna otra manera de configurar el número de secuencias, por ejemplo estableciendo parámetros de inicialización cuando se crea el receptor). Se ordena la lista de receptores de flujo. Para enumerarlos por valor de índice, llame al [**método IMFMediaSink::GetStreamSinkByIndex.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex)

Los receptores de flujo también tienen identificadores. Los identificadores de secuencia son únicos dentro del receptor de medios, pero no tienen que ser consecutivos. Dependiendo del receptor multimedia, los identificadores de flujo pueden tener algún significado relacionado con el contenido. Por ejemplo, un receptor de archivo podría escribir los identificadores de flujo en el encabezado de archivo. De lo contrario, son arbitrarias. Para obtener un receptor de flujo por su identificador, llame [**a IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid).

## <a name="presentation-clock"></a>Reloj de presentación

El reloj de presentación controla la velocidad a la que un receptor multimedia consume [muestras.](presentation-clock.md) La sesión multimedia selecciona el reloj de presentación y lo establece en el receptor de medios mediante una llamada al método [**INMEDIASink::SetPresentationClock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-setpresentationclock) del receptor multimedia. El reloj de presentación debe establecerse en el receptor de medios antes de que pueda comenzar el streaming. Cada receptor multimedia requiere que se ejecute un reloj de presentación. El receptor multimedia usa el reloj de presentación para dos propósitos:

-   Para recibir notificaciones cuando se inicia o se detiene el streaming. El receptor multimedia recibe estas notificaciones a través de la interfaz [**IMFClockStateSink,**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) que todos los receptores multimedia deben implementar.

-   Para determinar cuándo debe representar muestras. Cuando el receptor multimedia recibe un nuevo ejemplo, obtiene la marca de tiempo de la muestra e intenta representar el ejemplo en ese momento de presentación.

El reloj de presentación deriva sus horas de reloj de otro objeto denominado origen *de la hora de presentación.* Los orígenes de tiempo de presentación exponen [**la interfaz IMFPresentationTimeSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) Algunos receptores multimedia tienen acceso a un reloj preciso, por lo que exponen esta interfaz. Esto significa que un receptor multimedia podría programar muestras en una hora proporcionada por su propio reloj. Sin embargo, el receptor de medios no puede suponer que esto sea así. Siempre debe usar la hora del reloj de presentación, independientemente de si el reloj de presentación está controlado por el propio receptor multimedia o por algún otro reloj.

Si un receptor multimedia no puede coincidir con velocidades con un reloj distinto de su propio, el método [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) devuelve la marca MEDIASINK \_ CANNOT MATCH \_ \_ CLOCK. Si esta marca está presente y el reloj de presentación usa un origen de tiempo de presentación diferente, es probable que el receptor multimedia tenga un rendimiento deficiente. Por ejemplo, podría tener problemas durante la reproducción.

Un *receptor sin* velocidad es un receptor multimedia que omite las marcas de tiempo de las muestras y consume datos en cuanto llega cada muestra. Un receptor de medios sin velocidad devuelve la marca RATELESS DE MEDIASINK \_ del [**método GetCharacteristics.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) Normalmente, esta marca se aplica a los receptores de archivo. Si todos los receptores multimedia de la canalización no tienen velocidad, la sesión multimedia usa un reloj de presentación sin velocidad especial. Este reloj se ejecuta tan rápido como los receptores consumen ejemplos.

## <a name="stream-formats"></a>Formatos de secuencia

Para que el receptor de medios pueda recibir ejemplos, el cliente debe establecer el tipo de medio en los receptores de flujo. Para establecer el tipo de medio, llame al método [**IMFStreamSink::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-getmediatypehandler) del receptor de secuencias. Este método devuelve un puntero a la [**interfaz IMFMediaTypeHandler.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) Use esta interfaz para obtener la lista de tipos de medios preferidos, obtener el tipo de medio actual y establecer el tipo de medio.

Para obtener la lista de tipos de medios preferidos, llame [**a IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex). Los tipos preferidos se deben tomar como una sugerencia para el cliente. La lista puede estar incompleta o incluir tipos de medios parciales. Un tipo de medio parcial es aquel que no tiene todos los atributos necesarios para describir un formato válido. Por ejemplo, un tipo de vídeo parcial podría especificar el espacio de color y la profundidad de bits, pero no el ancho o alto de la imagen. Un tipo de audio parcial puede especificar el formato de compresión y la frecuencia de muestreo, pero no el número de canales de audio.

Para obtener el tipo de medio actual del receptor de secuencias, llame [**a IMFMediaTypeHandler::GetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getcurrentmediatype). Cuando se crea por primera vez un receptor de flujo, es posible que ya tenga un tipo de medio predeterminado establecido o que no tenga ningún tipo de medio hasta que el cliente establezca uno.

Para establecer el tipo de medio, llame [**a IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype). Es posible que algunos receptores de flujos no admitan el cambio del tipo una vez establecido. Por lo tanto, resulta útil probar los tipos de medios antes de establecerlos. Para probar si el receptor de medios aceptará un tipo de medio ( sin establecer el tipo ), llame a [**LA PROPIEDAD DEMEDIATYPEHandler::IsMediaTypeSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-ismediatypesupported).

## <a name="data-flow"></a>Data Flow

Los receptores multimedia usan un *modelo de extracción*, lo que significa que los receptores de flujo solicitan datos a medida que los necesitan. El cliente debe responder de forma oportuna para evitar problemas.

Algunos receptores multimedia *admiten la inscripción previa* de . La inscripción previa es el proceso de proporcionar datos al receptor de medios antes de que se inicie el reloj de presentación. Si un receptor de medios admite la inscripción previa, el receptor multimedia expone la interfaz [**DE PREROLL DE LOSMEDIAMEDIASink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll) y el método [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) devuelve la marca MEDIASINK \_ CAN \_ PREROLL. La inscripción previa garantiza que el receptor de medios esté listo para presentar el primer ejemplo cuando se inicie el reloj de presentación. Se recomienda que el cliente siempre se insinste previamente si el receptor multimedia lo admite, ya que puede evitar problemas o espacios durante la reproducción.

El flujo de datos a un receptor multimedia funciona de la siguiente manera:

1.  El cliente establece los tipos de medios y el reloj de presentación. El receptor multimedia se registra con el reloj de presentación para recibir notificaciones sobre los cambios de estado del reloj.
2.  Opcionalmente, el cliente consulta [**SIEDONMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll). Si el receptor de medios expone esta interfaz, el cliente llama a [**IMFMediaSinkPreroll::NotifyPreroll**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasinkpreroll-notifypreroll). De lo contrario, el cliente omite el paso 5.
3.  Cada receptor de flujo envía uno o varios [eventos MEStreamSinkRequestSample.](mestreamsinkrequestsample.md) En respuesta a cada uno de estos eventos, el cliente obtiene el siguiente ejemplo de datos para esa secuencia y llama a [**IMFStreamSink::P rocessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample).
4.  Cuando cada receptor de flujo recibe suficientes datos de inscripción previa, envía un [evento MEStreamSinkPrerolled.](mestreamsinkprerolled.md)
5.  El cliente llama [**a IMFPresentationClock::Start para**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) iniciar el reloj de presentación.
6.  El reloj de presentación notifica al receptor multimedia que el reloj se está iniciando mediante una llamada a [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart).
7.  Para obtener más datos, cada receptor de flujo envía [eventos MEStreamSinkRequestSample.](mestreamsinkrequestsample.md) En respuesta a cada uno de estos eventos, el cliente obtiene el ejemplo siguiente y llama a [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample). Este paso se repite hasta que finaliza la presentación.

La mayoría de los receptores multimedia procesan ejemplos de forma asincrónica, por lo que los receptores de flujo pueden enviar más de una solicitud de ejemplo a la vez.

Durante el streaming, el cliente puede llamar [**a IMFStreamSink::P laceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) y [**a IMFStreamSink::Flush**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-flush) en cualquier momento. Los marcadores se describen en la sección siguiente. El vaciado hace que el receptor del flujo coloque las muestras que ha puesto en cola pero que aún no se han representado.

## <a name="markers"></a>Marcadores

Los marcadores proporcionan una manera para que el cliente indique puntos específicos en la secuencia. Un marcador consta de la siguiente información:

-   Tipo de marcador, definido como miembro de la [**enumeración MFSTREAMSINK \_ MARKER \_ TYPE.**](/windows/desktop/api/mfidl/ne-mfidl-mfstreamsink_marker_type)
-   Datos asociados al marcador. El significado de los datos depende del tipo de marcador. Algunos tipos de marcador no tienen datos.
-   Datos opcionales para el propio uso del cliente.

Para colocar un marcador, el cliente llama [**a IMFStreamSink::P laceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker). El receptor de flujo termina de procesar los ejemplos que recibió antes de la llamada a **PlaceMarker** y, a continuación, envía un [evento MEStreamSinkMarker.](mestreamsinkmarker.md)

La mayoría de los receptores multimedia mantienen una cola de ejemplos pendientes, que procesan de forma asincrónica. Los eventos de marcador se deben serializar con el procesamiento de ejemplo, por lo que el receptor de medios debe colocar los marcadores en la misma cola. Por ejemplo, suponga que el cliente realiza las siguientes llamadas de método:

1.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (ejemplo \# 1)
2.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (ejemplo \# 2)
3.  [**Marcador de posición**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) (marcador \# 1)
4.  [**ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) (ejemplo \# 3)
5.  [**PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) (marcador \# 2)

En este ejemplo, el receptor de flujo debe enviar el evento [MEStreamSinkMarker](mestreamsinkmarker.md) para el marcador 1 después de que procese el ejemplo 2 y el evento para el marcador 2 después de que procese el ejemplo \# \# \# \# 3.

Si el cliente vacía un receptor de flujo, el receptor de flujo procesa inmediatamente los marcadores que estaban en la cola. Establece el código de estado en E \_ ABORT en estos eventos.

Algunos marcadores contienen información que es relevante para el receptor de medios:

-   **MFSTREAMSINK \_ MARKER \_ TICK**: indica que hay una brecha en la secuencia. El ejemplo siguiente será una discontinuidad.
-   **MFSTREAMSINK \_ MARKER \_ ENDOFSEGMENT:** indica el final de un segmento o el final de una secuencia. El ejemplo siguiente (si lo hubiera) podría ser una discontinuidad.
-   **MFSTREAMSINK \_ MARKER \_ EVENT**: contiene un evento. Según el tipo de evento y la implementación del receptor de medios, el receptor multimedia podría controlar el evento o ignorarlo.

## <a name="state-changes"></a>Cambios de estado

A un receptor de medios se le notifican los cambios de estado en el reloj de presentación a través de la interfaz [**DEClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) del receptor de medios. Cuando el cliente establece el reloj de presentación, el receptor multimedia llama a [**IMFPresentationClock::AddClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) para registrarse para recibir notificaciones del reloj. En la tabla siguiente se resume cómo se comporta un receptor multimedia en respuesta a los cambios de estado del reloj.



| Cambio de estado del reloj                                         | Procesamiento de ejemplo                                                                                                                                                                                                                                             | Procesamiento de marcadores                                                                                                                                                                                   |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | Procese ejemplos cuya marca de tiempo sea igual o posterior a la hora de inicio del reloj.                                                                                                                                                                              | Envíe el [evento MEStreamSinkMarker](mestreamsinkmarker.md) cuando se hayan procesado todos los ejemplos recibidos antes del marcador.                                                                 |
| [**OnClockPause**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause)     | El receptor de medios puede producir [**un error en ProcessSample**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample) mientras está en pausa.<br/> Si el receptor de medios acepta muestras mientras está en pausa, debe ponerlas en cola hasta que se reinicie el reloj. No procese ninguna muestra en cola mientras está en pausa.<br/> | Si hay ejemplos en cola, coloque marcadores en la misma cola. Envíe el evento de marcador cuando se reinicie el reloj.<br/> De lo contrario, envíe el evento de marcador inmediatamente.<br/>                    |
| [**OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | Procese los ejemplos que se han en cola mientras estaba en pausa y, a continuación, trate lo mismo que [**OnClockStart.**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)                                                                                                                         | Envíe [eventos MEStreamSinkMarker](mestreamsinkmarker.md) para marcadores en cola (serializados con el procesamiento de ejemplo) y, a continuación, trate lo mismo que [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart). |
| [**OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | Quitar todos los ejemplos en cola. Se pueden producir errores en otras llamadas a [**ProcessSample.**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-processsample)                                                                                                                                                      | Enviar eventos de marcador en cola. En las llamadas posteriores [**a PlaceMarker,**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker)envíe inmediatamente el evento de marcador.                                                              |



 

Además, los receptores de flujo deben enviar los siguientes eventos cuando hayan completado las transiciones de estado:

-   [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart), [**OnClockRestart:**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) [evento MEStreamSinkStarted](mestreamsinkstarted.md)
-   [**OnClockPause:**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause) [evento MEStreamSinkPaused](mestreamsinkpaused.md)
-   [**OnClockStop:**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop) [evento MEStreamSinkStopped](mestreamsinkstopped.md)

## <a name="finalizing"></a>Finalizando

Algunos receptores multimedia requieren un paso de procesamiento adicional después de entregar el último ejemplo. Normalmente, este requisito se aplica a los receptores de archivo, que deben escribir encabezados o índices en el archivo. Si un receptor de medios requiere algún procesamiento final, expone la interfaz [**IMFFinalizableMediaSink.**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)

Una vez que el cliente entrega el último ejemplo, el cliente consulta esta interfaz. Si el receptor multimedia admite la interfaz , el cliente llama a [**IMFFinalizableMediaSink::BeginFinalize**](/windows/desktop/api/mfidl/nf-mfidl-imffinalizablemediasink-beginfinalize) para realizar el procesamiento final de forma asincrónica. Este método sigue el modelo Media Foundation asincrónico, descrito en [Métodos de devolución de llamada asincrónicos](asynchronous-callback-methods.md). El receptor de medios puede suponer que el cliente llamará **a BeginFinalize.** Si no se llama **a BeginFinalize,** puede producirse un archivo de creación incorrecta.

## <a name="shutting-down"></a>Cerrando

Cuando el cliente ha terminado de usar el receptor de medios, el cliente llama [**a IMFMediaSink::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown). Dentro de este método, el receptor de medios debe interrumpir los recuentos de referencias circulares. Normalmente, habrá referencias circulares entre el receptor multimedia y los receptores de flujo.

Si usa el objeto del asistente de cola de eventos para implementar [**IMFMediaEventGenerator,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)llame a [**IMFMediaEventQueue::Shutdown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventqueue-shutdown) en la cola de eventos. Este método cierra la cola de eventos y señala a cualquier llamador que esté esperando un evento.

Después del apagado, todos los métodos del receptor multimedia devuelven MF \_ E \_ SHUTDOWN, a excepción de **los métodos IUnknown.**

## <a name="media-sink-interfaces"></a>Interfaces de receptor multimedia

En la tabla siguiente se enumeran las interfaces estándar que los receptores multimedia pueden exponer a través **de QueryInterface**. Los receptores multimedia también pueden exponer interfaces personalizadas.



| Interfaz                                                      | Descripción                                                                                   |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)                           | Interfaz principal para receptores multimedia. (Requerido)                                            |
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                 | Se usa para notificar al receptor de medios cuando el reloj de presentación cambia de estado. (Requerido)              |
| [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)     | Implemente si el receptor de medios debe realizar un paso de procesamiento final. (Opcional).                 |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                         | Implemente si el receptor multimedia expone las interfaces de servicio. (Opcional).                       |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)       | Implemente si el receptor de medios envía eventos. (Opcional).                                     |
| [**IMFMediaSinkPreroll**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasinkpreroll)             | Implemente si el receptor de medios admite la inscripción previa. (Opcional).                                     |
| [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) | Implemente si el receptor de medios puede proporcionar un origen de hora para el reloj de presentación. (Opcional). |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)                   | Implemente si el receptor multimedia puede ajustar la calidad de reproducción. (Opcional).                          |



 

Opcionalmente, un receptor multimedia puede implementar la siguiente interfaz como servicio.



| Interfaz de servicio                        | Descripción                                    |
|------------------------------------------|------------------------------------------------|
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) | Notifica el intervalo de velocidades de reproducción admitidas. |



 

Para obtener más información sobre las interfaces de servicio [**y ELSERVICIOGETGET ,**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)vea [Interfaces de servicio](service-interfaces.md).

## <a name="stream-sink-interfaces"></a>Interfaces de receptor de flujo

Los receptores de flujo deben exponer las interfaces siguientes a través **de QueryInterface**.



| Interfaz                                                | Descripción                                                                                              |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)                   | Interfaz principal para receptores de flujo. (Requerido)                                                      |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Pone en cola los eventos. La [**interfaz IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) hereda esta interfaz. (Requerido) |



 

Actualmente no se definen interfaces de servicio para los receptores de flujos.

## <a name="stream-sink-events"></a>Eventos de receptor de secuencias

En la tabla siguiente se enumeran los eventos definidos para los receptores de flujos genéricos. Los receptores de flujos también pueden enviar eventos personalizados que no aparecen aquí.



| Evento                                                                  | Descripción                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [MEStreamSinkFormatChanged](mestreamsinkformatchanged.md)             | El tipo de medio del receptor de secuencias ya no es válido. (Opcional). |
| [MEStreamSinkMarker](mestreamsinkmarker.md)                           | Se procesó un marcador. (Requerido)                          |
| [MEStreamSinkPaused](mestreamsinkpaused.md)                           | El receptor del flujo se ha pausado. (Requerido)                      |
| [MEStreamSinkPrerolled](mestreamsinkprerolled.md)                     | La inscripción previa se ha completado. (Opcional).                             |
| [MEStreamSinkRateChanged](mestreamsinkratechanged.md)                 | El receptor del flujo ha cambiado la velocidad de reproducción. (Opcional).       |
| [MEStreamSinkRequestSample](mestreamsinkrequestsample.md)             | Se solicita un nuevo ejemplo. (Requerido)                       |
| [MEStreamSinkScrubSampleComplete](mestreamsinkscrubsamplecomplete.md) | Se completó una solicitud de limpieza. (Opcional).                   |
| [MEStreamSinkStarted](mestreamsinkstarted.md)                         | Se ha iniciado el receptor del flujo. (Requerido)                     |
| [MEStreamSinkStopped](mestreamsinkstopped.md)                         | El receptor de flujo se ha detenido. (Requerido)                     |



 

Actualmente no se define ningún evento de uso general para receptores multimedia. Algunos receptores multimedia pueden enviar eventos personalizados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation canalización](media-foundation-pipeline.md)
</dt> <dt>

[Arquitectura de Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 




