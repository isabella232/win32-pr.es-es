---
description: Representa los datos de estado de la característica de descarga de puertos.
ms.assetid: 1117b9e4-cff7-4c9e-bf5e-74499297e84e
title: Msvm_EthernetSwitchPortOffloadData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortOffloadData
- Msvm_EthernetSwitchPortOffloadData.InstanceID
- Msvm_EthernetSwitchPortOffloadData.Caption
- Msvm_EthernetSwitchPortOffloadData.Description
- Msvm_EthernetSwitchPortOffloadData.ElementName
- Msvm_EthernetSwitchPortOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchPortOffloadData.SystemName
- Msvm_EthernetSwitchPortOffloadData.DeviceCreationClassName
- Msvm_EthernetSwitchPortOffloadData.DeviceID
- Msvm_EthernetSwitchPortOffloadData.CreationClassName
- Msvm_EthernetSwitchPortOffloadData.Name
- Msvm_EthernetSwitchPortOffloadData.IpsecCurrentOffloadSaCount
- Msvm_EthernetSwitchPortOffloadData.IovOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQOffloadUsage
- Msvm_EthernetSwitchPortOffloadData.VMQId
- Msvm_EthernetSwitchPortOffloadData.IovVfId
- Msvm_EthernetSwitchPortOffloadData.IovVfDataPathActive
- Msvm_EthernetSwitchPortOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchPortOffloadData.VmmqQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VrssVmbusChannelAffinityPolicy
- Msvm_EthernetSwitchPortOffloadData.VrssIndependentHostSpreading
- Msvm_EthernetSwitchPortOffloadData.VrssExcludePrimaryProcessor
- Msvm_EthernetSwitchPortOffloadData.VrssQueueSchedulingMode
- Msvm_EthernetSwitchPortOffloadData.VrssMinQueuePairs
- Msvm_EthernetSwitchPortOffloadData.VmmqEnabled
- Msvm_EthernetSwitchPortOffloadData.VrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: fd60e98c8df12b539bb51c60b34e7931b762dc03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670028"
---
# <a name="msvm_ethernetswitchportoffloaddata-class"></a><span data-ttu-id="4fabd-103">MSVM \_ EthernetSwitchPortOffloadData (clase)</span><span class="sxs-lookup"><span data-stu-id="4fabd-103">Msvm\_EthernetSwitchPortOffloadData class</span></span>

<span data-ttu-id="4fabd-104">Representa los datos de estado de la característica de descarga de puertos.</span><span class="sxs-lookup"><span data-stu-id="4fabd-104">Represents the port offload feature status data.</span></span>

<span data-ttu-id="4fabd-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4fabd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fabd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4fabd-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("C885BFD1-ABB7-418F-8163-9F379C9F7166"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("3"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Offload Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortOffloadData : Msvm_EthernetPortData
{
  string  InstanceID;
  string  Caption = "Ethernet Switch Port Offload Feature Status";
  string  Description = "Represents the port offload feature status data.";
  string  ElementName = "Ethernet Switch Port Offload Feature Status";
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string  DeviceID;
  string  CreationClassName = "Msvm_EthernetSwitchPortOffloadData";
  string  Name;
  uint32  IpsecCurrentOffloadSaCount = 0;
  uint32  IovOffloadUsage = 0;
  uint32  VMQOffloadUsage = 0;
  uint32  VMQId = 0;
  uint16  IovVfId = 0;
  boolean IovVfDataPathActive = FALSE;
  uint32  IovQueuePairUsage = 0;
  uint32  VmmqQueuePairs = 0;
  uint32  VrssVmbusChannelAffinityPolicy = 0;
  boolean VrssIndependentHostSpreading = FALSE;
  boolean VrssExcludePrimaryProcessor = FALSE;
  uint32  VrssQueueSchedulingMode = 0;
  uint32  VrssMinQueuePairs = 0;
  boolean VmmqEnabled = FALSE;
  boolean VrssEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="4fabd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="4fabd-107">Members</span></span>

<span data-ttu-id="4fabd-108">La clase **MSVM \_ EthernetSwitchPortOffloadData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4fabd-108">The **Msvm\_EthernetSwitchPortOffloadData** class has these types of members:</span></span>

-   [<span data-ttu-id="4fabd-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4fabd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4fabd-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4fabd-110">Properties</span></span>

<span data-ttu-id="4fabd-111">La clase **MSVM \_ EthernetSwitchPortOffloadData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4fabd-111">The **Msvm\_EthernetSwitchPortOffloadData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4fabd-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="4fabd-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4fabd-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="4fabd-115">A short description of the object.</span></span> <span data-ttu-id="4fabd-116">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "estado de la característica de descarga de puertos del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="4fabd-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4fabd-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4fabd-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-120">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="4fabd-120">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-121">Nombre de la subclase utilizada en la creación de esta instancia de datos de puerto.</span><span class="sxs-lookup"><span data-stu-id="4fabd-121">The name of the subclass used in the creation of this port data instance.</span></span> <span data-ttu-id="4fabd-122">Esta propiedad se hereda de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)y siempre se establece en "MSVM \_ EthernetSwitchPortOffloadData".</span><span class="sxs-lookup"><span data-stu-id="4fabd-122">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPortOffloadData".</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-123">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4fabd-123">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4fabd-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-126">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="4fabd-126">A description of the object.</span></span> <span data-ttu-id="4fabd-127">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "representa los datos de estado de la característica de descarga de puertos".</span><span class="sxs-lookup"><span data-stu-id="4fabd-127">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port offload feature status data.".</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-128">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4fabd-128">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4fabd-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-131">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="4fabd-131">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-132">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="4fabd-132">The scoping system's creation class name.</span></span> <span data-ttu-id="4fabd-133">Esta propiedad se hereda de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)y siempre se establece en "MSVM \_ EthernetSwitchPort".</span><span class="sxs-lookup"><span data-stu-id="4fabd-133">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-134">**ID**</span><span class="sxs-lookup"><span data-stu-id="4fabd-134">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4fabd-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-137">Calificadores: **clave**, **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="4fabd-137">Qualifiers: **Key**, **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-138">El ID. de dispositivo del puerto que limita esta instancia de datos del puerto.</span><span class="sxs-lookup"><span data-stu-id="4fabd-138">The Device ID of the port that scopes this port data instance.</span></span> <span data-ttu-id="4fabd-139">Esta propiedad se hereda de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="4fabd-139">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-140">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="4fabd-140">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4fabd-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-143">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="4fabd-143">A display name for the object.</span></span> <span data-ttu-id="4fabd-144">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "estado de la característica de descarga de puertos del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="4fabd-144">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Offload Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-145">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4fabd-145">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4fabd-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-148">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="4fabd-148">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-149">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="4fabd-149">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="4fabd-150">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="4fabd-150">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-151">**IovOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="4fabd-151">**IovOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-152">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4fabd-152">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-153">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4fabd-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-154">Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4fabd-154">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-155">El uso de la descarga actual de la virtualización de e/s (IOV).</span><span class="sxs-lookup"><span data-stu-id="4fabd-155">The current I/O virtualization (IOV) offload usage.</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-156">**IovQueuePairUsage**</span><span class="sxs-lookup"><span data-stu-id="4fabd-156">**IovQueuePairUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-157">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4fabd-157">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-158">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4fabd-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-159">Calificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4fabd-159">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-160">Número actual de pares de colas utilizados por el puerto.</span><span class="sxs-lookup"><span data-stu-id="4fabd-160">The current number of queue pairs being used by the port.</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-161">**IovVfDataPathActive**</span><span class="sxs-lookup"><span data-stu-id="4fabd-161">**IovVfDataPathActive**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-162">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4fabd-162">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4fabd-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-164">Calificadores: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4fabd-164">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-165">Indica si la ruta de acceso de datos de VF de IOV está activa.</span><span class="sxs-lookup"><span data-stu-id="4fabd-165">Indicates whether the IOV VF data path is active.</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-166">**IovVfId**</span><span class="sxs-lookup"><span data-stu-id="4fabd-166">**IovVfId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-167">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4fabd-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-168">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4fabd-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-169">Calificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4fabd-169">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-170">Identificador del FV de IOV actual que está asignado al puerto.</span><span class="sxs-lookup"><span data-stu-id="4fabd-170">The current IOV VF identifier that is assigned to the port.</span></span> <span data-ttu-id="4fabd-171">Es válido si **IovOffloadUsage** no es cero.</span><span class="sxs-lookup"><span data-stu-id="4fabd-171">This is valid if **IovOffloadUsage** is not zero.</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-172">**IpsecCurrentOffloadSaCount**</span><span class="sxs-lookup"><span data-stu-id="4fabd-172">**IpsecCurrentOffloadSaCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-173">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4fabd-173">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-174">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4fabd-174">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-175">Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4fabd-175">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-176">El número actual de ranuras de descarga de la Asociación de seguridad (SA) en uso en el puerto.</span><span class="sxs-lookup"><span data-stu-id="4fabd-176">The current number of security association (SA) offload slots in use on the port.</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-177">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="4fabd-177">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4fabd-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-179">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-179">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-180">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="4fabd-180">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-181">Cadena que identifica de forma única esta instancia de datos de puerto en el ámbito del modificador y el puerto.</span><span class="sxs-lookup"><span data-stu-id="4fabd-181">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span> <span data-ttu-id="4fabd-182">Esta propiedad se hereda de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="4fabd-182">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-183">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="4fabd-183">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-184">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4fabd-184">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-185">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-185">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-186">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="4fabd-186">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-187">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="4fabd-187">The scoping system's creation class name.</span></span> <span data-ttu-id="4fabd-188">Esta propiedad se hereda de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)y siempre se establece en "MSVM \_ VirtualEthernetSwitch".</span><span class="sxs-lookup"><span data-stu-id="4fabd-188">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-189">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="4fabd-189">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-190">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4fabd-190">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-191">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-191">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-192">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="4fabd-192">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-193">El nombre del conmutador virtual que limita esta instancia de datos de puerto.</span><span class="sxs-lookup"><span data-stu-id="4fabd-193">The name of the virtual switch that scopes this port data instance.</span></span> <span data-ttu-id="4fabd-194">Esta propiedad se hereda de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="4fabd-194">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-195">**VmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="4fabd-195">**VmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-196">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4fabd-196">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-197">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-197">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-198">Calificadores: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4fabd-198">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-199">Indica si VMMQ está activo.</span><span class="sxs-lookup"><span data-stu-id="4fabd-199">Indicates if VMMQ is active.</span></span>

> [!Note]  
> <span data-ttu-id="4fabd-200">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4fabd-200">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="4fabd-201">**VmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="4fabd-201">**VmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-202">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4fabd-202">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-204">Calificadores: **WmiDataId** (10), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4fabd-204">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-205">Indica cuántas colas se utilizan para VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="4fabd-205">Indicates how many queues are used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="4fabd-206">Esta propiedad se agregó en Windows 10, versión 1703 y Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="4fabd-206">This property was added in Windows 10, version 1703 and Windows Server 2016.</span></span>

 

</dd> <dt>

<span data-ttu-id="4fabd-207">**VMQId**</span><span class="sxs-lookup"><span data-stu-id="4fabd-207">**VMQId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-208">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4fabd-208">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-209">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4fabd-209">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-210">Calificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4fabd-210">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-211">Identificador de la cola de máquina virtual actual asignado al puerto.</span><span class="sxs-lookup"><span data-stu-id="4fabd-211">The current virtual machine queue identifier that is assigned to the port.</span></span> <span data-ttu-id="4fabd-212">Es válido si **VMQOffloadUsage** no es cero.</span><span class="sxs-lookup"><span data-stu-id="4fabd-212">This is valid if **VMQOffloadUsage** is not zero.</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-213">**VMQOffloadUsage**</span><span class="sxs-lookup"><span data-stu-id="4fabd-213">**VMQOffloadUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-214">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4fabd-214">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-215">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4fabd-215">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-216">Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4fabd-216">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-217">El uso de la descarga actual de la cola de máquinas virtuales (VMQ).</span><span class="sxs-lookup"><span data-stu-id="4fabd-217">The current virtual machine queue (VMQ) offload usage.</span></span>

</dd> <dt>

<span data-ttu-id="4fabd-218">**VrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="4fabd-218">**VrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-219">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4fabd-219">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-220">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-220">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-221">Calificadores: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4fabd-221">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-222">Indica si vRSS está activo.</span><span class="sxs-lookup"><span data-stu-id="4fabd-222">Indicates if vRSS is active.</span></span>

> [!Note]  
> <span data-ttu-id="4fabd-223">Esta propiedad se agregó en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="4fabd-223">This property was added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="4fabd-224">**VrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="4fabd-224">**VrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-225">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4fabd-225">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-226">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-226">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-227">Calificadores: **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4fabd-227">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-228">Indica si la CPU VMQ primaria está excluida de la tabla de indirección VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="4fabd-228">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="4fabd-229">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="4fabd-229">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="4fabd-230">**VrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="4fabd-230">**VrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-231">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="4fabd-231">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-232">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-232">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-233">Calificadores: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4fabd-233">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-234">Indica si se produce la propagación de VRSS/VMMQ del lado del host, independientemente de la configuración de RSS de la NIC virtual.</span><span class="sxs-lookup"><span data-stu-id="4fabd-234">Indicates whether host side VRSS/VMMQ spreading happens, regardless of RSS settings of the virtual NIC.</span></span>

> [!Note]  
> <span data-ttu-id="4fabd-235">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="4fabd-235">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="4fabd-236">**VrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="4fabd-236">**VrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-237">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4fabd-237">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-238">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-238">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-239">Calificadores: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4fabd-239">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-240">Indica el número mínimo de colas usadas para VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="4fabd-240">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="4fabd-241">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="4fabd-241">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="4fabd-242">**VrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="4fabd-242">**VrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-243">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4fabd-243">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-244">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-244">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-245">Calificadores: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4fabd-245">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-246">Indica cómo se dirigen las colas de VRSS/VMMQ a diferentes procesadores de host.</span><span class="sxs-lookup"><span data-stu-id="4fabd-246">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="4fabd-247">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="4fabd-247">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="4fabd-248">**VrssVmbusChannelAffinityPolicy**</span><span class="sxs-lookup"><span data-stu-id="4fabd-248">**VrssVmbusChannelAffinityPolicy**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4fabd-249">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4fabd-249">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-250">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4fabd-250">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4fabd-251">Calificadores: **WmiDataId** (15), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="4fabd-251">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="4fabd-252">Indica cómo se afinidad con los canales de Vmbus para hospedar procesadores.</span><span class="sxs-lookup"><span data-stu-id="4fabd-252">Indicates how Vmbus channels are affinitized to host processors.</span></span>

> [!Note]  
> <span data-ttu-id="4fabd-253">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="4fabd-253">Added in Windows 10, version 1709.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4fabd-254">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4fabd-254">Requirements</span></span>



| <span data-ttu-id="4fabd-255">Requisito</span><span class="sxs-lookup"><span data-stu-id="4fabd-255">Requirement</span></span> | <span data-ttu-id="4fabd-256">Value</span><span class="sxs-lookup"><span data-stu-id="4fabd-256">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fabd-257">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fabd-257">Minimum supported client</span></span><br/> | <span data-ttu-id="4fabd-258">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="4fabd-258">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="4fabd-259">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4fabd-259">Minimum supported server</span></span><br/> | <span data-ttu-id="4fabd-260">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="4fabd-260">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4fabd-261">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4fabd-261">Namespace</span></span><br/>                | <span data-ttu-id="4fabd-262">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4fabd-262">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="4fabd-263">MOF</span><span class="sxs-lookup"><span data-stu-id="4fabd-263">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4fabd-264"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4fabd-264"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4fabd-265">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4fabd-265">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fabd-266"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4fabd-266"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

