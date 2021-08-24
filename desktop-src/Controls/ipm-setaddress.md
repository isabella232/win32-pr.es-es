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
ms.openlocfilehash: 54817d2206295432e9b477532268a000fc43047ae928ab02224d668912474519
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434495"
---
# <a name="ipm_setaddress-message"></a>Mensaje \_ SETADDRESS de IPM

Establece los valores de dirección de los cuatro campos del control de direcciones IP.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Valor **DWORD** que contiene la nueva dirección. El valor del campo 3 se encuentra en los bits 0 a 7. El valor del campo 2 está contenido en los bits 8 a 15. El valor del campo 1 está contenido en los bits 16 a 23. El valor del campo 0 está contenido en los bits 24 a 31. La [**macro MAKEIPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-makeipaddress) también se puede usar para crear la información de dirección.

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
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





