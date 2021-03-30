---
title: Mensaje de LVM_GETHOTCURSOR (commctrl. h)
description: Recupera el valor de HCURSOR que se usa cuando el puntero se encuentra sobre un elemento mientras está habilitado el seguimiento activo. Puede enviar este mensaje explícitamente o utilizar la \_ macro GetHotCursor de ListView.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- LVM_GETHOTCURSOR controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddd8fa4c038bf2fb1c10816319504dd9de32c0e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803404"
---
# <a name="lvm_gethotcursor-message"></a>\_Mensaje GETHOTCURSOR LVM

Recupera el valor de HCURSOR que se usa cuando el puntero se encuentra sobre un elemento mientras está habilitado el seguimiento activo. Puede enviar este mensaje explícitamente o utilizar la [**macro \_ GetHotCursor de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de HCURSOR que es el identificador del cursor que el control de vista de lista utiliza cuando está habilitado el seguimiento activo.

## <a name="remarks"></a>Observaciones

Un control de vista de lista usa el seguimiento activo y la selección del mouse cuando se establece el estilo [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





