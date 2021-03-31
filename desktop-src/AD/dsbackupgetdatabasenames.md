---
title: Función DsBackupGetDatabaseNames (Ntdsbcli. h)
description: Obtiene la lista de archivos de base de datos de la que se va a realizar una copia de seguridad para el contexto de copia de seguridad determinado.
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupGetDatabaseNames
topic_type:
- apiref
api_name:
- DsBackupGetDatabaseNames
- DsBackupGetDatabaseNamesA
- DsBackupGetDatabaseNamesW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6643b17a85727f6e0df4e8deea9609f73afd1e76
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491027"
---
# <a name="dsbackupgetdatabasenames-function"></a>DsBackupGetDatabaseNames función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]

La función **DsBackupGetDatabaseNames** obtiene la lista de archivos de base de datos de los que se va a realizar una copia de seguridad para el contexto de copia de seguridad determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsBackupGetDatabaseNames(
  _In_  HBC     hbc,
  _Out_ LPTSTR  *pszAttachmentInfo,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HBC* \[ de\]
</dt> <dd>

Contiene el identificador de contexto de copia de seguridad obtenido con la función [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> <dt>

*pszAttachmentInfo* \[ enuncia\]
</dt> <dd>

Puntero a un puntero de cadena que recibe la lista de nombres de archivo de base de datos como rutas de acceso UNC. Este valor se debe inicializar en **null** antes de llamar a **DsBackupGetDatabaseNames**.

Esta lista recibe una lista de dos cadenas terminadas en NULL con un valor nulo.

Este búfer se asigna mediante la función **DsBackupGetDatabaseNames** y se debe liberar cuando ya no es necesario llamando a la función [**DsBackupFree**](dsbackupfree.md) .

El primer carácter de cada nombre de archivo contiene una de las [**constantes BFT**](bft-constants.md) que identifica el tipo de nombre. La función [**DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) solo proporciona los siguientes tipos de nombres.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_base de \_ datos Ntds BFT**


</dt> <dd>

El archivo es un archivo de base de datos NTDS. Este archivo debe copiarse en el archivo identificado como **BFT \_ NTDS \_ Database** cuando se restauren los datos.

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span id="BFT_LOG"></span><span id="bft_log"></span>**registro de BFT \_**


</dt> <dd>

El archivo es un archivo de registro. Todos los archivos de registro se copian en el directorio identificado como **BFT de \_ registro de inicio de sesión \_** cuando se restauran los datos.

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_archivo de revisión BFT \_**


</dt> <dd>

El archivo es un archivo de revisión. Todos los archivos de revisión se copian en el directorio identificado como **BFT \_ Checkpoint \_ dir** cuando se restauran los datos.

</dd> </dl> </dd> <dt>

*PCB* \[ enuncia\]
</dt> <dd>

Puntero al valor **DWORD** que recibe el tamaño, en bytes, del búfer *pszAttachmentInfo* .

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

*HBC*, *pszAttachmentInfo* o *PCB* no son válidos.

</dd> <dt>

**ERROR \_ de \_ memoria insuficiente \_**
</dt> <dd>

Error de asignación de memoria.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función **DsBackupGetDatabaseNames** proporciona una lista de los archivos de base de datos necesarios para una copia de seguridad. Una copia de seguridad completa consta de los archivos de base de datos y los archivos de registro proporcionados por la función [**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md) . No se admiten copias de seguridad incrementales de servidores de Active Directory.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                              |
| Encabezado<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>     |
| Nombres Unicode y ANSI<br/>   | **DsBackupGetDatabaseNamesW** (Unicode) y **DsBackupGetDatabaseNamesA** (ANSI)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**Constantes de BFT**](bft-constants.md)
</dt> <dt>

[Copia de seguridad de un servidor Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

