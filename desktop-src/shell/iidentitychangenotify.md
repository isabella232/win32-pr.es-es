---
description: Desusado. Proporciona una notificación de las modificaciones realizadas en las identidades de usuario en el sistema, así como las solicitudes de usuario para cambiar la identidad del usuario actual.
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: Interfaz IIdentityChangeNotify (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 4a217b2cfb046bfb9ae5546e015264f74d00b1d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276737"
---
# <a name="iidentitychangenotify-interface"></a>Interfaz IIdentityChangeNotify

\[La interfaz **IIdentityChangeNotify** está disponible para su uso en Windows 2000. En Windows XP, esta funcionalidad se ha sustituido por [las cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md), y puede modificarse o no estar disponible en las versiones posteriores.\]

En desuso. Proporciona una notificación de las modificaciones realizadas en las identidades de usuario en el sistema, así como las solicitudes de usuario para cambiar la identidad del usuario actual.

## <a name="members"></a>Miembros

La interfaz **IIdentityChangeNotify** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IIdentityChangeNotify** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IIdentityChangeNotify** tiene estos métodos.



| Método                                                                                 | Descripción                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**IdentityInformationChanged**](iidentitychangenotify-identityinformationchanged.md) | En desuso. Se llama cuando ha cambiado la información sobre una identidad de usuario o cuando se ha agregado o eliminado una identidad de usuario.<br/>  |
| [**QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md)           | En desuso. Se llama cuando el usuario actual ha solicitado que se cambie su identidad de usuario, pero antes de que se produzca el cambio.<br/> |
| [**SwitchIdentities**](iidentitychangenotify-switchidentities.md)                     | En desuso. Se llama cuando se cambian las identidades de usuario.<br/>                                                                      |



 

## <a name="remarks"></a>Observaciones

Para implementar notificaciones, una interfaz derivada debe conectarse al [**IUserIdentityManager**](iuseridentitymanager.md) llamando a [**IConnectionPoint:: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) y pasando un puntero a la interfaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 
