---
title: elemento title (WPL)
description: El elemento title especifica un título para la lista de reproducción.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- elemento title (WPL) Reproductor de Windows Media
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5649553ab51a43bd1fb0aeb78d505d7e922bf80b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127465844"
---
# <a name="title-element-wpl"></a>elemento title (WPL)

El **elemento title** especifica un título para la lista de reproducción.

``` syntax
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```

## <a name="attributes"></a>Atributos

Este elemento no tiene atributos.

## <a name="parentchild-elements"></a>Elementos primarios y secundarios



| Hierarchy | Elementos                 |
|-----------|--------------------------|
| Parent    | [head](head-element.md) |
| Elemento secundario     | None                     |



 

## <a name="remarks"></a>Observaciones

Al elegir un título para una lista de reproducción Windows multimedia (WPL), tenga en cuenta que el contenido de la lista de reproducción puede ser dinámico. Un buen enfoque es basar el  título en la lógica de los elementos de argumento porque esto es lo que define el contenido de la lista de reproducción. Algunos ejemplos de esto son "My Favorite Rock Songs from 1966" (Mis canciones favoritas de rock de 1966) o "Dance Songs That I Haven't Played Recently".

## <a name="examples"></a>Ejemplos


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media serie 9 o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**elemento argument**](argument-element.md)
</dt> <dt>

[**elemento head**](head-element.md)
</dt> <dt>

[**Windows Referencia de elementos de lista de reproducción multimedia**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





