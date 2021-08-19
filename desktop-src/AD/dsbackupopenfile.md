---
title: Función DsBackupOpenFile (Ntdsbcli.h)
description: Abre el archivo especificado y realiza las operaciones de cliente y servidor necesarias para preparar el archivo para la copia de seguridad.
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- Función DsBackupOpenFile Active Directory
topic_type:
- apiref
api_name:
- DsBackupOpenFile
- DsBackupOpenFileA
- DsBackupOpenFileW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6331dc79a93e515d49c688bc8c5dd3b9e747cfbac91ace9c7685a219ae21e95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430017"
---
# <a name="dsbackupopenfile-function"></a>Función DsBackupOpenFile

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [Servicio de instantáneas de volumen (VSS) en](../vss/volume-shadow-copy-service-overview.md) su lugar.\]

La **función DsBackupOpenFile** abre el archivo especificado y realiza las operaciones de cliente y servidor necesarias para preparar el archivo para la copia de seguridad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsBackupOpenFile(
  _In_  HBC           hbc,
  _In_  LPCTSTR       szAttachmentName,
  _In_  DWORD         cbReadHintSize,
  _Out_ LARGE_INTEGER *pliFileSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hbc* \[ En\]
</dt> <dd>

Contiene el identificador de contexto de copia de seguridad obtenido con la [**función DsBackupPrepare.**](dsbackupprepare.md)

</dd> <dt>

*szAttachmentName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que especifica el nombre del archivo de copia de seguridad que se abrirá.

</dd> <dt>

*cbReadHintSize* \[ En\]
</dt> <dd>

Contiene el tamaño posible, en bytes, del búfer pasado como argumento *pvBuffer* en la [**función DsBackupRead.**](dsbackupread.md) Las funciones de copia de seguridad usan este valor como sugerencia para optimizar el tráfico de red. Este valor debe ser un múltiplo de 8192 y debe ser mayor o igual que 24576.

</dd> <dt>

*licaFileSize* \[ out\]
</dt> <dd>

Puntero a un **valor \_ INTEGER GRANDE** que recibe el tamaño, en bytes, del archivo de copia de seguridad abierto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** la función se realiza correctamente o un código de error win32 o RPC en caso contrario. En la lista siguiente se enumeran otros códigos de error posibles.

<dl> <dt>

**ACCESO DE ERROR \_ \_ DENEGADO**
</dt> <dd>

El autor de la llamada no tiene los privilegios de acceso adecuados para llamar a esta función. La [**función DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.

</dd> <dt>

**ERROR \_ PARÁMETRO NO \_ VÁLIDO**
</dt> <dd>

*hbc,* *szAttachmentName* o *pliFileSize* no son válidos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DsBackupOpenFileW** (Unicode) y **DsBackupOpenFileA** (ANSI)<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DsBackupRead**](dsbackupread.md)
</dt> <dt>

[Copia de seguridad de un Active Directory servidor](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

