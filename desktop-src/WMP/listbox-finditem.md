---
title: LISTBOX. findItem
description: El método findItem busca una cadena determinada empezando por el elemento que sigue al índice de elemento especificado.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- Media Player de Windows de LISTBOX. findItem
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161f4dd8b93fe4fed6a794dffde3e58e840c74e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699646"
---
# <a name="listboxfinditem"></a>LISTBOX. findItem

El método **findItem** busca una cadena determinada empezando por el elemento que sigue al índice de elemento especificado.

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*Super*
</dt> <dd>

**Número** (**largo**) que contiene el índice del elemento en el que se va a iniciar la búsqueda.

</dd> <dt>

<span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*
</dt> <dd>

**Cadena** que contiene el texto que se va a buscar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **número** (**Long**) que contiene el índice del elemento que contiene la cadena.

## <a name="remarks"></a>Observaciones

Para iniciar la búsqueda en la primera línea del control de cuadro de lista, use 1 como *startIndex*. Para continuar buscando texto después de encontrar la primera línea, use el índice de línea devuelto como *startIndex* y la búsqueda se iniciará en la línea siguiente. Este método buscará subcadenas y no distingue entre mayúsculas y minúsculas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





