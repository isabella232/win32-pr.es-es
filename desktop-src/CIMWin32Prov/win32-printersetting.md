---
description: La clase WMI de asociación PrinterSetting de Win32 \_ relaciona una impresora y sus opciones de configuración.
ms.assetid: 5d0f0724-0583-449b-a6da-336e7c8e526e
ms.tgt_platform: multiple
title: Win32_PrinterSetting clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PrinterSetting
- Win32_PrinterSetting.Setting
- Win32_PrinterSetting.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: be39a9f614ab172c75e5ddc857254cdd91ea20d1352a33071cd6fa3627132d71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759385"
---
# <a name="win32_printersetting-class"></a>Clase PrinterSetting de Win32 \_

La clase WMI **de asociación \_ PrinterSetting** [de](../wmisdk/retrieving-a-class.md) Win32 relaciona una impresora y sus opciones de configuración.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_PrinterSetting : Win32_DeviceSettings
{
  CIM_Setting       REF Setting;
  CIM_LogicalDevice REF Element;
};
```

## <a name="members"></a>Miembros

La **clase \_ PrinterSetting de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ PrinterSetting de Win32** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CIM \| \_ LogicalDevice cim")
</dt> </dl>

Un [**\_ dispositivo lógico CIM**](cim-logicaldevice.md) que representa las propiedades del dispositivo lógico en el que se puede aplicar la configuración.

Esta propiedad se hereda de [**Win32 \_ DeviceSettings.**](win32-devicesettings.md)

</dd> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos: **Configuración de CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("cim \| \_ setting")
</dt> </dl>

Una [**configuración \_ CIM**](cim-setting.md) que representa la configuración que se puede aplicar al dispositivo lógico.

Esta propiedad se hereda de [**Win32 \_ DeviceSettings.**](win32-devicesettings.md)

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ PrinterSetting de Win32** se deriva de [**Win32 \_ DeviceSettings.**](win32-devicesettings.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                        |
| MOF<br/>                      | <dl> <dt>Win32 \_ Printer.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dispositivo \_ Win32Settings**](win32-devicesettings.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
