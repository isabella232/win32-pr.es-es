---
description: Asociación que se usa para establecer &0034;parte de&0034; relaciones entre una instancia de Msvm EthernetPortAllocationSettingData y una o varias instancias de \# \# \_ Msvm \_ EthernetSwitchFeatureSettingData.
ms.assetid: fab15342-a134-4d4a-9668-1272041614b9
title: Msvm_EthernetPortSettingDataComponent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortSettingDataComponent
- Msvm_EthernetPortSettingDataComponent.GroupComponent
- Msvm_EthernetPortSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 989d734d4c59d710c737c218b22591517347a8f5e434ff99e195887cbb4b6774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524845"
---
# <a name="msvm_ethernetportsettingdatacomponent-class"></a>Clase Msvm \_ EthernetPortSettingDataComponent

Asociación que se usa para establecer relaciones "parte de" entre una instancia de [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) y una o varias instancias de [**Msvm \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortSettingDataComponent : CIM_Component
{
  Msvm_EthernetPortAllocationSettingData    REF GroupComponent;
  Msvm_EthernetSwitchPortFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ EthernetPortSettingDataComponent** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ EthernetPortSettingDataComponent** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia a una instancia de la clase [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) que representa el puerto Ethernet.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Referencia a una instancia de la clase [**\_ Msvm EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) que representa la configuración de características aplicada al puerto.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

