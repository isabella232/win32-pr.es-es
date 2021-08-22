---
title: EDITBOX.setSelection
description: El método setSelection selecciona el texto del control de cuadro de edición del índice inicial especificado al índice final especificado.
ms.assetid: 97b20a17-4b9c-4144-b448-8d7611c0e994
keywords:
- EDITBOX.setSelection Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.setSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b4ed2bc9ca861bcf38c2b9aecc4969c80b14ba56d87ad2250dd53ed8c7a6655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118838723"
---
# <a name="editboxsetselection"></a>EDITBOX.setSelection

El **método setSelection** selecciona el texto del control de cuadro de edición del índice inicial especificado al índice final especificado.

``` syntax
        elementID.setSelection(start, end)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="start"></span><span id="START"></span>*Empezar*
</dt> <dd>

**Number** (**long**) que contiene el índice de caracteres de la posición inicial del texto seleccionado.

</dd> <dt>

<span id="end"></span><span id="END"></span>*Final*
</dt> <dd>

**Number** (**long**) que contiene el índice de caracteres de la posición final del texto seleccionado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si el inicio es 0 y el final es 1, se selecciona todo el texto del control de cuadro de edición. Si el inicio es 1, se deselecciona cualquier selección actual.

Solo se puede llamar a este método después de que el control se vuelva visible.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX.getSelectionEnd**](editbox-getselectionend.md)
</dt> <dt>

[**EDITBOX.getSelectionStart**](editbox-getselectionstart.md)
</dt> <dt>

[**EDITBOX.replaceSelection**](editbox-replaceselection.md)
</dt> </dl>

 

 





