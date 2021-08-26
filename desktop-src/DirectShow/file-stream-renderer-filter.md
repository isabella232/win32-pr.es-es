---
description: Filtro del representador de secuencias de archivos
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filtro del representador de secuencias de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3da8651d61559a9b22b722f91563426cb067f7a3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470570"
---
# <a name="file-stream-renderer-filter"></a>Filtro del representador de secuencias de archivos

El filtro Representador de secuencias de archivos representa los nombres de archivo que analiza el filtro [Analizador de varios](multi-file-parser-filter.md) archivos. Para obtener más información, consulte la documentación de ese filtro.

El uso de este filtro está en desuso. Para representar varios archivos dentro del mismo gráfico de filtros, la aplicación simplemente debe llamar varias veces a **RenderFile** **o AddSourceFilter.**




| | | Filtrado de interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Tipos de medios de pin de entrada | <ul><li>Tipo principal: MEDIATYPE_File</li><li>Subtipo: GUID_NULL</li><li>Tipo de formato: MEDIATYPE_File</li></ul> | | Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Tipos de medios de pin de salida | Ninguno | | Interfaces de pin de salida | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a> | | Filtrar clsid | CLSID_FileRend | | Archivos ejecutables | Quartz.dll | | <a href="merit.md">|</a> MERIT_UNLIKELY | | <a href="filter-categories.md">Categoría de</a> filtro | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Comentarios

El CLSID del filtro no está definido en Uuids.h. Use esta macro en su propio archivo de encabezado:


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



