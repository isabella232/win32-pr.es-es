---
description: Asocia un sistema virtual a una instantánea que se capturó del sistema virtual.
ms.assetid: CF1C1C04-02BC-4AC3-8327-FEE54ECE8541
title: Msvm_SnapshotOfVirtualSystem (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SnapshotOfVirtualSystem
- Msvm_SnapshotOfVirtualSystem.Antecedent
- Msvm_SnapshotOfVirtualSystem.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bd006093347d7eb9354944409082a0e069b0cd54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001491"
---
# <a name="msvm_snapshotofvirtualsystem-class"></a>MSVM \_ SnapshotOfVirtualSystem (clase)

Asocia un sistema virtual a una instantánea que se capturó del sistema virtual.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SnapshotOfVirtualSystem : CIM_SnapshotOfVirtualSystem
{
  Msvm_ComputerSystem           REF Antecedent;
  Msvm_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ SnapshotOfVirtualSystem** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ SnapshotOfVirtualSystem** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ ComputerSystem**](msvm-computersystem.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de la clase [**MSVM \_ ComputerSystem**](msvm-computersystem.md) que representa el sistema virtual. Esta propiedad se deriva de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Dependientes**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Referencia a una instancia de la clase [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa la instantánea. Esta propiedad se deriva de [**la \_ dependencia CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> </dl>

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

[**\_SNAPSHOTOFVIRTUALSYSTEM CIM**](cim-snapshotofvirtualsystem.md)
</dt> <dt>

[**CreateSnapshot**](createsnapshot-msvm-virtualsystemsnapshotservice.md)
</dt> </dl>

 

