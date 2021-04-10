---
description: Filtro de origen de Windows Media
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Filtro de origen de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe60a038cfd5109a5c55ca6c40640d39b2426d3a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279781"
---
# <a name="windows-media-source-filter"></a>Filtro de origen de Windows Media

Este filtro es el filtro de origen heredado para el contenido de Windows Media®. Lo usa Windows Media Player 6,4. En general, la manera más sencilla y confiable de usar este filtro es usar el control ActiveX de Windows Media Player 6,4. Muchos de los métodos expuestos por este filtro también se exponen a través del control ActiveX. Para obtener más información, consulte el SDK de Windows Media Player.

Cuando este filtro recibe el nombre de un archivo ASF local o de una dirección URL de un archivo remoto, lee el archivo, analiza los flujos comprimidos y crea un PIN de salida para cada uno de ellos. Este filtro no utiliza el SDK de Windows Media Format. Usa las versiones de códec instalables de los descodificadores de Windows Media, no las versiones de DMO. El PIN de salida de audio siempre se conecta al filtro del controlador ACM de ASF y el PIN de vídeo siempre se conecta al controlador ICM de ASF. (ICM en este caso hace referencia al nombre original del administrador de compresión de vídeo). El filtro no admite búsquedas.

En el diagrama siguiente se muestra un gráfico de filtros con este filtro.

![gráfico de filtro de origen de Windows Media](images/wms-wmv-graph.png)

Para mantener la compatibilidad con versiones anteriores de Windows Media Player 6,4, este filtro es el filtro de origen predeterminado para los archivos con las extensiones de archivo. WMA,. WMV y. ASF. Para la reproducción de archivos, las aplicaciones más recientes deben usar el filtro de [lector ASF de WM](wm-asf-reader-filter.md) . Sin embargo, el lector ASF de WM no admite la reproducción de contenido transmitido por secuencias.

La forma más sencilla de que una aplicación reproduzca contenido basado en Windows Media de transmisión por secuencias es usar el SDK de Windows Media Player. Otra opción es usar el SDK de Windows Media Format. No se recomienda intentar crear un reproductor personalizado basado en el filtro de origen de Windows Media.



|                                          |                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMChannelInfo**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo), [**IAMExtendedSeeking**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking), [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IAMNetShowConfig**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig), [**IAMNetShowExProps**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops), [**IAMNetShowPreroll**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll), [**IAMNetworkStatus**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) |
| Tipos de medios de anclaje de entrada                    | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Interfaces de PIN de entrada                     | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Tipos de medios de anclaje de salida                   | Varía en función de las secuencias del archivo ASF.                                                                                                                                                                                                                                                                                                                                                                                                               |
| Interfaces de clavija de salida                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Identificador CLSID                             | Ver comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Executable                               | dxmasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Fundament](merit.md)                       | MÉRITO \_ normal                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Observaciones

El CLSID del filtro no está definido en qnetwork. h. Use esta macro en su propio archivo de encabezado:


```C++
//  {6B6D0800-9ADA-11d0-A520-00A0D10129C0}
DEFINE_GUID(CLSID_NetShowSource, 
0x6b6d0800, 0x9ada, 0x11d0, 0xa5, 0x20, 0x0, 0xa0, 0xd1, 0x1, 0x29, 0xc0);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Leer archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> <dt>

[Filtro de lector ASF de WM](wm-asf-reader-filter.md)
</dt> </dl>

 

 



