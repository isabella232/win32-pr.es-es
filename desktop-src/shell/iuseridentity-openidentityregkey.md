---
description: Desusado. Recupera la clave del Registro que corresponde a esta identidad de usuario.
ms.assetid: eecf8b73-e86a-4274-8d9c-c601153f81db
title: Método IUserIdentity::OpenIdentityRegKey (Msident.h)
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
ms.openlocfilehash: 89b80162b558222e1dc3e8caf518042ac90700ae7f7bde82b1b235111c9bdb43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117678439"
---
# <a name="iuseridentityopenidentityregkey-method"></a>IUserIdentity::OpenIdentityRegKey (método)

\[El **método IUserIdentity::OpenIdentityRegKey** está disponible para su uso en Windows 2000. En Windows XP, esta funcionalidad se ha reemplazado por cuentas de usuario con cambio rápido de usuario y [Escritorio remoto](fastuserswitching.md), y podría modificarse o no estar disponible en versiones posteriores.\]

En desuso. Recupera la clave del Registro que corresponde a esta identidad de usuario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT OpenIdentityRegKey(
  [in]  DWORD dwDesiredAccess,
  [out] HKEY  *phKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwDesiredAccess* \[ En\]
</dt> <dd>

Tipo: **DWORD**

Valor que describe el nivel de acceso solicitado de la clave del Registro.

</dd> <dt>

*phKey* \[ out\]
</dt> <dd>

Tipo: **HKEY \***

Puntero que recibe la clave del Registro.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Resultado de la solicitud del Registro. Si se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devolverá uno de los siguientes códigos de error.



| Código devuelto                                                                                            | Descripción                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**E \_ IDENTITY \_ NOT \_ FOUND**</dt> </dl> | Esta identidad no tiene una clave del Registro asociada.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                 | No se pudo acceder a la clave del Registro.<br/>             |



 

## <a name="remarks"></a>Comentarios

El *parámetro dwDesiredAccess es* un descriptor de seguridad de acceso al Registro estándar que describe el acceso que desea obtener a la clave del Registro. Para obtener más información sobre la seguridad del Registro, incluida una lista de valores aceptables para este parámetro, vea Derechos de acceso y seguridad de claves [del Registro.](../sysinfo/registry-key-security-and-access-rights.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Encabezado<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**IUserIdentity::GetIdentityFolder**](iuseridentity-getidentityfolder.md)
</dt> </dl>

 

 
