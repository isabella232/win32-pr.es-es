---
description: Representa las capacidades y la administración de un dispositivo de puerto de canal de fibra (FC).
ms.assetid: 32a11971-9e18-410d-a3cd-4921a7e986f0
title: CIM_FCPort (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FCPort
- CIM_FCPort.PortType
- CIM_FCPort.SupportedCOS
- CIM_FCPort.ActiveCOS
- CIM_FCPort.SupportedFC4Types
- CIM_FCPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6a858cbb4603743e1ddd11cac71500a9e39325a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686515"
---
# <a name="cim_fcport-class"></a>\_Clase FCPort de CIM

> [!NOTE]
> Este artículo contiene referencias al término esclavo, un término que Microsoft ya no usa. Cuando se quite el término del software, se quitará también del artículo.

Representa las capacidades y la administración de un dispositivo de puerto de canal de fibra (FC).

## <a name="syntax"></a>Sintaxis

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::FC"), AMENDMENT]
class CIM_FCPort : CIM_NetworkPort
{
  uint16 PortType;
  uint16 SupportedCOS[];
  uint16 ActiveCOS[];
  uint16 SupportedFC4Types[];
  uint16 ActiveFC4Types[];
};
```

## <a name="members"></a>Miembros

> [!NOTE]
> Este artículo contiene referencias al término esclavo, un término que Microsoft ya no usa. Cuando se quite el término del software, se quitará también del artículo.

La clase **CIM \_ FCPort** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La clase **CIM \_ FCPort** tiene estas propiedades.

<dl> <dt>

**ActiveCOS**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ FCPort**.**SupportedCOS**")
</dt> </dl>

La configuración de clase activa de servicio (COS) para el canal de fibra.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="1"></span>

**1** (1)


</dt> <dd></dd> <dt>

<span id="2"></span>

**2** (2)


</dt> <dd></dd> <dt>

<span id="3"></span>

**3** (3)


</dt> <dd></dd> <dt>

<span id="4"></span>

**4** (4)


</dt> <dd></dd> <dt>

<span id="5"></span>

**5** (5)


</dt> <dd></dd> <dt>

<span id="6"></span>

**6** (6)


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

**F** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**ActiveFC4Types**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ FCPort**.**SupportedFC4Types**")
</dt> </dl>

Los protocolos FC-4 que se ejecutan en el canal de fibra.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

**ISO/IEC 8802-2 LLC** (4)


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

**IP a través de FC** (5)


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

**SCSI-FCP** (8)


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

**SCSI-GPP** (9)


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

**Patrón IPI-3** (17)


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

**IPI-3 esclavo** (18)


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

**IPI-3 del mismo nivel** (19)


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

**CP IPI-3 maestro** (21)


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

**CP IPI-3 esclavo** (22)


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

**CP IPI-3 del mismo nivel** (23)


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

**Canal SBCCS** (25)


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

**Unidad de control SBCCS** (26)


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

**Canal FC-SB-2** (27)


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

**Unidad de control FC-SB-2** (28)


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

**Canal de fibra Services (FC-GS, FC-GS-2, FC-GS-3)** (32)


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

**FC-SW** (34)


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

**FC-SNMP** (36)


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

**HIPPI-FP** (64)


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

**Control BBL** (80)


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

**PDU de LAN encapsulada BBL FDDI** (81)


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

**PDU de LAN encapsulada BBL 802,3** (82)


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

**FC-VI** (88)


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

**FC-AV** (96)


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

**Proveedor único** (255)


</dt> <dd></dd> </dl>

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("portType")
</dt> </dl>

Modo habilitado para el puerto. Los modos de puerto se definen mediante los estándares de ANSI X3. Si el puerto está conectado, será el tipo de Puerto negociado, de lo contrario, se informará del tipo de puerto configurado.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)


</dt> <dd>

La propiedad relacionada **OtherPortType** contiene una descripción de cadena del tipo de puerto.

</dd> <dt>

<span id="N"></span><span id="n"></span>

<span id="N"></span><span id="n"></span>**N** (10)


</dt> <dd>

Puerto de nodo

</dd> <dt>

<span id="NL"></span><span id="nl"></span>

<span id="NL"></span><span id="nl"></span>**Nl** (11)


</dt> <dd>

Puerto de nodo que admite el bucle de FC Arbitrated

</dd> <dt>

<span id="F_NL"></span><span id="f_nl"></span>

<span id="F_NL"></span><span id="f_nl"></span>**F/nl** (12)


</dt> <dd></dd> <dt>

<span id="Nx"></span><span id="nx"></span><span id="NX"></span>

<span id="Nx"></span><span id="nx"></span><span id="NX"></span>**NX** (13)


</dt> <dd>

El puerto puede negociar para que se convierta en un puerto de nodo (N) o en un puerto de nodo que admita FC Arbitrated Loop (NL)

</dd> <dt>

<span id="E"></span><span id="e"></span>

<span id="E"></span><span id="e"></span>**E** (14)


</dt> <dd>

Puerto de expansión que conecta elementos de tejido (por ejemplo, conmutadores FC)

</dd> <dt>

<span id="F"></span><span id="f"></span>

<span id="F"></span><span id="f"></span>**F** (15)


</dt> <dd>

Puerto de tejido (elemento)

</dd> <dt>

<span id="FL"></span><span id="fl"></span>

<span id="FL"></span><span id="fl"></span>**FL** (16)


</dt> <dd>

Puerto de tejido (elemento) que admite el bucle de FC Arbitrated

</dd> <dt>

<span id="B"></span><span id="b"></span>

<span id="B"></span><span id="b"></span>**B** (17)


</dt> <dd>

Puerto de puente

</dd> <dt>

<span id="G"></span><span id="g"></span>

<span id="G"></span><span id="g"></span>**G** (18)


</dt> <dd>

El puerto puede negociar para que se convierta en un puerto de expansión (E) o en un puerto de tejido (F)

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (16000.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportedCOS**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La configuración de clase de servicio (COS) que es compatible con el canal de fibra.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="1"></span>

**1** (1)


</dt> <dd></dd> <dt>

<span id="2"></span>

**2** (2)


</dt> <dd></dd> <dt>

<span id="3"></span>

**3** (3)


</dt> <dd></dd> <dt>

<span id="4"></span>

**4** (4)


</dt> <dd></dd> <dt>

<span id="5"></span>

**5** (5)


</dt> <dd></dd> <dt>

<span id="6"></span>

**6** (6)


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

**F** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportedFC4Types**
</dt> <dd> <dl> <dt>

Tipo de datos: matriz **UInt16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Los protocolos FC-4 que son compatibles con el canal de fibra.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconocido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Otro** (1)


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

**ISO/IEC 8802-2 LLC** (4)


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

**IP a través de FC** (5)


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

**SCSI-FCP** (8)


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

**SCSI-GPP** (9)


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

**Patrón IPI-3** (17)


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

**IPI-3 esclavo** (18)


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

**IPI-3 del mismo nivel** (19)


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

**CP IPI-3 maestro** (21)


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

**CP IPI-3 esclavo** (22)


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

**CP IPI-3 del mismo nivel** (23)


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

**Canal SBCCS** (25)


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

**Unidad de control SBCCS** (26)


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

**Canal FC-SB-2** (27)


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

**Unidad de control FC-SB-2** (28)


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

**Canal de fibra Services (FC-GS, FC-GS-2, FC-GS-3)** (32)


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

**FC-SW** (34)


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

**FC-SNMP** (36)


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

**HIPPI-FP** (64)


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

**Control BBL** (80)


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

**PDU de LAN encapsulada BBL FDDI** (81)


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

**PDU de LAN encapsulada BBL 802,3** (82)


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

**FC-VI** (88)


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

**FC-AV** (96)


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

**Proveedor único** (255)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                          |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_NETWORKPORT CIM**](cim-networkport.md)
</dt> </dl>

 

