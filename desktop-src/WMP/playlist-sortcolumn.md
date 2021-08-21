---
title: PLAYLIST.sortColumn
description: El método sortColumn ordena los datos de la columna especificada.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- PLAYLIST.sortColumn Reproductor de Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34dfce7306ceb39d64665538a21dbaef965ea799141a2756c2fea5bbe23ea9cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335667"
---
# <a name="playlistsortcolumn"></a>PLAYLIST.sortColumn

El **método sortColumn** ordena los datos de la columna especificada.

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*Columna*
</dt> <dd>

**Number** (**long**) que indica el índice de la columna que se debe ordenar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Este método ordena la columna especificada de la misma manera que los botones de encabezado de columna en el elemento **PLAYLIST.** Si la columna aún no se ha ordenado, se ordena en orden alfanumérico. Si se ha ordenado, se invierte su orden.

Para que este método funcione, **el atributo allowColumnSorting** debe establecerse en true.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.allowColumnSorting**](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





