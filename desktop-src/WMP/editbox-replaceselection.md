---
title: EDITBOX.replaceSelection
description: El método replaceSelection reemplaza la selección actual por el texto especificado.
ms.assetid: 600650fb-f0c8-489a-9bf2-04f31705c6b0
keywords:
- EDITBOX.replaceSelection Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.replaceSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 296a78bd4fbe112cbe6b0fb859c6451b6a3a892cb42ca8e91e2b4fcf911d4c20
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935287"
---
# <a name="editboxreplaceselection"></a>EDITBOX.replaceSelection

El **método replaceSelection** reemplaza la selección actual por el texto especificado.

``` syntax
        elementID.replaceSelection(newValue)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*
</dt> <dd>

**Cadena** que contiene el texto para reemplazar el texto seleccionado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si no hay texto seleccionado, el texto de reemplazo se inserta en la ubicación actual del punto de inserción.

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

[**EDITBOX.setSelection**](editbox-setselection.md)
</dt> </dl>

 

 





