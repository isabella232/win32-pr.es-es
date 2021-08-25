---
title: LVM_GETHOVERTIME mensaje (Commctrl.h)
description: Recupera la cantidad de tiempo que el cursor del mouse debe mantener el puntero sobre un elemento antes de seleccionarlo. Puede enviar este mensaje explícitamente o usar la \_ macro ListView GetHoverTime.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- LVM_GETHOVERTIME controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_GETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 150a8eff54f8b3c27f0e7783ceda67af60c326e370d1a518d83e6bdd214fb529
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920105"
---
# <a name="lvm_gethovertime-message"></a>Mensaje \_ GETHOVERTIME de LVM

Recupera la cantidad de tiempo que el cursor del mouse debe mantener el puntero sobre un elemento antes de seleccionarlo. Puede enviar este mensaje explícitamente o usar la macro [**\_ ListView GetHoverTime.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la cantidad de tiempo, en milisegundos, que el cursor del mouse debe mantener el puntero sobre un elemento antes de seleccionarlo. Si el valor devuelto es (**DWORD**)-1, la hora de mantener el puntero es la hora de desplazamiento predeterminada.

## <a name="remarks"></a>Comentarios

El tiempo de desplazamiento del mouse solo afecta a los controles de vista de lista que tienen el estilo de vista de lista extendido [**LVS \_ EX \_ TRACKSELECT,**](extended-list-view-styles.md) [**LVS \_ EX \_ ONECLICKACTIVATE**](extended-list-view-styles.md)o [**LVS EX \_ \_ TWOCLICKACTIVATE.**](extended-list-view-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





