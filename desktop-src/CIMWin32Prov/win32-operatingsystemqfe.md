---
description: La clase WMI de asociación OperatingSystemQFE de Win32 relaciona un sistema operativo y las actualizaciones del producto aplicadas como se representa en \_ \_ QuickFixEngineering de Win32.
ms.assetid: 71985759-7e45-44df-82a9-f9a93e3b923e
ms.tgt_platform: multiple
title: Win32_OperatingSystemQFE clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_OperatingSystemQFE
- Win32_OperatingSystemQFE.Antecedent
- Win32_OperatingSystemQFE.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 60fa11faaf7b6d85ce7d3494e1081afc4742b65e27f11fc2cebcd94949373745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119972355"
---
# <a name="win32_operatingsystemqfe-class"></a>Clase OperatingSystemQFE de Win32 \_

La clase [WMI](../wmisdk/retrieving-a-class.md) de asociación **\_ Win32 OperatingSystemQFE** relaciona un sistema operativo y las actualizaciones del producto aplicadas como se representa en [**\_ QuickFixEngineering de Win32.**](win32-quickfixengineering.md)

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{2CB2C452-C516-11D2-B364-00105A1F77A1}"), AMENDMENT]
class Win32_OperatingSystemQFE : CIM_Dependency
{
  Win32_OperatingSystem     REF Antecedent;
  Win32_QuickFixEngineering REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ OperatingSystemQFE de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ OperatingSystemQFE de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ OperatingSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Wmi \| Win32 \_ OperatingSystem")
</dt> </dl>

Referencia a la instancia de que representa el sistema afectado por la actualización del producto en esta asociación.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ QuickFixEngineering de Win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**Weak**](../wmisdk/standard-qualifiers.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ QuickFixEngineering")
</dt> </dl>

Referencia a la instancia de que representa la instancia de objeto aplicada al sistema operativo en esta asociación.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ OperatingSystemQFE de Win32** se deriva de [**la dependencia CIM \_**](cim-dependency.md).

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

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
