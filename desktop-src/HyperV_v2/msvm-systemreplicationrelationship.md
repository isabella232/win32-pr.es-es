---
description: Representa una asociación entre una instancia de Msvm ComputerSystem que representa la máquina virtual y una instancia de \_ Msvm ReplicationRelationship que representa una relación de replicación de la \_ máquina virtual.
ms.assetid: 23E7BF91-9527-434C-A571-05879E83950E
title: Msvm_SystemReplicationRelationship clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemReplicationRelationship
- Msvm_SystemReplicationRelationship.Antecedent
- Msvm_SystemReplicationRelationship.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86040e6dc5676f6cd40b223f0a3cbd31864965722de957fda6ff1d140ad94b18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117810626"
---
# <a name="msvm_systemreplicationrelationship-class"></a>Clase \_ SystemReplicationRelationship de Msvm

Representa una asociación entre una instancia de [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa la máquina virtual y una instancia de [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) que representa una relación de replicación de la máquina virtual. Esta clase se deriva de la [**clase \_ de dependencia CIM.**](/windows/desktop/CIMWin32Prov/cim-dependency)

La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemReplicationRelationship : CIM_Dependency
{
  Msvm_ComputerSystem          REF Antecedent;
  Msvm_ReplicationRelationship REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase \_ SystemReplicationRelationship de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SystemReplicationRelationship de Msvm** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **Msvm \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) \_ ("CIM Dependency.Antecedent")
</dt> </dl>

Referencia a la instancia de la [**clase \_ ComputerSystem de Msvm**](msvm-computersystem.md) que representa la máquina virtual.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ ReplicationRelationship de Msvm**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) \_ ("CIM Dependency.Dependent")
</dt> </dl>

Referencia a la instancia de la clase [**\_ ReplicationRelationship de Msvm**](msvm-replicationrelationship.md) que representa la relación de replicación de un sistema virtual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                            |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                                 |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Dependencia \_ cim**](cim-dependency.md)
</dt> <dt>

[**Dependencia \_ cim**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

