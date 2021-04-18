---
description: Asocia una instancia de una asignación de recursos al grupo de recursos desde el que se asigna.
ms.assetid: A2B3996D-7886-4B5F-BC89-EFDC1A48249B
title: Msvm_ResourceAllocationFromPool (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourceAllocationFromPool
- Msvm_ResourceAllocationFromPool.Antecedent
- Msvm_ResourceAllocationFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5bb3db9bce86731b12730966a7a2f6d1c9dc8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687777"
---
# <a name="msvm_resourceallocationfrompool-class"></a>MSVM \_ ResourceAllocationFromPool (clase)

Asocia una instancia de una asignación de recursos al grupo de recursos desde el que se asigna.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourceAllocationFromPool : CIM_ResourceAllocationFromPool
{
  CIM_ResourcePool                  REF Antecedent;
  CIM_ResourceAllocationSettingData REF Dependent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ ResourceAllocationFromPool** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ ResourceAllocationFromPool** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **invalidación**, **máx** . (1)
</dt> </dl>

Grupo de recursos. Esta propiedad se hereda de [**\_ ResourceAllocationFromPool CIM**](/previous-versions//cc150673(v=vs.85)).

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Asignación de recursos. Esta propiedad se hereda de [**\_ ResourceAllocationFromPool CIM**](/previous-versions//cc150673(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Observaciones

El acceso a la clase **MSVM \_ ResourceAllocationFromPool** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_RESOURCEALLOCATIONFROMPOOL CIM**](cim-resourceallocationfrompool.md)
</dt> <dt>

[**\_RESOURCEALLOCATIONFROMPOOL CIM**](/previous-versions//cc150673(v=vs.85))
</dt> <dt>

[**MSVM \_ ResourceAllocationFromPool (V1)**](/previous-versions/windows/desktop/virtual/msvm-resourceallocationfrompool)
</dt> <dt>

[Clases de administración de recursos](resource-management-classes.md)
</dt> </dl>

 

