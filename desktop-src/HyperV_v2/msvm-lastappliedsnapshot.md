---
description: Representa una asociación entre un sistema virtual y los datos de configuración de la instantánea que se aplicó más recientemente al sistema virtual.
ms.assetid: 9231b441-20c4-468b-905f-5baabc32a8cc
title: Msvm_LastAppliedSnapshot clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LastAppliedSnapshot
- Msvm_LastAppliedSnapshot.Antecedent
- Msvm_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e34260e0bfe77b847437e9b3d49794334b3897d8425981fecb2032098e24fa7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521925"
---
# <a name="msvm_lastappliedsnapshot-class"></a>Clase Msvm \_ LastAppliedSnapshot

Representa una asociación entre un sistema virtual y los datos de configuración de la instantánea que se aplicó más recientemente al sistema virtual.

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LastAppliedSnapshot : CIM_LastAppliedSnapshot
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ LastAppliedSnapshot** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ LastAppliedSnapshot** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Override**, **Min** ( 0 ), **Max** ( 1 )
</dt> </dl>

Referencia a una instancia de la clase [**\_ Msvm VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa la instantánea del sistema virtual que se aplicó por última vez al sistema virtual. Esta propiedad se hereda de la **dependencia \_ CIM**.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Override**, **Min** ( 0 ), **Max** ( 1 )
</dt> </dl>

Referencia a una instancia de la clase [**\_ ComputerSystem de Msvm**](msvm-computersystem.md) que representa el sistema virtual en el que se aplicó la instantánea del sistema virtual representada por la propiedad **Antecedentes** más recientemente. Esta propiedad se hereda de la **dependencia \_ CIM**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




