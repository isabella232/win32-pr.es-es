---
title: Función DsBackupRead (Ntdsbcli. h)
description: Lee un bloque de datos del archivo abierto actual, en un búfer.
ms.assetid: 01576d41-3cd6-4540-966b-7d98561f7b8c
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupRead
topic_type:
- apiref
api_name:
- DsBackupRead
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409c2a7d93503aad4edff88070c0458efc961d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996297"
---
# <a name="dsbackupread-function"></a>DsBackupRead función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]

La función **DsBackupRead** Lee un bloque de datos del archivo abierto actual, en un búfer. Se espera que la aplicación cliente llame a esta función repetidamente hasta que se haya recibido todo el archivo de copia de seguridad. La función [**DsBackupOpenFile**](dsbackupopenfile.md) proporciona el tamaño completo del archivo de copia de seguridad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsBackupRead(
  _In_  HBC    hbc,
  _In_  PVOID  pvBuffer,
  _In_  DWORD  cbBuffer,
  _Out_ PDWORD pcbRead
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HBC* \[ de\]
</dt> <dd>

Contiene el identificador de contexto de copia de seguridad obtenido con la función [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> <dt>

*pvBuffer* \[ de\]
</dt> <dd>

Puntero a un búfer que recibe los datos. Este búfer debe tener un tamaño mínimo de *cbBuffer* bytes.

</dd> <dt>

*cbBuffer* \[ de\]
</dt> <dd>

Contiene el tamaño, en bytes, del búfer en *pvBuffer*. Este valor debe ser un múltiplo de 8192 y debe ser mayor o igual que 24576.

</dd> <dt>

*pcbRead* \[ enuncia\]
</dt> <dd>

Puntero a un valor **DWORD** que recibe el número real de bytes leídos. Puede ser menor que el número de bytes solicitados porque algunos transportes fragmentan el búfer que se está transmitiendo en lugar de llenar todo el búfer con datos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario. Entre los posibles códigos de error se incluyen los siguientes.

<dl> <dt>

**ERROR \_ de \_ parámetro no válido**
</dt> <dd>

Uno o más parámetros no son válidos.

</dd> <dt>

**ERROR de \_ control de \_ EOF**
</dt> <dd>

Se alcanzó el final del archivo de copia de seguridad.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[**DsBackupFree**](dsbackupfree.md)
</dt> <dt>

[Copia de seguridad de un servidor Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

