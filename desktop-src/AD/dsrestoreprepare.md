---
title: Función DsRestorePrepare (Ntdsbcli. h)
description: Conecta con el servidor de directorio especificado y lo prepara para la operación de restauración.
ms.assetid: e847d57a-32e1-49c0-800c-7ce0e5f442fa
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsRestorePrepare
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
ms.openlocfilehash: cb040a315b6cc94f2d296b032a954b00473a4ca2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150203"
---
# <a name="dsrestoreprepare-function"></a>DsRestorePrepare función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]

La función **DsRestorePrepare** se conecta al servidor de directorio especificado y lo prepara para la operación de restauración.

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

*szServerName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que contiene el nombre del servidor que se va a restaurar. Las barras diagonales inversas anteriores son opcionales. El servidor debe ser el mismo equipo desde el que se llama a esta función. El nombre del servidor no puede contener caracteres de subrayado ( \_ ). Un ejemplo de un nombre de servidor es " \\ \\ server1".

</dd> <dt>

*rtFlag* \[ de\]
</dt> <dd>

Especifica el tipo de restauración que se va a realizar. Puede ser cero o uno de los valores siguientes.

<dt>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>

<span id="RESTORE_TYPE_CATCHUP"></span><span id="restore_type_catchup"></span>**tipo de restauración \_ \_ puesta al día**


</dt> <dd>

Predeterminada. La versión restaurada se concilia a través de la lógica de conciliación estándar para que el DIT restaurado pueda sincronizarse con otros equipos de servidor de empresa.

</dd> <dt>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>

<span id="RESTORE_TYPE_AUTHORATATIVE"></span><span id="restore_type_authoratative"></span>**tipo de restauración \_ \_ AUTHORATATIVE**


</dt> <dd>

No compatible.

</dd> <dt>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>

<span id="RESTORE_TYPE_ONLINE"></span><span id="restore_type_online"></span>**tipo de restauración \_ \_ en línea**


</dt> <dd>

No compatible. La restauración se realiza cuando NTDS está en línea.

</dd> </dl> </dd> <dt>

*pvExpiryToken* \[ de\]
</dt> <dd>

Puntero al token de expiración asociado a la copia de seguridad que se está restaurando. Este token se obtuvo de la función [**DsBackupPrepare**](dsbackupprepare.md) cuando se realizó una copia de seguridad del directorio.

Si este parámetro es **null**, el identificador devuelto en *phbc* solo se puede usar para obtener los directorios de restauración con la función [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) . El identificador no se puede usar para otras funciones de restauración.

</dd> <dt>

*cbExpiryTokenSize* \[ de\]
</dt> <dd>

Contiene el tamaño, en bytes, del token de expiración en *pvExpiryToken*.

</dd> <dt>

*phbc* \[ enuncia\]
</dt> <dd>

Puntero a un valor de **HBC** que recibe el identificador de la restauración. Este identificador se usa al llamar a otras funciones de restauración del servicio de directorio, como [**DsBackupOpenFile**](dsbackupopenfile.md) y [**DsRestoreEnd**](dsrestoreend.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si es correcto, devuelve un código **HRESULT** estándar; de lo contrario, se devuelve un código de error.

## <a name="remarks"></a>Observaciones

La función **DsRestorePrepare** requiere que el autor de la llamada sea miembro del grupo administradores en el servidor.

**DsRestorePrepare** se puede usar con o sin un token proporcionado. Si se proporciona el token, se comprueba la expiración y se permiten todas las operaciones en el contexto devuelto. Si no se proporciona el token, el contexto devuelto es restringido y solo se puede usar para la función [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) . No se puede usar para la función [**DsRestoreRegister**](dsrestoreregister.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DsRestorePrepareW** (Unicode) y **DsRestorePrepareA** (ANSI)<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Restauración de un servidor de Active Directory](restoring-an-active-directory-server.md)
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

 

