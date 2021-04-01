---
title: Mensaje de LVM_SETHOVERTIME (commctrl. h)
description: Establece la cantidad de tiempo que el cursor del mouse debe mantener el puntero sobre un elemento antes de que se seleccione. Puede enviar este mensaje explícitamente o utilizar la \_ macro SetHoverTime de ListView.
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- LVM_SETHOVERTIME controles de mensajes de Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149896"
---
# <a name="lvm_sethovertime-message"></a>\_Mensaje SETHOVERTIME LVM

Establece la cantidad de tiempo que el cursor del mouse debe mantener el puntero sobre un elemento antes de que se seleccione. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetHoverTime de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

La nueva cantidad de tiempo, en milisegundos, que el cursor del mouse debe mantener el puntero sobre un elemento antes de que se seleccione. Si este valor es (**DWORD**)-1, el tiempo de desplazamiento se establece en el tiempo de desplazamiento predeterminado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el tiempo de desplazamiento anterior.

## <a name="remarks"></a>Observaciones

El tiempo de desplazamiento solo afecta a los controles de vista de lista que tienen el estilo de vista de lista extendido [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)o [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





