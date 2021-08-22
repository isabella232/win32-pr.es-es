---
description: Asociación que se usa para establecer relaciones entre una instancia de Msvm EmulatedEthernetPortSettingData y una o varias instancias de \_ Msvm \_ EthernetSwitchFeatureSettingData.
ms.assetid: A2929D81-ED86-4C5A-9280-276204EDE89B
title: Msvm_EthernetPortFailoverSettingDataComponent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortFailoverSettingDataComponent
- Msvm_EthernetPortFailoverSettingDataComponent.GroupComponent
- Msvm_EthernetPortFailoverSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00653b19cffabeb658e7727332b7e6fe1b2e23be7ff0c4eba298ef198404234c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531525"
---
# <a name="msvm_ethernetportfailoversettingdatacomponent-class"></a>Clase Msvm \_ EthernetPortFailoverSettingDataComponent

Asociación que se usa para establecer relaciones entre una instancia de [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) y una o varias instancias de [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortFailoverSettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData      REF GroupComponent;
  Msvm_FailoverNetworkAdapterSettingData REF PartComponent;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ EthernetPortFailoverSettingDataComponent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ EthernetPortFailoverSettingDataComponent** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ Cim ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia a una instancia de la clase [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) o [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) que representa el puerto Ethernet.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ FailoverNetworkAdapterSettingData**](msvm-failovernetworkadaptersettingdata.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Referencia a una instancia de la clase [**\_ FailoverNetworkAdapterSettingData de Msvm**](msvm-failovernetworkadaptersettingdata.md) que representa la configuración del adaptador de red invitado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

