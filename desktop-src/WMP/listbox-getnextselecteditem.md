---
title: LISTBOX.getNextSelectedItem
description: El método getNextSelectedItem recupera el siguiente elemento seleccionado en el control de cuadro de lista a partir del elemento después del que tiene el índice especificado.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- LISTBOX.getNextSelectedItem Reproductor de Windows Media
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f4a5d95880b1300ebfb7f1732e7c20b6975ad82cf2d15514c58e68b9f9c42cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003405"
---
# <a name="listboxgetnextselecteditem"></a>LISTBOX.getNextSelectedItem

El **método getNextSelectedItem** recupera el siguiente elemento seleccionado en el control de cuadro de lista a partir del elemento después del que tiene el índice especificado.

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*Startindex*
</dt> <dd>

**Number** (**long**) que contiene el índice del elemento que precede al elemento que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor Number** (**long**) que contiene el índice del siguiente elemento seleccionado.

## <a name="remarks"></a>Comentarios

Para iniciar la búsqueda desde el principio, use 1 para el índice inicial.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





