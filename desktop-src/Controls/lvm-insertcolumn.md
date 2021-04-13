---
title: Mensaje de LVM_INSERTCOLUMN (commctrl. h)
description: Inserta una nueva columna en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la \_ macro InsertColumn de ListView.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- LVM_INSERTCOLUMN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be89ff0b4ef417a715085582544112cb90cb6b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535032"
---
# <a name="lvm_insertcolumn-message"></a>\_Mensaje INSERTCOLUMN LVM

Inserta una nueva columna en un control de vista de lista. Puede enviar este mensaje explícitamente o mediante la macro [**\_ InsertColumn de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de la nueva columna.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una estructura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que contiene los atributos de la nueva columna.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el índice de la nueva columna si se realiza correctamente, o-1 en caso contrario.

## <a name="remarks"></a>Observaciones

Las columnas solo son visibles en la vista informe (detalles).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





