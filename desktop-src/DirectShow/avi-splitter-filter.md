---
description: Filtro divisor avi
ms.assetid: df3c7d11-7ecc-499a-af36-b74437e21999
title: Filtro de divisor AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24335511e9b7b866c85792c2036a4d4b6d089f2a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909663"
---
# <a name="avi-splitter-filter"></a>Filtro de divisor AVI

El filtro divisor de AVI se usa para la reproducción de archivos AVI. Acepta datos en formato AVI y los divide en sus flujos constituyentes para su posterior procesamiento o representación.



| Etiqueta | Value |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMMediaContent,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag)                        |
| Tipos de medios de pin de entrada                    | MEDIATYPE \_ Stream, MEDIASUBTYPE \_ Avi                                                                                                                                |
| Interfaces de pin de entrada                     | [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                                                                                    |
| Tipos de medios de pin de salida                   | Normalmente, **vídeo MEDIATYPE \_** o **\_ audio MEDIATYPE**. El tipo exacto depende del contenido del archivo, de si el archivo está comprimido y del códec que se usó. |
| Interfaces de pin de salida                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin)IPropertyBag, [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)    |
| Filtrar CLSID                             | CLSID \_ AviSplitter                                                                                                                                                  |
| CLSID de la página de propiedades                      | No hay ninguna página de propiedades.                                                                                                                                                   |
| Executable                               | quartz.dll                                                                                                                                                          |
| [Mérito](merit.md)                       | PROCEDIMIENTO \_ NORMAL                                                                                                                                                       |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                       |



 

## <a name="remarks"></a>Comentarios

Este filtro normalmente está conectado al filtro [Async File Source](file-source--async--filter.md) (Origen de archivo asincrónico) en su pin de entrada. Puede conectarse a cualquier filtro cuyo pin de salida admita [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) y ofrece el tipo de medio correcto al pin de entrada del filtro del divisor AVI.

Los pines de salida del divisor AVI admiten el método IPropertyBag::Read para leer propiedades de secuencias individuales. Actualmente, se define la siguiente propiedad.



| Propiedad | Descripción                                                                                                                                    |
|----------|------------------------------------------------------------------------------------------------------------------------------------------------|
| name     | Devuelve el nombre de la secuencia, tomado del `'strn'` fragmento del archivo AVI. Si este fragmento no está presente, el método Read devuelve E \_ INVALIDARG. |



 

El método IPropertyBag::Write devuelve E \_ FAIL. El [filtro AVI Mux](avi-mux-filter.md) admite IPropertyBag::Write para guardar las propiedades de flujo en un archivo AVI.

El divisor AVI no permite que los filtros de nivel inferior usen su propio asignador.

La duración de intercalación en el archivo determina la cantidad de memoria que asignará el divisor AVI para procesarlo. Un archivo intercalado en fragmentos de un segundo requerirá mucho más memoria para procesar que un archivo cuya duración de intercalación se establece en uno o dos fotogramas. En equipos modernos, esto no suele ser un problema a menos que ejecute varias instancias del divisor AVI simultáneamente.

### <a name="seeking"></a>Buscando

Si el archivo contiene una secuencia de vídeo, el divisor AVI admite la búsqueda por número de fotograma. Para habilitar la búsqueda basada en fotogramas, llame a [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) en el Administrador de [gráficos](filter-graph-manager.md) de filtros con el valor **TIME FORMAT \_ \_ FRAME**.

Si el archivo contiene una secuencia de audio, el divisor AVI admite la búsqueda por número de ejemplo. Para habilitar la búsqueda basada en muestras, llame [**a SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) en el Administrador de gráficos de filtros con el valor **TIME FORMAT \_ \_ SAMPLE**.

En ambos casos, la patilla de salida de esa secuencia debe estar conectada a un filtro de representador.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



