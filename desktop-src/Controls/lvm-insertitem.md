---
title: Mensaje de LVM_INSERTITEM (commctrl. h)
description: Inserta un nuevo elemento en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro InsertItem de ListView.
ms.assetid: ac283e81-5b9f-4a90-acdb-fd7813c9cb84
keywords:
- LVM_INSERTITEM controles de mensajes de Windows
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
ms.openlocfilehash: 467c6b595e307dc16f87e40da858ff8b120fb3f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105658331"
---
# <a name="lvm_insertitem-message"></a>\_Mensaje INSERTITEM de LVM

Inserta un nuevo elemento en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ InsertItem de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que especifica los atributos del elemento de vista de lista. Use el miembro **iItem** para especificar el índice basado en cero en el que se debe insertar el nuevo elemento. Si este valor es mayor que el número de elementos que contiene ListView actualmente, el nuevo elemento se anexará al final de la lista y se le asignará el índice correcto. Examine el valor devuelto del mensaje para determinar el índice real asignado al elemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice del nuevo elemento si se realiza correctamente, o-1 en caso contrario.

## <a name="remarks"></a>Observaciones

No se puede usar [**ListView \_ InsertItem**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertitem) o **LVM \_ InsertItem** para insertar subelementos. El miembro **iSubItem** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) debe ser cero. Vea [**LVM \_ SETITEM**](lvm-setitem.md) para obtener información sobre la configuración de subelementos.

Si un control de vista de lista tiene establecido el estilo [**\_ \_ casillas de LVS ex**](extended-list-view-styles.md) , se omitirá cualquier valor colocado en los bits 12 a 15 del miembro **State** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) . Cuando se agrega un elemento con este conjunto de estilos, siempre se establecerá en el estado desactivado.

Si un control de vista de lista tiene el estilo de ventana [**LVS \_ SORTASCENDING**](list-view-window-styles.md) o [**LVS \_ SORTDESCENDING**](list-view-window-styles.md) , se producirá un error en un mensaje **\_ INSERTITEM de LVM** si intenta insertar un elemento que tenga LPSTR \_ TEXTCALLBACK como valor para su miembro **miembros pszText** .

El **mensaje \_ INSERTITEM de LVM** insertará el nuevo elemento en la posición adecuada en el criterio de ordenación si se cumplen las condiciones siguientes:

-   Está usando uno de los estilos de LVS \_ SORTXXX.
-   No se usa el estilo [**\_ OWNERDRAW LVS**](list-view-window-styles.md) .
-   El miembro **miembros pszText** de la estructura a la que apunta **pitem** no se establece en LPSTR \_ TEXTCALLBACK.

Si la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) no contiene LVIF \_ GROUPID en el miembro **Mask** , el valor del miembro **iGroupId** es GROUPIDCALLBACK de \_ forma predeterminada.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **LVM \_ INSERTITEMW** (Unicode) y **\_ INSERTITEMA de LVM** (ANSI)<br/>             |



 

 





