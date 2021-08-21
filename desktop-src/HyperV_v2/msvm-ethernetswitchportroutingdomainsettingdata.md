---
description: Representa los datos de configuración del dominio de enrutamiento.
ms.assetid: 6216cc4e-b2aa-4344-b8fa-489b986c14be
title: Msvm_EthernetSwitchPortRoutingDomainSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortRoutingDomainSettingData
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainGuid
- Msvm_EthernetSwitchPortRoutingDomainSettingData.RoutingDomainName
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdList
- Msvm_EthernetSwitchPortRoutingDomainSettingData.IsolationIdNameList
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b0bc01c7e771996d46c29b0f6341e3a535860c4c36996562e7e526ca5db59a2e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523845"
---
# <a name="msvm_ethernetswitchportroutingdomainsettingdata-class"></a>Clase Msvm \_ EthernetSwitchPortRoutingDomainSettingData

Representa los datos de configuración del dominio de enrutamiento.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("BF874DF0-F729-4312-A0FA-194271B88990"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Routing Domain Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortRoutingDomainSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string RoutingDomainGuid = "";
  string RoutingDomainName = "";
  uint32 IsolationIdList[] = {};
  string IsolationIdNameList[] = {};
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ EthernetSwitchPortRoutingDomainSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ EthernetSwitchPortRoutingDomainSettingData** tiene estas propiedades.

<dl> <dt>

**IsolationIdList**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (3), [**Versión**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisión**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Identificadores de VLAN o VirtualSubnetId para los dominios de enrutamiento.

</dd> <dt>

**IsolationIdNameList**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (4), [**Versión**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisión**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Matriz de nombres descriptivos de VirtualSubnetId o VLAN.

</dd> <dt>

**RoutingDomainGuid**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (38), **WmiDataId** (1), [**Versión**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisión**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

GUID del dominio de enrutamiento.

</dd> <dt>

**RoutingDomainName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (2), [**Versión**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisión**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Nombre descriptivo del dominio de enrutamiento.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espacio de nombres<br/>                | Virtualización \\ raíz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

