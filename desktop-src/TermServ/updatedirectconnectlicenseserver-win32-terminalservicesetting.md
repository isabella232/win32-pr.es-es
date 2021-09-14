---
title: Método UpdateDirectConnectLicenseServer de la Win32_TerminalServiceSetting clase
description: UpdateDirectConnectLicenseServer ya no está disponible.
ms.assetid: 0b6e0dba-e23b-4c8d-8021-93d802501359
ms.tgt_platform: multiple
keywords:
- Método UpdateDirectConnectLicenseServer Servicios de Escritorio remoto
- Método UpdateDirectConnectLicenseServer Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método UpdateDirectConnectLicenseServer
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.UpdateDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2249dd00b44955a4e2712b8b7bf746793e89d57
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126967987"
---
# <a name="updatedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a>Método UpdateDirectConnectLicenseServer de la clase TerminalServiceSetting de Win32 \_

\[**UpdateDirectConnectLicenseServer** ya no está disponible para su uso a partir Windows Server 2008 R2.\]

**Windows Server 2008:** Actualiza la lista de servidores de licencias de detección. La lista de servidores está delimitada por punto y coma (";").

## <a name="syntax"></a>Sintaxis


```mof
uint32 UpdateDirectConnectLicenseServer(
  [in] string LicenseServerList
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*LicenseServerList* \[ En\]
</dt> <dd>

Lista de servidores de licencias.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Observaciones

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                                                               |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> </dl>

 

