---
description: Filtro de representador de comando de script interno
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Filtro de representador de comando de script interno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b241643d991e9348015dc51ea5b2f1c4875f079d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537348"
---
# <a name="internal-script-command-renderer-filter"></a>Filtro de representador de comando de script interno

Recibe comandos de script y los envía a la aplicación.

Este filtro acepta comandos de script en uno de los dos formatos siguientes:

-   \_Texto MEDIATYPE: cada ejemplo multimedia contiene una cadena de texto ANSI.
-   MEDIATYPE \_ comando: cada ejemplo multimedia contiene dos cadenas Unicode terminadas en null, concatenadas entre sí. La primera cadena describe el tipo de comando y la segunda cadena es el comando de script.

    Cuando el filtro recibe un ejemplo, envía una notificación de evento de [**\_ \_ evento OLE de EC**](ec-ole-event.md) . El primer parámetro de evento es un **BSTR** con el tipo de comando o `Text` si el formato es \_ texto de MEDIATYPE. El segundo parámetro de evento es un **BSTR** con el comando de script. La aplicación puede recuperar el evento y responder al comando de script.

Para obtener un ejemplo de cómo usar este filtro, vea [Sami (CC) parser](sami--cc--parser-filter.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtro</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de entrada</td>
<td><ul>
<li>MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</li>
<li>MEDIATYPE_Text, MEDIASUBTYPE_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de PIN de entrada</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Tipos de medios de anclaje de salida</td>
<td>No aplicable</td>
</tr>
<tr class="odd">
<td>Interfaces de clavija de salida</td>
<td>No aplicable</td>
</tr>
<tr class="even">
<td>Identificador CLSID</td>
<td>{48025243-2D39-11CE-875D-00608CB78066}</td>
</tr>
<tr class="odd">
<td>CLSID de la página de propiedades</td>
<td>Ninguna página de propiedades</td>
</tr>
<tr class="even">
<td>Executable</td>
<td>Quartz.dll</td>
</tr>
<tr class="odd">
<td><a href="merit.md">Fundament</a></td>
<td>MERIT_PREFERRED + 1</td>
</tr>
<tr class="even">
<td><a href="filter-categories.md">Categoría de filtro</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Filtros de DirectShow](directshow-filters.md)
</dt> </dl>

 

 



