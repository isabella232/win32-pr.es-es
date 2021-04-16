---
title: Función DsSetAuthIdentity (Ntdsbcli. h)
description: Establece el contexto de seguridad en el que se llama a las API de copia de seguridad de directorio.
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsSetAuthIdentity
topic_type:
- apiref
api_name:
- DsSetAuthIdentity
- DsSetAuthIdentityA
- DsSetAuthIdentityW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40d973d5f818b4bd81278a1466487ae89ebf888f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491236"
---
# <a name="dssetauthidentity-function"></a>DsSetAuthIdentity función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]

La función **DsSetAuthIdentity** establece el contexto de seguridad en el que se llama a las API de copia de seguridad de directorio.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsSetAuthIdentity(
  _In_ LPCTSTR szUserName,
  _In_ LPCTSTR szDomainName,
  _In_ LPCTSTR szPassword
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szUserName* \[ de\]
</dt> <dd>

Cadena terminada en null que especifica el nombre de usuario.

</dd> <dt>

*szDomainName* \[ de\]
</dt> <dd>

Cadena terminada en null que especifica el nombre del dominio al que pertenece el usuario.

</dd> <dt>

*szPassword* \[ de\]
</dt> <dd>

Cadena terminada en null que especifica la contraseña del usuario en el dominio especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, devuelve un código de error **HRESULT** estándar; de lo contrario, se devuelve un código de error.

## <a name="remarks"></a>Observaciones

Si no se llama a **DsSetAuthIdentity** , se supone el contexto de seguridad del proceso actual.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DsSetAuthIdentityW** (Unicode) y **DsSetAuthIdentityA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Copia de seguridad y restauración de un servidor Active Directory](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

