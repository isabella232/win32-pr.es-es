---
description: 'IUserIdentityManager:: EnumIdentities no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use cuentas de usuario con cambio rápido de usuario y Escritorio remoto.'
ms.assetid: 8111fbcd-dc4d-45cb-83e0-3c2cd7c4df27
title: 'IUserIdentityManager:: EnumIdentities (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.EnumIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 3109867651b69e311639d8b2e70e5f02e33a3dc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153604"
---
# <a name="iuseridentitymanagerenumidentities-method"></a>IUserIdentityManager:: EnumIdentities (método)

\[**IUserIdentityManager:: EnumIdentities** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md).\]

Obtiene un objeto [**IEnumUserIdentity**](ienumuseridentity.md) , que se puede utilizar para enumerar las identidades de usuario presentes en el sistema.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumIdentities(
  [out] IEnumUserIdentity **ppEnumUser
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnumUser* \[ enuncia\]
</dt> <dd>

Tipo: **[ **IEnumUserIdentity**](ienumuseridentity.md)\*\***

Dirección del puntero al nuevo objeto de enumeración de identidades.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Resultado de la operación de recuperación. Si se realiza correctamente, devuelve S \_ correcto. Si no se pudo crear el objeto de enumeración, devuelve E \_ OUTOFMEMORY.

## <a name="remarks"></a>Observaciones

Este método es útil para la iteración en la lista de identidades del sistema. Para recuperar una única identidad por su cookie sin tener acceso a la lista, llame a [**IUserIdentityManager:: GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md).

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

[**IUserIdentityManager**](iuseridentitymanager.md)
</dt> <dt>

[**IEnumUserIdentity**](ienumuseridentity.md)
</dt> <dt>

[**IUserIdentityManager::GetIdentityByCookie**](iuseridentitymanager-getidentitybycookie.md)
</dt> </dl>

 

 




