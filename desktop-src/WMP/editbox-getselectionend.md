---
title: EDITBOX.getSelectionEnd
description: El método getSelectionEnd recupera la posición final del texto seleccionado en el control de cuadro de edición.
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- EDITBOX.getSelectionEnd Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8dff56bda802286ed76ba3b448478dfa57d005c13baf229612e190bbf163b25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118838849"
---
# <a name="editboxgetselectionend"></a>EDITBOX.getSelectionEnd

El **método getSelectionEnd** recupera la posición final del texto seleccionado en el control de cuadro de edición.

``` syntax
        elementID.getSelectionEnd()
```

## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor Number** (**long**).

## <a name="remarks"></a>Comentarios

Si no se selecciona ningún texto, este método devuelve la posición del punto de inserción.

Si el control es multilínea, este método devuelve el índice de caracteres del control, no el índice de línea.

Solo se puede llamar a este método después de que el control se vuelva visible.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX.getSelectionStart**](editbox-getselectionstart.md)
</dt> <dt>

[**EDITBOX.replaceSelection**](editbox-replaceselection.md)
</dt> <dt>

[**EDITBOX.setSelection**](editbox-setselection.md)
</dt> </dl>

 

 





