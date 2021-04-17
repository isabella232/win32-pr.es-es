---
title: EDITBOX. getSelectionEnd
description: El método getSelectionEnd recupera la posición final del texto seleccionado en el control EditBox.
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- GetSelectionEnd Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f27c2974360e7e77becfa67a27b4e96b529ad1e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700410"
---
# <a name="editboxgetselectionend"></a>EDITBOX. getSelectionEnd

El método **getSelectionEnd** recupera la posición final del texto seleccionado en el control EditBox.

``` syntax
        elementID.getSelectionEnd()
```

## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **número** (**Long**).

## <a name="remarks"></a>Observaciones

Si no hay texto seleccionado, este método devuelve la posición del punto de inserción.

Si el control es multilínea, este método devuelve el índice de carácter del control, no el índice de línea.

Solo se puede llamar a este método después de que el control se vuelva visible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX. getSelectionStart**](editbox-getselectionstart.md)
</dt> <dt>

[**EDITBOX. replaceSelection**](editbox-replaceselection.md)
</dt> <dt>

[**EDITBOX. setSelection**](editbox-setselection.md)
</dt> </dl>

 

 





