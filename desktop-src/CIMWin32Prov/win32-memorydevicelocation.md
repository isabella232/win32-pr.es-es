---
description: La \_ clase WMI MemoryDeviceLocation Association de Win32 relaciona un dispositivo de memoria y la memoria física en la que existe.
ms.assetid: 6fef916e-44e2-4b9f-94b7-c7204259004a
ms.tgt_platform: multiple
title: Win32_MemoryDeviceLocation (clase)
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
ms.openlocfilehash: 5cf1ba93a2574810892443aefa43e1c7c501636c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998154"
---
# <a name="win32_memorydevicelocation-class"></a>\_Clase Win32 MemoryDeviceLocation

La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MemoryDeviceLocation** Association de Win32 relaciona un dispositivo de memoria y la memoria física en la que existe.

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

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ PhysicalMemory")
</dt> </dl>

[**\_ PhysicalMemory de Win32**](win32-physicalmemory.md) que representa la memoria física que contiene el dispositivo de memoria.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ MemoryDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryDevice")
</dt> </dl>

**\_ MemoryDeviceLocation de Win32** que representa el dispositivo de memoria existente en la memoria física.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ MemoryDeviceLocation de Win32** se deriva de los [**\_ beneficios de CIM**](cim-realizes.md).

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

[**Contrataciones \_ de CIM**](cim-realizes.md)
</dt> <dt>

[Clases de hardware de sistema del equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

