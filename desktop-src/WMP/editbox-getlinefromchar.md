---
title: EDITBOX.getLineFromChar
description: El método getLineFromChar recupera el índice de línea para el índice de caracteres especificado.
ms.assetid: c3a29bdf-ff63-4b6d-90e8-d414dde87f85
keywords:
- EDITBOX.getLineFromChar Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.getLineFromChar
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 110030c3c756a91c993857cef125c51669f71eb9a358eb7261205fde0b0ad4a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749311"
---
# <a name="editboxgetlinefromchar"></a>EDITBOX.getLineFromChar

El **método getLineFromChar** recupera el índice de línea para el índice de caracteres especificado.

``` syntax
        elementID.getLineFromChar(index)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Índice*
</dt> <dd>

**Number** (**long**) que contiene el índice del carácter cuyo índice de línea se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor Number** (**long**).

## <a name="remarks"></a>Comentarios

Si la posición de carácter especificada es 1, este método recupera el índice de línea de la línea actual.

Solo se puede llamar a este método después de que el control se vuelva visible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX.getLine**](editbox-getline.md)
</dt> <dt>

[**EDITBOX.getLineIndex**](editbox-getlineindex.md)
</dt> </dl>

 

 





