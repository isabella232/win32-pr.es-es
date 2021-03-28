---
description: Establece u obtiene un valor que controla cómo se resuelve el identificador de seguridad (SID) del usuario en los nombres de usuario.
title: Propiedad DiskQuotaControl. UserNameResolution
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
ms.openlocfilehash: fbe079680191937f022bd45a491fad054e1a9033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984414"
---
# <a name="diskquotacontrolusernameresolution-property"></a>Propiedad DiskQuotaControl. UserNameResolution

Establece u obtiene un valor que controla cómo se resuelve el identificador de seguridad (SID) del usuario en los nombres de usuario.

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
| dqResolveNone   | 0     | No resuelva la información del nombre de usuario.                                                                                                                    |
| dqResolveSync   | 1     | Espere mientras se resuelve la información de nombre.                                                                                                                   |
| dqResolveAsync  | 2     | No espere a que se resuelva la información de nombre. El evento [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) se desencadena cuando se resuelve el nombre. |



 

## <a name="remarks"></a>Observaciones

Esta propiedad afecta a la enumeración de los objetos [**DIDiskQuotaUser**](didiskquotauser-object.md) y a los métodos [**adduser**](diskquotacontrol-adduser.md) y [**FindUser**](diskquotacontrol-finduser.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




