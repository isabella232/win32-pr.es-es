---
title: Método CreateUserDiskTemplate de la Win32_TSSessionDirectory clase
description: Crea una plantilla de disco de usuario.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- Método CreateUserDiskTemplate Servicios de Escritorio remoto
- Método CreateUserDiskTemplate Servicios de Escritorio remoto , Win32_TSSessionDirectory clase
- Win32_TSSessionDirectory clase Servicios de Escritorio remoto , método CreateUserDiskTemplate
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
ms.openlocfilehash: cdc16d293f901efb6fc684d03ec7b47aa7496120c462a32414c747d15c02810a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120010235"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a>Método CreateUserDiskTemplate de la clase TSSessionDirectory de Win32 \_

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

*UserDisksStorageUrl* \[ En\]
</dt> <dd>

Ubicación del recurso compartido donde se almacenan todos los discos de usuario.

</dd> <dt>

*UserDiskMaxSizeInGB* \[ En\]
</dt> <dd>

Tamaño máximo en gigabytes para todos los discos de usuario.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md)
</dt> </dl>

 

 





