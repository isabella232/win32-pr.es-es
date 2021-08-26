---
description: Windows Filtro de origen de medios
ms.assetid: e59b3086-4f62-4541-8bef-b0581f01906f
title: Windows Filtro de origen de medios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb1e617a51095aec7cb409e46ba8f19f14f76fcd6f8d8a9bffeaa13843b1728b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982215"
---
# <a name="windows-media-source-filter"></a>Windows Filtro de origen de medios

Este filtro es el filtro de origen heredado para Windows contenido ® multimedia. Lo usa Reproductor de Windows Media 6.4. En general, la manera más sencilla y confiable de usar este filtro es usar el control Reproductor de Windows Media 6.4 ActiveX 6.4. Muchos de los métodos expuestos por este filtro también se exponen a través del control ActiveX datos. Consulte el SDK Reproductor de Windows Media para obtener más información.

Cuando a este filtro se le da el nombre de un archivo ASF local o una dirección URL para un archivo remoto, lee el archivo, analiza los flujos comprimidos y crea un pin de salida para cada uno. Este filtro no usa el SDK Windows Media Format. Usa las versiones de códec instalables de los descodificadores Windows multimedia, no las versiones DMO instalación. El pin de salida de audio siempre se conecta al filtro asf ACM Handler y el pin de vídeo siempre se conecta al controlador de ICM ASF. (ICM en este caso hace referencia al nombre original del Administrador de compresión de vídeo). El filtro no admite búsquedas.

En el diagrama siguiente se muestra un gráfico de filtros con este filtro.

![Gráfico de filtro de origen de windows media](images/wms-wmv-graph.png)

Para mantener la compatibilidad con versiones anteriores con Reproductor de Windows Media 6.4, este filtro es el filtro de origen predeterminado para los archivos con extensiones de archivo .wma, .wmv y .asf. Para la reproducción de archivos, las aplicaciones más recientes deben usar el [filtro WM ASF Reader.](wm-asf-reader-filter.md) Sin embargo, wm asf reader no admite la reproducción de contenido transmitido.

La manera más sencilla de que una aplicación reprodgue contenido Windows basado en multimedia es usar el SDK Reproductor de Windows Media. Otra opción es usar el SDK Windows Media Format. No se recomienda intentar crear un reproductor personalizado basado en Windows filtro de origen multimedia.



| Etiqueta | Value |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IAMChannelInfo,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamchannelinfo) [**IAMExtendedSeeking,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamextendedseeking) [**IAMMediaContent,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent) [**IAMOpenProgress,**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress) [**IAMNetShowConfig,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowconfig) [**IAMNetShowExProps,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowexprops) [**IAMNetShowPreroll,**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetshowpreroll) [**IAMNetworkStatus**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iamnetworkstatus), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) |
| Tipos de medios de pin de entrada                    | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Interfaces de pin de entrada                     | No es aplicable.                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Tipos de medios de pin de salida                   | Varía en función de las secuencias dentro del archivo ASF.                                                                                                                                                                                                                                                                                                                                                                                                               |
| Interfaces de pin de salida                    | [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Filtrar CLSID                             | Consulte Comentarios.                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Executable                               | dxmasf.dll                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [Mérito](merit.md)                       | PROCEDIMIENTO \_ NORMAL                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
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

[DirectShow Filtros](directshow-filters.md)
</dt> <dt>

[Lectura de archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> <dt>

[Filtro de lector DE ASF de WM](wm-asf-reader-filter.md)
</dt> </dl>

 

 



