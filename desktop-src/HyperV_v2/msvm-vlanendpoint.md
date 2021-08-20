---
description: Representa el punto de conexión VLAN de un puerto de conmutador.
ms.assetid: 82F2EC39-0C9C-4A9D-A6C4-1543A62A341D
title: Msvm_VLANEndpoint clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VLANEndpoint
- Msvm_VLANEndpoint.InstanceID
- Msvm_VLANEndpoint.Caption
- Msvm_VLANEndpoint.Description
- Msvm_VLANEndpoint.ElementName
- Msvm_VLANEndpoint.InstallDate
- Msvm_VLANEndpoint.Name
- Msvm_VLANEndpoint.OperationalStatus
- Msvm_VLANEndpoint.StatusDescriptions
- Msvm_VLANEndpoint.Status
- Msvm_VLANEndpoint.HealthState
- Msvm_VLANEndpoint.CommunicationStatus
- Msvm_VLANEndpoint.DetailedStatus
- Msvm_VLANEndpoint.OperatingStatus
- Msvm_VLANEndpoint.PrimaryStatus
- Msvm_VLANEndpoint.EnabledState
- Msvm_VLANEndpoint.OtherEnabledState
- Msvm_VLANEndpoint.RequestedState
- Msvm_VLANEndpoint.EnabledDefault
- Msvm_VLANEndpoint.TimeOfLastStateChange
- Msvm_VLANEndpoint.AvailableRequestedStates
- Msvm_VLANEndpoint.TransitioningToState
- Msvm_VLANEndpoint.SystemCreationClassName
- Msvm_VLANEndpoint.SystemName
- Msvm_VLANEndpoint.CreationClassName
- Msvm_VLANEndpoint.NameFormat
- Msvm_VLANEndpoint.ProtocolType
- Msvm_VLANEndpoint.ProtocolIFType
- Msvm_VLANEndpoint.OtherTypeDescription
- Msvm_VLANEndpoint.DesiredEndpointMode
- Msvm_VLANEndpoint.OtherEndpointMode
- Msvm_VLANEndpoint.OperationalEndpointMode
- Msvm_VLANEndpoint.DesiredVLANTrunkEncapsulation
- Msvm_VLANEndpoint.OtherTrunkEncapsulation
- Msvm_VLANEndpoint.OperationalVLANTrunkEncapsulation
- Msvm_VLANEndpoint.GVRPStatus
- Msvm_VLANEndpoint.SupportedEndpointModes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: beeecdebe03a443c1da95a75598bc83b9c7e2f0952cd85ceaad1866e2200ef7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146238"
---
# <a name="msvm_vlanendpoint-class"></a>Clase VLANEndpoint de Msvm \_

Representa el punto de conexión VLAN de un puerto de conmutador. La configuración de este punto de conexión cambiará la forma en que el puerto del conmutador envía paquetes VLAN a través del conmutador.

La sintaxis siguiente se Managed Object Format código (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VLANEndpoint : CIM_VLANEndpoint
{
  string   InstanceID;
  String   Caption = "VLAN Endpoint";
  string   Description = "Microsoft VLAN Endpoint";
  String   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState = 5;
  String   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName = "Msvm_VirtualSwitch";
  string   SystemName;
  String   CreationClassName = "Msvm_VLANEndpoint";
  String   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 1;
  String   OtherTypeDescription = "Virtual Ethernet";
  uint16   DesiredEndpointMode;
  string   OtherEndpointMode;
  uint16   OperationalEndpointMode;
  uint16   DesiredVLANTrunkEncapsulation;
  string   OtherTrunkEncapsulation;
  uint16   OperationalVLANTrunkEncapsulation;
  uint16   GVRPStatus;
  uint16   SupportedEndpointModes[];
};
```

## <a name="members"></a>Miembros

La **clase \_ VLANEndpoint de Msvm** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ VLANEndpoint de Msvm** tiene estos métodos.



| Método                                                             | Descripción                         |
|:-------------------------------------------------------------------|:------------------------------------|
| [**RequestStateChange**](msvm-vlanendpoint-requeststatechange.md) | Solicita un cambio de estado.<br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ VLANEndpoint de Msvm** tiene estas propiedades.

<dl> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica los valores posibles para el parámetro *RequestedState* del [**método RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado. Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)). Esta propiedad puede ser no **NULL** si una implementación puede anunciar el conjunto de valores posibles como una función del estado actual. Esta propiedad será **Null si** una implementación no puede determinar el conjunto de valores posibles como una función del estado actual.

Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement.**](/previous-versions//cc136818(v=vs.85))

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin** conexión (6)
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Aplazar** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (.. )
</dt> </dl>

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **String**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "Punto de conexión VLAN".

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica la capacidad de la instrumentación para comunicarse con el elemento administrado subyacente. Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **String**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la clase o la subclase usada en la creación de una instancia de . Esta propiedad se hereda de [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)y siempre se establece en "Msvm \_ VLANEndpoint".

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "Punto de conexión vlan de Microsoft".

</dd> <dt>

**DesiredEndpointMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo escritura
</dt> </dl>

El modo VLAN deseado que se solicita para su uso. La propiedad **OperationalEndpointMode** proporciona el modo actual. Esta propiedad se hereda de [**\_ CIM VLANEndpoint.**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)



| Value                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reservado**</dt> <dt>0</dt> </dl>                       |                                                                                                                                                                                                                                                                                  |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Otros**</dt> <dt>1</dt> </dl>                                                       |                                                                                                                                                                                                                                                                                  |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <dt>**Acceso**</dt> <dt>2</dt> </dl>                                                   | Coloca el puerto de punto de conexión o conmutador en modo permanente sintrusión y negocia convertir el vínculo en un vínculo notrunk. El punto de conexión se convierte en una interfaz notrunk.<br/>                                                                                                     |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <dt>**Dynamic Auto**</dt> <dt>3</dt> </dl>                           | Hace que el punto de conexión pueda convertir el vínculo en un vínculo de tronco. El punto de conexión se convierte en una interfaz de tronco si la interfaz adyacente está establecida en tronco o en modo deseable.<br/>                                                                                                   |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <dt>**Deseable dinámico**</dt> <dt>4</dt> </dl>       | Hace que el punto de conexión intente convertir activamente el vínculo en un vínculo de tronco. El punto de conexión se convierte en una interfaz de tronco si la interfaz adyacente está establecida en el modo tronco, deseable o automático. El modo de puerto de conmutador predeterminado para todas las interfaces Ethernet es deseable de forma dinámica.<br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <dt>**Tronco**</dt> <dt>5</dt> </dl>                                                       | Coloca el punto de conexión en modo de tronco permanente y negocia convertir el vínculo en un vínculo de tronco. El punto de conexión se convierte en una interfaz de tronco incluso si la interfaz adyacente no es una interfaz de tronco.<br/>                                                               |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <dt>**Dot1Q Tunnel**</dt> <dt>6</dt> </dl>                           | Configura la interfaz como un punto de conexión o puerto de túnel (notrunking) para conectarse en un vínculo asimétrico con un puerto de tronco 802.1Q. La tunelización 802.1Q se usa para mantener la integridad de VLAN del cliente en una red del proveedor de servicios.<br/>                                     |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reservado**</dt> <dt>7 32767</dt> </dl>                 |                                                                                                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Proveedor reservado**</dt> <dt>32768 65535</dt> </dl> |                                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

**DesiredVLANTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de encapsulación VLAN que se solicita para su uso. La encapsulación actualmente en uso la proporciona **la propiedad OperationalVLANTrunkEncapsulation.** Esta propiedad solo es aplicable cuando el punto de conexión funciona en modo de enlace (consulte la **propiedad OperationalEndpointMode** para obtener más detalles). Esta propiedad es 2 (no aplicable) (es decir, el punto de conexión nunca se colocará en un modo de enlace), un tipo determinado (802.1Q o Cisco ISL) o 5 (Negotiate) (es decir, el resultado de la negociación entre esta interfaz y su vecino). El valor 5 (Negotiate) no se permite si el punto de conexión no admite la negociación. Esta funcionalidad depende del hardware y del proveedor. Esta propiedad se hereda de [**\_ CIM VLANEndpoint.**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)

<dl> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (2)
</dt> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)
</dt> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)
</dt> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Negotiate** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (6 32767)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)
</dt> </dl>

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Complementa la **propiedad PrimaryStatus con** detalles de estado adicionales. Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) y siempre se establece en 2 (Habilitado).

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados habilitados y deshabilitados de este elemento. Esta propiedad se hereda de [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre se establece en 5 (no aplicable).

</dd> <dt>

**GVRPStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el protocolo de registro de VLAN de GARP (GVRP) está habilitado o deshabilitado en el punto de conexión o puerto del tronco. Esta propiedad es 2 (no aplicable) a menos que el punto de conexión sea compatible con GVRP. Esta propiedad solo es aplicable cuando el punto de conexión funciona en modo de enlace (consulte la **propiedad OperationalEndpointMode** para obtener más detalles). Esta propiedad se hereda de [**\_ CIM VLANEndpoint.**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (2)
</dt> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)
</dt> <dt>

<span id="Disabled_"></span><span id="disabled_"></span><span id="DISABLED_"></span>**Deshabilitado** (4 )
</dt> </dl>

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual del elemento. Esta propiedad expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes. Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento es completamente no funcional. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y siempre se establece en 5 (Correcto).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se instaló el objeto. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y no se usa.

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

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Etiqueta por la que se conoce el objeto. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Heurística de nomenclatura que se selecciona para asegurarse de que el valor de la **propiedad Name** es único. Esta propiedad se hereda de [**Cim \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) y no se usa.

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información de estado actual para la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la **propiedad EnabledState.** Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**OperationalEndpointMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Modo de configuración para el punto de conexión de VLAN. Esta propiedad se hereda de [**\_ CIM VLANEndpoint.**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)



| Valor                                                                                                                                                                                                                                                                     | Significado                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reservado**</dt> <dt>0</dt> </dl>                       |                                                                                                                                                                                                                                                                     |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <dt>**Otros**</dt> <dt>1</dt> </dl>                                                       | El punto de conexión no tiene en cuenta la VLAN.<br/>                                                                                                                                                                                                                          |
| <span id="Access"></span><span id="access"></span><span id="ACCESS"></span><dl> <dt>**Acceso**</dt> <dt>2</dt> </dl>                                                   | Coloca el punto de conexión en modo de notrunking permanente y negocia convertir el vínculo en un vínculo notrunk. El punto de conexión se convierte en una interfaz notrunk.<br/>                                                                                                    |
| <span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span><dl> <dt>**Dynamic Auto**</dt> <dt>3</dt> </dl>                           | Hace que el punto de conexión pueda convertir el vínculo en un vínculo de tronco. El punto de conexión se convierte en una interfaz de tronco si la interfaz adyacente está establecida en el tronco o en el modo deseable.<br/>                                                                                      |
| <span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span><dl> <dt>**Deseable dinámico**</dt> <dt>4</dt> </dl>       | Hace que el punto de conexión intente convertir activamente el vínculo en un vínculo de tronco. El punto de conexión se convierte en una interfaz de tronco si la interfaz adyacente está establecida en el modo tronco, deseable o automático. Este es el modo de puerto de conmutador predeterminado para todas las interfaces Ethernet.<br/> |
| <span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span><dl> <dt>**Tronco**</dt> <dt>5</dt> </dl>                                                       | Coloca el punto de conexión en modo de enlace permanente y negocia convertir el vínculo en un vínculo de tronco. El punto de conexión se convierte en una interfaz de tronco incluso si la interfaz adyacente no es una interfaz de tronco.<br/>                                                  |
| <span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span><dl> <dt>**Dot1Q Tunnel**</dt> <dt>6</dt> </dl>                           | Configura la interfaz como un punto de conexión o puerto de túnel (sintrusión) que se va a conectar en un vínculo asimétrico con un puerto de tronco 802.1Q. La tunelización 802.1Q se usa para mantener la integridad de la VLAN del cliente en una red del proveedor de servicios.<br/>                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF Reservado**</dt> <dt>7 32767</dt> </dl>                 |                                                                                                                                                                                                                                                                     |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <dt> **Vendor Reserved**</dt> <dt>32768 65535</dt> </dl> |                                                                                                                                                                                                                                                                     |



 

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados actuales del objeto. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de matriz siempre se establece en 2 (correcto).

</dd> <dt>

**OperationalVLANTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de encapsulación vlan en uso en un puerto o punto de conexión de tronco. Esta propiedad es 2 (no aplicable) (es decir, el punto de conexión no funciona en modo de enlace), un tipo determinado (3 - 802.1Q o 4 - Cisco ISL), 5 (Negotiate) (es decir, los puntos de conexión están negociando el tipo de encapsulación). Esta propiedad solo es aplicable cuando el punto de conexión funciona en modo de enlace (consulte la **propiedad OperationalEndpointMode** para obtener más detalles). Esta propiedad se hereda de [**\_ CIM VLANEndpoint.**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)
</dt> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**No aplicable** (2)
</dt> <dt>

<span id="802.1Q"></span><span id="802.1q"></span>**802.1Q** (3)
</dt> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>**Cisco ISL** (4)
</dt> <dt>

<span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>**Negociación** (5)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (6 32767)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32768 65535)
</dt> </dl>

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe el estado habilitado o deshabilitado del elemento cuando la **propiedad EnabledState** está establecida en 1 ("Other"). Esta propiedad debe establecerse en **Null cuando** **EnabledState** es cualquier valor distinto de 1. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre se establece en **Null.**

</dd> <dt>

**OtherEndpointMode**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

El tipo de modelo de punto de conexión de VLAN que admite este punto de conexión de VLAN, cuando el valor de la **propiedad OperationalEndpointMode** se establece en 1 (Otros). Esta propiedad debe establecerse en **Null cuando** la **propiedad OperationalEndpointMode** sea cualquier valor distinto de 1. Esta propiedad se hereda de [**\_ CIM VLANEndpoint.**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)

</dd> <dt>

**OtherTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de encapsulación de VLAN que admite este punto de conexión de VLAN, cuando el valor de la propiedad **OperationalVLANTrunkEncapsulation** se establece en 1 (Otro). Esta propiedad debe establecerse en **Null cuando** la propiedad de encapsulación deseada sea cualquier valor distinto de 1. Esta propiedad se hereda de [**\_ CIM VLANEndpoint.**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **Cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de punto de conexión de protocolo cuando la propiedad **Type** de esta clase (o cualquiera de sus subclases) se establece en 1 (Other). Esta propiedad se hereda de [**CIM \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)y siempre se establece en "Virtual Ethernet".

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información de estado de alto nivel. Esta propiedad debe usarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes. Un **valor** NULL indica que esta propiedad no está implementada. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**ProtocolIFType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

MiB [ifType de IANA.](https://www.iana.org/assignments/ianaiftype-mib) Esta propiedad se hereda de [**Cim \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint)y siempre se establece en 1 (Otros).

</dd> <dt>

**ProtocolType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se hereda de [**Cim \_ ProtocolEndpoint**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint) y no se usa.

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Último estado solicitado o deseado para el servicio de administración. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre se establece en 12 (no aplicable).



| Valor                                                                         | Significado                    |
|-------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>12</dt> </dl> | No es aplicable.<br/> |



 

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe el estado del elemento. Esta propiedad se hereda de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

"Ok" (Aceptar)

"Error"

"Degradado"

"Desconocido"

"Error previo"

"Starting"

"Deteniendo"

"Servicio"

"Estresado"

"NonRecover"

"Sin contacto"

"Lost Comm"

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz de** cadenas
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadenas que describen los distintos **valores de la matriz OperationalStatus.** Esta propiedad se hereda de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)y cada elemento de matriz siempre se establece en "Ok".

</dd> <dt>

**SupportedEndpointModes**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Modos de punto de conexión admitidos por este puerto.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de clase de creación del sistema de ámbito. Esta propiedad se hereda de [**CIM \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)y siempre se establece en "Msvm \_ VirtualSwitch".

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre del sistema del sistema de ámbito. Esta propiedad se hereda del [**servicio \_ CIMAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que cambió por última vez el estado habilitado del elemento. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement,**](/previous-versions//cc136818(v=vs.85))pero no se admite.

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el estado de destino al que se está transfiriendo la instancia. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement,**](/previous-versions//cc136818(v=vs.85))pero no se usa.

</dd> </dl>

## <a name="remarks"></a>Comentarios

El acceso a la **clase \_ VLANEndpoint de Msvm** puede estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Ejemplos

Consulte [Consulta de objetos de red.](querying-networking-objects.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md)
</dt> <dt>

[**CIM \_ VLANEndpoint**](/previous-versions/windows/desktop/clushyperv/cim-vlanendpoint)
</dt> </dl>

 

