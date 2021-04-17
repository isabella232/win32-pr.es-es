---
description: Asociación que se usa para establecer &\# 0034; parte de&\# 0034; relaciones entre una instancia de un \_ EthernetPortAllocationSettingData de MSVM y una o varias instancias de una EthernetSwitchFeatureSettingData MSVM \_ .
ms.assetid: fab15342-a134-4d4a-9668-1272041614b9
title: Msvm_EthernetPortSettingDataComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortSettingDataComponent
- Msvm_EthernetPortSettingDataComponent.GroupComponent
- Msvm_EthernetPortSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c00c056bd5095d945af12fde3556d92b9a2d7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667564"
---
# <a name="msvm_ethernetportsettingdatacomponent-class"></a><span data-ttu-id="9728b-103">MSVM \_ EthernetPortSettingDataComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="9728b-103">Msvm\_EthernetPortSettingDataComponent class</span></span>

<span data-ttu-id="9728b-104">Asociación que se usa para establecer relaciones entre una instancia de un [**\_ EthernetPortAllocationSettingData de MSVM**](msvm-ethernetportallocationsettingdata.md) y una o más instancias de una [**MSVM \_ EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="9728b-104">An association used to establish "part of" relationships between one instance of an [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) and one or more instances of an [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md).</span></span>

<span data-ttu-id="9728b-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9728b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9728b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9728b-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortSettingDataComponent : CIM_Component
{
  Msvm_EthernetPortAllocationSettingData    REF GroupComponent;
  Msvm_EthernetSwitchPortFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="9728b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9728b-107">Members</span></span>

<span data-ttu-id="9728b-108">La clase **MSVM \_ EthernetPortSettingDataComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9728b-108">The **Msvm\_EthernetPortSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="9728b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9728b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9728b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9728b-110">Properties</span></span>

<span data-ttu-id="9728b-111">La clase **MSVM \_ EthernetPortSettingDataComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9728b-111">The **Msvm\_EthernetPortSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9728b-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="9728b-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9728b-113">Tipo de datos: **[ **MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="9728b-113">Data type: **[**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="9728b-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9728b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9728b-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agregado**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="9728b-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="9728b-116">Referencia a una instancia de la clase [**MSVM \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) que representa el puerto Ethernet.</span><span class="sxs-lookup"><span data-stu-id="9728b-116">A reference to an instance of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that represents the Ethernet port.</span></span>

</dd> <dt>

<span data-ttu-id="9728b-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="9728b-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9728b-118">Tipo de datos: **[ **MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**</span><span class="sxs-lookup"><span data-stu-id="9728b-118">Data type: **[**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)**</span></span>
</dt> <dt>

<span data-ttu-id="9728b-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9728b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9728b-120">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="9728b-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="9728b-121">Referencia a una instancia de la clase [**MSVM \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) que representa la configuración de características aplicada al puerto.</span><span class="sxs-lookup"><span data-stu-id="9728b-121">A reference to an instance of the [**Msvm\_EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represents the feature settings applied to the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9728b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9728b-122">Requirements</span></span>



| <span data-ttu-id="9728b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="9728b-123">Requirement</span></span> | <span data-ttu-id="9728b-124">Value</span><span class="sxs-lookup"><span data-stu-id="9728b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9728b-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9728b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9728b-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="9728b-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9728b-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9728b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9728b-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9728b-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9728b-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9728b-129">Namespace</span></span><br/>                | <span data-ttu-id="9728b-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9728b-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9728b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="9728b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9728b-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9728b-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9728b-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9728b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9728b-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9728b-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

