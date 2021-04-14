---
title: Elemento sourceFilter
description: El elemento sourceFilter contiene elementos que seleccionan elementos de una biblioteca.
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- Elemento sourceFilter Media Player Windows
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb43a9577c5fe8857b63067db5be90d314037b84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653868"
---
# <a name="sourcefilter-element"></a>Elemento sourceFilter

El elemento **sourceFilter** contiene elementos que seleccionan elementos de una biblioteca.

``` syntax
<sourceFilter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</sourceFilter>
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="type"></span><span id="TYPE"></span>**automáticamente**
</dt> <dd>

Tipo de objeto de filtro. No hay valores predefinidos para este atributo.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obligatorio) 
</dt> <dd>

GUID que identifica de forma única el objeto de filtro de origen. Los métodos del objeto de filtro de origen se invocan para interpretar los elementos de **fragmento** contenidos en el elemento **sourceFilter** .



| Value                                  | Descripción                                              |
|----------------------------------------|----------------------------------------------------------|
| {4202947A-A563-4B05-A754-A1B4B5989849} | El GUID para el filtro de origen "música en mi biblioteca".    |
| {B2D9BDDC-8E49-444B-9BA4-193ABF9C7870} | El GUID para el filtro de origen "vídeo en mi biblioteca".    |
| {CC823400-A8E4-4081-B073-D3B6D952FE69} | El GUID para el filtro de origen "imágenes en mi biblioteca". |
| {E5415A66-7763-4BDE-B97F-5557CA73C303} | El GUID para el filtro de origen "programas de TV en mi biblioteca". |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nombre** (obligatorio) 
</dt> <dd>

Nombre del objeto de filtro.



| Value                  | Descripción                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| Música en mi biblioteca    | Objeto de filtro que selecciona los elementos especificados del conjunto de elementos de música de la biblioteca del usuario. |
| Vídeo en mi biblioteca    | Un objeto de filtro que selecciona los elementos especificados del conjunto de elementos de vídeo en la biblioteca del usuario. |
| Imágenes en mi biblioteca | Un objeto de filtro que selecciona los elementos especificados del conjunto de elementos de fotografía en la biblioteca del usuario. |
| Programas de TV en mi biblioteca | Un objeto de filtro que selecciona los elementos especificados del conjunto de elementos de TV en la biblioteca del usuario.    |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                         |
|-----------|----------------------------------|
| Parent    | [querySet](queryset-element.md) |
| Elemento secundario     | [Fragment](fragment-element.md) |



 

## <a name="remarks"></a>Observaciones

El elemento **sourceFilter** selecciona los elementos de la biblioteca sin tener en cuenta el tamaño del conjunto de resultados. Por otro lado, el elemento **Filter** limita el tamaño del conjunto de resultados.

## <a name="examples"></a>Ejemplos


```
<sourceFilter 
    type = "smartFilterObject" 
    id = "{4202947A-A563-4B05-A754-A1B4B5989849}" 
    name = "Music in my library">
        <fragment name = "Genre">
            <argument name = "condition">Is</argument>
            <argument name = "value">Rock</argument>
        </fragment>
        <fragment name = "Album Artist">
            <argument name = "condition">Is Not</argument>
            <argument name = "value">Brenda Diaz</argument>
        </fragment>
</sourceFilter>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento Filter**](filter-element.md)
</dt> <dt>

[**Elemento Fragment**](fragment-element.md)
</dt> <dt>

[**Elemento querySet**](queryset-element.md)
</dt> <dt>

[**Referencia de elementos de lista de reproducción de Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





