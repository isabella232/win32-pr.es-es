---
description: Describe los datos de configuración de un conmutador Ethernet virtual.
ms.assetid: 462cff06-5ba6-410a-b091-5c6abab13f03
title: CIM_VirtualEthernetSwitchSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualEthernetSwitchSettingData
- CIM_VirtualEthernetSwitchSettingData.VLANConnection
- CIM_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- CIM_VirtualEthernetSwitchSettingData.MaxNumMACAddress
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64d7053364aebe1fab5739cd75389b1a9343efe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666899"
---
# <a name="cim_virtualethernetswitchsettingdata-class"></a><span data-ttu-id="467aa-103">\_Clase VirtualEthernetSwitchSettingData de CIM</span><span class="sxs-lookup"><span data-stu-id="467aa-103">CIM\_VirtualEthernetSwitchSettingData class</span></span>

<span data-ttu-id="467aa-104">Describe los datos de configuración de un conmutador Ethernet virtual.</span><span class="sxs-lookup"><span data-stu-id="467aa-104">Describes settings data for a virtual ethernet switch.</span></span>

## <a name="syntax"></a><span data-ttu-id="467aa-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="467aa-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualEthernetSwitchSettingData : CIM_VirtualSystemSettingData
{
  string VLANConnection[];
  string AssociatedResourcePool[];
  uint32 MaxNumMACAddress;
};
```

## <a name="members"></a><span data-ttu-id="467aa-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="467aa-106">Members</span></span>

<span data-ttu-id="467aa-107">La clase **CIM \_ VirtualEthernetSwitchSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="467aa-107">The **CIM\_VirtualEthernetSwitchSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="467aa-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="467aa-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="467aa-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="467aa-109">Properties</span></span>

<span data-ttu-id="467aa-110">La clase **CIM \_ VirtualEthernetSwitchSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="467aa-110">The **CIM\_VirtualEthernetSwitchSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="467aa-111">**AssociatedResourcePool**</span><span class="sxs-lookup"><span data-stu-id="467aa-111">**AssociatedResourcePool**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="467aa-112">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="467aa-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="467aa-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="467aa-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="467aa-114">Una matriz que contiene los grupos de recursos de host asociados actualmente o que se asocian con el conmutador Ethernet para asignar conexiones Ethernet entre el conmutador Ethernet y una máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="467aa-114">An array that contains the host resource pools that are currently associated, or to associate with the ethernet switch, in order to allocate ethernet connections between the ethernet switch and a virtual machine.</span></span> <span data-ttu-id="467aa-115">Cada valor distinto de NULL de esta propiedad debe ajustarse **al \_ URI \_ de WBEM UntypedInstancePath** tal y como se define en la especificación DMTF "DSP0207".</span><span class="sxs-lookup"><span data-stu-id="467aa-115">Each non-Null value of this property must conform to **WBEM\_URI\_UntypedInstancePath** as defined in the DMTF "DSP0207" specification.</span></span>

</dd> <dt>

<span data-ttu-id="467aa-116">**MaxNumMACAddress**</span><span class="sxs-lookup"><span data-stu-id="467aa-116">**MaxNumMACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="467aa-117">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="467aa-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="467aa-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="467aa-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="467aa-119">El número de direcciones MAC únicas que el conmutador puede aprender para el aprendizaje de direcciones MAC, tal como se define en el estándar IEEE 802,1.</span><span class="sxs-lookup"><span data-stu-id="467aa-119">The number of unique MAC addresses that the switch can learn for MAC address learning, as defined in the IEEE 802.1 standard.</span></span>

</dd> <dt>

<span data-ttu-id="467aa-120">**VLANConnection**</span><span class="sxs-lookup"><span data-stu-id="467aa-120">**VLANConnection**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="467aa-121">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="467aa-121">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="467aa-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="467aa-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="467aa-123">Una matriz que contiene los identificadores de VLAN a los que puede tener acceso el conmutador.</span><span class="sxs-lookup"><span data-stu-id="467aa-123">An array that contains the VLAN IDs that the switch can access.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="467aa-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="467aa-124">Requirements</span></span>



| <span data-ttu-id="467aa-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="467aa-125">Requirement</span></span> | <span data-ttu-id="467aa-126">Value</span><span class="sxs-lookup"><span data-stu-id="467aa-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="467aa-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="467aa-127">Minimum supported client</span></span><br/> | <span data-ttu-id="467aa-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="467aa-128">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="467aa-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="467aa-129">Minimum supported server</span></span><br/> | <span data-ttu-id="467aa-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="467aa-130">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="467aa-131">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="467aa-131">Namespace</span></span><br/>                | <span data-ttu-id="467aa-132">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="467aa-132">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="467aa-133">MOF</span><span class="sxs-lookup"><span data-stu-id="467aa-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="467aa-134"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="467aa-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="467aa-135">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="467aa-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="467aa-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="467aa-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="467aa-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="467aa-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="467aa-138">**\_VIRTUALSYSTEMSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="467aa-138">**CIM\_VirtualSystemSettingData**</span></span>](cim-virtualsystemsettingdata.md)
</dt> </dl>

 

 




