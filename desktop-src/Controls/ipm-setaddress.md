---
title: Mensaje de IPM_SETADDRESS (commctrl. h)
description: Establece los valores de dirección de los cuatro campos en el control de dirección IP.
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- IPM_SETADDRESS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- IPM_SETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a8e8e4fa69791f93094d24f990ad62207cad33dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150547"
---
# <a name="ipm_setaddress-message"></a>\_Mensaje SETADDRESS de IPM

Establece los valores de dirección de los cuatro campos en el control de dirección IP.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor **DWORD** que contiene la nueva dirección. El valor del campo 3 se incluye en los bits 0 a 7. El valor del campo 2 se incluye en los bits 8 a 15. El valor del campo 1 se incluye en los bits 16 a 23. El valor del campo 0 está incluido en los bits 24 a 31. La macro [**MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) también se puede usar para crear la información de dirección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se utiliza el valor devuelto.

## <a name="remarks"></a>Observaciones

Este mensaje no genera una notificación [**de \_ FIELDCHANGED de IPN**](ipn-fieldchanged.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





