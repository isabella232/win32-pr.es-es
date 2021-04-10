---
description: Un punto de conexión en un conmutador o estación final que se asigna a una VLAN, o acepta tráfico de una o varias VLAN.
ms.assetid: 20943be3-35c3-4bf5-8f1a-d4095fa6897e
title: CIM_VLANEndpoint (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpoint
- CIM_VLANEndpoint.DesiredEndpointMode
- CIM_VLANEndpoint.OtherEndpointMode
- CIM_VLANEndpoint.OperationalEndpointMode
- CIM_VLANEndpoint.DesiredVLANTrunkEncapsulation
- CIM_VLANEndpoint.OtherTrunkEncapsulation
- CIM_VLANEndpoint.OperationalVLANTrunkEncapsulation
- CIM_VLANEndpoint.GVRPStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f7b0d1318e4c24ab7381032877d16a8ea83868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153749"
---
# <a name="cim_vlanendpoint-class"></a><span data-ttu-id="307d4-103">\_Clase VLANEndpoint de CIM</span><span class="sxs-lookup"><span data-stu-id="307d4-103">CIM\_VLANEndpoint class</span></span>

<span data-ttu-id="307d4-104">Un punto de conexión en un conmutador o estación final que se asigna a una VLAN, o acepta tráfico de una o varias VLAN.</span><span class="sxs-lookup"><span data-stu-id="307d4-104">An endpoint on a switch or end station that is assigned to a VLAN, or accepts traffic from one or more VLANs.</span></span>

## <a name="syntax"></a><span data-ttu-id="307d4-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="307d4-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Network::VLAN"), AMENDMENT]
class CIM_VLANEndpoint : CIM_ProtocolEndpoint
{
  uint16 DesiredEndpointMode;
  string OtherEndpointMode;
  uint16 OperationalEndpointMode;
  uint16 DesiredVLANTrunkEncapsulation;
  string OtherTrunkEncapsulation;
  uint16 OperationalVLANTrunkEncapsulation;
  uint16 GVRPStatus;
};
```

## <a name="members"></a><span data-ttu-id="307d4-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="307d4-106">Members</span></span>

<span data-ttu-id="307d4-107">La clase **CIM \_ VLANEndpoint** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="307d4-107">The **CIM\_VLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="307d4-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="307d4-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="307d4-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="307d4-109">Properties</span></span>

<span data-ttu-id="307d4-110">La clase **CIM \_ VLANEndpoint** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="307d4-110">The **CIM\_VLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="307d4-111">**DesiredEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="307d4-111">**DesiredEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="307d4-112">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="307d4-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="307d4-113">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="307d4-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="307d4-114">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OperationalEndpointMode**","**\_ VLANEndpoint CIM**.**OtherEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="307d4-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OperationalEndpointMode**", "**CIM\_VLANEndpoint**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="307d4-115">El modo VLAN solicitado para el extremo.</span><span class="sxs-lookup"><span data-stu-id="307d4-115">The requested VLAN mode for the endpoint.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="307d4-116">**DMTF reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="307d4-116">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="307d4-117">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="307d4-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="307d4-118">**Acceso** (2)</span><span class="sxs-lookup"><span data-stu-id="307d4-118">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="307d4-119">**Dynamic Auto** (3)</span><span class="sxs-lookup"><span data-stu-id="307d4-119">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="307d4-120">**Deseable dinámico** (4)</span><span class="sxs-lookup"><span data-stu-id="307d4-120">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="307d4-121">**Tronco** (5)</span><span class="sxs-lookup"><span data-stu-id="307d4-121">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="307d4-122">**Túnel Dot1Q** (6)</span><span class="sxs-lookup"><span data-stu-id="307d4-122">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="307d4-123">**DMTF reservado** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="307d4-123">**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="307d4-124">**Proveedor reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="307d4-124">**Vendor Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="307d4-125">**DesiredVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="307d4-125">**DesiredVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="307d4-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="307d4-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="307d4-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="307d4-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="307d4-128">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VLANEndpointCapabilities. SupportsTrunkEncapsulationNegotiation", "**CIM \_ VLANEndpoint**.**OperationalVLANTrunkEncapsulation**","**\_ VLANEndpoint CIM**.**OtherTrunkEncapsulation**")</span><span class="sxs-lookup"><span data-stu-id="307d4-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VLANEndpointCapabilities.SupportsTrunkEncapsulationNegotiation", "**CIM\_VLANEndpoint**.**OperationalVLANTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**OtherTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="307d4-129">El tipo de encapsulación de VLAN solicitado.</span><span class="sxs-lookup"><span data-stu-id="307d4-129">The requested VLAN encapsulation type.</span></span>

> [!Note]  
> <span data-ttu-id="307d4-130">Esta propiedad solo se usa cuando el extremo de la VLAN está en modo de tronco.</span><span class="sxs-lookup"><span data-stu-id="307d4-130">This property is only used when the VLAN endpoint is in trunking mode.</span></span>

 

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="307d4-131">**DMTF reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="307d4-131">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="307d4-132">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="307d4-132">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="307d4-133">**No aplicable** (2)</span><span class="sxs-lookup"><span data-stu-id="307d4-133">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

<span data-ttu-id="307d4-134">**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="307d4-134">**802.1q** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

<span data-ttu-id="307d4-135">**ISL de Cisco** (4)</span><span class="sxs-lookup"><span data-stu-id="307d4-135">**Cisco ISL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="307d4-136">**Negotiate** (5)</span><span class="sxs-lookup"><span data-stu-id="307d4-136">**Negotiate** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="307d4-137">**DMTF reservado** (6.. 32767)</span><span class="sxs-lookup"><span data-stu-id="307d4-137">**DMTF Reserved** (6..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="307d4-138">**Proveedor reservado** (32768...)</span><span class="sxs-lookup"><span data-stu-id="307d4-138">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="307d4-139">**GVRPStatus**</span><span class="sxs-lookup"><span data-stu-id="307d4-139">**GVRPStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="307d4-140">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="307d4-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="307d4-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="307d4-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="307d4-142">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OperationalEndpointMode**, CIM \_ VLANEndpointCapabilities. Dot1QTagging ")</span><span class="sxs-lookup"><span data-stu-id="307d4-142">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OperationalEndpointMode**, CIM\_VLANEndpointCapabilities.Dot1QTagging")</span></span>
</dt> </dl>

<span data-ttu-id="307d4-143">Indica si el protocolo de registro de VLAN de GARP (GVRP) está habilitado o deshabilitado en el punto de conexión de tronco.</span><span class="sxs-lookup"><span data-stu-id="307d4-143">Indicates whether GARP VLAN Registration Protocol (GVRP) is enabled or disabled on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="307d4-144">Esta propiedad solo se utiliza cuando GVRP es compatible con el punto de conexión y está habilitado el modo de tronco.</span><span class="sxs-lookup"><span data-stu-id="307d4-144">This property is only used when GVRP is supported by the endpoint, and trunking mode is enabled.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="307d4-145">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="307d4-145">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="307d4-146">**No aplicable** (2)</span><span class="sxs-lookup"><span data-stu-id="307d4-146">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="307d4-147">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="307d4-147">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="307d4-148">**Deshabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="307d4-148">**Disabled** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="307d4-149">**OperationalEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="307d4-149">**OperationalEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="307d4-150">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="307d4-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="307d4-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="307d4-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="307d4-152">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredEndpointMode**","**\_ VLANEndpoint CIM**.**OtherEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="307d4-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_VLANEndpoint**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="307d4-153">El modo VLAN actual para el extremo.</span><span class="sxs-lookup"><span data-stu-id="307d4-153">The current VLAN mode for the endpoint.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="307d4-154">**DMTF reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="307d4-154">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="307d4-155">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="307d4-155">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="307d4-156">**Acceso** (2)</span><span class="sxs-lookup"><span data-stu-id="307d4-156">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="307d4-157">**Dynamic Auto** (3)</span><span class="sxs-lookup"><span data-stu-id="307d4-157">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="307d4-158">**Deseable dinámico** (4)</span><span class="sxs-lookup"><span data-stu-id="307d4-158">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="307d4-159">**Tronco** (5)</span><span class="sxs-lookup"><span data-stu-id="307d4-159">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="307d4-160">**Túnel Dot1Q** (6)</span><span class="sxs-lookup"><span data-stu-id="307d4-160">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="307d4-161">**DMTF reservado** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="307d4-161">**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="307d4-162">**Proveedor reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="307d4-162">**Vendor Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="307d4-163">**OperationalVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="307d4-163">**OperationalVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="307d4-164">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="307d4-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="307d4-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="307d4-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="307d4-166">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OtherTrunkEncapsulation**","**\_ VLANEndpoint CIM**.**DesiredVLANTrunkEncapsulation**")</span><span class="sxs-lookup"><span data-stu-id="307d4-166">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OtherTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**DesiredVLANTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="307d4-167">El tipo de encapsulación de VLAN actual.</span><span class="sxs-lookup"><span data-stu-id="307d4-167">The current VLAN encapsulation type.</span></span>

> [!Note]  
> <span data-ttu-id="307d4-168">Esta propiedad solo se usa cuando el extremo de la VLAN está en modo de tronco.</span><span class="sxs-lookup"><span data-stu-id="307d4-168">This property is only used when the VLAN endpoint is in trunking mode.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="307d4-169">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="307d4-169">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="307d4-170">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="307d4-170">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="307d4-171">**No aplicable** (2)</span><span class="sxs-lookup"><span data-stu-id="307d4-171">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

<span data-ttu-id="307d4-172">**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="307d4-172">**802.1q** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

<span data-ttu-id="307d4-173">**ISL de Cisco** (4)</span><span class="sxs-lookup"><span data-stu-id="307d4-173">**Cisco ISL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>

<span data-ttu-id="307d4-174">**Negociar** (5)</span><span class="sxs-lookup"><span data-stu-id="307d4-174">**Negotiating** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="307d4-175">**DMTF reservado** (6.. 32767)</span><span class="sxs-lookup"><span data-stu-id="307d4-175">**DMTF Reserved** (6..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="307d4-176">**Proveedor reservado** (32768...)</span><span class="sxs-lookup"><span data-stu-id="307d4-176">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="307d4-177">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="307d4-177">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="307d4-178">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="307d4-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="307d4-179">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="307d4-179">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="307d4-180">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredEndpointMode**","**\_ VLANEndpoint CIM**.**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="307d4-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_VLANEndpoint**.**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="307d4-181">El tipo de modelo de punto de conexión de VLAN que es compatible con VLANEndpoint cuando el valor de **DesiredEndpointMode** se establece en "1" (otro); de lo contrario, **es null**.</span><span class="sxs-lookup"><span data-stu-id="307d4-181">The type of VLAN endpoint model that is supported by the VLANEndpoint when the value of **DesiredEndpointMode** is set to "1" (other); otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="307d4-182">**OtherTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="307d4-182">**OtherTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="307d4-183">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="307d4-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="307d4-184">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="307d4-184">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="307d4-185">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredVLANTrunkEncapsulation**","**\_ VLANEndpoint CIM**.**OperationalVLANTrunkEncapsulation**")</span><span class="sxs-lookup"><span data-stu-id="307d4-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredVLANTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**OperationalVLANTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="307d4-186">El tipo de encapsulación de VLAN que es compatible con el punto de conexión de la VLAN cuando el valor de la propiedad **DesiredVLANTrunkEncapsulation** se establece en 1 (otro); de lo contrario, **es null**.</span><span class="sxs-lookup"><span data-stu-id="307d4-186">The type of VLAN encapsulation that is supported by the VLAN endpoint when the value of the **DesiredVLANTrunkEncapsulation** property is set to 1 (other); otherwise, **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="307d4-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="307d4-187">Requirements</span></span>



| <span data-ttu-id="307d4-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="307d4-188">Requirement</span></span> | <span data-ttu-id="307d4-189">Value</span><span class="sxs-lookup"><span data-stu-id="307d4-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="307d4-190">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="307d4-190">Minimum supported client</span></span><br/> | <span data-ttu-id="307d4-191">Windows 8</span><span class="sxs-lookup"><span data-stu-id="307d4-191">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="307d4-192">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="307d4-192">Minimum supported server</span></span><br/> | <span data-ttu-id="307d4-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="307d4-193">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="307d4-194">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="307d4-194">Namespace</span></span><br/>                | <span data-ttu-id="307d4-195">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="307d4-195">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="307d4-196">MOF</span><span class="sxs-lookup"><span data-stu-id="307d4-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="307d4-197"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="307d4-197"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="307d4-198">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="307d4-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="307d4-199"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="307d4-199"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="307d4-200">Vea también</span><span class="sxs-lookup"><span data-stu-id="307d4-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="307d4-201">**ProtocolEndpoint de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="307d4-201">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

