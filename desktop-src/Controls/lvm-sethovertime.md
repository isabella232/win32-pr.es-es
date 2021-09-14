---
title: LVM_SETHOVERTIME mensaje (Commctrl.h)
description: Establece la cantidad de tiempo que el cursor del mouse debe mantener el puntero sobre un elemento antes de seleccionarlo. Puede enviar este mensaje explícitamente o usar la \_ macro SetHoverTime de ListView.
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- LVM_SETHOVERTIME controles de Windows mensaje
topic_type:
- apiref
api_name:
- LVM_SETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3aecd3c0d48cddc2cbaae49e7e888f91a985575
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362730"
---
# <a name="lvm_sethovertime-message"></a>Mensaje \_ LVM SETHOVERTIME

Establece la cantidad de tiempo que el cursor del mouse debe mantener el puntero sobre un elemento antes de seleccionarlo. Puede enviar este mensaje explícitamente o usar la macro [**\_ SetHoverTime de ListView.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Nueva cantidad de tiempo, en milisegundos, que el cursor del mouse debe mantener el puntero sobre un elemento antes de seleccionarlo. Si este valor es (**DWORD**)-1, la hora de mantener el puntero se establece en la hora de desplazamiento predeterminada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la hora de mantener el puntero anterior.

## <a name="remarks"></a>Observaciones

El tiempo de desplazamiento del mouse solo afecta a los controles de vista de lista que tienen el estilo de vista de lista extendido [**LVS \_ EX \_ TRACKSELECT,**](extended-list-view-styles.md) [**LVS \_ EX \_ ONECLICKACTIVATE**](extended-list-view-styles.md)o [**LVS EX \_ \_ TWOCLICKACTIVATE.**](extended-list-view-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





