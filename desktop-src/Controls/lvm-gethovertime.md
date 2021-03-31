---
title: Mensaje de LVM_GETHOVERTIME (commctrl. h)
description: Recupera la cantidad de tiempo que el cursor del mouse debe mantener el puntero sobre un elemento antes de que se seleccione. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetHoverTime de ListView.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- LVM_GETHOVERTIME controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491465"
---
# <a name="lvm_gethovertime-message"></a>\_Mensaje GETHOVERTIME LVM

Recupera la cantidad de tiempo que el cursor del mouse debe mantener el puntero sobre un elemento antes de que se seleccione. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetHoverTime de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la cantidad de tiempo, en milisegundos, que el cursor del mouse debe mantener el puntero sobre un elemento antes de que se seleccione. Si el valor devuelto es (**DWORD**)-1, el tiempo de activación es el tiempo de desplazamiento predeterminado.

## <a name="remarks"></a>Observaciones

El tiempo de desplazamiento solo afecta a los controles de vista de lista que tienen el estilo de vista de lista extendido [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)o [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





