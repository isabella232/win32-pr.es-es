---
title: Método SetTimeZoneRedirection de la clase Win32_TerminalServiceSetting
description: El método SetTimeZoneRedirection establece la propiedad TimeZoneRedirection, que permite al equipo cliente redirigir su configuración de zona horaria a la sesión de Servicios de Escritorio remoto.
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- Método SetTimeZoneRedirection Servicios de Escritorio remoto
- Método SetTimeZoneRedirection Servicios de Escritorio remoto, clase Win32_TerminalServiceSetting
- Win32_TerminalServiceSetting de clase Servicios de Escritorio remoto, método SetTimeZoneRedirection
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetTimeZoneRedirection
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2761567c724abf129ac881188bc468b228d7fd11
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676725"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a>Método SetTimeZoneRedirection de la \_ clase TerminalServiceSetting de Win32

El método **SetTimeZoneRedirection** establece la propiedad **TimeZoneRedirection** , que permite al equipo cliente redirigir su configuración de zona horaria a la sesión de servicios de escritorio remoto.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TimeZoneRedirection* \[ de\]
</dt> <dd>

Nuevo valor de la propiedad **TimeZoneRedirection** .

<dt>

<span id="0"></span>

<span id="0"></span>**0,1**


</dt> <dd>

Deshabilita la propiedad **TimeZoneRedirection** . No se produce la redirección de zona horaria.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Habilita la propiedad **TimeZoneRedirection** . La zona horaria del cliente se redirige a la zona horaria de la sesión.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Observaciones

De forma predeterminada, la zona horaria de la sesión Servicios de Escritorio remoto es la misma que la zona horaria del servidor host de sesión Escritorio remoto (host de sesión de escritorio remoto). Los equipos cliente no pueden redirigir la información de zona horaria.

Si se deshabilita la redirección de zona horaria, las nuevas sesiones heredan la zona horaria del servidor. Cuando una sesión se vuelve a conectar, la sesión conserva la zona horaria que tenía antes de la desconexión.

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

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md)
</dt> </dl>

 

