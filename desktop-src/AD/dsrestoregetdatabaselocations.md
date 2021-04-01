---
title: Función DsRestoreGetDatabaseLocations (Ntdsbcli. h)
description: Obtiene las ubicaciones en las que se deben copiar los archivos de copia de seguridad durante una operación de restauración.
ms.assetid: f91d701c-72cf-418a-8d1c-6bf6ef41c2c1
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsRestoreGetDatabaseLocations
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
ms.openlocfilehash: 7bcebb9f3822332269e1db09f3246c128e4ad1f2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905410"
---
# <a name="dsrestoregetdatabaselocations-function"></a>DsRestoreGetDatabaseLocations función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]

La función **DsRestoreGetDatabaseLocations** obtiene las ubicaciones en las que se deben copiar los archivos de copia de seguridad durante una operación de restauración.

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

*HBC* \[ de\]
</dt> <dd>

Contiene el identificador de contexto de restauración obtenido con la función [**DsRestorePrepare**](dsrestoreprepare.md) .

</dd> <dt>

*pszDatabaseLocationList* \[ enuncia\]
</dt> <dd>

Puntero a un puntero de cadena que recibe la lista de ubicaciones de la base de datos como rutas UNC. Esta lista recibe una lista de dos cadenas terminadas en NULL con un valor nulo.

Este búfer se asigna mediante la función **DsRestoreGetDatabaseLocations** y se debe liberar cuando ya no es necesario llamando a la función [**DsBackupFree**](dsbackupfree.md) .

El primer carácter de cada uno de los nombres de archivo contiene una de las [**constantes BFT**](bft-constants.md) que identifica el tipo de nombre. La función **DsRestoreGetDatabaseLocations** solo proporciona los siguientes tipos de nombre.

<dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_base de \_ datos Ntds BFT**


</dt> <dd>

El archivo de base de datos NTDS debe copiarse en este archivo. Este es el archivo que se identificó como **BFT \_ NTDS \_ Database** cuando se realizó la copia de seguridad.

</dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**DIR. de registro de BFT \_ \_**


</dt> <dd>

Todos los archivos de registro se copian en este directorio. Los archivos de registro se identificaron como **\_ registro de BFT** cuando se realizó la copia de seguridad.

</dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**DIR. de punto de BFT \_ \_**


</dt> <dd>

Todos los archivos de revisión se copian en este directorio. Los archivos de revisión se identificaron como **\_ \_ archivo de revisión BFT** cuando se realizó la copia de seguridad.

</dd> </dl> </dd> <dt>

*PCB* \[ enuncia\]
</dt> <dd>

Puntero al valor **DWORD** que recibe el tamaño, en bytes, del búfer *pszDatabaseLocationList* .

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

*HBC*, *pszDatabaseLocationList* o *PCB* no son válidos.

</dd> <dt>

**ERROR \_ de \_ memoria insuficiente \_**
</dt> <dd>

Error de asignación de memoria.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La función **DsRestoreGetDatabaseLocations** se puede usar para obtener los directorios de restauración sin acceso a los datos de los que se ha realizado una copia de seguridad. Para ello, llame a [**DsRestorePrepare**](dsrestoreprepare.md) con **null** para el parámetro *pvExpiryToken* . Esto hace que **DsRestorePrepare** devuelva un identificador de contexto restringido que solo se puede usar con la función **DsRestoreGetDatabaseLocations** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                        |
| Encabezado<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>                 |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl>               |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl>               |
| Nombres Unicode y ANSI<br/>   | **DsRestoreGetDatabaseLocationsW** (Unicode) y **DsRestoreGetDatabaseLocationsA** (ANSI)<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DsRestorePrepare**](dsrestoreprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> <dt>

[Restauración de Active Directory](restoring-an-active-directory-server.md)
</dt> </dl>

 

