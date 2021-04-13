---
description: La \_ clase WMI SystemDriverPNPEntity Association de Win32 relaciona un dispositivo Plug and Play en el equipo que ejecuta Windows y el controlador que admite el dispositivo Plug and Play.
ms.assetid: 2696c8e5-3bc3-42e3-807b-a387607c7c09
ms.tgt_platform: multiple
title: Win32_SystemDriverPNPEntity (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemDriverPNPEntity
- Win32_SystemDriverPNPEntity.Antecedent
- Win32_SystemDriverPNPEntity.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8b5a7eedfbd7a545e37cb9cda38c19cf61308761
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538914"
---
# <a name="win32_systemdriverpnpentity-class"></a>\_Clase Win32 SystemDriverPNPEntity

La [clase WMI](../wmisdk/retrieving-a-class.md) **\_ SystemDriverPNPEntity** Association de Win32 relaciona un dispositivo Plug and Play en el equipo que ejecuta Windows y el controlador que admite el dispositivo Plug and Play.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{0800F074-CB98-11d2-B35D-00104BC97924}"), AMENDMENT]
class Win32_SystemDriverPNPEntity : CIM_Dependency
{
  Win32_PNPEntity    REF Antecedent;
  Win32_SystemDriver REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ SystemDriverPNPEntity de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemDriverPNPEntity de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ PNPEntity**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PNPEntity")
</dt> </dl>

Representa el dispositivo Plug and Play controlado por el controlador.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ SystemDriver**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](../wmisdk/key-qualifier.md), [**invalidación**](../wmisdk/standard-qualifiers.md) ("dependiente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")
</dt> </dl>

[**\_ SystemDriver de Win32**](win32-systemdriver.md) que representa el controlador que admite el dispositivo Plug and Play.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ SystemDriverPNPEntity de Win32** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).

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

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
