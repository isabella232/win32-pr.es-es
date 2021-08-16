---
title: Función DsRestoreGetDatabaseLocations (Ntdsbcli.h)
description: Obtiene las ubicaciones donde se deben copiar los archivos de copia de seguridad durante una operación de restauración.
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- Función DsRestoreGetDatabaseLocations Active Directory
topic_type:
- apiref
api_name:
- DsRestoreGetDatabaseLocations
- DsRestoreGetDatabaseLocationsA
- DsRestoreGetDatabaseLocationsW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c5626e2e0dc679a4669bb5d8be8096b6ae0629aeed7c833f397b5f9bca45db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118429997"
---
# <a name="dsrestoregetdatabaselocations-function"></a>Función DsRestoreGetDatabaseLocations

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [Servicio de instantáneas de volumen (VSS) en](../vss/volume-shadow-copy-service-overview.md) su lugar.\]

La **función DsRestoreGetDatabaseLocations** obtiene las ubicaciones donde se deben copiar los archivos de copia de seguridad durante una operación de restauración.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsRestoreGetDatabaseLocations(
  _In_  HBC     hbc,
  _Out_ LPWSTR  *pszDatabaseLocationList,
  _Out_ LPDWORD pcbSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hbc* \[ En\]
</dt> <dd>

Contiene el identificador de contexto de restauración obtenido con la [**función DsRestorePrepare.**](dsrestoreprepare.md)

</dd> <dt>

*pszDatabaseLocationList* \[ out\]
</dt> <dd>

Puntero a un puntero de cadena que recibe la lista de ubicaciones de base de datos como rutas de acceso UNC. Esta lista recibe una lista doble terminada en NULL de cadenas terminadas en null únicas.

La función **DsRestoreGetDatabaseLocations** asigna este búfer y se debe liberar cuando ya no sea necesario mediante una llamada a la función [**DsBackupFree.**](dsbackupfree.md)

El primer carácter de cada uno de los nombres de archivo contiene una de las constantes [**de BFT**](bft-constants.md) que identifica el tipo de nombre. La **función DsRestoreGetDatabaseLocations** solo proporciona los siguientes tipos de nombre.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ NTDS \_ DATABASE**


</dt> <dd>

El archivo de base de datos NTDS debe copiarse en este archivo. Este es el archivo que se identificó como **BFT \_ NTDS \_ DATABASE** cuando se realizó la copia de seguridad.

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT \_ LOG \_ DIR**


</dt> <dd>

Todos los archivos de registro se copian en este directorio. Los archivos de registro se identificaron como **BFT \_ LOG** cuando se realizó la copia de seguridad.

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**DIRECTORIO DE PUNTO DE COMPROBACIÓN DE BFT \_ \_**


</dt> <dd>

Todos los archivos de revisión se copian en este directorio. Los archivos de revisión se identificaron como **BFT \_ PATCH FILE \_ cuando** se realizó la copia de seguridad.

</dd> </dl> </dd> <dt>

*sizesize* \[ out\]
</dt> <dd>

Puntero al **valor DWORD** que recibe el tamaño, en bytes, del *búfer pszDatabaseLocationList.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** la función se realiza correctamente o un código de error win32 o RPC en caso contrario. En la lista siguiente se enumeran los posibles códigos de error.

<dl> <dt>

**ACCESO DE ERROR \_ \_ DENEGADO**
</dt> <dd>

El autor de la llamada no tiene los privilegios de acceso adecuados para llamar a esta función. La [**función DsSetAuthIdentity**](dssetauthidentity.md) se puede usar para establecer las credenciales que se usarán para las funciones de copia de seguridad y restauración.

</dd> <dt>

**ERROR \_ PARÁMETRO NO \_ VÁLIDO**
</dt> <dd>

*hbc,* *pszDatabaseLocationList* o *hbSize* no son válidos.

</dd> <dt>

**ERROR \_ NO HAY SUFICIENTE \_ \_ MEMORIA**
</dt> <dd>

Se produjo un error de asignación de memoria.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **función DsRestoreGetDatabaseLocations** se puede usar para obtener los directorios de restauración sin acceso a los datos de copia de seguridad. Para ello, llame a [**DsRestorePrepare**](dsrestoreprepare.md) con **NULL para** el *parámetro pvExpiryToken.* Esto hace **que DsRestorePrepare** devuelva un identificador de contexto restringido que solo se puede usar con la función **DsRestoreGetDatabaseLocations.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                        |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>                 |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl>               |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>               |
| Nombres Unicode y ANSI<br/>   | **DsRestoreGetDatabaseLocationsW** (Unicode) y **DsRestoreGetDatabaseLocationsA** (ANSI)<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> <dt>

[Restauración de Active Directory](restoring-an-active-directory-server.md)
</dt> </dl>

 

