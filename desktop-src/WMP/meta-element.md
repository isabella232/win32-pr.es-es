---
title: meta (Elemento)
description: El meta elemento especifica los metadatos que se aplican a toda la lista de reproducción.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- meta Element Reproductor de Windows Media
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f3c41c25a0df0895c645c34f97495712b113ffc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361733"
---
# <a name="meta-element"></a>meta (Elemento)

El **meta** elemento especifica los metadatos que se aplican a toda la lista de reproducción.

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a>Atributos



| Término                                                                       | Descripción                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="name"></span><span id="NAME"></span>**Nombre**<br/>          | Nombre de un elemento de metadatos.<br/>                                                                                       |
| <span id="content"></span><span id="CONTENT"></span>**Contenido**<br/> | Valor de un elemento de metadatos. Por ejemplo, si el atributo name es "Genre", el atributo content podría ser "Rock".<br/> |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                 |
|-----------|--------------------------|
| Parent    | [head](head-element.md) |
| Elemento secundario     | None                     |



 

## <a name="remarks"></a>Observaciones

El creador de una lista Windows multimedia puede establecer el atributo name de un meta elemento en cualquier cadena. En la lista siguiente se muestran algunos atributos de nombre típicos que se encuentran en Windows listas de reproducción multimedia creadas por Reproductor de Windows Media y otros componentes de Microsoft.

-   Autor
-   Category
-   Género
-   UserName
-   UserRating
-   Generator

## <a name="examples"></a>Ejemplos


```
<head>
    <meta name = "Author" content = "Frank Lee"/>
    <meta name = "Category" content = "Classic"/>
    <meta name = "Genre" content = "Rock"/>
</head>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**elemento head**](head-element.md)
</dt> <dt>

[**Windows Referencia de elementos de lista de reproducción multimedia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





