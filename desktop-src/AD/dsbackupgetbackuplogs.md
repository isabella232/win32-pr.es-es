---
title: Función DsBackupGetBackupLogs (Ntdsbcli.h)
description: Obtiene la lista de archivos de registro de los que se debe realizar una copia de seguridad para el contexto de copia de seguridad especificado.
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- Función DsBackupGetBackupLogs Active Directory
topic_type:
- apiref
api_name:
- DsBackupGetBackupLogs
- DsBackupGetBackupLogsA
- DsBackupGetBackupLogsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d4a240ef514fc62450a04f512f04d985380b79fa20daaee9ff4b27ccb71027a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430123"
---
# <a name="dsbackupgetbackuplogs-function"></a>Función DsBackupGetBackupLogs

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [Servicio de instantáneas de volumen (VSS) en](../vss/volume-shadow-copy-service-overview.md) su lugar.\]

La **función DsBackupGetBackupLogs** obtiene la lista de archivos de registro de los que se debe realizar una copia de seguridad para el contexto de copia de seguridad especificado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsBackupGetBackupLogs(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszBackupLogFiles,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hbc* \[ En\]
</dt> <dd>

Contiene el identificador de contexto de copia de seguridad obtenido con la [**función DsBackupPrepare.**](dsbackupprepare.md)

</dd> <dt>

*pszBackupLogFiles* \[ out\]
</dt> <dd>

Puntero a un puntero de cadena que recibe la lista de nombres de archivo de registro como rutas de acceso UNC. Inicialice este valor **en NULL** antes de llamar a **DsBackupGetBackupLogs.**

Esta lista recibe una lista doble terminada en NULL de cadenas terminadas en null únicas.

La función **DsBackupGetBackupLogs** asigna este búfer y se debe liberar cuando ya no sea necesario mediante una llamada a la [**función DsBackupFree.**](dsbackupfree.md)

El primer carácter de cada uno de los nombres de archivo contiene una de las constantes [**de BFT**](bft-constants.md) que identifica el tipo de nombre.

</dd> <dt>

*sizesize* \[ out\]
</dt> <dd>

Puntero al **valor DWORD** que recibe el tamaño, en bytes, del búfer *pszBackupLogFiles.*

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

*hbc,* *pszBackupLogFiles* o *vhSize no* es válido.

</dd> <dt>

**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**
</dt> <dd>

Se produjo un error de asignación de memoria.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **función DsBackupGetBackupLogs proporciona** una lista de los archivos de registro necesarios para una copia de seguridad. Una copia de seguridad completa consta de los archivos de base de datos proporcionados por la función [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) y los archivos de registro. No se admiten copias de Active Directory incrementales de servidores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DsBackupGetBackupLogsW** (Unicode) y **DsBackupGetBackupLogsA** (ANSI)<br/>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md)
</dt> <dt>

[**Constantes de BFT**](bft-constants.md)
</dt> <dt>

[Copia de seguridad de un Active Directory servidor](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

