---
description: La clase WMI de asociación CIMLogicalDeviceCIMDataFile de Win32 relaciona los dispositivos lógicos y los archivos de datos, lo que indica los archivos de controlador utilizados \_ por el dispositivo. Esta clase se usa para detectar qué controladores de dispositivo usa un dispositivo.
ms.assetid: 892272de-920d-4fa0-adbc-f584ed6e8748
ms.tgt_platform: multiple
title: Win32_CIMLogicalDeviceCIMDataFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CIMLogicalDeviceCIMDataFile
- Win32_CIMLogicalDeviceCIMDataFile.Dependent
- Win32_CIMLogicalDeviceCIMDataFile.Antecedent
- Win32_CIMLogicalDeviceCIMDataFile.Purpose
- Win32_CIMLogicalDeviceCIMDataFile.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8124031c07091399241ce355eef0a499235892bff3875e4248641f0454671540
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119917985"
---
# <a name="win32_cimlogicaldevicecimdatafile-class"></a>Clase \_ CIMLogicalDeviceCIMDataFile de Win32

La clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) de asociación **\_ CIMLogicalDeviceCIMDataFile de Win32** relaciona los dispositivos lógicos y los archivos de datos, lo que indica los archivos de controlador utilizados por el dispositivo. Esta clase se usa para detectar qué controladores de dispositivo usa un dispositivo.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C510-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_CIMLogicalDeviceCIMDataFile : CIM_Dependency
{
  CIM_DataFile      REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint16                Purpose;
  string                PurposeDescription;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIMLogicalDeviceCIMDataFile de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIMLogicalDeviceCIMDataFile de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| \_ LogicalDevice")
</dt> </dl>

Un [**\_ dispositivo lógico CIM**](cim-logicaldevice.md) que representa las propiedades del dispositivo lógico que usa el archivo de datos.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cim \_ DataFile**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| \_ DataFile")
</dt> </dl>

Un [**archivo de \_ datos CIM**](cim-datafile.md) que representa las propiedades del archivo de datos asignado al dispositivo lógico.

</dd> <dt>

**Propósito**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")
</dt> </dl>

Rol que desempeña el archivo de datos con respecto a su dispositivo lógico asociado.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

**Controlador** (2)


</dt> <dd></dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

**Software de configuración** (3)


</dt> <dd></dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

**Software de aplicación** (4)


</dt> <dd></dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

**Instrumentación** (5)


</dt> <dd></dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

**Firmware** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**PurposeDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM")
</dt> </dl>

Extiende el valor de la **propiedad Purpose** de esta clase.

Ejemplo: "Controlador de disquete"

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ CIMLogicalDeviceCIMDataFile de Win32** se deriva de [**la dependencia \_ CIM**](cim-logicaldevice.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia \_ cim**](cim-dependency.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

