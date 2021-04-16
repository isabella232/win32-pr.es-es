---
description: Representa el estado del recurso de ancho de banda del conmutador.
ms.assetid: 9aa3e57e-9452-4c60-a052-83ae35b3607c
title: Msvm_EthernetSwitchBandwidthData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchBandwidthData
- Msvm_EthernetSwitchBandwidthData.InstanceID
- Msvm_EthernetSwitchBandwidthData.Caption
- Msvm_EthernetSwitchBandwidthData.Description
- Msvm_EthernetSwitchBandwidthData.ElementName
- Msvm_EthernetSwitchBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchBandwidthData.SystemName
- Msvm_EthernetSwitchBandwidthData.CreationClassName
- Msvm_EthernetSwitchBandwidthData.Name
- Msvm_EthernetSwitchBandwidthData.Capacity
- Msvm_EthernetSwitchBandwidthData.Reservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservationPercentage
- Msvm_EthernetSwitchBandwidthData.DefaultFlowReservation
- Msvm_EthernetSwitchBandwidthData.DefaultFlowWeight
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d238b8ddc40506a3eae8a6c7c089de2ebd87db5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686742"
---
# <a name="msvm_ethernetswitchbandwidthdata-class"></a><span data-ttu-id="513fc-103">MSVM \_ EthernetSwitchBandwidthData (clase)</span><span class="sxs-lookup"><span data-stu-id="513fc-103">Msvm\_EthernetSwitchBandwidthData class</span></span>

<span data-ttu-id="513fc-104">Representa el estado del recurso de ancho de banda del conmutador.</span><span class="sxs-lookup"><span data-stu-id="513fc-104">Represents the switch bandwidth resource status.</span></span>

<span data-ttu-id="513fc-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="513fc-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="513fc-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="513fc-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("8F425906-034D-42AB-BD16-EDB31CEC55EF"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Bandwidth data"), AMENDMENT]
class Msvm_EthernetSwitchBandwidthData : Msvm_EthernetSwitchData
{
  string InstanceID;
  string Caption = "Ethernet Switch Bandwidth data";
  string Description = "Represents the switch bandwidth resource status.";
  string ElementName = "Ethernet Switch Bandwidth data";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string CreationClassName = "Msvm_EthernetSwitchBandwidthData";
  string Name;
  uint64 Capacity = 100000000;
  uint64 Reservation = 100000000;
  uint32 DefaultFlowReservationPercentage = 10;
  uint64 DefaultFlowReservation = 100000000;
  uint64 DefaultFlowWeight = 0;
};
```

## <a name="members"></a><span data-ttu-id="513fc-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="513fc-107">Members</span></span>

<span data-ttu-id="513fc-108">La clase **MSVM \_ EthernetSwitchBandwidthData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="513fc-108">The **Msvm\_EthernetSwitchBandwidthData** class has these types of members:</span></span>

-   [<span data-ttu-id="513fc-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="513fc-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="513fc-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="513fc-110">Properties</span></span>

<span data-ttu-id="513fc-111">La clase **MSVM \_ EthernetSwitchBandwidthData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="513fc-111">The **Msvm\_EthernetSwitchBandwidthData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="513fc-112">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="513fc-112">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="513fc-113">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="513fc-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="513fc-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="513fc-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="513fc-115">Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="513fc-115">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="513fc-116">Ancho de banda máximo disponible en el conmutador.</span><span class="sxs-lookup"><span data-stu-id="513fc-116">The maximum bandwidth available on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="513fc-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="513fc-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="513fc-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="513fc-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="513fc-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="513fc-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="513fc-120">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="513fc-120">A short description of the object.</span></span> <span data-ttu-id="513fc-121">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="513fc-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="513fc-122">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="513fc-122">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="513fc-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="513fc-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="513fc-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="513fc-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="513fc-125">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="513fc-125">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="513fc-126">Nombre de la clase o subclase utilizada en la creación de esta instancia.</span><span class="sxs-lookup"><span data-stu-id="513fc-126">The name of the class or subclass used in the creation of this instance.</span></span>

</dd> <dt>

<span data-ttu-id="513fc-127">**DefaultFlowReservation**</span><span class="sxs-lookup"><span data-stu-id="513fc-127">**DefaultFlowReservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="513fc-128">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="513fc-128">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="513fc-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="513fc-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="513fc-130">Calificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="513fc-130">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="513fc-131">Ancho de banda absoluto actual reservado en el conmutador para el flujo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="513fc-131">The current absolute bandwidth reserved on the switch for default flow.</span></span>

</dd> <dt>

<span data-ttu-id="513fc-132">**DefaultFlowReservationPercentage**</span><span class="sxs-lookup"><span data-stu-id="513fc-132">**DefaultFlowReservationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="513fc-133">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="513fc-133">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="513fc-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="513fc-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="513fc-135">Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="513fc-135">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="513fc-136">Porcentaje actual de ancho de banda reservado en el conmutador para el flujo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="513fc-136">The current percentage of bandwidth reserved on the switch for default flow.</span></span>

</dd> <dt>

<span data-ttu-id="513fc-137">**DefaultFlowWeight**</span><span class="sxs-lookup"><span data-stu-id="513fc-137">**DefaultFlowWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="513fc-138">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="513fc-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="513fc-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="513fc-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="513fc-140">Calificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="513fc-140">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="513fc-141">Peso actual del flujo predeterminado en el modificador.</span><span class="sxs-lookup"><span data-stu-id="513fc-141">The current weight for the default flow on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="513fc-142">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="513fc-142">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="513fc-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="513fc-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="513fc-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="513fc-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="513fc-145">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="513fc-145">A description of the object.</span></span> <span data-ttu-id="513fc-146">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="513fc-146">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="513fc-147">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="513fc-147">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="513fc-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="513fc-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="513fc-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="513fc-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="513fc-150">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="513fc-150">A display name for the object.</span></span> <span data-ttu-id="513fc-151">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="513fc-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="513fc-152">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="513fc-152">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="513fc-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="513fc-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="513fc-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="513fc-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="513fc-155">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="513fc-155">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="513fc-156">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="513fc-156">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="513fc-157">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="513fc-157">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="513fc-158">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="513fc-158">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="513fc-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="513fc-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="513fc-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="513fc-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="513fc-161">Calificadores: **clave**, **invalidación**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="513fc-161">Qualifiers: **Key**, **Override**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="513fc-162">Nombre único del recurso.</span><span class="sxs-lookup"><span data-stu-id="513fc-162">The unique name of the resource.</span></span>

</dd> <dt>

<span data-ttu-id="513fc-163">**Reserva**</span><span class="sxs-lookup"><span data-stu-id="513fc-163">**Reservation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="513fc-164">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="513fc-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="513fc-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="513fc-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="513fc-166">Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="513fc-166">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="513fc-167">Ancho de banda actual reservado en el conmutador.</span><span class="sxs-lookup"><span data-stu-id="513fc-167">The current bandwidth reserved on the switch.</span></span>

</dd> <dt>

<span data-ttu-id="513fc-168">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="513fc-168">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="513fc-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="513fc-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="513fc-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="513fc-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="513fc-171">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="513fc-171">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="513fc-172">Nombre de la clase de creación del sistema de hospedaje.</span><span class="sxs-lookup"><span data-stu-id="513fc-172">The hosting system's creation class name.</span></span> <span data-ttu-id="513fc-173">Esta propiedad se hereda del [**\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service).</span><span class="sxs-lookup"><span data-stu-id="513fc-173">This property is inherited from [**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service).</span></span>

</dd> <dt>

<span data-ttu-id="513fc-174">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="513fc-174">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="513fc-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="513fc-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="513fc-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="513fc-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="513fc-177">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="513fc-177">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="513fc-178">El nombre del conmutador virtual al que está enlazada la instancia de recurso asociada.</span><span class="sxs-lookup"><span data-stu-id="513fc-178">The name of the virtual switch to which the associated resource instance is bound.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="513fc-179">Requisitos</span><span class="sxs-lookup"><span data-stu-id="513fc-179">Requirements</span></span>



| <span data-ttu-id="513fc-180">Requisito</span><span class="sxs-lookup"><span data-stu-id="513fc-180">Requirement</span></span> | <span data-ttu-id="513fc-181">Value</span><span class="sxs-lookup"><span data-stu-id="513fc-181">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="513fc-182">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="513fc-182">Minimum supported client</span></span><br/> | <span data-ttu-id="513fc-183">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="513fc-183">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="513fc-184">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="513fc-184">Minimum supported server</span></span><br/> | <span data-ttu-id="513fc-185">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="513fc-185">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="513fc-186">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="513fc-186">Namespace</span></span><br/>                | <span data-ttu-id="513fc-187">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="513fc-187">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="513fc-188">MOF</span><span class="sxs-lookup"><span data-stu-id="513fc-188">MOF</span></span><br/>                      | <dl> <span data-ttu-id="513fc-189"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="513fc-189"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="513fc-190">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="513fc-190">DLL</span></span><br/>                      | <dl> <span data-ttu-id="513fc-191"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="513fc-191"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

