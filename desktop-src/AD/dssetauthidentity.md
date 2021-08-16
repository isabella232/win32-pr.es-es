---
title: Función DsSetAuthIdentity (Ntdsbcli.h)
description: Establece el contexto de seguridad en el que se llama a las API de copia de seguridad de directorios.
ms.assetid: bfa2f847-6fe3-4f9b-bafa-acf6a7c861d9
ms.tgt_platform: multiple
keywords:
- Función DsSetAuthIdentity Active Directory
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
ms.openlocfilehash: a8e4f990d1fa0c6a6a22b0068ea207be61b4aece441977b976f32f82b7b75c8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118695510"
---
# <a name="dssetauthidentity-function"></a>Función DsSetAuthIdentity

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [Servicio de instantáneas de volumen (VSS) en](../vss/volume-shadow-copy-service-overview.md) su lugar.\]

La **función DsSetAuthIdentity establece** el contexto de seguridad bajo el que se llama a las API de copia de seguridad de directorios.

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

*szUserName* \[ En\]
</dt> <dd>

Cadena terminada en NULL que especifica el nombre de usuario.

</dd> <dt>

*szDomainName* \[ En\]
</dt> <dd>

Cadena terminada en NULL que especifica el nombre del dominio al que pertenece el usuario.

</dd> <dt>

*szPassword* \[ En\]
</dt> <dd>

Cadena terminada en NULL que especifica la contraseña del usuario en el dominio especificado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, devuelve un **código HRESULT** estándar; De lo contrario, se devuelve un código de error.

## <a name="remarks"></a>Comentarios

Si **no se llama a DsSetAuthIdentity,** se supone el contexto de seguridad del proceso actual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DsSetAuthIdentityW** (Unicode) y **DsSetAuthIdentityA** (ANSI)<br/>           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Copia de seguridad y restauración de un servidor Active Directory servidor](backing-up-and-restoring-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

