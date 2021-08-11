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
ms.openlocfilehash: cfc86f7f7da03ea4ffb092d50b51ef0c69349935cdae40586e08ae50f6ea251b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118224618"
---
# <a name="diskquotacontrolusernameresolution-property"></a>Propiedad DiskQuotaControl.UserNameResolution

Establece u obtiene un valor que controla cómo se resuelve el identificador de seguridad de usuario (SID) en nombres de usuario.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


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



 

## <a name="remarks"></a>Comentarios

Esta propiedad afecta a la enumeración de [**objetos DIDiskQuotaUser**](didiskquotauser-object.md) y a los [**métodos AddUser**](diskquotacontrol-adduser.md) [**y FindUser.**](diskquotacontrol-finduser.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulta también

<dl> <dt>

[**DiskQuotaControl (objeto)**](diskquotacontrol-object.md)
</dt> </dl>

 

 




