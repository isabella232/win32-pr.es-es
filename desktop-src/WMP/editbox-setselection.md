---
title: EDITBOX. setSelection
description: El método setSelection selecciona el texto del control de cuadro de edición desde el índice de inicio especificado hasta el índice final especificado.
ms.assetid: 97b20a17-4b9c-4144-b448-8d7611c0e994
keywords:
- SetSelection Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.setSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d7077de0ea59940c4afa551d22188d5583d0e4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699390"
---
# <a name="editboxsetselection"></a>EDITBOX. setSelection

El método **setSelection** selecciona el texto del control de cuadro de edición desde el índice de inicio especificado hasta el índice final especificado.

``` syntax
        elementID.setSelection(start, end)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="start"></span><span id="START"></span>*iniciales*
</dt> <dd>

**Número** (**largo**) que contiene el índice de carácter de la posición inicial del texto seleccionado.

</dd> <dt>

<span id="end"></span><span id="END"></span>*extremo*
</dt> <dd>

**Número** (**largo**) que contiene el índice de carácter de la posición final del texto seleccionado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si el inicio es 0 y el final es 1, se selecciona todo el texto del control cuadro de edición. Si el inicio es 1, se anula la selección de cualquier selección actual.

Solo se puede llamar a este método después de que el control se vuelva visible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX. getSelectionEnd**](editbox-getselectionend.md)
</dt> <dt>

[**EDITBOX. getSelectionStart**](editbox-getselectionstart.md)
</dt> <dt>

[**EDITBOX. replaceSelection**](editbox-replaceselection.md)
</dt> </dl>

 

 





