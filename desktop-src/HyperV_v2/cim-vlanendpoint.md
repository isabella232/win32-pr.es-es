---
description: Un punto de conexión en un conmutador o una estación de conexión que se asigna a una VLAN o que acepta tráfico de una o varias VLAN.
ms.assetid: 20943be3-35c3-4bf5-8f1a-d4095fa6897e
title: CIM_VLANEndpoint clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpoint
- CIM_VLANEndpoint.DesiredEndpointMode
- CIM_VLANEndpoint.OtherEndpointMode
- CIM_VLANEndpoint.OperationalEndpointMode
- CIM_VLANEndpoint.DesiredVLANTrunkEncapsulation
- CIM_VLANEndpoint.OtherTrunkEncapsulation
- CIM_VLANEndpoint.OperationalVLANTrunkEncapsulation
- CIM_VLANEndpoint.GVRPStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: caaedae456ded5b918a19b09f18ebcf7f32c0edf2c0eff6c16d8ff98519b1dd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068505"
---
# <a name="cim_vlanendpoint-class"></a>CIM \_ VLANEndpoint (clase)

Un punto de conexión en un conmutador o una estación de conexión que se asigna a una VLAN o que acepta tráfico de una o varias VLAN.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Network::VLAN"), AMENDMENT]
class CIM_VLANEndpoint : CIM_ProtocolEndpoint
{
  uint16 DesiredEndpointMode;
  string OtherEndpointMode;
  uint16 OperationalEndpointMode;
  uint16 DesiredVLANTrunkEncapsulation;
  string OtherTrunkEncapsulation;
  uint16 OperationalVLANTrunkEncapsulation;
  uint16 GVRPStatus;
};
```

## <a name="members"></a>Miembros

La **clase \_ CIM VLANEndpoint** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ CIM VLANEndpoint** tiene estas propiedades.

<dl> <dt>

**DesiredEndpointMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OperationalEndpointMode**", "**CIM \_ VLANEndpoint**.**OtherEndpointMode**")
</dt> </dl>

Modo VLAN solicitado para el punto de conexión.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

**Acceso** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

**Dynamic Auto** (3)


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

**Deseable dinámico** (4)


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

**Tronco** (5)


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

**Dot1Q Tunnel** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (7..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Vendor Reserved** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**DesiredVLANTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VLANEndpointCapabilities.SupportsTrunkEncapsulationNegotiation", "**CIM \_ VLANEndpoint**.**OperationalVLANTrunkEncapsulation**", "**CIM \_ VLANEndpoint**.**OtherTrunkEncapsulation**")
</dt> </dl>

Tipo de encapsulación VLAN solicitado.

> [!Note]  
> Esta propiedad solo se usa cuando el punto de conexión de VLAN está en modo de enlace de tronco.

 

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**No aplicable** (2)


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

**802.1q** (3)


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

**Cisco ISL** (4)


</dt> <dd></dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

**Negotiate** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (6..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Reservado por** el proveedor (32768.).


</dt> <dd></dd> </dl>

</dd> <dt>

**GVRPStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OperationalEndpointMode**, CIM \_ VLANEndpointCapabilities.Dot1QTagging")
</dt> </dl>

Indica si el protocolo de registro de VLAN de GARP (GVRP) está habilitado o deshabilitado en el punto de conexión del tronco.

> [!Note]  
> Esta propiedad solo se usa cuando el punto de conexión admite GVRP y el modo de enlace está habilitado.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**No aplicable** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Habilitado** (3)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deshabilitado** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**OperationalEndpointMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredEndpointMode**", "**\_ CIM VLANEndpoint**.**OtherEndpointMode**")
</dt> </dl>

Modo VLAN actual para el punto de conexión.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

**Acceso** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

**Dynamic Auto** (3)


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

**Deseable dinámico** (4)


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

**Tronco** (5)


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

**Dot1Q Tunnel** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (7..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Vendor Reserved** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**OperationalVLANTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OtherTrunkEncapsulation**", "**CIM \_ VLANEndpoint**.**DesiredVLANTrunkEncapsulation**")
</dt> </dl>

Tipo de encapsulación VLAN actual.

> [!Note]  
> Esta propiedad solo se usa cuando el punto de conexión de VLAN está en modo de enlace de tronco.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**No aplicable** (2)


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

**802.1q** (3)


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

**Cisco ISL** (4)


</dt> <dd></dd> <dt>

<span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>

**Negociación** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (6..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Reservado por** el proveedor (32768.).


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherEndpointMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredEndpointMode**", "**\_ CIM VLANEndpoint**.**OperationalEndpointMode**")
</dt> </dl>

El tipo de modelo de punto de conexión de VLAN compatible con VLANEndpoint cuando el valor de **DesiredEndpointMode** se establece en "1" (otro); de lo contrario, **NULL.**

</dd> <dt>

**OtherTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: lectura y escritura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredVLANTrunkEncapsulation**","**CIM \_ VLANEndpoint**.**OperationalVLANTrunkEncapsulation**")
</dt> </dl>

El tipo de encapsulación VLAN que admite el punto de conexión vlan cuando el valor de la propiedad **DesiredVLANTrunkEncapsulation** se establece en 1 (otro); de lo contrario, **NULL.**

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

[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md)
</dt> </dl>

 

