---
title: Función DsBackupRead (Ntdsbcli.h)
description: Lee un bloque de datos del archivo abierto actual en un búfer.
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- Función DsBackupRead Active Directory
topic_type:
- apiref
api_name:
- DsBackupRead
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16b5ea4da5b004bb4584eb119419b8c89658f36fed7e8c47514bae47d44e31b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430007"
---
# <a name="dsbackupread-function"></a>Función DsBackupRead

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [Servicio de instantáneas de volumen (VSS) en](../vss/volume-shadow-copy-service-overview.md) su lugar.\]

La **función DsBackupRead** lee un bloque de datos del archivo abierto actual en un búfer. Se espera que la aplicación cliente llame a esta función varias veces hasta que se reciba todo el archivo de copia de seguridad. La [**función DsBackupOpenFile**](dsbackupopenfile.md) proporciona el tamaño completo del archivo de copia de seguridad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsBackupRead(
  _In_  HBC    hbc,
  _In_  PVOID  pvBuffer,
  _In_  DWORD  cbBuffer,
  _Out_ PDWORD pcbRead
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hbc* \[ En\]
</dt> <dd>

Contiene el identificador de contexto de copia de seguridad obtenido con la [**función DsBackupPrepare.**](dsbackupprepare.md)

</dd> <dt>

*pvBuffer* \[ En\]
</dt> <dd>

Puntero a un búfer que recibe los datos. Este búfer debe tener al menos *bytes cbBuffer* de tamaño.

</dd> <dt>

*cbBuffer* \[ En\]
</dt> <dd>

Contiene el tamaño, en bytes, del búfer en *pvBuffer*. Este valor debe ser un múltiplo de 8192 y debe ser mayor o igual que 24576.

</dd> <dt>

*readread* \[ out\]
</dt> <dd>

Puntero a un **valor DWORD** que recibe el número real de bytes leídos. Esto puede ser menor que el número de bytes solicitado porque algunos transportes fragmentan el búfer que se transmite en lugar de rellenar todo el búfer con datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** la función se realiza correctamente o un código de error win32 o RPC en caso contrario. Entre los posibles códigos de error se incluyen los siguientes.

<dl> <dt>

**ERROR \_ PARÁMETRO NO \_ VÁLIDO**
</dt> <dd>

Uno o varios parámetros no son válidos.

</dd> <dt>

**EOF \_ DEL \_ IDENTIFICADOR DE ERROR**
</dt> <dd>

Se alcanzó el final del archivo de copia de seguridad.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[Hacer una copia de seguridad de Active Directory Server](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

