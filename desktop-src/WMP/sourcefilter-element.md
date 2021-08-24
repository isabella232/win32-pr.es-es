---
title: elemento sourceFilter
description: El elemento sourceFilter contiene elementos que seleccionan elementos de una biblioteca.
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- SourceFilter Element Reproductor de Windows Media
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14294f227e5ebe29e422d60a95734f7b93207880ea82ef9fb70ed3f7cf6dac4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763275"
---
# <a name="sourcefilter-element"></a>elemento sourceFilter

El **elemento sourceFilter** contiene elementos que seleccionan elementos de una biblioteca.

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

<span id="type"></span><span id="TYPE"></span>**Tipo**
</dt> <dd>

Tipo de objeto de filtro. No hay valores predefinidos para este atributo.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (obligatorio) 
</dt> <dd>

GUID que identifica de forma única el objeto de filtro de origen. Los métodos del objeto de filtro de origen se invocan para interpretar los elementos **de** fragmento contenidos en el **elemento sourceFilter.**



| Value                                  | Descripción                                              |
|----------------------------------------|----------------------------------------------------------|
| {4202947A-A563-4B05-A754-A1B4B5989849} | Guid del filtro de origen "Música en mi biblioteca".    |
| {B2D9BDDC-8E49-444B-9BA4-193ABF9C7870} | GUID del filtro de origen "Vídeo en mi biblioteca".    |
| {CC823400-A8E4-4081-B073-D3B6D952FE69} | GUID del filtro de origen "Imágenes en mi biblioteca". |
| {E5415A66-7763-4BDE-B97F-5557CA73C303} | Guid del filtro de origen "Tv shows in my library". |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (obligatorio) 
</dt> <dd>

Nombre del objeto de filtro.



| Value                  | Descripción                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| Música en mi biblioteca    | Objeto de filtro que selecciona los elementos especificados del conjunto de elementos de música de la biblioteca del usuario. |
| Vídeo en mi biblioteca    | Objeto de filtro que selecciona los elementos especificados del conjunto de elementos de vídeo de la biblioteca del usuario. |
| Imágenes de mi biblioteca | Objeto de filtro que selecciona los elementos especificados del conjunto de elementos de foto de la biblioteca del usuario. |
| Programas de TV en mi biblioteca | Objeto de filtro que selecciona los elementos especificados del conjunto de elementos de TV de la biblioteca del usuario.    |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                         |
|-----------|----------------------------------|
| Parent    | [querySet](queryset-element.md) |
| Elemento secundario     | [Fragmento](fragment-element.md) |



 

## <a name="remarks"></a>Comentarios

El **elemento sourceFilter** selecciona elementos de la biblioteca sin tener en cuenta el tamaño del conjunto de resultados. Por **otro** lado, el elemento filter limita el tamaño del conjunto de resultados.

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
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**elemento filter**](filter-element.md)
</dt> <dt>

[**elemento fragment**](fragment-element.md)
</dt> <dt>

[**elemento querySet**](queryset-element.md)
</dt> <dt>

[**Windows Referencia de elementos de lista de reproducción multimedia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





