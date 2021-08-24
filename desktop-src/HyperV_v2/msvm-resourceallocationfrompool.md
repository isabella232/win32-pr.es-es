---
description: Asocia una instancia de una asignación de recursos al grupo de recursos desde el que se asigna.
ms.assetid: A2B3996D-7886-4B5F-BC89-EFDC1A48249B
title: Msvm_ResourceAllocationFromPool clase
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
ms.openlocfilehash: c8d3913f03560262309084d99ea97b44a165944d4b71acdcac17e2a39bfd44a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148208"
---
# <a name="msvm_resourceallocationfrompool-class"></a>Clase \_ ResourceAllocationFromPool de Msvm

Asocia una instancia de una asignación de recursos al grupo de recursos desde el que se asigna.

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

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

La **clase \_ ResourceAllocationFromPool de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ ResourceAllocationFromPool de Msvm** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Cim \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Override**, **Max** (1)
</dt> </dl>

Grupo de recursos. Esta propiedad se hereda de [**\_ CIM ResourceAllocationFromPool.**](/previous-versions//cc150673(v=vs.85))

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ Cim ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Asignación de recursos. Esta propiedad se hereda de [**\_ CIM ResourceAllocationFromPool.**](/previous-versions//cc150673(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a **la clase \_ ResourceAllocationFromPool de Msvm** podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ ResourceAllocationFromPool**](cim-resourceallocationfrompool.md)
</dt> <dt>

[**CIM \_ ResourceAllocationFromPool**](/previous-versions//cc150673(v=vs.85))
</dt> <dt>

[**Msvm \_ ResourceAllocationFromPool (V1)**](/previous-versions/windows/desktop/virtual/msvm-resourceallocationfrompool)
</dt> <dt>

[Clases de administración de recursos](resource-management-classes.md)
</dt> </dl>

 

