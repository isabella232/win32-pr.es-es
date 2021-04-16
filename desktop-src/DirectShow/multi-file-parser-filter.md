---
description: Filtro de analizador de varios archivos
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: Filtro de analizador de varios archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fc83a56bb12c307b85be875a3a2e7e73b744d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105686353"
---
# <a name="multi-file-parser-filter"></a>Filtro de analizador de varios archivos

El filtro de analizador de varios archivos analiza un formato de archivo simple que permite especificar varios nombres de archivo como si fueran un archivo. Estos archivos tienen el formato que se muestra en el ejemplo siguiente:


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



El uso de este filtro está en desuso. Para representar varios archivos en el mismo gráfico de filtros, la aplicación simplemente debe llamar a **RenderFile** o **AddSourceFilter** varias veces.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td><ul>
<li>Tipo principal: MEDIATYPE_Stream</li>
<li>Subtipo: CLSID_MultFile</li>
<li>Tipo de formato: GUID_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td><ul>
<li>Tipo principal: MEDIATYPE_File</li>
<li>Subtipo: GUID_NULL</li>
<li>Tipo de formato: MEDIATYPE_File</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>CLSID_MultFile</td>
</tr>
<tr class="odd">
<td>Executable</td>
<td>Quartz.dll</td>
</tr>
<tr class="even">
<td><a href="merit.md">Fundament</a></td>
<td>MERIT_UNLIKELY</td>
</tr>
<tr class="odd">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

El filtro crea un PIN de salida para cada archivo que aparece en el archivo de código fuente. El tipo de salida es el \_ archivo MEDIATYPE y el bloque de formato para el tipo de salida es una cadena de caracteres anchos que contiene el nombre de archivo. Cada pin se conecta a una instancia del filtro de [representador de secuencia de archivos](file-stream-renderer-filter.md) . El filtro de representador de flujo de archivo crea un PIN de salida, que expone la interfaz [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) . El PIN de salida representa el archivo especificado. No viajan los datos multimedia entre el analizador de varios archivos y el representador de flujo de archivos.

El CLSID del filtro no está definido en UUID. h. Use esta macro en su propio archivo de encabezado:


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



