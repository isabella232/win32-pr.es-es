---
description: Representa una asociación en la que un objeto LogicalElement de CIM \_ representa un recurso asignado desde un objeto \_ ResourcePool de CIM.
ms.assetid: 5e3c95c5-1cbb-40de-b285-0bf9b34a5ca8
title: CIM_ElementAllocatedFromPool clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementAllocatedFromPool
- CIM_ElementAllocatedFromPool.Antecedent
- CIM_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: aa1eb526054c665366211ec4fe3a5abdb1a001bddc098fba2c867479f23b18a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117812562"
---
# <a name="cim_elementallocatedfrompool-class"></a>Cim \_ ElementAllocatedFromPool (clase)

Representa una asociación en la que un [**objeto \_ LogicalElement**](cim-logicalelement.md) de CIM representa un recurso asignado desde un objeto [**\_ ResourcePool**](cim-resourcepool.md) de CIM.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ElementAllocatedFromPool : CIM_Dependency
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ ElementAllocatedFromPool** de CIM tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM ElementAllocatedFromPool** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ResourcePool**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Grupo de recursos.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ LogicalElement**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependiente")
</dt> </dl>

Recurso asignado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia \_ cim**](cim-dependency.md)
</dt> </dl>

 

