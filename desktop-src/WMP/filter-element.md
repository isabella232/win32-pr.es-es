---
title: elemento filter
description: El elemento filter contiene elementos que limitan el tamaño de una lista de reproducción, la duración de una lista de reproducción o el número de elementos multimedia de una lista de reproducción.
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- Filter Element Reproductor de Windows Media
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a059a6a2820d99541076775ac869de0767ffd739743f5b145a155efd0a25abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576782"
---
# <a name="filter-element"></a>elemento filter

El **elemento filter** contiene elementos que limitan el tamaño de una lista de reproducción, la duración de una lista de reproducción o el número de elementos multimedia de una lista de reproducción.

``` syntax
<filter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</filter>
            
```

## <a name="attributes"></a>Atributos

<dl> <dt>

<span id="type"></span><span id="TYPE"></span>**Tipo**
</dt> <dd>

Tipo de objeto de filtro. No hay valores predefinidos para este atributo.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (obligatorio) 
</dt> <dd>

GUID que identifica de forma única un objeto de filtro. Los métodos del objeto de filtro se invocan para interpretar los elementos **de fragmento** contenidos en el **elemento de** filtro.



| Valor                                  | Descripción                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| {BC5E21B0-504C-46F6-82BF-FB975C911AD6} | Identificador del filtro "Filtro de lista de reproducción automática de Microsoft: limita las listas de reproducción automáticas por recuento, tamaño o duración". |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (obligatorio) 
</dt> <dd>

Nombre del objeto de filtro.



| Valor                                                                              | Descripción                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| Filtro de lista de reproducción automática de Microsoft: limita las listas de reproducción automáticas por recuento, tamaño o duración | Limita las listas de reproducción automáticas por recuento, tamaño o duración. |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                                   |
|-----------|--------------------------------------------|
| Parent    | [smartPlaylist](smartplaylist-element.md) |
| Elemento secundario     | [Fragmento](fragment-element.md)           |



 

## <a name="remarks"></a>Comentarios

El **elemento filter** no agrega ningún elemento multimedia a una lista de reproducción; simplemente quita o filtra el contenido seleccionado por el **elemento sourceFilter.**

## <a name="examples"></a>Ejemplos


```XML
<filter 
    type = "smartFilterObject" 
    id = "{BC5E21B0-504C-46F6-82BF-FB975C911AD6}" 
    name = "Microsoft Auto Playlist Filter -- Limits auto playlists by count,size or duration">
        <fragment name = "Limit Number of Items">
            <argument name = "number">25</argument>
        </fragment>
</filter>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**elemento argument**](argument-element.md)
</dt> <dt>

[**elemento fragment**](fragment-element.md)
</dt> <dt>

[**elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**elemento sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Windows Referencia de elementos de lista de reproducción multimedia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





