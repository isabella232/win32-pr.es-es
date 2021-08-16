---
title: Función DsBackupGetDatabaseNames (Ntdsbcli.h)
description: Obtiene la lista de archivos de base de datos de los que se va a realizar una copia de seguridad para el contexto de copia de seguridad especificado.
ms.assetid: ba0447a1-38b0-4c0a-8c63-abaefb5b908f
ms.tgt_platform: multiple
keywords:
- Función DsBackupGetDatabaseNames Active Directory
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
ms.openlocfilehash: 620ad77f84aa2cb52a7bd99a96a22e7de560b53b2c3ba2022598609dde3737fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118191861"
---
# <a name="dsbackupgetdatabasenames-function"></a>Función DsBackupGetDatabaseNames

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [Servicio de instantáneas de volumen (VSS) en](../vss/volume-shadow-copy-service-overview.md) su lugar.\]

La **función DsBackupGetDatabaseNames** obtiene la lista de archivos de base de datos de los que se va a realizar una copia de seguridad para el contexto de copia de seguridad especificado.

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

*hbc* \[ En\]
</dt> <dd>

Contiene el identificador de contexto de copia de seguridad obtenido con la [**función DsBackupPrepare.**](dsbackupprepare.md)

</dd> <dt>

*pszAttachmentInfo* \[ out\]
</dt> <dd>

Puntero a un puntero de cadena que recibe la lista de nombres de archivo de base de datos como rutas de acceso UNC. Este valor debe inicializarse en **NULL antes** de llamar a **DsBackupGetDatabaseNames.**

Esta lista recibe una lista doble terminada en NULL de cadenas terminadas en null únicas.

La función **DsBackupGetDatabaseNames** asigna este búfer y se debe liberar cuando ya no sea necesario mediante una llamada a la función [**DsBackupFree.**](dsbackupfree.md)

El primer carácter de cada nombre de archivo contiene una de las [**constantes de BFT**](bft-constants.md) que identifica el tipo de nombre. La [**función DsRestoreGetDatabaseLocations**](dsrestoregetdatabaselocations.md) solo proporciona los siguientes tipos de nombres.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ NTDS \_ DATABASE**


</dt> <dd>

El archivo es un archivo de base de datos NTDS. Este archivo se debe copiar en el archivo identificado como **BFT \_ NTDS \_ DATABASE** cuando se restauran los datos.

</dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>

<span id="BFT_LOG"></span><span id="bft_log"></span>**BFT \_ LOG**


</dt> <dd>

El archivo es un archivo de registro. Todos los archivos de registro se copian en el directorio identificado como **BFT \_ LOG \_ DIR** cuando se restauran los datos.

</dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**ARCHIVO DE \_ REVISIÓN DE \_ BFT**


</dt> <dd>

El archivo es un archivo de revisión. Todos los archivos de revisión se copian en el directorio identificado como DIR de punto de comprobación **de BFT \_ \_** cuando se restauran los datos.

</dd> </dl> </dd> <dt>

*sizesize* \[ out\]
</dt> <dd>

Puntero al **valor DWORD** que recibe el tamaño, en bytes, del *búfer pszAttachmentInfo.*

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

*hbc,* *pszAttachmentInfo* o *vhSize* no son válidos.

</dd> <dt>

**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**
</dt> <dd>

Error de asignación de memoria.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **función DsBackupGetDatabaseNames** proporciona una lista de los archivos de base de datos necesarios para una copia de seguridad. Una copia de seguridad completa consta de los archivos de base de datos y los archivos de registro proporcionados por la [**función DsBackupGetBackupLogs.**](dsbackupgetbackuplogs.md) No se admiten copias de Active Directory incrementales de servidores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                              |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>       |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl>     |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>     |
| Nombres Unicode y ANSI<br/>   | **DsBackupGetDatabaseNamesW** (Unicode) y **DsBackupGetDatabaseNamesA** (ANSI)<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[**DsBackupGetBackupLogs**](dsbackupgetbackuplogs.md)
</dt> <dt>

[**Constantes de BFT**](bft-constants.md)
</dt> <dt>

[Hacer una copia de seguridad de Active Directory Server](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

