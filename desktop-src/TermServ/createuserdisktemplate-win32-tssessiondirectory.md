---
title: Método CreateUserDiskTemplate de la clase Win32_TSSessionDirectory
description: Crea una plantilla de disco de usuario.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- Método CreateUserDiskTemplate Servicios de Escritorio remoto
- Método CreateUserDiskTemplate Servicios de Escritorio remoto, clase Win32_TSSessionDirectory
- Win32_TSSessionDirectory de clase Servicios de Escritorio remoto, método CreateUserDiskTemplate
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.CreateUserDiskTemplate
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c142834b4501639499cd0bcf102dadcc1b07d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150002"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a>Método CreateUserDiskTemplate de la \_ clase TSSessionDirectory de Win32

Crea una plantilla de disco de usuario.

## <a name="syntax"></a>Sintaxis


```mof
uint32 CreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UserDisksStorageUrl* \[ de\]
</dt> <dd>

La ubicación del recurso compartido donde se almacenan todos los discos de usuario.

</dd> <dt>

*UserDiskMaxSizeInGB* \[ de\]
</dt> <dd>

El tamaño máximo en gigabytes, para todos los discos de usuario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

 





