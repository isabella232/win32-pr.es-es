---
title: Función DsBackupClose (Ntdsbcli. h)
description: Cierra un archivo de copia de seguridad abierto con la función DsBackupOpenFile.
ms.assetid: 5452a222-abe8-4d2d-84ff-6f577073b220
ms.tgt_platform: multiple
keywords:
- Active Directory de la función DsBackupClose
topic_type:
- apiref
api_name:
- DsBackupClose
api_location:
- Ntdsbcli.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d03c9cd7f125d223d264236a52120714d5198c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490252"
---
# <a name="dsbackupclose-function"></a>DsBackupClose función)

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir de Windows Vista, use [servicio de instantáneas de volumen (VSS)](../vss/volume-shadow-copy-service-overview.md) en su lugar.\]

La función **DsBackupClose** cierra un archivo de copia de seguridad abierto con la función [**DsBackupOpenFile**](dsbackupopenfile.md) . Para cada identificador de copia de seguridad, solo se puede abrir un archivo cada vez, por lo que esta función cierra el archivo abierto actualmente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsBackupClose(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HBC* \[ de\]
</dt> <dd>

Contiene el identificador de contexto de copia de seguridad obtenido con la función [**DsBackupPrepare**](dsbackupprepare.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK** si la función es correcta o un código de error de Win32 o RPC en caso contrario. En la lista siguiente se enumeran otros códigos de error posibles.

<dl> <dt>

**ERROR \_ de \_ parámetro no válido**
</dt> <dd>

*HBC* no es válido.

</dd> <dt>

**hrInvalidHandle**
</dt> <dd>

No hay ningún archivo abierto actualmente.

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

[Copia de seguridad de un servidor Active Directory](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

