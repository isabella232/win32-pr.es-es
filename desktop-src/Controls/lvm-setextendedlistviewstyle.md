---
title: Mensaje de LVM_SETEXTENDEDLISTVIEWSTYLE (commctrl. h)
description: Establece los estilos extendidos en los controles de vista de lista. Puede enviar este mensaje explícitamente o utilizar la \_ macro SetExtendedListViewStyle o ListView \_ SetExtendedListViewStyleEx de ListView.
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- LVM_SETEXTENDEDLISTVIEWSTYLE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETEXTENDEDLISTVIEWSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7d36869283d863bef7b31187a002125c9cd79bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995937"
---
# <a name="lvm_setextendedlistviewstyle-message"></a>\_Mensaje SETEXTENDEDLISTVIEWSTYLE LVM

Establece los estilos extendidos en los controles de vista de lista. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) o [**ListView \_ SetExtendedListViewStyleEx**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) de ListView.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **DWORD** que especifica los estilos de *lParam* que se van a ver afectados. Este parámetro puede ser una combinación de [**estilos de List-View extendidos**](extended-list-view-styles.md). Solo se cambiarán los estilos extendidos de *wParam* . Todos los demás estilos se conservarán tal como están. Si este parámetro es cero, se verán afectados todos los estilos de *lParam* .

</dd> <dt>

*lParam* 
</dt> <dd>

Valor **DWORD** que especifica los estilos extendidos de control de vista de lista que se van a establecer. Este parámetro puede ser una combinación de [**estilos de List-View extendidos**](extended-list-view-styles.md). Los estilos que no están establecidos, pero que se especifican en *wParam*, se quitan.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **DWORD** que contiene los estilos de control extendidos anteriores de la vista de lista.

## <a name="remarks"></a>Observaciones

El parámetro *wParam* permite modificar uno o más estilos extendidos sin tener que recuperar primero los estilos existentes. Por ejemplo, si pasa [**LVS \_ ex \_ FULLROWSELECT**](extended-list-view-styles.md) para *wParam* y 0 para *lParam*, se borrará el estilo **LVS \_ ex \_ FULLROWSELECT** , pero el resto de los estilos permanecerán iguales.

Por motivos de compatibilidad con versiones anteriores, la macro [**\_ SetExtendedListViewStyle de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) no se ha actualizado para usar *wParam*. Para usar el valor *wParam* , use la [**macro \_ SetExtendedListViewStyleEx de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex) .

Cuando se usa este mensaje para establecer el [**estilo \_ \_ casillas de LVS ex**](extended-list-view-styles.md) , se descartará cualquier índice de imagen de estado establecido previamente. Todas las casillas se inicializarán en estado desactivado. El índice de la imagen de estado se encuentra en los bits 12 a 15 del miembro **State** de la estructura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





