---
description: Se produce cuando se ha resuelto la información de nombre de un objeto DIDiskQuotaUser.
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: Función OnUserNameChanged (Dskquota.h)
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
ms.openlocfilehash: 02e4227e06d9c9303a5fe9b799afff6e452843bbb7c0dac096b39f925e568d25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459898"
---
# <a name="onusernamechanged-function"></a>Función OnUserNameChanged

Se produce cuando se ha resuelto la información de nombre de un objeto [**DIDiskQuotaUser.**](didiskquotauser-object.md)

## <a name="parameters"></a>Parámetros

<dl> <dt>

*oUser* 
</dt> <dd>

Objeto **que** se evalúa como el [**objeto DIDiskQuotaUser**](didiskquotauser-object.md) asociado al usuario cuyo nombre se ha resuelto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Cuando un cliente [**enumera los**](didiskquotauser-object.md)usuarios o llama al método [**AddUser**](diskquotacontrol-adduser.md) o [**FindUser,**](diskquotacontrol-finduser.md) el nombre de usuario debe resolverse en el identificador de seguridad (SID) asociado. Dado que este procedimiento puede llevar mucho tiempo, un cliente puede hacer que la resolución de nombres se haga de forma asincrónica en un subproceso en segundo plano. Cuando se resuelve el nombre de un usuario, el [**objeto DiskQuotaControl**](diskquotacontrol-object.md) notifica a su cliente mediante la activación del **evento OnUserNameChanged.** Un **objeto DIDiskQuotaUser** asociado al usuario se pasa como parámetro. Este objeto permite al cliente modificar la configuración de cuota del usuario.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Dskquota.h</dt> </dl>                         |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DiskQuotaControl (objeto)**](diskquotacontrol-object.md)
</dt> </dl>

 

 




