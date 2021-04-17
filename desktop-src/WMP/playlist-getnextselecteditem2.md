---
title: Lista de reproducción. getNextSelectedItem2
description: El método getNextSelectedItem2 recupera el índice del siguiente elemento seleccionado en la lista de reproducción después del índice especificado.
ms.assetid: 18acf95c-ab79-4b5c-b904-e13ef9a034dc
keywords:
- Windows Media Player de lista de reproducción. getNextSelectedItem2
topic_type:
- apiref
api_name:
- PLAYLIST.getNextSelectedItem2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27d166887bb2fa98e184e1f64f4aaceb89930d00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708227"
---
# <a name="playlistgetnextselecteditem2"></a>Lista de reproducción. getNextSelectedItem2

El método **getNextSelectedItem2** recupera el índice del siguiente elemento seleccionado en la lista de reproducción después del índice especificado.

``` syntax
        elementID.getNextSelectedItem2(item)
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

Este método puede trabajar con listas de reproducción anidadas y reemplaza al método **getNextSelectedItem** , que no puede. Pase 1 en el parámetro *Item* para buscar el primer elemento seleccionado. Cuando no hay ningún elemento seleccionado, se devuelve-1.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**Lista de reproducción. getNextSelectedItem**](playlist-getnextselecteditem.md)
</dt> </dl>

 

 





