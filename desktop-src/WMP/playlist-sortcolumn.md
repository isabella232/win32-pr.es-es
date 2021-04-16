---
title: Lista de reproducción. sortColumn
description: El método sortColumn ordena los datos de la columna especificada.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- Media Player de listas de reproducción. sortColumn de Windows
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f21f0032ee4db4c7af46b5dda814bb11db551330
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105719019"
---
# <a name="playlistsortcolumn"></a>Lista de reproducción. sortColumn

El método **sortColumn** ordena los datos de la columna especificada.

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*artículo*
</dt> <dd>

**Número** (**largo**) que indica el índice de la columna que se va a ordenar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método ordena la columna especificada de la misma manera que los botones de encabezado de columna del elemento de **lista de reproducción** . Si la columna no se ha ordenado todavía, se ordena en orden alfanumérico. Si se ha ordenado, se invierte su orden.

Para que este método funcione, el atributo **allowColumnSorting** debe establecerse en true.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Lista de reproducción. allowColumnSorting**](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





