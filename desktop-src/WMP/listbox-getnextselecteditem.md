---
title: LISTBOX. getNextSelectedItem
description: El método getNextSelectedItem recupera el siguiente elemento seleccionado en el control de cuadro de lista a partir del elemento situado después del objeto con el índice especificado.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- LISTBOX. getNextSelectedItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8afb3df1f1b6a6adc528e02dd6531ac4fc1a9a3e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699632"
---
# <a name="listboxgetnextselecteditem"></a>LISTBOX. getNextSelectedItem

El método **getNextSelectedItem** recupera el siguiente elemento seleccionado en el control de cuadro de lista a partir del elemento situado después del objeto con el índice especificado.

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a>Parámetros

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*Super*
</dt> <dd>

**Número** (**largo**) que contiene el índice del elemento que precede al elemento que se va a recuperar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **número** (**largo**) que contiene el índice del siguiente elemento seleccionado.

## <a name="remarks"></a>Observaciones

Para iniciar la búsqueda desde el principio, use 1 para el índice de inicio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Windows Media Player para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





