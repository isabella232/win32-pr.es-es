---
description: La clase WMI de asociación SystemBIOS de Win32 relaciona un sistema informático (incluidos datos como propiedades de inicio, zonas horarias, configuraciones de arranque o contraseñas administrativas) y un BIOS del sistema (servicios, lenguajes y propiedades de administración del \_ sistema).
ms.assetid: 92747b1b-ef28-40ab-868a-6755aee8c723
ms.tgt_platform: multiple
title: Win32_SystemBIOS clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SystemBIOS
- Win32_SystemBIOS.PartComponent
- Win32_SystemBIOS.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bc8ec1f3526e2faefe0e63c9dea357accd025c13
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061471"
---
# <a name="win32_systembios-class"></a>Clase SystemBIOS de Win32 \_

La clase [WMI](../wmisdk/retrieving-a-class.md) de asociación **\_ SystemBIOS de Win32** relaciona un sistema informático (incluidos datos como propiedades de inicio, zonas horarias, configuraciones de arranque o contraseñas administrativas) y un BIOS del sistema (servicios, lenguajes y propiedades de administración del sistema).

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EE-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SystemBIOS : CIM_SystemComponent
{
  Win32_BIOS           REF PartComponent;
  Win32_ComputerSystem REF GroupComponent;
};
```

## <a name="members"></a>Members

La **clase \_ SystemBIOS de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemBIOS de Win32** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("GroupComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ ComputerSystem")
</dt> </dl>

El [**sistema de equipos \_ Win32**](win32-computersystemprocessor.md) que contiene el BIOS de la asociación.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ BIOS win32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("PartComponent"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ BIOS")
</dt> </dl>

Un [**\_ BIOS win32**](win32-bios.md) contenido en el sistema informático de esta asociación.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ SystemBIOS de Win32** se deriva de [**CIM \_ SystemComponent**](cim-systemcomponent.md).

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

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
