---
title: EDITBOX. replaceSelection
description: El método replaceSelection reemplaza la selección actual por el texto especificado.
ms.assetid: 600650fb-f0c8-489a-9bf2-04f31705c6b0
keywords:
- EDITBOX. replaceSelection Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.replaceSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6546f24c864d0b466acd17d9a42616c3f8ab01b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699391"
---
# <a name="editboxreplaceselection"></a>EDITBOX. replaceSelection

El método **replaceSelection** reemplaza la selección actual por el texto especificado.

``` syntax
        elementID.replaceSelection(newValue)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*Nuevovalor*
</dt> <dd>

**Cadena** que contiene el texto en el que se va a reemplazar el texto seleccionado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si no hay texto seleccionado, el texto de sustitución se inserta en la ubicación actual del punto de inserción.

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

[**EDITBOX. setSelection**](editbox-setselection.md)
</dt> </dl>

 

 





