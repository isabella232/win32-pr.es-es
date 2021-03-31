---
title: Función DsBackupGetBackupLogs (Ntdsbcli. h)
description: Obtiene la lista de archivos de registro de los que se debe hacer una copia de seguridad para el contexto de copia de seguridad dado.
ms.assetid: 09b3fdac-41ea-471c-a0dd-54414181f6fe
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupGetBackupLogs
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
ms.openlocfilehash: 4a02c5c7234810623a95dea030f0c623cca92293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996512"
---
# <a name="dsbackupgetbackuplogs-function"></a>DsBackupGetBackupLogs función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]

La función **DsBackupGetBackupLogs** obtiene la lista de archivos de registro de los que se debe hacer una copia de seguridad para el contexto de copia de seguridad determinado.

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

*HBC* \[ de\]
</dt> <dd>

Contiene el identificador de contexto de copia de seguridad obtenido con la función [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> <dt>

*pszBackupLogFiles* \[ enuncia\]
</dt> <dd>

Puntero a un puntero de cadena que recibe la lista de nombres de archivo de registro como rutas de acceso UNC. Inicialice este valor en **null** antes de llamar a **DsBackupGetBackupLogs**.

Esta lista recibe una lista de dos cadenas terminadas en NULL con un valor nulo.

Este búfer se asigna mediante la función **DsBackupGetBackupLogs** y se debe liberar cuando ya no se necesite llamando a la función [**DsBackupFree**](dsbackupfree.md) .

El primer carácter de cada uno de los nombres de archivo contiene una de las [**constantes BFT**](bft-constants.md) que identifica el tipo de nombre.

</dd> <dt>

*PCB* \[ enuncia\]
</dt> <dd>

Puntero al valor **DWORD** que recibe el tamaño, en bytes, del búfer *pszBackupLogFiles* .

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

*HBC*, *pszBackupLogFiles* o *PCB* no es válido.

</dd> <dt>

**ERROR \_ de \_ memoria insuficiente \_**
</dt> <dd>

Error de asignación de memoria.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función **DsBackupGetBackupLogs** proporciona una lista de los archivos de registro necesarios para una copia de seguridad. Una copia de seguridad completa consta de los archivos de base de datos proporcionados por la función [**DsBackupGetDatabaseNames**](dsbackupgetdatabasenames.md) y los archivos de registro. No se admiten copias de seguridad incrementales de servidores de Active Directory.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
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

[Copia de seguridad de un servidor Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

