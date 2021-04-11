---
description: Asociación que se usa para establecer &\# 0034; parte de&\# 0034; relaciones entre una instancia de MSVM \_ VirtualEthernetSwitchSettingData y una o varias instancias de MSVM \_ EthernetSwitchFeatureSettingData.
ms.assetid: b3adac33-056e-4f39-8022-5d9ef78370e9
title: Msvm_VirtualEthernetSwitchSettingDataComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingDataComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.GroupComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8fa53514c5db3128e13f0504bb883cb802021c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276174"
---
# <a name="msvm_virtualethernetswitchsettingdatacomponent-class"></a>MSVM \_ VirtualEthernetSwitchSettingDataComponent (clase)

Asociación que se usa para establecer las relaciones entre una instancia de [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) y una o varias instancias de [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingDataComponent : CIM_Component
{
  Msvm_VirtualEthernetSwitchSettingData REF GroupComponent;
  Msvm_EthernetSwitchFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ VirtualEthernetSwitchSettingDataComponent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ VirtualEthernetSwitchSettingDataComponent** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **MSVM \_ VirtualEthernetSwitchSettingData**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agregado**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia a una instancia de la clase [**MSVM \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md) que representa un puerto Ethernet.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **MSVM \_ EthernetSwitchFeatureSettingData**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Referencia a una instancia de la clase [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) que representa la configuración aplicada al modificador.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

