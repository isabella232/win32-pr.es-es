---
description: Filtro de divisor de AVI
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: Filtro de divisor de AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e61b9a60c4c42aafa875c166ae08ccdf337793c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104152602"
---
# <a name="avi-splitter-filter"></a>Filtro de divisor de AVI

El filtro de divisor de AVI se usa para la reproducción de archivos AVI. Acepta los datos en formato AVI y los divide en sus flujos constituyentes para su procesamiento y/o representación.



|                                          |                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)                        |
| Tipos de medios de anclaje de entrada                    | \_Secuencia MEDIATYPE, MEDIASUBTYPE \_ AVI                                                                                                                                |
| Interfaces de PIN de entrada                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                    |
| Tipos de medios de anclaje de salida                   | Normalmente **, \_ vídeo** o **\_ audio de mediatype**. El tipo exacto depende del contenido del archivo, si el archivo está comprimido y qué códec se ha usado. |
| Interfaces de clavija de salida                    | [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)    |
| Identificador CLSID                             | CLSID \_ AviSplitter                                                                                                                                                  |
| CLSID de la página de propiedades                      | Ninguna página de propiedades.                                                                                                                                                   |
| Executable                               | quartz.dll                                                                                                                                                          |
| [Fundament](merit.md)                       | MÉRITO \_ normal                                                                                                                                                       |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                       |



 

## <a name="remarks"></a>Observaciones

Este filtro se conecta normalmente al filtro de [origen de archivo asincrónico](file-source--async--filter.md) en su PIN de entrada. Puede conectarse a cualquier filtro cuyo PIN de salida admita [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) y ofrezca el tipo de medio correcto al pin de entrada del filtro de divisor de AVI.

Los pin de salida del divisor de AVI admiten el método IPropertyBag:: Read para leer propiedades de flujos individuales. Actualmente, se define la propiedad siguiente.



| Propiedad | Descripción                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| name     | Devuelve el nombre de la secuencia, tomada del `'strn'` fragmento en el archivo AVI. Si este fragmento está ausente, el método Read devuelve E \_ INVALIDARG. |



 

El método IPropertyBag:: Write devuelve E \_ Fail. El filtro de [AVI MUX](avi-mux-filter.md) admite IPropertyBag:: Write para guardar las propiedades de la secuencia en un archivo AVI.

El divisor de AVI no permite que los filtros de nivel inferior utilicen su propio asignador.

La duración de intercalación en el archivo determina la cantidad de memoria que el divisor de AVI asignará para procesarla. Un archivo intercalado en fragmentos de un segundo requerirá mucha más memoria para procesarse que un archivo cuya duración de intercalación está establecida en uno o dos fotogramas. En los equipos modernos, este no suele ser un problema, a menos que se ejecuten varias instancias del divisor de AVI simultáneamente.

### <a name="seeking"></a>Invoca

Si el archivo contiene una secuencia de vídeo, el divisor de AVI admite búsquedas por número de fotogramas. Para habilitar la búsqueda basada en fotogramas, llame a [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) en el [Administrador de gráficos de filtro](filter-graph-manager.md) con el **\_ \_ marco de formato de hora** de valor.

Si el archivo contiene una secuencia de audio, el divisor de AVI admite búsquedas por número de muestra. Para habilitar la búsqueda basada en el ejemplo, llame a [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) en el administrador de gráficos de filtro con el **ejemplo de \_ formato \_ de hora** de valor.

En ambos casos, el PIN de salida de esa secuencia debe estar conectado a un filtro de representador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



