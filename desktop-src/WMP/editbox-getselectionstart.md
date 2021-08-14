---
title: EDITBOX.getSelectionStart
description: El método getSelectionStart recupera la posición inicial del texto seleccionado en el control de cuadro de edición.
ms.assetid: 2d7efe14-549c-4f73-96a7-b8ce88b881ad
keywords:
- EDITBOX.getSelectionStart Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionStart
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c555cc7231440e15275dcd44a2508f1d8cc5ba53a8137db861cc71b61528ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340036"
---
# <a name="editboxgetselectionstart"></a>EDITBOX.getSelectionStart

El **método getSelectionStart** recupera la posición inicial del texto seleccionado en el control de cuadro de edición.

``` syntax
        elementID.getSelectionStart()
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

[**EDITBOX.getSelectionEnd**](editbox-getselectionend.md)
</dt> <dt>

[**EDITBOX.replaceSelection**](editbox-replaceselection.md)
</dt> <dt>

[**EDITBOX.setSelection**](editbox-setselection.md)
</dt> </dl>

 

 





