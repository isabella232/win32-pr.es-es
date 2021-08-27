---
title: LVM_SETHOTCURSOR mensaje (Commctrl.h)
description: Establece el valor HCURSOR que usa el control de vista de lista cuando el puntero está sobre un elemento mientras está habilitado el seguimiento de acceso activa.
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
ms.openlocfilehash: 3407c5d8b53483d3a639fc40959768b3fa8eea0e7b439ab8871d36346b7079d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077255"
---
# <a name="lvm_sethotcursor-message"></a>Mensaje \_ SETHOTCURSOR de LVM

Establece el valor HCURSOR que usa el control de vista de lista cuando el puntero está sobre un elemento mientras está habilitado el seguimiento de acceso activa. Puede enviar este mensaje explícitamente o usar la macro [**\_ ListView SetHotCursor.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotcursor) Para comprobar si está habilitado el seguimiento en caliente, llame [**a SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa).

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

## <a name="remarks"></a>Comentarios

Un control de vista de lista usa el seguimiento de actividad y mantiene el puntero sobre la selección cuando se establece el estilo [**LVS \_ EX \_ TRACKSELECT.**](extended-list-view-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

