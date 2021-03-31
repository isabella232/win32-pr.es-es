---
title: Función DsRestoreRegister (Ntdsbcli. h)
description: Registra una operación de restauración.
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsRestoreRegister
topic_type:
- apiref
api_name:
- DsRestoreRegister
- DsRestoreRegisterA
- DsRestoreRegisterW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 610d49c73ade9bab47c95e90af73bac606f4bd23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079491"
---
# <a name="dsrestoreregister-function"></a>DsRestoreRegister función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]

La función **DsRestoreRegister** registra una operación de restauración. Esta función bloquea todas las operaciones de restauración posteriores y evita que el destino de restauración se inicie hasta que se llame a la función [**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsRestoreRegister(
  _In_ HBC        hbc,
  _In_ LPCTSTR    szCheckPointFilePath,
  _In_ LPCTSTR    szLogPath,
  _In_ EDB_RSTMAP rgrstmap[],
  _In_ LONG       crstmap,
  _In_ LPCTSTR    szBackupLogPath,
  _In_ ULONG      genLow,
  _In_ ULONG      genHigh
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HBC* \[ de\]
</dt> <dd>

Contiene el identificador de contexto de restauración obtenido con la función [**DsRestorePrepare**](dsrestoreprepare.md) .

</dd> <dt>

*szCheckPointFilePath* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que contiene la ruta de acceso al archivo de punto de comprobación. La función [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) proporciona esta ruta de acceso y tiene un valor **BFT** de **BFT \_ Checkpoint \_ dir**. Normalmente, es igual que la ruta de acceso de la base de datos del sistema. Esta ruta de acceso es necesaria para la función de restauración de copia de seguridad adecuada. Este parámetro no puede ser **null**. Si se pasa **null** en este parámetro, se producirá un error durante el proceso de restauración.

</dd> <dt>

*szLogPath* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que contiene la ruta de acceso donde se restaurarán los archivos de registro. La función [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) proporciona esta ruta de acceso y tiene un valor **BFT** de **BFT \_ log \_ dir**. Si la ruta de acceso apunta a un directorio vacío, se crean nuevos archivos de registro. Este parámetro no puede ser **null**.

</dd> <dt>

*rgrstmap* \[ de\]
</dt> <dd>

Una matriz de estructuras [**EDB \_ RSTMAP**](edb-rstmap.md) que contiene las rutas de acceso antiguas y nuevas para cada base de datos. Hay una estructura para cada base de datos. En el directorio, existe una estructura para la base de datos del sistema y otra estructura para la base de datos de directorio. No importa el orden de los elementos de la matriz. El parámetro *crstmap* contiene el número de elementos de la matriz.

</dd> <dt>

*crstmap* \[ de\]
</dt> <dd>

Contiene el número de elementos de la matriz *rgrstmap* .

</dd> <dt>

*szBackupLogPath* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que contiene la ruta de acceso donde residen los archivos de registro de los que se ha realizado una copia de seguridad. Este parámetro no puede ser **null**.

</dd> <dt>

*genLow* \[ de\]
</dt> <dd>

Contiene el número de registro más bajo que se va a restaurar en esta sesión de restauración. Es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF.

</dd> <dt>

*genHigh* \[ de\]
</dt> <dd>

Contiene el número de registro más alto que se va a restaurar en esta sesión de restauración. Es un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario. En la lista siguiente se enumeran los posibles códigos de error.

<dl> <dt>

**ERROR de \_ acceso \_ denegado**
</dt> <dd>

El autor de la llamada no dispone de los privilegios de acceso adecuados para llamar a esta función. La función [**DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.

</dd> <dt>

**ERROR \_ de \_ parámetro no válido**
</dt> <dd>

Uno o más parámetros no son válidos.

</dd> <dt>

**hrMissingExpiryToken**
</dt> <dd>

El token de expiración proporcionado a [**DsRestorePrepare**](dsrestoreprepare.md) no era válido. Este valor se define en Ntdsbmsg. h.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DsRestoreRegisterW** (Unicode) y **DsRestoreRegisterA** (ANSI)<br/>           |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md)
</dt> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**DsRestoreEnd**](dsrestoreend.md)
</dt> <dt>

[**EDB \_ RSTMAP**](edb-rstmap.md)
</dt> <dt>

[Restauración de Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

