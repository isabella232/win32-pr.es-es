---
title: Función DsBackupOpenFile (Ntdsbcli. h)
description: Abre el archivo especificado y realiza las operaciones de cliente y servidor necesarias para preparar el archivo para la copia de seguridad.
ms.assetid: 1ffb81ee-9e7e-4d88-91fc-f1857377d125
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupOpenFile
topic_type:
- apiref
api_name:
- DsBackupOpenFile
- DsBackupOpenFileA
- DsBackupOpenFileW
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f9c4eac9c9825f510848583d7f707a2c244c52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150411"
---
# <a name="dsbackupopenfile-function"></a>DsBackupOpenFile función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]

La función **DsBackupOpenFile** abre el archivo especificado y realiza las operaciones de cliente y servidor necesarias para preparar el archivo para la copia de seguridad.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsBackupOpenFile(
  _In_  HBC           hbc,
  _In_  LPCTSTR       szAttachmentName,
  _In_  DWORD         cbReadHintSize,
  _Out_ LARGE_INTEGER *pliFileSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HBC* \[ de\]
</dt> <dd>

Contiene el identificador de contexto de copia de seguridad obtenido con la función [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> <dt>

*szAttachmentName* \[ de\]
</dt> <dd>

Puntero a una cadena terminada en null que especifica el nombre del archivo de copia de seguridad que se va a abrir.

</dd> <dt>

*cbReadHintSize* \[ de\]
</dt> <dd>

Contiene el tamaño posible, en bytes, del búfer pasado como el argumento *pvBuffer* en la función [**DsBackupRead**](dsbackupread.md) . Las funciones de copia de seguridad usan este valor como una sugerencia para optimizar el tráfico de red. Este valor debe ser un múltiplo de 8192 y debe ser mayor o igual que 24576.

</dd> <dt>

*pliFileSize* \[ enuncia\]
</dt> <dd>

Puntero a un **valor \_ entero grande** que recibe el tamaño, en bytes, del archivo de copia de seguridad abierto.

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

*HBC*, *szAttachmentName* o *pliFileSize* no son válidos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **DsBackupOpenFileW** (Unicode) y **DsBackupOpenFileA** (ANSI)<br/>             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DsBackupRead**](dsbackupread.md)
</dt> <dt>

[Copia de seguridad de un servidor Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

