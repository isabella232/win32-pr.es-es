---
description: Reloj de presentación
ms.assetid: cb8bb62a-ef80-4de0-9a44-3bb77edc9dd5
title: Reloj de presentación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0219b6384373fd75bc8a424935e502841071f69eaa9ae719ec6ed35c950218
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239169"
---
# <a name="presentation-clock"></a>Reloj de presentación

El *reloj de* presentación es un objeto que genera la hora del reloj para una presentación. La hora notificada por el reloj de presentación se denomina hora *de presentación*. Todas las secuencias de una presentación se sincronizan con la hora de presentación. El reloj de presentación expone las interfaces siguientes.



| Interfaz                                            | Descripción                                         |
|------------------------------------------------------|-----------------------------------------------------|
| [**IMFPresentationClock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) | Interfaz principal para usar el reloj de presentación. |
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)             | Controla la velocidad del reloj.                            |
| [**IMFTimer**](/windows/desktop/api/mfidl/nn-mfidl-imftimer)                         | Proporciona una devolución de llamada de temporizador.                          |
| [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown)                   | Apaga el reloj de presentación.                  |



 

Los receptores multimedia usan el tiempo de presentación para programar cuándo representar ejemplos. Cada vez que un receptor multimedia recibe un nuevo ejemplo, obtiene la marca de tiempo de la muestra y la representa en el momento indicado, o lo más cerca posible de esa hora. Dado que todos los receptores multimedia de una topología comparten el mismo reloj de presentación, se sincronizan varias secuencias (como audio y vídeo). Los orígenes multimedia y las transformaciones no usan el reloj de presentación, ya que no programan cuándo entregar ejemplos. En su lugar, generan ejemplos cada vez que la canalización solicita un nuevo ejemplo.

Si usa la sesión multimedia para la reproducción, la sesión multimedia controla todos los detalles de la creación del reloj de presentación, la selección de un origen de hora y la notificación a los receptores multimedia. La aplicación podría usar el reloj de presentación para obtener el tiempo de presentación actual durante la reproducción, pero de lo contrario no llamará a ningún método en el reloj de presentación.

## <a name="clock-time-and-clock-states"></a>Hora del reloj y estados de reloj

Para obtener la hora del reloj más reciente del reloj de presentación, llame a [**IMFPresentationClock::GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime). Las horas de reloj siempre están en unidades de 100 nanosegundos, por lo que un segundo es 10 000 000 tics (10^7). Esto corresponde a una frecuencia de 10 MHz.

El reloj de presentación tiene tres estados: En ejecución, en pausa y detenido.

-   Para ejecutar el reloj, llame [**a IMFPresentationClock::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start). El **método Start** especifica la hora de inicio del reloj. Mientras se ejecuta el reloj, la hora del reloj se incrementa a partir de la hora de inicio, a la velocidad de reloj actual.
-   Para pausar el reloj, llame [**a IMFPresentationClock::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause). Mientras el reloj está en pausa, la hora del reloj no avanza y [**GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) devuelve la hora a la que se detuvo el reloj.
-   Para detener el reloj, llame [**a IMFPresentationClock::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop). Cuando se detiene el reloj, la hora del reloj no avanza y [**GetTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) devuelve cero.

De forma predeterminada, el reloj avanza a una velocidad de 1,0, lo que significa 1 tic por cada 100 nanosegundos. Para cambiar la velocidad a la que avanza el reloj, consulte el reloj de presentación de la interfaz [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) y llame a [**IMFRateControl::SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).

Los objetos pueden recibir notificaciones de cambios de estado (incluidos los cambios de velocidad) desde el reloj de presentación. Para recibir notificaciones, implemente la interfaz [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) y llame a [**IMFPresentationClock::AddClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-addclockstatesink) en el reloj de presentación. Antes de cerrar, llame a [**IMFPresentationClock::RemoveClockStateSink**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-removeclockstatesink) para anular el registro del objeto. Los receptores multimedia usan este mecanismo para recibir notificaciones del reloj.

## <a name="presentation-times"></a>Tiempos de presentación

Un receptor multimedia intenta programar cada muestra para que se represente en el momento correcto o lo más cerca posible de la hora correcta. Se aplican las siguientes definiciones:

-   *Tiempo de presentación.* Hora a la que se debe representar un ejemplo. El tiempo se da en unidades de 100 nanosegundos.
-   *Hora del medio.* Hora relativa al inicio del contenido. Por ejemplo, si un archivo de vídeo tiene una duración de 10 segundos, el punto medio a través del archivo tiene un tiempo multimedia de 5 segundos.
-   *Marca de tiempo.* Hora marcada en un ejemplo multimedia. Para obtener la marca de tiempo, llame [**a IMFSample::GetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime). Cuando un origen multimedia genera un ejemplo, establece la marca de tiempo igual a la hora del medio. La sesión multimedia traduce la marca de tiempo en tiempo de presentación.

De forma predeterminada, el tiempo de los medios y el tiempo de presentación son los mismos; por ejemplo, si un fotograma de vídeo aparece a 5 segundos en el archivo de origen, el tiempo del medio y el tiempo de presentación son 5 segundos. Si usa el origen [del secuenciador](sequencer-source.md), el modelo de control de tiempo es algo más complicado, para permitir transiciones fluidas entre segmentos. Para obtener más información sobre el modelo de tiempo del origen del secuenciador, vea [Tiempos de presentación de secuencia.](sequence-presentation-times.md)

El origen de medios siempre establece la marca de tiempo igual a la hora del medio. Si el tiempo de presentación no está alineado con la hora del medio, la sesión multimedia convierte las marcas de tiempo en los ejemplos multimedia. En el momento en que el receptor recibe una muestra, la marca de tiempo de la muestra se ha convertido al tiempo de presentación. El receptor programa el ejemplo con la hora actual del reloj de presentación. (Los receptores sin velocidad son una excepción, porque omiten el reloj de presentación).

Si la aplicación busca una nueva posición, la sesión multimedia reinicia el reloj de presentación a la hora de búsqueda especificada. Por ejemplo, si la aplicación busca la posición de 5 segundos en el archivo, la sesión multimedia inicia el reloj en 5 segundos. El origen de medios podría entregar ejemplos con una marca de tiempo ligeramente anterior si la hora de búsqueda no se encuentra en un límite de fotograma clave. Esto es necesario para que los descodificadores puedan descodificar todos los fotogramas. La sesión multimedia quita o recorta ejemplos antes de que lleguen a los receptores multimedia, para que coincidan con el tiempo de búsqueda solicitado. Por ejemplo, si el tiempo de búsqueda es de 5 segundos, la primera muestra de audio podría comenzar en 4,5 segundos. La sesión multimedia recortará los primeros 0,5 segundos de la primera muestra de audio descodificada.

## <a name="creating-the-presentation-clock"></a>Creación del reloj de presentación

Para crear el reloj de presentación, llame [**a MFCreatePresentationClock**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationclock). Para apagar el reloj, consulte la interfaz [**IMFShutdown**](/windows/desktop/api/mfidl/nn-mfidl-imfshutdown) y llame a [**IMFShutdown::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown). El autor de la **llamada de MFCreatePresentationClock** es responsable de llamar a **Shutdown**; En la mayoría de los casos, se trata de la sesión multimedia en lugar de la aplicación.

## <a name="presentation-time-sources"></a>Orígenes de tiempo de presentación

A pesar de su nombre, el reloj de presentación no implementa realmente un reloj. En su lugar, obtiene las horas del reloj de otro objeto, denominado origen *de la hora de presentación.* El origen de hora puede ser cualquier objeto que genere tics de reloj precisos y exponga la interfaz [**IMFPresentationTimeSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) En la siguiente ilustración se muestra este proceso.

![diagrama que muestra la relación entre el reloj de presentación y el origen de la hora de presentación](images/dedc255c-eb6d-49fc-8892-7b6076ed4488.gif)

Cuando se crea por primera vez el reloj de presentación, no tiene un origen de hora. Para establecer el origen de hora, llame a [**IMFPresentationClock::SetTimeSource**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-settimesource) con un puntero a la interfaz [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) del origen de la hora. Un origen de hora admite los mismos estados que el reloj de presentación (en ejecución, en pausa y en detenerse) y debe implementar la interfaz [**IMFClockStateSink.**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) El reloj de presentación usa esta interfaz para notificar al origen de hora cuándo se debe cambiar el estado. De este modo, el origen de la hora proporciona los tics del reloj, pero el reloj de presentación inicia los cambios de estado en el reloj.

Algunos receptores multimedia tienen acceso a un reloj preciso y, por lo tanto, exponen la interfaz [**IMFPresentationTimeSource.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource) En concreto, el representador de audio puede usar la frecuencia de la tarjeta de sonido como un reloj. En la reproducción de audio, resulta útil que el representador de audio actúe como origen de la hora, de modo que el vídeo se sincronice con la velocidad de reproducción de audio. Por lo general, esto genera mejores resultados que intentar hacer coincidir el audio con un reloj externo.

Media Foundation también proporciona un origen de hora de presentación basado en el reloj del sistema. Para crear este objeto, llame [**a MFCreateSystemTimeSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesystemtimesource). El origen de hora del sistema se puede usar cuando ningún receptor multimedia proporciona un origen de hora.

En general, un receptor multimedia debe usar el reloj de presentación que se le proporciona, independientemente del origen de hora que use el reloj de presentación. Esta regla se aplica incluso cuando un receptor multimedia implementa [**IMFPresentationTimeSource**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationtimesource). Si el reloj de presentación usa algún otro origen de hora, el receptor multimedia debe seguir ese origen de hora, no su propio reloj interno.

Hay dos situaciones en las que un receptor multimedia no seguirá el reloj de presentación:

-   Algunos receptores de medios *no tienen velocidad.* Si un receptor multimedia no tiene velocidad, consume muestras lo antes posible, sin programarlas según el reloj de presentación. Normalmente, los receptores sin velocidad escriben datos en un archivo, por lo que es conveniente completar la operación lo antes posible. Un receptor sin velocidad devuelve la marca RATELESS DE MEDIASINK en \_ su [**método IMFMediaSink::GetCharacteristics.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) Cuando todos los receptores de una topología no tienen velocidad, la sesión multimedia inserta los datos a través de la canalización lo más rápido posible.

-   Algunos receptores multimedia no pueden coincidir con velocidades con un origen de hora distinto de ellos mismos. Si es así, el receptor devuelve la marca MEDIASINK \_ CANNOT MATCH CLOCK en su método \_ \_ [**GetCharacteristics.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) La canalización todavía puede usar otro origen de hora, pero los resultados serán menores que los óptimos. Es probable que el receptor se retrase y cause problemas durante la reproducción.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation API de plataforma de aplicaciones](media-foundation-platform-apis.md)
</dt> </dl>

 

 



