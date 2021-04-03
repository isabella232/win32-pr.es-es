---
description: Filtro de multiplexor DV
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: Filtro de multiplexor DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2154dd1fc1617ff3f717b1ace6e52c9c507a38e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103806698"
---
# <a name="dv-muxer-filter"></a>Filtro de multiplexor DV

Este filtro combina una secuencia de vídeo codificada en vídeo digital (DV) con uno o dos flujos de audio para producir una secuencia DV intercalada. Para escribir el flujo en un archivo AVI, conecte este filtro al filtro de [AVI-MUX](avi-mux-filter.md) y conecte el filtro de escritura de *AVI* al filtro del escritor de [archivos](file-writer-filter.md) . Para obtener más información, vea [vídeo digital en DirectShow](digital-video-in-directshow.md).



|                                          |                                                                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                             |
| Tipos de medios de anclaje de entrada                    | **Vídeo**: mediatype \_ vídeo, MEDIASUBTYPE \_ DVSD, formato \_ videoinfo **audio**: mediatype \_ audio, MEDIASUBTYPE \_ PCM, format \_ WaveFormatEx |
| Interfaces de PIN de entrada                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                 |
| Tipos de medios de anclaje de salida                   | MEDIATYPE \_ intercalado, MEDIASUBTYPE \_ DVSD, format \_ DvInfo                                                                             |
| Interfaces de clavija de salida                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                       |
| Identificador CLSID                             | CLSID \_ DVMux                                                                                                                           |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                       |
| Executable                               | qdv.dll                                                                                                                                |
| [Fundament](merit.md)                       | MÉRITO \_ improbable                                                                                                                        |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                          |



 

## <a name="remarks"></a>Observaciones

La multiplexor DV puede crear dos clavijas de entrada de audio. Admite los formatos de audio que se muestran en la tabla siguiente.



PIN de audio 1

PIN de audio 2

Formato de salida

Frecuencia de muestreo (kHz)

Bits/ejemplo

Canales

Velocidad de muestreo

Bits/ejemplo

Canales

32

16

Mono

No conectado

Canal SD 2

32

16

Estéreo

No conectado

Canal SD 4

44,1 o 48

16

Estéreo o mono

No conectado

Canal SD 2

No conectado

32

16

Estéreo o mono

No permitida.

No conectado

44,1 o 48

16

Mono

No permitida.

No conectado

44,1 o 48

16

Estéreo

Canal SD 2

32

16

Mono

32

16

Mono

Canal SD 2

32

16

Estéreo o mono\*

32

16

Estéreo o mono\*

Canal SD 4

44,1

16

Mono

44,1

16

Mono

Canal SD 2

48

16

Mono

48

16

Mono

Canal SD 2

\* Si al menos un PIN de entrada es estéreo.



 

En esta tabla, el PIN de audio 1 se define como el primer PIN de entrada conectado a una fuente de audio, y el PIN de audio 2 se define como el segundo PIN de entrada conectado a un origen de audio. Una vez conectado un PIN de audio, este esquema de numeración permanece en vigor a menos que ambos pines de audio estén desconectados. Por ejemplo, si conecta ambos PIN de audio y, a continuación, desconecta el PIN de audio 1, el PIN restante todavía se considera pin 2.

El audio proporcionado al pin 1 se graba en el primer bloque de audio de los fotogramas DV (CH1), y el audio proporcionado al pin 2 se graba en el segundo bloque de audio (CH2). Excepción: Si el filtro tiene una sola entrada estéreo a 44,1 kHz o 48 kHz, el canal de audio izquierdo se graba en el primer bloque de audio y el canal de audio derecho se graba en el segundo bloque de audio.

Para la salida de canal SD 4: Si la entrada es estéreo, la pista de la izquierda se registra en CHa o CHc y la pista adecuada se registra en CHb o CHd. Si la entrada es mono, el audio se graba en CHa o CHc, y CHb y CHd son silenciosos.

Al conectar y desconectar el PIN de audio 1, es posible llegar a un formato no permitido. En ese caso, el método [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) del filtro devuelve VFW \_ E \_ not \_ connected. Esta limitación evita una situación en la que el primer bloque de audio no tiene audio, pero el segundo bloque de audio tiene audio. El segundo bloque solo debe tener audio si el primer bloque también tiene audio.

La multiplexor DV no permite entradas de audio con diferentes velocidades de muestreo. Sin embargo, los métodos de creación de gráficos como [**IGraphBuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) agregarán normalmente el filtro [contenedor ACM](acm-wrapper-filter.md) , que convertirá la segunda secuencia de audio para que coincida con la velocidad de muestreo de la primera secuencia.

Si la entrada de audio es 48 kHz o 32 kHz, la salida de audio está bloqueada. (No es posible bloquear audio de 44,1 kHz).

Si no hay ningún PIN de audio conectado, la salida contiene los datos de audio de los fotogramas DV entrantes. Esto podría ser el silencio o los datos de audio válidos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



