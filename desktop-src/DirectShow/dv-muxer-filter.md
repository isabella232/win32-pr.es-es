---
description: Filtro dv muxer
ms.assetid: 4dd57202-f4de-40d9-b720-efaba8a60a7c
title: Filtro dv muxer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 013251f2f9c1946aaa0f7b3c95edfd2de81c4d78
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127246615"
---
# <a name="dv-muxer-filter"></a>Filtro dv muxer

Este filtro combina un vídeo digital (DV): secuencia de vídeo codificada con una o dos secuencias de audio para generar una secuencia DV intercalada. Para escribir la secuencia en un archivo AVI, conecte este filtro al filtro [AVI Mux](avi-mux-filter.md) y conecte el *Mux* avi al filtro [file writer.](file-writer-filter.md) Para obtener más información, [vea Vídeo digital en DirectShow](digital-video-in-directshow.md).



| Etiqueta | Value |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                             |
| Tipos de medios de pin de entrada                    | **Vídeo:** MEDIATYPE \_ Video, MEDIASUBTYPE \_ dvsd, FORMAT \_ VideoInfo **Audio**: MEDIATYPE \_ Audio, MEDIASUBTYPE \_ PCM, FORMAT \_ WaveFormatEx |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                 |
| Tipos de medios de pin de salida                   | MEDIATYPE \_ intercalado, MEDIASUBTYPE \_ dvsd, FORMAT \_ DvInfo                                                                             |
| Interfaces de pin de salida                    | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                       |
| Filtrar CLSID                             | CLSID \_ DVMux                                                                                                                           |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                       |
| Executable                               | qdv.dll                                                                                                                                |
| [Mérito](merit.md)                       | NO PROBABLE \_ QUE SE PRODUZCAN LOS CASO                                                                                                                        |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                          |



 

## <a name="remarks"></a>Observaciones

Dv Muxer puede crear dos pines de entrada de audio. Admite los formatos de audio que se muestran en la tabla siguiente.



Patilla de audio 1

Patilla de audio 2

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

Desconectado

Canal SD 2

32

16

Estéreo

Desconectado

Canal SD 4

44.1 o 48

16

Estéreo o Mono

Desconectado

Canal SD 2

Desconectado

32

16

Estéreo o Mono

No permitida.

Desconectado

44.1 o 48

16

Mono

No permitida.

Desconectado

44.1 o 48

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

Estéreo o Mono\*

32

16

Estéreo o Mono\*

Canal SD 4

44.1

16

Mono

44.1

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

\* Si al menos un pin de entrada es estéreo.



 

Para esta tabla, el pin de audio 1 se define como el primer pin de entrada conectado a un origen de audio y el pin de audio 2 se define como el segundo pin de entrada conectado a un origen de audio. Una vez conectada una clavija de audio, este esquema de numeración permanece en vigor a menos que se desconecten ambas clavijas de audio. Por ejemplo, si conecta ambas clavijas de audio y, a continuación, desconecta el pin de audio 1, el pin restante todavía se considera el pin 2.

El audio proporcionado para anclar 1 se graba en el primer bloque de audio de los marcos DV (CH1) y el audio proporcionado para anclar 2 se graba en el segundo bloque de audio (CH2). Excepción: si el filtro tiene una única entrada estéreo a 44,1 kHz o 48 kHz, el canal de audio izquierdo se graba en el primer bloque de audio y el canal de audio derecho se graba en el segundo bloque de audio.

Para la salida sd de 4 canales: si la entrada es estéreo, la pista izquierda se graba en CHa o CHc y la pista derecha se registra en CHb o CHd. Si la entrada es mono, el audio se graba en CHa o CHc, y CHb y CHd son silenciosos.

Al conectar y desconectar el pin de audio 1, es posible alcanzar un formato no permitido. En ese caso, el método [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) del filtro devuelve VFW \_ E NOT \_ \_ CONNECTED. Esta limitación evita una situación en la que el primer bloque de audio no tiene audio, pero el segundo bloque de audio sí tiene audio. El segundo bloque solo debe tener audio si el primer bloque también tiene audio.

Dv Muxer no permite entradas de audio con diferentes velocidades de muestreo. Sin embargo, los métodos de creación de grafos como [**IGraphBuilder::Conectar**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) normalmente agregarán el filtro contenedor de [ACM,](acm-wrapper-filter.md) que convertirá la segunda secuencia de audio para que coincida con la velocidad de muestreo de la primera secuencia.

Si la entrada de audio es de 48 kHz o 32 kHz, la salida de audio se bloquea. (No es posible bloquear el audio de 44,1 kHz).

Si no hay ningún pin de audio conectado, la salida contiene los datos de audio de los fotogramas DV entrantes. Esto puede ser silencio o datos de audio válidos.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Vídeo digital en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



