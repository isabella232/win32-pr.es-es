---
description: Representa los datos de estado de la característica de ancho de banda de puerto.
ms.assetid: 1f7be0dd-3d2f-49ef-aff0-cb162389194a
title: Msvm_EthernetSwitchPortBandwidthData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortBandwidthData
- Msvm_EthernetSwitchPortBandwidthData.InstanceID
- Msvm_EthernetSwitchPortBandwidthData.Caption
- Msvm_EthernetSwitchPortBandwidthData.Description
- Msvm_EthernetSwitchPortBandwidthData.ElementName
- Msvm_EthernetSwitchPortBandwidthData.SystemCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.SystemName
- Msvm_EthernetSwitchPortBandwidthData.DeviceCreationClassName
- Msvm_EthernetSwitchPortBandwidthData.DeviceID
- Msvm_EthernetSwitchPortBandwidthData.CreationClassName
- Msvm_EthernetSwitchPortBandwidthData.Name
- Msvm_EthernetSwitchPortBandwidthData.CurrentBandwidthReservationPercentage
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 55e8ad735d712bdd388e42b1f4174ee1a78af184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666678"
---
# <a name="msvm_ethernetswitchportbandwidthdata-class"></a><span data-ttu-id="ccd34-103">MSVM \_ EthernetSwitchPortBandwidthData (clase)</span><span class="sxs-lookup"><span data-stu-id="ccd34-103">Msvm\_EthernetSwitchPortBandwidthData class</span></span>

<span data-ttu-id="ccd34-104">Representa los datos de estado de la característica de ancho de banda de puerto.</span><span class="sxs-lookup"><span data-stu-id="ccd34-104">Represents the port bandwidth feature status data.</span></span>

<span data-ttu-id="ccd34-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ccd34-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ccd34-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ccd34-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("24AD3CE1-69BD-4978-B2AC-DAAD389D699C"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Bandwidth Feature Status"), AMENDMENT]
class Msvm_EthernetSwitchPortBandwidthData : Msvm_EthernetPortData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port Bandwidth Feature Status";
  string Description = "Represents the port bandwidth feature status data.";
  string ElementName = "Ethernet Switch Port Bandwidth Feature Status";
  string SystemCreationClassName = "Msvm_VirtualEthernetSwitch";
  string SystemName;
  string DeviceCreationClassName = "Msvm_EthernetSwitchPort";
  string DeviceID;
  string CreationClassName = "Msvm_EthernetSwitchPortBandwidthData";
  string Name;
  uint32 CurrentBandwidthReservationPercentage = 0;
};
```

## <a name="members"></a><span data-ttu-id="ccd34-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ccd34-107">Members</span></span>

<span data-ttu-id="ccd34-108">La clase **MSVM \_ EthernetSwitchPortBandwidthData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ccd34-108">The **Msvm\_EthernetSwitchPortBandwidthData** class has these types of members:</span></span>

-   [<span data-ttu-id="ccd34-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ccd34-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ccd34-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ccd34-110">Properties</span></span>

<span data-ttu-id="ccd34-111">La clase **MSVM \_ EthernetSwitchPortBandwidthData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ccd34-111">The **Msvm\_EthernetSwitchPortBandwidthData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ccd34-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="ccd34-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccd34-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ccd34-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ccd34-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccd34-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ccd34-115">A short description of the object.</span></span> <span data-ttu-id="ccd34-116">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "estado de la característica de ancho de banda del puerto del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="ccd34-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="ccd34-117">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ccd34-117">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccd34-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ccd34-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ccd34-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-120">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="ccd34-120">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="ccd34-121">Nombre de la subclase utilizada en la creación de esta instancia de datos de puerto.</span><span class="sxs-lookup"><span data-stu-id="ccd34-121">The name of the subclass used in the creation of this port data instance.</span></span> <span data-ttu-id="ccd34-122">Esta propiedad se hereda de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)y siempre se establece en "MSVM \_ EthernetSwitchPortBandwidthData".</span><span class="sxs-lookup"><span data-stu-id="ccd34-122">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPortBandwidthData".</span></span>

</dd> <dt>

<span data-ttu-id="ccd34-123">**CurrentBandwidthReservationPercentage**</span><span class="sxs-lookup"><span data-stu-id="ccd34-123">**CurrentBandwidthReservationPercentage**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccd34-124">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ccd34-124">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="ccd34-125">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-126">Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="ccd34-126">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="ccd34-127">Porcentaje actual de ancho de banda reservado para este puerto.</span><span class="sxs-lookup"><span data-stu-id="ccd34-127">The current percentage of bandwidth reserved for this port.</span></span>

</dd> <dt>

<span data-ttu-id="ccd34-128">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="ccd34-128">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccd34-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ccd34-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ccd34-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccd34-131">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="ccd34-131">A description of the object.</span></span> <span data-ttu-id="ccd34-132">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "representa los datos de estado de la característica de ancho de banda de puerto".</span><span class="sxs-lookup"><span data-stu-id="ccd34-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the port bandwidth feature status data.".</span></span>

</dd> <dt>

<span data-ttu-id="ccd34-133">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ccd34-133">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccd34-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ccd34-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ccd34-135">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-136">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="ccd34-136">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="ccd34-137">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="ccd34-137">The scoping system's creation class name.</span></span> <span data-ttu-id="ccd34-138">Esta propiedad se hereda de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)y siempre se establece en "MSVM \_ EthernetSwitchPort".</span><span class="sxs-lookup"><span data-stu-id="ccd34-138">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_EthernetSwitchPort".</span></span>

</dd> <dt>

<span data-ttu-id="ccd34-139">**ID**</span><span class="sxs-lookup"><span data-stu-id="ccd34-139">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccd34-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ccd34-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ccd34-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-142">Calificadores: **clave**, **MaxLen** (64)</span><span class="sxs-lookup"><span data-stu-id="ccd34-142">Qualifiers: **Key**, **MaxLen** ( 64 )</span></span>
</dt> </dl>

<span data-ttu-id="ccd34-143">El ID. de dispositivo del puerto que limita esta instancia de datos del puerto.</span><span class="sxs-lookup"><span data-stu-id="ccd34-143">The Device ID of the port that scopes this port data instance.</span></span> <span data-ttu-id="ccd34-144">Esta propiedad se hereda de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="ccd34-144">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="ccd34-145">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="ccd34-145">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccd34-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ccd34-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ccd34-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ccd34-148">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="ccd34-148">A display name for the object.</span></span> <span data-ttu-id="ccd34-149">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "estado de la característica de ancho de banda del puerto del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="ccd34-149">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port Bandwidth Feature Status".</span></span>

</dd> <dt>

<span data-ttu-id="ccd34-150">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="ccd34-150">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccd34-151">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ccd34-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-152">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ccd34-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-153">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="ccd34-153">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="ccd34-154">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="ccd34-154">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="ccd34-155">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="ccd34-155">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="ccd34-156">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="ccd34-156">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccd34-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ccd34-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ccd34-158">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-159">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="ccd34-159">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="ccd34-160">Cadena que identifica de forma única esta instancia de datos de puerto en el ámbito del modificador y el puerto.</span><span class="sxs-lookup"><span data-stu-id="ccd34-160">A string that uniquely identifies this port data instance within the scope of the switch and port.</span></span> <span data-ttu-id="ccd34-161">Esta propiedad se hereda de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="ccd34-161">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="ccd34-162">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="ccd34-162">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccd34-163">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ccd34-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-164">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ccd34-164">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-165">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="ccd34-165">Qualifiers: **Key**, **MaxLen** (256)</span></span>
</dt> </dl>

<span data-ttu-id="ccd34-166">Nombre de la clase de creación del sistema de ámbito.</span><span class="sxs-lookup"><span data-stu-id="ccd34-166">The scoping system's creation class name.</span></span> <span data-ttu-id="ccd34-167">Esta propiedad se hereda de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md)y siempre se establece en "MSVM \_ VirtualEthernetSwitch".</span><span class="sxs-lookup"><span data-stu-id="ccd34-167">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md), and it is always set to "Msvm\_VirtualEthernetSwitch".</span></span>

</dd> <dt>

<span data-ttu-id="ccd34-168">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="ccd34-168">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ccd34-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="ccd34-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ccd34-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ccd34-171">Calificadores: **clave**, **MaxLen** (256)</span><span class="sxs-lookup"><span data-stu-id="ccd34-171">Qualifiers: **Key**, **MaxLen** ( 256 )</span></span>
</dt> </dl>

<span data-ttu-id="ccd34-172">El nombre del conmutador virtual que limita esta instancia de datos de puerto.</span><span class="sxs-lookup"><span data-stu-id="ccd34-172">The name of the virtual switch that scopes this port data instance.</span></span> <span data-ttu-id="ccd34-173">Esta propiedad se hereda de [**MSVM \_ EthernetPortData**](msvm-ethernetportdata.md).</span><span class="sxs-lookup"><span data-stu-id="ccd34-173">This property is inherited from [**Msvm\_EthernetPortData**](msvm-ethernetportdata.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ccd34-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccd34-174">Requirements</span></span>



| <span data-ttu-id="ccd34-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccd34-175">Requirement</span></span> | <span data-ttu-id="ccd34-176">Value</span><span class="sxs-lookup"><span data-stu-id="ccd34-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ccd34-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccd34-177">Minimum supported client</span></span><br/> | <span data-ttu-id="ccd34-178">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ccd34-178">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ccd34-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccd34-179">Minimum supported server</span></span><br/> | <span data-ttu-id="ccd34-180">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ccd34-180">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ccd34-181">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ccd34-181">Namespace</span></span><br/>                | <span data-ttu-id="ccd34-182">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ccd34-182">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ccd34-183">MOF</span><span class="sxs-lookup"><span data-stu-id="ccd34-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ccd34-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ccd34-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ccd34-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ccd34-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ccd34-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ccd34-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

