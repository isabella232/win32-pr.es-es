---
title: Función DsBackupPrepare (Ntdsbcli. h)
description: Prepara el directorio en el servidor especificado para la copia de seguridad en línea y devuelve un identificador de contexto de copia de seguridad utilizado en llamadas posteriores a otras funciones de copia de seguridad.
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupPrepare
topic_type:
- apiref
api_name:
- DsBackupPrepare
- DsBackupPrepareA
- DsBackupPrepareW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa561a7e41164ece68fb18fd882a8b05d6357cec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491026"
---
# <a name="dsbackupprepare-function"></a>DsBackupPrepare función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]

La función **DsBackupPrepare** prepara el directorio en el servidor especificado para la copia de seguridad en línea y devuelve un identificador de contexto de copia de seguridad utilizado en llamadas posteriores a otras funciones de copia de seguridad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsBackupPrepare(
  _In_  LPCTSTR szBackupServer,
  _In_  ULONG   grbit,
  _In_  ULONG   btBackupType,
  _Out_ PVOID   *ppvExpiryToken,
  _Out_ LPDWORD pcbExpiryTokenSize,
  _Out_ HBC     *phbc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*szBackupServer* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que contiene el nombre del servidor del que se va a realizar la copia de seguridad. Las barras diagonales inversas anteriores son opcionales. El servidor debe ser el mismo equipo desde el que se llama a esta función. El nombre del servidor no puede contener un carácter de subrayado ( \_ ). Un ejemplo de un nombre de servidor es " \\ \\ server1".

</dd> <dt>

*grbit* \[ de\]
</dt> <dd>

Determina si se realizará una copia de seguridad de los archivos de registro. Este valor siempre debe ser 0, ya que no se admiten las copias de seguridad incrementales.

</dd> <dt>

*btBackupType* \[ de\]
</dt> <dd>

Especifica el tipo de copia de seguridad. Puede ser uno de los valores siguientes.

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**tipo de copia de seguridad \_ \_ completo**


</dt> <dd>

Especifica una copia de seguridad completa. Se realiza una copia de seguridad del directorio completo (DIT, archivos de registro y archivos de actualización). Se realiza una copia de seguridad de todos los datos y los archivos de registro de transacciones se truncan. Solo se admiten copias de seguridad completas.

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**\_ \_ solo registros de tipo de copia de seguridad \_**


</dt> <dd>

Este valor no se admite. Especifica que solo se hará una copia de seguridad de los registros de la base de datos, y no de la propia base de datos. Normalmente se utiliza cuando se realiza una copia de seguridad diferencial o incremental.

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**tipo de copia de seguridad \_ \_ incremental**


</dt> <dd>

Este valor no se admite. **DsBackupPrepare** devuelve **un \_ \_ parámetro de error no válido**.

</dd> </dl> </dd> <dt>

*ppvExpiryToken* \[ enuncia\]
</dt> <dd>

Puntero a un valor de **PVOID** que recibe un puntero a un token de expiración asociado a esta copia de seguridad. *pcbExpiryTokenSize* recibe el tamaño, en bytes, de estos datos. El autor de la llamada debe guardar el contenido de este token con la copia de seguridad porque el token se debe pasar a [**DsRestorePrepare**](dsrestoreprepare.md) al intentar restaurar los datos. Una vez que el token se ha almacenado y ya no es necesario, el llamador debe liberar la memoria asignada mediante [**DsBackupFree**](dsbackupfree.md).

</dd> <dt>

*pcbExpiryTokenSize* \[ enuncia\]
</dt> <dd>

Puntero a un valor **DWORD** que recibe el tamaño, en bytes, del token en *ppvExpiryToken*.

</dd> <dt>

*phbc* \[ enuncia\]
</dt> <dd>

Puntero a un valor de **HBC** que recibe el identificador de la copia de seguridad. Este identificador se usa al llamar a otras funciones de copia de seguridad del servicio de directorio, como [**DsBackupOpenFile**](dsbackupopenfile.md) y [**DsBackupEnd**](dsbackupend.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK** si la función es correcta o un código de error en caso contrario. En la lista siguiente se enumeran otros códigos de error posibles.

<dl> <dt>

**ERROR de \_ acceso \_ denegado**
</dt> <dd>

El autor de la llamada no dispone de los privilegios de acceso adecuados para llamar a esta función. La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.

</dd> <dt>

**ERROR \_ de \_ parámetro no válido**
</dt> <dd>

*szBackupServer* o *phbcBackupContext* no son válidos.

</dd> <dt>

**ERROR \_ de \_ memoria insuficiente \_**
</dt> <dd>

Error de asignación de memoria.

</dd> <dt>

**hrCouldNotConnect**
</dt> <dd>

No se encontró el servidor en *szBackupServer* , no es un controlador de dominio o *szBackupServer* no tiene el formato correcto. Este valor se define en ntdsbmsg. h.

</dd> <dt>

**hrInvalidParam**
</dt> <dd>

*ppvExpiryToken* y/o *pcbExpiryTokenSize* no son válidos. Este valor se define en Ntdsbmsg. h.

</dd> <dt>

**enlace de RPC \_ S \_ no válido \_**
</dt> <dd>

Se llama a la función de forma remota o el servidor de *szServerName* no es un controlador de dominio.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Esta función requiere que el autor de la llamada tenga el privilegio de **\_ \_ nombre de copia de seguridad** . La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para cambiar el contexto de seguridad en el que se llama a esta función.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DsBackupPrepareW** (Unicode) y **DsBackupPrepareA** (ANSI)<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupEnd**](dsbackupend.md)
</dt> <dt>

[**DsSetAuthIdentity**](dssetauthidentity.md)
</dt> <dt>

[Copia de seguridad de un servidor Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

