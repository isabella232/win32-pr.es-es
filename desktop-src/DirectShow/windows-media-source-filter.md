---
description: Filtro de origen de Windows Media
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Filtro de origen de Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa8e2c2f2e575a70d85fdce3d9b8d643e270f721
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909003"
---
# <a name="windows-media-source-filter"></a>Filtro de origen de Windows Media

Este filtro es el filtro de origen heredado para el contenido ® Windows Media. Lo usa Reproductor de Windows Media 6.4. En general, la manera más sencilla y confiable de usar este filtro es usar el control ActiveX Reproductor de Windows Media 6.4. Muchos de los métodos expuestos por este filtro también se exponen a través del control ActiveX. Consulte el SDK Reproductor de Windows Media para obtener más información.

Cuando a este filtro se le da el nombre de un archivo ASF local o una dirección URL para un archivo remoto, lee el archivo, analiza los flujos comprimidos y crea un pin de salida para cada uno. Este filtro no usa el SDK Windows Media Format. Usa las versiones de códec instalables de los descodificadores de Windows Media, no las versiones DMO. El pin de salida de audio siempre se conecta al filtro asf ACM Handler y la clavija de vídeo siempre se conecta al controlador de ICM de ASF. (En este caso, ICM hace referencia al nombre original del Administrador de compresión de vídeo). El filtro no admite búsquedas.

En el diagrama siguiente se muestra un gráfico de filtros con este filtro.

![Gráfico de filtro de origen de windows media](images/wms-wmv-graph.png)

Para mantener la compatibilidad con versiones anteriores con Reproductor de Windows Media 6.4, este filtro es el filtro de origen predeterminado para los archivos con extensiones de archivo .wma, .wmv y .asf. Para la reproducción de archivos, las aplicaciones más recientes deben usar el [filtro WM ASF Reader.](wm-asf-reader-filter.md) Sin embargo, el lector DE ASF de WM no admite la reproducción de contenido transmitido por secuencias.

La manera más sencilla de que una aplicación reprodgue contenido basado en Windows Media es usar el SDK Reproductor de Windows Media streaming. Otra opción es usar el SDK Windows Media Format. No se recomienda intentar crear un reproductor personalizado basado en el filtro de origen de Windows Media.



| Etiqueta | Value |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IAMChannelInfo,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo) [**IAMExtendedSeeking,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking) [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IAMNetShowConfig,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig) [**IAMNetShowExProps**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops), [**IAMNetShowPreroll**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll), [**IAMNetworkStatus**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) |
| Tipos de medios de pin de entrada                    | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Interfaces de pin de entrada                     | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Tipos de medios de pin de salida                   | Varía en función de las secuencias dentro del archivo ASF.                                                                                                                                                                                                                                                                                                                                                                                                               |
| Interfaces de pin de salida                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Filtrar CLSID                             | Consulte Comentarios                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Executable                               | dxmasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Mérito](merit.md)                       | NORMAL DE LA OPERACIÓN DE \_ NORMALIZACIÓN                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

## <a name="remarks"></a>Comentarios

El CLSID del filtro no está definido en qnetwork.h. Use esta macro en su propio archivo de encabezado:


```C++
//  {6B6D0800-9ADA-11d0-A520-00A0D10129C0}
DEFINE_GUID(CLSID_NetShowSource, 
0x6b6d0800, 0x9ada, 0x11d0, 0xa5, 0x20, 0x0, 0xa0, 0xd1, 0x1, 0x29, 0xc0);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> <dt>

[Lectura de archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> <dt>

[Filtro de lector asf de WM](wm-asf-reader-filter.md)
</dt> </dl>

 

 



