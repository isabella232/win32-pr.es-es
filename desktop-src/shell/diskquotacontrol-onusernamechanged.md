---
description: Se produce cuando se ha resuelto la información de nombre de un objeto DIDiskQuotaUser.
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: Función OnUserNameChanged (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnUserNameChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 98906f281c6c93a64754c1aa5cecfc6624599c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360886"
---
# <a name="onusernamechanged-function"></a>OnUserNameChanged función)

Se produce cuando se ha resuelto la información de nombre de un objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) .

## <a name="parameters"></a>Parámetros

<dl> <dt>

*oUser* 
</dt> <dd>

**Objeto** que se evalúa como el objeto [**DIDiskQuotaUser**](didiskquotauser-object.md) asociado al usuario cuyo nombre se ha resuelto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Cuando un cliente [**enumera usuarios**](didiskquotauser-object.md)o llama al método [**adduser**](diskquotacontrol-adduser.md) o [**FindUser**](diskquotacontrol-finduser.md) , el nombre de usuario debe resolverse en el identificador de seguridad (SID) asociado. Dado que este procedimiento puede llevar mucho tiempo, un cliente puede tener una resolución de nombres realizada de forma asincrónica en un subproceso en segundo plano. Cuando se resuelve el nombre de un usuario, el objeto [**DiskQuotaControl**](diskquotacontrol-object.md) notifica a su cliente desencadenando el evento **OnUserNameChanged** . Un objeto **DIDiskQuotaUser** asociado al usuario se pasa como un parámetro. Este objeto permite al cliente modificar la configuración de la cuota del usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




