---
title: Función DsBackupTruncateLogs (Ntdsbcli. h)
description: Trunca los registros de copia de seguridad previamente leídos.
ms.assetid: fae2e19f-08b8-410f-a735-dd4d41fc71a6
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupTruncateLogs
topic_type:
- apiref
api_name:
- DsBackupTruncateLogs
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 051ced828656c6b6e5af156e2d1a69c3b741cdce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534053"
---
# <a name="dsbackuptruncatelogs-function"></a>DsBackupTruncateLogs función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]

La función **DsBackupTruncateLogs** trunca los registros de copia de seguridad previamente leídos.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsBackupTruncateLogs(
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

**ERROR de \_ acceso \_ denegado**
</dt> <dd>

El autor de la llamada no dispone de los privilegios de acceso adecuados para llamar a esta función. La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.

</dd> <dt>

**ERROR \_ de \_ parámetro no válido**
</dt> <dd>

*HBC* no es válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Utilice la función **DsBackupTruncateLogs** cuando se haya completado correctamente una copia de seguridad completa o incremental.

> [!Caution]  
> Si se llama a esta función después de una copia de seguridad diferencial, se perderá toda la información de copia de seguridad incremental.

 

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

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**DsSetCurrentBackupLog**](dssetcurrentbackuplog.md)
</dt> <dt>

[Copia de seguridad de un servidor Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

