---
title: LISTBOX.insertItem
description: El método insertItem inserta el texto especificado en el índice especificado en el control de cuadro de lista.
ms.assetid: c45eb75e-074d-4f3f-bfdd-6c3cbbd71f54
keywords:
- ListBOX.insertItem Reproductor de Windows Media
topic_type:
- apiref
api_name:
- LISTBOX.insertItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0344bbc9fbe4f8f2b680866f70c0fe16398ad08cbf4a916c454223fdff04614e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135308"
---
# <a name="listboxinsertitem"></a>LISTBOX.insertItem

El **método insertItem** inserta el texto especificado en el índice especificado en el control de cuadro de lista.

``` syntax
        elementID.insertItem(index, text)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Índice*
</dt> <dd>

**Number** (**long**) que contiene el índice de la línea que se recuperará.

</dd> <dt>

<span id="text"></span><span id="TEXT"></span>*Texto*
</dt> <dd>

**Cadena** que contiene el texto que se va a insertar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cuando se inserta una línea, los índices de línea de las líneas debajo de la línea insertada aumentan en uno.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





