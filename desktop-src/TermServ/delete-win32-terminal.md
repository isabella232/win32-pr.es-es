---
title: Método Delete de la Win32_Terminal clase
description: Elimina el terminal especificado.
ms.assetid: 59d8cc73-aef1-49d2-a7a2-dd3cbe5a8c52
ms.tgt_platform: multiple
keywords:
- Eliminar método Servicios de Escritorio remoto
- Método Delete Servicios de Escritorio remoto , Win32_Terminal clase
- Win32_Terminal clase Servicios de Escritorio remoto método , Delete
topic_type:
- apiref
api_name:
- Win32_Terminal.Delete
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47b7120c78eada2b047f836219d3382e5ce1e2f8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073350"
---
# <a name="delete-method-of-the-win32_terminal-class"></a>Método Delete de la clase Terminal Win32 \_

El **método** Delete elimina el terminal especificado.

## <a name="syntax"></a>Sintaxis


```mof
uint32 Delete(
  [in] string NewTerminalName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*NewTerminalName* \[ En\]
</dt> <dd>

Nombre del terminal que se eliminará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ Terminal**](win32-terminal.md)
</dt> </dl>

 

