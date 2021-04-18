---
description: IEnumUserIdentity no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: df4b6235-e66a-4187-b1f9-33c042cae2f2
title: Interfaz IEnumUserIdentity (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 48abf182942f90ecd477a241be3bf45323bdbdf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985411"
---
# <a name="ienumuseridentity-interface"></a>Interfaz IEnumUserIdentity

\[**IEnumUserIdentity** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]

Proporciona la enumeración de todas las identidades de usuario presentes en el sistema.

## <a name="members"></a>Miembros

La interfaz **IEnumUserIdentity** hereda de la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IEnumUserIdentity** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IEnumUserIdentity** tiene estos métodos.



| Método                                         | Descripción                                                                                                                  |
|:-----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**Clonar**](ienumuseridentity-clone.md)       | En desuso. Obtiene una copia de la enumeración actual.<br/>                                                               |
| [**GetCount**](ienumuseridentity-getcount.md) | En desuso. Obtiene el número de identidades de usuario actualmente en el sistema.<br/>                                            |
| [**Next**](ienumuseridentity-next.md)         | En desuso. Recupera una matriz de interfaces de identidad de usuario de la enumeración.<br/>                                  |
| [**Reset**](ienumuseridentity-reset.md)       | En desuso. Restablece el recuento interno de interfaces recuperadas en la enumeración.<br/>                                 |
| [**Omitir**](ienumuseridentity-skip.md)         | En desuso. Omite un número determinado de interfaces de identidad de usuario en la enumeración. Se utiliza al recuperar interfaces.<br/> |



 

## <a name="remarks"></a>Observaciones

Para recuperar información sobre las identidades de usuario presentes en el sistema, puede usar esta interfaz. Desde una interfaz [**IUserIdentityManager**](iuseridentitymanager.md) , puede llamar a [**IUserIdentityManager:: EnumIdentities**](iuseridentitymanager-enumidentities.md) para recuperar esta interfaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                  |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                         |
| Encabezado<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> </dl>

 

 
