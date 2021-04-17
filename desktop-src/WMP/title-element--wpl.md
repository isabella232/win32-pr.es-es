---
title: Elemento title (WPL)
description: El elemento title especifica un título para la lista de reproducción.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- Elemento title (WPL) Windows Media Player
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708922"
---
# <a name="title-element-wpl"></a>Elemento title (WPL)

El elemento **title** especifica un título para la lista de reproducción.

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

Al elegir un título para una lista de reproducción de Windows Media (WPL), tenga en cuenta que el contenido de la lista de reproducción puede ser dinámico. Un buen enfoque consiste en basar el título en la lógica de los elementos de **argumento** , ya que es lo que define el contenido de la lista de reproducción. Ejemplos de esto son "mis canciones de rock favoritas de 1966" o "las canciones de baile que no he reproducido recientemente".

## <a name="examples"></a>Ejemplos


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|----------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior.<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento argument**](argument-element.md)
</dt> <dt>

[**Elemento de encabezado**](head-element.md)
</dt> <dt>

[**Referencia de elementos de lista de reproducción de Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





