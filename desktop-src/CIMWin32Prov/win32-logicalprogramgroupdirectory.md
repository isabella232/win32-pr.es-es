---
description: La clase WMI de asociación LogicalProgramGroupDirectory de Win32 relaciona los grupos de programas lógicos (agrupaciones en el menú Inicio) y los directorios de archivos en los \_ que se almacenan.
ms.assetid: 31a8b56a-d4fd-4cc5-9997-ec6211fe9425
ms.tgt_platform: multiple
title: Win32_LogicalProgramGroupDirectory clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalProgramGroupDirectory
- Win32_LogicalProgramGroupDirectory.Antecedent
- Win32_LogicalProgramGroupDirectory.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6ebaddd4455ba1b62832f940d78534c90cefeeb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273431"
---
# <a name="win32_logicalprogramgroupdirectory-class"></a>Clase LogicalProgramGroupDirectory de Win32 \_

La clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) de asociación **\_ LogicalProgramGroupDirectory de Win32**  relaciona los grupos de programas lógicos (agrupaciones en el menú Inicio) y los directorios de archivos en los que se almacenan.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), Privileges("SeRestorePrivilege"), UUID("{F25FE467-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalProgramGroupDirectory : CIM_Dependency
{
  Win32_LogicalProgramGroup REF Antecedent;
  Win32_Directory           REF Dependent;
};
```

## <a name="members"></a>Members

La **clase \_ LogicalProgramGroupDirectory de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ LogicalProgramGroupDirectory de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ LogicalProgramGroup**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalProgramGroup")
</dt> </dl>

Referencia a la instancia de que representa el grupo de programas lógicos.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Directorio Win32 \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Wmi \| Win32 \_ Directory")
</dt> </dl>

Referencia a la instancia de que representa el directorio de archivos para el grupo de programas lógicos.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ LogicalProgramGroupDirectory de Win32** se deriva de [**la dependencia \_ CIM**](cim-dependency.md).

El proceso de llamada que usa esta clase debe tener el **SE \_ restore \_ NAME** en el equipo en el que reside el Registro. Por ejemplo, si enumera esta clase en el equipo local, la cuenta con la que se ejecuta la aplicación debe tener este privilegio. Para obtener más información, vea [Ejecutar operaciones con privilegios.](/windows/desktop/WmiSdk/executing-privileged-operations)

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

[**Dependencia \_ cim**](cim-dependency.md)
</dt> <dt>

[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

