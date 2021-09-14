---
title: Método AddDirectConnectLicenseServer de la Win32_TerminalServiceSetting clase
description: AddDirectConnectLicenseServer ya no está disponible.
ms.assetid: 7920fd28-0fa3-4f96-bec3-d9e37c97920c
ms.tgt_platform: multiple
keywords:
- Método AddDirectConnectLicenseServer Servicios de Escritorio remoto
- Método AddDirectConnectLicenseServer Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método AddDirectConnectLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.AddDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9bba23f5c0bfc69b4c8d7951ab38eac6690b84
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967983"
---
# <a name="adddirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Método AddDirectConnectLicenseServer de la clase \_ TerminalServiceSetting de Win32

\[**AddDirectConnectLicenseServer** ya no está disponible para su uso a partir Windows Server 2008 R2.\]

**Windows Server 2008:** Configura un nuevo servidor de licencias y agrega el servidor de licencias al Registro para su detección Escritorio remoto de host de sesión (host de sesión de Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 AddDirectConnectLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LicenseServerName* \[ En\]
</dt> <dd>

Nombre del servidor de licencias que se agregará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las clases Windows Management Instrumentation (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                                                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> </dl>

 

