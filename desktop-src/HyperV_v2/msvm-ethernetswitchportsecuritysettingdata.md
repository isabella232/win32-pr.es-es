---
description: Representa los datos de configuración de características de seguridad.
ms.assetid: 98e0de24-ccdc-4fc7-86a5-b68d454fde9d
title: Msvm_EthernetSwitchPortSecuritySettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortSecuritySettingData
- Msvm_EthernetSwitchPortSecuritySettingData.InstanceID
- Msvm_EthernetSwitchPortSecuritySettingData.Caption
- Msvm_EthernetSwitchPortSecuritySettingData.Description
- Msvm_EthernetSwitchPortSecuritySettingData.ElementName
- Msvm_EthernetSwitchPortSecuritySettingData.AllowMacSpoofing
- Msvm_EthernetSwitchPortSecuritySettingData.EnableDhcpGuard
- Msvm_EthernetSwitchPortSecuritySettingData.EnableRouterGuard
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorMode
- Msvm_EthernetSwitchPortSecuritySettingData.MonitorSession
- Msvm_EthernetSwitchPortSecuritySettingData.AllowIeeePriorityTag
- Msvm_EthernetSwitchPortSecuritySettingData.VirtualSubnetId
- Msvm_EthernetSwitchPortSecuritySettingData.AllowTeaming
- Msvm_EthernetSwitchPortSecuritySettingData.TeamName
- Msvm_EthernetSwitchPortSecuritySettingData.TeamNumber
- Msvm_EthernetSwitchPortSecuritySettingData.EnableFixSpeed10G
- Msvm_EthernetSwitchPortSecuritySettingData.Reserved
- Msvm_EthernetSwitchPortSecuritySettingData.DynamicIPAddressLimit
- Msvm_EthernetSwitchPortSecuritySettingData.StormLimit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 214a86513462e70025f0bcb6403faecc3b6663463dbef8c4cb9d1ea60a9c8f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681445"
---
# <a name="msvm_ethernetswitchportsecuritysettingdata-class"></a>Clase Msvm \_ EthernetSwitchPortSecuritySettingData

Representa los datos de configuración de características de seguridad.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("776E0BA7-94A1-41C8-8F28-951F524251B5"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Security Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortSecuritySettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Security Settings";
  string  Description = "Represents the security feature setting data.";
  string  ElementName = "Ethernet Switch Port Security Settings";
  boolean AllowMacSpoofing = FALSE;
  boolean EnableDhcpGuard = FALSE;
  boolean EnableRouterGuard = FALSE;
  uint8   MonitorMode = 0;
  uint8   MonitorSession = 0;
  boolean AllowIeeePriorityTag = FALSE;
  uint32  VirtualSubnetId = 0;
  boolean AllowTeaming = FALSE;
  string  TeamName = ;
  uint32  TeamNumber = 0;
  boolean EnableFixSpeed10G = FALSE;
  boolean Reserved = FALSE;
  uint32  DynamicIPAddressLimit = 0;
  uint32  StormLimit = 0;
};
```

## <a name="members"></a>Miembros

La **clase Msvm \_ EthernetSwitchPortSecuritySettingData** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase Msvm \_ EthernetSwitchPortSecuritySettingData** tiene estas propiedades.

<dl> <dt>

**AllowIeeePriorityTag**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica si el tráfico hacia y desde el puerto conserva la información 802.1P. Contiene **True** si el tráfico hacia y desde el puerto conserva la información 802.1P o **False en caso** contrario. El valor predeterminado es **False**.

</dd> <dt>

**AllowMacSpoofing**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Indica si el puerto permitirá la suplantación de MAC. Si esta propiedad es **True**, el puerto permitirá la suplantación de direcciones MAC. Se permiten todos los valores válidos de dirección MAC de unidifusión. Si esta propiedad es **False**, el puerto solo permitirá que se usen las direcciones MAC configuradas en la administración de Hyper-V. El valor predeterminado es **False**.

</dd> <dt>

**AllowTeaming**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Indica si las NIC conectadas al puerto pueden formar parte de un equipo. Esto solo se aplica a las NIC conectadas a máquinas virtuales. Contiene **True si** se permite la formación de equipos NIC o False en **caso** contrario. El valor predeterminado es **False**.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ MANAGEDElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)de CIM y siempre se establece en "Ethernet Switch Port Security Configuración".

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "Representa los datos de configuración de características de seguridad".

</dd> <dt>

**DynamicIPAddressLimit**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (12), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Define el límite para el número de direcciones IP dinámicas aprendidas. El valor predeterminado es none.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ MANAGEDElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)de CIM y siempre se establece en "Ethernet Switch Port Security Configuración".

</dd> <dt>

**EnableDhcpGuard**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica si las ofertas DHCP están bloqueadas desde el puerto. Contiene **True si** las ofertas DHCP están bloqueadas desde el puerto o **False** en caso contrario. El valor predeterminado es **False**.

</dd> <dt>

**EnableFixSpeed10G**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Establezca en TRUE si la velocidad fija 10G está habilitada de lo contrario, FALSE. El valor predeterminado es FALSE.

> [!Note]  
> Propiedad agregada en Windows 10.

 

</dd> <dt>

**EnableRouterGuard**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica si los anuncios de enrutador y los redireccionamientos del enrutador están bloqueados en el puerto. Contiene **True si** los anuncios de enrutador y los redireccionamientos del enrutador se bloquean desde el puerto o False en **caso** contrario. El valor predeterminado es **False**.

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

**MonitorMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Esto indica el modo de supervisión del puerto.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Ninguno** (0)


</dt> <dd></dd> <dt>

<span id="Destination"></span><span id="destination"></span><span id="DESTINATION"></span>

**Destino** (1)


</dt> <dd></dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>

**Origen** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**MonitorSession**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint8**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Especifica el identificador de la sesión de supervisión a la que pertenece este puerto.

</dd> <dt>

**Reserved**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**En desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("Sin valor"), **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)
</dt> </dl>

Reservada

> [!Note]  
> Propiedad agregada en Windows 10.

 

</dd> <dt>

**StormLimit**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (11), **InterfaceVersion** (2), **InterfaceRevision** (0)
</dt> </dl>

Define el límite de paquetes por segundo para el tráfico de difusión y multidifusión. El valor predeterminado es none.

</dd> <dt>

**TeamName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (127), **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Reservado para uso futuro.

</dd> <dt>

**TeamNumber**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (10), **InterfaceVersion** (1), **InterfaceRevision** (0)
</dt> </dl>

Reservado para uso futuro.

</dd> <dt>

**VirtualSubnetId**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0), [**MinValue**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**MaxValue**](/windows/desktop/WmiSdk/standard-qualifiers) (16777215)
</dt> </dl>

Especifica el identificador de la subred virtual de la que es miembro el puerto. El valor predeterminado es none.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

