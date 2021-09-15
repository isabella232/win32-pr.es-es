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
ms.openlocfilehash: 8afb3df1f1b6a6adc528e02dd6531ac4fc1a9a3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127474569"
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

**Number** (**long**) que contiene el índice del elemento que precede al elemento que se recupera.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un **valor Number** (**long**) que contiene el índice del siguiente elemento seleccionado.

## <a name="remarks"></a>Observaciones

Para iniciar la búsqueda desde el principio, use 1 para el índice de inicio.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------|
| Versión<br/> | Reproductor de Windows Media para Windows XP o posterior<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





