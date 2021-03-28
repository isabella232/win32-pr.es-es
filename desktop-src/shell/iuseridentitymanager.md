---
description: IUserIdentityManager no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 3d24b858-bbaf-455c-83cd-3f6f93aba2a8
title: Interfaz IUserIdentityManager (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d0d00399e0ba958ef63c5e6597eb4a34387f92f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907557"
---
# <a name="iuseridentitymanager-interface"></a>Interfaz IUserIdentityManager

\[**IUserIdentityManager** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]

Expone métodos que identifican, enumeran y administran identidades de usuario en el sistema.

## <a name="members"></a>Miembros

La interfaz **IUserIdentityManager** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUserIdentityManager** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IUserIdentityManager** tiene estos métodos.



| Método                                                                  | Descripción                                                                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumIdentities**](iuseridentitymanager-enumidentities.md)           | En desuso. Obtiene un objeto [**IEnumUserIdentity**](ienumuseridentity.md) , que se puede utilizar para enumerar las identidades de usuario presentes en el sistema.<br/> |
| [**GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md) | En desuso. Obtiene una identidad de usuario específica por la cookie usada para identificarla de forma única.<br/>                                                                        |
| [**Forzado**](iuseridentitymanager-logoff.md)                           | En desuso. Cierre la sesión actual.<br/>                                                                                                                    |
| [**Expire**](iuseridentitymanager-logon.md)                             | En desuso. Muestra una interfaz de usuario para el usuario, lo que permite al usuario elegir una identidad de usuario. Si se realiza correctamente, la identidad del usuario se iniciará y se recuperará.<br/>        |
| [**ManageIdentities**](iuseridentitymanager-manageidentities.md)       | En desuso. Muestra una interfaz de usuario para el usuario, lo que permite al usuario administrar las identidades de usuario.<br/>                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows 2000 Server<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IIdentityChangeNotify**](iidentitychangenotify.md)
</dt> </dl>

 

 
