---
title: Función DsBackupClose (Ntdsbcli.h)
description: Cierra un archivo de copia de seguridad abierto con la función DsBackupOpenFile.
ms.assetid: 5452a222-abe8-4d2d-84ff-6f577073b220
ms.tgt_platform: multiple
keywords:
- Función DsBackupClose Active Directory
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
ms.openlocfilehash: 00c9c8931d67b33fdad1f9e3605ee6efe801dac988d3931d96d1417561c093b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118192193"
---
# <a name="dsbackupclose-function"></a>Función DsBackupClose

\[Esta función está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En versiones posteriores podría modificarse o no estar disponible. A partir Windows Vista, use [Servicio de instantáneas de volumen (VSS) en](../vss/volume-shadow-copy-service-overview.md) su lugar.\]

La **función DsBackupClose** cierra un archivo de copia de seguridad abierto con la [**función DsBackupOpenFile.**](dsbackupopenfile.md) Para cada identificador de copia de seguridad, solo se puede abrir un archivo a la vez, por lo que esta función cierra el archivo abierto actualmente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DsBackupClose(
  _In_ HBC hbc
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hbc* \[ En\]
</dt> <dd>

Contiene el identificador de contexto de copia de seguridad obtenido con la [**función DsBackupPrepare.**](dsbackupprepare.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** la función es correcta o un código de error de Win32 o RPC en caso contrario. En la lista siguiente se enumeran otros códigos de error posibles.

<dl> <dt>

**ERROR \_ PARÁMETRO NO \_ VÁLIDO**
</dt> <dd>

*hbc* no es válido.

</dd> <dt>

**hrInvalidHandle**
</dt> <dd>

Actualmente no hay ningún archivo abierto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Ntdsbcli.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Ntdsbcli.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DsBackupOpenFile**](dsbackupopenfile.md)
</dt> <dt>

[**DsBackupPrepare**](dsbackupprepare.md)
</dt> <dt>

[Copia de seguridad de un Active Directory servidor](backing-up-an-active-directory-server.md)
</dt> <dt>

[Funciones de copia de seguridad de directorios](directory-backup-functions.md)
</dt> </dl>

 

