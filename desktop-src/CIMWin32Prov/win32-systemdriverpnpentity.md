---
description: La clase WMI de asociación SystemDriverPNPEntity de Win32 relaciona un dispositivo Plug and Play en el sistema informático que ejecuta Windows y el controlador que admite el \_ dispositivo Plug and Play.
ms.assetid: 2696c8e5-3bc3-42e3-807b-a387607c7c09
ms.tgt_platform: multiple
title: Win32_SystemDriverPNPEntity clase
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
ms.openlocfilehash: e4b0de9559d223db4c398387ca846be39b17566b3267c76399bdf4381cdd14e7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751115"
---
# <a name="win32_systemdriverpnpentity-class"></a>Clase \_ SystemDriverPNPEntity de Win32

La clase [WMI](../wmisdk/retrieving-a-class.md) de asociación **\_ SystemDriverPNPEntity de Win32** relaciona un dispositivo Plug and Play en el sistema informático que ejecuta Windows y el controlador que admite el Plug and Play.

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

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Antecedente"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ PNPEntity")
</dt> </dl>

Representa el Plug and Play controlado por el controlador.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ SystemDriver**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("Dependent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ SystemDriver")
</dt> </dl>

Un [**\_ SystemDriver de Win32**](win32-systemdriver.md) que representa el controlador que admite el Plug and Play dispositivo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ SystemDriverPNPEntity de Win32** se deriva de [**la dependencia CIM \_**](cim-dependency.md).

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

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
