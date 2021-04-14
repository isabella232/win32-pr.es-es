---
description: IUserIdentity no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: c2f11f8b-f944-445b-b4fc-ac57b0fe3a74
title: Interfaz IUserIdentity (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 068d806086aff44db172a4a7b09f55b600204478
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985402"
---
# <a name="iuseridentity-interface"></a>Interfaz IUserIdentity

\[**IUserIdentity** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]

Expone métodos que proporcionan datos de identificación, registro y carpeta para una identidad de usuario específica.

## <a name="members"></a>Miembros

La interfaz **IUserIdentity** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IUserIdentity** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IUserIdentity** tiene estos métodos.



| Método                                                         | Descripción                                                                                      |
|:---------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**GetCookie**](iuseridentity-getcookie.md)                   | En desuso. Obtiene la cookie usada para identificar de forma única esta identidad de usuario.<br/>             |
| [**GetIdentityFolder**](iuseridentity-getidentityfolder.md)   | En desuso. Obtiene la carpeta de archivos asociada a esta identidad.<br/>                       |
| [**GetName**](iuseridentity-getname.md)                       | En desuso. Obtiene el nombre asociado a esta identidad de usuario.<br/>                         |
| [**OpenIdentityRegKey**](iuseridentity-openidentityregkey.md) | En desuso. Recupera la clave del registro que corresponde a esta identidad de usuario.<br/> |



 

## <a name="remarks"></a>Observaciones

Esta interfaz proporciona información que corresponde a una identidad de usuario específica presente en el sistema. Puede tener acceso a la carpeta de identidad de esta identidad de usuario, su clave del registro y su cookie de identificación, así como recuperar el nombre asociado a la identidad del usuario.

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

[**IUserIdentity2**](iuseridentity2.md)
</dt> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> </dl>

 

 
