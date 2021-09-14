---
title: LVM_SETHOTCURSOR mensaje (Commctrl.h)
description: Establece el valor HCURSOR que usa el control de vista de lista cuando el puntero está sobre un elemento mientras está habilitado el seguimiento en caliente.
ms.assetid: e3ff8608-9389-4167-839b-ecc2be01bb64
keywords:
- LVM_SETHOTCURSOR controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974069"
---
# <a name="lvm_sethotcursor-message"></a>Mensaje \_ SETHOTCURSOR de LVM

Establece el valor HCURSOR que usa el control de vista de lista cuando el puntero está sobre un elemento mientras está habilitado el seguimiento en caliente. Puede enviar este mensaje explícitamente o usar la macro [**ListView \_ SetHotCursor.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) Para comprobar si está habilitado el seguimiento en caliente, llame [**a SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador del cursor que se va a establecer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor HCURSOR que es el cursor de acceso directo anterior.

## <a name="remarks"></a>Observaciones

Un control de vista de lista usa el seguimiento en caliente y la selección del mouse cuando se establece el estilo [**LVS \_ EX \_ TRACKSELECT.**](extended-list-view-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

