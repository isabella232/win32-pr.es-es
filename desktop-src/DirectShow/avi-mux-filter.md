---
description: Filtro de AVI-MUX
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: Filtro de AVI-MUX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3755a4d5f63e824ae08eb736a5999dcac3d7ab32
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906826"
---
# <a name="avi-mux-filter"></a>Filtro de AVI-MUX

El filtro de AVI-MUX acepta varios flujos de entrada y los intercala en formato AVI. El filtro utiliza clavijas de entrada independientes para cada flujo de entrada y un PIN de salida para el flujo AVI.

Las aplicaciones de captura de vídeo o de creación pueden utilizar este filtro para guardar archivos en el disco en formato AVI. Normalmente, el filtro se conecta al filtro del [escritor de archivos](file-writer-filter.md) , pero puede conectarse a cualquier filtro cuyo PIN de entrada admita las interfaces IStream e [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a>, ISpecifyPropertyPages</td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td>Cualquier tipo principal que se corresponda con un FOURCC de estilo antiguo o MEDIATYPE_AUXLine21Data. (Para obtener más información, vea <a href="fourccmap.md"><strong>clase FOURCCMap</strong></a>).
<ul>
<li>Si el tipo principal es MEDIATYPE_Audio, el formato debe ser FORMAT_WaveFormatEx.</li>
<li>Si el tipo principal es MEDIATYPE_Video, el formato debe ser FORMAT_VideoInfo o FORMAT_DvInfo.</li>
<li>Si el tipo principal es MEDIATYPE_Interleaved, el formato debe ser FORMAT_DvInfo.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td>MEDIATYPE_Stream, MEDIASUBTYPE_Avi</td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>CLSID_AviDest</td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td>CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1</td>
</tr>
<tr class="even">
<td>Executable</td>
<td>qcap.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Fundament</a></td>
<td>MERIT_DO_NOT_USE</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

### <a name="remarks"></a>Observaciones

En los comentarios siguientes se describen diversos aspectos de la funcionalidad del filtro de AVI.

Chinchetas

Cuando se crea el filtro de AVI, tiene un PIN de entrada. A medida que cada pin de entrada está conectado, el filtro crea un nuevo PIN de entrada.

Propiedades de la secuencia

Los pin de entrada admiten la interfaz IPropertyBag para establecer propiedades en flujos individuales. Actualmente, se define la propiedad siguiente:



| Propiedad | Descripción                                                           |
|----------|-----------------------------------------------------------------------|
| name     | El nombre del flujo. Esta propiedad se escribe como un `'strn'` fragmento. |



 

Si el filtro se está ejecutando o está en pausa, el método IPropertyBag:: Write devuelve el \_ Estado VFW E \_ incorrecto \_ .

Velocidades de fotogramas

Si el filtro de nivel superior no especifica una velocidad de fotogramas en el miembro **AvgTimePerFrame** de la estructura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) , el MUX de AVI usa las marcas de tiempo en el primer fotograma de vídeo. El formato de archivo AVI no admite velocidades de fotogramas variables.

Fotogramas quitados

El filtro de AVI de AVI calcula los fotogramas quitados según las horas de los medios de cada ejemplo, si están disponibles, o bien las marcas de tiempo del ejemplo. Escribe una entrada de índice de longitud cero para cada fotograma quitado.

IMediaSeeking

El filtro de AVI-MUX implementa la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) como se indica a continuación:

-   El método [**GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) devuelve el progreso actual de la multiplexación. Si va a transcodificar un archivo (más lento que en tiempo real), este valor es más preciso que el valor devuelto por el administrador de gráficos de filtro. Para obtener más información, vea la sección Comentarios de la página de referencia de GetCurrentPosition.
-   El método [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) consulta cada filtro de nivel superior y devuelve la duración de la secuencia más larga. Si alguno de estos filtros produce un error en la llamada a GetDuration (o no admite IMediaSeeking), el MUX de AVI devuelve un código de error y rellena el parámetro *pDuration* con la duración más larga encontrada. Sin embargo, el valor de *pDuration* en este caso no es necesariamente la longitud del flujo de entrada más largo.
-   AVI MUX no implementa los métodos GetStopPosition, GetPositions, GetAvailable, GetRate o GetPreroll. tampoco implementa ningún \* método Set para realizar búsquedas.

Extensiones de formato de archivo AVI 2,0

DirectShow actualmente admite las siguientes extensiones de formato de archivo AVI 2,0:

-   Aumento del tamaño de archivo AVI (más de 1 GB)
-   Indexación jerárquica

Para obtener más información, consulte la versión 1,02 de las "extensiones de formato de archivo AVI de OpenDML" publicada por el Subcomité formato de archivo AVI OpenDML AVI-JPEG.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



