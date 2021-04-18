---
description: Asociación que se usa para representar la configuración de red de la migración del sistema virtual del servicio de migración del sistema virtual.
ms.assetid: 5704dce7-1db3-4049-8c61-58bfa9596766
title: Msvm_VirtualSystemMigrationServiceSettingDataComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationServiceSettingDataComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.GroupComponent
- Msvm_VirtualSystemMigrationServiceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1ba69ebd6cfd50b30923db2ecc87e7e5aeebcaa5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666326"
---
# <a name="msvm_virtualsystemmigrationservicesettingdatacomponent-class"></a><span data-ttu-id="93d7b-103">MSVM \_ VirtualSystemMigrationServiceSettingDataComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="93d7b-103">Msvm\_VirtualSystemMigrationServiceSettingDataComponent class</span></span>

<span data-ttu-id="93d7b-104">Asociación que se usa para representar la configuración de red de la migración del sistema virtual del servicio de migración del sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="93d7b-104">An association used to represent virtual system migration network settings of the virtual system migration service.</span></span>

<span data-ttu-id="93d7b-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="93d7b-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="93d7b-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="93d7b-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationServiceSettingDataComponent : CIM_Component
{
  Msvm_VirtualSystemMigrationServiceSettingData REF GroupComponent;
  Msvm_VirtualSystemMigrationNetworkSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="93d7b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="93d7b-107">Members</span></span>

<span data-ttu-id="93d7b-108">La clase **MSVM \_ VirtualSystemMigrationServiceSettingDataComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="93d7b-108">The **Msvm\_VirtualSystemMigrationServiceSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="93d7b-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="93d7b-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93d7b-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="93d7b-110">Properties</span></span>

<span data-ttu-id="93d7b-111">La clase **MSVM \_ VirtualSystemMigrationServiceSettingDataComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="93d7b-111">The **Msvm\_VirtualSystemMigrationServiceSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93d7b-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="93d7b-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d7b-113">Tipo de datos: **MSVM \_ VirtualSystemMigrationServiceSettingData**</span><span class="sxs-lookup"><span data-stu-id="93d7b-113">Data type: **Msvm\_VirtualSystemMigrationServiceSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="93d7b-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93d7b-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93d7b-115">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**agregado**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="93d7b-115">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="93d7b-116">Referencia a una instancia de la clase [**MSVM \_ VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) que representa la configuración del servicio de migración.</span><span class="sxs-lookup"><span data-stu-id="93d7b-116">A reference to an instance of the [**Msvm\_VirtualSystemMigrationServiceSettingData**](msvm-virtualsystemmigrationservicesettingdata.md) class that represents the migration service settings.</span></span>

</dd> <dt>

<span data-ttu-id="93d7b-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="93d7b-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93d7b-118">Tipo de datos: **MSVM \_ VirtualSystemMigrationNetworkSettingData**</span><span class="sxs-lookup"><span data-stu-id="93d7b-118">Data type: **Msvm\_VirtualSystemMigrationNetworkSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="93d7b-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="93d7b-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93d7b-120">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="93d7b-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="93d7b-121">Una referencia a una instancia de la clase [**MSVM \_ VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) que representa la configuración de la red de migración.</span><span class="sxs-lookup"><span data-stu-id="93d7b-121">A reference to an instance of the [**Msvm\_VirtualSystemMigrationNetworkSettingData**](msvm-virtualsystemmigrationnetworksettingdata.md) class that represents the migration network settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93d7b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93d7b-122">Requirements</span></span>



| <span data-ttu-id="93d7b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="93d7b-123">Requirement</span></span> | <span data-ttu-id="93d7b-124">Value</span><span class="sxs-lookup"><span data-stu-id="93d7b-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93d7b-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93d7b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="93d7b-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="93d7b-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="93d7b-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="93d7b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="93d7b-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="93d7b-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93d7b-129">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="93d7b-129">Namespace</span></span><br/>                | <span data-ttu-id="93d7b-130">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="93d7b-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="93d7b-131">MOF</span><span class="sxs-lookup"><span data-stu-id="93d7b-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93d7b-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93d7b-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93d7b-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="93d7b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93d7b-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93d7b-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

