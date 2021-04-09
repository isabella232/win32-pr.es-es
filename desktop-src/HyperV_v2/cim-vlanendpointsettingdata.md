---
description: Representa los datos de configuración para un punto de conexión de VLAN.
ms.assetid: 5ef3cc55-cf27-40b4-9e94-2e2b42ca41c5
title: CIM_VLANEndpointSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpointSettingData
- CIM_VLANEndpointSettingData.PruneEligibleVLANList
- CIM_VLANEndpointSettingData.NativeVLAN
- CIM_VLANEndpointSettingData.DefaultVLAN
- CIM_VLANEndpointSettingData.TrunkedVLANList
- CIM_VLANEndpointSettingData.AccessVLAN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a510c4195c538ab9735e7544acec2c88beeaa1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913898"
---
# <a name="cim_vlanendpointsettingdata-class"></a><span data-ttu-id="b2e5b-103">\_Clase VLANEndpointSettingData de CIM</span><span class="sxs-lookup"><span data-stu-id="b2e5b-103">CIM\_VLANEndpointSettingData class</span></span>

<span data-ttu-id="b2e5b-104">Representa los datos de configuración para un punto de conexión de VLAN.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-104">Represents configuration data for a VLAN endpoint.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2e5b-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2e5b-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.11.0"), UMLPackagePath("CIM::Network::VLAN")]
class CIM_VLANEndpointSettingData : CIM_SettingData
{
  uint16 PruneEligibleVLANList[];
  uint16 NativeVLAN;
  uint16 DefaultVLAN;
  uint16 TrunkedVLANList[];
  uint16 AccessVLAN;
};
```

## <a name="members"></a><span data-ttu-id="b2e5b-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="b2e5b-106">Members</span></span>

<span data-ttu-id="b2e5b-107">La clase **CIM \_ VLANEndpointSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b2e5b-107">The **CIM\_VLANEndpointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="b2e5b-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b2e5b-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2e5b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b2e5b-109">Properties</span></span>

<span data-ttu-id="b2e5b-110">La clase **CIM \_ VLANEndpointSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-110">The **CIM\_VLANEndpointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2e5b-111">**AccessVLAN**</span><span class="sxs-lookup"><span data-stu-id="b2e5b-111">**AccessVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e5b-112">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2e5b-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b2e5b-113">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b2e5b-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b2e5b-114">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="b2e5b-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="b2e5b-115">La VLAN de acceso para el extremo.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-115">The access VLAN for the endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="b2e5b-116">**DefaultVLAN**</span><span class="sxs-lookup"><span data-stu-id="b2e5b-116">**DefaultVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e5b-117">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2e5b-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b2e5b-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b2e5b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b2e5b-119">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="b2e5b-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="b2e5b-120">El valor predeterminado de la VLAN nativa en el punto de conexión de tronco.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-120">The default value for the native VLAN on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="b2e5b-121">Esta propiedad solo se usa cuando el punto de conexión de VLAN está funcionando en modo de tronco, que se especifica en la propiedad **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="b2e5b-121">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="b2e5b-122">**NativeVLAN**</span><span class="sxs-lookup"><span data-stu-id="b2e5b-122">**NativeVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e5b-123">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2e5b-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b2e5b-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b2e5b-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b2e5b-125">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="b2e5b-125">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="b2e5b-126">El identificador de VLAN que se usa para etiquetar el tráfico no etiquetado recibido en el punto de conexión de tronco.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-126">The VLAN ID that is used to tag untagged traffic received on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="b2e5b-127">Esta propiedad solo se usa cuando el punto de conexión de VLAN está funcionando en modo de tronco, que se especifica en la propiedad **SwitchEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="b2e5b-127">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **SwitchEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="b2e5b-128">**PruneEligibleVLANList**</span><span class="sxs-lookup"><span data-stu-id="b2e5b-128">**PruneEligibleVLANList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e5b-129">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2e5b-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b2e5b-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b2e5b-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b2e5b-131">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="b2e5b-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="b2e5b-132">Una matriz que contiene los identificadores de VLAN que el sistema puede quitar del punto de conexión de tronco.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-132">An array that contains IDs of VLANs that the system may remove from the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="b2e5b-133">Esta propiedad solo se usa cuando el punto de conexión de VLAN está funcionando en modo de tronco, que se especifica en la propiedad **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="b2e5b-133">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="b2e5b-134">**TrunkedVLANList**</span><span class="sxs-lookup"><span data-stu-id="b2e5b-134">**TrunkedVLANList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2e5b-135">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b2e5b-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="b2e5b-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b2e5b-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b2e5b-137">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="b2e5b-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="b2e5b-138">Una matriz que contiene los identificadores de los puntos de conexión de VLAN con la Troncalización habilitada.</span><span class="sxs-lookup"><span data-stu-id="b2e5b-138">An array that contains IDs of VLAN endpoints with trunking enabled.</span></span>

> [!Note]  
> <span data-ttu-id="b2e5b-139">Esta propiedad solo se usa cuando el punto de conexión de VLAN está funcionando en modo de tronco, que se especifica en la propiedad **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="b2e5b-139">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b2e5b-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2e5b-140">Requirements</span></span>



| <span data-ttu-id="b2e5b-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2e5b-141">Requirement</span></span> | <span data-ttu-id="b2e5b-142">Value</span><span class="sxs-lookup"><span data-stu-id="b2e5b-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2e5b-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2e5b-143">Minimum supported client</span></span><br/> | <span data-ttu-id="b2e5b-144">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b2e5b-144">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="b2e5b-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2e5b-145">Minimum supported server</span></span><br/> | <span data-ttu-id="b2e5b-146">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="b2e5b-146">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="b2e5b-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b2e5b-147">Namespace</span></span><br/>                | <span data-ttu-id="b2e5b-148">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="b2e5b-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b2e5b-149">MOF</span><span class="sxs-lookup"><span data-stu-id="b2e5b-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2e5b-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2e5b-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2e5b-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b2e5b-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2e5b-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2e5b-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2e5b-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="b2e5b-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2e5b-154">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="b2e5b-154">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

