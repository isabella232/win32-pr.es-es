---
description: Punto de comunicación que se usa para enviar y recibir datos entre sistemas, interfaces de equipo y redes lógicas.
ms.assetid: e23ef66b-0bcb-400e-91ff-d6d687d3f0d2
title: CIM_ProtocolEndpoint clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolEndpoint
- CIM_ProtocolEndpoint.Description
- CIM_ProtocolEndpoint.OperationalStatus
- CIM_ProtocolEndpoint.EnabledState
- CIM_ProtocolEndpoint.TimeOfLastStateChange
- CIM_ProtocolEndpoint.Name
- CIM_ProtocolEndpoint.NameFormat
- CIM_ProtocolEndpoint.ProtocolType
- CIM_ProtocolEndpoint.ProtocolIFType
- CIM_ProtocolEndpoint.OtherTypeDescription
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2fa050bd301842b9f8eeb2816420e4f09601e29a0f47cace721f2d56583f3a5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981185"
---
# <a name="cim_protocolendpoint-class"></a>Cim \_ ProtocolEndpoint (clase)

Punto de comunicación que se usa para enviar y recibir datos entre sistemas, interfaces de equipo y redes lógicas.

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.15.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ProtocolEndpoint : CIM_ServiceAccessPoint
{
  string   Description;
  uint16   OperationalStatus[];
  uint16   EnabledState;
  datetime TimeOfLastStateChange;
  string   Name;
  string   NameFormat;
  uint16   ProtocolType;
  uint16   ProtocolIFType;
  string   OtherTypeDescription;
};
```

## <a name="members"></a>Miembros

La **clase \_ Cim ProtocolEndpoint** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ Cim ProtocolEndpoint** tiene estas propiedades.

<dl> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Description"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| IF-MIB.ifDescr")
</dt> </dl>

Descripción textual del objeto.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("EnabledState"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| IF-MIB.ifAdminStatus")
</dt> </dl>

Estado habilitado de un elemento.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificador único del punto de conexión de protocolo que indica la funcionalidad administrada. La convención de nomenclatura para esta propiedad se define en la **propiedad NameFormat.**

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Convención de nomenclatura utilizada por la **propiedad Name** para asegurarse de que **los valores** name son únicos. Por ejemplo, puede anexar el valor **de la propiedad ProtocolIFType** al principio del nombre seguido de un carácter de subrayado.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de datos: **matriz uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("OperationalStatus"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| IF-MIB.ifOperStatus")
</dt> </dl>

Matriz que contiene el estado actual del elemento. El primer valor de la **matriz OperationalStatus** debe contener el estado principal del elemento.

</dd> <dt>

**OtherTypeDescription**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ProtocolEndpoint**.**ProtocolType**", "**CIM \_ ProtocolEndpoint**.**ProtocolIFType**")
</dt> </dl>

Descripción de un tipo de protocolo de red que se usa cuando la **propiedad ProtocolIFType** se establece en "1" (Otros); De lo contrario, este valor debe establecerse en null.

</dd> <dt>

**ProtocolIFType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| IF-MIB.ifType"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ProtocolEndpoint**.**OtherTypeDescription**")
</dt> </dl>

Enumeración que se usa para clasificar y clasificar diferentes instancias de esta clase. Los valores posibles para esta propiedad se sincronizan con la autoridad de números asignados a Internet (IANA) ifType MIB-module (base de información de administración), que se mantiene en https://www.iana.org/assignments/ianaiftype-mib . Se incluyen valores adicionales definidos por dmtf.

> [!Note]  
> Si **ProtocolIFType se** establece en 1 (Otros), la información del tipo de protocolo debe proporcionarse en **la propiedad OtherTypeDescription.**

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="Regular_1822"></span><span id="regular_1822"></span><span id="REGULAR_1822"></span>

**Normal 1822** (2)


</dt> <dd></dd> <dt>

<span id="HDH_1822"></span><span id="hdh_1822"></span>

**HDH 1822** (3)


</dt> <dd></dd> <dt>

<span id="DDN_X.25"></span><span id="ddn_x.25"></span>

**DDN X.25** (4)


</dt> <dd></dd> <dt>

<span id="RFC877_X.25"></span><span id="rfc877_x.25"></span>

**RFC877 X.25** (5)


</dt> <dd></dd> <dt>

<span id="Ethernet_CSMA_CD"></span><span id="ethernet_csma_cd"></span><span id="ETHERNET_CSMA_CD"></span>

**Ethernet CSMA/CD** (6)


</dt> <dd></dd> <dt>

<span id="ISO_802.3_CSMA_CD"></span><span id="iso_802.3_csma_cd"></span>

**ISO 802.3 CSMA/CD** (7)


</dt> <dd></dd> <dt>

<span id="ISO_802.4_Token_Bus"></span><span id="iso_802.4_token_bus"></span><span id="ISO_802.4_TOKEN_BUS"></span>

**Bus de tokens ISO 802.4** (8)


</dt> <dd></dd> <dt>

<span id="ISO_802.5_Token_Ring"></span><span id="iso_802.5_token_ring"></span><span id="ISO_802.5_TOKEN_RING"></span>

**Anillo de token ISO 802.5** (9)


</dt> <dd></dd> <dt>

<span id="ISO_802.6_MAN"></span><span id="iso_802.6_man"></span>

**ISO 802.6 MAN** (10)


</dt> <dd></dd> <dt>

<span id="StarLAN"></span><span id="starlan"></span><span id="STARLAN"></span>

**StarLAN** (11)


</dt> <dd></dd> <dt>

<span id="Proteon_10Mbit"></span><span id="proteon_10mbit"></span><span id="PROTEON_10MBIT"></span>

**Seleón de 10 Mbit** (12)


</dt> <dd></dd> <dt>

<span id="Proteon_80Mbit"></span><span id="proteon_80mbit"></span><span id="PROTEON_80MBIT"></span>

**Seleón de 80 Mbit** (13)


</dt> <dd></dd> <dt>

<span id="HyperChannel"></span><span id="hyperchannel"></span><span id="HYPERCHANNEL"></span>

**HyperChannel** (14)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (15)


</dt> <dd></dd> <dt>

<span id="LAP-B"></span><span id="lap-b"></span>

**LAP-B** (16)


</dt> <dd></dd> <dt>

<span id="SDLC"></span><span id="sdlc"></span>

**SDLC** (17)


</dt> <dd></dd> <dt>

<span id="DS1"></span><span id="ds1"></span>

**DS1** (18)


</dt> <dd></dd> <dt>

<span id="E1"></span><span id="e1"></span>

**E1** (19)


</dt> <dd></dd> <dt>

<span id="Basic_ISDN"></span><span id="basic_isdn"></span><span id="BASIC_ISDN"></span>

**ISDN básico** (20)


</dt> <dd></dd> <dt>

<span id="Primary_ISDN"></span><span id="primary_isdn"></span><span id="PRIMARY_ISDN"></span>

**ISDN principal** (21)


</dt> <dd></dd> <dt>

<span id="Proprietary_Point-to-Point_Serial"></span><span id="proprietary_point-to-point_serial"></span><span id="PROPRIETARY_POINT-TO-POINT_SERIAL"></span>

**Serie de punto** a punto propietario (22)


</dt> <dd></dd> <dt>

<span id="PPP"></span><span id="ppp"></span>

**PPP** (23)


</dt> <dd></dd> <dt>

<span id="Software_Loopback"></span><span id="software_loopback"></span><span id="SOFTWARE_LOOPBACK"></span>

**Bucle recuperación de** software (24)


</dt> <dd></dd> <dt>

<span id="EON"></span><span id="eon"></span>

**EON** (25)


</dt> <dd></dd> <dt>

<span id="Ethernet_3Mbit"></span><span id="ethernet_3mbit"></span><span id="ETHERNET_3MBIT"></span>

**Ethernet de 3 bits** (26)


</dt> <dd></dd> <dt>

<span id="NSIP"></span><span id="nsip"></span>

**NSIP** (27)


</dt> <dd></dd> <dt>

<span id="SLIP"></span><span id="slip"></span>

**SLIP** (28)


</dt> <dd></dd> <dt>

<span id="Ultra"></span><span id="ultra"></span><span id="ULTRA"></span>

**Ultra** (29)


</dt> <dd></dd> <dt>

<span id="DS3"></span><span id="ds3"></span>

**DS3** (30)


</dt> <dd></dd> <dt>

<span id="SIP"></span><span id="sip"></span>

**SIP** (31)


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

**Frame Relay** (32)


</dt> <dd></dd> <dt>

<span id="RS-232"></span><span id="rs-232"></span>

**RS-232** (33)


</dt> <dd></dd> <dt>

<span id="Parallel"></span><span id="parallel"></span><span id="PARALLEL"></span>

**Parallel** (34)


</dt> <dd></dd> <dt>

<span id="ARCNet"></span><span id="arcnet"></span><span id="ARCNET"></span>

**ARCNet** (35)


</dt> <dd></dd> <dt>

<span id="ARCNet_Plus"></span><span id="arcnet_plus"></span><span id="ARCNET_PLUS"></span>

**ARCNet Plus** (36)


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

**ATM** (37)


</dt> <dd></dd> <dt>

<span id="MIO_X.25"></span><span id="mio_x.25"></span>

**MIO X.25** (38)


</dt> <dd></dd> <dt>

<span id="SONET"></span><span id="sonet"></span>

**SONET** (39)


</dt> <dd></dd> <dt>

<span id="X.25_PLE"></span><span id="x.25_ple"></span>

**X.25 PLE** (40)


</dt> <dd></dd> <dt>

<span id="ISO_802.211c"></span><span id="iso_802.211c"></span><span id="ISO_802.211C"></span>

**ISO 802.211c** (41)


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

**LocalTalk** (42)


</dt> <dd></dd> <dt>

<span id="SMDS_DXI"></span><span id="smds_dxi"></span>

**SMDS DXI** (43)


</dt> <dd></dd> <dt>

<span id="Frame_Relay_Service"></span><span id="frame_relay_service"></span><span id="FRAME_RELAY_SERVICE"></span>

**Servicio Frame Relay** (44)


</dt> <dd></dd> <dt>

<span id="V.35"></span><span id="v.35"></span>

**V.35** (45)


</dt> <dd></dd> <dt>

<span id="HSSI"></span><span id="hssi"></span>

**HSSI** (46)


</dt> <dd></dd> <dt>

<span id="HIPPI"></span><span id="hippi"></span>

**HIPPI** (47)


</dt> <dd></dd> <dt>

<span id="Modem"></span><span id="modem"></span><span id="MODEM"></span>

**Módem** (48)


</dt> <dd></dd> <dt>

<span id="AAL5"></span><span id="aal5"></span>

**AAL5** (49)


</dt> <dd></dd> <dt>

<span id="SONET_Path"></span><span id="sonet_path"></span><span id="SONET_PATH"></span>

**Ruta de acceso de SONET** (50)


</dt> <dd></dd> <dt>

<span id="SONET_VT"></span><span id="sonet_vt"></span>

**SONET VT** (51)


</dt> <dd></dd> <dt>

<span id="SMDS_ICIP"></span><span id="smds_icip"></span>

**SMDS ICIP** (52)


</dt> <dd></dd> <dt>

<span id="Proprietary_Virtual_Internal"></span><span id="proprietary_virtual_internal"></span><span id="PROPRIETARY_VIRTUAL_INTERNAL"></span>

**Propietario virtual/interno** (53)


</dt> <dd></dd> <dt>

<span id="Proprietary_Multiplexor"></span><span id="proprietary_multiplexor"></span><span id="PROPRIETARY_MULTIPLEXOR"></span>

**Multiplexor propietario** (54)


</dt> <dd></dd> <dt>

<span id="IEEE_802.12"></span><span id="ieee_802.12"></span>

**IEEE 802.12** (55)


</dt> <dd></dd> <dt>

<span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>

**Canal de fibra** (56)


</dt> <dd></dd> <dt>

<span id="HIPPI_Interface"></span><span id="hippi_interface"></span><span id="HIPPI_INTERFACE"></span>

**Interfaz HIPPI** (57)


</dt> <dd></dd> <dt>

<span id="Frame_Relay_Interconnect"></span><span id="frame_relay_interconnect"></span><span id="FRAME_RELAY_INTERCONNECT"></span>

**Interconexión de Frame Relay** (58)


</dt> <dd></dd> <dt>

<span id="ATM_Emulated_LAN_for_802.3"></span><span id="atm_emulated_lan_for_802.3"></span><span id="ATM_EMULATED_LAN_FOR_802.3"></span>

**LAN emulada por ATM para 802.3** (59)


</dt> <dd></dd> <dt>

<span id="ATM_Emulated_LAN_for_802.5"></span><span id="atm_emulated_lan_for_802.5"></span><span id="ATM_EMULATED_LAN_FOR_802.5"></span>

**LAN emulada de ATM para 802.5** (60)


</dt> <dd></dd> <dt>

<span id="ATM_Emulated_Circuit"></span><span id="atm_emulated_circuit"></span><span id="ATM_EMULATED_CIRCUIT"></span>

**Circuito emulado de ATM** (61)


</dt> <dd></dd> <dt>

<span id="Fast_Ethernet__100BaseT_"></span><span id="fast_ethernet__100baset_"></span><span id="FAST_ETHERNET__100BASET_"></span>

**Fast Ethernet (100BaseT)** (62)


</dt> <dd></dd> <dt>

<span id="ISDN"></span><span id="isdn"></span>

**ISDN** (63)


</dt> <dd></dd> <dt>

<span id="V.11"></span><span id="v.11"></span>

**V.11** (64)


</dt> <dd></dd> <dt>

<span id="V.36"></span><span id="v.36"></span>

**V.36** (65)


</dt> <dd></dd> <dt>

<span id="G703_at_64K"></span><span id="g703_at_64k"></span><span id="G703_AT_64K"></span>

**G703 a 64 K** (66)


</dt> <dd></dd> <dt>

<span id="G703_at_2Mb"></span><span id="g703_at_2mb"></span><span id="G703_AT_2MB"></span>

**G703 a 2 Mb** (67)


</dt> <dd></dd> <dt>

<span id="QLLC"></span><span id="qllc"></span>

**QLLC** (68)


</dt> <dd></dd> <dt>

<span id="Fast_Ethernet_100BaseFX"></span><span id="fast_ethernet_100basefx"></span><span id="FAST_ETHERNET_100BASEFX"></span>

**Fast Ethernet 100BaseFX** (69)


</dt> <dd></dd> <dt>

<span id="Channel"></span><span id="channel"></span><span id="CHANNEL"></span>

**Canal** (70)


</dt> <dd></dd> <dt>

<span id="IEEE_802.11"></span><span id="ieee_802.11"></span>

**IEEE 802.11** (71)


</dt> <dd></dd> <dt>

<span id="IBM_260_370_OEMI_Channel"></span><span id="ibm_260_370_oemi_channel"></span><span id="IBM_260_370_OEMI_CHANNEL"></span>

**Canal OEMI IBM 260/370** (72)


</dt> <dd></dd> <dt>

<span id="ESCON"></span><span id="escon"></span>

**ESCON** (73)


</dt> <dd></dd> <dt>

<span id="Data_Link_Switching"></span><span id="data_link_switching"></span><span id="DATA_LINK_SWITCHING"></span>

**Conmutación de vínculos de** datos (74)


</dt> <dd></dd> <dt>

<span id="ISDN_S_T_Interface"></span><span id="isdn_s_t_interface"></span><span id="ISDN_S_T_INTERFACE"></span>

**Interfaz S/T de ISDN** (75)


</dt> <dd></dd> <dt>

<span id="ISDN_U_Interface"></span><span id="isdn_u_interface"></span><span id="ISDN_U_INTERFACE"></span>

**Interfaz ISDN U** (76)


</dt> <dd></dd> <dt>

<span id="LAP-D"></span><span id="lap-d"></span>

**LAP-D** (77)


</dt> <dd></dd> <dt>

<span id="IP_Switch"></span><span id="ip_switch"></span><span id="IP_SWITCH"></span>

**Conmutador IP** (78)


</dt> <dd></dd> <dt>

<span id="Remote_Source_Route_Bridging"></span><span id="remote_source_route_bridging"></span><span id="REMOTE_SOURCE_ROUTE_BRIDGING"></span>

**Protocolo de puente de ruta de origen** remoto (79)


</dt> <dd></dd> <dt>

<span id="ATM_Logical"></span><span id="atm_logical"></span><span id="ATM_LOGICAL"></span>

**Lógico de ATM** (80)


</dt> <dd></dd> <dt>

<span id="DS0"></span><span id="ds0"></span>

**DS0** (81)


</dt> <dd></dd> <dt>

<span id="DS0_Bundle"></span><span id="ds0_bundle"></span><span id="DS0_BUNDLE"></span>

**Conjunto DS0** (82)


</dt> <dd></dd> <dt>

<span id="BSC"></span><span id="bsc"></span>

**BSC** (83)


</dt> <dd></dd> <dt>

<span id="Async"></span><span id="async"></span><span id="ASYNC"></span>

**Async** (84)


</dt> <dd></dd> <dt>

<span id="Combat_Net_Radio"></span><span id="combat_net_radio"></span><span id="COMBAT_NET_RADIO"></span>

**Radio neta de** guerra (85)


</dt> <dd></dd> <dt>

<span id="ISO_802.5r_DTR"></span><span id="iso_802.5r_dtr"></span><span id="ISO_802.5R_DTR"></span>

**ISO 802.5r DTR** (86)


</dt> <dd></dd> <dt>

<span id="Ext_Pos_Loc_Report_System"></span><span id="ext_pos_loc_report_system"></span><span id="EXT_POS_LOC_REPORT_SYSTEM"></span>

**Ext Pos Loc Report System** (87)


</dt> <dd></dd> <dt>

<span id="AppleTalk_Remote_Access_Protocol"></span><span id="appletalk_remote_access_protocol"></span><span id="APPLETALK_REMOTE_ACCESS_PROTOCOL"></span>

**Protocolo de acceso remoto de AppleTalk** (88)


</dt> <dd></dd> <dt>

<span id="Proprietary_Connectionless"></span><span id="proprietary_connectionless"></span><span id="PROPRIETARY_CONNECTIONLESS"></span>

**Sin conexión propietaria** (89)


</dt> <dd></dd> <dt>

<span id="ITU_X.29_Host_PAD"></span><span id="itu_x.29_host_pad"></span><span id="ITU_X.29_HOST_PAD"></span>

**PANEL de host X.29 de ITU** (90)


</dt> <dd></dd> <dt>

<span id="ITU_X.3_Terminal_PAD"></span><span id="itu_x.3_terminal_pad"></span><span id="ITU_X.3_TERMINAL_PAD"></span>

**PANEL de terminal ITU X.3** (91)


</dt> <dd></dd> <dt>

<span id="Frame_Relay_MPI"></span><span id="frame_relay_mpi"></span><span id="FRAME_RELAY_MPI"></span>

**Frame Relay MPI** (92)


</dt> <dd></dd> <dt>

<span id="ITU_X.213"></span><span id="itu_x.213"></span>

**ITU X.213** (93)


</dt> <dd></dd> <dt>

<span id="ADSL"></span><span id="adsl"></span>

**ADSL** (94)


</dt> <dd></dd> <dt>

<span id="RADSL"></span><span id="radsl"></span>

**RADSL** (95)


</dt> <dd></dd> <dt>

<span id="SDSL"></span><span id="sdsl"></span>

**SDSL** (96)


</dt> <dd></dd> <dt>

<span id="VDSL"></span><span id="vdsl"></span>

**VDSL** (97)


</dt> <dd></dd> <dt>

<span id="ISO_802.5_CRFP"></span><span id="iso_802.5_crfp"></span>

**ISO 802.5 CRFP** (98)


</dt> <dd></dd> <dt>

<span id="Myrinet"></span><span id="myrinet"></span><span id="MYRINET"></span>

**My pipet** (99)


</dt> <dd></dd> <dt>

<span id="Voice_Receive_and_Transmit"></span><span id="voice_receive_and_transmit"></span><span id="VOICE_RECEIVE_AND_TRANSMIT"></span>

**Recepción y transmisión de voz** (100)


</dt> <dd></dd> <dt>

<span id="Voice_Foreign_Exchange_Office"></span><span id="voice_foreign_exchange_office"></span><span id="VOICE_FOREIGN_EXCHANGE_OFFICE"></span>

**Voice Foreign Exchange Office** (101)


</dt> <dd></dd> <dt>

<span id="Voice_Foreign_Exchange_Service"></span><span id="voice_foreign_exchange_service"></span><span id="VOICE_FOREIGN_EXCHANGE_SERVICE"></span>

**Servicio de Exchange voz** externa (102)


</dt> <dd></dd> <dt>

<span id="Voice_Encapsulation"></span><span id="voice_encapsulation"></span><span id="VOICE_ENCAPSULATION"></span>

**Encapsulación de voz** (103)


</dt> <dd></dd> <dt>

<span id="Voice_over_IP"></span><span id="voice_over_ip"></span><span id="VOICE_OVER_IP"></span>

**Voz sobre IP** (104)


</dt> <dd></dd> <dt>

<span id="ATM_DXI"></span><span id="atm_dxi"></span>

**ATM DXI** (105)


</dt> <dd></dd> <dt>

<span id="ATM_FUNI"></span><span id="atm_funi"></span>

**FUNI de CAJERO** (106)


</dt> <dd></dd> <dt>

<span id="ATM_IMA"></span><span id="atm_ima"></span>

**ATM IMA** (107)


</dt> <dd></dd> <dt>

<span id="PPP_Multilink_Bundle"></span><span id="ppp_multilink_bundle"></span><span id="PPP_MULTILINK_BUNDLE"></span>

**Ppp Multilink Bundle** (108)


</dt> <dd></dd> <dt>

<span id="IP_over_CDLC"></span><span id="ip_over_cdlc"></span><span id="IP_OVER_CDLC"></span>

**IP a través de CDLC** (109)


</dt> <dd></dd> <dt>

<span id="IP_over_CLAW"></span><span id="ip_over_claw"></span><span id="IP_OVER_CLAW"></span>

**IP a través de LA PROPIEDAD** (110)


</dt> <dd></dd> <dt>

<span id="Stack_to_Stack"></span><span id="stack_to_stack"></span><span id="STACK_TO_STACK"></span>

**Pila a pila** (111)


</dt> <dd></dd> <dt>

<span id="Virtual_IP_Address"></span><span id="virtual_ip_address"></span><span id="VIRTUAL_IP_ADDRESS"></span>

**Dirección IP virtual** (112)


</dt> <dd></dd> <dt>

<span id="MPC"></span><span id="mpc"></span>

**MPC** (113)


</dt> <dd></dd> <dt>

<span id="IP_over_ATM"></span><span id="ip_over_atm"></span><span id="IP_OVER_ATM"></span>

**IP a través de un cajero** automático (114)


</dt> <dd></dd> <dt>

<span id="ISO_802.5j_Fibre_Token_Ring"></span><span id="iso_802.5j_fibre_token_ring"></span><span id="ISO_802.5J_FIBRE_TOKEN_RING"></span>

Anillo de token de fibra **ISO 802.5j** (115)


</dt> <dd></dd> <dt>

<span id="TDLC"></span><span id="tdlc"></span>

**TDLC** (116)


</dt> <dd></dd> <dt>

<span id="Gigabit_Ethernet"></span><span id="gigabit_ethernet"></span><span id="GIGABIT_ETHERNET"></span>

**Gigabit Ethernet** (117)


</dt> <dd></dd> <dt>

<span id="HDLC"></span><span id="hdlc"></span>

**HDLC** (118)


</dt> <dd></dd> <dt>

<span id="LAP-F"></span><span id="lap-f"></span>

**LAP-F** (119)


</dt> <dd></dd> <dt>

<span id="V.37"></span><span id="v.37"></span>

**V.37** (120)


</dt> <dd></dd> <dt>

<span id="X.25_MLP"></span><span id="x.25_mlp"></span>

**X.25 MLP** (121)


</dt> <dd></dd> <dt>

<span id="X.25_Hunt_Group"></span><span id="x.25_hunt_group"></span><span id="X.25_HUNT_GROUP"></span>

**X.25 Grupo de búsqueda** (122)


</dt> <dd></dd> <dt>

<span id="Transp_HDLC"></span><span id="transp_hdlc"></span><span id="TRANSP_HDLC"></span>

**Transp HDLC** (123)


</dt> <dd></dd> <dt>

<span id="Interleave_Channel"></span><span id="interleave_channel"></span><span id="INTERLEAVE_CHANNEL"></span>

**Canal de intercalación** (124)


</dt> <dd></dd> <dt>

<span id="FAST_Channel"></span><span id="fast_channel"></span><span id="FAST_CHANNEL"></span>

**FAST Channel** (125)


</dt> <dd></dd> <dt>

<span id="IP__for_APPN_HPR_in_IP_Networks_"></span><span id="ip__for_appn_hpr_in_ip_networks_"></span><span id="IP__FOR_APPN_HPR_IN_IP_NETWORKS_"></span>

**IP (para APPN HPR en redes IP)** (126)


</dt> <dd></dd> <dt>

<span id="CATV_MAC_Layer"></span><span id="catv_mac_layer"></span><span id="CATV_MAC_LAYER"></span>

**Capa MAC de CATV** (127)


</dt> <dd></dd> <dt>

<span id="CATV_Downstream"></span><span id="catv_downstream"></span><span id="CATV_DOWNSTREAM"></span>

**CATV de bajada** (128)


</dt> <dd></dd> <dt>

<span id="CATV_Upstream"></span><span id="catv_upstream"></span><span id="CATV_UPSTREAM"></span>

**CATV Upstream** (129)


</dt> <dd></dd> <dt>

<span id="Avalon_12MPP_Switch"></span><span id="avalon_12mpp_switch"></span><span id="AVALON_12MPP_SWITCH"></span>

**Conmutador de 12MPP de Asíns** (130)


</dt> <dd></dd> <dt>

<span id="Tunnel"></span><span id="tunnel"></span><span id="TUNNEL"></span>

**Tunnel** (131)


</dt> <dd></dd> <dt>

<span id="Coffee"></span><span id="coffee"></span><span id="COFFEE"></span>

**Café** (132)


</dt> <dd></dd> <dt>

<span id="Circuit_Emulation_Service"></span><span id="circuit_emulation_service"></span><span id="CIRCUIT_EMULATION_SERVICE"></span>

**Servicio de emulación de** circuito (133)


</dt> <dd></dd> <dt>

<span id="ATM_SubInterface"></span><span id="atm_subinterface"></span><span id="ATM_SUBINTERFACE"></span>

**Atm SubInterface** (134)


</dt> <dd></dd> <dt>

<span id="Layer_2_VLAN_using_802.1Q"></span><span id="layer_2_vlan_using_802.1q"></span><span id="LAYER_2_VLAN_USING_802.1Q"></span>

**VLAN de nivel 2 mediante 802.1Q** (135)


</dt> <dd></dd> <dt>

<span id="Layer_3_VLAN_using_IP"></span><span id="layer_3_vlan_using_ip"></span><span id="LAYER_3_VLAN_USING_IP"></span>

**VLAN de nivel 3 mediante IP** (136)


</dt> <dd></dd> <dt>

<span id="Layer_3_VLAN_using_IPX"></span><span id="layer_3_vlan_using_ipx"></span><span id="LAYER_3_VLAN_USING_IPX"></span>

**VLAN de nivel 3 mediante IPX** (137)


</dt> <dd></dd> <dt>

<span id="Digital_Power_Line"></span><span id="digital_power_line"></span><span id="DIGITAL_POWER_LINE"></span>

**Digital Power Line** (138)


</dt> <dd></dd> <dt>

<span id="Multimedia_Mail_over_IP"></span><span id="multimedia_mail_over_ip"></span><span id="MULTIMEDIA_MAIL_OVER_IP"></span>

**Correo multimedia a través de IP** (139)


</dt> <dd></dd> <dt>

<span id="DTM"></span><span id="dtm"></span>

**DTM** (140)


</dt> <dd></dd> <dt>

<span id="DCN"></span><span id="dcn"></span>

**DCN** (141)


</dt> <dd></dd> <dt>

<span id="IP_Forwarding"></span><span id="ip_forwarding"></span><span id="IP_FORWARDING"></span>

**Reenvío IP** (142)


</dt> <dd></dd> <dt>

<span id="MSDSL"></span><span id="msdsl"></span>

**MSDSL** (143)


</dt> <dd></dd> <dt>

<span id="IEEE_1394"></span><span id="ieee_1394"></span>

**IEEE 1394** (144)


</dt> <dd></dd> <dt>

<span id="IF-GSN_HIPPI-6400"></span><span id="if-gsn_hippi-6400"></span>

**IF-GSN/HIPPI-6400** (145)


</dt> <dd></dd> <dt>

<span id="DVB-RCC_MAC_Layer"></span><span id="dvb-rcc_mac_layer"></span><span id="DVB-RCC_MAC_LAYER"></span>

**Capa DE MAC DE RCC DE GRS** (146)


</dt> <dd></dd> <dt>

<span id="DVB-RCC_Downstream"></span><span id="dvb-rcc_downstream"></span><span id="DVB-RCC_DOWNSTREAM"></span>

**DT-RCC de bajada** (147)


</dt> <dd></dd> <dt>

<span id="DVB-RCC_Upstream"></span><span id="dvb-rcc_upstream"></span><span id="DVB-RCC_UPSTREAM"></span>

**UPSTREAM-RCC Upstream** (148)


</dt> <dd></dd> <dt>

<span id="ATM_Virtual"></span><span id="atm_virtual"></span><span id="ATM_VIRTUAL"></span>

**ATM Virtual** (149)


</dt> <dd></dd> <dt>

<span id="MPLS_Tunnel"></span><span id="mpls_tunnel"></span><span id="MPLS_TUNNEL"></span>

**MPLS Tunnel** (150)


</dt> <dd></dd> <dt>

<span id="SRP"></span><span id="srp"></span>

**SRP** (151)


</dt> <dd></dd> <dt>

<span id="Voice_over_ATM"></span><span id="voice_over_atm"></span><span id="VOICE_OVER_ATM"></span>

**Voz a través de un cajero** automático (152)


</dt> <dd></dd> <dt>

<span id="Voice_over_Frame_Relay"></span><span id="voice_over_frame_relay"></span><span id="VOICE_OVER_FRAME_RELAY"></span>

**Voice over Frame Relay** (153)


</dt> <dd></dd> <dt>

<span id="ISDL"></span><span id="isdl"></span>

**ISDL** (154)


</dt> <dd></dd> <dt>

<span id="Composite_Link"></span><span id="composite_link"></span><span id="COMPOSITE_LINK"></span>

**Vínculo compuesto** (155)


</dt> <dd></dd> <dt>

<span id="SS7_Signaling_Link"></span><span id="ss7_signaling_link"></span><span id="SS7_SIGNALING_LINK"></span>

**Vínculo de señalización SS7** (156)


</dt> <dd></dd> <dt>

<span id="Proprietary_P2P_Wireless"></span><span id="proprietary_p2p_wireless"></span><span id="PROPRIETARY_P2P_WIRELESS"></span>

**P2P Wireless** propietario (157)


</dt> <dd></dd> <dt>

<span id="Frame_Forward"></span><span id="frame_forward"></span><span id="FRAME_FORWARD"></span>

**Avance de** marco (158)


</dt> <dd></dd> <dt>

<span id="RFC1483_Multiprotocol_over_ATM"></span><span id="rfc1483_multiprotocol_over_atm"></span><span id="RFC1483_MULTIPROTOCOL_OVER_ATM"></span>

**RFC1483 Multiprotocol over ATM** (159)


</dt> <dd></dd> <dt>

<span id="USB"></span><span id="usb"></span>

**USB** (160)


</dt> <dd></dd> <dt>

<span id="IEEE_802.3ad_Link_Aggregate"></span><span id="ieee_802.3ad_link_aggregate"></span><span id="IEEE_802.3AD_LINK_AGGREGATE"></span>

**Agregado de vínculo IEEE 802.3ad** (161)


</dt> <dd></dd> <dt>

<span id="BGP_Policy_Accounting"></span><span id="bgp_policy_accounting"></span><span id="BGP_POLICY_ACCOUNTING"></span>

**Contabilidad de directivas BGP** (162)


</dt> <dd></dd> <dt>

<span id="FRF_.16_Multilink_FR"></span><span id="frf_.16_multilink_fr"></span><span id="FRF_.16_MULTILINK_FR"></span>

**FRF .16 Multilink FR** (163)


</dt> <dd></dd> <dt>

<span id="H.323_Gatekeeper"></span><span id="h.323_gatekeeper"></span><span id="H.323_GATEKEEPER"></span>

**H.323 Gatekeeper** (164)


</dt> <dd></dd> <dt>

<span id="H.323_Proxy"></span><span id="h.323_proxy"></span><span id="H.323_PROXY"></span>

**H.323 Proxy** (165)


</dt> <dd></dd> <dt>

<span id="MPLS"></span><span id="mpls"></span>

**MPLS** (166)


</dt> <dd></dd> <dt>

<span id="Multi-Frequency_Signaling_Link"></span><span id="multi-frequency_signaling_link"></span><span id="MULTI-FREQUENCY_SIGNALING_LINK"></span>

**Vínculo de señalización de varias frecuencias** (167)


</dt> <dd></dd> <dt>

<span id="HDSL-2"></span><span id="hdsl-2"></span>

**HDSL-2** (168)


</dt> <dd></dd> <dt>

<span id="S-HDSL"></span><span id="s-hdsl"></span>

**S-HDSL** (169)


</dt> <dd></dd> <dt>

<span id="DS1_Facility_Data_Link"></span><span id="ds1_facility_data_link"></span><span id="DS1_FACILITY_DATA_LINK"></span>

**Vínculo de datos de la instalación de DS1** (170)


</dt> <dd></dd> <dt>

<span id="Packet_over_SONET_SDH"></span><span id="packet_over_sonet_sdh"></span><span id="PACKET_OVER_SONET_SDH"></span>

**Paquete sobre SONET/SDH** (171)


</dt> <dd></dd> <dt>

<span id="DVB-ASI_Input"></span><span id="dvb-asi_input"></span><span id="DVB-ASI_INPUT"></span>

**Entrada DE SI-ASI** (172)


</dt> <dd></dd> <dt>

<span id="DVB-ASI_Output"></span><span id="dvb-asi_output"></span><span id="DVB-ASI_OUTPUT"></span>

**Salida de DVB-ASI** (173)


</dt> <dd></dd> <dt>

<span id="Power_Line"></span><span id="power_line"></span><span id="POWER_LINE"></span>

**Power Line** (174)


</dt> <dd></dd> <dt>

<span id="Non_Facility_Associated_Signaling"></span><span id="non_facility_associated_signaling"></span><span id="NON_FACILITY_ASSOCIATED_SIGNALING"></span>

**Señalización no asociada a instalaciones** (175)


</dt> <dd></dd> <dt>

<span id="TR008"></span><span id="tr008"></span>

**TR008** (176)


</dt> <dd></dd> <dt>

<span id="GR303_RDT"></span><span id="gr303_rdt"></span>

**GR303 RDT** (177)


</dt> <dd></dd> <dt>

<span id="GR303_IDT"></span><span id="gr303_idt"></span>

**GR303 IDT** (178)


</dt> <dd></dd> <dt>

<span id="ISUP"></span><span id="isup"></span>

**ISUP** (179)


</dt> <dd></dd> <dt>

<span id="Proprietary_Wireless_MAC_Layer"></span><span id="proprietary_wireless_mac_layer"></span><span id="PROPRIETARY_WIRELESS_MAC_LAYER"></span>

**Capa mac inalámbrica propietaria** (180)


</dt> <dd></dd> <dt>

<span id="Proprietary_Wireless_Downstream"></span><span id="proprietary_wireless_downstream"></span><span id="PROPRIETARY_WIRELESS_DOWNSTREAM"></span>

**Bajada inalámbrica propietaria** (181)


</dt> <dd></dd> <dt>

<span id="Proprietary_Wireless_Upstream"></span><span id="proprietary_wireless_upstream"></span><span id="PROPRIETARY_WIRELESS_UPSTREAM"></span>

**Canal ascendente inalámbrico propietario** (182)


</dt> <dd></dd> <dt>

<span id="HIPERLAN_Type_2"></span><span id="hiperlan_type_2"></span><span id="HIPERLAN_TYPE_2"></span>

**HIPERLAN tipo 2** (183)


</dt> <dd></dd> <dt>

<span id="Proprietary_Broadband_Wireless_Access_Point_to_Mulipoint"></span><span id="proprietary_broadband_wireless_access_point_to_mulipoint"></span><span id="PROPRIETARY_BROADBAND_WIRELESS_ACCESS_POINT_TO_MULIPOINT"></span>

**Punto de acceso inalámbrico de banda ancha propietario a Mliopoint** (184)


</dt> <dd></dd> <dt>

<span id="SONET_Overhead_Channel"></span><span id="sonet_overhead_channel"></span><span id="SONET_OVERHEAD_CHANNEL"></span>

**Canal de sobrecarga de SONET** (185)


</dt> <dd></dd> <dt>

<span id="Digital_Wrapper_Overhead_Channel"></span><span id="digital_wrapper_overhead_channel"></span><span id="DIGITAL_WRAPPER_OVERHEAD_CHANNEL"></span>

**Canal de sobrecarga del contenedor digital** (186)


</dt> <dd></dd> <dt>

<span id="ATM_Adaptation_Layer_2"></span><span id="atm_adaptation_layer_2"></span><span id="ATM_ADAPTATION_LAYER_2"></span>

**Capa 2 de adaptación de ATM** (187)


</dt> <dd></dd> <dt>

<span id="Radio_MAC"></span><span id="radio_mac"></span><span id="RADIO_MAC"></span>

**Radio MAC** (188)


</dt> <dd></dd> <dt>

<span id="ATM_Radio"></span><span id="atm_radio"></span><span id="ATM_RADIO"></span>

**Radio ATM** (189)


</dt> <dd></dd> <dt>

<span id="Inter_Machine_Trunk"></span><span id="inter_machine_trunk"></span><span id="INTER_MACHINE_TRUNK"></span>

**Inter Machine Trunk** (190)


</dt> <dd></dd> <dt>

<span id="MVL_DSL"></span><span id="mvl_dsl"></span>

**DSL de MVL** (191)


</dt> <dd></dd> <dt>

<span id="Long_Read_DSL"></span><span id="long_read_dsl"></span><span id="LONG_READ_DSL"></span>

**DSL de lectura larga** (192)


</dt> <dd></dd> <dt>

<span id="Frame_Relay_DLCI_Endpoint"></span><span id="frame_relay_dlci_endpoint"></span><span id="FRAME_RELAY_DLCI_ENDPOINT"></span>

**Punto de conexión de DLCI de Frame Relay** (193)


</dt> <dd></dd> <dt>

<span id="ATM_VCI_Endpoint"></span><span id="atm_vci_endpoint"></span><span id="ATM_VCI_ENDPOINT"></span>

**Punto de conexión de VCI de ATM** (194)


</dt> <dd></dd> <dt>

<span id="Optical_Channel"></span><span id="optical_channel"></span><span id="OPTICAL_CHANNEL"></span>

**Canal óptico** (195)


</dt> <dd></dd> <dt>

<span id="Optical_Transport"></span><span id="optical_transport"></span><span id="OPTICAL_TRANSPORT"></span>

**Transporte óptico** (196)


</dt> <dd></dd> <dt>

<span id="Proprietary_ATM"></span><span id="proprietary_atm"></span><span id="PROPRIETARY_ATM"></span>

**Cajero automático propietario** (197)


</dt> <dd></dd> <dt>

<span id="Voice_over_Cable"></span><span id="voice_over_cable"></span><span id="VOICE_OVER_CABLE"></span>

**Voz a través de cable** (198)


</dt> <dd></dd> <dt>

<span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

**Infiniband** (199)


</dt> <dd></dd> <dt>

<span id="TE_Link"></span><span id="te_link"></span><span id="TE_LINK"></span>

**VÍNCULO DE TE** (200)


</dt> <dd></dd> <dt>

<span id="Q.2931"></span><span id="q.2931"></span>

**Q.2931** (201)


</dt> <dd></dd> <dt>

<span id="Virtual_Trunk_Group"></span><span id="virtual_trunk_group"></span><span id="VIRTUAL_TRUNK_GROUP"></span>

**Grupo de troncos** virtuales (202)


</dt> <dd></dd> <dt>

<span id="SIP_Trunk_Group"></span><span id="sip_trunk_group"></span><span id="SIP_TRUNK_GROUP"></span>

**Grupo de troncos DE SIP** (203)


</dt> <dd></dd> <dt>

<span id="SIP_Signaling"></span><span id="sip_signaling"></span><span id="SIP_SIGNALING"></span>

**Señalización DE SIP** (204)


</dt> <dd></dd> <dt>

<span id="CATV_Upstream_Channel"></span><span id="catv_upstream_channel"></span><span id="CATV_UPSTREAM_CHANNEL"></span>

**Canal ascendente de CATV** (205)


</dt> <dd></dd> <dt>

<span id="Econet"></span><span id="econet"></span><span id="ECONET"></span>

**Econet** (206)


</dt> <dd></dd> <dt>

<span id="FSAN_155Mb_PON"></span><span id="fsan_155mb_pon"></span><span id="FSAN_155MB_PON"></span>

**HANN 155 Mb DE PON** (207)


</dt> <dd></dd> <dt>

<span id="FSAN_622Mb_PON"></span><span id="fsan_622mb_pon"></span><span id="FSAN_622MB_PON"></span>

**PONN de 622 Mb** (208)


</dt> <dd></dd> <dt>

<span id="Transparent_Bridge"></span><span id="transparent_bridge"></span><span id="TRANSPARENT_BRIDGE"></span>

**Puente transparente** (209)


</dt> <dd></dd> <dt>

<span id="Line_Group"></span><span id="line_group"></span><span id="LINE_GROUP"></span>

**Grupo de** líneas (210)


</dt> <dd></dd> <dt>

<span id="Voice_E_M_Feature_Group"></span><span id="voice_e_m_feature_group"></span><span id="VOICE_E_M_FEATURE_GROUP"></span>

**Voice E&M Feature Group** (211)


</dt> <dd></dd> <dt>

<span id="Voice_FGD_EANA"></span><span id="voice_fgd_eana"></span><span id="VOICE_FGD_EANA"></span>

**Voice FGD EANA** (212)


</dt> <dd></dd> <dt>

<span id="Voice_DID"></span><span id="voice_did"></span><span id="VOICE_DID"></span>

**Voice DID** (213)


</dt> <dd></dd> <dt>

<span id="MPEG_Transport"></span><span id="mpeg_transport"></span><span id="MPEG_TRANSPORT"></span>

**Transporte MPEG** (214)


</dt> <dd></dd> <dt>

<span id="6To4"></span><span id="6to4"></span><span id="6TO4"></span>

**6To4** (215)


</dt> <dd></dd> <dt>

<span id="GTP"></span><span id="gtp"></span>

**GTP** (216)


</dt> <dd></dd> <dt>

<span id="Paradyne_EtherLoop_1"></span><span id="paradyne_etherloop_1"></span><span id="PARADYNE_ETHERLOOP_1"></span>

**Parad etherLoop 1** (217)


</dt> <dd></dd> <dt>

<span id="Paradyne_EtherLoop_2"></span><span id="paradyne_etherloop_2"></span><span id="PARADYNE_ETHERLOOP_2"></span>

**Parad etherLoop 2** (218)


</dt> <dd></dd> <dt>

<span id="Optical_Channel_Group"></span><span id="optical_channel_group"></span><span id="OPTICAL_CHANNEL_GROUP"></span>

**Grupo de canales ópticos** (219)


</dt> <dd></dd> <dt>

<span id="HomePNA"></span><span id="homepna"></span><span id="HOMEPNA"></span>

**HomePNA** (220)


</dt> <dd></dd> <dt>

<span id="GFP"></span><span id="gfp"></span>

**GFP** (221)


</dt> <dd></dd> <dt>

<span id="ciscoISLvlan"></span><span id="ciscoislvlan"></span><span id="CISCOISLVLAN"></span>

**ciscoISLvlan** (222)


</dt> <dd></dd> <dt>

<span id="actelisMetaLOOP"></span><span id="actelismetaloop"></span><span id="ACTELISMETALOOP"></span>

**actelisMetaLOOP** (223)


</dt> <dd></dd> <dt>

<span id="Fcip"></span><span id="fcip"></span><span id="FCIP"></span>

**Fcip** (224)


</dt> <dd></dd> <dt>

<span id="IANA_Reserved"></span><span id="iana_reserved"></span><span id="IANA_RESERVED"></span>

**IANA Reservado** (225..4095)


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (4096)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (4097)


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

**IPv4/v6** (4098)


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

**IPX** (4099)


</dt> <dd></dd> <dt>

<span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>

**DECnet** (4100)


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

**SNA** (4101)


</dt> <dd></dd> <dt>

<span id="CONP"></span><span id="conp"></span>

**CONP** (4102)


</dt> <dd></dd> <dt>

<span id="CLNP"></span><span id="clnp"></span>

**CLNP** (4103)


</dt> <dd></dd> <dt>

<span id="VINES"></span><span id="vines"></span>

**SARS** (4104)


</dt> <dd></dd> <dt>

<span id="XNS"></span><span id="xns"></span>

**XNS** (4105)


</dt> <dd></dd> <dt>

<span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>

**Punto de conexión de canal B de ISDN** (4106)


</dt> <dd></dd> <dt>

<span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>

**Punto de conexión de canal de ISDN D** (4107)


</dt> <dd></dd> <dt>

<span id="BGP"></span><span id="bgp"></span>

**BGP** (4108)


</dt> <dd></dd> <dt>

<span id="OSPF"></span><span id="ospf"></span>

**OSPF** (4109)


</dt> <dd></dd> <dt>

<span id="UDP"></span><span id="udp"></span>

**UDP** (4110)


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (4111)


</dt> <dd></dd> <dt>

<span id="802.11a"></span><span id="802.11A"></span>

**802.11a** (4112)


</dt> <dd></dd> <dt>

<span id="802.11b"></span><span id="802.11B"></span>

**802.11b** (4113)


</dt> <dd></dd> <dt>

<span id="802.11g"></span><span id="802.11G"></span>

**802.11g** (4114)


</dt> <dd></dd> <dt>

<span id="802.11h"></span><span id="802.11H"></span>

**802.11h** (4115)


</dt> <dd></dd> <dt>

<span id="NFS"></span><span id="nfs"></span>

**NFS** (4200)


</dt> <dd></dd> <dt>

<span id="CIFS"></span><span id="cifs"></span>

**CIFS** (4201)


</dt> <dd></dd> <dt>

<span id="DAFS"></span><span id="dafs"></span>

**DAFS** (4202)


</dt> <dd></dd> <dt>

<span id="WebDAV"></span><span id="webdav"></span><span id="WEBDAV"></span>

**WebDAV** (4203)


</dt> <dd></dd> <dt>

<span id="HTTP"></span><span id="http"></span>

**HTTP** (4204)


</dt> <dd></dd> <dt>

<span id="FTP"></span><span id="ftp"></span>

**FTP** (4205)


</dt> <dd></dd> <dt>

<span id="NDMP"></span><span id="ndmp"></span>

**NDMP** (4300)


</dt> <dd></dd> <dt>

<span id="Telnet"></span><span id="telnet"></span><span id="TELNET"></span>

**Telnet** (4400)


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

**SSH** (4401)


</dt> <dd></dd> <dt>

<span id="SM_CLP"></span><span id="sm_clp"></span>

**SM CLP** (4402)


</dt> <dd></dd> <dt>

<span id="SMTP"></span><span id="smtp"></span>

**SMTP** (4403)


</dt> <dd></dd> <dt>

<span id="LDAP"></span><span id="ldap"></span>

**LDAP** (4404)


</dt> <dd></dd> <dt>

<span id="RDP"></span><span id="rdp"></span>

**RDP** (4405)


</dt> <dd></dd> <dt>

<span id="HTTPS"></span><span id="https"></span>

**HTTPS** (4406)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Vendor Reserved** (32768.).


</dt> <dd></dd> </dl>

</dd> <dt>

**ProtocolType**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**en desuso**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Cim \_ ProtocolEndpoint**.**ProtocolIFType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ProtocolEndpoint**.**OtherTypeDescription**")
</dt> </dl>

> [!Note]  
> Descripción en desuso: enumeración que se usa para clasificar y clasificar diferentes instancias de esta clase.

 

Esta propiedad está desusada. En su lugar, use **la propiedad ProtocolIFType.**

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otros** (1)


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (2)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (3)


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

**IPX** (4)


</dt> <dd></dd> <dt>

<span id="AppleTalk"></span><span id="appletalk"></span><span id="APPLETALK"></span>

**AppleTalk** (5)


</dt> <dd></dd> <dt>

<span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>

**DECnet** (6)


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

**SNA** (7)


</dt> <dd></dd> <dt>

<span id="CONP"></span><span id="conp"></span>

**CONP** (8)


</dt> <dd></dd> <dt>

<span id="CLNP"></span><span id="clnp"></span>

**CLNP** (9)


</dt> <dd></dd> <dt>

<span id="VINES"></span><span id="vines"></span>

**SES** (10)


</dt> <dd></dd> <dt>

<span id="XNS"></span><span id="xns"></span>

**XNS** (11)


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

**ATM** (12)


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

**Frame Relay** (13)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (14)


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

**TokenRing** (15)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (16)


</dt> <dd></dd> <dt>

<span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

**Infiniband** (17)


</dt> <dd></dd> <dt>

<span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>

**Canal de fibra** (18)


</dt> <dd></dd> <dt>

<span id="ISDN_BRI_Endpoint"></span><span id="isdn_bri_endpoint"></span><span id="ISDN_BRI_ENDPOINT"></span>

**Punto de conexión BRI de ISDN** (19)


</dt> <dd></dd> <dt>

<span id="ISDN_B_Channel_Endpoint"></span><span id="isdn_b_channel_endpoint"></span><span id="ISDN_B_CHANNEL_ENDPOINT"></span>

**Punto de conexión de canal B de ISDN** (20)


</dt> <dd></dd> <dt>

<span id="ISDN_D_Channel_Endpoint"></span><span id="isdn_d_channel_endpoint"></span><span id="ISDN_D_CHANNEL_ENDPOINT"></span>

**Punto de conexión de canal de ISDN D** (21)


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

**IPv4/v6** (22)


</dt> <dd></dd> <dt>

<span id="BGP"></span><span id="bgp"></span>

**BGP** (23)


</dt> <dd></dd> <dt>

<span id="OSPF"></span><span id="ospf"></span>

**OSPF** (24)


</dt> <dd></dd> <dt>

<span id="MPLS"></span><span id="mpls"></span>

**MPLS** (25)


</dt> <dd></dd> <dt>

<span id="UDP"></span><span id="udp"></span>

**UDP** (26)


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (27)


</dt> <dd></dd> </dl>

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo de datos: **datetime**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("TimeOfLastStateChange"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| IF-MIB.ifLastChange")
</dt> </dl>

Fecha y hora en que cambió por última vez la propiedad **EnabledState.** Si **EnabledState** no ha cambiado y esta propiedad se rellena, debe establecerse en un valor de intervalo cero. Si se solicitó un cambio de estado, pero se rechazó o aún no se procesó, la propiedad no debe actualizarse.

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

[**Servicio \_ CIMAccessPoint**](cim-serviceaccesspoint.md)
</dt> </dl>

 

