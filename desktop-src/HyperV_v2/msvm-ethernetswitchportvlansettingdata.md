---
description: Representa los datos de configuración de LAN virtual (VLAN).
ms.assetid: c3a49021-5256-4751-a5a5-81bf1c6d6e6d
title: Msvm_EthernetSwitchPortVlanSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortVlanSettingData
- Msvm_EthernetSwitchPortVlanSettingData.InstanceID
- Msvm_EthernetSwitchPortVlanSettingData.Caption
- Msvm_EthernetSwitchPortVlanSettingData.Description
- Msvm_EthernetSwitchPortVlanSettingData.ElementName
- Msvm_EthernetSwitchPortVlanSettingData.OperationMode
- Msvm_EthernetSwitchPortVlanSettingData.AccessVlanId
- Msvm_EthernetSwitchPortVlanSettingData.NativeVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PvlanMode
- Msvm_EthernetSwitchPortVlanSettingData.PrimaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanId
- Msvm_EthernetSwitchPortVlanSettingData.PruneVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.TrunkVlanIdArray
- Msvm_EthernetSwitchPortVlanSettingData.SecondaryVlanIdArray
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6fce6416696a99e5d928b774e2ba2a05b1dc21d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105670021"
---
# <a name="msvm_ethernetswitchportvlansettingdata-class"></a><span data-ttu-id="13eee-103">MSVM \_ EthernetSwitchPortVlanSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="13eee-103">Msvm\_EthernetSwitchPortVlanSettingData class</span></span>

<span data-ttu-id="13eee-104">Representa los datos de configuración de LAN virtual (VLAN).</span><span class="sxs-lookup"><span data-stu-id="13eee-104">Represents the virtual LAN (VLAN) setting data.</span></span>

<span data-ttu-id="13eee-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="13eee-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="13eee-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="13eee-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("952C5004-4465-451C-8CB8-FA9AB382B773"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port VLAN Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortVlanSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  string InstanceID;
  string Caption = "Ethernet Switch Port VLAN Settings";
  string Description = "Represents the vlan setting data.";
  string ElementName = "Ethernet Switch Port VLAN Settings";
  uint32 OperationMode = 0;
  uint16 AccessVlanId = 0;
  uint16 NativeVlanId = 0;
  uint32 PvlanMode = 0;
  uint16 PrimaryVlanId = 0;
  uint16 SecondaryVlanId = 0;
  uint16 PruneVlanIdArray[] = {};
  uint16 TrunkVlanIdArray[] = {};
  uint16 SecondaryVlanIdArray[] = {};
};
```

## <a name="members"></a><span data-ttu-id="13eee-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="13eee-107">Members</span></span>

<span data-ttu-id="13eee-108">La clase **MSVM \_ EthernetSwitchPortVlanSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="13eee-108">The **Msvm\_EthernetSwitchPortVlanSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="13eee-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="13eee-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="13eee-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="13eee-110">Properties</span></span>

<span data-ttu-id="13eee-111">La clase **MSVM \_ EthernetSwitchPortVlanSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="13eee-111">The **Msvm\_EthernetSwitchPortVlanSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="13eee-112">**AccessVlanId**</span><span class="sxs-lookup"><span data-stu-id="13eee-112">**AccessVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eee-113">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13eee-113">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13eee-114">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="13eee-114">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="13eee-115">Calificadores: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="13eee-115">Qualifiers: **WmiDataId** (2), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="13eee-116">Especifica el identificador de VLAN en modo de acceso.</span><span class="sxs-lookup"><span data-stu-id="13eee-116">Specifies the VLAN identifier in access mode.</span></span>

</dd> <dt>

<span data-ttu-id="13eee-117">**Caption**</span><span class="sxs-lookup"><span data-stu-id="13eee-117">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eee-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="13eee-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eee-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13eee-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13eee-120">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="13eee-120">A short description of the object.</span></span> <span data-ttu-id="13eee-121">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración de VLAN del puerto del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="13eee-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port VLAN Settings".</span></span>

</dd> <dt>

<span data-ttu-id="13eee-122">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="13eee-122">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eee-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="13eee-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eee-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13eee-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13eee-125">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="13eee-125">A description of the object.</span></span> <span data-ttu-id="13eee-126">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre está establecida en "representa los datos de configuración de VLAN".</span><span class="sxs-lookup"><span data-stu-id="13eee-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Represents the vlan setting data.".</span></span>

</dd> <dt>

<span data-ttu-id="13eee-127">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="13eee-127">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eee-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="13eee-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eee-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13eee-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="13eee-130">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="13eee-130">A display name for the object.</span></span> <span data-ttu-id="13eee-131">Esta propiedad se hereda de [**la \_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)y siempre se establece en "configuración de VLAN del puerto del conmutador Ethernet".</span><span class="sxs-lookup"><span data-stu-id="13eee-131">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement), and it is always set to "Ethernet Switch Port VLAN Settings".</span></span>

</dd> <dt>

<span data-ttu-id="13eee-132">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="13eee-132">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eee-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="13eee-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="13eee-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="13eee-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="13eee-135">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="13eee-135">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="13eee-136">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="13eee-136">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="13eee-137">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="13eee-137">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="13eee-138">**NativeVlanId**</span><span class="sxs-lookup"><span data-stu-id="13eee-138">**NativeVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eee-139">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13eee-139">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13eee-140">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="13eee-140">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="13eee-141">Calificadores: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="13eee-141">Qualifiers: **WmiDataId** (3), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="13eee-142">Especifica el identificador de VLAN en el modo de tronco.</span><span class="sxs-lookup"><span data-stu-id="13eee-142">Specifies the VLAN identifier in trunk mode.</span></span>

</dd> <dt>

<span data-ttu-id="13eee-143">**OperationMode**</span><span class="sxs-lookup"><span data-stu-id="13eee-143">**OperationMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eee-144">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13eee-144">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13eee-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="13eee-145">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="13eee-146">Calificadores: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="13eee-146">Qualifiers: **WmiDataId** (1), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="13eee-147">Especifica el modo de operación de VLAN.</span><span class="sxs-lookup"><span data-stu-id="13eee-147">Specifies the VLAN operation mode.</span></span>

<dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="13eee-148">**Acceso** (1)</span><span class="sxs-lookup"><span data-stu-id="13eee-148">**Access** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="13eee-149">**Tronco** (2)</span><span class="sxs-lookup"><span data-stu-id="13eee-149">**Trunk** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Private"></span><span id="private"></span><span id="PRIVATE"></span>

<span data-ttu-id="13eee-150">**Privado** (3)</span><span class="sxs-lookup"><span data-stu-id="13eee-150">**Private** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13eee-151">**PrimaryVlanId**</span><span class="sxs-lookup"><span data-stu-id="13eee-151">**PrimaryVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eee-152">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13eee-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13eee-153">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="13eee-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="13eee-154">Calificadores: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="13eee-154">Qualifiers: **WmiDataId** (5), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="13eee-155">Especifica el identificador de VLAN principal en modo privado.</span><span class="sxs-lookup"><span data-stu-id="13eee-155">Specifies the primary VLAN identifier in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="13eee-156">**PruneVlanIdArray**</span><span class="sxs-lookup"><span data-stu-id="13eee-156">**PruneVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eee-157">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13eee-157">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="13eee-158">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="13eee-158">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="13eee-159">Calificadores: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="13eee-159">Qualifiers: **WmiDataId** (7), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="13eee-160">Especifica el mapa de bits de la eliminación del identificador de VLAN en el modo de tronco.</span><span class="sxs-lookup"><span data-stu-id="13eee-160">Specifies the prune VLAN identifier bitmap in trunk mode.</span></span>

</dd> <dt>

<span data-ttu-id="13eee-161">**PvlanMode**</span><span class="sxs-lookup"><span data-stu-id="13eee-161">**PvlanMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eee-162">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="13eee-162">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="13eee-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="13eee-163">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="13eee-164">Calificadores: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="13eee-164">Qualifiers: **WmiDataId** (4), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="13eee-165">Especifica el modo de VLAN privada.</span><span class="sxs-lookup"><span data-stu-id="13eee-165">Specifies the private VLAN mode.</span></span>

<dt>

<span id="Isolated"></span><span id="isolated"></span><span id="ISOLATED"></span>

<span data-ttu-id="13eee-166">**Aislado** (1)</span><span class="sxs-lookup"><span data-stu-id="13eee-166">**Isolated** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Community"></span><span id="community"></span><span id="COMMUNITY"></span>

<span data-ttu-id="13eee-167">**Comunidad** (2)</span><span class="sxs-lookup"><span data-stu-id="13eee-167">**Community** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Promiscuous"></span><span id="promiscuous"></span><span id="PROMISCUOUS"></span>

<span data-ttu-id="13eee-168">**Promiscuo** (3)</span><span class="sxs-lookup"><span data-stu-id="13eee-168">**Promiscuous** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="13eee-169">**SecondaryVlanId**</span><span class="sxs-lookup"><span data-stu-id="13eee-169">**SecondaryVlanId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eee-170">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13eee-170">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="13eee-171">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="13eee-171">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="13eee-172">Calificadores: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="13eee-172">Qualifiers: **WmiDataId** (6), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="13eee-173">Especifica el identificador de VLAN secundario en modo privado.</span><span class="sxs-lookup"><span data-stu-id="13eee-173">Specifies the secondary VLAN identifier in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="13eee-174">**SecondaryVlanIdArray**</span><span class="sxs-lookup"><span data-stu-id="13eee-174">**SecondaryVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eee-175">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13eee-175">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="13eee-176">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="13eee-176">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="13eee-177">Calificadores: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="13eee-177">Qualifiers: **WmiDataId** (9), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="13eee-178">Especifica el mapa de bits del identificador de VLAN secundario en modo privado.</span><span class="sxs-lookup"><span data-stu-id="13eee-178">Specifies the secondary VLAN identifier bitmap in private mode.</span></span>

</dd> <dt>

<span data-ttu-id="13eee-179">**TrunkVlanIdArray**</span><span class="sxs-lookup"><span data-stu-id="13eee-179">**TrunkVlanIdArray**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="13eee-180">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="13eee-180">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="13eee-181">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="13eee-181">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="13eee-182">Calificadores: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span><span class="sxs-lookup"><span data-stu-id="13eee-182">Qualifiers: **WmiDataId** (8), **InterfaceVersion** (1), **InterfaceRevision** (0)</span></span>
</dt> </dl>

<span data-ttu-id="13eee-183">Especifica el mapa de bits del identificador de VLAN de tronco en el modo de tronco.</span><span class="sxs-lookup"><span data-stu-id="13eee-183">Specifies the trunk VLAN identifier bitmap in trunk mode.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13eee-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13eee-184">Requirements</span></span>



| <span data-ttu-id="13eee-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="13eee-185">Requirement</span></span> | <span data-ttu-id="13eee-186">Value</span><span class="sxs-lookup"><span data-stu-id="13eee-186">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13eee-187">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13eee-187">Minimum supported client</span></span><br/> | <span data-ttu-id="13eee-188">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="13eee-188">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="13eee-189">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13eee-189">Minimum supported server</span></span><br/> | <span data-ttu-id="13eee-190">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="13eee-190">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="13eee-191">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="13eee-191">Namespace</span></span><br/>                | <span data-ttu-id="13eee-192">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="13eee-192">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="13eee-193">MOF</span><span class="sxs-lookup"><span data-stu-id="13eee-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13eee-194"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="13eee-194"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="13eee-195">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="13eee-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13eee-196"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="13eee-196"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

