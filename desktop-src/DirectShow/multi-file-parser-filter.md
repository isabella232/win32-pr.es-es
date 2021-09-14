---
description: Filtro del analizador de varios archivos
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: Filtro del analizador de varios archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a91196f9712dc05e64f1d70072d3af9d1c0a39f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254331"
---
# <a name="multi-file-parser-filter"></a>Filtro del analizador de varios archivos

El filtro Analizador de varios archivos analiza un formato de archivo simple que permite especificar varios nombres de archivo como si fueran un archivo. Estos archivos tienen el formato que se muestra en el ejemplo siguiente:


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



El uso de este filtro está en desuso. Para representar varios archivos dentro del mismo gráfico de filtros, la aplicación simplemente debe llamar varias veces a **RenderFile** **o AddSourceFilter.**




| Etiqueta | Value |
|--------|-------|
| Interfaces de filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | 
| Tipos de medios de pin de entrada | <ul><li>Tipo principal: MEDIATYPE_Stream</li><li>Subtipo: CLSID_MultFile</li><li>Tipo de formato: GUID_NULL</li></ul> | 
| Interfaces de pin de entrada | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Tipos de medios de pin de salida | <ul><li>Tipo principal: MEDIATYPE_File</li><li>Subtipo: GUID_NULL</li><li>Tipo de formato: MEDIATYPE_File</li></ul> | 
| Interfaces de pin de salida | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Filtrar CLSID | CLSID_MultFile | 
| Executable | Quartz.dll | 
| <a href="merit.md">Mérito</a> | MERIT_UNLIKELY | 
| <a href="filter-categories.md">Categoría de filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Observaciones

El filtro crea un pin de salida para cada archivo enumerado en el archivo de origen. El tipo de salida es MEDIATYPE File y el bloque de formato para el tipo de salida es una cadena de caracteres \_ anchos que contiene el nombre de archivo. Cada pin se conecta a una instancia del filtro [Representador de secuencias de](file-stream-renderer-filter.md) archivos. El filtro Representador de secuencias de archivos crea un pin de salida, que expone la [**interfaz IStreamBuilder.**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) El pin de salida representa el archivo especificado. Ningún dato multimedia viaja entre el analizador de varios archivos y el representador de secuencias de archivos.

El CLSID del filtro no está definido en Uuids.h. Use esta macro en su propio archivo de encabezado:


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[DirectShow Filtros](directshow-filters.md)
</dt> </dl>

 

 



