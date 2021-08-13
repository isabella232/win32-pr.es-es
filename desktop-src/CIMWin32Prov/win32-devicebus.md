---
description: La clase WMI de asociación \_ Win32 DeviceBus relaciona un bus del sistema y un dispositivo lógico mediante el bus. Esta clase se usa para detectar qué dispositivos están en qué bus.
ms.assetid: 2d7d83a5-c058-40c0-aab3-7700f4067a16
ms.tgt_platform: multiple
title: Win32_DeviceBus clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DeviceBus
- Win32_DeviceBus.Dependent
- Win32_DeviceBus.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc8c6c8cb1d83d31539fa405d09d60db2de68089d82213d08ee9ba8f0491a731
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439165"
---
# <a name="win32_devicebus-class"></a>Clase DeviceBus de Win32 \_

La clase [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **de asociación \_ Win32 DeviceBus** relaciona un bus del sistema y un dispositivo lógico mediante el bus. Esta clase se usa para detectar qué dispositivos están en qué bus.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C50F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DeviceBus : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  Win32_Bus         REF Antecedent;
};
```

## <a name="members"></a>Miembros

La **clase \_ DeviceBus win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ DeviceBus win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ Bus**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bus \| Win32 \_ wmi")
</dt> </dl>

Un [**bus Win32 \_ que**](win32-bus.md) describe las propiedades del bus del sistema que usa el dispositivo lógico.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) \| ("CIM \_ LogicalDevice")
</dt> </dl>

Un [**dispositivo \_ lógico CIM**](cim-logicaldevice.md) que describe las propiedades del dispositivo lógico que usa el bus del sistema.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ DeviceBus de Win32** se deriva de [**la dependencia CIM \_**](cim-dependency.md).

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

 

