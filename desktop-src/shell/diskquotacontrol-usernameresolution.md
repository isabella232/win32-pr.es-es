---
description: Establece u obtiene un valor que controla cómo se resuelve el identificador de seguridad de usuario (SID) en nombres de usuario.
title: Propiedad DiskQuotaControl.UserNameResolution
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.UserNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: dc936421-e66d-4762-912a-c586f9cdace4
ms.openlocfilehash: 169f4db6e135392e9548767520f6d2b0bd2d527c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841466"
---
# <a name="diskquotacontrolusernameresolution-property"></a>Propiedad DiskQuotaControl.UserNameResolution

Establece u obtiene un valor que controla cómo se resuelve el identificador de seguridad de usuario (SID) en nombres de usuario.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a>Valor de propiedad

Esta propiedad se puede establecer en uno de los valores siguientes.



| Tipo de resolución | Value | Descripción                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| dqResolveNone   | 0     | No resuelva la información de nombre de usuario.                                                                                                                    |
| dqResolveSync   | 1     | Espere mientras resuelve la información de nombre.                                                                                                                   |
| dqResolveAsync  | 2     | No espere mientras resuelve la información de nombre. El [**evento OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) se produce cuando se resuelve el nombre. |



 

## <a name="remarks"></a>Observaciones

Esta propiedad afecta a la enumeración de [**objetos DIDiskQuotaUser**](didiskquotauser-object.md) y a los [**métodos AddUser**](diskquotacontrol-adduser.md) [**y FindUser.**](diskquotacontrol-finduser.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DiskQuotaControl (objeto)**](diskquotacontrol-object.md)
</dt> </dl>

 

 




