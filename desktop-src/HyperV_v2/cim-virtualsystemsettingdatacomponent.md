---
description: Representa una parte de una relación entre una instancia de CIM \_ VirtualSystemSettingData y un conjunto de \_ instancias de RESOURCEALLOCATIONSETTINGDATA de CIM.
ms.assetid: 4f167517-079e-4b5f-885a-741ac1d1dc71
title: CIM_VirtualSystemSettingDataComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingDataComponent
- CIM_VirtualSystemSettingDataComponent.GroupComponent
- CIM_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afbd7ab192c65e99f4479e5380e57dc78c8a0a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156845"
---
# <a name="cim_virtualsystemsettingdatacomponent-class"></a><span data-ttu-id="e262d-103">\_Clase VirtualSystemSettingDataComponent de CIM</span><span class="sxs-lookup"><span data-stu-id="e262d-103">CIM\_VirtualSystemSettingDataComponent class</span></span>

<span data-ttu-id="e262d-104">Representa una parte de una relación entre una instancia de [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) y un conjunto de instancias de [**\_ ResourceAllocationSettingData de CIM**](cim-resourceallocationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="e262d-104">Represents a portion of a relationship between a [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) instance and a set of [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="e262d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e262d-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingDataComponent : CIM_Component
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="e262d-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="e262d-106">Members</span></span>

<span data-ttu-id="e262d-107">La clase **CIM \_ VirtualSystemSettingDataComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e262d-107">The **CIM\_VirtualSystemSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="e262d-108">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e262d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e262d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e262d-109">Properties</span></span>

<span data-ttu-id="e262d-110">La clase **CIM \_ VirtualSystemSettingDataComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e262d-110">The **CIM\_VirtualSystemSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e262d-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e262d-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262d-112">Tipo de datos: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="e262d-112">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="e262d-113">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e262d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262d-114">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="e262d-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e262d-115">Referencia al objeto [**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) de nivel superior de la configuración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="e262d-115">A reference to the top-level [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) object of the virtual system configuration.</span></span>

</dd> <dt>

<span data-ttu-id="e262d-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e262d-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e262d-117">Tipo de datos: **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="e262d-117">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="e262d-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e262d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e262d-119">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="e262d-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e262d-120">Referencia al objeto [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa una parte de la configuración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="e262d-120">A reference the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) object that represents a part of the virtual system configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e262d-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e262d-121">Requirements</span></span>



| <span data-ttu-id="e262d-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e262d-122">Requirement</span></span> | <span data-ttu-id="e262d-123">Value</span><span class="sxs-lookup"><span data-stu-id="e262d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e262d-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e262d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e262d-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="e262d-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="e262d-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e262d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e262d-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="e262d-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="e262d-128">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e262d-128">Namespace</span></span><br/>                | <span data-ttu-id="e262d-129">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="e262d-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e262d-130">MOF</span><span class="sxs-lookup"><span data-stu-id="e262d-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e262d-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e262d-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e262d-132">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e262d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e262d-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e262d-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e262d-134">Vea también</span><span class="sxs-lookup"><span data-stu-id="e262d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e262d-135">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="e262d-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

