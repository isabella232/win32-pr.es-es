---
title: Método ConnectionSettings de la Win32_TSClientSetting clase
description: El método ConnectionSettings establece la configuración de sesión que se aplica al proceso de conexión e inicio de sesión.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- Método ConnectionSettings Servicios de Escritorio remoto
- Método ConnectionSettings Servicios de Escritorio remoto , Win32_TSClientSetting clase
- Win32_TSClientSetting clase Servicios de Escritorio remoto , método ConnectionSettings
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.ConnectionSettings
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3f48a93959b1e86eb77f6ab0fbfab444444ca1c077835e1c28330d34ed66c87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119656175"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a>Método ConnectionSettings de la clase \_ TSClientSetting de Win32

El **método ConnectionSettings** establece la configuración de sesión que se aplica al proceso de conexión e inicio de sesión.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ConnectionSettings(
  [in] uint32 ConnectClientDrivesAtLogon,
  [in] uint32 ConnectPrinterAtLogon,
  [in] uint32 DefaultToClientPrinter
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ConnectClientDrivesAtLogon* \[ En\]
</dt> <dd>

Marca la habilitación o deshabilitación de la propiedad **ConnectClientDrivesAtLogon** que especifica si las unidades del cliente se conectan automáticamente durante el procedimiento de inicio de sesión.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Las unidades del cliente no se conectan automáticamente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Las unidades del cliente se conectan automáticamente.

</dd> </dl> </dd> <dt>

*ConnectPrinterAtLogon* \[ En\]
</dt> <dd>

Marca que habilita o deshabilita la propiedad **ConnectPrinterAtLogon,** que especifica si todas las impresoras cliente locales asignadas se conectan automáticamente durante el procedimiento de inicio de sesión.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Todas las impresoras locales asignadas no se conectan automáticamente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Todas las impresoras locales asignadas se conectan automáticamente.

</dd> </dl> </dd> <dt>

*DefaultToClientPrinter* \[ En\]
</dt> <dd>

Marca la habilitación o deshabilitación de la propiedad **DefaultToClientPrinter,** que especifica si los trabajos de impresión se envían automáticamente a la impresora local del cliente.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

Los trabajos de impresión no se envían automáticamente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Los trabajos de impresión se envían automáticamente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si el servidor invalida la configuración de conexión del usuario.

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

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

