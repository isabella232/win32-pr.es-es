---
description: Filtro Mux de AVI
ms.assetid: 31d30c91-fc6a-45ec-a2e0-34e6a1e902a4
title: Filtro Mux de AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f923ed944781bbaa36179b02db9022f38fc98ff6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478641"
---
# <a name="avi-mux-filter"></a>Filtro Mux de AVI

El filtro AVI Mux acepta varios flujos de entrada y los intercala en formato AVI. El filtro usa pasadores de entrada independientes para cada flujo de entrada y un pin de salida para el flujo AVI.

Las aplicaciones de creación o captura de vídeo pueden usar este filtro para guardar archivos en el disco en formato AVI. Normalmente, el filtro está conectado al filtro [File Writer,](file-writer-filter.md) pero puede conectarse a cualquier filtro cuyo pin de entrada admita las interfaces IStream e [**IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)




| | | Filtrar interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iconfigavimux"><strong>IConfigAviMux,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving"><strong>IConfigInterleaving,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag,</strong></a>ISpecifyPropertyPages | | Tipos de medios de pin de entrada | Cualquier tipo principal que se corresponda con un FOURCC de estilo antiguo o MEDIATYPE_AUXLine21Data. (Para obtener más información, vea <a href="fourccmap.md"><strong>FOURCCMap (Clase).</strong></a><ul><li>Si el tipo principal es MEDIATYPE_Audio, el formato debe ser FORMAT_WaveFormatEx.</li><li>Si el tipo principal es MEDIATYPE_Video, el formato debe ser FORMAT_VideoInfo o FORMAT_DvInfo.</li><li>Si el tipo principal es MEDIATYPE_Interleaved, el formato debe ser FORMAT_DvInfo.</li></ul> | | Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol"><strong>IAMStreamControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a>IPropertyBag, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de medios de pin de salida | MEDIATYPE_Stream, MEDIASUBTYPE_Avi | | Interfaces de pin de salida | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrar clsid | CLSID_AviDest | | ClSID de página de propiedades | CLSID_AviMuxProptyPage, CLSID_AviMuxProptyPage1 | | Archivos ejecutables | qcap.dll | | <a href="merit.md">Ventajas |</a> MERIT_DO_NOT_USE | | <a href="filter-categories.md">Filtrar categoría |</a> CLSID_LegacyAmFilterCategory | 




 

### <a name="remarks"></a>Comentarios

En los comentarios siguientes se describen varios aspectos de la funcionalidad del filtro AVI Mux.

Chinchetas

Cuando se crea el filtro AVI Mux, tiene un pin de entrada. A medida que se conecta cada pin de entrada, el filtro crea un nuevo pin de entrada.

Propiedades de la secuencia

Los pines de entrada admiten la interfaz IPropertyBag para establecer propiedades en secuencias individuales. Actualmente, se define la siguiente propiedad:



| Propiedad | Descripción                                                           |
|----------|-----------------------------------------------------------------------|
| name     | El nombre del flujo. Esta propiedad se escribe como `'strn'` un fragmento. |



 

Si el filtro se está ejecutando o en pausa, el método IPropertyBag::Write devuelve VFW \_ E \_ WRONG \_ STATE.

Velocidades de fotogramas

Si el filtro ascendente no especifica una velocidad de fotogramas en el miembro **AvgTimePerFrame** de la estructura [**VIDEOINFOHEADER,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) avi Mux usa las marcas de tiempo en el primer fotograma de vídeo. El formato de archivo AVI no admite velocidades de fotogramas variables.

Fotogramas eliminados

El filtro AVI Mux calcula los fotogramas descartados en función de los tiempos multimedia de cada muestra, si están disponibles, o de lo contrario, las marcas de tiempo de la muestra. Escribe una entrada de índice de longitud cero para cada fotograma eliminado.

IMediaSeeking

El filtro avi Mux implementa la [**interfaz IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) de la siguiente manera:

-   El [**método GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) devuelve el progreso actual de la multiplexación. Si va a transcodificación de un archivo (más lento que en tiempo real), este valor es más preciso que el valor devuelto por filter Graph Manager. Para obtener más información, vea la sección Comentarios de la página de referencia getCurrentPosition.
-   El [**método GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) consulta cada filtro ascendente y devuelve la duración de la secuencia más larga. Si alguno de estos filtros produce un error en la llamada a GetDuration (o no admite IMediaSeeking), avi Mux devuelve un código de error y rellena el parámetro *pDuration* con la duración más larga encontrada. Sin embargo, el valor *de pDuration en* este caso no es necesariamente la longitud del flujo de entrada más largo.
-   Avi Mux no implementa los métodos GetStopPosition, GetPositions, GetAvailable, GetRate ni GetPreroll; ni implementa ningún método Set \* para la búsqueda.

Extensiones de formato de archivo AVI 2.0

DirectShow admite actualmente las siguientes extensiones de formato de archivo AVI 2.0:

-   Mayor tamaño de archivo AVI (más de 1 GB)
-   Indexación jerárquica

Para obtener más información, vea la versión 1.02 de "Extensiones de formato de archivo OPENDML AVI" publicadas por el subcomando de formato de archivo M-JPEG de OpenDML AVI.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



