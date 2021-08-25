---
description: La clase WMI de asociación SystemProgramGroups de Win32 relaciona \_ un sistema informático y un grupo de programas lógicos.
ms.assetid: cbf810c8-a967-4d60-889c-e47c43b039ea
ms.tgt_platform: multiple
title: Win32_SystemProgramGroups clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemProgramGroups
- Win32_SystemProgramGroups.Element
- Win32_SystemProgramGroups.Setting
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: c33511d1f8a1b7ccf3657f31a0c3b997f7e1044f7425de9683f167d557b1dba9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827985"
---
# <a name="win32_systemprogramgroups-class"></a>Clase \_ SystemProgramGroups de Win32

La clase WMI **de asociación \_ SystemProgramGroups** [de](../wmisdk/retrieving-a-class.md) Win32 relaciona un sistema informático y un grupo de programas lógicos.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades y los métodos están en orden alfabético, no en el orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C505-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemProgramGroups : Win32_SystemSetting
{
  Win32_ComputerSystem      REF Element;
  Win32_LogicalProgramGroup REF Setting;
};
```

## <a name="members"></a>Miembros

La **clase \_ SystemProgramGroups de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemProgramGroups de Win32** tiene estas propiedades.

<dl> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Element"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

Referencia a la instancia de que representa el sistema informático que contiene el grupo de programas lógicos.

</dd> <dt>

**Configuración**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ LogicalProgramGroup**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](../wmisdk/standard-qualifiers.md) ("Setting"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ LogicalProgramGroup")
</dt> </dl>

Referencia a la instancia de que representa el grupo de programas lógicos en el sistema del equipo.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ SystemProgramGroups de Win32** se deriva de [**\_ SystemSetting de Win32.**](win32-systemsetting.md)

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

[**SystemSetting de Win32 \_**](win32-systemsetting.md)
</dt> <dt>

[Clases de sistema operativo](./operating-system-classes.md)
</dt> </dl>

 

 
