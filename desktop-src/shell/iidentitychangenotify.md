---
description: Desusado. Proporciona notificaciones de modificaciones en las identidades de usuario en el sistema, así como solicitudes de usuario para cambiar la identidad de usuario actual.
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: Interfaz IIdentityChangeNotify (Msident.h)
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
ms.openlocfilehash: 4419f55b2fe4561a22035d962da5e3c271108d06fa417cfbed1b603c883e5b32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118721913"
---
# <a name="iidentitychangenotify-interface"></a>IIdentityChangeNotify (interfaz)

\[La **interfaz IIdentityChangeNotify** está disponible para su uso Windows 2000. En Windows XP, esta funcionalidad se ha reemplazado por cuentas de usuario con cambio rápido de usuario y [Escritorio remoto](fastuserswitching.md), y podría modificarse o no estar disponible en versiones posteriores.\]

En desuso. Proporciona notificaciones de modificaciones en las identidades de usuario en el sistema, así como solicitudes de usuario para cambiar la identidad de usuario actual.

## <a name="members"></a>Miembros

La **interfaz IIdentityChangeNotify** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IIdentityChangeNotify** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IIdentityChangeNotify** tiene estos métodos.



| Método                                                                                 | Descripción                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [**IdentityInformationChanged**](iidentitychangenotify-identityinformationchanged.md) | En desuso. Se llama cuando ha cambiado la información sobre una identidad de usuario o cuando se ha agregado o eliminado una identidad de usuario.<br/>  |
| [**QuerySwitchIdentities**](iidentitychangenotify-queryswitchidentities.md)           | En desuso. Se llama cuando el usuario actual ha solicitado que se cambie su identidad de usuario, pero antes de que se produzca el cambio.<br/> |
| [**SwitchIdentities**](iidentitychangenotify-switchidentities.md)                     | En desuso. Se llama cuando se cambian las identidades de usuario.<br/>                                                                      |



 

## <a name="remarks"></a>Comentarios

Para implementar notificaciones, una interfaz derivada debe conectarse a [**IUserIdentityManager**](iuseridentitymanager.md) llamando a [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) y pasando un puntero a la interfaz .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msoe.dll</dt> </dl>    |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IConnectionPoint**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 
