---
title: Función DsRestorePrepare (Ntdsbcli.h)
description: Se conecta al servidor de directorio especificado y lo prepara para la operación de restauración.
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- Función DsRestorePrepare Active Directory
topic_type:
- apiref
api_name:
- DsRestorePrepare
- DsRestorePrepareA
- DsRestorePrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f11b844919cc459788bbd8acda722a68344ae16807e45be9bd6dcd5780b09d6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191811"
---
# <a name="dsrestoreprepare-function"></a>Función DsRestorePrepare

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir Windows Vista, use [Servicio de instantáneas de volumen (VSS) en](../vss/volume-shadow-copy-service-overview.md) su lugar.\]

La **función DsRestorePrepare** se conecta al servidor de directorio especificado y lo prepara para la operación de restauración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsRestorePrepare(
  _In_  LPCWSTR szServerName,
  _In_  ULONG   rtFlag,
  _In_  PVOID   pvExpiryToken,
  _In_  DWORD   cbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szServerName* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene el nombre del servidor que se restaurará. Las barras diagonales inversas anteriores son opcionales. El servidor debe ser el mismo equipo desde el que se llama a esta función. El nombre del servidor no puede contener caracteres de subrayado ( \_ ). Un ejemplo de un nombre de servidor es \\ \\ "server1".

</dd> <dt>

*rtFlag* \[ En\]
</dt> <dd>

Especifica el tipo de restauración que se realizará. Puede ser cero o uno de los valores siguientes.

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**RESTORE \_ TYPE \_ CATCHUP**


</dt> <dd>

Predeterminada. La versión restaurada se concilia mediante la lógica de conciliación estándar para que el DIT restaurado pueda sincronizarse con otros equipos de servidor empresarial.

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**RESTORE \_ TYPE \_ AUTHORATATIVE**


</dt> <dd>

No compatible.

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**RESTORE \_ TYPE \_ ONLINE**


</dt> <dd>

No compatible. La restauración se realiza cuando NTDS está en línea.

</dd> </dl> </dd> <dt>

*pvExpiryToken* \[ En\]
</dt> <dd>

Puntero al token de expiración asociado a la copia de seguridad que se va a restaurar. Este token se obtuvo de la función [**DsBackupPrepare**](dsbackupprepare.md) cuando se escribió una copia de seguridad del directorio.

Si este parámetro es **NULL,** el identificador devuelto en *phbc* solo se puede usar para obtener los directorios de restauración con la función [**DsRestoreGetDatabaseLocations.**](dsrestoregetdatabaselocations.md) El identificador no se puede usar para ninguna otra función de restauración.

</dd> <dt>

*cbExpiryTokenSize* \[ En\]
</dt> <dd>

Contiene el tamaño, en bytes, del token de expiración en *pvExpiryToken.*

</dd> <dt>

*phbc* \[ out\]
</dt> <dd>

Puntero a un **valor HBC** que recibe el identificador para la restauración. Este identificador se usa al llamar a otras funciones de restauración del servicio de directorio, como [**DsBackupOpenFile**](dsbackupopenfile.md) y [**DsRestoreEnd.**](dsrestoreend.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se realiza correctamente, devuelve un código **HRESULT** estándar; De lo contrario, se devuelve un código de error.

## <a name="remarks"></a>Comentarios

La **función DsRestorePrepare** requiere que el autor de la llamada sea miembro del grupo Administradores del servidor.

**DsRestorePrepare** se puede usar con o sin un token proporcionado. Si se proporciona el token, se comprueba la expiración y se permiten todas las operaciones en el contexto devuelto. Si no se proporciona el token, el contexto devuelto está restringido y solo se puede usar para la función [**DsRestoreGetDatabaseLocations.**](dsrestoregetdatabaselocations.md) No se puede usar para la [**función DsRestoreRegister.**](dsrestoreregister.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DsRestorePrepareW** (Unicode) y **DsRestorePrepareA** (ANSI)<br/>             |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Restaurar un servidor Active Directory servidor](restoring-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**DsRestoreRegister**](dsrestoreregister.md)
</dt> <dt>

[**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md)
</dt> <dt>

[**DsRestoreEnd**](dsrestoreend.md)
</dt> </dl>

 

