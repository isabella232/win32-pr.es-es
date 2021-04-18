---
title: EDITBOX. getLineFromChar
description: El método getLineFromChar recupera el índice de línea para el índice de carácter especificado.
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- GetLineFromChar Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3462ce628da72ca1e55df79e408fc79e0ec8b63a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700411"
---
# <a name="editboxgetlinefromchar"></a>EDITBOX. getLineFromChar

El método **getLineFromChar** recupera el índice de línea para el índice de carácter especificado.

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*ajustar*
</dt> <dd>

**Número** (**largo**) que contiene el índice del carácter cuyo índice de línea se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **número** (**Long**).

## <a name="remarks"></a>Observaciones

Si la posición de carácter especificada es 1, este método recupera el índice de línea de la línea actual.

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

[**EDITBOX. getLineIndex**](editbox-getlineindex.md)
</dt> </dl>

 

 





