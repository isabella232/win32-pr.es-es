---
title: IPM_GETADDRESS mensaje (Commctrl.h)
description: Obtiene los valores de dirección de los cuatro campos del control de direcciones IP.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- IPM_GETADDRESS controles de Windows mensaje
topic_type:
- apiref
api_name:
- IPM_GETADDRESS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9bcb35ed71532e815b33b45e1c15e9b82b75b5c87fac406b52de80670e3d72a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434524"
---
# <a name="ipm_getaddress-message"></a>Mensaje \_ GETADDRESS de IPM

Obtiene los valores de dirección de los cuatro campos del control de direcciones IP.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a un **valor DWORD** que recibe la dirección . El valor del campo 3 se incluirá en los bits 0 a 7. El valor del campo 2 se incluirá en los bits 8 a 15. El valor del campo 1 se incluirá en los bits 16 a 23. El valor del campo 0 se incluirá en los bits 24 a 31. Las macros [**FIRST \_ IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress), [**SECOND \_ IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress), [**THIRD \_ IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)y [**FOURTH \_ IPADDRESS**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) también se pueden usar para extraer la información de dirección. Se devolverá cero como dirección de los campos en blanco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de campos no en página.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





