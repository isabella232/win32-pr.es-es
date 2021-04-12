---
description: Reloj de presentación
ms.assetid: cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5
title: Reloj de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f61ad02537a2591c681db78721376651f7854ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155336"
---
# <a name="presentation-clock"></a>Reloj de presentación

El *reloj* de la presentación es un objeto que genera la hora de reloj de una presentación. El tiempo indicado por el reloj de la presentación se denomina *tiempo de presentación*. Todas las secuencias de una presentación se sincronizan con el tiempo de presentación. El reloj de la presentación expone las siguientes interfaces.



| Interfaz                                            | Descripción                                         |
|------------------------------------------------------|-----------------------------------------------------|
| [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) | Interfaz principal para usar el reloj de presentación. |
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)             | Controla la velocidad del reloj.                            |
| [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer)                         | Proporciona una devolución de llamada del temporizador.                          |
| [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)                   | Apaga el reloj de la presentación.                  |



 

Los receptores de medios usan el tiempo de presentación para programar el momento de representación de los ejemplos. Cada vez que un receptor de medios recibe un nuevo ejemplo, obtiene la marca de tiempo del ejemplo y representa el ejemplo en el momento indicado o lo más cerca posible de ese tiempo. Dado que todos los receptores de medios de una topología comparten el mismo reloj de presentación, se sincronizan varias secuencias (como audio y vídeo). Los orígenes y las transformaciones multimedia no usan el reloj de la presentación, ya que no se programan cuando se entregan ejemplos. En su lugar, generan ejemplos cada vez que la canalización solicita un nuevo ejemplo.

Si usa la sesión multimedia para la reproducción, la sesión multimedia controla todos los detalles de la creación del reloj de la presentación, la selección de un origen de hora y la notificación de los receptores de medios. La aplicación podría usar el reloj de la presentación para obtener el tiempo de presentación actual durante la reproducción, pero de lo contrario no llamará a ningún método en el reloj de la presentación.

## <a name="clock-time-and-clock-states"></a>Hora del reloj y Estados del reloj

Para obtener la hora del reloj más reciente desde el reloj de la presentación, llame a [**IMFPresentationClock:: getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime). Los tiempos de reloj siempre están en unidades de 100-nanosegundos, por lo que un segundo es 10 millones (10 ^ 7) TICs. Esto corresponde a una frecuencia de 10 MHz.

El reloj de la presentación tiene tres Estados: en ejecución, en pausa y detenido.

-   Para ejecutar el reloj, llame a [**IMFPresentationClock:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start). El método **Start** especifica la hora de inicio del reloj. Mientras se ejecuta el reloj, la hora del reloj se incrementa desde la hora de inicio, a la velocidad de reloj actual.
-   Para pausar el reloj, llame a [**IMFPresentationClock::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause). Mientras el reloj está en pausa, la hora del reloj no avanza y [**getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) devuelve la hora a la que se pausó el reloj.
-   Para detener el reloj, llame a [**IMFPresentationClock:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop). Cuando se detiene el reloj, la hora del reloj no avanza y [**getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) devuelve cero.

De forma predeterminada, el reloj avanza a una velocidad de 1,0, lo que significa 1 TIC por 100 nanosegundos. Para cambiar la velocidad a la que avanza el reloj, consulte el reloj de presentación de la interfaz [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) y llame a [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).

Los objetos pueden recibir notificaciones de cambios de estado (incluidos los cambios de velocidad) del reloj de presentación. Para recibir notificaciones, implemente la interfaz [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) y llame a [**IMFPresentationClock:: AddClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) en el reloj de la presentación. Antes de apagar, llame a [**IMFPresentationClock:: RemoveClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-removeclockstatesink) para anular el registro del objeto. Los receptores de medios usan este mecanismo para recibir notificaciones del reloj.

## <a name="presentation-times"></a>Tiempos de presentación

Un receptor de medios intenta programar cada ejemplo para que el ejemplo se represente en el momento correcto o lo más cerca posible de la hora correcta. Se aplican las siguientes definiciones:

-   *Tiempo de presentación.* La hora a la que se debe representar una muestra. El tiempo se expresa en unidades de 100 nanosegundos.
-   *Tiempo medio.* Hora relativa al inicio del contenido. Por ejemplo, si un archivo de vídeo tiene una longitud de 10 segundos, la mitad del punto a través del archivo tiene un tiempo medio de 5 segundos.
-   *Marca de tiempo.* La hora marcada en un ejemplo multimedia. Para obtener la marca de tiempo, llame a [**IMFSample:: GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime). Cuando un origen de medios produce un ejemplo, establece la marca de tiempo igual a la hora del medio. La sesión multimedia traduce la marca de tiempo en tiempo de presentación.

De forma predeterminada, la hora del medio y el tiempo de presentación son los mismos, por ejemplo, si aparece un fotograma de vídeo de 5 segundos en el archivo de origen, la hora del medio y el tiempo de presentación son 5 segundos. Si usa el origen del [secuenciador](sequencer-source.md), el modelo de control de tiempo es algo más complicado, para permitir transiciones suaves entre segmentos. Para obtener más información sobre el modelo de control de tiempo del origen del secuenciador, vea [tiempos de presentación de secuencias](sequence-presentation-times.md).

El origen multimedia siempre establece la marca de tiempo igual a la hora del medio. Si el tiempo de presentación no está alineado con la hora del medio, la sesión multimedia convierte las marcas de tiempo en los ejemplos de medios. En el momento en que el receptor recibe un ejemplo, la marca de tiempo del ejemplo se ha convertido en el tiempo de presentación. El receptor programa el ejemplo con la hora actual del reloj de presentación. (Los receptores sin velocidad son una excepción, ya que omiten el reloj de la presentación).

Si la aplicación busca una nueva posición, la sesión multimedia reinicia el reloj de la presentación en el tiempo de búsqueda especificado. Por ejemplo, si la aplicación busca la posición de 5 segundos en el archivo, la sesión multimedia inicia el reloj en 5 segundos. El origen multimedia podría proporcionar muestras con una marca de tiempo ligeramente anterior si el tiempo de búsqueda no se encuentra en un límite de fotogramas clave. Esto es necesario para que los descodificadores puedan descodificar todos los marcos. La sesión multimedia quita o recorta muestras antes de que lleguen a los receptores de medios, con el fin de que coincidan con el tiempo de búsqueda solicitado. Por ejemplo, si el tiempo de búsqueda es de 5 segundos, la primera muestra de audio podría comenzar en 4,5 segundos. La sesión multimedia recortará los primeros 0,5 segundos del primer ejemplo de audio descodificado.

## <a name="creating-the-presentation-clock"></a>Crear el reloj de la presentación

Para crear el reloj de la presentación, llame a [**MFCreatePresentationClock**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationclock). Para apagar el reloj, consulte la interfaz [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) y llame a [**IMFShutdown:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown). El autor de la llamada de **MFCreatePresentationClock** es responsable de llamar a **Shutdown**; en la mayoría de los casos, se trata de la sesión multimedia en lugar de la aplicación.

## <a name="presentation-time-sources"></a>Orígenes de tiempo de presentación

A pesar de su nombre, el reloj de la presentación no implementa realmente un reloj. En su lugar, obtiene las horas de reloj de otro objeto, denominado *origen de tiempo de presentación*. El origen de la hora puede ser cualquier objeto que genere TICs de reloj precisos y exponga la interfaz [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) . En la siguiente ilustración se muestra este proceso.

![diagrama que muestra la relación entre el reloj de presentación y el origen de tiempo de presentación](images/dedc255c-eb6d-49fc-8892-7b6076ed4488.gif)

Cuando el reloj de la presentación se crea por primera vez, no tiene un origen de hora. Para establecer el origen de la hora, llame a [**IMFPresentationClock:: SetTimeSource**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource) con un puntero a la interfaz [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) del origen de la hora. Un origen de hora admite los mismos Estados que el reloj de presentación (en ejecución, en pausa y detenerse) y debe implementar la interfaz [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) . El reloj de la presentación usa esta interfaz para notificar al origen de la hora Cuándo cambiar el estado. De esta manera, el origen de la hora proporciona los tics del reloj, pero el reloj de la presentación inicia los cambios de estado en el reloj.

Algunos receptores de medios tienen acceso a un reloj preciso y, por lo tanto, exponen la interfaz [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) . En concreto, el representador de audio puede usar la frecuencia de la tarjeta de sonido como reloj. En la reproducción de audio, es útil que el procesador de audio actúe como el origen de la hora, de modo que el vídeo se sincronice con la velocidad de reproducción de audio. Por lo general, esto genera mejores resultados que intentar hacer coincidir el audio con un reloj externo.

Media Foundation también proporciona un origen de tiempo de presentación basado en el reloj del sistema. Para crear este objeto, llame a [**MFCreateSystemTimeSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesystemtimesource). El origen de la hora del sistema se puede usar cuando ningún receptor de medios proporciona un origen de hora.

En general, un receptor de medios debe usar el reloj de presentación que se le proporcionó, independientemente de la hora en la que se use el reloj de presentación. Esta regla se aplica incluso cuando un receptor de medios implementa [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource). Si el reloj de la presentación utiliza algún otro origen de hora, el receptor de medios debe seguir ese origen de hora, no su propio reloj interno.

Hay dos situaciones en las que un receptor de medios no seguirá el reloj de la presentación:

-   Algunos receptores de medios tienen *tasas*. Si un receptor de medios tiene una limitación, consume ejemplos lo más rápido posible, sin programarlos según el reloj de la presentación. Normalmente, los receptores sin velocidad escriben datos en un archivo, por lo que es conveniente completar la operación lo más rápido posible. Un receptor sin velocidad devuelve la \_ marca sin velocidad MEDIASINK en su [**método IMFMediaSink:: GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) . Cuando todos los receptores de una topología no tienen una frecuencia, la sesión multimedia inserta los datos a través de la canalización lo más rápido posible.

-   Algunos receptores de medios no pueden coincidir con tasas con un origen de hora distinto de ellos mismos. Si es así, el receptor devuelve el MEDIASINK \_ no puede \_ coincidir con la \_ marca del reloj en su método [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) . La canalización puede seguir usando otro origen de hora, pero los resultados serán inferiores a los óptimos. El receptor probablemente se retrasará y provocará problemas durante la reproducción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[API de Media Foundation Platform](media-foundation-platform-apis.md)
</dt> </dl>

 

 



