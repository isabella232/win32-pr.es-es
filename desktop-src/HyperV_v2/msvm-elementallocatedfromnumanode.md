---
description: Asocia una instancia de un recurso asignado al nodo NUMA físico desde el que se asignó.
ms.assetid: 811ed19f-9084-4e30-8604-860d2bf722c7
title: Msvm_ElementAllocatedFromNumaNode (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromNumaNode
- Msvm_ElementAllocatedFromNumaNode.Antecedent
- Msvm_ElementAllocatedFromNumaNode.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 98940306f25d46c6af1be31133ee336765f8f1a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911025"
---
# <a name="msvm_elementallocatedfromnumanode-class"></a>MSVM \_ ElementAllocatedFromNumaNode (clase)

Asocia una instancia de un recurso asignado al nodo NUMA físico desde el que se asignó.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromNumaNode : CIM_Dependency
{
  Msvm_NumaNode      REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ ElementAllocatedFromNumaNode** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ ElementAllocatedFromNumaNode** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ NumaNode**](msvm-numanode.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Nodo NUMA físico.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Recurso asignado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

