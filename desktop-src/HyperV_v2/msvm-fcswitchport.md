---
description: Representa un puerto en el conmutador de Canal de fibra virtual.
ms.assetid: 6b4553b7-2717-4285-9e1a-e2ad22a60997
title: Clase Msvm_FcSwitchPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcSwitchPort
- Msvm_FcSwitchPort.SetPowerState
- Msvm_FcSwitchPort.EnableDevice
- Msvm_FcSwitchPort.OnlineDevice
- Msvm_FcSwitchPort.QuiesceDevice
- Msvm_FcSwitchPort.SaveProperties
- Msvm_FcSwitchPort.RestoreProperties
- Msvm_FcSwitchPort.InstanceID
- Msvm_FcSwitchPort.Caption
- Msvm_FcSwitchPort.Description
- Msvm_FcSwitchPort.ElementName
- Msvm_FcSwitchPort.InstallDate
- Msvm_FcSwitchPort.Name
- Msvm_FcSwitchPort.OperationalStatus
- Msvm_FcSwitchPort.StatusDescriptions
- Msvm_FcSwitchPort.Status
- Msvm_FcSwitchPort.HealthState
- Msvm_FcSwitchPort.CommunicationStatus
- Msvm_FcSwitchPort.DetailedStatus
- Msvm_FcSwitchPort.OperatingStatus
- Msvm_FcSwitchPort.PrimaryStatus
- Msvm_FcSwitchPort.EnabledState
- Msvm_FcSwitchPort.OtherEnabledState
- Msvm_FcSwitchPort.RequestedState
- Msvm_FcSwitchPort.EnabledDefault
- Msvm_FcSwitchPort.TimeOfLastStateChange
- Msvm_FcSwitchPort.AvailableRequestedStates
- Msvm_FcSwitchPort.TransitioningToState
- Msvm_FcSwitchPort.SystemCreationClassName
- Msvm_FcSwitchPort.SystemName
- Msvm_FcSwitchPort.CreationClassName
- Msvm_FcSwitchPort.DeviceID
- Msvm_FcSwitchPort.PowerManagementSupported
- Msvm_FcSwitchPort.PowerManagementCapabilities
- Msvm_FcSwitchPort.Availability
- Msvm_FcSwitchPort.StatusInfo
- Msvm_FcSwitchPort.LastErrorCode
- Msvm_FcSwitchPort.ErrorDescription
- Msvm_FcSwitchPort.ErrorCleared
- Msvm_FcSwitchPort.OtherIdentifyingInfo
- Msvm_FcSwitchPort.PowerOnHours
- Msvm_FcSwitchPort.TotalPowerOnHours
- Msvm_FcSwitchPort.IdentifyingDescriptions
- Msvm_FcSwitchPort.AdditionalAvailability
- Msvm_FcSwitchPort.MaxQuiesceTime
- Msvm_FcSwitchPort.Speed
- Msvm_FcSwitchPort.MaxSpeed
- Msvm_FcSwitchPort.RequestedSpeed
- Msvm_FcSwitchPort.UsageRestriction
- Msvm_FcSwitchPort.PortType
- Msvm_FcSwitchPort.OtherPortType
- Msvm_FcSwitchPort.OtherNetworkPortType
- Msvm_FcSwitchPort.PortNumber
- Msvm_FcSwitchPort.LinkTechnology
- Msvm_FcSwitchPort.OtherLinkTechnology
- Msvm_FcSwitchPort.PermanentAddress
- Msvm_FcSwitchPort.NetworkAddresses
- Msvm_FcSwitchPort.FullDuplex
- Msvm_FcSwitchPort.AutoSense
- Msvm_FcSwitchPort.SupportedMaximumTransmissionUnit
- Msvm_FcSwitchPort.ActiveMaximumTransmissionUnit
- Msvm_FcSwitchPort.SupportedCOS
- Msvm_FcSwitchPort.ActiveCOS
- Msvm_FcSwitchPort.SupportedFC4Types
- Msvm_FcSwitchPort.ActiveFC4Types
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 443ae1065b7c7a6a4bb1523a672e388cacb91667
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542478"
---
# <a name="msvm_fcswitchport-class"></a><span data-ttu-id="45cf8-103">MSVM \_ FcSwitchPort (clase)</span><span class="sxs-lookup"><span data-stu-id="45cf8-103">Msvm\_FcSwitchPort class</span></span>

> [!NOTE]
> <span data-ttu-id="45cf8-104">Este artículo contiene referencias al término esclavo, un término que Microsoft ya no usa.</span><span class="sxs-lookup"><span data-stu-id="45cf8-104">This article contains references to the term slave, a term that Microsoft no longer uses.</span></span> <span data-ttu-id="45cf8-105">Cuando se quite el término del software, se quitará también del artículo.</span><span class="sxs-lookup"><span data-stu-id="45cf8-105">When the term is removed from the software, we’ll remove it from this article.</span></span>

<span data-ttu-id="45cf8-106">Representa un puerto en el conmutador de Canal de fibra virtual.</span><span class="sxs-lookup"><span data-stu-id="45cf8-106">Represents a port on the virtual Fibre Channel switch.</span></span>

<span data-ttu-id="45cf8-107">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="45cf8-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="45cf8-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45cf8-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcSwitchPort : CIM_FCPort
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
};
```

## <a name="members"></a><span data-ttu-id="45cf8-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="45cf8-109">Members</span></span>

<span data-ttu-id="45cf8-110">La clase **MSVM \_ FcSwitchPort** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="45cf8-110">The **Msvm\_FcSwitchPort** class has these types of members:</span></span>

-   [<span data-ttu-id="45cf8-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="45cf8-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="45cf8-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="45cf8-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="45cf8-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="45cf8-113">Methods</span></span>

<span data-ttu-id="45cf8-114">La clase **MSVM \_ FcSwitchPort** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="45cf8-114">The **Msvm\_FcSwitchPort** class has these methods.</span></span>



| <span data-ttu-id="45cf8-115">Método</span><span class="sxs-lookup"><span data-stu-id="45cf8-115">Method</span></span>                                                             | <span data-ttu-id="45cf8-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="45cf8-116">Description</span></span>                              |
|:-------------------------------------------------------------------|:-----------------------------------------|
| <span data-ttu-id="45cf8-117">**EnableDevice**</span><span class="sxs-lookup"><span data-stu-id="45cf8-117">**EnableDevice**</span></span>                                                   | <span data-ttu-id="45cf8-118">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="45cf8-118">This method is not supported.</span></span><br/> |
| <span data-ttu-id="45cf8-119">**OnlineDevice**</span><span class="sxs-lookup"><span data-stu-id="45cf8-119">**OnlineDevice**</span></span>                                                   | <span data-ttu-id="45cf8-120">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="45cf8-120">This method is not supported.</span></span><br/> |
| <span data-ttu-id="45cf8-121">**QuiesceDevice**</span><span class="sxs-lookup"><span data-stu-id="45cf8-121">**QuiesceDevice**</span></span>                                                  | <span data-ttu-id="45cf8-122">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="45cf8-122">This method is not supported.</span></span><br/> |
| [<span data-ttu-id="45cf8-123">**RequestStateChange**</span><span class="sxs-lookup"><span data-stu-id="45cf8-123">**RequestStateChange**</span></span>](msvm-fcswitchport-requeststatechange.md) | <span data-ttu-id="45cf8-124">solicita un cambio de estado.</span><span class="sxs-lookup"><span data-stu-id="45cf8-124">requests a state change.</span></span><br/>      |
| [<span data-ttu-id="45cf8-125">**Reset**</span><span class="sxs-lookup"><span data-stu-id="45cf8-125">**Reset**</span></span>](msvm-fcswitchport-reset.md)                           | <span data-ttu-id="45cf8-126">Restablece el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="45cf8-126">Resets the virtual device.</span></span><br/>    |
| <span data-ttu-id="45cf8-127">**RestoreProperties**</span><span class="sxs-lookup"><span data-stu-id="45cf8-127">**RestoreProperties**</span></span>                                              | <span data-ttu-id="45cf8-128">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="45cf8-128">This method is not supported.</span></span><br/> |
| <span data-ttu-id="45cf8-129">**SaveProperties**</span><span class="sxs-lookup"><span data-stu-id="45cf8-129">**SaveProperties**</span></span>                                                 | <span data-ttu-id="45cf8-130">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="45cf8-130">This method is not supported.</span></span><br/> |
| <span data-ttu-id="45cf8-131">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="45cf8-131">**SetPowerState**</span></span>                                                  | <span data-ttu-id="45cf8-132">No se admite este método.</span><span class="sxs-lookup"><span data-stu-id="45cf8-132">This method is not supported.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="45cf8-133">Propiedades</span><span class="sxs-lookup"><span data-stu-id="45cf8-133">Properties</span></span>

<span data-ttu-id="45cf8-134">La clase **MSVM \_ FcSwitchPort** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="45cf8-134">The **Msvm\_FcSwitchPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="45cf8-135">**ActiveCOS**</span><span class="sxs-lookup"><span data-stu-id="45cf8-135">**ActiveCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-136">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-136">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-137">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-138">Matriz de enteros que indica las clases de servicio que están activas.</span><span class="sxs-lookup"><span data-stu-id="45cf8-138">An array of integers that indicates the classes of service that are active.</span></span> <span data-ttu-id="45cf8-139">Los co admitidos se especifican mediante la propiedad **SupportedCOS** .</span><span class="sxs-lookup"><span data-stu-id="45cf8-139">The supported COS are specified by the **SupportedCOS** property.</span></span> <span data-ttu-id="45cf8-140">Esta propiedad se hereda de **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="45cf8-140">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="45cf8-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="45cf8-141"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-142"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="45cf8-142"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-143"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="45cf8-143"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-144"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="45cf8-144"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-145"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="45cf8-145"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-146"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="45cf8-146"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-147"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="45cf8-147"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-148"><span id="F"></span><span id="f"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="45cf8-148"><span id="F"></span><span id="f"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45cf8-149">**ActiveFC4Types**</span><span class="sxs-lookup"><span data-stu-id="45cf8-149">**ActiveFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-150">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-150">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-152">Matriz de enteros que indica los protocolos Canal de fibra FC-4 que se están ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="45cf8-152">An array of integers that indicates the Fibre Channel FC-4 protocols currently running.</span></span> <span data-ttu-id="45cf8-153">La propiedad **SupportedFC4Types** especifica una lista de todos los protocolos admitidos.</span><span class="sxs-lookup"><span data-stu-id="45cf8-153">A list of all supported protocols is specified by the **SupportedFC4Types** property.</span></span> <span data-ttu-id="45cf8-154">Esta propiedad se hereda de **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="45cf8-154">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="45cf8-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="45cf8-155"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="45cf8-156"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="45cf8-157"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP a través de FC** (5)</span><span class="sxs-lookup"><span data-stu-id="45cf8-158"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="45cf8-159"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="45cf8-160"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Patrón IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="45cf8-161"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 esclavo** (18)</span><span class="sxs-lookup"><span data-stu-id="45cf8-162"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 del mismo nivel** (19)</span><span class="sxs-lookup"><span data-stu-id="45cf8-163"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 maestro** (21)</span><span class="sxs-lookup"><span data-stu-id="45cf8-164"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 esclavo** (22)</span><span class="sxs-lookup"><span data-stu-id="45cf8-165"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 del mismo nivel** (23)</span><span class="sxs-lookup"><span data-stu-id="45cf8-166"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="45cf8-167"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unidad de control SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="45cf8-168"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="45cf8-169"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unidad de control FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="45cf8-170"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Canal de fibra Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="45cf8-171"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="45cf8-172"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="45cf8-173"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="45cf8-174"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Control BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="45cf8-175"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL FDDI** (81)</span><span class="sxs-lookup"><span data-stu-id="45cf8-176"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="45cf8-177"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="45cf8-178"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="45cf8-179"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Proveedor único** (255)</span><span class="sxs-lookup"><span data-stu-id="45cf8-180"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45cf8-181">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="45cf8-181">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-182">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="45cf8-182">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-184">Calificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="45cf8-184">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-185">La unidad de transmisión máxima (MTU) activa o negociada que se puede admitir, en bytes.</span><span class="sxs-lookup"><span data-stu-id="45cf8-185">The active or negotiated maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="45cf8-186">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="45cf8-186">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-187">**AdditionalAvailability**</span><span class="sxs-lookup"><span data-stu-id="45cf8-187">**AdditionalAvailability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-188">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-188">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-189">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-189">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-190">Cualquier disponibilidad adicional y estado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45cf8-190">Any additional availability and status of the device.</span></span> <span data-ttu-id="45cf8-191">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="45cf8-191">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-192">**Percepción automática**</span><span class="sxs-lookup"><span data-stu-id="45cf8-192">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-193">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="45cf8-193">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-194">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-194">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-195">Indica si el puerto es capaz de determinar automáticamente la velocidad u otras características de comunicación de los medios de red conectados.</span><span class="sxs-lookup"><span data-stu-id="45cf8-195">Indicates whether the port is capable of automatically determining the speed or other communications characteristics of the attached network media.</span></span> <span data-ttu-id="45cf8-196">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="45cf8-196">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-197">**Disponibilidad**</span><span class="sxs-lookup"><span data-stu-id="45cf8-197">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-198">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-198">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-199">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-199">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-200">La disponibilidad y el estado principales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45cf8-200">The primary availability and status of the device.</span></span> <span data-ttu-id="45cf8-201">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="45cf8-201">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-202">**AvailableRequestedStates**</span><span class="sxs-lookup"><span data-stu-id="45cf8-202">**AvailableRequestedStates**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-203">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-203">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-204">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-205">Indica los valores posibles para el parámetro *RequestedState* del método **RequestStateChange** .</span><span class="sxs-lookup"><span data-stu-id="45cf8-205">Indicates the possible values for the *RequestedState* parameter of the **RequestStateChange** method.</span></span> <span data-ttu-id="45cf8-206">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="45cf8-206">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-207">**Caption**</span><span class="sxs-lookup"><span data-stu-id="45cf8-207">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-208">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-209">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-210">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="45cf8-210">A short description of the object.</span></span> <span data-ttu-id="45cf8-211">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="45cf8-211">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-212">**CommunicationStatus**</span><span class="sxs-lookup"><span data-stu-id="45cf8-212">**CommunicationStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-213">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-214">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-214">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-215">Indica la capacidad de la instrumentación de comunicarse con el elemento administrado subyacente.</span><span class="sxs-lookup"><span data-stu-id="45cf8-215">Indicates the ability of the instrumentation to communicate with the underlying managed element.</span></span> <span data-ttu-id="45cf8-216">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="45cf8-216">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="45cf8-217">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45cf8-217">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="45cf8-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="45cf8-218"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="45cf8-219"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Comunicación correcta** (2)</span><span class="sxs-lookup"><span data-stu-id="45cf8-220"><span id="Communication_OK"></span><span id="communication_ok"></span><span id="COMMUNICATION_OK"></span>**Communication OK** (2)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicación perdida** (3)</span><span class="sxs-lookup"><span data-stu-id="45cf8-221"><span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Lost Communication** (3)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sin contacto** (4)</span><span class="sxs-lookup"><span data-stu-id="45cf8-222"><span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**No Contact** (4)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="45cf8-223"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="45cf8-224"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="45cf8-225">)</span><span class="sxs-lookup"><span data-stu-id="45cf8-225">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45cf8-226">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="45cf8-226">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-227">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-228">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-229">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="45cf8-229">The scoping system's creation class name.</span></span> <span data-ttu-id="45cf8-230">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="45cf8-230">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-231">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="45cf8-231">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-232">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-233">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-234">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="45cf8-234">A description of the object.</span></span> <span data-ttu-id="45cf8-235">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="45cf8-235">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-236">**DetailedStatus**</span><span class="sxs-lookup"><span data-stu-id="45cf8-236">**DetailedStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-237">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-237">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-239">Complementa la propiedad **PrimaryStatus** con detalles de estado adicionales.</span><span class="sxs-lookup"><span data-stu-id="45cf8-239">Compliments the **PrimaryStatus** property with additional status detail.</span></span> <span data-ttu-id="45cf8-240">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="45cf8-240">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="45cf8-241">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45cf8-241">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="45cf8-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (0)</span><span class="sxs-lookup"><span data-stu-id="45cf8-242"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No hay información adicional** (1)</span><span class="sxs-lookup"><span data-stu-id="45cf8-243"><span id="No_Additional_Information"></span><span id="no_additional_information"></span><span id="NO_ADDITIONAL_INFORMATION"></span>**No Additional Information** (1)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>Con **estrés** (2)</span><span class="sxs-lookup"><span data-stu-id="45cf8-244"><span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>**Stressed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Error predictivo** (3)</span><span class="sxs-lookup"><span data-stu-id="45cf8-245"><span id="Predictive_Failure"></span><span id="predictive_failure"></span><span id="PREDICTIVE_FAILURE"></span>**Predictive Failure** (3)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Error no recuperable** (4)</span><span class="sxs-lookup"><span data-stu-id="45cf8-246"><span id="Non-Recoverable_Error"></span><span id="non-recoverable_error"></span><span id="NON-RECOVERABLE_ERROR"></span>**Non-Recoverable Error** (4)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Entidad auxiliar en error** (5)</span><span class="sxs-lookup"><span data-stu-id="45cf8-247"><span id="Supporting_Entity_in_Error"></span><span id="supporting_entity_in_error"></span><span id="SUPPORTING_ENTITY_IN_ERROR"></span>**Supporting Entity in Error** (5)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="45cf8-248"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="45cf8-249"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="45cf8-250">)</span><span class="sxs-lookup"><span data-stu-id="45cf8-250">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45cf8-251">**ID**</span><span class="sxs-lookup"><span data-stu-id="45cf8-251">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-252">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-252">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-253">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-254">Una dirección u otra información de identificación para asignar un nombre único al dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="45cf8-254">An address or other identifying information to uniquely name the logical device.</span></span> <span data-ttu-id="45cf8-255">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="45cf8-255">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-256">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="45cf8-256">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-257">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-258">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-259">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="45cf8-259">A display name for the object.</span></span> <span data-ttu-id="45cf8-260">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="45cf8-260">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-261">**EnabledDefault**</span><span class="sxs-lookup"><span data-stu-id="45cf8-261">**EnabledDefault**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-262">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-262">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-263">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-264">Configuración predeterminada o de inicio de un administrador para la propiedad **EnabledState** de un elemento.</span><span class="sxs-lookup"><span data-stu-id="45cf8-264">An administrator's default or startup configuration for the **EnabledState** property of an element.</span></span> <span data-ttu-id="45cf8-265">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 2 (habilitada).</span><span class="sxs-lookup"><span data-stu-id="45cf8-265">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 2 (Enabled).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-266">**EnabledState**</span><span class="sxs-lookup"><span data-stu-id="45cf8-266">**EnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-267">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-267">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-268">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-268">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-269">Estados habilitado y deshabilitado de un elemento.</span><span class="sxs-lookup"><span data-stu-id="45cf8-269">The enabled and disabled states of an element.</span></span> <span data-ttu-id="45cf8-270">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y será uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="45cf8-270">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it will be one of the following values.</span></span>



| <span data-ttu-id="45cf8-271">Value</span><span class="sxs-lookup"><span data-stu-id="45cf8-271">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="45cf8-272">Significado</span><span class="sxs-lookup"><span data-stu-id="45cf8-272">Meaning</span></span>                                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="45cf8-273"><dt>**Desconocido**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="45cf8-273"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="45cf8-274">No se pudo determinar el estado del elemento.</span><span class="sxs-lookup"><span data-stu-id="45cf8-274">The state of the element could not be determined.</span></span><br/>                                                                                                                                                    |
| <span id="Other"></span><span id="other"></span><span id="OTHER"></span><dl> <span data-ttu-id="45cf8-275"><dt>**Otro**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="45cf8-275"><dt>**Other**</dt> <dt>1</dt></span></span> </dl>                                                         |                                                                                                                                                                                                                 |
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <span data-ttu-id="45cf8-276"><dt>**Habilitado**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="45cf8-276"><dt>**Enabled**</dt> <dt>2</dt></span></span> </dl>                                                 | <span data-ttu-id="45cf8-277">El elemento se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="45cf8-277">The element is running.</span></span><br/>                                                                                                                                                                              |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <span data-ttu-id="45cf8-278"><dt>**Deshabilitado**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="45cf8-278"><dt>**Disabled**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="45cf8-279">El elemento está desactivado.</span><span class="sxs-lookup"><span data-stu-id="45cf8-279">The element is turned off.</span></span><br/>                                                                                                                                                                           |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <span data-ttu-id="45cf8-280"><dt>**Cerrando**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="45cf8-280"><dt>**Shutting Down**</dt> <dt>4</dt></span></span> </dl>                         | <span data-ttu-id="45cf8-281">El elemento está en el proceso de pasar a un Estado deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="45cf8-281">The element is in the process of going to a Disabled state.</span></span><br/>                                                                                                                                          |
| <span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span><dl> <span data-ttu-id="45cf8-282"><dt>**No aplicable**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="45cf8-282"><dt>**Not Applicable**</dt> <dt>5</dt></span></span> </dl>                     | <span data-ttu-id="45cf8-283">El elemento no admite la habilitación o deshabilitación.</span><span class="sxs-lookup"><span data-stu-id="45cf8-283">The element does not support being enabled or disabled.</span></span><br/>                                                                                                                                              |
| <span id="Enabled_but_Offline"></span><span id="enabled_but_offline"></span><span id="ENABLED_BUT_OFFLINE"></span><dl> <span data-ttu-id="45cf8-284"><dt>**Habilitada pero sin conexión**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="45cf8-284"><dt>**Enabled but Offline**</dt> <dt>6</dt></span></span> </dl> | <span data-ttu-id="45cf8-285">Es posible que el elemento esté completando comandos y quitará todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="45cf8-285">The element might be completing commands, and it will drop any new requests.</span></span><br/>                                                                                                                         |
| <span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span><dl> <span data-ttu-id="45cf8-286"><dt>**En la prueba**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="45cf8-286"><dt>**In Test**</dt> <dt>7</dt></span></span> </dl>                                                 | <span data-ttu-id="45cf8-287">El elemento está en un estado de prueba.</span><span class="sxs-lookup"><span data-stu-id="45cf8-287">The element is in a test state.</span></span><br/>                                                                                                                                                                      |
| <span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span><dl> <span data-ttu-id="45cf8-288"><dt>**Aplazado**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="45cf8-288"><dt>**Deferred**</dt> <dt>8</dt></span></span> </dl>                                             | <span data-ttu-id="45cf8-289">Es posible que el elemento esté completando los comandos, pero pondrá en cola todas las solicitudes nuevas.</span><span class="sxs-lookup"><span data-stu-id="45cf8-289">The element might be completing commands, but it will queue any new requests.</span></span><br/>                                                                                                                        |
| <span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span><dl> <span data-ttu-id="45cf8-290">Modo <dt>**inactivo**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="45cf8-290"><dt>**Quiesce**</dt> <dt>9</dt></span></span> </dl>                                                 | <span data-ttu-id="45cf8-291">El elemento está habilitado pero en modo restringido.</span><span class="sxs-lookup"><span data-stu-id="45cf8-291">The element is enabled but in a restricted mode.</span></span> <span data-ttu-id="45cf8-292">El comportamiento del elemento es similar al estado habilitado (2), pero solo procesa un conjunto restringido de comandos.</span><span class="sxs-lookup"><span data-stu-id="45cf8-292">The behavior of the element is similar to the Enabled state (2), but it processes only a restricted set of commands.</span></span> <span data-ttu-id="45cf8-293">Todas las demás solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="45cf8-293">All other requests are queued.</span></span><br/> |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <span data-ttu-id="45cf8-294"><dt>**Inicio**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="45cf8-294"><dt>**Starting**</dt> <dt>10</dt></span></span> </dl>                                            | <span data-ttu-id="45cf8-295">El elemento está en proceso de pasar a un estado habilitado (2).</span><span class="sxs-lookup"><span data-stu-id="45cf8-295">The element is in the process of going to an Enabled state (2).</span></span> <span data-ttu-id="45cf8-296">Las nuevas solicitudes se ponen en cola.</span><span class="sxs-lookup"><span data-stu-id="45cf8-296">New requests are queued.</span></span><br/>                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="45cf8-297">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="45cf8-297">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-298">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="45cf8-298">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-299">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-299">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-300">Indica si el error comunicado en **LastErrorCode** se ha borrado.</span><span class="sxs-lookup"><span data-stu-id="45cf8-300">Indicates whether the error reported in **LastErrorCode** is now cleared.</span></span> <span data-ttu-id="45cf8-301">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="45cf8-301">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-302">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="45cf8-302">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-303">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-303">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-304">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-304">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-305">Una cadena que proporciona más información sobre el error registrado en **LastErrorCode** e información acerca de las acciones correctivas que se pueden realizar.</span><span class="sxs-lookup"><span data-stu-id="45cf8-305">A string that provides more information about the error recorded in **LastErrorCode** and information about any corrective actions that can be taken.</span></span> <span data-ttu-id="45cf8-306">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="45cf8-306">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-307">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="45cf8-307">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-308">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="45cf8-308">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-309">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-309">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-310">Indica si el puerto está funcionando en modo dúplex completo.</span><span class="sxs-lookup"><span data-stu-id="45cf8-310">Indicates whether the port is operating in full duplex mode.</span></span> <span data-ttu-id="45cf8-311">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="45cf8-311">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-312">**HealthState**</span><span class="sxs-lookup"><span data-stu-id="45cf8-312">**HealthState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-313">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-313">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-314">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-314">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-315">Estado actual del elemento.</span><span class="sxs-lookup"><span data-stu-id="45cf8-315">The current health of the element.</span></span> <span data-ttu-id="45cf8-316">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45cf8-316">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-317">**IdentifyingDescriptions**</span><span class="sxs-lookup"><span data-stu-id="45cf8-317">**IdentifyingDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-318">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="45cf8-318">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-319">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-319">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-320">Matriz de cadenas de forma libre que proporcionan explicaciones y detalles detrás de las entradas de la matriz de propiedades **OtherIdentifyingInfo** .</span><span class="sxs-lookup"><span data-stu-id="45cf8-320">An array of free-form strings that provide explanations and details behind the entries in the **OtherIdentifyingInfo** property array.</span></span> <span data-ttu-id="45cf8-321">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="45cf8-321">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-322">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="45cf8-322">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-323">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="45cf8-323">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-324">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-325">Fecha y hora en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="45cf8-325">The date and time when the object was installed.</span></span> <span data-ttu-id="45cf8-326">Esta propiedad no necesita un valor para indicar que el objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="45cf8-326">This property does not need a value to indicate that the object is installed.</span></span> <span data-ttu-id="45cf8-327">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45cf8-327">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-328">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="45cf8-328">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-329">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-329">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-330">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-330">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-331">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="45cf8-331">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-332">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="45cf8-332">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="45cf8-333">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="45cf8-333">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-334">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="45cf8-334">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-335">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="45cf8-335">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-336">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-336">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-337">Último código de error indicado por el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="45cf8-337">The last error code reported by the logical device.</span></span> <span data-ttu-id="45cf8-338">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="45cf8-338">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-339">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="45cf8-339">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-340">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-340">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-341">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-341">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-342">Especifica el tipo de tecnología de vínculo para el puerto.</span><span class="sxs-lookup"><span data-stu-id="45cf8-342">Specifies the type of link technology for the port.</span></span> <span data-ttu-id="45cf8-343">Cuando se establece en 1 (otro), la propiedad **OtherLinkTechnology** contiene una descripción de cadena del tipo de vínculo.</span><span class="sxs-lookup"><span data-stu-id="45cf8-343">When set to 1 (Other), the **OtherLinkTechnology** property contains a string description of the type of link.</span></span> <span data-ttu-id="45cf8-344">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="45cf8-344">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

<dl> <dt>

<span data-ttu-id="45cf8-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="45cf8-345"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="45cf8-346"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-347"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="45cf8-347"><span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>**Ethernet** (2)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-348"><span id="IB"></span><span id="ib"></span>**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="45cf8-348"><span id="IB"></span><span id="ib"></span>**IB** (3)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-349"><span id="FC"></span><span id="fc"></span>**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="45cf8-349"><span id="FC"></span><span id="fc"></span>**FC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-350"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="45cf8-350"><span id="FDDI"></span><span id="fddi"></span>**FDDI** (5)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-351"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="45cf8-351"><span id="ATM"></span><span id="atm"></span>**ATM** (6)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-352"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="45cf8-352"><span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>**Token Ring** (7)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-353"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="45cf8-353"><span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>**Frame Relay** (8)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-354"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrarrojos** (9)</span><span class="sxs-lookup"><span data-stu-id="45cf8-354"><span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>**Infrared** (9)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-355"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="45cf8-355"><span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>**BlueTooth** (10)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-356"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**LAN inalámbrica** (11)</span><span class="sxs-lookup"><span data-stu-id="45cf8-356"><span id="Wireless_LAN_"></span><span id="wireless_lan_"></span><span id="WIRELESS_LAN_"></span>**Wireless LAN** (11 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45cf8-357">**MaxQuiesceTime**</span><span class="sxs-lookup"><span data-stu-id="45cf8-357">**MaxQuiesceTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-358">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="45cf8-358">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-359">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-359">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-360">Esta propiedad está en desuso.</span><span class="sxs-lookup"><span data-stu-id="45cf8-360">This property has been deprecated.</span></span> <span data-ttu-id="45cf8-361">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="45cf8-361">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-362">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="45cf8-362">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-363">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="45cf8-363">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-364">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-364">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-365">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="45cf8-365">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-366">Ancho de banda máximo del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="45cf8-366">The maximum bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="45cf8-367">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="45cf8-367">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-368">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="45cf8-368">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-369">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-369">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-370">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-370">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-371">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="45cf8-371">The label by which the object is known.</span></span> <span data-ttu-id="45cf8-372">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45cf8-372">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-373">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="45cf8-373">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-374">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="45cf8-374">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-375">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-375">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-376">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="45cf8-376">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-377">Una matriz de cadenas que contienen las direcciones MAC para el puerto.</span><span class="sxs-lookup"><span data-stu-id="45cf8-377">An array of strings that contain the MAC addresses for the port.</span></span> <span data-ttu-id="45cf8-378">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="45cf8-378">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-379">**OperatingStatus**</span><span class="sxs-lookup"><span data-stu-id="45cf8-379">**OperatingStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-380">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-380">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-381">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-381">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-382">Proporciona información sobre el estado actual de la condición operativa del elemento y se puede usar para proporcionar más detalles con respecto al valor de la propiedad **EnabledState** .</span><span class="sxs-lookup"><span data-stu-id="45cf8-382">Provides current status information for the operational condition of the element and can be used for providing more detail with respect to the value of the **EnabledState** property.</span></span> <span data-ttu-id="45cf8-383">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="45cf8-383">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="45cf8-384">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45cf8-384">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="45cf8-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="45cf8-385"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-386"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**No disponible** (1)</span><span class="sxs-lookup"><span data-stu-id="45cf8-386"><span id="Not_Available"></span><span id="not_available"></span><span id="NOT_AVAILABLE"></span>**Not Available** (1)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-387"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Mantenimiento** (2)</span><span class="sxs-lookup"><span data-stu-id="45cf8-387"><span id="Servicing"></span><span id="servicing"></span><span id="SERVICING"></span>**Servicing** (2)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-388"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Inicio** (3)</span><span class="sxs-lookup"><span data-stu-id="45cf8-388"><span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>**Starting** (3)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-389"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Detención** (4)</span><span class="sxs-lookup"><span data-stu-id="45cf8-389"><span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>**Stopping** (4)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-390"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Detenido** (5)</span><span class="sxs-lookup"><span data-stu-id="45cf8-390"><span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Stopped** (5)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-391"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Anulado** (6)</span><span class="sxs-lookup"><span data-stu-id="45cf8-391"><span id="Aborted"></span><span id="aborted"></span><span id="ABORTED"></span>**Aborted** (6)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-392"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Inactivo** (7)</span><span class="sxs-lookup"><span data-stu-id="45cf8-392"><span id="Dormant"></span><span id="dormant"></span><span id="DORMANT"></span>**Dormant** (7)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-393"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completado** (8)</span><span class="sxs-lookup"><span data-stu-id="45cf8-393"><span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span>**Completed** (8)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-394"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migración** (9)</span><span class="sxs-lookup"><span data-stu-id="45cf8-394"><span id="Migrating"></span><span id="migrating"></span><span id="MIGRATING"></span>**Migrating** (9)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-395"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span><span class="sxs-lookup"><span data-stu-id="45cf8-395"><span id="Emigrating"></span><span id="emigrating"></span><span id="EMIGRATING"></span>**Emigrating** (10)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-396"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Migración** (11)</span><span class="sxs-lookup"><span data-stu-id="45cf8-396"><span id="Immigrating"></span><span id="immigrating"></span><span id="IMMIGRATING"></span>**Immigrating** (11)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-397"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Instantánea** (12)</span><span class="sxs-lookup"><span data-stu-id="45cf8-397"><span id="Snapshotting"></span><span id="snapshotting"></span><span id="SNAPSHOTTING"></span>**Snapshotting** (12)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-398"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Cerrando** (13)</span><span class="sxs-lookup"><span data-stu-id="45cf8-398"><span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span>**Shutting Down** (13)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-399"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**En pruebas** (14)</span><span class="sxs-lookup"><span data-stu-id="45cf8-399"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (14)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-400"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transición** (15)</span><span class="sxs-lookup"><span data-stu-id="45cf8-400"><span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transitioning** (15)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-401"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**En servicio** (16)</span><span class="sxs-lookup"><span data-stu-id="45cf8-401"><span id="In_Service"></span><span id="in_service"></span><span id="IN_SERVICE"></span>**In Service** (16)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-402"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="45cf8-402"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-403"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="45cf8-403"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="45cf8-404">)</span><span class="sxs-lookup"><span data-stu-id="45cf8-404">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45cf8-405">**OperationalStatus**</span><span class="sxs-lookup"><span data-stu-id="45cf8-405">**OperationalStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-406">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-406">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-407">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-407">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-408">Estados actuales del objeto.</span><span class="sxs-lookup"><span data-stu-id="45cf8-408">The current statuses of the object.</span></span> <span data-ttu-id="45cf8-409">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45cf8-409">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-410">**OtherEnabledState**</span><span class="sxs-lookup"><span data-stu-id="45cf8-410">**OtherEnabledState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-411">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-411">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-412">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-412">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-413">Cadena que describe el estado habilitado o deshabilitado del elemento cuando la propiedad **EnabledState** está establecida en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="45cf8-413">A string that describes the enabled or disabled state of the element when the **EnabledState** property is set to 1 (Other).</span></span> <span data-ttu-id="45cf8-414">Esta propiedad debe establecerse en **null** cuando la propiedad **EnabledState** es cualquier valor distinto de 1.</span><span class="sxs-lookup"><span data-stu-id="45cf8-414">This property must be set to **Null** when the **EnabledState** property is any value other than 1.</span></span> <span data-ttu-id="45cf8-415">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="45cf8-415">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-416">**OtherIdentifyingInfo**</span><span class="sxs-lookup"><span data-stu-id="45cf8-416">**OtherIdentifyingInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-417">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="45cf8-417">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-418">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-418">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-419">Cualquier dato adicional, más allá de la información del ID. de dispositivo, que se puede usar para identificar un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="45cf8-419">Any additional data, beyond device ID information, that could be used to identify a logical device.</span></span> <span data-ttu-id="45cf8-420">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="45cf8-420">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-421">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="45cf8-421">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-422">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-422">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-423">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-423">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-424">Un valor de cadena que describe **LinkTechnology** cuando se establece en 1, (otro).</span><span class="sxs-lookup"><span data-stu-id="45cf8-424">A string value that describes **LinkTechnology** when it is set to 1, (Other).</span></span> <span data-ttu-id="45cf8-425">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="45cf8-425">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-426">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="45cf8-426">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-427">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-428">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-428">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-429">El uso de esta propiedad está en desuso en lugar de la propiedad **portType** .</span><span class="sxs-lookup"><span data-stu-id="45cf8-429">The use of this property is deprecated in lieu of the **PortType** property.</span></span> <span data-ttu-id="45cf8-430">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="45cf8-430">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-431">**OtherPortType**</span><span class="sxs-lookup"><span data-stu-id="45cf8-431">**OtherPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-432">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-432">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-433">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-433">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-434">Describe el tipo de módulo cuando **portType** está establecido en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="45cf8-434">Describes the type of module when **PortType** is set to 1 (Other).</span></span> <span data-ttu-id="45cf8-435">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="45cf8-435">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-436">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="45cf8-436">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-437">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-437">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-438">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-438">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-439">Calificadores: **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="45cf8-439">Qualifiers: **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-440">La dirección de red que está codificada en un puerto.</span><span class="sxs-lookup"><span data-stu-id="45cf8-440">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="45cf8-441">Esta dirección codificada se puede cambiar mediante una actualización de firmware o una configuración de software.</span><span class="sxs-lookup"><span data-stu-id="45cf8-441">This hardcoded address can be changed by using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="45cf8-442">Cuando se realiza este cambio, el campo debe actualizarse al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="45cf8-442">When this change is made, the field should be updated at the same time.</span></span> <span data-ttu-id="45cf8-443">Esta propiedad debe ser **null** si no existe ninguna dirección codificada para el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="45cf8-443">This property should be **Null** if no hardcoded address exists for the network adapter.</span></span> <span data-ttu-id="45cf8-444">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="45cf8-444">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-445">**NúmeroDePuerto**</span><span class="sxs-lookup"><span data-stu-id="45cf8-445">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-446">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-446">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-447">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-447">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-448">El número de puerto.</span><span class="sxs-lookup"><span data-stu-id="45cf8-448">The port number.</span></span> <span data-ttu-id="45cf8-449">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="45cf8-449">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-450">**PortType**</span><span class="sxs-lookup"><span data-stu-id="45cf8-450">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-451">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-451">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-452">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-452">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-453">Modo específico que está habilitado actualmente para el puerto.</span><span class="sxs-lookup"><span data-stu-id="45cf8-453">The specific mode that is currently enabled for the port.</span></span> <span data-ttu-id="45cf8-454">Cuando se establece en 1 (otro), la propiedad **OtherPortType** relacionada contiene una descripción de cadena del tipo de puerto.</span><span class="sxs-lookup"><span data-stu-id="45cf8-454">When set to 1 (Other), the related **OtherPortType** property contains a string description of the type of port.</span></span> <span data-ttu-id="45cf8-455">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="45cf8-455">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="45cf8-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="45cf8-456"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="45cf8-457"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-458"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 cobre 10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="45cf8-458"><span id="__50_Copper___________________10BaseT"></span><span id="__50_copper___________________10baset"></span><span id="__50_COPPER___________________10BASET"></span>**//50 Copper 10BaseT** (50)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-459"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="45cf8-459"><span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>**10-100BaseT** (51)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-460"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="45cf8-460"><span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>**100BaseT** (52)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-461"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span><span class="sxs-lookup"><span data-stu-id="45cf8-461"><span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>**1000BaseT** (53)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-462"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="45cf8-462"><span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>**2500BaseT** (54)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-463"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="45cf8-463"><span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>**10GBaseT** (55)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-464"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="45cf8-464"><span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>**10GBase-CX4** (56)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-465"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 fibra 100Base-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="45cf8-465"><span id="__100_Fibre___________________100Base-FX"></span><span id="__100_fibre___________________100base-fx"></span><span id="__100_FIBRE___________________100BASE-FX"></span>**//100 Fibre 100Base-FX** (100)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-466"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="45cf8-466"><span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>**100Base-SX** (101)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-467"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="45cf8-467"><span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>**1000Base-SX** (102)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-468"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="45cf8-468"><span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>**1000Base-LX** (103)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-469"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="45cf8-469"><span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>**1000Base-CX** (104)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-470"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBASE-SR** (105)</span><span class="sxs-lookup"><span data-stu-id="45cf8-470"><span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>**10GBase-SR** (105)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-471"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="45cf8-471"><span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>**10GBase-SW** (106)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-472"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="45cf8-472"><span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>**10GBase-LX4** (107)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-473"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="45cf8-473"><span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>**10GBase-LR** (108)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-474"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="45cf8-474"><span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>**10GBase-LW** (109)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-475"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="45cf8-475"><span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>**10GBase-ER** (110)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-476"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBASE-uevo** (111)</span><span class="sxs-lookup"><span data-stu-id="45cf8-476"><span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>**10GBase-EW** (111)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="45cf8-477"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (16000..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45cf8-478">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="45cf8-478">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-479">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-479">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-480">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-480">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-481">Las capacidades de administración de energía del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45cf8-481">The power management capabilities of the device.</span></span> <span data-ttu-id="45cf8-482">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="45cf8-482">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-483">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="45cf8-483">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-484">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="45cf8-484">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-485">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-485">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-486">Indica si el dispositivo puede administrarse con energía.</span><span class="sxs-lookup"><span data-stu-id="45cf8-486">Indicates whether the device can be power managed.</span></span> <span data-ttu-id="45cf8-487">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="45cf8-487">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-488">**PowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="45cf8-488">**PowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-489">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="45cf8-489">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-490">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-490">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-491">El número de horas consecutivas en que se ha encendido este dispositivo desde el último ciclo de energía.</span><span class="sxs-lookup"><span data-stu-id="45cf8-491">The number of consecutive hours that this device has been powered on since its last power cycle.</span></span> <span data-ttu-id="45cf8-492">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="45cf8-492">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-493">**PrimaryStatus**</span><span class="sxs-lookup"><span data-stu-id="45cf8-493">**PrimaryStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-494">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-494">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-495">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-496">Proporciona información de estado de alto nivel.</span><span class="sxs-lookup"><span data-stu-id="45cf8-496">Provides high level status information.</span></span> <span data-ttu-id="45cf8-497">Esta propiedad debe utilizarse junto con la propiedad **DetailedStatus** para proporcionar el estado de mantenimiento detallado y de alto nivel del elemento y sus subcomponentes.</span><span class="sxs-lookup"><span data-stu-id="45cf8-497">This property should be used in conjunction with the **DetailedStatus** property to provide high level and detailed health status of the element and its subcomponents.</span></span> <span data-ttu-id="45cf8-498">Un valor **null** indica que esta propiedad no está implementada.</span><span class="sxs-lookup"><span data-stu-id="45cf8-498">A **Null** value indicates that this property is not implemented.</span></span> <span data-ttu-id="45cf8-499">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45cf8-499">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

<dl> <dt>

<span data-ttu-id="45cf8-500"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="45cf8-500"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-501"><span id="OK"></span><span id="ok"></span>**Aceptar** (1)</span><span class="sxs-lookup"><span data-stu-id="45cf8-501"><span id="OK"></span><span id="ok"></span>**OK** (1)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-502"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (2)</span><span class="sxs-lookup"><span data-stu-id="45cf8-502"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (2)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-503"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span><span class="sxs-lookup"><span data-stu-id="45cf8-503"><span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Error** (3)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-504"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="45cf8-504"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-505"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000...</span><span class="sxs-lookup"><span data-stu-id="45cf8-505"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..</span></span> <span data-ttu-id="45cf8-506">)</span><span class="sxs-lookup"><span data-stu-id="45cf8-506">)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45cf8-507">**RequestedSpeed**</span><span class="sxs-lookup"><span data-stu-id="45cf8-507">**RequestedSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-508">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="45cf8-508">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-509">Tipo de acceso: solo escritura</span><span class="sxs-lookup"><span data-stu-id="45cf8-509">Access type: Write-only</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-510">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="45cf8-510">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-511">Ancho de banda solicitado del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="45cf8-511">The requested bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="45cf8-512">El ancho de banda real se registra en la propiedad **Speed** .</span><span class="sxs-lookup"><span data-stu-id="45cf8-512">The actual bandwidth is reported in the **Speed** property.</span></span> <span data-ttu-id="45cf8-513">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="45cf8-513">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-514">**RequestedState**</span><span class="sxs-lookup"><span data-stu-id="45cf8-514">**RequestedState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-515">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-515">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-516">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-517">Último estado solicitado o deseado del elemento.</span><span class="sxs-lookup"><span data-stu-id="45cf8-517">The last requested or desired state for the element.</span></span> <span data-ttu-id="45cf8-518">Esta propiedad se hereda de [**\_ EnabledLogicalElement CIM**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en 12 (no aplicable).</span><span class="sxs-lookup"><span data-stu-id="45cf8-518">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to 12 (Not Applicable).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-519">**Velocidad**</span><span class="sxs-lookup"><span data-stu-id="45cf8-519">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-520">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="45cf8-520">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-521">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-521">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-522">Calificadores: **unidades** ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="45cf8-522">Qualifiers: **Units** ("Bits per Second")</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-523">Ancho de banda del puerto, en bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="45cf8-523">The bandwidth of the port, in bits per second.</span></span> <span data-ttu-id="45cf8-524">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="45cf8-524">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-525">**Estado**</span><span class="sxs-lookup"><span data-stu-id="45cf8-525">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-526">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-526">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-527">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-527">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-528">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="45cf8-528">The current status of the object.</span></span> <span data-ttu-id="45cf8-529">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="45cf8-529">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-530">**StatusDescriptions**</span><span class="sxs-lookup"><span data-stu-id="45cf8-530">**StatusDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-531">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="45cf8-531">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-532">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-532">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-533">Cadenas que describen los distintos valores de la matriz **OperationalStatus** .</span><span class="sxs-lookup"><span data-stu-id="45cf8-533">Strings that describe the various **OperationalStatus** array values.</span></span> <span data-ttu-id="45cf8-534">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span><span class="sxs-lookup"><span data-stu-id="45cf8-534">This property is inherited from [**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-535">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="45cf8-535">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-536">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-536">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-537">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-537">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-538">Estado actual del dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="45cf8-538">The current state of the logical device.</span></span> <span data-ttu-id="45cf8-539">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="45cf8-539">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-540">**SupportedCOS**</span><span class="sxs-lookup"><span data-stu-id="45cf8-540">**SupportedCOS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-541">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-541">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-542">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-542">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-543">Matriz de enteros que indica el Canal de fibra clases de servicio (COS) que se admiten.</span><span class="sxs-lookup"><span data-stu-id="45cf8-543">An array of integers that indicates the Fibre Channel classes of service (COS) that are supported.</span></span> <span data-ttu-id="45cf8-544">La propiedad **ActiveCOS** especifica los cos activos.</span><span class="sxs-lookup"><span data-stu-id="45cf8-544">The active COS are specified by the **ActiveCOS** property.</span></span> <span data-ttu-id="45cf8-545">Esta propiedad se hereda de **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="45cf8-545">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="45cf8-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="45cf8-546"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-547"><span id="1"></span>**1** (1)</span><span class="sxs-lookup"><span data-stu-id="45cf8-547"><span id="1"></span>**1** (1)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-548"><span id="2"></span>**2** (2)</span><span class="sxs-lookup"><span data-stu-id="45cf8-548"><span id="2"></span>**2** (2)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-549"><span id="3"></span>**3** (3)</span><span class="sxs-lookup"><span data-stu-id="45cf8-549"><span id="3"></span>**3** (3)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-550"><span id="4"></span>**4** (4)</span><span class="sxs-lookup"><span data-stu-id="45cf8-550"><span id="4"></span>**4** (4)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-551"><span id="5"></span>**5** (5)</span><span class="sxs-lookup"><span data-stu-id="45cf8-551"><span id="5"></span>**5** (5)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-552"><span id="6"></span>**6** (6)</span><span class="sxs-lookup"><span data-stu-id="45cf8-552"><span id="6"></span>**6** (6)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-553"><span id="F_"></span><span id="f_"></span>**F** (7)</span><span class="sxs-lookup"><span data-stu-id="45cf8-553"><span id="F_"></span><span id="f_"></span>**F** (7 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45cf8-554">**SupportedFC4Types**</span><span class="sxs-lookup"><span data-stu-id="45cf8-554">**SupportedFC4Types**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-555">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-555">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-556">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-556">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-557">Matriz de enteros que indica los protocolos Canal de fibra FC-4 admitidos.</span><span class="sxs-lookup"><span data-stu-id="45cf8-557">An array of integers that indicates the Fibre Channel FC-4 protocols supported.</span></span> <span data-ttu-id="45cf8-558">Los protocolos que están activos y en ejecución se especifican mediante la propiedad **ActiveFC4Types** .</span><span class="sxs-lookup"><span data-stu-id="45cf8-558">The protocols that are active and running are specified by the **ActiveFC4Types** property.</span></span> <span data-ttu-id="45cf8-559">Esta propiedad se hereda de **\_ FCPort CIM**.</span><span class="sxs-lookup"><span data-stu-id="45cf8-559">This property is inherited from **CIM\_FCPort**.</span></span>

<dl> <dt>

<span data-ttu-id="45cf8-560"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="45cf8-560"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-561"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="45cf8-561"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-562"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802-2 LLC** (4)</span><span class="sxs-lookup"><span data-stu-id="45cf8-562"><span id="ISO_IEC_8802_-_2_LLC"></span><span id="iso_iec_8802_-_2_llc"></span>**ISO/IEC 8802 - 2 LLC** (4)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-563"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP a través de FC** (5)</span><span class="sxs-lookup"><span data-stu-id="45cf8-563"><span id="IP_over_FC"></span><span id="ip_over_fc"></span><span id="IP_OVER_FC"></span>**IP over FC** (5)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-564"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI-FCP** (8)</span><span class="sxs-lookup"><span data-stu-id="45cf8-564"><span id="SCSI_-_FCP"></span><span id="scsi_-_fcp"></span>**SCSI - FCP** (8)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-565"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI-GPP** (9)</span><span class="sxs-lookup"><span data-stu-id="45cf8-565"><span id="SCSI_-_GPP"></span><span id="scsi_-_gpp"></span>**SCSI - GPP** (9)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-566"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**Patrón IPI-3** (17)</span><span class="sxs-lookup"><span data-stu-id="45cf8-566"><span id="IPI_-_3_Master"></span><span id="ipi_-_3_master"></span><span id="IPI_-_3_MASTER"></span>**IPI - 3 Master** (17)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-567"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI-3 esclavo** (18)</span><span class="sxs-lookup"><span data-stu-id="45cf8-567"><span id="IPI_-_3_Slave"></span><span id="ipi_-_3_slave"></span><span id="IPI_-_3_SLAVE"></span>**IPI - 3 Slave** (18)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-568"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI-3 del mismo nivel** (19)</span><span class="sxs-lookup"><span data-stu-id="45cf8-568"><span id="IPI_-_3_Peer"></span><span id="ipi_-_3_peer"></span><span id="IPI_-_3_PEER"></span>**IPI - 3 Peer** (19)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-569"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI-3 maestro** (21)</span><span class="sxs-lookup"><span data-stu-id="45cf8-569"><span id="CP_IPI_-_3_Master"></span><span id="cp_ipi_-_3_master"></span><span id="CP_IPI_-_3_MASTER"></span>**CP IPI - 3 Master** (21)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-570"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI-3 esclavo** (22)</span><span class="sxs-lookup"><span data-stu-id="45cf8-570"><span id="CP_IPI_-_3_Slave"></span><span id="cp_ipi_-_3_slave"></span><span id="CP_IPI_-_3_SLAVE"></span>**CP IPI - 3 Slave** (22)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-571"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI-3 del mismo nivel** (23)</span><span class="sxs-lookup"><span data-stu-id="45cf8-571"><span id="CP_IPI_-_3_Peer"></span><span id="cp_ipi_-_3_peer"></span><span id="CP_IPI_-_3_PEER"></span>**CP IPI - 3 Peer** (23)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-572"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**Canal SBCCS** (25)</span><span class="sxs-lookup"><span data-stu-id="45cf8-572"><span id="SBCCS_Channel"></span><span id="sbccs_channel"></span><span id="SBCCS_CHANNEL"></span>**SBCCS Channel** (25)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-573"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**Unidad de control SBCCS** (26)</span><span class="sxs-lookup"><span data-stu-id="45cf8-573"><span id="SBCCS_Control_Unit"></span><span id="sbccs_control_unit"></span><span id="SBCCS_CONTROL_UNIT"></span>**SBCCS Control Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-574"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**Canal FC-SB-2** (27)</span><span class="sxs-lookup"><span data-stu-id="45cf8-574"><span id="FC-SB-2_Channel"></span><span id="fc-sb-2_channel"></span><span id="FC-SB-2_CHANNEL"></span>**FC-SB-2 Channel** (27)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-575"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**Unidad de control FC-SB-2** (28)</span><span class="sxs-lookup"><span data-stu-id="45cf8-575"><span id="FC-SB-2_Control_Unit"></span><span id="fc-sb-2_control_unit"></span><span id="FC-SB-2_CONTROL_UNIT"></span>**FC-SB-2 Control Unit** (28)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-576"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Canal de fibra Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span><span class="sxs-lookup"><span data-stu-id="45cf8-576"><span id="Fibre_Channel_Services__FC-GS__FC-GS-2__FC-GS-3_"></span><span id="fibre_channel_services__fc-gs__fc-gs-2__fc-gs-3_"></span><span id="FIBRE_CHANNEL_SERVICES__FC-GS__FC-GS-2__FC-GS-3_"></span>**Fibre Channel Services (FC-GS, FC-GS-2, FC-GS-3)** (32)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-577"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span><span class="sxs-lookup"><span data-stu-id="45cf8-577"><span id="FC-SW"></span><span id="fc-sw"></span>**FC-SW** (34)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-578"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC-SNMP** (36)</span><span class="sxs-lookup"><span data-stu-id="45cf8-578"><span id="FC_-_SNMP"></span><span id="fc_-_snmp"></span>**FC - SNMP** (36)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-579"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI-FP** (64)</span><span class="sxs-lookup"><span data-stu-id="45cf8-579"><span id="HIPPI_-_FP"></span><span id="hippi_-_fp"></span>**HIPPI - FP** (64)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-580"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**Control BBL** (80)</span><span class="sxs-lookup"><span data-stu-id="45cf8-580"><span id="BBL_Control"></span><span id="bbl_control"></span><span id="BBL_CONTROL"></span>**BBL Control** (80)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-581"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL FDDI** (81)</span><span class="sxs-lookup"><span data-stu-id="45cf8-581"><span id="BBL_FDDI_Encapsulated_LAN_PDU"></span><span id="bbl_fddi_encapsulated_lan_pdu"></span><span id="BBL_FDDI_ENCAPSULATED_LAN_PDU"></span>**BBL FDDI Encapsulated LAN PDU** (81)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-582"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**PDU de LAN encapsulada BBL 802,3** (82)</span><span class="sxs-lookup"><span data-stu-id="45cf8-582"><span id="BBL_802.3_Encapsulated_LAN_PDU"></span><span id="bbl_802.3_encapsulated_lan_pdu"></span><span id="BBL_802.3_ENCAPSULATED_LAN_PDU"></span>**BBL 802.3 Encapsulated LAN PDU** (82)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-583"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC-VI** (88)</span><span class="sxs-lookup"><span data-stu-id="45cf8-583"><span id="FC_-_VI"></span><span id="fc_-_vi"></span>**FC - VI** (88)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-584"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC-AV** (96)</span><span class="sxs-lookup"><span data-stu-id="45cf8-584"><span id="FC_-_AV"></span><span id="fc_-_av"></span>**FC - AV** (96)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-585"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Proveedor único** (255)</span><span class="sxs-lookup"><span data-stu-id="45cf8-585"><span id="Vendor_unique"></span><span id="vendor_unique"></span><span id="VENDOR_UNIQUE"></span>**Vendor unique** (255)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="45cf8-586">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="45cf8-586">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-587">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="45cf8-587">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-588">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-588">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-589">Calificadores: **unidades** ("bytes")</span><span class="sxs-lookup"><span data-stu-id="45cf8-589">Qualifiers: **Units** ("Bytes")</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-590">La unidad de transmisión máxima (MTU) que se puede admitir, en bytes.</span><span class="sxs-lookup"><span data-stu-id="45cf8-590">The maximum transmission unit (MTU) that can be supported, in bytes.</span></span> <span data-ttu-id="45cf8-591">Esta propiedad se hereda de [**\_ NetworkPort CIM**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span><span class="sxs-lookup"><span data-stu-id="45cf8-591">This property is inherited from [**CIM\_NetworkPort**](/previous-versions/windows/desktop/iscsitarg/cim-networkport).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-592">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="45cf8-592">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-593">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-593">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-594">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-594">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-595">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="45cf8-595">The scoping system's creation class name.</span></span> <span data-ttu-id="45cf8-596">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="45cf8-596">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-597">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="45cf8-597">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-598">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="45cf8-598">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-599">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-599">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-600">Nombre del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="45cf8-600">The scoping system's name.</span></span> <span data-ttu-id="45cf8-601">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span><span class="sxs-lookup"><span data-stu-id="45cf8-601">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice).</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-602">**TimeOfLastStateChange**</span><span class="sxs-lookup"><span data-stu-id="45cf8-602">**TimeOfLastStateChange**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-603">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="45cf8-603">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-604">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-604">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-605">Fecha u hora en que se cambió por última vez el estado habilitado del elemento.</span><span class="sxs-lookup"><span data-stu-id="45cf8-605">The date or time when the enabled state of the element last changed.</span></span> <span data-ttu-id="45cf8-606">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="45cf8-606">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-607">**TotalPowerOnHours**</span><span class="sxs-lookup"><span data-stu-id="45cf8-607">**TotalPowerOnHours**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-608">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="45cf8-608">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-609">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-609">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-610">Número total de horas que se ha alimentado este dispositivo.</span><span class="sxs-lookup"><span data-stu-id="45cf8-610">The total number of hours that this device has been powered.</span></span> <span data-ttu-id="45cf8-611">Esta propiedad se hereda del [**\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), pero no se usa.</span><span class="sxs-lookup"><span data-stu-id="45cf8-611">This property is inherited from [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice), but it is not used.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-612">**TransitioningToState**</span><span class="sxs-lookup"><span data-stu-id="45cf8-612">**TransitioningToState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-613">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-613">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-614">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-614">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-615">Indica el estado de destino al que la instancia está cambiando.</span><span class="sxs-lookup"><span data-stu-id="45cf8-615">Indicates the target state to which the instance is transitioning.</span></span> <span data-ttu-id="45cf8-616">Esta propiedad se hereda de [**CIM \_ EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="45cf8-616">This property is inherited from [**CIM\_EnabledLogicalElement**](/previous-versions//cc136818(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> <dt>

<span data-ttu-id="45cf8-617">**UsageRestriction**</span><span class="sxs-lookup"><span data-stu-id="45cf8-617">**UsageRestriction**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="45cf8-618">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="45cf8-618">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-619">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="45cf8-619">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="45cf8-620">En algunas circunstancias, un puerto lógico puede identificarse como un puerto de front-end o back-end.</span><span class="sxs-lookup"><span data-stu-id="45cf8-620">In some circumstances, a logical port might be identifiable as a front end or back end port.</span></span> <span data-ttu-id="45cf8-621">Un ejemplo de esta situación sería una matriz de almacenamiento que podría tener puertos back-end para comunicarse con las unidades de disco y los puertos front-end para comunicarse con los hosts.</span><span class="sxs-lookup"><span data-stu-id="45cf8-621">An example of this situation would be a storage array that might have back end ports to communicate with disk drives and front end ports to communicate with hosts.</span></span> <span data-ttu-id="45cf8-622">Si no hay ninguna restricción sobre el uso del puerto, el valor debe establecerse en 4 (no restringido).</span><span class="sxs-lookup"><span data-stu-id="45cf8-622">If there is no restriction on the use of the port, then the value should be set to 4 (Not restricted).</span></span> <span data-ttu-id="45cf8-623">Esta propiedad se hereda de [**\_ LogicalPort CIM**](/previous-versions//cc136869(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="45cf8-623">This property is inherited from [**CIM\_LogicalPort**](/previous-versions//cc136869(v=vs.85)).</span></span>

<dl> <dt>

<span data-ttu-id="45cf8-624"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="45cf8-624"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-625"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Solo front-end** (2)</span><span class="sxs-lookup"><span data-stu-id="45cf8-625"><span id="Front-end_only"></span><span id="front-end_only"></span><span id="FRONT-END_ONLY"></span>**Front-end only** (2)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-626"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Solo back-end** (3)</span><span class="sxs-lookup"><span data-stu-id="45cf8-626"><span id="Back-end_only"></span><span id="back-end_only"></span><span id="BACK-END_ONLY"></span>**Back-end only** (3)</span></span>
</dt> <dt>

<span data-ttu-id="45cf8-627"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**No restringido** (4)</span><span class="sxs-lookup"><span data-stu-id="45cf8-627"><span id="Not_restricted_"></span><span id="not_restricted_"></span><span id="NOT_RESTRICTED_"></span>**Not restricted** (4 )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="45cf8-628">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45cf8-628">Requirements</span></span>



| <span data-ttu-id="45cf8-629">Requisito</span><span class="sxs-lookup"><span data-stu-id="45cf8-629">Requirement</span></span> | <span data-ttu-id="45cf8-630">Value</span><span class="sxs-lookup"><span data-stu-id="45cf8-630">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45cf8-631">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45cf8-631">Minimum supported client</span></span><br/> | <span data-ttu-id="45cf8-632">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="45cf8-632">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="45cf8-633">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="45cf8-633">Minimum supported server</span></span><br/> | <span data-ttu-id="45cf8-634">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="45cf8-634">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="45cf8-635">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="45cf8-635">Namespace</span></span><br/>                | <span data-ttu-id="45cf8-636">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="45cf8-636">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="45cf8-637">MOF</span><span class="sxs-lookup"><span data-stu-id="45cf8-637">MOF</span></span><br/>                      | <dl> <span data-ttu-id="45cf8-638"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="45cf8-638"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="45cf8-639">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="45cf8-639">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45cf8-640"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="45cf8-640"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

