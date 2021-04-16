---
description: Representa la configuración para la asignación del puerto Ethernet, además de los valores proporcionados por la \_ clase EthernetPort de CIM. Esta configuración se usa para proporcionar información específica del propio recurso.
ms.assetid: f59ebaf1-60dd-49bd-b48e-d7a6c2650909
title: CIM_EthernetPortAllocationSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPortAllocationSettingData
- CIM_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- CIM_EthernetPortAllocationSettingData.OtherEndpointMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e77b4387f77e88ceaff273b8be72a354c989e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686516"
---
# <a name="cim_ethernetportallocationsettingdata-class"></a><span data-ttu-id="4d1b2-104">\_Clase EthernetPortAllocationSettingData de CIM</span><span class="sxs-lookup"><span data-stu-id="4d1b2-104">CIM\_EthernetPortAllocationSettingData class</span></span>

<span data-ttu-id="4d1b2-105">Representa la configuración para la asignación del puerto Ethernet, además de los valores proporcionados por la [**clase \_ EthernetPort de CIM**](cim-ethernetport.md) .</span><span class="sxs-lookup"><span data-stu-id="4d1b2-105">Represents settings for the allocation of the ethernet port, in addition to the settings provided by the [**CIM\_EthernetPort**](cim-ethernetport.md) class.</span></span> <span data-ttu-id="4d1b2-106">Esta configuración se usa para proporcionar información específica del propio recurso.</span><span class="sxs-lookup"><span data-stu-id="4d1b2-106">These settings are used to provide information specific to the resource itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d1b2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4d1b2-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_EthernetPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint16 DesiredVLANEndpointMode;
  string OtherEndpointMode;
};
```

## <a name="members"></a><span data-ttu-id="4d1b2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="4d1b2-108">Members</span></span>

<span data-ttu-id="4d1b2-109">La clase **CIM \_ EthernetPortAllocationSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4d1b2-109">The **CIM\_EthernetPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="4d1b2-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d1b2-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4d1b2-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4d1b2-111">Properties</span></span>

<span data-ttu-id="4d1b2-112">La clase **CIM \_ EthernetPortAllocationSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4d1b2-112">The **CIM\_EthernetPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4d1b2-113">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-113">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d1b2-114">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="4d1b2-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d1b2-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d1b2-116">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**","**\_ VLANEndpoint CIM**.**DesiredEndpointMode**","**\_ EthernetPortAllocationSettingData CIM**.**OtherEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="4d1b2-116">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**", "**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_EthernetPortAllocationSettingData**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="4d1b2-117">El modo de VLAN solicitado.</span><span class="sxs-lookup"><span data-stu-id="4d1b2-117">The requested VLAN mode.</span></span> <span data-ttu-id="4d1b2-118">Esta propiedad se usa para establecer el valor de la propiedad **OperationalEndpointMode** inicial en la instancia de **\_ VLANEndpoint de CIM** asociada con el puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="4d1b2-118">This property is used to set the initial **OperationalEndpointMode** property value in the instance of **CIM\_VLANEndpoint** associated with the ethernet port.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4d1b2-119">**DMTF reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="4d1b2-119">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="4d1b2-120">**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="4d1b2-120">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="4d1b2-121">**Acceso** (2)</span><span class="sxs-lookup"><span data-stu-id="4d1b2-121">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="4d1b2-122">**Dynamic Auto** (3)</span><span class="sxs-lookup"><span data-stu-id="4d1b2-122">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="4d1b2-123">**Deseable dinámico** (4)</span><span class="sxs-lookup"><span data-stu-id="4d1b2-123">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="4d1b2-124">**Tronco** (5)</span><span class="sxs-lookup"><span data-stu-id="4d1b2-124">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="4d1b2-125">**Túnel Dot1Q** (6)</span><span class="sxs-lookup"><span data-stu-id="4d1b2-125">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="4d1b2-126">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="4d1b2-126">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="4d1b2-127">**Proveedor reservado** (0x8000... 0XFFFF</span><span class="sxs-lookup"><span data-stu-id="4d1b2-127">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="4d1b2-128">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-128">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4d1b2-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4d1b2-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4d1b2-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4d1b2-131">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EthernetPortAllocationSettingData**.**DesiredVLANEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="4d1b2-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPortAllocationSettingData**.**DesiredVLANEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="4d1b2-132">El tipo de modelo de punto de conexión de VLAN que es compatible con este extremo de VLAN, cuando el valor de la propiedad Mode está establecido en "1" (otro).</span><span class="sxs-lookup"><span data-stu-id="4d1b2-132">The type of VLAN endpoint model that is supported by this VLAN endpoint, when the value of the mode property is set to "1" (Other).</span></span> <span data-ttu-id="4d1b2-133">Esta propiedad debe establecerse en **null** cuando la propiedad de modo es cualquier valor distinto de "1".</span><span class="sxs-lookup"><span data-stu-id="4d1b2-133">This property should be set to **NULL** when the mode property is any value other than "1".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4d1b2-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4d1b2-134">Requirements</span></span>



| <span data-ttu-id="4d1b2-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="4d1b2-135">Requirement</span></span> | <span data-ttu-id="4d1b2-136">Value</span><span class="sxs-lookup"><span data-stu-id="4d1b2-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d1b2-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d1b2-137">Minimum supported client</span></span><br/> | <span data-ttu-id="4d1b2-138">Windows 8</span><span class="sxs-lookup"><span data-stu-id="4d1b2-138">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="4d1b2-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4d1b2-139">Minimum supported server</span></span><br/> | <span data-ttu-id="4d1b2-140">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4d1b2-140">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="4d1b2-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4d1b2-141">Namespace</span></span><br/>                | <span data-ttu-id="4d1b2-142">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="4d1b2-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="4d1b2-143">MOF</span><span class="sxs-lookup"><span data-stu-id="4d1b2-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d1b2-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d1b2-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d1b2-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4d1b2-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d1b2-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="4d1b2-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="4d1b2-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="4d1b2-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d1b2-148">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="4d1b2-148">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

