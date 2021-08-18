---
description: La clase WMI de asociación MemoryDeviceLocation de Win32 relaciona un dispositivo de memoria y la memoria física en \_ la que existe.
ms.assetid: 6fef916e-44e2-4b9f-94b7-c7204259004a
ms.tgt_platform: multiple
title: Win32_MemoryDeviceLocation clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceLocation
- Win32_MemoryDeviceLocation.Dependent
- Win32_MemoryDeviceLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba19807d888c27246a17d8af73cfd81bfd8ba52136e466ab78433316ea533339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973015"
---
# <a name="win32_memorydevicelocation-class"></a>Clase MemoryDeviceLocation de Win32 \_

La clase WMI **de asociación \_ MemoryDeviceLocation** [de](/windows/desktop/WmiSdk/retrieving-a-class) Win32 relaciona un dispositivo de memoria y la memoria física en la que existe.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDeviceLocation : CIM_Realizes
{
  Win32_MemoryDevice   REF Dependent;
  Win32_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a>Miembros

La **clase \_ MemoryDeviceLocation de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ MemoryDeviceLocation de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ PhysicalMemory**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Wmi \| Win32 \_ PhysicalMemory")
</dt> </dl>

Un [**objeto \_ PhysicalMemory de Win32**](win32-physicalmemory.md) que representa la memoria física que contiene el dispositivo de memoria.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ MemoryDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryDevice")
</dt> </dl>

**\_ MemoryDeviceLocation de Win32** que representa el dispositivo de memoria existente en la memoria física.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ MemoryDeviceLocation de Win32** se deriva de [**CIM \_ Realizes**](cim-realizes.md).

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

[**CIM \_ se da cuenta**](cim-realizes.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

