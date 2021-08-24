---
description: La relación dispositivo CIMSoftware identifica el software asociado a un dispositivo, como controladores, software de configuración o \_ de aplicación, o firmware.
ms.assetid: 831d0014-2a01-49f4-9642-fae5682f0388
ms.tgt_platform: multiple
title: CIM_DeviceSoftware clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceSoftware
- CIM_DeviceSoftware.Dependent
- CIM_DeviceSoftware.Antecedent
- CIM_DeviceSoftware.Purpose
- CIM_DeviceSoftware.PurposeDescription
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 483490c35066457b3c640ef934b6543a737bc52bd31e5178aee837b2a7abc321
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119321585"
---
# <a name="cim_devicesoftware-class"></a>Cim \_ DeviceSoftware (clase)

La **relación \_ dispositivo CIMSoftware** identifica el software asociado a un dispositivo, como controladores, software de configuración o de aplicación, o firmware.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, UUID("{36363AAA-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceSoftware : CIM_Dependency
{
  CIM_LogicalDevice   REF Dependent;
  CIM_SoftwareElement REF Antecedent;
  uint16                  Purpose;
  string                  PurposeDescription;
};
```

## <a name="members"></a>Miembros

La **clase \_ DeviceSoftware** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ DeviceSoftware** de CIM tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ SoftwareElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente")
</dt> </dl>

Un [**\_ elemento SoftwareElement de CIM**](cim-softwareelement.md) que describe el elemento de software.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidar**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Un [**\_ dispositivo lógico CIM**](cim-logicaldevice.md) que describe el dispositivo lógico que requiere o usa el software.

</dd> <dt>

**Propósito**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DeviceSoftware**.**PurposeDescription**")
</dt> </dl>

Rol que el software toma con respecto a su dispositivo asociado.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd>

Desconocido.

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)


</dt> <dd>

Otros.

</dd> <dt>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>

<span id="Driver"></span><span id="driver"></span><span id="DRIVER"></span>**Controlador** (2)


</dt> <dd>

Conductor.

</dd> <dt>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>

<span id="Configuration_Software"></span><span id="configuration_software"></span><span id="CONFIGURATION_SOFTWARE"></span>**Software de configuración** (3)


</dt> <dd>

Software de configuración.

</dd> <dt>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>

<span id="Application_Software"></span><span id="application_software"></span><span id="APPLICATION_SOFTWARE"></span>**Software de aplicación** (4)


</dt> <dd>

Software de aplicación.

</dd> <dt>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>

<span id="Instrumentation"></span><span id="instrumentation"></span><span id="INSTRUMENTATION"></span>**Instrumentación** (5)


</dt> <dd>

Instrumentación.

</dd> <dt>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>

<span id="Firmware"></span><span id="firmware"></span><span id="FIRMWARE"></span>**Firmware** (6)


</dt> <dd>

Firmware.

</dd> <dt>

<span id="BIOS"></span><span id="bios"></span>

<span id="BIOS"></span><span id="bios"></span>**BIOS** (7)


</dt> <dd>

Bios.

</dd> <dt>

<span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>

<span id="Boot_ROM"></span><span id="boot_rom"></span><span id="BOOT_ROM"></span>**ROM de arranque** (8)


</dt> <dd>

ROM de arranque.

</dd> </dl>

</dd> <dt>

**PurposeDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ DeviceSoftware**.**Propósito**")
</dt> </dl>

Cadena de forma libre que proporciona más información para la **propiedad Purpose,** por ejemplo, "Software de aplicación".

</dd> </dl>

## <a name="remarks"></a>Comentarios

WMI no implementa esta clase.

La **clase \_ DeviceSoftware** de CIM se deriva de [**la dependencia \_ CIM**](cim-dependency.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 

