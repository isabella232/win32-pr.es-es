---
description: Representa una parte de una relación entre una instancia de CIM \_ VirtualSystemSettingData y un conjunto de instancias de \_ ResourceAllocationSettingData de CIM.
ms.assetid: 4f167517-079e-4b5f-885a-741ac1d1dc71
title: CIM_VirtualSystemSettingDataComponent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingDataComponent
- CIM_VirtualSystemSettingDataComponent.GroupComponent
- CIM_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 54ceb24806b21a06a9a0e8e82cf5fbb6ca96776d645b45679edb3adfcbd46c3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118150291"
---
# <a name="cim_virtualsystemsettingdatacomponent-class"></a>Cim \_ VirtualSystemSettingDataComponent (clase)

Representa una parte de una relación entre una instancia [**de CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) y un conjunto de instancias [**de \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) de CIM.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingDataComponent : CIM_Component
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM VirtualSystemSettingDataComponent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase CIM \_ VirtualSystemSettingDataComponent** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Referencia al objeto [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) de nivel superior de la configuración del sistema virtual.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **\_ Cim ResourceAllocationSettingData**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Referencia al objeto [**\_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) de CIM que representa una parte de la configuración del sistema virtual.

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

[**Componente \_ CIM**](cim-component.md)
</dt> </dl>

 

