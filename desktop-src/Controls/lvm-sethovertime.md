---
title: LVM_SETHOVERTIME mensaje (Commctrl.h)
description: Establece la cantidad de tiempo que el cursor del mouse debe mantener el puntero sobre un elemento antes de seleccionarlo. Puede enviar este mensaje explícitamente o usar la macro ListView \_ SetHoverTime.
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
ms.openlocfilehash: 8f93edf917dc50384f3a09f7eadf013561715735a995c63a695cb8f9ad91dbce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077235"
---
# <a name="lvm_sethovertime-message"></a>Mensaje \_ LVM SETHOVERTIME

Establece la cantidad de tiempo que el cursor del mouse debe mantener el puntero sobre un elemento antes de seleccionarlo. Puede enviar este mensaje explícitamente o usar la macro [**ListView \_ SetHoverTime.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Nueva cantidad de tiempo, en milisegundos, que el cursor del mouse debe mantener el puntero sobre un elemento antes de seleccionarlo. Si este valor es (**DWORD**)-1, el tiempo de desplazamiento se establece en el tiempo de desplazamiento predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve la hora de desplazamiento anterior.

## <a name="remarks"></a>Comentarios

El tiempo de desplazamiento solo afecta a los controles de vista de lista que tienen el estilo de vista de lista extendido [**LVS \_ EX \_ TRACKSELECT,**](extended-list-view-styles.md) [**LVS \_ EX \_ ONECLICKACTIVATE**](extended-list-view-styles.md)o [**LVS EX \_ \_ TWOCLICKACTIVATE.**](extended-list-view-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





