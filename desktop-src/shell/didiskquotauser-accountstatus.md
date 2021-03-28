---
description: Obtiene el estado de la cuenta del usuario.
title: Propiedad DIDiskQuotaUser. Estados
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
ms.openlocfilehash: 155ae627d70c5125fd0d1d501062224450fc8e3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984290"
---
# <a name="didiskquotauseraccountstatus-property"></a>Propiedad DIDiskQuotaUser. Estados

Obtiene el estado de la cuenta del usuario.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad puede tomar uno de los valores siguientes.



| Estado            | Value | Descripción                         |
|-------------------|-------|-------------------------------------|
| dqAcctResolved    | 0     | Se resolvió la información de la cuenta.    |
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
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> </dl>

 

 




