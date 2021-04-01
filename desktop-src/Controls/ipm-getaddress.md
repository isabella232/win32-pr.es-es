---
title: Mensaje de IPM_GETADDRESS (commctrl. h)
description: Obtiene los valores de dirección de los cuatro campos del control de dirección IP.
ms.assetid: 4fe68d45-7d7f-46da-a110-65f899b3c393
keywords:
- IPM_GETADDRESS controles de mensajes de Windows
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
ms.openlocfilehash: 426e9c76712701b2f4e108679133be23eb700687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996648"
---
# <a name="ipm_getaddress-message"></a>Mensaje de GETADDRESS de IPM \_

Obtiene los valores de dirección de los cuatro campos del control de dirección IP.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>

Un puntero a un valor **DWORD** que recibe la dirección. El valor del campo 3 se incluirá en los bits 0 a 7. El valor del campo 2 estará incluido en los bits 8 a 15. El valor del campo 1 se incluirá en los bits 16 a 23. El valor del campo 0 se incluirá en los bits 24 a 31. Las [**primeras \_**](/windows/desktop/api/Commctrl/nf-commctrl-first_ipaddress)macros IPAddress, [**Second \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-second_ipaddress), [**tercera \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-third_ipaddress)y [**cuarto \_ IPAddress**](/windows/desktop/api/Commctrl/nf-commctrl-fourth_ipaddress) también se pueden usar para extraer la información de dirección. Se devolverá cero como dirección para los campos en blanco.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve el número de campos que no están en blanco.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





