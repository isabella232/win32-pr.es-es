---
title: Función DsBackupEnd (Ntdsbcli. h)
description: Se llama para finalizar una operación de copia de seguridad.
ms.assetid: 872645bc-3dbe-4b12-af4f-778d54feb18f
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupEnd
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
ms.openlocfilehash: 9663eedec7bc298ef594990baababcf2083546e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905183"
---
# <a name="dsbackupend-function"></a>DsBackupEnd función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]

Se llama a la función **DsBackupEnd** para finalizar una operación de copia de seguridad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsBackupEnd(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HBC* \[ de\]
</dt> <dd>

Contiene el identificador de contexto de copia de seguridad obtenido con la función [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario. En la lista siguiente se enumeran otros códigos de error posibles.

<dl> <dt>

**ERROR \_ de \_ parámetro no válido**
</dt> <dd>

*HBC* no es válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función **DsBackupEnd** cierra los identificadores de enlace pendientes y realiza una limpieza después de un intento de copia de seguridad correcto o incorrecto.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Copia de seguridad de un servidor Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

