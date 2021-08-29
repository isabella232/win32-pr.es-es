---
description: La clase WMI de asociación AllocatedResource de Win32 \_ relaciona un dispositivo lógico con un recurso del sistema. Esta clase se usa para detectar qué recursos, como IRQs o canales DMA, están en uso por un dispositivo específico.
ms.assetid: cfac1209-1405-4fee-847c-8a61504bfac1
ms.tgt_platform: multiple
title: Win32_AllocatedResource clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AllocatedResource
- Win32_AllocatedResource.Dependent
- Win32_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b5bbc459a020758398eef8de3db8d809378a1a88095c69fd91a170ce3930e3b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119816665"
---
# <a name="win32_allocatedresource-class"></a>Clase AllocatedResource de Win32 \_

La clase WMI **de asociación \_ AllocatedResource** [de](/windows/desktop/WmiSdk/retrieving-a-class) Win32 relaciona un dispositivo lógico con un recurso del sistema. Esta clase se usa para detectar qué recursos, como IRQs o canales DMA, están en uso por un dispositivo específico.

Esta clase está obsoleta. En lugar de esta clase, debe usar las propiedades de la [**clase \_ PNPAllocatedResource de Win32.**](win32-pnpallocatedresource.md)

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C50D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a>Miembros

La **clase \_ AllocatedResource de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ AllocatedResource de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ SystemResource**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| \_ SystemResource")
</dt> </dl>

Un [**objeto \_ SystemResource de CIM**](cim-systemresource.md) que describe las propiedades de un recurso del sistema disponible para el dispositivo lógico.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim LogicalDevice**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) \| ("CIM \_ LogicalDevice")
</dt> </dl>

Un [**\_ dispositivo lógico CIM**](cim-logicaldevice.md) que representa las propiedades del dispositivo lógico que usa los recursos del sistema asignados a él.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ AllocatedResource de Win32** se deriva de [**la dependencia CIM \_**](cim-dependency.md).

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

 

