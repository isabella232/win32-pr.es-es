---
description: IEnumUserIdentity no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: df4b6235-e66a-4187-b1f9-33c042cae2f2
title: Interfaz IEnumUserIdentity (Msident.h)
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
ms.openlocfilehash: e5acab235abf16afd5659c091caa59190b05ab7d1b565d093a8902f0ede39026
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119821935"
---
# <a name="ienumuseridentity-interface"></a>IEnumUserIdentity (interfaz)

\[**IEnumUserIdentity** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, [use cuentas de usuario con cambio rápido de usuario Escritorio remoto](fastuserswitching.md).\]

Proporciona la enumeración de todas las identidades de usuario presentes en el sistema.

## <a name="members"></a>Miembros

La **interfaz IEnumUserIdentity** hereda de la [**interfaz IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IEnumUserIdentity** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IEnumUserIdentity** tiene estos métodos.



| Método                                         | Descripción                                                                                                                  |
|:-----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [**Clon**](ienumuseridentity-clone.md)       | En desuso. Obtiene una copia de la enumeración actual.<br/>                                                               |
| [**GetCount**](ienumuseridentity-getcount.md) | En desuso. Obtiene el recuento de identidades de usuario actualmente en el sistema.<br/>                                            |
| [**Next**](ienumuseridentity-next.md)         | En desuso. Recupera una matriz de interfaces de identidad de usuario de la enumeración .<br/>                                  |
| [**Restablecer**](ienumuseridentity-reset.md)       | En desuso. Restablece el recuento interno de interfaces recuperadas en la enumeración .<br/>                                 |
| [**Omitir**](ienumuseridentity-skip.md)         | En desuso. Omite un número determinado de interfaces de identidad de usuario en la enumeración . Se usa al recuperar interfaces.<br/> |



 

## <a name="remarks"></a>Comentarios

Para recuperar información sobre las identidades de usuario presentes en el sistema, puede usar esta interfaz. Desde una [**interfaz IUserIdentityManager,**](iuseridentitymanager.md) puede llamar a [**IUserIdentityManager::EnumIdentities**](iuseridentitymanager-enumidentities.md) para recuperar esta interfaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                   |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                  |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> </dl>

 

 
