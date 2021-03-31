---
description: Representa la configuración de formación de equipos NIC del conmutador.
ms.assetid: 7a48bdae-1953-4011-aaa8-1e3ca73494ff
title: Msvm_VirtualEthernetSwitchNicTeamingSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingSettingData
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.TeamingMode
- Msvm_VirtualEthernetSwitchNicTeamingSettingData.LoadBalancingAlgorithm
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 45f306f9ddb388ef4e8124d7ab2c8dd125a62e01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819491"
---
# <a name="msvm_virtualethernetswitchnicteamingsettingdata-class"></a>MSVM \_ VirtualEthernetSwitchNicTeamingSettingData (clase)

Representa la configuración de formación de equipos NIC del conmutador.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("17AD26F1-DD6F-4ED9-BD2F-3750ADE6B68B"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Nic Teaming Settings"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingSettingData : Msvm_EthernetSwitchFeatureSettingData
{
  UINT32 TeamingMode = 0;
  UINT32 LoadBalancingAlgorithm = 5;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ VirtualEthernetSwitchNicTeamingSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **MSVM \_ VirtualEthernetSwitchNicTeamingSettingData** tiene estas propiedades.

<dl> <dt>

**LoadBalancingAlgorithm**
</dt> <dd> <dl> <dt>

Tipo de datos: **UINT32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Algoritmo de equilibrio de carga.

</dd> <dt>

**TeamingMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **UINT32**
</dt> <dt>

Tipo de acceso: lectura/escritura
</dt> <dt>

Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Modo de formación de equipos.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md)
</dt> </dl>

 

 




