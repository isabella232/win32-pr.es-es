---
description: Filtro de representador de secuencias de archivos
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filtro de representador de secuencias de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d438d77b4f402cefed2e80f2c32d061d1652710f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255159"
---
# <a name="file-stream-renderer-filter"></a>Filtro de representador de secuencias de archivos

El filtro Representador de secuencias de archivos representa los nombres de archivo que analiza el filtro [Analizador de varios](multi-file-parser-filter.md) archivos. Para más información, consulte la documentación de ese filtro.

El uso de este filtro está en desuso. Para representar varios archivos dentro del mismo gráfico de filtro, la aplicación simplemente debe llamar a **RenderFile** o **AddSourceFilter** varias veces.




| Etiqueta | Value |
|--------|-------|
| Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | 
| Tipos de medios de pin de entrada | <ul><li>Tipo principal: MEDIATYPE_File</li><li>Subtipo: GUID_NULL</li><li>Tipo de formato: MEDIATYPE_File</li></ul> | 
| Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Tipos de medios de pin de salida | None | 
| Interfaces de pin de salida | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a> | 
| Filtrar CLSID | CLSID_FileRend | 
| Executable | Quartz.dll | 
| <a href="merit.md">Mérito</a> | MERIT_UNLIKELY | 
| <a href="filter-categories.md">Categoría de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Observaciones

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

 

 



