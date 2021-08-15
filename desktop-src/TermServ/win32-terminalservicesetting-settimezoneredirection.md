---
title: Método SetTimeZoneRedirection de la Win32_TerminalServiceSetting clase
description: El método SetTimeZoneRedirection establece la propiedad TimeZoneRedirection, que permite al equipo cliente redirigir su configuración de zona horaria a la Servicios de Escritorio remoto predeterminada.
ms.assetid: 4ae149b7-b7de-4530-a142-7253dd1e0d07
ms.tgt_platform: multiple
keywords:
- Método SetTimeZoneRedirection Servicios de Escritorio remoto
- Método SetTimeZoneRedirection Servicios de Escritorio remoto , Win32_TerminalServiceSetting clase
- Win32_TerminalServiceSetting clase Servicios de Escritorio remoto , método SetTimeZoneRedirection
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
ms.openlocfilehash: 802cd4741f4ea30f378492075f69dfa21dfce54688fbc7ff9e72b957689d7c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117755646"
---
# <a name="settimezoneredirection-method-of-the-win32_terminalservicesetting-class"></a>Método SetTimeZoneRedirection de la clase \_ TerminalServiceSetting de Win32

El **método SetTimeZoneRedirection** establece la propiedad **TimeZoneRedirection,** que permite al equipo cliente redirigir su configuración de zona horaria a la Servicios de Escritorio remoto predeterminada.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetTimeZoneRedirection(
  [in] uint32 TimeZoneRedirection
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*TimeZoneRedirection* \[ En\]
</dt> <dd>

Nuevo valor de la **propiedad TimeZoneRedirection.**

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Deshabilita la **propiedad TimeZoneRedirection.** No se produce ningún redireccionamiento de zona horaria.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Habilita la **propiedad TimeZoneRedirection.** La zona horaria del cliente se redirige a la zona horaria de la sesión.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="remarks"></a>Comentarios

De forma predeterminada, la zona horaria de la sesión Servicios de Escritorio remoto es la misma que la zona horaria del servidor Escritorio remoto Session Host (Host de sesión de Escritorio remoto). Los equipos cliente no pueden redirigir la información de zona horaria.

Si el redireccionamiento de zona horaria está deshabilitado, las nuevas sesiones heredan la zona horaria del servidor. Cuando se vuelve a conectar una sesión, la sesión conserva la zona horaria que tenía antes de desconectarse.

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de administración (WMI). Los archivos MOF no se instalan como parte de Microsoft Windows Software Development Kit (SDK). Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Root \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**TerminalServiceSetting de Win32 \_**](win32-terminalservicesetting.md)
</dt> </dl>

 

