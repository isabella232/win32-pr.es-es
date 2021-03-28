---
description: Desusado. Recupera la clave del registro que corresponde a esta identidad de usuario.
ms.assetid: eecf8b73-e86a-4274-8d9c-c601153f81db
title: 'IUserIdentity:: OpenIdentityRegKey (método) (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.OpenIdentityRegKey
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f1d67918f4a9802e63682e0663994c1ea6a06200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984607"
---
# <a name="iuseridentityopenidentityregkey-method"></a>IUserIdentity:: OpenIdentityRegKey (método)

\[El método **IUserIdentity:: OpenIdentityRegKey** está disponible para su uso en Windows 2000. En Windows XP, esta funcionalidad se ha sustituido por [las cuentas de usuario con cambio rápido de usuario y escritorio remoto](fastuserswitching.md), y puede modificarse o no estar disponible en las versiones posteriores.\]

En desuso. Recupera la clave del registro que corresponde a esta identidad de usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OpenIdentityRegKey(
  [in]  DWORD dwDesiredAccess,
  [out] HKEY  *phKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwDesiredAccess* \[ de\]
</dt> <dd>

Tipo: **DWORD**

Valor que describe el nivel de acceso solicitado de la clave del registro.

</dd> <dt>

*phKey* \[ enuncia\]
</dt> <dd>

Tipo: **HKEY \** _

Puntero que recibe la clave del registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Resultado de la solicitud del registro. Si se realiza correctamente, devuelve **S \_ correcto**. De lo contrario, devolverá uno de los siguientes códigos de error.



| Código devuelto                                                                                            | Descripción                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**identidad de E \_ \_ no \_ encontrada**</dt> </dl> | Esta identidad no tiene una clave del registro asociada.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                 | No se pudo obtener acceso a la clave del registro.<br/>             |



 

## <a name="remarks"></a>Observaciones

El parámetro *dwDesiredAccess* es un descriptor de seguridad de acceso al registro estándar que describe el acceso que se desea obtener a la clave del registro. Para obtener más información sobre la seguridad del registro, incluida una lista de valores aceptables para este parámetro, consulte [derechos de acceso y seguridad de la clave del registro](../sysinfo/registry-key-security-and-access-rights.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity::GetIdentityFolder**](iuseridentity-getidentityfolder.md)
</dt> </dl>

 

 
