---
title: LVM_SORTITEMSEX mensaje (Commctrl.h)
description: Usa una función de comparación definida por la aplicación para ordenar los elementos de un control de vista de lista. El índice de cada elemento cambia para reflejar la nueva secuencia. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView SortItemsEx.
ms.assetid: eab2f6f5-68fd-4cb6-acf4-cb267ee40fdc
keywords:
- LVM_SORTITEMSEX controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SORTITEMSEX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef492ff11980e764b33942f54c0732a64e799a94dde0e3d872ef0cb7bfb66c0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170371"
---
# <a name="lvm_sortitemsex-message"></a>Mensaje \_ LVM SORTITEMSEX

Usa una función de comparación definida por la aplicación para ordenar los elementos de un control de vista de lista. El índice de cada elemento cambia para reflejar la nueva secuencia. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView SortItemsEx.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sortitemsex)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor definido por la aplicación que se pasa a la función de comparación.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una función de comparación definida por la aplicación. Se llama durante la operación de ordenación cada vez que es necesario comparar el orden relativo de dos elementos de lista.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** en caso contrario.

## <a name="remarks"></a>Comentarios

La función de comparación tiene el formato siguiente:

``` syntax
int CALLBACK CompareFunc(LPARAM lParam1, LPARAM lParam2, LPARAM lParamSort);  
```

Este mensaje es similar a [**LVM \_ SORTITEMS,**](lvm-sortitems.md)excepto el tipo de información que se pasa a la función de comparación. Con **LVM \_ SORTITEMSEX,** *lParam1* es el índice actual del primer elemento y *lParam2* es el índice actual del segundo elemento. Puede enviar un mensaje [**\_ GETITEMTEXT de LVM**](lvm-getitemtext.md) para recuperar más información sobre un elemento, si es necesario.

La función de comparación debe devolver un valor negativo si el primer elemento debe preceder al segundo, un valor positivo si el primer elemento debe seguir al segundo o cero si los dos elementos son equivalentes.

> [!Note]  
> Durante el proceso de ordenación, el contenido de la vista de lista es inestable. Si la función de devolución de llamada envía mensajes al control list-view aparte de [**LVM \_ GETITEM**](lvm-getitem.md) [**(ListView \_ GetItem),**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitem)los resultados son impredecibles.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





