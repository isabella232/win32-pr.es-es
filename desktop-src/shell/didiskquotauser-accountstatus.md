---
description: Obtiene el estado de la cuenta del usuario.
title: Propiedad DIDiskQuotaUser.AccountStatus
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ff2234f7-4758-43c7-a3c2-8fb980b27c04
ms.openlocfilehash: e27e86fadab02616f91a4838acfc4be93e985ebd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841656"
---
# <a name="didiskquotauseraccountstatus-property"></a>Propiedad DIDiskQuotaUser.AccountStatus

Obtiene el estado de la cuenta del usuario.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad puede tomar uno de los siguientes valores.



| Estado            | Value | Descripción                         |
|-------------------|-------|-------------------------------------|
| dqAcctResolved    | 0     | Se resuelve la información de la cuenta.    |
| dqAcctUnavailable | 1     | La información de la cuenta no está disponible. |
| dqAcctDeleted     | 2     | Se ha eliminado la cuenta.           |
| dqAcctInvalid     | 3     | La cuenta no es válida.                 |
| dqAcctUnknown     | 4     | No se encuentra la cuenta.            |
| dqAcctUnresolved  | 5     | La información de la cuenta no está resuelta.  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DIDiskQuotaUser (objeto)**](didiskquotauser-object.md)
</dt> </dl>

 

 




