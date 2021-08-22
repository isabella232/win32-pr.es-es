---
description: Establezca una relación entre una instancia de la clase Msvm \_ EmulatedEthernetPortSettingData o Msvm SyntheticEthernetPortSettingData con una instancia de la clase \_ \_ GuestNetworkAdapterConfiguration de Msvm.
ms.assetid: 82262e67-1e72-4bad-974e-f18d00a94c3d
title: Msvm_SettingDataComponent clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingDataComponent
- Msvm_SettingDataComponent.GroupComponent
- Msvm_SettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c96ad2d24291226934e50b338f2a0a4d77e9d966d2a821b73ad38d671b50fa04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950484"
---
# <a name="msvm_settingdatacomponent-class"></a>Clase SettingDataComponent de Msvm \_

Establezca una relación entre una instancia de la clase [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) o [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) con una instancia de la clase [**\_ GuestNetworkAdapterConfiguration de Msvm.**](msvm-guestnetworkadapterconfiguration.md)

La sintaxis siguiente se Managed Object Format código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData     REF GroupComponent;
  Msvm_GuestNetworkAdapterConfiguration REF PartComponent;
};
```

## <a name="members"></a>Miembros

La **clase \_ SettingDataComponent de Msvm** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SettingDataComponent de Msvm** tiene estas propiedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **\_ Cim ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referencia a una instancia de la clase [**Msvm \_ EmulatedEthernetPortSettingData**](msvm-emulatedethernetportsettingdata.md) o [**Msvm \_ SyntheticEthernetPortSettingData**](msvm-syntheticethernetportsettingdata.md) que representa un puerto Ethernet.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de datos: **[ **Msvm \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Referencia a una instancia de la clase [**\_ GuestNetworkAdapterConfiguration de Msvm**](msvm-guestnetworkadapterconfiguration.md) que representa una configuración del adaptador de red invitado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

