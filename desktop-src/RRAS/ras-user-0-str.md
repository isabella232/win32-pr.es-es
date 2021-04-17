---
title: RAS_USER_0 estructura (rassapi. h)
description: La \_ \_ estructura de usuario de Ras 0 se usa en las funciones RasAdminUserSetInfo y RasAdminUserGetInfo para especificar información sobre un usuario.
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS_USER_0 de la estructura RAS
- PRAS_USER_0 de puntero de estructura RAS
topic_type:
- apiref
api_name:
- RAS_USER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c79a6b946ed9d10cd2bfc989f8cde27fad2ffa92
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534102"
---
# <a name="ras_user_0-structure"></a>Estructura del usuario de RAS \_ \_ 0

\[Esta versión de la estructura de **usuario de Ras \_ \_ 0** no es compatible con Windows Vista. En su lugar, use el [**\_ usuario ras \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) más reciente definido en mprapi. h.\]

La estructura de **usuario de Ras \_ \_ 0** se usa en las funciones [**RasAdminUserSetInfo**](rasadminusersetinfo.md) y [**RasAdminUserGetInfo**](rasadminusergetinfo.md) para especificar información sobre un usuario.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _RAS_USER_0 {
  BYTE  bfPrivilege;
  WCHAR szPhoneNumber[RASSAPI_MAX_PHONENUMBER_SIZE + 1];
} RAS_USER_0, *PRAS_USER_0;
```



## <a name="members"></a>Miembros

<dl> <dt>

**bfPrivilege**
</dt> <dd>

Un conjunto de marcadores de bits que especifican los privilegios RAS del usuario. Este miembro puede ser una combinación de la \_ marca RASPRIV DialinPrivilege y una de las marcas de devolución de llamada. Use la máscara de CallbackType de RASPRIV \_ para identificar el tipo de privilegio de devolución de llamada que se proporciona al usuario. Se definen las marcas siguientes.



| Value                                                                                                                                                                                                                                         | Significado                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <dt>**RASPRIV \_ Nocallback**</dt> </dl>                             | El usuario no tiene ningún privilegio de devolución de llamada.<br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <dt>**RASPRIV \_ AdminSetCallback**</dt> </dl>     | La cuenta de usuario está configurada para que el administrador establezca el número de devolución de llamada.<br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <dt>**RASPRIV \_ CallerSetCallback**</dt> </dl> | El usuario remoto puede especificar un número de teléfono de devolución de llamada al llamar a.<br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <dt>**RASPRIV \_ DialinPrivilege**</dt> </dl>         | El usuario tiene permiso para llamar a este servidor.<br/>                                 |



 

Especifique una de las marcas de devolución de llamada en la llamada a la función [**RasAdminUserSetInfo**](rasadminusersetinfo.md) .

</dd> <dt>

**szPhoneNumber**
</dt> <dd>

Una cadena Unicode terminada en null que especifica el número de teléfono de devolución de llamada para el usuario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Estructuras de administración del servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

 





