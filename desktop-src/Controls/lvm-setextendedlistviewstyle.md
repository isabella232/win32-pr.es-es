---
title: LVM_SETEXTENDEDLISTVIEWSTYLE mensaje (Commctrl.h)
description: Establece estilos extendidos en controles de vista de lista. Puede enviar este mensaje explícitamente o usar la \_ macro ListView SetExtendedListViewStyle o ListView \_ SetExtendedListViewStyleEx.
ms.assetid: eb3f47ed-484a-49a8-94b0-e50ee081bd69
keywords:
- LVM_SETEXTENDEDLISTVIEWSTYLE controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061793"
---
# <a name="lvm_setextendedlistviewstyle-message"></a>Mensaje LVM \_ SETEXTENDEDLISTVIEWSTYLE

Establece estilos extendidos en controles de vista de lista. Puede enviar este mensaje explícitamente o usar la macro [**\_ ListView SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) o [**ListView \_ SetExtendedListViewStyleEx.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Valor DWORD** que especifica los estilos de *lParam* que se van a ver afectados. Este parámetro puede ser una combinación de [**extended List-View Styles**](extended-list-view-styles.md). Solo se cambiarán los estilos extendidos de *wParam.* Todos los demás estilos se mantendrán tal y como están. Si este parámetro es cero, todos los estilos de *lParam* se verán afectados.

</dd> <dt>

*lParam* 
</dt> <dd>

**Valor DWORD** que especifica los estilos de control de vista de lista extendidos que se establecerán. Este parámetro puede ser una combinación de [**extended List-View Styles**](extended-list-view-styles.md). Se quitan los estilos que no están establecidos, pero que se especifican en *wParam.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que contiene los estilos de control de vista de lista extendidos anteriores.

## <a name="remarks"></a>Observaciones

El *parámetro wParam* permite modificar uno o varios estilos extendidos sin tener que recuperar primero los estilos existentes. Por ejemplo, si pasa [**LVS \_ EX \_ FULLROWSELECT**](extended-list-view-styles.md) para *wParam* y 0 para *lParam,* se borrará el estilo **LVS \_ EX \_ FULLROWSELECT,** pero todos los demás estilos seguirán siendo los mismos.

Por motivos de compatibilidad con versiones anteriores, la macro [**\_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) de ListView no se ha actualizado para usar *wParam*. Para usar el *valor wParam,* use la macro [**\_ ListView SetExtendedListViewStyleEx.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)

Cuando use este mensaje para establecer el estilo [**LVS \_ EX \_ CHECKBOXES,**](extended-list-view-styles.md) se descartará cualquier índice de imagen de estado establecido previamente. Todas las casillas se inicializarán en el estado desactivado. El índice de imagen de estado se encuentra en los bits 12 a 15 del miembro **de** estado de la [**estructura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





