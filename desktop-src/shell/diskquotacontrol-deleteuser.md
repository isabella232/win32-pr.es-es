---
description: Elimina un usuario del volumen.
ms.assetid: 56a07388-b7d8-41a4-b29a-8a57fe0b9d19
title: Método DiskQuotaControl. DeleteUser (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DeleteUser
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c159375727ef115631a8a047d69ce235a5b8f2a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275232"
---
# <a name="diskquotacontroldeleteuser-method"></a>DiskQuotaControl. DeleteUser, método

Elimina un usuario del volumen.

## <a name="syntax"></a>Sintaxis


```JScript
DiskQuotaControl.DeleteUser(
  oUser
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*oUser* 
</dt> <dd>

Tipo: **Object**

Expresión de objeto que se evalúa como el objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) del usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Este método produce un error si el usuario posee algún almacenamiento en el volumen. Antes de eliminar un usuario de un volumen, se debe eliminar todo el almacenamiento de ese usuario, moverse a otro volumen o transferir su propiedad a otro usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AddUser**](diskquotacontrol-adduser.md)
</dt> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




