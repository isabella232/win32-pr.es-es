---
description: IUserIdentity2 no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use Cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: Interfaz IUserIdentity2 (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: a1a23ea6e0d5832ee6d78453f3a246b9db749c0d7b24b90a2199a7e8cfd225b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720591"
---
# <a name="iuseridentity2-interface"></a>Interfaz IUserIdentity2

\[**IUserIdentity2** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, [use cuentas de usuario con cambio rápido de usuario y Escritorio remoto](fastuserswitching.md).\]

Expone métodos que proporcionan nomenclatura, contraseña y control ordinal para una identidad de usuario específica.

## <a name="members"></a>Miembros

La **interfaz IUserIdentity2** hereda de [**IUserIdentity.**](iuseridentity.md) **IUserIdentity2** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IUserIdentity2** tiene estos métodos.



| Método                                                  | Descripción                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**ChangePassword**](iuseridentity2-changepassword.md) | En desuso. Establece una nueva contraseña para la identidad.<br/>      |
| [**GetOrdinal**](iuseridentity2-getordinal.md)         | En desuso. Obtiene el número ordinal de esta identidad.<br/> |
| [**SetName**](iuseridentity2-setname.md)               | En desuso. Establece el nombre para mostrar de la identidad.<br/>     |



 

## <a name="remarks"></a>Observaciones

Esta interfaz también proporciona los métodos de la [**interfaz IUserIdentity,**](iuseridentity.md) de la que hereda.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows 2000 Professional<br/>                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> </dl>

 

 




