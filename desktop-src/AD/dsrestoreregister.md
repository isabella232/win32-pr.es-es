---
title: Función DsRestoreRegister (Ntdsbcli.h)
description: Registra una operación de restauración.
ms.assetid: 83a56985-89be-4a95-9a8d-7c6f78d61c9a
ms.tgt_platform: multiple
keywords:
- Función DsRestoreRegister Active Directory
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
ms.openlocfilehash: f3e878a5d2b9567ae7a483344a2240d3480620ea00706db1ed0c834fd2c5553a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962464"
---
# <a name="dsrestoreregister-function"></a>Función DsRestoreRegister

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir Windows Vista, use [Servicio de instantáneas de volumen (VSS) en](../vss/volume-shadow-copy-service-overview.md) su lugar.\]

La **función DsRestoreRegister** registra una operación de restauración. Esta función interbloquea todas las operaciones de restauración posteriores e impide que el destino de restauración se inicie hasta que se llame a la función [**DsRestoreRegisterComplete.**](dsrestoreregistercomplete.md)

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

*hbc* \[ En\]
</dt> <dd>

Contiene el identificador de contexto de restauración obtenido con la [**función DsRestorePrepare.**](dsrestoreprepare.md)

</dd> <dt>

*szCheckPointFilePath* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene la ruta de acceso al archivo de punto de comprobación. Esta ruta de acceso la proporciona la función [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) y tiene un **valor BFT** de DIR de punto de **\_ \_ comprobación de BFT.** Normalmente, esto es lo mismo que la ruta de acceso de la base de datos del sistema. Esta ruta de acceso es necesaria para la función de restauración de copia de seguridad adecuada. Este parámetro no puede ser **NULL.** Si **se pasa NULL** en este parámetro, se producirá un error durante el proceso de restauración.

</dd> <dt>

*szLogPath* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene la ruta de acceso donde se restaurarán los archivos de registro. Esta ruta de acceso la proporciona la función [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) y tiene un **valor BFT** de **BFT \_ LOG \_ DIR**. Si la ruta de acceso apunta a un directorio vacío, allí se crean nuevos archivos de registro. Este parámetro no puede ser **NULL.**

</dd> <dt>

*rgrstmap* \[ En\]
</dt> <dd>

Matriz de [**estructuras \_ RSTMAP de EDB**](edb-rstmap.md) que contiene las rutas de acceso antiguas y nuevas para cada base de datos. Hay una estructura para cada base de datos. Para el directorio , hay una estructura para la base de datos del sistema y otra estructura para la base de datos de directorios. El orden de los elementos de la matriz no importa. El *parámetro crstmap* contiene el número de elementos de la matriz.

</dd> <dt>

*crstmap* \[ En\]
</dt> <dd>

Contiene el número de elementos de la *matriz rgrstmap.*

</dd> <dt>

*szBackupLogPath* \[ En\]
</dt> <dd>

Puntero a una cadena terminada en NULL que contiene la ruta de acceso donde residen actualmente los archivos de registro de los que se ha hecho una copia de seguridad. Este parámetro no puede ser **NULL.**

</dd> <dt>

*genLow* \[ En\]
</dt> <dd>

Contiene el número de registro más bajo que se va a restaurar en esta sesión de restauración. Se trata de un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF.

</dd> <dt>

*genHigh* \[ En\]
</dt> <dd>

Contiene el número de registro más alto que se va a restaurar en esta sesión de restauración. Se trata de un número hexadecimal en el intervalo de 0x00000 a 0xFFFFF.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** la función es correcta o un código de error de Win32 o RPC en caso contrario. En la lista siguiente se enumeran los códigos de error posibles.

<dl> <dt>

**ERROR \_ DE ACCESO \_ DENEGADO**
</dt> <dd>

El autor de la llamada no tiene los privilegios de acceso adecuados para llamar a esta función. La [**función DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.

</dd> <dt>

**ERROR \_ PARÁMETRO NO \_ VÁLIDO**
</dt> <dd>

Uno o varios parámetros no son válidos.

</dd> <dt>

**hrMissingExpiryToken**
</dt> <dd>

El token de expiración proporcionado a [**DsRestorePrepare**](dsrestoreprepare.md) no era válido. Este valor se define en Ntdsbmsg.h.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DsRestoreRegisterW** (Unicode) y **DsRestoreRegisterA** (ANSI)<br/>           |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DsRestoreRegisterComplete**](dsrestoreregistercomplete.md)
</dt> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md)
</dt> <dt>

[**DsRestoreEnd**](dsrestoreend.md)
</dt> <dt>

[**\_RSTMAP de EDB**](edb-rstmap.md)
</dt> <dt>

[Restauración de Active Directory](restoring-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

