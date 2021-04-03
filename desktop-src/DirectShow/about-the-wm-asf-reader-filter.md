---
description: Acerca del filtro de lector ASF de WM
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: Acerca del filtro de lector ASF de WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 350e6597aa6aa66193af37a30ed54c37139d5f81
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906773"
---
# <a name="about-the-wm-asf-reader-filter"></a>Acerca del filtro de lector ASF de WM

La reproducción de archivos ASF se controla mediante el filtro [lector ASF de WM](wm-asf-reader-filter.md) . Cuando el lector ASF de WM lee un archivo, crea automáticamente un PIN de salida para cada flujo, incluidas las secuencias Web, secuencias de comandos de script y cualquier otro tipo de secuencia arbitraria. En el caso de varios archivos de velocidad de bits, los pin solo se crean para las secuencias seleccionadas actualmente. Para reproducir un archivo ASF con el filtro de lector ASF de WM, llame a [**IGraphBuilder:: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) o [**IGraphBuilder:: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).

El lector ASF de WM admite la interfaz [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) de DirectShow, que permite a las aplicaciones realizar búsquedas temporales en el archivo. Sin embargo, no se admite la reproducción a velocidades distintas de 1,0 (tal y como se especifica en [**IMediaSeeking:: SetRate**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)).

El filtro lector ASF de WM también expone varias interfaces del SDK de Windows Media Format, como se describe en la tabla siguiente. Estas interfaces se documentan en la documentación del SDK de Windows Media Format.



| Interfaz                                             | Cómo se exponen                                 | Comentarios                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | A través de **IServiceProvider** en el filtro. | Se proporciona para las aplicaciones que necesitan reproducir contenido protegido por Rights Management digitales (DRM).                             |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** en el filtro.           | Proporcionado para que las aplicaciones puedan leer atributos de archivo y de contenido, así como información de marcadores y metadatos.     |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** en el filtro.           | Implementado parcialmente en el filtro para que las aplicaciones puedan tener acceso a los métodos informativos del objeto lector de WM.         |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** en el filtro.           | Implementado parcialmente en el filtro para que las aplicaciones puedan tener acceso a los métodos informativos del objeto lector SDK Reader. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Leer archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



