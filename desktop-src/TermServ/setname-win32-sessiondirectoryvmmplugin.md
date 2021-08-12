---
title: Método SetName de la Win32_SessionDirectoryVMMPlugin clase
description: Establece el nombre del complemento.
ms.assetid: 8af4abca-f147-4027-91fb-4d669b58caa4
ms.tgt_platform: multiple
keywords:
- Método SetName Servicios de Escritorio remoto
- Método SetName Servicios de Escritorio remoto , Win32_SessionDirectoryVMMPlugin clase
- Win32_SessionDirectoryVMMPlugin clase Servicios de Escritorio remoto , método SetName
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetName
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6960d08f39e7ce026a36d1644bebf49aec292a44d900974ebd8481379b00dcf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604644"
---
# <a name="setname-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Método SetName de la clase \_ SessionDirectoryVMMPlugin de Win32

Establece el nombre del complemento.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetName(
  [in] string sName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sName* \[ En\]
</dt> <dd>

Nombre del complemento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ SessionDirectoryVMMPlugin**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





