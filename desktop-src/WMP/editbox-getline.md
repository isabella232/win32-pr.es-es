---
title: EDITBOX.getLine
description: El método getLine recupera el texto de la línea con el índice especificado.
ms.assetid: a692c32b-86b9-419e-a3a5-464687be04da
keywords:
- EDITBOX.getLine Reproductor de Windows Media
topic_type:
- apiref
api_name:
- EDITBOX.getLine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3b0b9a15f9eff8c2612e7a242a205c1d9411a60c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127241034"
---
# <a name="editboxgetline"></a>EDITBOX.getLine

El **método getLine** recupera el texto de la línea con el índice especificado.

``` syntax
        elementID.getLine(index)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Índice*
</dt> <dd>

**Number** (**long**) que contiene el índice de la línea que se recuperará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve una **cadena**.

## <a name="remarks"></a>Observaciones

Si el índice no es válido, se devuelve una cadena vacía. Solo se puede llamar a este método después de que el control se vuelva visible.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX.getLineFromChar**](editbox-getlinefromchar.md)
</dt> <dt>

[**EDITBOX.getLineIndex**](editbox-getlineindex.md)
</dt> </dl>

 

 





