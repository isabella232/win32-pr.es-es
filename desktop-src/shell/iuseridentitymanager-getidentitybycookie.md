---
description: GetIdentityByCookie no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use Cuentas de usuario con cambio rápido de usuario y Escritorio remoto.
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: Método IUserIdentityManager::GetIdentityByCookie (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.GetIdentityByCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: a077f3e6a65a04e4c018198dde39b80c5a6e5acbee282c9e2cc282642526894b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678159"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a>IUserIdentityManager::GetIdentityByCookie (método)

\[**GetIdentityByCookie** no se admite y puede modificarse o no estar disponible en el futuro. En su lugar, use [cuentas de usuario con cambio rápido de usuario y Escritorio remoto](fastuserswitching.md).\]

Obtiene una identidad de usuario específica por la cookie que se usa para identificarla de forma única.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetIdentityByCookie(
  [in]  GUID          *uidCookie,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uidCookie* \[ En\]
</dt> <dd>

Tipo: **\* GUID**

Dirección de un **valor GUID** que representa la cookie de la identidad que desea recuperar.

</dd> <dt>

*ppIdentity* \[ out\]
</dt> <dd>

Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***

Dirección del puntero que recibirá el objeto de identidad del usuario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Resultado de la solicitud de recuperación. Si se realiza correctamente, devuelve S \_ OK. De lo contrario, devolverá uno de los siguientes códigos de error.



| Código devuelto                                                                                            | Descripción                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**E \_ IDENTITY \_ NOT \_ FOUND**</dt> </dl> | No se encontró la identidad solicitada.<br/>     |
| <dl> <dt>**IDENTIDADES \_ E \_ DESHABILITADAS**</dt> </dl> | La administración de identidades está deshabilitada en el sistema.<br/> |



 

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



 

 




