---
title: Función DsBackupPrepare (Ntdsbcli.h)
description: Prepara el directorio en el servidor especificado para la copia de seguridad en línea y devuelve un identificador de contexto de copia de seguridad usado en llamadas posteriores a otras funciones de copia de seguridad.
ms.assetid: 18c6dbcf-b707-4674-9af5-40f2178e6d2b
ms.tgt_platform: multiple
keywords:
- Función DsBackupPrepare Active Directory
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
ms.openlocfilehash: ea1f24c6cbf3f05ce69d8a71900bfe4d1b08899b98590dc75410b9d5ed92d90a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191841"
---
# <a name="dsbackupprepare-function"></a>Función DsBackupPrepare

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir Windows Vista, use [Servicio de instantáneas de volumen (VSS) en](../vss/volume-shadow-copy-service-overview.md) su lugar.\]

La **función DsBackupPrepare** prepara el directorio en el servidor especificado para la copia de seguridad en línea y devuelve un identificador de contexto de copia de seguridad usado en llamadas posteriores a otras funciones de copia de seguridad.

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

*szBackupServer* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene el nombre del servidor del que se copia la copia de seguridad. Las barras diagonales inversas anteriores son opcionales. El servidor debe ser el mismo equipo desde el que se llama a esta función. El nombre del servidor no puede contener un carácter de subrayado ( \_ ). Un ejemplo de un nombre de servidor es \\ \\ "server1".

</dd> <dt>

*grbit* \[ En\]
</dt> <dd>

Determina si se realizará una copia de seguridad de los archivos de registro. Este valor siempre debe ser 0 porque no se admiten copias de seguridad incrementales.

</dd> <dt>

*btBackupType* \[ En\]
</dt> <dd>

Especifica el tipo de copia de seguridad. Puede ser uno de los siguientes valores.

<dt>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>

<span id="BACKUP_TYPE_FULL"></span><span id="backup_type_full"></span>**BACKUP \_ TYPE \_ FULL**


</dt> <dd>

Especifica una copia de seguridad completa. Se hace una copia de seguridad del directorio completo (DIT, archivos de registro y archivos de actualización). Se hace una copia de seguridad de todos los datos y se truncan los archivos de registro de transacciones. Solo se admiten copias de seguridad completas.

</dd> <dt>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>

<span id="BACKUP_TYPE_LOGS_ONLY"></span><span id="backup_type_logs_only"></span>**SOLO REGISTROS \_ DE TIPO DE COPIA DE \_ \_ SEGURIDAD**


</dt> <dd>

Este valor no se admite. Especifica que solo se realizará una copia de seguridad de los registros de la base de datos, y no de la propia base de datos. Esto se usa normalmente al realizar una copia de seguridad diferencial o incremental.

</dd> <dt>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>

<span id="BACKUP_TYPE_INCREMENTAL"></span><span id="backup_type_incremental"></span>**BACKUP \_ TYPE \_ INCREMENTAL**


</dt> <dd>

Este valor no se admite. **DsBackupPrepare devuelve** **ERROR INVALID \_ \_ PARAMETER**.

</dd> </dl> </dd> <dt>

*ppvExpiryToken* \[ out\]
</dt> <dd>

Puntero a un **valor PVOID** que recibe un puntero a un token de expiración asociado a esta copia de seguridad. *byteExpiryTokenSize* recibe el tamaño, en bytes, de estos datos. El autor de la llamada debe guardar el contenido de este token con la copia de seguridad porque el token debe pasarse a [**DsRestorePrepare**](dsrestoreprepare.md) al intentar restaurar los datos. Una vez que el token se ha almacenado y ya no es necesario, el autor de la llamada debe liberar la memoria asignada mediante [**DsBackupFree.**](dsbackupfree.md)

</dd> <dt>

*pwExpiryTokenSize* \[ out\]
</dt> <dd>

Puntero a un **valor DWORD** que recibe el tamaño, en bytes, del token en *ppvExpiryToken*.

</dd> <dt>

*phbc* \[ out\]
</dt> <dd>

Puntero a un **valor HBC** que recibe el identificador de la copia de seguridad. Este identificador se usa al llamar a otras funciones de copia de seguridad del servicio de directorio, como [**DsBackupOpenFile**](dsbackupopenfile.md) y [**DsBackupEnd.**](dsbackupend.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** la función es correcta o un código de error en caso contrario. En la lista siguiente se enumeran otros códigos de error posibles.

<dl> <dt>

**ERROR \_ DE ACCESO \_ DENEGADO**
</dt> <dd>

El autor de la llamada no tiene los privilegios de acceso adecuados para llamar a esta función. La [**función DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.

</dd> <dt>

**ERROR \_ PARÁMETRO NO \_ VÁLIDO**
</dt> <dd>

*szBackupServer* o *phbcBackupContext* no son válidos.

</dd> <dt>

**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**
</dt> <dd>

Error de asignación de memoria.

</dd> <dt>

**hrConnectldNotConnect**
</dt> <dd>

No se encontró el servidor de *szBackupServer,* no es un controlador de dominio o *szBackupServer* no tiene el formato correcto. Este valor se define en ntdsbmsg.h.

</dd> <dt>

**hrInvalidParam**
</dt> <dd>

*ppvExpiryToken* *oexpiryTokenSize* no son válidos. Este valor se define en Ntdsbmsg.h.

</dd> <dt>

**ENLACE \_ RPC S NO \_ \_ VÁLIDO**
</dt> <dd>

Se llama a la función de forma remota o el servidor de *szServerName* no es un controlador de dominio.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Esta función requiere que el autor de la llamada **tenga el SE BACKUP \_ \_ NAME.** La [**función DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para cambiar el contexto de seguridad bajo el que se llama a esta función.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DsBackupPrepareW** (Unicode) y **DsBackupPrepareA** (ANSI)<br/>               |



## <a name="see-also"></a>Consulte también

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

[Copia de seguridad de un Active Directory servidor](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

