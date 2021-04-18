---
title: Método ConnectionSettings de la clase Win32_TSClientSetting
description: El método ConnectionSettings establece la configuración de sesión que se aplica a la conexión y al proceso de inicio de sesión.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- Método ConnectionSettings Servicios de Escritorio remoto
- Método ConnectionSettings Servicios de Escritorio remoto, clase Win32_TSClientSetting
- Win32_TSClientSetting de clase Servicios de Escritorio remoto, método ConnectionSettings
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
ms.openlocfilehash: ec255f00656684751b750e92d7a3df8290e3573e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534060"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a>Método ConnectionSettings de la \_ clase TSClientSetting de Win32

El método **ConnectionSettings** establece la configuración de sesión que se aplica a la conexión y al proceso de inicio de sesión.

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

*ConnectClientDrivesAtLogon* \[ de\]
</dt> <dd>

Marca que habilita o deshabilita la propiedad **ConnectClientDrivesAtLogon** , que especifica si las unidades del cliente se conectan automáticamente durante el procedimiento de inicio de sesión.

<dt>

<span id="0"></span>

<span id="0"></span>**0,1**


</dt> <dd>

Las unidades del cliente no se conectan automáticamente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Las unidades del cliente se conectan automáticamente.

</dd> </dl> </dd> <dt>

*ConnectPrinterAtLogon* \[ de\]
</dt> <dd>

Marca que habilita o deshabilita la propiedad **ConnectPrinterAtLogon** , que especifica si todas las impresoras de cliente local asignadas se conectan automáticamente durante el procedimiento de inicio de sesión.

<dt>

<span id="0"></span>

<span id="0"></span>**0,1**


</dt> <dd>

Todas las impresoras locales asignadas no se conectan automáticamente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Todas las impresoras locales asignadas se conectan automáticamente.

</dd> </dl> </dd> <dt>

*DefaultToClientPrinter* \[ de\]
</dt> <dd>

Marca que habilita o deshabilita la propiedad **DefaultToClientPrinter** , que especifica si los trabajos de impresión se envían automáticamente a la impresora local del cliente.

<dt>

<span id="0"></span>

<span id="0"></span>**0,1**


</dt> <dd>

Los trabajos de impresión no se envían automáticamente.

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Los trabajos de impresión se envían automáticamente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI. Consulte [servicios de escritorio remoto códigos de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores. El método devuelve un error si el servidor invalida la configuración de conexión del usuario.

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

[**Win32 \_ TSClientSetting**](win32-tsclientsetting.md)
</dt> </dl>

 

