---
description: Representa una asociación entre un sistema virtual y la instantánea más reciente del sistema. Esta asociación solo puede existir si el sistema virtual se creó mediante una instantánea o si se creó una instantánea desde el sistema virtual.
ms.assetid: e6040818-84cf-4cec-ab7b-a733fe5d01d2
title: CIM_MostCurrentSnapshotInBranch clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MostCurrentSnapshotInBranch
- CIM_MostCurrentSnapshotInBranch.Antecedent
- CIM_MostCurrentSnapshotInBranch.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: de94bf0e6f88240ac89eb62de881540f5c747b7a1d0ec13307e7e5d35fe53da4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694975"
---
# <a name="cim_mostcurrentsnapshotinbranch-class"></a>Cim \_ MostCurrentSnapshotInBranch (clase)

Representa una asociación entre un sistema virtual y la instantánea más reciente del sistema. Esta asociación solo puede existir si el sistema virtual se creó mediante una instantánea o si se creó una instantánea desde el sistema virtual.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Experimental, Version("2.16.0"), AMENDMENT]
class CIM_MostCurrentSnapshotInBranch : CIM_Dependency
{
  CIM_ComputerSystem           REF Antecedent;
  CIM_VirtualSystemSettingData REF Dependent;
};
```

## <a name="members"></a>Miembros

La **clase CIM \_ MostCurrentSnapshotInBranch** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ MostCurrentSnapshotInBranch** tiene estas propiedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ ComputerSystem**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedente"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referencia a la instancia de [**CIM \_ ComputerSystem**](cim-computersystem.md) que representa el sistema virtual.

</dd> <dt>

**Dependiente**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referencia a la instancia de [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa la instantánea del sistema virtual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
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

 

