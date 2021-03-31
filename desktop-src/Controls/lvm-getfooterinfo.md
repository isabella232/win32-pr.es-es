---
title: Mensaje de LVM_GETFOOTERINFO (commctrl. h)
description: Obtiene información sobre el pie de página de un control de vista de lista. Envíe este mensaje explícitamente o mediante la \_ macro GetFooterInfo de ListView.
ms.assetid: 5734e151-50c0-46df-8f2c-220c4910a590
keywords:
- LVM_GETFOOTERINFO controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LVM_GETFOOTERINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718e6c165985981190b5a1d4c52e851d1a2d504d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995939"
---
# <a name="lvm_getfooterinfo-message"></a>\_Mensaje GETFOOTERINFO LVM

Obtiene información sobre el pie de página de un control de vista de lista. Envíe este mensaje explícitamente o mediante la [**macro \_ GetFooterInfo de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getfooterinfo) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

No se utiliza. Debe ser 0.

</dd> <dt>

*lParam* \[ in, out\]
</dt> <dd>

Un puntero a una estructura [**LVFOOTERINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfooterinfo) para recibir información según el valor del miembro de **máscara** . El proceso de llamada es responsable de asignar esta estructura y establecer el miembro de la **máscara** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





