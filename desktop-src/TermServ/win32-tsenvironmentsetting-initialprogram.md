---
title: Método InitialProgram de la clase Win32_TSEnvironmentSetting
description: El método InitialProgram establece las propiedades del programa de inicio, como el nombre, el directorio de trabajo y la ruta de acceso del programa que se va a iniciar inmediatamente después del inicio de sesión en el servidor de host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: e53621cf-ade8-4301-acc0-232866e88488
ms.tgt_platform: multiple
keywords:
- Método InitialProgram Servicios de Escritorio remoto
- Método InitialProgram Servicios de Escritorio remoto, clase Win32_TSEnvironmentSetting
- Win32_TSEnvironmentSetting de clase Servicios de Escritorio remoto, método InitialProgram
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685962"
---
# <a name="initialprogram-method-of-the-win32_tsenvironmentsetting-class"></a>Método InitialProgram de la \_ clase TSEnvironmentSetting de Win32

El método **InitialProgram** establece las propiedades del programa de inicio, como el nombre, el directorio de trabajo y la ruta de acceso del programa que se va a iniciar inmediatamente después del inicio de sesión en el servidor de host de sesión de escritorio remoto (host de sesión de escritorio remoto).

## <a name="syntax"></a>Sintaxis


```mof
uint32 InitialProgram(
  [in] string InitialProgramPath,
  [in] string Startin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*InitialProgramPath* \[ de\]
</dt> <dd>

El nombre y la ruta de acceso del programa de inicio.

</dd> <dt>

*Inicio* \[ de\]
</dt> <dd>

La ruta de acceso al directorio de trabajo del programa de inicio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si la configuración está en control de directiva de grupo.

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ TSEnvironmentSetting**](win32-tsenvironmentsetting.md)
</dt> </dl>

 

