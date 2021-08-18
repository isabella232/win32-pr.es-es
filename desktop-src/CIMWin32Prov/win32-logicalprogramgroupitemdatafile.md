---
description: La clase WMI de asociación LogicalProgramGroupItemDataFile de Win32 relaciona los elementos de grupo de programas de la menú Inicio y los archivos en los que \_ se almacenan.
ms.assetid: 9327c205-d0ad-4f2b-a65e-2a648e7c13e0
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroupItemDataFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupItemDataFile
- Win32_LogicalProgramGroupItemDataFile.Antecedent
- Win32_LogicalProgramGroupItemDataFile.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b6f69c23ae545de837e9d6578ba2f64eed51ecbc6f10780e40c809cb2e362b33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973064"
---
# <a name="win32_logicalprogramgroupitemdatafile-class"></a>Clase \_ LogicalProgramGroupItemDataFile de Win32

La clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **de asociación \_ LogicalProgramGroupItemDataFile de Win32** relaciona los elementos de grupo de programas del menú Inicio y los archivos en los que se almacenan. 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{08FFAD62-8050-11d2-90CE-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupItemDataFile : CIM_Dependency
{
  Win32_LogicalProgramGroupItem REF Antecedent;
  CIM_DataFile                  REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ LogicalProgramGroupItemDataFile de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ LogicalProgramGroupItemDataFile de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ LogicalProgramGroupItem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalProgramGroupItem")
</dt> </dl>

Referencia a la instancia de que representa las agrupaciones de programas en el **menú** Inicio.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ DataFile**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| \_ DataFile")
</dt> </dl>

Referencia a la instancia de que representa la clase asociada al grupo de programas.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ LogicalProgramGroupItemDataFile de Win32** se deriva de [**la dependencia \_ CIM**](cim-dependency.md).

El proceso de llamada que usa esta clase debe tener el **SE \_ restore \_ NAME** en el equipo en el que reside el Registro. Por ejemplo, si enumera esta clase en el equipo local, la cuenta con la que se ejecuta la aplicación debe tener este privilegio. Para obtener más información, vea [Ejecutar operaciones con privilegios.](/windows/desktop/WmiSdk/executing-privileged-operations)

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

 

