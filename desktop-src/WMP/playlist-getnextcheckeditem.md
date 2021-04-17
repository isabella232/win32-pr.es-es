---
title: Lista de reproducción. getNextCheckedItem
description: El método getNextCheckedItem recupera el índice del siguiente elemento activado en la lista de reproducción que sigue al índice especificado.
ms.assetid: 474a497d-5efe-4c95-8eb5-2ba71bd29057
keywords:
- Windows Media Player de lista de reproducción. getNextCheckedItem
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1b4a85fdccc5de227ab8aea3d0ee4f93d46eed50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708233"
---
# <a name="playlistgetnextcheckeditem"></a>Lista de reproducción. getNextCheckedItem

El método **getNextCheckedItem** recupera el índice del siguiente elemento activado en la lista de reproducción que sigue al índice especificado.

``` syntax
        elementID.getNextCheckedItem(item)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="item"></span><span id="ITEM"></span>*movs*
</dt> <dd>

**Número** (**largo**) que indica el índice del elemento que se va a buscar después de.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **número** (**Long**).

## <a name="remarks"></a>Observaciones

Cuando no hay más elementos marcados, este método devuelve 1.

Este método se ha reemplazado por **getNextCheckedItem2**, que admite listas de reproducción anidadas.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------|
| Versión<br/> | Windows Media Player versión 7,0 o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Lista de reproducción. getNextCheckedItem2**](playlist-getnextcheckeditem2.md)
</dt> </dl>

 

 





