---
title: LVM_INSERTITEM mensaje (Commctrl.h)
description: Inserta un nuevo elemento en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro \_ ListView InsertItem.
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- LVM_INSERTITEM controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_INSERTITEM
- LVM_INSERTITEMA
- LVM_INSERTITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9408a8d09adca2a097281b13e56241c66a68521dcef0892502d7f8d0e14d25e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575715"
---
# <a name="lvm_insertitem-message"></a>Mensaje \_ INSERTITEM de LVM

Inserta un nuevo elemento en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ ListView InsertItem.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una [**estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que especifica los atributos del elemento de vista de lista. Use el **miembro iItem** para especificar el índice de base cero en el que se debe insertar el nuevo elemento. Si este valor es mayor que el número de elementos contenidos actualmente en la vista de lista, el nuevo elemento se anexará al final de la lista y se le asignará el índice correcto. Examine el valor devuelto del mensaje para determinar el índice real asignado al elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del nuevo elemento si se realiza correctamente o -1 en caso contrario.

## <a name="remarks"></a>Comentarios

No puede usar [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) **ni LVM \_ INSERTITEM para** insertar subelementos. El **miembro iSubItem** de la [**estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) debe ser cero. Consulte [**LVM \_ SETITEM para**](lvm-setitem.md) obtener información sobre cómo establecer subelementos.

Si un control de vista de lista tiene el estilo [**LVS \_ EX \_ CHECKBOXES**](extended-list-view-styles.md) establecido,  se omitirá cualquier valor situado en los bits 12 a 15 del miembro de estado de la estructura [**LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema) Cuando se agrega un elemento con este conjunto de estilos, siempre se establecerá en el estado desactivado.

Si un control de vista de lista tiene el estilo de ventana [**LVS \_ SORTASCENDING**](list-view-window-styles.md) o [**LVS \_ SORTDESCENDING,**](list-view-window-styles.md) se producirá un error en un mensaje **\_ INSERTITEM** de LVM si intenta insertar un elemento que tenga LPSTR TEXTCALLBACK como valor para su \_ miembro **pszText.**

El **mensaje LVM \_ INSERTITEM** insertará el nuevo elemento en la posición adecuada en el criterio de ordenación si se cumplen las condiciones siguientes:

-   Está usando uno de los estilos LVS \_ SORTXXX.
-   No usa el estilo [**LVS \_ OWNERDRAW.**](list-view-window-styles.md)
-   El **miembro pszText** de la estructura a la que apunta **pitem** no se establece en LPSTR \_ TEXTCALLBACK.

Si la [**estructura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) no contiene LVIF GROUPID en el miembro mask, el valor del miembro \_ **iGroupId** es I  \_ GROUPIDCALLBACK de forma predeterminada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ INSERTITEMW** (Unicode) y **LVM \_ INSERTITEMA** (ANSI)<br/>             |



 

 





