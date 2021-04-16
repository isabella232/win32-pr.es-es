---
title: Elemento Filter
description: El elemento Filter contiene elementos que limitan el tamaño de una lista de reproducción, la duración de una lista de reproducción o el número de elementos multimedia de una lista de reproducción.
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- filtro de ventanas de elementos Media Player
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32d2d306faebef813996b59575220efeba99dfb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699534"
---
# <a name="filter-element"></a>Elemento Filter

El elemento **Filter** contiene elementos que limitan el tamaño de una lista de reproducción, la duración de una lista de reproducción o el número de elementos multimedia de una lista de reproducción.

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

<span id="type"></span><span id="TYPE"></span>**automáticamente**
</dt> <dd>

Tipo de objeto de filtro. No hay valores predefinidos para este atributo.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obligatorio) 
</dt> <dd>

GUID que identifica de forma única un objeto de filtro. Los métodos del objeto Filter se invocan para interpretar los elementos **Fragment** contenidos en el elemento **Filter** .



| Value                                  | Descripción                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| {BC5E21B0-504C-46F6-82BF-FB975C911AD6} | El identificador del filtro "filtro de lista de reproducción automática de Microsoft--limita las listas de reproducción automáticas por recuento, tamaño o duración". |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nombre** (obligatorio) 
</dt> <dd>

Nombre del objeto de filtro.



| Value                                                                              | Descripción                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| Filtro de lista de reproducción automática de Microsoft: limita las listas de reproducción automáticas por número, tamaño o duración | Limita las listas de reproducción automáticas por número, tamaño o duración. |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                                   |
|-----------|--------------------------------------------|
| Parent    | [smartPlaylist](smartplaylist-element.md) |
| Elemento secundario     | [Fragment](fragment-element.md)           |



 

## <a name="remarks"></a>Observaciones

El elemento **Filter** no agrega elementos multimedia a una lista de reproducción; simplemente quita o filtra el contenido seleccionado por el elemento **sourceFilter** .

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



| Requisito | Value |
|--------------------|----------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Elemento Fragment**](fragment-element.md)
</dt> <dt>

[**Elemento smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Elemento sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Referencia de elementos de lista de reproducción de Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





