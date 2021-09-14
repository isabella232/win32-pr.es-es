---
title: Método SetHomeDirectory de la Win32_TerminalServiceSetting clase
description: Establece la propiedad TerminalServicesHomeDirectory para la clase .
ms.assetid: 8173cd5b-965e-41bc-97cf-70d8729b8cea
ms.tgt_platform: multiple
keywords:
- Método SetHomeDirectory Servicios de Escritorio remoto
- Método SetHomeDirectory Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método SetHomeDirectory
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetHomeDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be732cae76b0681afd77693a07f673ef37c4a12
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967951"
---
# <a name="sethomedirectory-method-of-the-win32_terminalservicesetting-class"></a>Método SetHomeDirectory de la clase \_ TerminalServiceSetting de Win32

El **método SetHomeDirectory** establece la **propiedad TerminalServicesHomeDirectory** para la clase .

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetHomeDirectory(
  [in] string HomeDirectory
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*HomeDirectory* \[ En\]
</dt> <dd>

Nuevo valor de la **propiedad TerminalServicesHomeDirectory,** que especifica el directorio raíz del equipo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve Success si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Para obtener una lista de códigos de error wmi, [vea Servicios de Escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md).

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> </dl>

 

