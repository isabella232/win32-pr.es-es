---
description: Acerca del filtro de lector ASF de WM
ms.assetid: e698c0da-88b2-497a-8a25-9d3b76c85a7d
title: Acerca del filtro de lector ASF de WM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b71d0b25070c446ebff88f18785df7b55ba7bbcc7b1bcaa1dcf21995185252ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873705"
---
# <a name="about-the-wm-asf-reader-filter"></a>Acerca del filtro de lector ASF de WM

La reproducción de archivos ASF se controla mediante el filtro [WM ASF Reader.](wm-asf-reader-filter.md) Cuando el lector DE ASF de WM lee un archivo, crea automáticamente un pin de salida para cada secuencia, incluidos flujos web, secuencias de comandos de script y cualquier otro tipo de secuencia arbitraria. En el caso de varios archivos de velocidad de bits, los pins solo se crean para las secuencias seleccionadas actualmente. Para reproducir un archivo ASF con el filtro WM ASF Reader, llame a [**IGraphBuilder::RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) o [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter).

Wm ASF Reader admite la interfaz DirectShow [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) que permite a las aplicaciones realizar búsquedas temporales dentro del archivo. Sin embargo, no se admite la reproducción a velocidades diferentes de 1.0 (como se especifica en [**IMediaSeeking::SetRate).**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setrate)

El filtro WM ASF Reader también expone varias interfaces Windows SDK de formato multimedia, como se describe en la tabla siguiente. Estas interfaces se documentan en la documentación Windows SDK de formato multimedia.



| Interfaz                                             | Exposición                                 | Comentarios                                                                                                                       |
|-------------------------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**IWMDRMReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | A **través de IServiceProvider** en el filtro. | Se proporciona para las aplicaciones que necesitan reproducir contenido protegido por Digital Rights Management (DRM).                             |
| [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** en el filtro.           | Se proporciona para que las aplicaciones puedan leer atributos de archivo y contenido, así como información de marcadores y scripts y metadatos.     |
| [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** en el filtro.           | Parcialmente implementado en el filtro para que las aplicaciones puedan tener acceso a los métodos informativos en el objeto WM Reader.         |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** en el filtro.           | Parcialmente implementado en el filtro para que las aplicaciones puedan acceder a los métodos informativos en el objeto de lector del SDK de formato. |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Lectura de archivos ASF en DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



