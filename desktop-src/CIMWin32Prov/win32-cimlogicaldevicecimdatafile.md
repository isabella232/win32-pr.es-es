---
description: La \_ clase WMI CIMLogicalDeviceCIMDataFile Association de Win32 relaciona los dispositivos lógicos y los archivos de datos, que indican los archivos de controlador utilizados por el dispositivo. Esta clase se usa para detectar los controladores de dispositivo que usa un dispositivo.
ms.assetid: 892272de-920d-4fa0-adbc-f584ed6e8748
ms.tgt_platform: multiple
title: Win32_CIMLogicalDeviceCIMDataFile (clase)
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
ms.openlocfilehash: 15db6209360cbd150a722dc98b6255afd696cbe9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539153"
---
# <a name="win32_cimlogicaldevicecimdatafile-class"></a>\_Clase Win32 CIMLogicalDeviceCIMDataFile

La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ CIMLogicalDeviceCIMDataFile** Association de Win32 relaciona los dispositivos lógicos y los archivos de datos, que indican los archivos de controlador utilizados por el dispositivo. Esta clase se usa para detectar los controladores de dispositivo que usa un dispositivo.

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

Tipo de datos **: \_ LogicalDevice de CIM**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| lógico CIM CIM \_ ")
</dt> </dl>

Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que representa las propiedades del dispositivo lógico utilizado por el archivo de datos.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos **: \_ archivo** de datos CIM
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM archivo de \_ archivos")
</dt> </dl>

Un [**\_ archivo**](cim-datafile.md) de datos CIM que representa las propiedades del archivo de datos asignado al dispositivo lógico.

</dd> <dt>

**Propósito**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
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

**Otro** (1)


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

Extiende el valor de la propiedad **purpose** de esta clase.

Ejemplo: "controlador de disquete"

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ CIMLogicalDeviceCIMDataFile de Win32** se deriva de la [**\_ dependencia CIM**](cim-logicaldevice.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia de CIM \_**](cim-dependency.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

