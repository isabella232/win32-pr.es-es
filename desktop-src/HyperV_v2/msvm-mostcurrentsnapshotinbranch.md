---
description: Asocia una instancia de la clase Msvm ComputerSystem o Msvm PlannedComputerSystem que representa un sistema virtual, con una instancia de la clase \_ \_ Msvm VirtualSystemSettingData que representa la instantánea del sistema virtual que es la instantánea más actual en una rama de \_ instantáneas dependientes.
ms.assetid: EEB9D2C1-C463-4EFE-862F-95E8AD8E1753
title: Msvm_MostCurrentSnapshotInBranch clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MostCurrentSnapshotInBranch
- Msvm_MostCurrentSnapshotInBranch.Antecedent
- Msvm_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 16e9ec84be25e9cd7967debc78b6413c8c8a9606d5e7dbbeecbbdc6e564b994a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117811455"
---
# <a name="msvm_mostcurrentsnapshotinbranch-class"></a>Clase Msvm \_ MostCurrentSnapshotInBranch

Asocia una instancia de la clase [**Msvm \_ ComputerSystem**](msvm-computersystem.md) o [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) que representa un sistema virtual, con una instancia de la clase [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa la instantánea del sistema virtual que es la instantánea más actual en una rama de instantáneas dependientes.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Experimental, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MostCurrentSnapshotInBranch : CIM_MostCurrentSnapshotInBranch
{
  CIM_ComputerSystem            REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ MostCurrentSnapshotInBranch** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ MostCurrentSnapshotInBranch** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referencia a una instancia de la clase [**Msvm \_ ComputerSystem**](msvm-computersystem.md) o [**Msvm \_ PlannedComputerSystem**](msvm-plannedcomputersystem.md) que representa el sistema virtual. Esta propiedad se hereda de la [**dependencia \_ CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referencia a una instancia de la clase [**\_ Msvm VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa la instantánea del sistema virtual que es la instantánea más actual en una rama de instantáneas dependientes. Esta propiedad se hereda de la [**dependencia \_ CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

