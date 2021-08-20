---
description: Filtro del escritor de archivos
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Filtro del escritor de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9f21009d8135cb42ec93c4f5727398dcdf3094ed4e5da666c325c959dbffc16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651375"
---
# <a name="file-writer-filter"></a>Filtro del escritor de archivos

El filtro Escritor de archivos se puede usar para escribir archivos en un disco independientemente del formato. El filtro simplemente escribe en el disco lo que recibe en su pin de entrada, por lo que debe estar conectado ascendentemente a un multiplexor que pueda dar formato al archivo correctamente. Puede crear un nuevo archivo de salida con el escritor de archivos o especificar un archivo existente. Si el archivo ya existe, se sobrescribirá completamente con los nuevos datos.

El filtro de escritor de archivos usa las marcas de tiempo del flujo de entrada como desplazamientos de archivo y proporciona acceso aleatorio al archivo. Admite **IStream para** permitir la lectura y escritura del encabezado de archivo después de detener el gráfico. Para mejorar el rendimiento, también admite escrituras superpuestas no almacenadas en búfer y controla la negociación de búfer correspondiente.

> [!Note]  
> Para escribir archivos ASF, use el filtro [WM ASF Writer.](wm-asf-writer-filter.md)

 



| Etiqueta | Valor |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interfaces de filtro                        | [**IAMFilterMiscFlags,**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags) [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2,**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2) **IPersistStream** |
| Tipos de medios de pin de entrada                    | SECUENCIA \_ MEDIATYPE, MEDIASUBTYPE \_ NULL                                                                                                                                                              |
| Interfaces de pin de entrada                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) **IStream**                                                                                |
| Tipos de medios de pin de salida                   | No aplicable                                                                                                                                                                                     |
| Interfaces de pin de salida                    | No aplicable                                                                                                                                                                                     |
| Filtrar CLSID                             | CLSID \_ FileWriter                                                                                                                                                                                  |
| CLSID de la página de propiedades                      | Ninguna página de propiedades                                                                                                                                                                                   |
| Executable                               | qcap.dll                                                                                                                                                                                           |
| [Mérito](merit.md)                       | NO USE EL VALOR DE NO \_ \_ \_ USE.                                                                                                                                                                                |
| [Categoría de filtro](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                                                                      |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



