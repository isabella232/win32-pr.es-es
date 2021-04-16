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
# <a name="cim_fcport-class"></a><span data-ttu-id="a3fa4-103">\_Clase FCPort de CIM</span><span class="sxs-lookup"><span data-stu-id="a3fa4-103">CIM\_FCPort class</span></span>

> [!NOTE]
> <span data-ttu-id="a3fa4-104">Este artículo contiene referencias al término esclavo, un término que Microsoft ya no usa.</span><span class="sxs-lookup"><span data-stu-id="a3fa4-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="a3fa4-105">Cuando se quite el término del software, se quitará también del artículo.</span><span class="sxs-lookup"><span data-stu-id="a3fa4-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="a3fa4-106">Representa las capacidades y la administración de un dispositivo de puerto de canal de fibra (FC).</span><span class="sxs-lookup"><span data-stu-id="a3fa4-106">Represents the capabilities and management of a fibre channel (FC) port device.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3fa4-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3fa4-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="a3fa4-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a3fa4-108">Members</span></span>

> [!NOTE]
> <span data-ttu-id="a3fa4-109">Este artículo contiene referencias al término esclavo, un término que Microsoft ya no usa.</span><span class="sxs-lookup"><span data-stu-id="a3fa4-109">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="a3fa4-110">Cuando se quite el término del software, se quitará también del artículo.</span><span class="sxs-lookup"><span data-stu-id="a3fa4-110">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="a3fa4-111">La clase **CIM \_ FCPort** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a3fa4-111">The **CIM\_FCPort** class has these types of members:</span></span>

-   [<span data-ttu-id="a3fa4-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a3fa4-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a3fa4-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a3fa4-113">Properties</span></span>

<span data-ttu-id="a3fa4-114">La clase **CIM \_ FCPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a3fa4-114">The **CIM\_FCPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a3fa4-115">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="a3fa4-115">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3fa4-116">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3fa4-116">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a3fa4-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3fa4-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3fa4-118">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ FCPort**.**SupportedCOS**")</span><span class="sxs-lookup"><span data-stu-id="a3fa4-118">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_FCPort**.**SupportedCOS**")</span></span>
</dt> </dl>

<span data-ttu-id="a3fa4-119">La configuración de clase activa de servicio (COS) para el canal de fibra.</span><span class="sxs-lookup"><span data-stu-id="a3fa4-119">The active class of service (COS) settings for the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a3fa4-120">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-120">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="1"></span>

<span data-ttu-id="a3fa4-121">**1** (1)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-121">**1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="a3fa4-122">**2** (2)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-122">**2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="a3fa4-123">**3** (3)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-123">**3** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="a3fa4-124">**4** (4)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-124">**4** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="5"></span>

<span data-ttu-id="a3fa4-125">**5** (5)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-125">**5** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="6"></span>

<span data-ttu-id="a3fa4-126">**6** (6)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-126">**6** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="a3fa4-127">**F** (7)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-127">**F** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a3fa4-128">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="a3fa4-128">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3fa4-129">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3fa4-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a3fa4-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3fa4-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3fa4-131">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ FCPort**.**SupportedFC4Types**")</span><span class="sxs-lookup"><span data-stu-id="a3fa4-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_FCPort**.**SupportedFC4Types**")</span></span>
</dt> </dl>

<span data-ttu-id="a3fa4-132">Los protocolos FC-4 que se ejecutan en el canal de fibra.</span><span class="sxs-lookup"><span data-stu-id="a3fa4-132">The FC-4 protocols that are running on the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a3fa4-133">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-133">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a3fa4-134">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-134">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

<span data-ttu-id="a3fa4-135">**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-135">**ISO/IEC 8802 - 2 LLC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

<span data-ttu-id="a3fa4-136">**IP a través de FC** (5)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-136">**IP over FC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

<span data-ttu-id="a3fa4-137">**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-137">**SCSI - FCP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

<span data-ttu-id="a3fa4-138">**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-138">**SCSI - GPP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

<span data-ttu-id="a3fa4-139">**Patrón IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-139">**IPI - 3 Master** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

<span data-ttu-id="a3fa4-140">**IPI-3 esclavo** (18)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-140">**IPI - 3 Slave** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

<span data-ttu-id="a3fa4-141">**IPI-3 del mismo nivel** (19)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-141">**IPI - 3 Peer** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

<span data-ttu-id="a3fa4-142">**CP IPI-3 maestro** (21)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-142">**CP IPI - 3 Master** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

<span data-ttu-id="a3fa4-143">**CP IPI-3 esclavo** (22)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-143">**CP IPI - 3 Slave** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

<span data-ttu-id="a3fa4-144">**CP IPI-3 del mismo nivel** (23)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-144">**CP IPI - 3 Peer** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

<span data-ttu-id="a3fa4-145">**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-145">**SBCCS Channel** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

<span data-ttu-id="a3fa4-146">**Unidad de control SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-146">**SBCCS Control Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

<span data-ttu-id="a3fa4-147">**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-147">**FC-SB-2 Channel** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

<span data-ttu-id="a3fa4-148">**Unidad de control FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-148">**FC-SB-2 Control Unit** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

<span data-ttu-id="a3fa4-149">**Canal de fibra Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-149">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

<span data-ttu-id="a3fa4-150">**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-150">**FC-SW** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

<span data-ttu-id="a3fa4-151">**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-151">**FC - SNMP** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

<span data-ttu-id="a3fa4-152">**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-152">**HIPPI - FP** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

<span data-ttu-id="a3fa4-153">**Control BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-153">**BBL Control** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="a3fa4-154">**PDU de LAN encapsulada BBL FDDI** (81)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-154">**BBL FDDI Encapsulated LAN PDU** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="a3fa4-155">**PDU de LAN encapsulada BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-155">**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

<span data-ttu-id="a3fa4-156">**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-156">**FC - VI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

<span data-ttu-id="a3fa4-157">**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-157">**FC - AV** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

<span data-ttu-id="a3fa4-158">**Proveedor único** (255)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-158">**Vendor Unique** (255)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a3fa4-159">**PortType**</span><span class="sxs-lookup"><span data-stu-id="a3fa4-159">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3fa4-160">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3fa4-160">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="a3fa4-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3fa4-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a3fa4-162">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("portType")</span><span class="sxs-lookup"><span data-stu-id="a3fa4-162">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="a3fa4-163">Modo habilitado para el puerto.</span><span class="sxs-lookup"><span data-stu-id="a3fa4-163">The enabled mode for the port.</span></span> <span data-ttu-id="a3fa4-164">Los modos de puerto se definen mediante los estándares de ANSI X3.</span><span class="sxs-lookup"><span data-stu-id="a3fa4-164">The port modes are defined by ANSI X3 standards.</span></span> <span data-ttu-id="a3fa4-165">Si el puerto está conectado, será el tipo de Puerto negociado, de lo contrario, se informará del tipo de puerto configurado.</span><span class="sxs-lookup"><span data-stu-id="a3fa4-165">If the port is logged in, this will be the negotiated port type, otherwise the configured port type will be reported.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a3fa4-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-166"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a3fa4-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-167"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a3fa4-168">La propiedad relacionada **OtherPortType** contiene una descripción de cadena del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="a3fa4-168">The related property **OtherPortType** contains a string description of the type of port</span></span>

</dd> <dt>

<span id="N"></span><span id="n"></span>

<span data-ttu-id="a3fa4-169"><span id="N"></span><span id="n"></span>**N** (10)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-169"><span id="N"></span><span id="n"></span>**N** (10)</span></span>


</dt> <dd>

<span data-ttu-id="a3fa4-170">Puerto de nodo</span><span class="sxs-lookup"><span data-stu-id="a3fa4-170">Node Port</span></span>

</dd> <dt>

<span id="NL"></span><span id="nl"></span>

<span data-ttu-id="a3fa4-171"><span id="NL"></span><span id="nl"></span>**Nl** (11)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-171"><span id="NL"></span><span id="nl"></span>**NL** (11)</span></span>


</dt> <dd>

<span data-ttu-id="a3fa4-172">Puerto de nodo que admite el bucle de FC Arbitrated</span><span class="sxs-lookup"><span data-stu-id="a3fa4-172">Node Port supporting FC arbitrated loop</span></span>

</dd> <dt>

<span id="F_NL"></span><span id="f_nl"></span>

<span data-ttu-id="a3fa4-173"><span id="F_NL"></span><span id="f_nl"></span>**F/nl** (12)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-173"><span id="F_NL"></span><span id="f_nl"></span>**F/NL** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Nx"></span><span id="nx"></span><span id="NX"></span>

<span data-ttu-id="a3fa4-174"><span id="Nx"></span><span id="nx"></span><span id="NX"></span>**NX** (13)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-174"><span id="Nx"></span><span id="nx"></span><span id="NX"></span>**Nx** (13)</span></span>


</dt> <dd>

<span data-ttu-id="a3fa4-175">El puerto puede negociar para que se convierta en un puerto de nodo (N) o en un puerto de nodo que admita FC Arbitrated Loop (NL)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-175">Port may negotiate to become either a node port (N) or a node port supporting FC arbitrated loop (NL)</span></span>

</dd> <dt>

<span id="E"></span><span id="e"></span>

<span data-ttu-id="a3fa4-176"><span id="E"></span><span id="e"></span>**E** (14)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-176"><span id="E"></span><span id="e"></span>**E** (14)</span></span>


</dt> <dd>

<span data-ttu-id="a3fa4-177">Puerto de expansión que conecta elementos de tejido (por ejemplo, conmutadores FC)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-177">Expansion Port connecting fabric elements (for example, FC switches)</span></span>

</dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="a3fa4-178"><span id="F"></span><span id="f"></span>**F** (15)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-178"><span id="F"></span><span id="f"></span>**F** (15)</span></span>


</dt> <dd>

<span data-ttu-id="a3fa4-179">Puerto de tejido (elemento)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-179">Fabric (element) Port</span></span>

</dd> <dt>

<span id="FL"></span><span id="fl"></span>

<span data-ttu-id="a3fa4-180"><span id="FL"></span><span id="fl"></span>**FL** (16)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-180"><span id="FL"></span><span id="fl"></span>**FL** (16)</span></span>


</dt> <dd>

<span data-ttu-id="a3fa4-181">Puerto de tejido (elemento) que admite el bucle de FC Arbitrated</span><span class="sxs-lookup"><span data-stu-id="a3fa4-181">Fabric (element) Port supporting FC arbitrated loop</span></span>

</dd> <dt>

<span id="B"></span><span id="b"></span>

<span data-ttu-id="a3fa4-182"><span id="B"></span><span id="b"></span>**B** (17)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-182"><span id="B"></span><span id="b"></span>**B** (17)</span></span>


</dt> <dd>

<span data-ttu-id="a3fa4-183">Puerto de puente</span><span class="sxs-lookup"><span data-stu-id="a3fa4-183">Bridge port</span></span>

</dd> <dt>

<span id="G"></span><span id="g"></span>

<span data-ttu-id="a3fa4-184"><span id="G"></span><span id="g"></span>**G** (18)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-184"><span id="G"></span><span id="g"></span>**G** (18)</span></span>


</dt> <dd>

<span data-ttu-id="a3fa4-185">El puerto puede negociar para que se convierta en un puerto de expansión (E) o en un puerto de tejido (F)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-185">Port may negotiate to become either an expansion port (E), or a fabric port (F)</span></span>

</dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="a3fa4-186"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Proveedor reservado** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-186"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (16000..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a3fa4-187">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="a3fa4-187">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3fa4-188">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3fa4-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a3fa4-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3fa4-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3fa4-190">La configuración de clase de servicio (COS) que es compatible con el canal de fibra.</span><span class="sxs-lookup"><span data-stu-id="a3fa4-190">The class of service (COS) settings that are supported by the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a3fa4-191">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-191">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="1"></span>

<span data-ttu-id="a3fa4-192">**1** (1)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-192">**1** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="2"></span>

<span data-ttu-id="a3fa4-193">**2** (2)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-193">**2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="3"></span>

<span data-ttu-id="a3fa4-194">**3** (3)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-194">**3** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="4"></span>

<span data-ttu-id="a3fa4-195">**4** (4)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-195">**4** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="5"></span>

<span data-ttu-id="a3fa4-196">**5** (5)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-196">**5** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="6"></span>

<span data-ttu-id="a3fa4-197">**6** (6)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-197">**6** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="F"></span><span id="f"></span>

<span data-ttu-id="a3fa4-198">**F** (7)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-198">**F** (7)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="a3fa4-199">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="a3fa4-199">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a3fa4-200">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a3fa4-200">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="a3fa4-201">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a3fa4-201">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a3fa4-202">Los protocolos FC-4 que son compatibles con el canal de fibra.</span><span class="sxs-lookup"><span data-stu-id="a3fa4-202">The FC-4 protocols that are supported by the fibre channel.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="a3fa4-203">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-203">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a3fa4-204">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-204">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>

<span data-ttu-id="a3fa4-205">**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-205">**ISO/IEC 8802 - 2 LLC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>

<span data-ttu-id="a3fa4-206">**IP a través de FC** (5)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-206">**IP over FC** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>

<span data-ttu-id="a3fa4-207">**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-207">**SCSI - FCP** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>

<span data-ttu-id="a3fa4-208">**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-208">**SCSI - GPP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>

<span data-ttu-id="a3fa4-209">**Patrón IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-209">**IPI - 3 Master** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>

<span data-ttu-id="a3fa4-210">**IPI-3 esclavo** (18)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-210">**IPI - 3 Slave** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>

<span data-ttu-id="a3fa4-211">**IPI-3 del mismo nivel** (19)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-211">**IPI - 3 Peer** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>

<span data-ttu-id="a3fa4-212">**CP IPI-3 maestro** (21)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-212">**CP IPI - 3 Master** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>

<span data-ttu-id="a3fa4-213">**CP IPI-3 esclavo** (22)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-213">**CP IPI - 3 Slave** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>

<span data-ttu-id="a3fa4-214">**CP IPI-3 del mismo nivel** (23)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-214">**CP IPI - 3 Peer** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>

<span data-ttu-id="a3fa4-215">**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-215">**SBCCS Channel** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>

<span data-ttu-id="a3fa4-216">**Unidad de control SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-216">**SBCCS Control Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>

<span data-ttu-id="a3fa4-217">**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-217">**FC-SB-2 Channel** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>

<span data-ttu-id="a3fa4-218">**Unidad de control FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-218">**FC-SB-2 Control Unit** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>

<span data-ttu-id="a3fa4-219">**Canal de fibra Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-219">**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="FC-SW"></span><span id="fc-sw"></span>

<span data-ttu-id="a3fa4-220">**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-220">**FC-SW** (34)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>

<span data-ttu-id="a3fa4-221">**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-221">**FC - SNMP** (36)</span></span>


</dt> <dd></dd> <dt>

<span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>

<span data-ttu-id="a3fa4-222">**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-222">**HIPPI - FP** (64)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>

<span data-ttu-id="a3fa4-223">**Control BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-223">**BBL Control** (80)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="a3fa4-224">**PDU de LAN encapsulada BBL FDDI** (81)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-224">**BBL FDDI Encapsulated LAN PDU** (81)</span></span>


</dt> <dd></dd> <dt>

<span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>

<span data-ttu-id="a3fa4-225">**PDU de LAN encapsulada BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-225">**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_VI"></span><span id="fc_-_vi"></span>

<span data-ttu-id="a3fa4-226">**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-226">**FC - VI** (88)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_-_AV"></span><span id="fc_-_av"></span>

<span data-ttu-id="a3fa4-227">**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-227">**FC - AV** (96)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>

<span data-ttu-id="a3fa4-228">**Proveedor único** (255)</span><span class="sxs-lookup"><span data-stu-id="a3fa4-228">**Vendor Unique** (255)</span></span>


<span data-ttu-id="a3fa4-229"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a3fa4-229"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a3fa4-230">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3fa4-230">Requirements</span></span>



| <span data-ttu-id="a3fa4-231">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3fa4-231">Requirement</span></span> | <span data-ttu-id="a3fa4-232">Value</span><span class="sxs-lookup"><span data-stu-id="a3fa4-232">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3fa4-233">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3fa4-233">Minimum supported client</span></span><br/> | <span data-ttu-id="a3fa4-234">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a3fa4-234">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="a3fa4-235">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a3fa4-235">Minimum supported server</span></span><br/> | <span data-ttu-id="a3fa4-236">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a3fa4-236">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="a3fa4-237">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a3fa4-237">Namespace</span></span><br/>                | <span data-ttu-id="a3fa4-238">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="a3fa4-238">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="a3fa4-239">MOF</span><span class="sxs-lookup"><span data-stu-id="a3fa4-239">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a3fa4-240"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a3fa4-240"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a3fa4-241">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a3fa4-241">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a3fa4-242"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a3fa4-242"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a3fa4-243">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3fa4-243">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3fa4-244">**\_NETWORKPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="a3fa4-244">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

