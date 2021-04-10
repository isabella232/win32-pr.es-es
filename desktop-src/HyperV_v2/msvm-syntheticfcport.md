---
description: Representa un puerto de Canal de fibra sintético.
ms.assetid: 6ca827b5-3ea0-4967-ba1f-b41e84c84009
title: Clase Msvm_SyntheticFcPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticFcPort
- Msvm_SyntheticFcPort.SetPowerState
- Msvm_SyntheticFcPort.EnableDevice
- Msvm_SyntheticFcPort.OnlineDevice
- Msvm_SyntheticFcPort.QuiesceDevice
- Msvm_SyntheticFcPort.SaveProperties
- Msvm_SyntheticFcPort.RestoreProperties
- Msvm_SyntheticFcPort.InstanceID
- Msvm_SyntheticFcPort.Caption
- Msvm_SyntheticFcPort.Description
- Msvm_SyntheticFcPort.ElementName
- Msvm_SyntheticFcPort.InstallDate
- Msvm_SyntheticFcPort.Name
- Msvm_SyntheticFcPort.OperationalStatus
- Msvm_SyntheticFcPort.StatusDescriptions
- Msvm_SyntheticFcPort.Status
- Msvm_SyntheticFcPort.HealthState
- Msvm_SyntheticFcPort.CommunicationStatus
- Msvm_SyntheticFcPort.DetailedStatus
- Msvm_SyntheticFcPort.OperatingStatus
- Msvm_SyntheticFcPort.PrimaryStatus
- Msvm_SyntheticFcPort.EnabledState
- Msvm_SyntheticFcPort.OtherEnabledState
- Msvm_SyntheticFcPort.RequestedState
- Msvm_SyntheticFcPort.EnabledDefault
- Msvm_SyntheticFcPort.TimeOfLastStateChange
- Msvm_SyntheticFcPort.AvailableRequestedStates
- Msvm_SyntheticFcPort.TransitioningToState
- Msvm_SyntheticFcPort.SystemCreationClassName
- Msvm_SyntheticFcPort.SystemName
- Msvm_SyntheticFcPort.CreationClassName
- Msvm_SyntheticFcPort.DeviceID
- Msvm_SyntheticFcPort.PowerManagementSupported
- Msvm_SyntheticFcPort.PowerManagementCapabilities
- Msvm_SyntheticFcPort.Availability
- Msvm_SyntheticFcPort.StatusInfo
- Msvm_SyntheticFcPort.LastErrorCode
- Msvm_SyntheticFcPort.ErrorDescription
- Msvm_SyntheticFcPort.ErrorCleared
- Msvm_SyntheticFcPort.OtherIdentifyingInfo
- Msvm_SyntheticFcPort.PowerOnHours
- Msvm_SyntheticFcPort.TotalPowerOnHours
- Msvm_SyntheticFcPort.IdentifyingDescriptions
- Msvm_SyntheticFcPort.AdditionalAvailability
- Msvm_SyntheticFcPort.MaxQuiesceTime
- Msvm_SyntheticFcPort.Speed
- Msvm_SyntheticFcPort.MaxSpeed
- Msvm_SyntheticFcPort.RequestedSpeed
- Msvm_SyntheticFcPort.UsageRestriction
- Msvm_SyntheticFcPort.PortType
- Msvm_SyntheticFcPort.OtherPortType
- Msvm_SyntheticFcPort.OtherNetworkPortType
- Msvm_SyntheticFcPort.PortNumber
- Msvm_SyntheticFcPort.LinkTechnology
- Msvm_SyntheticFcPort.OtherLinkTechnology
- Msvm_SyntheticFcPort.PermanentAddress
- Msvm_SyntheticFcPort.NetworkAddresses
- Msvm_SyntheticFcPort.FullDuplex
- Msvm_SyntheticFcPort.AutoSense
- Msvm_SyntheticFcPort.SupportedMaximumTransmissionUnit
- Msvm_SyntheticFcPort.ActiveMaximumTransmissionUnit
- Msvm_SyntheticFcPort.SupportedCOS
- Msvm_SyntheticFcPort.ActiveCOS
- Msvm_SyntheticFcPort.SupportedFC4Types
- Msvm_SyntheticFcPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f28614a7c885c0cfc03d546219518cda240219a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153901"
---
# <a name="msvm_syntheticfcport-class"></a><span data-ttu-id="fbf5e-103">MSVM \_ SyntheticFcPort (clase)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-103">Msvm\_SyntheticFcPort class</span></span>

> [!NOTE]
> <span data-ttu-id="fbf5e-104">Este artículo contiene referencias al término esclavo, un término que Microsoft ya no usa.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="fbf5e-105">Cuando se quite el término del software, se quitará también del artículo.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="fbf5e-106">Representa un puerto de Canal de fibra sintético.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-106">Represents a synthetic Fibre Channel port.</span></span>

<span data-ttu-id="fbf5e-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbf5e-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fbf5e-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticFcPort : CIM_FCPort
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
  uint16   LinkTechnology = 4;
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
};
```

## <a name="members"></a><span data-ttu-id="fbf5e-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="fbf5e-109">Members</span></span>

<span data-ttu-id="fbf5e-110">La clase **MSVM \_ SyntheticFcPort** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fbf5e-110">The **Msvm\_SyntheticFcPort** class has these types of members:</span></span>

-   [<span data-ttu-id="fbf5e-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="fbf5e-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="fbf5e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fbf5e-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="fbf5e-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="fbf5e-113">Methods</span></span>

<span data-ttu-id="fbf5e-114">La clase **MSVM \_ SyntheticFcPort** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-114">The **Msvm\_SyntheticFcPort** class has these methods.</span></span>



| <span data-ttu-id="fbf5e-115">Método</span><span class="sxs-lookup"><span data-stu-id="fbf5e-115">Method</span></span>                                                                | <span data-ttu-id="fbf5e-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="fbf5e-116">Description</span></span>                              |
|:----------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="fbf5e-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-117">**EnableDevice**</span></span>                                                      | <span data-ttu-id="fbf5e-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="fbf5e-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-119">**OnlineDevice**</span></span>                                                      | <span data-ttu-id="fbf5e-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="fbf5e-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-121">**QuiesceDevice**</span></span>                                                     | <span data-ttu-id="fbf5e-122">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="fbf5e-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-123">**RequestStateChange**</span></span>](msvm-syntheticfcport-requeststatechange.md) | <span data-ttu-id="fbf5e-124">Solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-124">Requests a state change.</span></span><br/>      |
| [<span data-ttu-id="fbf5e-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-125">**Reset**</span></span>](msvm-syntheticfcport-reset.md)                           | <span data-ttu-id="fbf5e-126">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="fbf5e-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-127">**RestoreProperties**</span></span>                                                 | <span data-ttu-id="fbf5e-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="fbf5e-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-129">**SaveProperties**</span></span>                                                    | <span data-ttu-id="fbf5e-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="fbf5e-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-131">**SetPowerState**</span></span>                                                     | <span data-ttu-id="fbf5e-132">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="fbf5e-133">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fbf5e-133">Properties</span></span>

<span data-ttu-id="fbf5e-134">La clase **MSVM \_ SyntheticFcPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-134">The **Msvm\_SyntheticFcPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fbf5e-135">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-136">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-138">Matriz de enteros que indica las clases de servicio que están activas.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="fbf5e-139">Los co admitidos se especifican mediante la propiedad **SupportedCOS** .</span><span class="sxs-lookup"><span data-stu-id="fbf5e-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="fbf5e-140">Esta propiedad se hereda de **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="fbf5e-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-142"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-143"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-144"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-145"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-146"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-147"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-148"><span id="F"></span><span id="f"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbf5e-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-150">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-152">Matriz de enteros que indica los protocolos Canal de fibra FC-4 que se están ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="fbf5e-153">La propiedad **SupportedFC4Types** especifica una lista de todos los protocolos admitidos.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="fbf5e-154">Esta propiedad se hereda de **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="fbf5e-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP a través de FC** (5)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Patrón IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 esclavo** (18)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 del mismo nivel** (19)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 maestro** (21)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 esclavo** (22)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 del mismo nivel** (23)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unidad de control SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unidad de control FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Canal de fibra Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Control BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL FDDI** (81)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Proveedor único** (255)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbf5e-181">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-182">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-184">Calificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="fbf5e-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-185">La unidad de transmisión máxima (MTU) activa o negociada que se puede admitir, en bytes.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="fbf5e-186">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-187">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-188">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-190">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="fbf5e-191">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-192">**Percepción automática**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-193">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-195">Indica si el puerto es capaz de determinar automáticamente la velocidad u otras características de comunicación de los medios de red conectados.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="fbf5e-196">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-197">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-198">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-200">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-200">The primary availability and status of the device.</span></span> <span data-ttu-id="fbf5e-201">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-202">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-203">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-205">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="fbf5e-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="fbf5e-206">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-207">**Caption**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-210">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-210">A short description of the object.</span></span> <span data-ttu-id="fbf5e-211">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-212">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-213">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-215">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="fbf5e-216">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fbf5e-217">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="fbf5e-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="fbf5e-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="fbf5e-225">)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbf5e-226">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-229">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-229">The scoping system's creation class name.</span></span> <span data-ttu-id="fbf5e-230">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-231">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-232">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-234">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-234">A description of the object.</span></span> <span data-ttu-id="fbf5e-235">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-237">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-239">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="fbf5e-240">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fbf5e-241">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="fbf5e-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="fbf5e-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="fbf5e-250">)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbf5e-251">**ID**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-254">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="fbf5e-255">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-259">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-259">A display name for the object.</span></span> <span data-ttu-id="fbf5e-260">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-261">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-262">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-264">Configuración predeterminada o de inicio de un administrador para la propiedad **EnabledState** de un elemento.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="fbf5e-265">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-267">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-269">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="fbf5e-270">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="fbf5e-271">Value</span><span class="sxs-lookup"><span data-stu-id="fbf5e-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="fbf5e-272">Significado</span><span class="sxs-lookup"><span data-stu-id="fbf5e-272">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="fbf5e-273"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fbf5e-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="fbf5e-274">No se pudo determinar el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="fbf5e-275"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fbf5e-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="fbf5e-276"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fbf5e-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="fbf5e-277">El elemento se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-277">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="fbf5e-278"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="fbf5e-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="fbf5e-279">El elemento está desactivado.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-279">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="fbf5e-280"><dt>**Cerrando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fbf5e-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="fbf5e-281">El elemento está en el proceso de pasar a un Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="fbf5e-282"><dt>**No aplicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="fbf5e-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="fbf5e-283">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="fbf5e-284"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="fbf5e-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="fbf5e-285">Es posible que el elemento esté completando comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="fbf5e-286"><dt>**En la prueba**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="fbf5e-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="fbf5e-287">El elemento está en un estado de prueba.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-287">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="fbf5e-288"><dt>**Aplazado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="fbf5e-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="fbf5e-289">Es posible que el elemento esté completando los comandos, pero pondrá en cola todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="fbf5e-290">Modo <dt>**inactivo**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="fbf5e-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="fbf5e-291">El elemento está habilitado pero en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-291">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="fbf5e-292">El comportamiento del elemento es similar al estado habilitado (2), pero solo procesa un conjunto restringido de comandos.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="fbf5e-293">Todas las demás solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="fbf5e-294"><dt>**Inicio**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="fbf5e-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="fbf5e-295">El elemento está en proceso de pasar a un estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="fbf5e-296">Las nuevas solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-296">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="fbf5e-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-298">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-300">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="fbf5e-301">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-305">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="fbf5e-306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-307">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-308">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-310">Indica si el puerto está funcionando en modo dúplex completo.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="fbf5e-311">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-313">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-315">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-315">The current health of the element.</span></span> <span data-ttu-id="fbf5e-316">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-318">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-320">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="fbf5e-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="fbf5e-321">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-323">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-325">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-325">The date and time when the object was installed.</span></span> <span data-ttu-id="fbf5e-326">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="fbf5e-327">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-329">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-331">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-332">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="fbf5e-333">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-335">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-337">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-337">The last error code reported by the logical device.</span></span> <span data-ttu-id="fbf5e-338">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-339">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-339">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-340">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-342">Especifica el tipo de tecnología de vínculo para el puerto.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-342">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="fbf5e-343">Cuando se establece en 1 (otro), la propiedad **OtherLinkTechnology** contiene una descripción de cadena del tipo de vínculo.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-343">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="fbf5e-344">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-344">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>



| <span data-ttu-id="fbf5e-345">Value</span><span class="sxs-lookup"><span data-stu-id="fbf5e-345">Value</span></span>                                                                                                                                                                              | <span data-ttu-id="fbf5e-346">Significado</span><span class="sxs-lookup"><span data-stu-id="fbf5e-346">Meaning</span></span>                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------|
| <span id="FC"></span><span id="fc"></span><dl> <span data-ttu-id="fbf5e-347"><dt>**FC**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="fbf5e-347"><dt>**FC**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="fbf5e-348">Canal de fibra</span><span class="sxs-lookup"><span data-stu-id="fbf5e-348">Fibre channel</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="fbf5e-349">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-349">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-350">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-350">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-351">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-351">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-352">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-352">This property has been deprecated.</span></span> <span data-ttu-id="fbf5e-353">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-353">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-354">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-354">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-355">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-355">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-356">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-356">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-357">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="fbf5e-357">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-358">Ancho de banda máximo del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-358">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="fbf5e-359">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-359">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-360">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-360">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-361">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-361">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-362">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-362">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-363">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-363">The label by which the object is known.</span></span> <span data-ttu-id="fbf5e-364">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-364">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-365">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-365">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-366">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-366">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-367">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-367">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-368">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-368">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-369">Una matriz de cadenas que contienen las direcciones MAC para el puerto.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-369">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="fbf5e-370">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-370">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-371">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-371">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-372">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-372">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-373">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-373">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-374">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="fbf5e-374">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="fbf5e-375">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-375">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fbf5e-376">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-376">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="fbf5e-377"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-377"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-378"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-378"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-379"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-379"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-380"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-380"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-381"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-381"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-382"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-382"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-383"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-383"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-384"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-384"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-385"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-385"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-386"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-386"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-387"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-387"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-388"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-388"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-389"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-389"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-390"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-390"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-391"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-391"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-392"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-392"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-393"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-393"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-394"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-394"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-395"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="fbf5e-395"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="fbf5e-396">)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-396">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbf5e-397">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-397">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-398">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-398">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-399">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-399">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-400">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-400">The current statuses of the object.</span></span> <span data-ttu-id="fbf5e-401">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-401">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-402">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-402">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-403">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-403">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-404">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-404">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-405">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-405">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="fbf5e-406">Esta propiedad debe establecerse en **null** cuando la propiedad **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-406">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="fbf5e-407">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-407">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-408">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-408">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-409">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-409">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-410">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-410">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-411">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-411">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="fbf5e-412">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-412">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-413">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-413">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-414">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-414">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-415">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-415">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-416">Un valor de cadena que describe **LinkTechnology** cuando se establece en 1, (otro).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-416">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="fbf5e-417">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-417">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-418">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-418">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-419">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-419">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-420">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-420">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-421">El uso de esta propiedad está en desuso en lugar de la propiedad **portType** .</span><span class="sxs-lookup"><span data-stu-id="fbf5e-421">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="fbf5e-422">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-422">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-423">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-423">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-424">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-424">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-425">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-425">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-426">Describe el tipo de módulo, cuando **portType** está establecido en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-426">Describes the type of module, when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="fbf5e-427">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-427">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-428">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-428">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-429">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-429">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-430">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-430">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-431">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-431">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-432">La dirección de red que está codificada en un puerto.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-432">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="fbf5e-433">Esta dirección codificada se puede cambiar mediante una actualización de firmware o una configuración de software.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-433">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="fbf5e-434">Cuando se realiza este cambio, el campo debe actualizarse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-434">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="fbf5e-435">Esta propiedad debe ser **null** si no existe ninguna dirección codificada para el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-435">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="fbf5e-436">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-436">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-437">**NúmeroDePuerto**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-437">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-438">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-439">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-440">El número de puerto.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-440">The port number.</span></span> <span data-ttu-id="fbf5e-441">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-441">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-442">**PortType**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-442">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-443">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-443">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-444">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-444">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-445">Modo específico que está habilitado actualmente para el puerto.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-445">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="fbf5e-446">Cuando se establece en 1 (otro), la propiedad **OtherPortType** relacionada contiene una descripción de cadena del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-446">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="fbf5e-447">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-447">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="fbf5e-448"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-448"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-449"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-449"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-450"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 cobre 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-450"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-451"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-451"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-452"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-452"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-453"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-453"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-454"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-454"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-455"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-455"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-456"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-456"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-457"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 fibra 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-457"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-458"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-458"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-459"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-459"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-460"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-460"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-461"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-461"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-462"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-462"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-463"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-463"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-464"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-464"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-465"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-465"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-466"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-466"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-467"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-467"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-468"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-uevo** (111)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-468"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-469"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-469"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbf5e-470">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-470">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-471">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-471">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-472">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-472">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-473">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-473">The power management capabilities of the device.</span></span> <span data-ttu-id="fbf5e-474">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-474">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-475">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-475">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-476">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-476">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-477">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-477">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-478">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-478">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="fbf5e-479">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-479">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-480">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-480">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-481">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-481">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-482">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-482">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-483">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-483">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="fbf5e-484">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-484">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-485">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-485">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-486">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-486">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-487">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-487">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-488">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-488">Provides high level status information.</span></span> <span data-ttu-id="fbf5e-489">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-489">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="fbf5e-490">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-490">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="fbf5e-491">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-491">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="fbf5e-492"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-492"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-493"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-493"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-494"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-494"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-495"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-495"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-496"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-496"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-497"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="fbf5e-497"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="fbf5e-498">)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-498">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbf5e-499">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-499">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-500">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-500">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-501">Tipo de acceso: solo escritura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-501">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-502">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="fbf5e-502">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-503">Ancho de banda solicitado del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-503">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="fbf5e-504">El ancho de banda real se registra en la propiedad **Speed** .</span><span class="sxs-lookup"><span data-stu-id="fbf5e-504">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="fbf5e-505">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-505">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-506">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-506">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-507">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-507">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-508">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-508">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-509">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-509">The last requested or desired state for the element.</span></span> <span data-ttu-id="fbf5e-510">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-510">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-511">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-511">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-512">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-512">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-513">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-513">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-514">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="fbf5e-514">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-515">Ancho de banda del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-515">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="fbf5e-516">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-516">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-517">**Estado**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-517">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-518">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-518">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-519">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-519">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-520">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-520">The current status of the object.</span></span> <span data-ttu-id="fbf5e-521">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-521">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-522">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-522">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-523">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-523">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-524">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-524">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-525">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="fbf5e-525">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="fbf5e-526">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-526">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-527">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-527">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-528">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-528">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-529">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-529">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-530">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-530">The current state of the logical device.</span></span> <span data-ttu-id="fbf5e-531">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-531">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-532">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-532">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-533">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-533">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-534">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-534">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-535">Matriz de enteros que indica el Canal de fibra clases de servicio (COS) que se admiten.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-535">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="fbf5e-536">La propiedad **ActiveCOS** especifica los cos activos.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-536">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="fbf5e-537">Esta propiedad se hereda de **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-537">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="fbf5e-538"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-538"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-539"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-539"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-540"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-540"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-541"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-541"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-542"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-542"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-543"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-543"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-544"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-544"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-545"><span id="F_"></span><span id="f_"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-545"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbf5e-546">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-546">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-547">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-547">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-548">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-548">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-549">Matriz de enteros que indica los protocolos Canal de fibra FC-4 admitidos.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-549">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="fbf5e-550">Los protocolos que están activos y en ejecución se especifican mediante la propiedad **ActiveFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="fbf5e-550">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="fbf5e-551">Esta propiedad se hereda de **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-551">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="fbf5e-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-552"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-553"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-553"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-554"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-554"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-555"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP a través de FC** (5)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-555"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-556"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-556"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-557"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-557"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-558"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Patrón IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-558"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-559"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 esclavo** (18)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-559"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-560"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 del mismo nivel** (19)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-560"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-561"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 maestro** (21)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-561"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-562"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 esclavo** (22)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-562"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-563"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 del mismo nivel** (23)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-563"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-564"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-564"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-565"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unidad de control SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-565"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-566"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-566"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-567"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unidad de control FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-567"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-568"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Canal de fibra Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-568"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-569"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-569"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-570"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-570"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-571"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-571"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-572"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Control BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-572"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-573"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL FDDI** (81)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-573"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-574"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-574"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-575"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-575"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-576"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-576"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-577"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Proveedor único** (255)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-577"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="fbf5e-578">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-578">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-579">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-579">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-580">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-581">Calificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="fbf5e-581">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-582">La unidad de transmisión máxima (MTU) que se puede admitir, en bytes.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-582">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="fbf5e-583">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-583">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-584">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-584">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-585">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-585">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-586">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-586">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-587">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-587">The scoping system's creation class name.</span></span> <span data-ttu-id="fbf5e-588">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-588">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-589">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-589">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-590">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-590">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-591">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-591">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-592">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-592">The scoping system's name.</span></span> <span data-ttu-id="fbf5e-593">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-593">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-594">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-594">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-595">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-595">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-596">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-596">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-597">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-597">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="fbf5e-598">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-598">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-599">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-599">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-600">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-600">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-601">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-601">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-602">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-602">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="fbf5e-603">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-603">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-604">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-604">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-605">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-605">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-606">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-606">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-607">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-607">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="fbf5e-608">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-608">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="fbf5e-609">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-609">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fbf5e-610">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fbf5e-610">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-611">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fbf5e-611">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fbf5e-612">En algunas circunstancias, un puerto lógico puede identificarse como un puerto de front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-612">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="fbf5e-613">Un ejemplo de esta situación sería una matriz de almacenamiento que podría tener puertos back-end para comunicarse con las unidades de disco y los puertos front-end para comunicarse con los hosts.</span><span class="sxs-lookup"><span data-stu-id="fbf5e-613">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="fbf5e-614">Si no hay ninguna restricción sobre el uso del puerto, el valor debe establecerse en 4 (no restringido).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-614">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="fbf5e-615">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="fbf5e-615">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="fbf5e-616"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-616"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-617"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Solo front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-617"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-618"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Solo back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-618"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="fbf5e-619"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**No restringido** (4)</span><span class="sxs-lookup"><span data-stu-id="fbf5e-619"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fbf5e-620">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fbf5e-620">Requirements</span></span>



| <span data-ttu-id="fbf5e-621">Requisito</span><span class="sxs-lookup"><span data-stu-id="fbf5e-621">Requirement</span></span> | <span data-ttu-id="fbf5e-622">Value</span><span class="sxs-lookup"><span data-stu-id="fbf5e-622">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbf5e-623">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbf5e-623">Minimum supported client</span></span><br/> | <span data-ttu-id="fbf5e-624">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="fbf5e-624">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="fbf5e-625">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fbf5e-625">Minimum supported server</span></span><br/> | <span data-ttu-id="fbf5e-626">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="fbf5e-626">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fbf5e-627">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fbf5e-627">Namespace</span></span><br/>                | <span data-ttu-id="fbf5e-628">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="fbf5e-628">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="fbf5e-629">MOF</span><span class="sxs-lookup"><span data-stu-id="fbf5e-629">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fbf5e-630"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fbf5e-630"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fbf5e-631">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fbf5e-631">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fbf5e-632"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fbf5e-632"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

