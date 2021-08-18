---
title: Método ExplicitLogon de la Win32_TSLogonSetting clase
description: El método ExplicitLogon establece las credenciales que se usarán para la autenticación.
ms.assetid: cfd43396-0d66-4d5e-81c8-5c0e66422dc5
ms.tgt_platform: multiple
keywords:
- Método ExplicitLogon Servicios de Escritorio remoto
- Método ExplicitLogon Servicios de Escritorio remoto , Win32_TSLogonSetting clase
- Win32_TSLogonSetting clase Servicios de Escritorio remoto método , ExplicitLogon
topic_type:
- apiref
api_name:
- Win32_TSLogonSetting.ExplicitLogon
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7303f06967d26276c7b43e06109cd9b37d664b960946afdffbb4f6a5a7c18821
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119137788"
---
# <a name="explicitlogon-method-of-the-win32_tslogonsetting-class"></a>Método ExplicitLogon de la clase \_ TSLogonSetting de Win32

El **método ExplicitLogon** establece las credenciales que se usarán para la autenticación.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ExplicitLogon(
  [in] string UserName,
  [in] string Domain,
  [in] string Password
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*UserName* \[ En\]
</dt> <dd>

Credencial de inicio de sesión de nombre de usuario.

</dd> <dt>

*Dominio* \[ En\]
</dt> <dd>

Credencial de inicio de sesión de dominio.

</dd> <dt>

*Contraseña* \[ En\]
</dt> <dd>

Credencial de inicio de sesión de contraseña.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve Correcto si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está bajo control de directiva de grupo.

## <a name="remarks"></a>Comentarios

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

[**Win32 \_ TSLogonSetting**](win32-tslogonsetting.md)
</dt> </dl>

 

