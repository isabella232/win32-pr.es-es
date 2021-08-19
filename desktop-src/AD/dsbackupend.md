---
title: Función DsBackupEnd (Ntdsbcli.h)
description: Se llama para finalizar una operación de copia de seguridad.
ms.assetid: 872645bc-3dbe-4b12-af4f-778d54feb18f
ms.tgt_platform: multiple
keywords:
- Función DsBackupEnd Active Directory
topic_type:
- apiref
api_name:
- DsBackupEnd
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479a1641a6d347837733da7e7d26e67b2011654e638681ec774a6ec5d931e211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430255"
---
# <a name="dsbackupend-function"></a>Función DsBackupEnd

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir Windows Vista, use [Servicio de instantáneas de volumen (VSS) en](../vss/volume-shadow-copy-service-overview.md) su lugar.\]

Se **llama a la función DsBackupEnd** para finalizar una operación de copia de seguridad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsBackupEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hbc* \[ En\]
</dt> <dd>

Contiene el identificador de contexto de copia de seguridad obtenido con la [**función DsBackupPrepare.**](dsbackupprepare.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** la función es correcta o un código de error de Win32 o RPC en caso contrario. En la lista siguiente se enumeran otros códigos de error posibles.

<dl> <dt>

**ERROR \_ PARÁMETRO NO \_ VÁLIDO**
</dt> <dd>

*hbc* no es válido.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **función DsBackupEnd** cierra los identificadores de enlace pendientes y realiza una limpieza después de un intento de copia de seguridad correcto o fallido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Copia de seguridad de un Active Directory servidor](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

