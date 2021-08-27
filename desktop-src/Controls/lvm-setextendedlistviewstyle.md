---
title: LVM_SETEXTENDEDLISTVIEWSTYLE mensaje (Commctrl.h)
description: Establece estilos extendidos en controles de vista de lista. Puede enviar este mensaje explícitamente o usar la \_ macro ListView SetExtendedListViewStyle o \_ ListView SetExtendedListViewStyleEx.
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
ms.openlocfilehash: 336732b927c7ee6170e777f2f7c1cd57eac6baa2c7706870e681f602e2309c37
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077285"
---
# <a name="lvm_setextendedlistviewstyle-message"></a>Mensaje \_ LVM SETEXTENDEDLISTVIEWSTYLE

Establece estilos extendidos en controles de vista de lista. Puede enviar este mensaje explícitamente o usar la macro [**\_ ListView SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) o [**\_ ListView SetExtendedListViewStyleEx.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Valor DWORD** que especifica qué estilos de *lParam* se verán afectados. Este parámetro puede ser una combinación de [**estilos List-View extendidos.**](extended-list-view-styles.md) Solo se cambiarán los estilos extendidos de *wParam.* Todos los demás estilos se mantendrán tal y como están. Si este parámetro es cero, se verán afectados todos los estilos de *lParam.*

</dd> <dt>

*lParam* 
</dt> <dd>

**Valor DWORD** que especifica los estilos de control de vista de lista extendidos que se establecerán. Este parámetro puede ser una combinación de [**estilos List-View extendidos.**](extended-list-view-styles.md) Se quitan los estilos que no se establecen, pero que se especifican en *wParam.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor DWORD** que contiene los estilos de control de vista de lista extendidos anteriores.

## <a name="remarks"></a>Comentarios

El *parámetro wParam* permite modificar uno o varios estilos extendidos sin tener que recuperar primero los estilos existentes. Por ejemplo, si pasa [**LVS \_ EX \_ FULLROWSELECT**](extended-list-view-styles.md) para *wParam* y 0 para *lParam*, se borrará el estilo **LVS \_ EX \_ FULLROWSELECT,** pero todos los demás estilos seguirán siendo los mismos.

Por motivos de compatibilidad con versiones anteriores, la macro [**\_ SetExtendedListViewStyle**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyle) de ListView no se ha actualizado para usar *wParam*. Para usar el *valor wParam,* use la macro [**\_ SetExtendedListViewStyleEx de ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setextendedlistviewstyleex)

Cuando use este mensaje para establecer el estilo [**LVS \_ EX \_ CHECKBOXES,**](extended-list-view-styles.md) se descartará cualquier índice de imagen de estado establecido previamente. Todas las casillas se inicializarán en el estado desactivado. El índice de imagen de estado se encuentra en los bits 12 a 15 del miembro **de** estado de la [**estructura LVITEM.**](/windows/win32/api/commctrl/ns-commctrl-lvitema)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





