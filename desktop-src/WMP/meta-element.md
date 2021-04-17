---
title: Elemento meta
description: El elemento meta especifica metadatos que se aplican a toda la lista de reproducción.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- Media Player del elemento meta de Windows
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653544"
---
# <a name="meta-element"></a>Elemento meta

El elemento **meta** especifica metadatos que se aplican a toda la lista de reproducción.

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a>Atributos



| Término                                                                       | Descripción                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="name"></span><span id="NAME"></span>**Name**<br/>          | Nombre de un elemento de metadatos.<br/>                                                                                       |
| <span id="content"></span><span id="CONTENT"></span>**Content**<br/> | Valor de un elemento de metadatos. Por ejemplo, si el atributo de nombre es "género", el atributo de contenido podría ser "Rock".<br/> |



 

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                 |
|-----------|--------------------------|
| Parent    | [head](head-element.md) |
| Elemento secundario     | None                     |



 

## <a name="remarks"></a>Observaciones

El creador de una lista de reproducción de Windows Media puede establecer el atributo de nombre de un elemento meta en cualquier cadena. La lista siguiente muestra algunos atributos de nombre típicos que se encuentran en las listas de reproducción de Windows Media creadas por Windows Media Player y otros componentes de Microsoft.

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
| Versión<br/> | Windows Media Player 9 series o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento de encabezado**](head-element.md)
</dt> <dt>

[**Referencia de elementos de lista de reproducción de Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





