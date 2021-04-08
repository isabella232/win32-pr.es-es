---
description: Representa una asociación en la que \_ se asigna una instancia de ResourceAllocationSettingData de CIM desde un grupo de recursos.
ms.assetid: ca9060e5-4434-4302-a840-a7d9cf5db714
title: CIM_ResourceAllocationFromPool (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourceAllocationFromPool
- CIM_ResourceAllocationFromPool.Antecedent
- CIM_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 09bd7b70d49d2304062d35d29586fea886c86a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002488"
---
# <a name="cim_resourceallocationfrompool-class"></a>\_Clase ResourceAllocationFromPool de CIM

Representa una asociación en la que se asigna una instancia de [**\_ ResourceAllocationSettingData de CIM**](cim-resourceallocationsettingdata.md) desde un grupo de recursos.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::Resource"), AMENDMENT]
class CIM_ResourceAllocationFromPool : CIM_Dependency
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a>Miembros

La clase **CIM \_ ResourceAllocationFromPool** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ ResourceAllocationFromPool** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ResourcePool**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Grupo de recursos.

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ResourceAllocationSettingData**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")
</dt> </dl>

Los datos de asignación de recursos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia de CIM \_**](cim-dependency.md)
</dt> </dl>

 

