---
title: PLAYLIST.sortColumn
description: El método sortColumn ordena los datos de la columna especificada.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- LISTA DE REPRODUCCIÓN.sortColumn Reproductor de Windows Media
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127570101"
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

## <a name="remarks"></a>Observaciones

Este método ordena la columna especificada de la misma manera que los botones de encabezado de columna en el elemento **PLAYLIST.** Si la columna aún no se ha ordenado, se ordena en orden alfanumérico. Si se ha ordenado, se invierte su orden.

Para que este método funcione, **el atributo allowColumnSorting** debe establecerse en true.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media versión 7.0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ELEMENTO PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST.allowColumnSorting**](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





