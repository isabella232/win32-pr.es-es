---
title: IPM_SETADDRESS mensaje (Commctrl.h)
description: Establece los valores de dirección de los cuatro campos del control de direcciones IP.
ms.assetid: 52e72437-3558-4789-844f-5ab5b0b7967c
keywords:
- IPM_SETADDRESS controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061900"
---
# <a name="ipm_setaddress-message"></a>Mensaje \_ SETADDRESS de IPM

Establece los valores de dirección de los cuatro campos del control de direcciones IP.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor **DWORD** que contiene la nueva dirección. El valor del campo 3 se encuentra en los bits 0 a 7. El valor del campo 2 se encuentra en los bits 8 a 15. El valor del campo 1 se encuentra en los bits 16 a 23. El valor del campo 0 se encuentra en los bits 24 a 31. La [**macro MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) también se puede usar para crear la información de dirección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No se usa el valor devuelto.

## <a name="remarks"></a>Observaciones

Este mensaje no genera una notificación [**\_ FIELDCHANGED de IPN.**](ipn-fieldchanged.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





