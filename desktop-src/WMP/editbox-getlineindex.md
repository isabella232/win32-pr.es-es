---
title: EDITBOX. getLineIndex
description: El método getLineIndex recupera el índice de carácter del primer carácter de la línea con el índice de línea especificado.
ms.assetid: 1298227a-d839-44fc-bacb-44c3c968bd94
keywords:
- GetLineIndex Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5f55027bb7d577b7080ad2f006a5a006e718c2d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700412"
---
# <a name="editboxgetlineindex"></a>EDITBOX. getLineIndex

El método **getLineIndex** recupera el índice de carácter del primer carácter de la línea con el índice de línea especificado.

``` syntax
        elementID.getLineIndex(index)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*ajustar*
</dt> <dd>

**Número** (**largo**) que contiene el índice de la línea cuyo índice de caracteres se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **número** (**Long**).

## <a name="remarks"></a>Observaciones

Si el índice de línea especificado es 1, se usa la línea que contiene el punto de inserción.

Solo se puede llamar a este método después de que el control se vuelva visible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX. getLine**](editbox-getline.md)
</dt> <dt>

[**EDITBOX. getLineFromChar**](editbox-getlinefromchar.md)
</dt> </dl>

 

 





