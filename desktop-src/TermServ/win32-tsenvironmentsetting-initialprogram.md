---
title: Método InitialProgram de la Win32_TSEnvironmentSetting clase
description: El método InitialProgram establece las propiedades del programa de inicio, como el nombre, el directorio de trabajo y la ruta de acceso del programa que se iniciarán inmediatamente después de iniciar sesión en el servidor de host de sesión de Escritorio remoto (host de sesión de Escritorio remoto).
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- Método InitialProgram Servicios de Escritorio remoto
- Método InitialProgram Servicios de Escritorio remoto , Win32_TSEnvironmentSetting clase
- Win32_TSEnvironmentSetting clase Servicios de Escritorio remoto método , InitialProgram
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.InitialProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccd41e1af990e37b8458431106bc2ec9a8489b14
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127172777"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a>Método InitialProgram de la clase \_ TSEnvironmentSetting de Win32

El **método InitialProgram** establece las propiedades del programa de inicio, como el nombre, el directorio de trabajo y la ruta de acceso del programa para que se inicie inmediatamente después de iniciar sesión en el servidor Escritorio remoto Session Host (Host de sesión de Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*InitialProgramPath* \[ En\]
</dt> <dd>

Nombre y ruta de acceso del programa de inicio.

</dd> <dt>

*Startin* \[ En\]
</dt> <dd>

Ruta de acceso al directorio de trabajo del programa de inicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está bajo control de directiva de grupo.

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

