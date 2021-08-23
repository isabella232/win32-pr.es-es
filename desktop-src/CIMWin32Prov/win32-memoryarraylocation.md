---
description: La clase WMI de asociación MemoryArrayLocation de Win32 relaciona una matriz de memoria lógica y la matriz de memoria física en \_ la que existe.
ms.assetid: 455daeee-ad67-4599-84d6-fa3f4ac593aa
ms.tgt_platform: multiple
title: Win32_MemoryArrayLocation clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryArrayLocation
- Win32_MemoryArrayLocation.Dependent
- Win32_MemoryArrayLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a0fd01751794dc9177f3840804f0412db70531f6706a452793fe6cbcf3aa2389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079808"
---
# <a name="win32_memoryarraylocation-class"></a>Clase MemoryArrayLocation de Win32 \_

La clase WMI **de asociación \_ MemoryArrayLocation** [de](/windows/desktop/WmiSdk/retrieving-a-class) Win32 relaciona una matriz de memoria lógica y la matriz de memoria física en la que existe.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{B24EF561-BBBE-11d2-ABFB-00805F538618}"), AMENDMENT]
class Win32_MemoryArrayLocation : CIM_Realizes
{
  Win32_MemoryArray         REF Dependent;
  Win32_PhysicalMemoryArray REF Antecedent;
};
```

## <a name="members"></a>Miembros

La **clase \_ MemoryArrayLocation de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ MemoryArrayLocation de Win32** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ PhysicalMemoryArray**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ PhysicalMemoryArray")
</dt> </dl>

Clase [**\_ PhysicalMemoryArray de Win32**](win32-physicalmemoryarray.md) que describe la matriz de memoria física que implementa la matriz de memoria lógica.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Win32 \_ MemoryArray**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryArray")
</dt> </dl>

MemoryArray [**de \_ Win32**](win32-memoryarray.md) que describe la matriz de memoria lógica implementada por la matriz de memoria física.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ MemoryArrayLocation de Win32** se deriva de [**CIM \_ Realizes**](cim-realizes.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CIM \_ Se da cuenta**](cim-realizes.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

