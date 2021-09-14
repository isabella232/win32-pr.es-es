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
ms.openlocfilehash: 83e243ece42f06ffe35eb31954d9ca0dd44957be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974086"
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

## <a name="remarks"></a>Observaciones

El tiempo de desplazamiento del mouse solo afecta a los controles de vista de lista que tienen el estilo de vista de lista extendido [**LVS \_ EX \_ TRACKSELECT,**](extended-list-view-styles.md) [**LVS \_ EX \_ ONECLICKACTIVATE**](extended-list-view-styles.md)o [**LVS EX \_ \_ TWOCLICKACTIVATE.**](extended-list-view-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





