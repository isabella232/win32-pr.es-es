---
title: Lista de reproducción. getNextCheckedItem2
description: El método getNextCheckedItem2 recupera el índice del siguiente elemento activado en la lista de reproducción que sigue al índice especificado.
ms.assetid: 64e51fd1-eb0f-47e5-8684-96824f4f3194
keywords:
- Windows Media Player de lista de reproducción. getNextCheckedItem2
topic_type:
- apiref
api_name:
- PLAYLIST.getNextCheckedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 50bb2fd6ed6e3328df29a59381571204ebd28369
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708232"
---
# <a name="playlistgetnextcheckeditem2"></a>Lista de reproducción. getNextCheckedItem2

El método **getNextCheckedItem2** recupera el índice del siguiente elemento activado en la lista de reproducción que sigue al índice especificado.

``` syntax
        elementID.getNextCheckedItem2(item)
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

Este método puede trabajar con listas de reproducción anidadas y reemplaza al método **getNextCheckedItem** , que no puede. Pase 1 en el parámetro *Item* para buscar el primer elemento activado. Cuando no hay más elementos marcados, este método devuelve 1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Lista de reproducción. getNextCheckedItem**](playlist-getnextcheckeditem.md)
</dt> </dl>

 

 





