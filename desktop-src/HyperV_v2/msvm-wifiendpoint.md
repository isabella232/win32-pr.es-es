---
description: Representa el punto de conexión lógico para un adaptador de red. Cuando el extremo de Wi-Fi está conectado a un puerto de conmutador, el adaptador de red conectado al punto de conexión de Wi-Fi tiene conectividad de red.
ms.assetid: 66ed1503-9c11-4a51-a3a5-21e5d7021197
title: Msvm_WiFiEndpoint (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_WiFiEndpoint
- Msvm_WiFiEndpoint.RequestStateChange
- Msvm_WiFiEndpoint.InstanceID
- Msvm_WiFiEndpoint.Caption
- Msvm_WiFiEndpoint.Description
- Msvm_WiFiEndpoint.ElementName
- Msvm_WiFiEndpoint.InstallDate
- Msvm_WiFiEndpoint.Name
- Msvm_WiFiEndpoint.OperationalStatus
- Msvm_WiFiEndpoint.StatusDescriptions
- Msvm_WiFiEndpoint.Status
- Msvm_WiFiEndpoint.HealthState
- Msvm_WiFiEndpoint.CommunicationStatus
- Msvm_WiFiEndpoint.DetailedStatus
- Msvm_WiFiEndpoint.OperatingStatus
- Msvm_WiFiEndpoint.PrimaryStatus
- Msvm_WiFiEndpoint.EnabledState
- Msvm_WiFiEndpoint.OtherEnabledState
- Msvm_WiFiEndpoint.RequestedState
- Msvm_WiFiEndpoint.EnabledDefault
- Msvm_WiFiEndpoint.TimeOfLastStateChange
- Msvm_WiFiEndpoint.AvailableRequestedStates
- Msvm_WiFiEndpoint.TransitioningToState
- Msvm_WiFiEndpoint.SystemCreationClassName
- Msvm_WiFiEndpoint.SystemName
- Msvm_WiFiEndpoint.CreationClassName
- Msvm_WiFiEndpoint.NameFormat
- Msvm_WiFiEndpoint.ProtocolType
- Msvm_WiFiEndpoint.ProtocolIFType
- Msvm_WiFiEndpoint.OtherTypeDescription
- Msvm_WiFiEndpoint.LANID
- Msvm_WiFiEndpoint.LANType
- Msvm_WiFiEndpoint.OtherLANType
- Msvm_WiFiEndpoint.MACAddress
- Msvm_WiFiEndpoint.AliasAddresses
- Msvm_WiFiEndpoint.GroupAddresses
- Msvm_WiFiEndpoint.MaxDataSize
- Msvm_WiFiEndpoint.Connected
- Msvm_WiFiEndpoint.EncryptionMethod
- Msvm_WiFiEndpoint.OtherEncryptionMethod
- Msvm_WiFiEndpoint.AuthenticationMethod
- Msvm_WiFiEndpoint.OtherAuthenticationMethod
- Msvm_WiFiEndpoint.IEEE8021xAuthenticationProtocol
- Msvm_WiFiEndpoint.AccessPointAddress
- Msvm_WiFiEndpoint.BSSType
- Msvm_WiFiEndpoint.Associated
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f4a0a287d85b7a229b0e8e50a10c402fca734429
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001103"
---
# <a name="msvm_wifiendpoint-class"></a>MSVM \_ WiFiEndpoint (clase)

Representa el punto de conexión lógico para un adaptador de red. Cuando el extremo de Wi-Fi está conectado a un puerto de conmutador, el adaptador de red conectado al punto de conexión de Wi-Fi tiene conectividad de red.

La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_WiFiEndpoint : CIM_WiFiEndpoint
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[];
  string   StatusDescriptions[];
  string   Status;
  uint16   HealthState;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  uint16   EnabledState;
  string   OtherEnabledState;
  uint16   RequestedState;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType = 71;
  string   OtherTypeDescription;
  string   LANID;
  uint16   LANType;
  string   OtherLANType;
  string   MACAddress;
  string   AliasAddresses[];
  string   GroupAddresses[];
  uint32   MaxDataSize;
  boolean  Connected;
  uint16   EncryptionMethod;
  string   OtherEncryptionMethod;
  uint16   AuthenticationMethod;
  string   OtherAuthenticationMethod;
  uint16   IEEE8021xAuthenticationProtocol;
  string   AccessPointAddress;
  uint16   BSSType;
  boolean  Associated;
};
```

## <a name="members"></a>Miembros

La clase **MSVM \_ WiFiEndpoint** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **MSVM \_ WiFiEndpoint** tiene estos métodos.



| Método                 | Descripción                              |
|:-----------------------|:-----------------------------------------|
| **RequestStateChange** | No se admite este método.<br/> |



 

### <a name="properties"></a>Propiedades

La clase **MSVM \_ WiFiEndpoint** tiene estas propiedades.

<dl> <dt>

**AccessPointAddress**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Contiene la dirección MAC del punto de acceso con el que está asociado actualmente el punto de conexión de Wi-Fi. Si el extremo de Wi-Fi no está asociado actualmente, **AccessPointAddress** debe ser **null**. Se debe dar formato a la dirección MAC como doce dígitos hexadecimales (por ejemplo, "010203040506"), donde cada par representa uno de los seis octetos de la dirección MAC en orden de bits canónico (por ejemplo, el bit de dirección de grupo se encuentra en el bit de orden inferior del primer carácter de la cadena).

</dd> <dt>

**AliasAddresses**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Otras direcciones de unidifusión que se pueden usar para comunicarse con el punto de conexión de LAN. Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).

</dd> <dt>

**Asociado**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el extremo Wi-Fi está asociado actualmente a un punto de acceso o a una estación de cliente.

Contiene **true** si el extremo Wi-Fi está asociado a un punto de acceso o a una estación de cliente; en caso contrario, **false**.

</dd> <dt>

**AuthenticationMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el método utilizado para autenticar el Wi-Fi punto de conexión y la red entre sí.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)
</dt> <dt>

<span id="Open_System"></span><span id="open_system"></span><span id="OPEN_SYSTEM"></span>**Abrir sistema** (2)
</dt> <dt>

<span id="Shared_Key"></span><span id="shared_key"></span><span id="SHARED_KEY"></span>**Clave compartida** (3)
</dt> <dt>

<span id="WPA_PSK"></span><span id="wpa_psk"></span>**WPA PSK** (4)
</dt> <dt>

<span id="WPA_IEEE_802.1x"></span><span id="wpa_ieee_802.1x"></span><span id="WPA_IEEE_802.1X"></span>**WPA IEEE 802.1 x** (5)
</dt> <dt>

<span id="WPA2_PSK"></span><span id="wpa2_psk"></span>**PSK de WPA2** (6)
</dt> <dt>

<span id="WPA2_IEEE_802.1x"></span><span id="wpa2_ieee_802.1x"></span><span id="WPA2_IEEE_802.1X"></span>**IEEE 802.1 de WPA2 x** (7)
</dt> <dt>

<span id="CCKM_IEEE_802.1x"></span><span id="cckm_ieee_802.1x"></span><span id="CCKM_IEEE_802.1X"></span>**CCKM IEEE 802.1 x** (8)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (9.. )
</dt> </dl>

</dd> <dt>

**AvailableRequestedStates**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica los valores posibles para el parámetro *RequestedState* del método [**RequestStateChange**](/previous-versions/windows/desktop/iscsitarg/requeststatechange-cim-enabledlogicalelement) usado para iniciar un cambio de estado. Los valores enumerados serán un subconjunto de los valores contenidos en la propiedad **RequestedStatesSupported** de la instancia asociada de **CIM \_ EnabledLogicalElementCapabilities**, donde los valores seleccionados son una función del estado actual de la [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)). Esta propiedad puede ser distinta de **null** si una implementación de puede anunciar el conjunto de valores posibles como una función del estado actual. Esta propiedad será **null** si una implementación de no puede determinar el conjunto de valores posibles como una función del estado actual.

Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)
</dt> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Apagar** (4)
</dt> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Sin conexión** (6)
</dt> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>**Prueba** (7)
</dt> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Diferir** (8)
</dt> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>Modo **inactivo** (9)
</dt> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reinicio** (10)
</dt> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Restablecer** (11)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (.. )
</dt> </dl>

</dd> <dt>

**BSSType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el tipo básico de Service Set (BSS) de la red que corresponde a la instancia de. Un conjunto de servicios básico es un conjunto de estaciones controlado por una única función de coordinación.



| Value                                                                                                                                                                                                                                                      | Significado                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt>**Desconocido**</dt> <dt>0</dt> </dl>                                |                                                                                    |
| <span id="Independent"></span><span id="independent"></span><span id="INDEPENDENT"></span><dl> <dt>**Independiente**</dt> <dt>2</dt> </dl>                | El extremo Wi-Fi está asociado directamente a otra estación cliente.<br/>    |
| <span id="Infrastructure"></span><span id="infrastructure"></span><span id="INFRASTRUCTURE"></span><dl> <dt>**Infraestructura**</dt> <dt>3</dt> </dl>    | El extremo Wi-Fi está asociado a una red mediante un punto de acceso.<br/> |
| <span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span><dl> <dt> **Reservado para DMTF**</dt> <dt>4..</dt> </dl> |                                                                                    |



 

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Breve descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente. Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**Conectada**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad se establece en **true** si el extremo Wi-Fi está conectado a un puerto de conmutador.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**, **MaxLen** (256)
</dt> </dl>

Nombre de la clase o subclase utilizada en la creación de una instancia de. Esta propiedad se hereda de [**\_ punto CIM**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales. Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre para mostrar del objeto. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**EnabledDefault**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Configuración predeterminada o de inicio de un administrador para el estado habilitado de un elemento. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)) y tendrá uno de los valores siguientes.

<dl> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)
</dt> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Deshabilitado** (3)
</dt> <dt>

<span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span>**Habilitada pero sin conexión** (6)
</dt> </dl>

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el estado habilitado del sistema planeado. Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y puede ser uno de los valores siguientes.



| Value                                                                                                                                                                                                                                                                       | Significado                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Deshabilitado**</dt> <dt>3</dt> </dl>                                             | El sistema está desactivado.<br/>                                             |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <dt>**No aplicable**</dt> <dt>5</dt> </dl>                     | El elemento no admite la habilitación o deshabilitación.<br/>               |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <dt>**Habilitada pero sin conexión**</dt> <dt>6</dt> </dl> | El sistema está habilitado, pero sin conexión. Se quitarán las nuevas solicitudes.<br/> |



 

</dd> <dt>

**EncryptionMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el método de cifrado que se usa para proteger la confidencialidad de los datos enviados y recibidos por el punto de conexión de Wi-Fi.

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)
</dt> <dt>

<span id="WEP"></span><span id="wep"></span>**WEP** (2)
</dt> <dt>

<span id="TKIP"></span><span id="tkip"></span>**TKIP** (3)
</dt> <dt>

<span id="CCMP"></span><span id="ccmp"></span>**CCMP** (4)
</dt> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno** (5)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (6.. )
</dt> </dl>

</dd> <dt>

**GroupAddresses**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Direcciones de multidifusión a las que el punto de conexión de LAN realiza escuchas. Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estado actual del elemento. Esta propiedad expresa el estado de este elemento, pero no necesariamente el de sus subcomponentes. Los valores posibles son de 0 a 30, donde 5 significa que el elemento es completamente correcto y 30 significa que el elemento no es totalmente funcional. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**IEEE8021xAuthenticationProtocol**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Contiene el tipo de protocolo de autenticación extensible (EAP) si el **AuthenticationMethod** contiene 5 (WPA IEEE 802.1 x), 7 (WPA2 IEEE 802.1 x) o 8 (CCKM IEEE 802.1 x).

<dl> <dt>

<span id="EAP-TLS"></span><span id="eap-tls"></span>**EAP-TLS** (0)
</dt> <dt>

<span id="EAP-TTLS_MSCHAPv2"></span><span id="eap-ttls_mschapv2"></span><span id="EAP-TTLS_MSCHAPV2"></span>**EAP-TTLS/MSCHAPv2** (1)
</dt> <dt>

<span id="PEAPv0_EAP-MSCHAPv2"></span><span id="peapv0_eap-mschapv2"></span><span id="PEAPV0_EAP-MSCHAPV2"></span>**PEAPv0/EAP-MSCHAPv2** (2)
</dt> <dt>

<span id="PEAPv1_EAP-GTC"></span><span id="peapv1_eap-gtc"></span><span id="PEAPV1_EAP-GTC"></span>**PEAPv1/EAP-GTC** (3)
</dt> <dt>

<span id="EAP-FAST_MSCHAPv2"></span><span id="eap-fast_mschapv2"></span><span id="EAP-FAST_MSCHAPV2"></span>**EAP-FAST/MSCHAPv2** (4)
</dt> <dt>

<span id="EAP-FAST_GTC"></span><span id="eap-fast_gtc"></span>**EAP-FAST/GTC** (5)
</dt> <dt>

<span id="EAP-MD5"></span><span id="eap-md5"></span>**EAP-MD5** (6)
</dt> <dt>

<span id="EAP-PSK"></span><span id="eap-psk"></span>**EAP-PSK** (7)
</dt> <dt>

<span id="EAP-SIM"></span><span id="eap-sim"></span>**EAP-SIM** (8)
</dt> <dt>

<span id="EAP-AKA"></span><span id="eap-aka"></span>**EAP-AKA** (9)
</dt> <dt>

<span id="EAP-FAST_TLS"></span><span id="eap-fast_tls"></span>**EAP-FAST/TLS** (10)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (11.. )
</dt> </dl>

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se creó la configuración de la máquina virtual. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**
</dt> </dl>

Identifica de forma única una instancia de esta clase. Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**LANID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Etiqueta o identificador del segmento de LAN al que está conectado el extremo. Si el extremo no está activo o conectado actualmente, o no se conoce esta información, esta propiedad será **null**. Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).

</dd> <dt>

**LANType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad está en desuso en lugar de la propiedad **protocolType** . Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).

</dd> <dt>

**Mac**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (12)
</dt> </dl>

Dirección MAC que se usa en la comunicación con el punto de conexión de LAN. La dirección MAC tiene el formato de doce dígitos hexadecimales (por ejemplo, "010203040506"), donde cada par representa uno de los seis octetos de la dirección MAC en orden de bits canónico según RFC 2469. Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **unidades** ("bits")
</dt> </dl>

Tamaño máximo, en número de bits, del campo de información que puede ser enviado o recibido por el punto de conexión de LAN. Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Etiqueta por la que se conoce el objeto. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (256)
</dt> </dl>

Contiene la heurística de nomenclatura que se selecciona para asegurarse de que el valor de la propiedad **Name** es único. Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** . Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Estados actuales del objeto. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**OtherAuthenticationMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el método de autenticación 802,11 solo si **AuthenticationMethod** contiene 1 (otro). El formato de esta cadena es específico del proveedor.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 ("otro"). Esta propiedad debe establecerse en **null** cuando **EnabledState** es cualquier valor distinto de 1. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**OtherEncryptionMethod**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Especifica el método de cifrado 802,11 si y solo si **EncryptionMethod** contiene 1 (otro). El formato de esta cadena es específico del proveedor.

</dd> <dt>

**OtherLANType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad está en desuso en lugar de la propiedad **OtherTypeDescription** . Esta propiedad se hereda de [**\_ LANEndpoint CIM**](/previous-versions//cc136865(v=vs.85)).

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **MaxLen** (64)
</dt> </dl>

Una cadena que describe el tipo de extremo de protocolo cuando la propiedad **ProtocolIFType** de esta clase (o cualquiera de sus subclases) está establecida en 1 (otro). Esta propiedad debe establecerse en **null** cuando la propiedad **ProtocolIFType** es cualquier valor distinto de 1. Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Proporciona información de estado de alto nivel. Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar información de estado de mantenimiento detallada y de alto nivel para el elemento y sus subcomponentes. Un valor **null** indica que esta propiedad no está implementada. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ProtocolIFType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La propiedad se utiliza para categorizar y clasificar las instancias de esta clase. Si **ProtocolIFType** se establece en 1 (otro), se debe proporcionar la información de tipo en la propiedad **OtherTypeDescription** . Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).

> [!Note]  
> **ProtocolIFType** es una enumeración que está sincronizada con la [MIB de ifType de IANA](https://www.iana.org/assignments/ianaiftype-mib). También se incluyen los valores adicionales definidos por DMTF.

 

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)
</dt> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>**IEEE 802,11** (71)
</dt> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>**IANA reservado** (225.. 4095)
</dt> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (4301.. 32767)
</dt> <dt>

<span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (32768.. )
</dt> </dl>

</dd> <dt>

**ProtocolType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Esta propiedad está en desuso en lugar de la propiedad **ProtocolIFType** . Esta propiedad se hereda del [**\_ ProtocolEndpoint de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-protocolendpoint).

</dd> <dt>

**RequestedState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Último estado solicitado o deseado para el servicio de administración. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**Estado**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Describe el estado del elemento. Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

ACEPTAR

Error

Degradado

Unknown

"Pred FAIL"

Comenzar

Bloqueo

Servicio

Calca

"Recover"

"Sin contacto"

"Pérdida de comunicación"

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz de **cadenas**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Cadenas que describen los distintos valores de la matriz **OperationalStatus** . Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de la clase de creación del sistema de hospedaje. Esta propiedad se hereda de [**\_ punto CIM**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: **clave**, **MaxLen** (256)
</dt> </dl>

Nombre del sistema de hospedaje. Esta propiedad se hereda de [**\_ punto CIM**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint).

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo de datos: **DateTime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que se cambió por última vez el estado habilitado del elemento. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> <dt>

**TransitioningToState**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica el estado de destino al que la instancia está cambiando. Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

