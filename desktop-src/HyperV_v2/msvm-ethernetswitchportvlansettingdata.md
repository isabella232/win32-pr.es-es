---
description: Representa los datos de configuración de LAN virtual (VLAN).
ms.assetid: c3a49021-5256-4751-a5a5-81bf1c6d6e6d
title: Msvm_EthernetSwitchPortVlanSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortVlanSettingData
- Msvm_EthernetSwitchPortVlanSettingData.InstanceID
- Msvm_EthernetSwitchPortVlanSettingData.Caption
- Msvm_EthernetSwitchPortVlanSettingData.Description
- Msvm_EthernetSwitchPortVlanSettingData.ElementName
- Msvm_EthernetSwitchPortVlanSettingData.OperationMode
- Msvm_EthernetSwitchPortVlanSettingData.AccessVlanId
- Msvm_EthernetSwitchPortVlanSettingData.NativeVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PvlanMode
- Msvm_EthernetSwitchPortVlanSettingData.PrimaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PruneVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.TrunkVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanIdArray
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8c4d9c3c3101cb7593f54e8624a2d7e316cb27378b0ad504cdf8364b03020efb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523775"
---
# <a name="msvm_ethernetswitchportvlansettingdata-class"></a>Clase Msvm \_ EthernetSwitchPortVlanSettingData

Representa los datos de configuración de LAN virtual (VLAN).

La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("952C5004-4465-451C-8CB8-FA9AB382B773"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VLAN Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortVlanSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port VLAN Settings";
  string Description = "Represents the vlan setting data.";
  string ElementName = "Ethernet Switch Port VLAN Settings";
  uint32 OperationMode = 0;
  uint16 AccessVlanId = 0;
  uint16 NativeVlanId = 0;
  uint32 PvlanMode = 0;
  uint16 PrimaryVlanId = 0;
  uint16 SecondaryVlanId = 0;
  uint16 PruneVlanIdArray[] = {};
  uint16 TrunkVlanIdArray[] = {};
  uint16 SecondaryVlanIdArray[] = {};
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ EthernetSwitchPortVlanSettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ EthernetSwitchPortVlanSettingData** tiene estas propiedades.

<dl> <dt>

**AccessVlanId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica el identificador de VLAN en modo de acceso.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)de CIM y siempre se establece en "Ethernet Switch Port VLAN Configuración".

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "Representa los datos de configuración de vlan".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)de CIM y siempre se establece en "Ethernet Switch Port VLAN Configuración".

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **Clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**NativeVlanId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica el identificador de VLAN en modo de tronco.

</dd> <dt>

**OperationMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica el modo de operación de VLAN.

<dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

**Acceso** (1)


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

**Tronco** (2)


</dt> <dd></dd> <dt>

<span id="Private"></span><span id="private"></span><span id="PRIVATE"></span>

**Privado** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**PrimaryVlanId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica el identificador de VLAN principal en modo privado.

</dd> <dt>

**PruneVlanIdArray**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica el mapa de bits del identificador de VLAN en modo de tronco.

</dd> <dt>

**PvlanMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica el modo VLAN privado.

<dt>

<span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>

**Aislado** (1)


</dt> <dd></dd> <dt>

<span id="Community"></span><span id="community"></span><span id="COMMUNITY"></span>

**Community** (2)


</dt> <dd></dd> <dt>

<span id="Promiscuous"></span><span id="promiscuous"></span><span id="PROMISCUOUS"></span>

**Promiscuous** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**SecondaryVlanId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica el identificador de VLAN secundario en modo privado.

</dd> <dt>

**SecondaryVlanIdArray**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica el mapa de bits del identificador de VLAN secundario en modo privado.

</dd> <dt>

**TrunkVlanIdArray**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica el mapa de bits del identificador de VLAN del tronco en modo de tronco.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

