---
title: Método Rename de la Win32_Terminal clase
description: El método Rename cambia el nombre del terminal.
ms.assetid: 85b5c83b-8ca3-4ed0-852b-b11ba98c18a6
ms.tgt_platform: multiple
keywords:
- Cambiar nombre del método Servicios de Escritorio remoto
- Método Rename Servicios de Escritorio remoto , Win32_Terminal clase
- Win32_Terminal clase Servicios de Escritorio remoto , Método Rename
topic_type:
- apiref
api_name:
- Win32_Terminal.Rename
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 502c4ec711458d7551662ad071ecd0de71874920437068396a9b5daebf58200d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868005"
---
# <a name="rename-method-of-the-win32_terminal-class"></a>Método Rename de la clase Terminal win32 \_

El **método Rename** cambia el nombre del terminal.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Rename(
  [in] string NewTerminalName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewTerminalName* \[ En\]
</dt> <dd>

Nuevo nombre del terminal.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ Terminal**](win32-terminal.md)
</dt> </dl>

 

