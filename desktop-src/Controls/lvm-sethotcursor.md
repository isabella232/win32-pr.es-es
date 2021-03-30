---
title: Mensaje de LVM_SETHOTCURSOR (commctrl. h)
description: Establece el valor de HCURSOR que usa el control de vista de lista cuando el puntero se encuentra sobre un elemento mientras está habilitado el seguimiento activo.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- LVM_SETHOTCURSOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_SETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e743f74eda3b59f04f6f4793b47d76da3bab881
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801111"
---
# <a name="lvm_sethotcursor-message"></a>\_Mensaje SETHOTCURSOR LVM

Establece el valor de HCURSOR que usa el control de vista de lista cuando el puntero se encuentra sobre un elemento mientras está habilitado el seguimiento activo. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ SetHotCursor de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) . Para comprobar si el seguimiento activo está habilitado, llame a [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cursor que se va a establecer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de HCURSOR que es el cursor activo anterior.

## <a name="remarks"></a>Observaciones

Un control de vista de lista usa el seguimiento activo y la selección del mouse cuando se establece el estilo [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

