---
description: Representa el estado de descarga del hardware del conmutador.
ms.assetid: 77a34df7-e3c4-4d91-af5a-91a03dd8246d
title: Msvm_EthernetSwitchHardwareOffloadData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchHardwareOffloadData
- Msvm_EthernetSwitchHardwareOffloadData.InstanceID
- Msvm_EthernetSwitchHardwareOffloadData.Caption
- Msvm_EthernetSwitchHardwareOffloadData.Description
- Msvm_EthernetSwitchHardwareOffloadData.ElementName
- Msvm_EthernetSwitchHardwareOffloadData.SystemCreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.SystemName
- Msvm_EthernetSwitchHardwareOffloadData.CreationClassName
- Msvm_EthernetSwitchHardwareOffloadData.Name
- Msvm_EthernetSwitchHardwareOffloadData.IovVfCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovVfUsage
- Msvm_EthernetSwitchHardwareOffloadData.VmqCapacity
- Msvm_EthernetSwitchHardwareOffloadData.VmqUsage
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSACapacity
- Msvm_EthernetSwitchHardwareOffloadData.IPsecSAUsage
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairCapacity
- Msvm_EthernetSwitchHardwareOffloadData.IovQueuePairUsage
- Msvm_EthernetSwitchHardwareOffloadData.PacketDirectInUse
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssIndependentHostSpreading
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssExcludePrimaryProcessor
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssQueueSchedulingMode
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssMinQueuePairs
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVmmqEnabled
- Msvm_EthernetSwitchHardwareOffloadData.DefaultQueueVrssEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b64762b824cea7d3b064636e7f7f87777e053daf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670031"
---
# <a name="msvm_ethernetswitchhardwareoffloaddata-class"></a><span data-ttu-id="bd570-103">MSVM \_ EthernetSwitchHardwareOffloadData (clase)</span><span class="sxs-lookup"><span data-stu-id="bd570-103">Msvm\_EthernetSwitchHardwareOffloadData class</span></span>

<span data-ttu-id="bd570-104">Representa el estado de descarga del hardware del conmutador.</span><span class="sxs-lookup"><span data-stu-id="bd570-104">Represents the switch hardware offload status.</span></span>

<span data-ttu-id="bd570-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="bd570-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd570-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd570-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("1C37E01C-0CD6-496F-9076-90C131033DC2"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("4"), InterfaceRevision("0"), DisplayName("Ethernet Switch Offload Resource Status"), AMENDMENT]
class Msvm_EthernetSwitchHardwareOffloadData : Msvm_EthernetSwitchData
{
  string  InstanceID;
  string  Caption = Ethernet Switch Offload Resource Status;
  string  Description = Represents the switch hardware offload status.;
  string  ElementName = Ethernet Switch Offload Resource Status;
  string  SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string  SystemName;
  string  CreationClassName = "Msvm_EthernetSwitchHardwareOffloadData";
  string  Name;
  uint32  IovVfCapacity = 0;
  uint32  IovVfUsage = 0;
  uint32  VmqCapacity = 0;
  uint32  VmqUsage = 0;
  uint32  IPsecSACapacity = 0;
  uint32  IPsecSAUsage = 0;
  uint32  IovQueuePairCapacity = 0;
  uint32  IovQueuePairUsage = 0;
  boolean PacketDirectInUse = FALSE;
  uint32  DefaultQueueVmmqQueuePairs = 0;
  boolean DefaultQueueVrssIndependentHostSpreading = TRUE;
  boolean DefaultQueueVrssExcludePrimaryProcessor = FALSE;
  uint32  DefaultQueueVrssQueueSchedulingMode = 0;
  uint32  DefaultQueueVrssMinQueuePairs = 0;
  boolean DefaultQueueVmmqEnabled = FALSE;
  boolean DefaultQueueVrssEnabled = FALSE;
};
```

## <a name="members"></a><span data-ttu-id="bd570-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="bd570-107">Members</span></span>

<span data-ttu-id="bd570-108">La clase **MSVM \_ EthernetSwitchHardwareOffloadData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bd570-108">The **Msvm\_EthernetSwitchHardwareOffloadData** class has these types of members:</span></span>

-   [<span data-ttu-id="bd570-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bd570-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bd570-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bd570-110">Properties</span></span>

<span data-ttu-id="bd570-111">La clase **MSVM \_ EthernetSwitchHardwareOffloadData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bd570-111">The **Msvm\_EthernetSwitchHardwareOffloadData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd570-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="bd570-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bd570-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd570-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="bd570-115">A short description of the object.</span></span> <span data-ttu-id="bd570-116">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bd570-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bd570-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bd570-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bd570-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-120">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="bd570-120">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-121">Nombre de la clase o subclase utilizada en la creación de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="bd570-121">The name of the class or subclass used in the creation of this instance.</span></span> <span data-ttu-id="bd570-122">Esta propiedad se hereda de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="bd570-122">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd570-123">**DefaultQueueVmmqEnabled**</span><span class="sxs-lookup"><span data-stu-id="bd570-123">**DefaultQueueVmmqEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-124">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bd570-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-126">Calificadores: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-126">Qualifiers: **WmiDataId** (11), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-127">La configuración actual de VMMQ para la cola predeterminada</span><span class="sxs-lookup"><span data-stu-id="bd570-127">The current VMMQ setting for default queue</span></span>

> [!Note]  
> <span data-ttu-id="bd570-128">Propiedad agregada en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="bd570-128">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="bd570-129">**DefaultQueueVmmqQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="bd570-129">**DefaultQueueVmmqQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-130">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd570-130">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-132">Calificadores: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-132">Qualifiers: **WmiDataId** (12), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-133">El número actual de colas asignadas para la cola predeterminada</span><span class="sxs-lookup"><span data-stu-id="bd570-133">The current number of queues allocated for the default queue</span></span>

> [!Note]  
> <span data-ttu-id="bd570-134">Propiedad agregada en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="bd570-134">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="bd570-135">**DefaultQueueVrssEnabled**</span><span class="sxs-lookup"><span data-stu-id="bd570-135">**DefaultQueueVrssEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-136">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bd570-136">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-138">Calificadores: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-138">Qualifiers: **WmiDataId** (10), **InterfaceVersion** (3), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-139">La configuración de VRss actual para la cola predeterminada</span><span class="sxs-lookup"><span data-stu-id="bd570-139">The current VRss setting for default queue</span></span>

> [!Note]  
> <span data-ttu-id="bd570-140">Propiedad agregada en la versión 1703 de Windows 10.</span><span class="sxs-lookup"><span data-stu-id="bd570-140">Property added in Windows 10, version 1703.</span></span>

 

</dd> <dt>

<span data-ttu-id="bd570-141">**DefaultQueueVrssExcludePrimaryProcessor**</span><span class="sxs-lookup"><span data-stu-id="bd570-141">**DefaultQueueVrssExcludePrimaryProcessor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-142">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bd570-142">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-144">Calificadores: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-144">Qualifiers: **WmiDataId** (15), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-145">Indica si la CPU VMQ primaria está excluida de la tabla de indirección VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="bd570-145">Indicates whether the primary VMQ CPU is excluded from the VRSS/VMMQ indirection table.</span></span>

> [!Note]  
> <span data-ttu-id="bd570-146">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="bd570-146">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="bd570-147">**DefaultQueueVrssIndependentHostSpreading**</span><span class="sxs-lookup"><span data-stu-id="bd570-147">**DefaultQueueVrssIndependentHostSpreading**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-148">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bd570-148">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-150">Calificadores: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-150">Qualifiers: **WmiDataId** (16), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-151">Indica si se va a realizar siempre la propagación de VRSS para la cola predeterminada, independientemente del estado de RSS del vPort externo.</span><span class="sxs-lookup"><span data-stu-id="bd570-151">Indicates whether to always do VRSS spreading for default queue, regardless of the RSS state of the external vPort.</span></span>

> [!Note]  
> <span data-ttu-id="bd570-152">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="bd570-152">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="bd570-153">**DefaultQueueVrssMinQueuePairs**</span><span class="sxs-lookup"><span data-stu-id="bd570-153">**DefaultQueueVrssMinQueuePairs**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-154">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd570-154">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-156">Calificadores: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-156">Qualifiers: **WmiDataId** (13), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-157">Indica el número mínimo de colas usadas para VRSS/VMMQ.</span><span class="sxs-lookup"><span data-stu-id="bd570-157">Indicates minimum number of queues used for VRSS/VMMQ.</span></span>

> [!Note]  
> <span data-ttu-id="bd570-158">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="bd570-158">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="bd570-159">**DefaultQueueVrssQueueSchedulingMode**</span><span class="sxs-lookup"><span data-stu-id="bd570-159">**DefaultQueueVrssQueueSchedulingMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-160">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd570-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-162">Calificadores: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-162">Qualifiers: **WmiDataId** (14), **InterfaceVersion** (4), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-163">Indica cómo se dirigen las colas de VRSS/VMMQ a diferentes procesadores de host.</span><span class="sxs-lookup"><span data-stu-id="bd570-163">Indicates how VRSS/VMMQ queues are steered to different host processors.</span></span>

> [!Note]  
> <span data-ttu-id="bd570-164">Agregado en Windows 10, versión 1709.</span><span class="sxs-lookup"><span data-stu-id="bd570-164">Added in Windows 10, version 1709.</span></span>

 

</dd> <dt>

<span data-ttu-id="bd570-165">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bd570-165">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bd570-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd570-168">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="bd570-168">A description of the object.</span></span> <span data-ttu-id="bd570-169">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bd570-169">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bd570-170">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="bd570-170">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bd570-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd570-173">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="bd570-173">A display name for the object.</span></span> <span data-ttu-id="bd570-174">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bd570-174">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bd570-175">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="bd570-175">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-176">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bd570-176">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-177">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-177">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-178">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="bd570-178">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="bd570-179">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="bd570-179">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="bd570-180">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="bd570-180">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="bd570-181">**IovQueuePairCapacity**</span><span class="sxs-lookup"><span data-stu-id="bd570-181">**IovQueuePairCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-182">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd570-182">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-183">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-184">Calificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-184">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-185">Número máximo de pares de colas admitidos por el modificador.</span><span class="sxs-lookup"><span data-stu-id="bd570-185">The maximum number of queue pairs supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="bd570-186">**IovQueuePairUsage**</span><span class="sxs-lookup"><span data-stu-id="bd570-186">**IovQueuePairUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-187">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd570-187">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-188">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-188">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-189">Calificadores: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-189">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-190">Número actual de pares de colas utilizados por el modificador.</span><span class="sxs-lookup"><span data-stu-id="bd570-190">The current number of queue pairs being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="bd570-191">**IovVfCapacity**</span><span class="sxs-lookup"><span data-stu-id="bd570-191">**IovVfCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-192">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd570-192">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-193">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-193">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-194">Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-194">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-195">Número máximo de funciones virtuales admitidas por el modificador.</span><span class="sxs-lookup"><span data-stu-id="bd570-195">The maximum number of virtual functions supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="bd570-196">**IovVfUsage**</span><span class="sxs-lookup"><span data-stu-id="bd570-196">**IovVfUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-197">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd570-197">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-198">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-198">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-199">Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-199">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-200">Número actual de funciones virtuales que usa el modificador.</span><span class="sxs-lookup"><span data-stu-id="bd570-200">The current number of virtual functions being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="bd570-201">**IPsecSACapacity**</span><span class="sxs-lookup"><span data-stu-id="bd570-201">**IPsecSACapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-202">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd570-202">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-203">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-203">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-204">Calificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-204">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-205">Número máximo de descargas de Asociación de seguridad de IPsec admitidas por el modificador.</span><span class="sxs-lookup"><span data-stu-id="bd570-205">The maximum number of IPsec security association offloads supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="bd570-206">**IPsecSAUsage**</span><span class="sxs-lookup"><span data-stu-id="bd570-206">**IPsecSAUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-207">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd570-207">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-208">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-208">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-209">Calificadores: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-209">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-210">Número actual de descargas de la Asociación de seguridad de IPsec que utiliza el modificador.</span><span class="sxs-lookup"><span data-stu-id="bd570-210">The current number of IPsec security association offloads being used by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="bd570-211">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="bd570-211">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-212">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bd570-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-213">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-213">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-214">Calificadores: **clave**, **invalidación**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="bd570-214">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-215">Nombre único del recurso.</span><span class="sxs-lookup"><span data-stu-id="bd570-215">The unique name of the resource.</span></span> <span data-ttu-id="bd570-216">Esta propiedad se hereda de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="bd570-216">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd570-217">**PacketDirectInUse**</span><span class="sxs-lookup"><span data-stu-id="bd570-217">**PacketDirectInUse**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-218">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="bd570-218">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-219">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-220">Calificadores: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-220">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (2), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-221">Indica si el modificador está usando Packet Direct</span><span class="sxs-lookup"><span data-stu-id="bd570-221">Indicates if packet direct is being used by the switch</span></span>

> [!Note]  
> <span data-ttu-id="bd570-222">Propiedad agregada en Windows 10.</span><span class="sxs-lookup"><span data-stu-id="bd570-222">Property added in Windows 10.</span></span>

 

</dd> <dt>

<span data-ttu-id="bd570-223">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="bd570-223">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-224">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bd570-224">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-225">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-226">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="bd570-226">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-227">Nombre de la clase de creación del sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="bd570-227">The hosting system's creation class name.</span></span> <span data-ttu-id="bd570-228">Esta propiedad se hereda de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="bd570-228">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd570-229">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="bd570-229">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-230">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bd570-230">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-231">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-231">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-232">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="bd570-232">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-233">El nombre del conmutador virtual al que está enlazada la instancia de recurso asociada.</span><span class="sxs-lookup"><span data-stu-id="bd570-233">The name of the virtual switch to which the associated resource instance is bound.</span></span> <span data-ttu-id="bd570-234">Esta propiedad se hereda de [**MSVM \_ EthernetSwitchData**](msvm-ethernetswitchdata.md).</span><span class="sxs-lookup"><span data-stu-id="bd570-234">This property is inherited from [**Msvm\_EthernetSwitchData**](msvm-ethernetswitchdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="bd570-235">**VmqCapacity**</span><span class="sxs-lookup"><span data-stu-id="bd570-235">**VmqCapacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-236">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd570-236">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-237">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-237">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-238">Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-238">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-239">Número máximo de descargas de colas de máquinas virtuales admitidas por el modificador.</span><span class="sxs-lookup"><span data-stu-id="bd570-239">The maximum number of virtual machine queue offloads supported by the switch.</span></span>

</dd> <dt>

<span data-ttu-id="bd570-240">**VmqUsage**</span><span class="sxs-lookup"><span data-stu-id="bd570-240">**VmqUsage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd570-241">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="bd570-241">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="bd570-242">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd570-242">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd570-243">Calificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="bd570-243">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="bd570-244">Número actual de descargas de colas de máquinas virtuales que usa el modificador.</span><span class="sxs-lookup"><span data-stu-id="bd570-244">The current number of virtual machine queue offloads being used by the switch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bd570-245">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd570-245">Requirements</span></span>



| <span data-ttu-id="bd570-246">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd570-246">Requirement</span></span> | <span data-ttu-id="bd570-247">Value</span><span class="sxs-lookup"><span data-stu-id="bd570-247">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd570-248">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd570-248">Minimum supported client</span></span><br/> | <span data-ttu-id="bd570-249">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd570-249">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bd570-250">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd570-250">Minimum supported server</span></span><br/> | <span data-ttu-id="bd570-251">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="bd570-251">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bd570-252">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bd570-252">Namespace</span></span><br/>                | <span data-ttu-id="bd570-253">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="bd570-253">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bd570-254">MOF</span><span class="sxs-lookup"><span data-stu-id="bd570-254">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd570-255"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd570-255"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd570-256">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bd570-256">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd570-257"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bd570-257"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

