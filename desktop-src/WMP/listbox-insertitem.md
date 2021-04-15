---
title: LISTBOX. insertItem
description: El método insertItem inserta el texto especificado en el índice especificado del control de cuadro de lista.
ms.assetid: c45eb75e-074d-4f3f-bfdd-6c3cbbd71f54
keywords:
- LISTBOX. insertItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.insertItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3600b40ca164c71bd62c0a9a368516d6ad0e1edd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708854"
---
# <a name="listboxinsertitem"></a>LISTBOX. insertItem

El método **insertItem** inserta el texto especificado en el índice especificado del control de cuadro de lista.

``` syntax
        elementID.insertItem(index, text)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*ajustar*
</dt> <dd>

**Número** (**largo**) que contiene el índice de la línea que se va a recuperar.

</dd> <dt>

<span id="text"></span><span id="TEXT"></span>*negrita*
</dt> <dd>

**Cadena** que contiene el texto que se va a insertar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando se inserta una línea, los índices de línea de las líneas situadas debajo de la línea insertada aumentan en uno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





