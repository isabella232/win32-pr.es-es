---
description: La clase WMI de asociación SerialPortSetting de Win32 relaciona \_ un puerto serie y sus opciones de configuración.
ms.assetid: 57856207-abe5-4d93-9a34-acfe30ccd80c
ms.tgt_platform: multiple
title: Win32_SerialPortSetting clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortSetting
- Win32_SerialPortSetting.Setting
- Win32_SerialPortSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 713cdb57b5ed7135529959d3c17f7453924ce1dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266636"
---
# <a name="win32_serialportsetting-class"></a>Clase \_ SerialPortSetting de Win32

La clase WMI **de asociación \_ SerialPortSetting** [de](../wmisdk/retrieving-a-class.md) Win32 relaciona un puerto serie y sus opciones de configuración.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4FE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortSetting : Win32_DeviceSettings
{
  Win32_SerialPortConfiguration REF Setting;
  Win32_SerialPort              REF Element;
};
```

## <a name="members"></a>Members

La **clase \_ SerialPortSetting de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SerialPortSetting de Win32** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ SerialPort**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPort")
</dt> </dl>

Un [**\_ SerialPort de Win32**](win32-serialport.md) que contiene las propiedades de un puerto serie en el sistema del equipo.

</dd> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ SerialPortConfiguration**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SerialPortConfiguration")
</dt> </dl>

Un [**\_ serialPortConfiguration de Win32**](win32-serialportconfiguration.md) que contiene la configuración del puerto serie.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ SerialPortSetting de Win32** se deriva de [**Win32 \_ DeviceSettings.**](win32-devicesettings.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Win32 \_ DeviceSettings**](win32-devicesettings.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
