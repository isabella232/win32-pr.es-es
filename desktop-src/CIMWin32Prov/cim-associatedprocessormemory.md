---
description: La clase AssociatedProcessorMemory de CIM asocia el procesador y la memoria del sistema, o la memoria \_ caché de un procesador.
ms.assetid: a4c28a0a-e4cc-4db2-bd77-b7b5023eace6
ms.tgt_platform: multiple
title: CIM_AssociatedProcessorMemory clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedProcessorMemory
- CIM_AssociatedProcessorMemory.Antecedent
- CIM_AssociatedProcessorMemory.Dependent
- CIM_AssociatedProcessorMemory.BusSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 23b2ee879752365e3100866a4ea82a33b01a2236f4f3266539e79b3ee37b94e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701165"
---
# <a name="cim_associatedprocessormemory-class"></a>Cim \_ AssociatedProcessorMemory (clase)

La **clase \_ AssociatedProcessorMemory** de CIM asocia el procesador y la memoria del sistema, o la memoria caché de un procesador.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[abstract, UUID("{464FFAB1-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedProcessorMemory : CIM_AssociatedMemory
{
  CIM_Memory    REF Antecedent;
  CIM_Processor REF Dependent;
  uint32            BusSpeed;
};
```

## <a name="members"></a>Miembros

La **clase \_ AssociatedProcessorMemory** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ AssociatedProcessorMemory** de CIM tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Memoria CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Memoria [**CIM \_ que**](cim-memory.md) describe la memoria instalada en un dispositivo o asociada a él.

Esta propiedad se hereda de [**\_ CIM AssociatedMemory.**](cim-associatedmemory.md)

</dd> <dt>

**BusSpeed**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahercios")
</dt> </dl>

Velocidad del bus, en megahercios (MHz), entre el procesador y la memoria.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Procesador CIM \_**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Procesador [**CIM \_ que**](cim-processor.md) describe el procesador que tiene acceso a la memoria o usa la memoria caché.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La **clase \_ CIM AssociatedProcessorMemory** se deriva de [**CIM \_ AssociatedMemory**](cim-associatedmemory.md).

WMI no implementa esta clase. Para obtener más información sobre las clases derivadas de **CIM \_ AssociatedProcessorMemory**, vea [Clases win32](win32-provider.md).

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ AssociatedMemory**](cim-associatedmemory.md)
</dt> </dl>

 

