---
description: Filtro de representador de flujo de archivo
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filtro de representador de flujo de archivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64c8d8a0c87dab3aa811c8246be24ded8ee04dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537888"
---
# <a name="file-stream-renderer-filter"></a>Filtro de representador de flujo de archivo

El filtro de representador de secuencia de archivos representa los nombres de archivo que se analizan mediante el filtro del [analizador de varios archivos](multi-file-parser-filter.md) . Para obtener más información, consulte la documentación de ese filtro.

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
<li>Tipo principal: MEDIATYPE_File</li>
<li>Subtipo: GUID_NULL</li>
<li>Tipo de formato: MEDIATYPE_File</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td>None</td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>CLSID_FileRend</td>
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

El CLSID del filtro no está definido en UUID. h. Use esta macro en su propio archivo de encabezado:


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



