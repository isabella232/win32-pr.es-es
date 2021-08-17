---
title: RAS_USER_0 estructura (Rassapi.h)
description: La estructura RAS USER 0 se usa en las funciones \_ \_ RasAdminUserSetInfo y RasAdminUserGetInfo para especificar información sobre un usuario.
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS_USER_0 estructura RAS
- PRAS_USER_0 puntero raso de estructura
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
ms.openlocfilehash: cbb4b04ddf3b81d330825b3333899e149d2f7b0d1f30c19106c6977e5291846f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789147"
---
# <a name="ras_user_0-structure"></a>Estructura \_ RAS USER \_ 0

\[Esta versión de la **estructura \_ RAS USER \_ 0** no se admite desde Windows Vista. En su lugar, use la versión más reciente de [**\_ RAS USER \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) definida en mprapi.h.\]

La **estructura RAS USER \_ \_ 0** se usa en las funciones [**RasAdminUserSetInfo**](rasadminusersetinfo.md) y [**RasAdminUserGetInfo**](rasadminusergetinfo.md) para especificar información sobre un usuario.

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

Conjunto de marcas de bits que especifican los privilegios RAS del usuario. Este miembro puede ser una combinación de la marca \_ RASPRIV DialinPrivilege y una de las marcas de de vuelta de llamada. Use la máscara RASPRIV CallbackType para identificar el tipo de privilegios de devolución de \_ llamada proporcionados al usuario. Se definen las marcas siguientes.



| Value                                                                                                                                                                                                                                         | Significado                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <dt>**RASPRIV \_ NoCallback**</dt> </dl>                             | El usuario no tiene ningún privilegio de des llamada.<br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <dt>**RASPRIV \_ AdminSetCallback**</dt> </dl>     | La cuenta de usuario está configurada para que el administrador establezca el número de llamada atrás.<br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <dt>**RASPRIV \_ CallerSetCallback**</dt> </dl> | El usuario remoto puede especificar un número de teléfono de llamada al marcar.<br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <dt>**RASPRIV \_ DialinPrivilege**</dt> </dl>         | El usuario tiene permiso para acceder a este servidor.<br/>                                 |



 

Especifique una de las marcas de de vuelta de llamada en la llamada a la [**función RasAdminUserSetInfo.**](rasadminusersetinfo.md)

</dd> <dt>

**szPhoneNumber**
</dt> <dd>

Cadena Unicode terminada en NULL que especifica el número de teléfono de la llamada al usuario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Rassapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Introducción al Servicio de acceso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Estructuras de administración del servidor RAS](ras-server-administration-structures.md)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

 





