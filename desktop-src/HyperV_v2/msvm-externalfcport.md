---
description: Representa un puerto de Canal de fibra externo.
ms.assetid: bab3a243-5ebd-43e0-948e-ea8112e09d0a
title: Clase Msvm_ExternalFcPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ExternalFcPort
- Msvm_ExternalFcPort.SetPowerState
- Msvm_ExternalFcPort.EnableDevice
- Msvm_ExternalFcPort.OnlineDevice
- Msvm_ExternalFcPort.QuiesceDevice
- Msvm_ExternalFcPort.SaveProperties
- Msvm_ExternalFcPort.RestoreProperties
- Msvm_ExternalFcPort.InstanceID
- Msvm_ExternalFcPort.Caption
- Msvm_ExternalFcPort.Description
- Msvm_ExternalFcPort.ElementName
- Msvm_ExternalFcPort.InstallDate
- Msvm_ExternalFcPort.Name
- Msvm_ExternalFcPort.OperationalStatus
- Msvm_ExternalFcPort.StatusDescriptions
- Msvm_ExternalFcPort.Status
- Msvm_ExternalFcPort.HealthState
- Msvm_ExternalFcPort.CommunicationStatus
- Msvm_ExternalFcPort.DetailedStatus
- Msvm_ExternalFcPort.OperatingStatus
- Msvm_ExternalFcPort.PrimaryStatus
- Msvm_ExternalFcPort.EnabledState
- Msvm_ExternalFcPort.OtherEnabledState
- Msvm_ExternalFcPort.RequestedState
- Msvm_ExternalFcPort.EnabledDefault
- Msvm_ExternalFcPort.TimeOfLastStateChange
- Msvm_ExternalFcPort.AvailableRequestedStates
- Msvm_ExternalFcPort.TransitioningToState
- Msvm_ExternalFcPort.SystemCreationClassName
- Msvm_ExternalFcPort.SystemName
- Msvm_ExternalFcPort.CreationClassName
- Msvm_ExternalFcPort.DeviceID
- Msvm_ExternalFcPort.PowerManagementSupported
- Msvm_ExternalFcPort.PowerManagementCapabilities
- Msvm_ExternalFcPort.Availability
- Msvm_ExternalFcPort.StatusInfo
- Msvm_ExternalFcPort.LastErrorCode
- Msvm_ExternalFcPort.ErrorDescription
- Msvm_ExternalFcPort.ErrorCleared
- Msvm_ExternalFcPort.OtherIdentifyingInfo
- Msvm_ExternalFcPort.PowerOnHours
- Msvm_ExternalFcPort.TotalPowerOnHours
- Msvm_ExternalFcPort.IdentifyingDescriptions
- Msvm_ExternalFcPort.AdditionalAvailability
- Msvm_ExternalFcPort.MaxQuiesceTime
- Msvm_ExternalFcPort.Speed
- Msvm_ExternalFcPort.MaxSpeed
- Msvm_ExternalFcPort.RequestedSpeed
- Msvm_ExternalFcPort.UsageRestriction
- Msvm_ExternalFcPort.PortType
- Msvm_ExternalFcPort.OtherPortType
- Msvm_ExternalFcPort.OtherNetworkPortType
- Msvm_ExternalFcPort.PortNumber
- Msvm_ExternalFcPort.LinkTechnology
- Msvm_ExternalFcPort.OtherLinkTechnology
- Msvm_ExternalFcPort.PermanentAddress
- Msvm_ExternalFcPort.NetworkAddresses
- Msvm_ExternalFcPort.FullDuplex
- Msvm_ExternalFcPort.AutoSense
- Msvm_ExternalFcPort.SupportedMaximumTransmissionUnit
- Msvm_ExternalFcPort.ActiveMaximumTransmissionUnit
- Msvm_ExternalFcPort.SupportedCOS
- Msvm_ExternalFcPort.ActiveCOS
- Msvm_ExternalFcPort.SupportedFC4Types
- Msvm_ExternalFcPort.ActiveFC4Types
- Msvm_ExternalFcPort.IsHyperVCapable
- Msvm_ExternalFcPort.WWNN
- Msvm_ExternalFcPort.WWPN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f883afd2447c90c3167e8cf3145f8fd50ef2e72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686961"
---
# <a name="msvm_externalfcport-class"></a><span data-ttu-id="3ae2f-103">MSVM \_ ExternalFcPort (clase)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-103">Msvm\_ExternalFcPort class</span></span>

> [!NOTE]
> <span data-ttu-id="3ae2f-104">Este artículo contiene referencias al término esclavo, un término que Microsoft ya no usa.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="3ae2f-105">Cuando se quite el término del software, se quitará también del artículo.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="3ae2f-106">Representa un puerto de Canal de fibra externo.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-106">Represents an external Fibre Channel port.</span></span>

<span data-ttu-id="3ae2f-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ae2f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3ae2f-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ExternalFcPort : CIM_FCPort
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
  uint16   EnabledState = 2;
  string   OtherEnabledState;
  uint16   RequestedState = 12;
  uint16   EnabledDefault = 2;
  datetime TimeOfLastStateChange;
  uint16   AvailableRequestedStates[];
  uint16   TransitioningToState;
  string   SystemCreationClassName;
  string   SystemName;
  string   CreationClassName;
  string   DeviceID;
  boolean  PowerManagementSupported;
  uint16   PowerManagementCapabilities[];
  uint16   Availability;
  uint16   StatusInfo;
  uint32   LastErrorCode;
  string   ErrorDescription;
  boolean  ErrorCleared;
  string   OtherIdentifyingInfo[];
  uint64   PowerOnHours;
  uint64   TotalPowerOnHours;
  string   IdentifyingDescriptions[];
  uint16   AdditionalAvailability[];
  uint64   MaxQuiesceTime;
  uint64   Speed;
  uint64   MaxSpeed;
  uint64   RequestedSpeed;
  uint16   UsageRestriction;
  uint16   PortType;
  string   OtherPortType;
  string   OtherNetworkPortType;
  uint16   PortNumber;
  uint16   LinkTechnology;
  string   OtherLinkTechnology;
  string   PermanentAddress;
  string   NetworkAddresses[];
  boolean  FullDuplex;
  boolean  AutoSense;
  uint64   SupportedMaximumTransmissionUnit;
  uint64   ActiveMaximumTransmissionUnit;
  uint16   SupportedCOS[];
  uint16   ActiveCOS[];
  uint16   SupportedFC4Types[];
  uint16   ActiveFC4Types[];
  boolean  IsHyperVCapable;
  string   WWNN;
  string   WWPN;
};
```

## <a name="members"></a><span data-ttu-id="3ae2f-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="3ae2f-109">Members</span></span>

<span data-ttu-id="3ae2f-110">La clase **MSVM \_ ExternalFcPort** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3ae2f-110">The **Msvm\_ExternalFcPort** class has these types of members:</span></span>

-   [<span data-ttu-id="3ae2f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="3ae2f-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="3ae2f-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ae2f-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3ae2f-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="3ae2f-113">Methods</span></span>

<span data-ttu-id="3ae2f-114">La clase **MSVM \_ ExternalFcPort** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-114">The **Msvm\_ExternalFcPort** class has these methods.</span></span>



| <span data-ttu-id="3ae2f-115">Método</span><span class="sxs-lookup"><span data-stu-id="3ae2f-115">Method</span></span>                                                               | <span data-ttu-id="3ae2f-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="3ae2f-116">Description</span></span>                              |
|:---------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="3ae2f-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-117">**EnableDevice**</span></span>                                                     | <span data-ttu-id="3ae2f-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3ae2f-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-119">**OnlineDevice**</span></span>                                                     | <span data-ttu-id="3ae2f-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3ae2f-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-121">**QuiesceDevice**</span></span>                                                    | <span data-ttu-id="3ae2f-122">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="3ae2f-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-123">**RequestStateChange**</span></span>](msvm-externalfcport-requeststatechange.md) | <span data-ttu-id="3ae2f-124">Solicita un cambio de estado</span><span class="sxs-lookup"><span data-stu-id="3ae2f-124">Requests a state change</span></span><br/>       |
| [<span data-ttu-id="3ae2f-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-125">**Reset**</span></span>](msvm-externalfcport-reset.md)                           | <span data-ttu-id="3ae2f-126">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="3ae2f-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-127">**RestoreProperties**</span></span>                                                | <span data-ttu-id="3ae2f-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3ae2f-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-129">**SaveProperties**</span></span>                                                   | <span data-ttu-id="3ae2f-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="3ae2f-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-131">**SetPowerState**</span></span>                                                    | <span data-ttu-id="3ae2f-132">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="3ae2f-133">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3ae2f-133">Properties</span></span>

<span data-ttu-id="3ae2f-134">La clase **MSVM \_ ExternalFcPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-134">The **Msvm\_ExternalFcPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3ae2f-135">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-136">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-138">Matriz de enteros que indica las clases de servicio que están activas.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="3ae2f-139">Los co admitidos se especifican mediante la propiedad **SupportedCOS** .</span><span class="sxs-lookup"><span data-stu-id="3ae2f-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="3ae2f-140">Esta propiedad se hereda de **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="3ae2f-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-142"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-143"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-144"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-145"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-146"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-147"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-148"><span id="F"></span><span id="f"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ae2f-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-150">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-152">Matriz de enteros que indica los protocolos Canal de fibra FC-4 que se están ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="3ae2f-153">La propiedad **SupportedFC4Types** especifica una lista de todos los protocolos admitidos.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="3ae2f-154">Esta propiedad se hereda de **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="3ae2f-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP a través de FC** (5)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Patrón IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 esclavo** (18)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 del mismo nivel** (19)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 maestro** (21)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 esclavo** (22)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 del mismo nivel** (23)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unidad de control SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unidad de control FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Canal de fibra Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Control BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL FDDI** (81)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Proveedor único** (255)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ae2f-181">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-182">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-184">Calificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3ae2f-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-185">La unidad de transmisión máxima (MTU) activa o negociada que se puede admitir, en bytes.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="3ae2f-186">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-187">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-188">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-190">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="3ae2f-191">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-192">**Percepción automática**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-193">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-195">Indica si el puerto es capaz de determinar automáticamente la velocidad u otras características de comunicación de los medios de red conectados.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="3ae2f-196">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-197">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-198">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-200">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-200">The primary availability and status of the device.</span></span> <span data-ttu-id="3ae2f-201">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-202">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-203">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-205">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="3ae2f-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="3ae2f-206">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-207">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-210">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-210">A short description of the object.</span></span> <span data-ttu-id="3ae2f-211">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-212">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-213">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-215">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="3ae2f-216">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3ae2f-217">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3ae2f-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="3ae2f-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3ae2f-225">)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ae2f-226">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-229">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-229">The scoping system's creation class name.</span></span> <span data-ttu-id="3ae2f-230">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-231">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-232">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-234">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-234">A description of the object.</span></span> <span data-ttu-id="3ae2f-235">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-237">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-239">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="3ae2f-240">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3ae2f-241">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3ae2f-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="3ae2f-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3ae2f-250">)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ae2f-251">**ID**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-254">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="3ae2f-255">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-259">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-259">A display name for the object.</span></span> <span data-ttu-id="3ae2f-260">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-261">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-262">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-264">Configuración predeterminada o de inicio de un administrador para la propiedad **EnabledState** de un elemento.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="3ae2f-265">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-267">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-269">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="3ae2f-270">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="3ae2f-271">Value</span><span class="sxs-lookup"><span data-stu-id="3ae2f-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="3ae2f-272">Significado</span><span class="sxs-lookup"><span data-stu-id="3ae2f-272">Meaning</span></span>                                                                                                                                                                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="3ae2f-273"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3ae2f-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="3ae2f-274">No se pudo determinar el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                           |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="3ae2f-275"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="3ae2f-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                        |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="3ae2f-276"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="3ae2f-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="3ae2f-277">El elemento se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-277">The element is running.</span></span><br/>                                                                                                                                                                                     |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="3ae2f-278"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="3ae2f-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="3ae2f-279">El elemento está desactivado.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-279">The element is turned off.</span></span><br/>                                                                                                                                                                                  |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="3ae2f-280"><dt>**Cerrando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="3ae2f-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="3ae2f-281">El elemento está en el proceso de pasar a un Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                                 |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="3ae2f-282"><dt>**No aplicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3ae2f-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="3ae2f-283">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                                     |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="3ae2f-284"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3ae2f-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="3ae2f-285">Es posible que el elemento esté completando comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                                |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="3ae2f-286"><dt>**En la prueba**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3ae2f-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="3ae2f-287">El elemento está en un estado de prueba.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-287">The element is in a test state.</span></span><br/>                                                                                                                                                                             |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="3ae2f-288"><dt>**Aplazado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="3ae2f-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="3ae2f-289">Es posible que el elemento esté completando los comandos, pero pondrá en cola todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                               |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="3ae2f-290">Modo <dt>**inactivo**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="3ae2f-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="3ae2f-291">El elemento está habilitado, pero está en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-291">The element is enabled, but it is in a restricted mode.</span></span> <span data-ttu-id="3ae2f-292">El comportamiento del elemento es similar al estado habilitado (2), pero solo procesa un conjunto restringido de comandos.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="3ae2f-293">Todas las demás solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="3ae2f-294"><dt>**Inicio**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="3ae2f-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="3ae2f-295">El elemento está en proceso de pasar a un estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="3ae2f-296">Las nuevas solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-296">New requests are queued.</span></span><br/>                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="3ae2f-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-298">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-300">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="3ae2f-301">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-305">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="3ae2f-306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-307">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-308">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-310">Indica si el puerto está funcionando en modo dúplex completo.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="3ae2f-311">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-313">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-315">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-315">The current health of the element.</span></span> <span data-ttu-id="3ae2f-316">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-318">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-320">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="3ae2f-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="3ae2f-321">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-323">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-325">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-325">The date and time when the object was installed.</span></span> <span data-ttu-id="3ae2f-326">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="3ae2f-327">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-329">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-331">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-332">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="3ae2f-333">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-334">**IsHyperVCapable**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-334">**IsHyperVCapable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-335">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-335">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-337">Si esta propiedad es **true**, este puerto canal de fibra se puede conectar a los conmutadores y, por tanto, puede proporcionar conectividad a una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-337">If this property is **True**, this Fibre Channel port can be connected to the switches and thus can provide connectivity to a virtual machine.</span></span> <span data-ttu-id="3ae2f-338">Si esta propiedad es **false**, este puerto no se puede usar en la arquitectura canal de fibra la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-338">If this property is **False**, then this port cannot be used by the virtual machine Fibre Channel architecture.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-339">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-339">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-340">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-340">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-342">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-342">The last error code reported by the logical device.</span></span> <span data-ttu-id="3ae2f-343">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-343">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-344">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-344">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-345">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-345">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-346">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-346">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-347">Especifica el tipo de tecnología de vínculo para el puerto.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-347">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="3ae2f-348">Cuando se establece en 1 (otro), la propiedad **OtherLinkTechnology** contiene una descripción de cadena del tipo de vínculo.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-348">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="3ae2f-349">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-349">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="3ae2f-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-350"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-351"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-351"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-352"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-352"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-353"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-353"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-354"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-354"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-355"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-355"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-356"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-356"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-357"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-357"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-358"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-358"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-359"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarrojos** (9)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-359"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-360"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-360"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-361"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**LAN inalámbrica** (11)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-361"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ae2f-362">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-362">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-363">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-363">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-364">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-364">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-365">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-365">This property has been deprecated.</span></span> <span data-ttu-id="3ae2f-366">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-366">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-367">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-367">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-368">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-368">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-369">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-369">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-370">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="3ae2f-370">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-371">Ancho de banda máximo del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-371">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="3ae2f-372">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-372">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-373">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-373">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-374">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-374">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-375">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-376">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-376">The label by which the object is known.</span></span> <span data-ttu-id="3ae2f-377">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-377">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-378">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-378">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-379">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-379">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-380">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-380">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-381">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-381">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-382">Una matriz de cadenas que contienen las direcciones MAC para el puerto.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-382">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="3ae2f-383">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-383">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-384">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-384">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-385">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-385">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-386">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-386">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-387">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="3ae2f-387">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="3ae2f-388">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-388">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3ae2f-389">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-389">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3ae2f-390"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-390"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-391"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-391"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-392"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-392"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-393"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-393"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-394"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-394"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-395"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-395"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-396"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-396"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-397"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-397"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-398"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-398"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-399"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-399"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-400"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-400"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-401"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-401"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-402"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-402"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-403"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-403"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-404"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-404"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-405"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-405"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-406"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-406"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-407"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-407"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-408"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="3ae2f-408"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3ae2f-409">)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-409">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ae2f-410">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-410">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-411">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-411">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-412">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-413">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-413">The current statuses of the object.</span></span> <span data-ttu-id="3ae2f-414">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-414">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-415">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-415">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-416">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-416">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-417">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-417">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-418">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-418">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="3ae2f-419">Esta propiedad debe establecerse en **null** cuando la propiedad **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-419">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="3ae2f-420">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-420">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-421">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-421">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-422">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-422">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-423">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-424">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-424">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="3ae2f-425">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-425">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-426">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-426">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-427">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-428">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-429">Un valor de cadena que describe **LinkTechnology** cuando se establece en 1, (otro).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-429">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="3ae2f-430">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-430">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-431">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-431">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-432">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-432">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-433">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-434">El uso de esta propiedad está en desuso en lugar de la propiedad **portType** .</span><span class="sxs-lookup"><span data-stu-id="3ae2f-434">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="3ae2f-435">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-435">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-436">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-436">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-437">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-437">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-438">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-438">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-439">Describe el tipo de módulo, cuando **portType** está establecido en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-439">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="3ae2f-440">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-440">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-441">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-441">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-442">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-442">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-443">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-443">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-444">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-444">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-445">La dirección de red que está codificada en un puerto.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-445">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="3ae2f-446">Esta dirección codificada se puede cambiar mediante una actualización de firmware o una configuración de software.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-446">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="3ae2f-447">Cuando se realiza este cambio, el campo debe actualizarse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-447">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="3ae2f-448">Esta propiedad debe ser **null** si no existe ninguna dirección codificada para el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-448">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="3ae2f-449">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-449">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-450">**NúmeroDePuerto**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-450">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-451">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-452">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-453">El número de puerto.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-453">The port number.</span></span> <span data-ttu-id="3ae2f-454">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-454">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-455">**PortType**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-455">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-456">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-456">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-457">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-457">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-458">Modo específico que está habilitado actualmente para el puerto.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-458">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="3ae2f-459">Cuando se establece en 1 (otro), la propiedad **OtherPortType** relacionada contiene una descripción de cadena del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-459">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="3ae2f-460">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-460">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="3ae2f-461"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-461"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-462"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-462"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-463"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 cobre 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-463"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-464"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-464"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-465"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-465"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-466"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-466"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-467"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-467"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-468"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-468"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-469"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-469"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-470"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 fibra 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-470"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-471"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-471"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-472"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-472"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-473"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-473"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-474"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-474"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-475"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-475"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-476"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-476"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-477"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-477"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-478"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-478"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-479"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-479"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-480"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-480"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-481"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-uevo** (111)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-481"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-482"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-482"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ae2f-483">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-483">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-484">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-484">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-485">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-486">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-486">The power management capabilities of the device.</span></span> <span data-ttu-id="3ae2f-487">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-488">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-488">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-489">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-489">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-490">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-491">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-491">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="3ae2f-492">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-493">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-493">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-494">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-494">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-495">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-496">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-496">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="3ae2f-497">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-497">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-498">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-498">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-499">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-499">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-500">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-500">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-501">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-501">Provides high level status information.</span></span> <span data-ttu-id="3ae2f-502">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-502">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="3ae2f-503">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-503">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="3ae2f-504">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-504">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="3ae2f-505"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-505"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-506"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-506"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-507"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-507"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-508"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-508"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-509"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-509"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-510"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="3ae2f-510"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="3ae2f-511">)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-511">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ae2f-512">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-512">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-513">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-513">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-514">Tipo de acceso: solo escritura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-514">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-515">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="3ae2f-515">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-516">Ancho de banda solicitado del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-516">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="3ae2f-517">El ancho de banda real se registra en la propiedad **Speed** .</span><span class="sxs-lookup"><span data-stu-id="3ae2f-517">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="3ae2f-518">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-518">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-519">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-519">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-520">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-520">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-521">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-521">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-522">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-522">The last requested or desired state for the element.</span></span> <span data-ttu-id="3ae2f-523">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-523">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-524">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-524">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-525">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-525">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-526">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-526">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-527">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="3ae2f-527">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-528">Ancho de banda del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-528">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="3ae2f-529">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-529">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-530">**Estado**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-530">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-531">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-531">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-532">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-533">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-533">The current status of the object.</span></span> <span data-ttu-id="3ae2f-534">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-535">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-535">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-536">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-536">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-537">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-538">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="3ae2f-538">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="3ae2f-539">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-539">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-540">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-540">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-541">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-541">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-542">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-543">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-543">The current state of the logical device.</span></span> <span data-ttu-id="3ae2f-544">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-544">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-545">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-545">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-546">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-546">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-547">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-547">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-548">Matriz de enteros que indica el Canal de fibra clases de servicio (COS) que se admiten.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-548">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="3ae2f-549">La propiedad **ActiveCOS** especifica los cos activos.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-549">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="3ae2f-550">Esta propiedad se hereda de **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-550">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="3ae2f-551"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-551"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-552"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-552"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-553"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-553"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-554"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-554"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-555"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-555"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-556"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-556"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-557"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-557"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-558"><span id="F_"></span><span id="f_"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-558"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ae2f-559">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-559">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-560">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-560">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-561">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-561">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-562">Matriz de enteros que indica los protocolos Canal de fibra FC-4 admitidos.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-562">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="3ae2f-563">Los protocolos que están activos y en ejecución se especifican mediante la propiedad **ActiveFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="3ae2f-563">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="3ae2f-564">Esta propiedad se hereda de **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-564">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="3ae2f-565"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-565"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-566"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-566"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-567"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-567"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-568"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP a través de FC** (5)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-568"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-569"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-569"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-570"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-570"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-571"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Patrón IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-571"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-572"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 esclavo** (18)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-572"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-573"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 del mismo nivel** (19)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-573"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-574"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 maestro** (21)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-574"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-575"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 esclavo** (22)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-575"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-576"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 del mismo nivel** (23)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-576"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-577"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-577"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-578"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unidad de control SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-578"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-579"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-579"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-580"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unidad de control FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-580"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-581"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Canal de fibra Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-581"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-582"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-582"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-583"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-583"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-584"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-584"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-585"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Control BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-585"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-586"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL FDDI** (81)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-586"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-587"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-587"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-588"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-588"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-589"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-589"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-590"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Proveedor único** (255)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-590"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ae2f-591">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-591">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-592">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-592">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-593">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-593">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-594">Calificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="3ae2f-594">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-595">La unidad de transmisión máxima (MTU) que se puede admitir, en bytes.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-595">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="3ae2f-596">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-596">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-597">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-597">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-598">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-599">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-599">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-600">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-600">The scoping system's creation class name.</span></span> <span data-ttu-id="3ae2f-601">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-601">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-602">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-602">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-603">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-603">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-604">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-604">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-605">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-605">The scoping system's name.</span></span> <span data-ttu-id="3ae2f-606">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-606">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-607">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-607">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-608">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-608">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-609">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-609">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-610">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-610">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="3ae2f-611">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-611">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-612">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-612">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-613">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-613">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-614">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-615">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-615">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="3ae2f-616">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-616">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-617">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-617">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-618">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-618">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-619">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-619">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-620">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-620">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="3ae2f-621">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-621">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-622">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-622">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-623">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-623">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-624">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-624">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-625">En algunas circunstancias, un puerto lógico puede identificarse como un puerto de front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-625">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="3ae2f-626">Un ejemplo de esta situación sería una matriz de almacenamiento que podría tener puertos back-end para comunicarse con las unidades de disco y los puertos front-end para comunicarse con los hosts.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-626">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="3ae2f-627">Si no hay ninguna restricción sobre el uso del puerto, el valor debe establecerse en 4 (no restringido).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-627">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="3ae2f-628">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="3ae2f-628">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="3ae2f-629"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-629"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-630"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Solo front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-630"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-631"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Solo back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-631"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-632"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**No restringido** (4)</span><span class="sxs-lookup"><span data-stu-id="3ae2f-632"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="3ae2f-633">**WWNN**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-633">**WWNN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-634">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-634">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-635">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-635">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-636">Nombre del nodo World Wide node para este puerto Canal de fibra.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-636">The world wide node name for this Fibre Channel port.</span></span>

</dd> <dt>

<span data-ttu-id="3ae2f-637">**WWPN**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-637">**WWPN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3ae2f-638">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3ae2f-638">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3ae2f-639">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3ae2f-639">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3ae2f-640">Nombre de Puerto WWPN de este puerto de Canal de fibra.</span><span class="sxs-lookup"><span data-stu-id="3ae2f-640">The world wide port name for this Fibre Channel port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3ae2f-641">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3ae2f-641">Requirements</span></span>



| <span data-ttu-id="3ae2f-642">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ae2f-642">Requirement</span></span> | <span data-ttu-id="3ae2f-643">Value</span><span class="sxs-lookup"><span data-stu-id="3ae2f-643">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ae2f-644">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ae2f-644">Minimum supported client</span></span><br/> | <span data-ttu-id="3ae2f-645">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ae2f-645">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="3ae2f-646">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3ae2f-646">Minimum supported server</span></span><br/> | <span data-ttu-id="3ae2f-647">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="3ae2f-647">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3ae2f-648">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3ae2f-648">Namespace</span></span><br/>                | <span data-ttu-id="3ae2f-649">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="3ae2f-649">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="3ae2f-650">MOF</span><span class="sxs-lookup"><span data-stu-id="3ae2f-650">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3ae2f-651"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3ae2f-651"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="3ae2f-652">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3ae2f-652">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ae2f-653"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="3ae2f-653"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

