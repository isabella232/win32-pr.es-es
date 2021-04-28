---
description: 'Msvm_AbstractResourcePoolSettingData clase : representa la configuración de una instancia de ResourcePool de Msvm \_ que no está relacionada con la asignación.'
ms.assetid: c5954a92-8942-4b45-aae2-6936328dab1a
title: Msvm_AbstractResourcePoolSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AbstractResourcePoolSettingData
- Msvm_AbstractResourcePoolSettingData.InstanceID
- Msvm_AbstractResourcePoolSettingData.Caption
- Msvm_AbstractResourcePoolSettingData.Description
- Msvm_AbstractResourcePoolSettingData.ElementName
- Msvm_AbstractResourcePoolSettingData.PoolID
- Msvm_AbstractResourcePoolSettingData.ResourceType
- Msvm_AbstractResourcePoolSettingData.OtherResourceType
- Msvm_AbstractResourcePoolSettingData.ResourceSubType
- Msvm_AbstractResourcePoolSettingData.LoadBalancingBehavior
- Msvm_AbstractResourcePoolSettingData.MappingBehavior
- Msvm_AbstractResourcePoolSettingData.MappingOrder
- Msvm_AbstractResourcePoolSettingData.Notes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dca3da14ac74a8d6fab1ba96db98f9e2eccd74ea
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112123"
---
# <a name="msvm_abstractresourcepoolsettingdata-class"></a><span data-ttu-id="637c5-103">Clase Msvm \_ AbstractResourcePoolSettingData</span><span class="sxs-lookup"><span data-stu-id="637c5-103">Msvm\_AbstractResourcePoolSettingData class</span></span>

<span data-ttu-id="637c5-104">Representa la configuración de una instancia [**de \_ ResourcePool de Msvm**](msvm-resourcepool.md) que no está relacionada con la asignación.</span><span class="sxs-lookup"><span data-stu-id="637c5-104">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span>

<span data-ttu-id="637c5-105">La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="637c5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="637c5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="637c5-106">Syntax</span></span>

``` syntax
[Abstract, AMENDMENT]
class Msvm_AbstractResourcePoolSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string PoolID;
  uint16 ResourceType;
  string OtherResourceType;
  string ResourceSubType;
  uint16 LoadBalancingBehavior;
  uint16 MappingBehavior;
  string MappingOrder[];
  string Notes;
};
```

## <a name="members"></a><span data-ttu-id="637c5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="637c5-107">Members</span></span>

<span data-ttu-id="637c5-108">La **clase Msvm \_ AbstractResourcePoolSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="637c5-108">The **Msvm\_AbstractResourcePoolSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="637c5-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="637c5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="637c5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="637c5-110">Properties</span></span>

<span data-ttu-id="637c5-111">La **clase Msvm \_ AbstractResourcePoolSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="637c5-111">The **Msvm\_AbstractResourcePoolSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="637c5-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="637c5-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637c5-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="637c5-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="637c5-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637c5-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="637c5-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="637c5-115">A short description of the object.</span></span> <span data-ttu-id="637c5-116">Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)</span><span class="sxs-lookup"><span data-stu-id="637c5-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="637c5-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="637c5-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637c5-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="637c5-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="637c5-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637c5-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="637c5-120">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="637c5-120">A description of the object.</span></span> <span data-ttu-id="637c5-121">Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)</span><span class="sxs-lookup"><span data-stu-id="637c5-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="637c5-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="637c5-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637c5-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="637c5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="637c5-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637c5-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="637c5-125">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="637c5-125">A display name for the object.</span></span> <span data-ttu-id="637c5-126">Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)</span><span class="sxs-lookup"><span data-stu-id="637c5-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="637c5-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="637c5-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637c5-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="637c5-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="637c5-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637c5-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="637c5-130">Calificadores: **Clave**</span><span class="sxs-lookup"><span data-stu-id="637c5-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="637c5-131">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="637c5-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="637c5-132">Esta propiedad se hereda de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="637c5-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="637c5-133">**LoadBalancingBehavior**</span><span class="sxs-lookup"><span data-stu-id="637c5-133">**LoadBalancingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637c5-134">Tipo de datos: **uint16**</span><span class="sxs-lookup"><span data-stu-id="637c5-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="637c5-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637c5-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="637c5-136">Especifica la estrategia de asignación que usará el grupo de recursos para equilibrar el uso de recursos entre sus recursos agregados.</span><span class="sxs-lookup"><span data-stu-id="637c5-136">Specifies the allocation strategy to be used by the resource pool to balance resource usage across its aggregated resources.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="637c5-137">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="637c5-137">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="637c5-138">**No compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="637c5-138">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span data-ttu-id="637c5-139">**Ninguno** (3)</span><span class="sxs-lookup"><span data-stu-id="637c5-139">**None** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>

<span data-ttu-id="637c5-140">**Distribuido** (4)</span><span class="sxs-lookup"><span data-stu-id="637c5-140">**Distributed** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Consolidated"></span><span id="consolidated"></span><span id="CONSOLIDATED"></span>

<span data-ttu-id="637c5-141">**Consolidado** (5)</span><span class="sxs-lookup"><span data-stu-id="637c5-141">**Consolidated** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="637c5-142">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="637c5-142">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637c5-143">Tipo de datos: **uint16**</span><span class="sxs-lookup"><span data-stu-id="637c5-143">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="637c5-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637c5-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="637c5-145">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**MappingBehavior**")</span><span class="sxs-lookup"><span data-stu-id="637c5-145">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="637c5-146">Especifica si el grupo de recursos puede intentar usar otros recursos de host para satisfacer la solicitud de asignación si no se pueden asignar los recursos deseados.</span><span class="sxs-lookup"><span data-stu-id="637c5-146">Specifies whether the resource pool can attempt to use other host resources to satisfy the allocation request if the desired resources cannot be allocated.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="637c5-147">**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="637c5-147">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="637c5-148">**No compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="637c5-148">**Not Supported** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>

<span data-ttu-id="637c5-149">**Dedicado** (3)</span><span class="sxs-lookup"><span data-stu-id="637c5-149">**Dedicated** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>

<span data-ttu-id="637c5-150">**Afinidad flexible** (4)</span><span class="sxs-lookup"><span data-stu-id="637c5-150">**Soft Affinity** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>

<span data-ttu-id="637c5-151">**Afinidad dura** (5)</span><span class="sxs-lookup"><span data-stu-id="637c5-151">**Hard Affinity** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="637c5-152">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="637c5-152">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="637c5-153">**Vendor Reserved** (32767..65535)</span><span class="sxs-lookup"><span data-stu-id="637c5-153">**Vendor Reserved** (32767..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="637c5-154">**MappingOrder**</span><span class="sxs-lookup"><span data-stu-id="637c5-154">**MappingOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637c5-155">Tipo de datos: **matriz de** cadenas</span><span class="sxs-lookup"><span data-stu-id="637c5-155">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="637c5-156">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637c5-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="637c5-157">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md).**MappingBehavior**")</span><span class="sxs-lookup"><span data-stu-id="637c5-157">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm\_ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md).**MappingBehavior**")</span></span>
</dt> </dl>

<span data-ttu-id="637c5-158">Especifica el orden en el que se seleccionarán los recursos de host disponibles a través de este grupo al intentar satisfacer una solicitud de asignación, y el recurso host solicitado no está disponible o no se especifica ningún recurso host.</span><span class="sxs-lookup"><span data-stu-id="637c5-158">Specifies the order in which host resources available through this pool will be selected when attempting to satisfy an allocation request, and the requested host resource is not available or no host resource is specified.</span></span>

</dd> <dt>

<span data-ttu-id="637c5-159">**Notas**</span><span class="sxs-lookup"><span data-stu-id="637c5-159">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637c5-160">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="637c5-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="637c5-161">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637c5-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="637c5-162">El usuario final proporcionó notas relacionadas con este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="637c5-162">End-user supplied notes that are related to this resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="637c5-163">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="637c5-163">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637c5-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="637c5-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="637c5-165">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637c5-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="637c5-166">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**OtherResourceType**")</span><span class="sxs-lookup"><span data-stu-id="637c5-166">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**OtherResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="637c5-167">Cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y **ResourceType** se establece en 0 (Otros).</span><span class="sxs-lookup"><span data-stu-id="637c5-167">A string that describes the resource type when a well defined value is not available and **ResourceType** is set to 0 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="637c5-168">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="637c5-168">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637c5-169">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="637c5-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="637c5-170">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637c5-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="637c5-171">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**PoolID**")</span><span class="sxs-lookup"><span data-stu-id="637c5-171">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**PoolID**")</span></span>
</dt> </dl>

<span data-ttu-id="637c5-172">Identificador del grupo.</span><span class="sxs-lookup"><span data-stu-id="637c5-172">An identifier for the pool.</span></span> <span data-ttu-id="637c5-173">Esta propiedad se usa para proporcionar correlación entre guardar y restaurar datos de configuración en el almacenamiento persistente subyacente.</span><span class="sxs-lookup"><span data-stu-id="637c5-173">This property is used to provide correlation across save and restore of configuration data to underlying persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="637c5-174">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="637c5-174">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637c5-175">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="637c5-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="637c5-176">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637c5-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="637c5-177">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**ResourceSubType**")</span><span class="sxs-lookup"><span data-stu-id="637c5-177">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceSubType**")</span></span>
</dt> </dl>

<span data-ttu-id="637c5-178">Cadena que describe un subtipo específico de implementación para este grupo.</span><span class="sxs-lookup"><span data-stu-id="637c5-178">A string that describes an implementation specific sub-type for this pool.</span></span> <span data-ttu-id="637c5-179">Por ejemplo, esto se puede usar para distinguir distintos modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="637c5-179">For example, this may be used to distinguish different models of the same resource type.</span></span>

</dd> <dt>

<span data-ttu-id="637c5-180">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="637c5-180">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="637c5-181">Tipo de datos: **uint16**</span><span class="sxs-lookup"><span data-stu-id="637c5-181">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="637c5-182">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="637c5-182">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="637c5-183">Calificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ ResourcePool**](cim-resourcepool.md).**ResourceType**")</span><span class="sxs-lookup"><span data-stu-id="637c5-183">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_ResourcePool**](cim-resourcepool.md).**ResourceType**")</span></span>
</dt> </dl>

<span data-ttu-id="637c5-184">Tipo de recurso que este grupo de recursos puede asignar.</span><span class="sxs-lookup"><span data-stu-id="637c5-184">The type of resource this resource pool can allocate.</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="637c5-185">**Otros** (1)</span><span class="sxs-lookup"><span data-stu-id="637c5-185">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>

<span data-ttu-id="637c5-186">**Sistema informático** (2)</span><span class="sxs-lookup"><span data-stu-id="637c5-186">**Computer System** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>

<span data-ttu-id="637c5-187">**Procesador** (3)</span><span class="sxs-lookup"><span data-stu-id="637c5-187">**Processor** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>

<span data-ttu-id="637c5-188">**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="637c5-188">**Memory** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>

<span data-ttu-id="637c5-189">**Controlador IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="637c5-189">**IDE Controller** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>

<span data-ttu-id="637c5-190">**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="637c5-190">**Parallel SCSI HBA** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="FC_HBA"></span><span id="fc_hba"></span>

<span data-ttu-id="637c5-191">**FC HBA** (7)</span><span class="sxs-lookup"><span data-stu-id="637c5-191">**FC HBA** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>

<span data-ttu-id="637c5-192">**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="637c5-192">**iSCSI HBA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="IB_HCA"></span><span id="ib_hca"></span>

<span data-ttu-id="637c5-193">**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="637c5-193">**IB HCA** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>

<span data-ttu-id="637c5-194">**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="637c5-194">**Ethernet Adapter** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>

<span data-ttu-id="637c5-195">**Otro adaptador de red** (11)</span><span class="sxs-lookup"><span data-stu-id="637c5-195">**Other Network Adapter** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>

<span data-ttu-id="637c5-196">**Ranura de E/S** (12)</span><span class="sxs-lookup"><span data-stu-id="637c5-196">**I/O Slot** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>

<span data-ttu-id="637c5-197">**Dispositivo de E/S** (13)</span><span class="sxs-lookup"><span data-stu-id="637c5-197">**I/O Device** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>

<span data-ttu-id="637c5-198">**Disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="637c5-198">**Floppy Drive** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>

<span data-ttu-id="637c5-199">**Unidad de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="637c5-199">**CD Drive** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>

<span data-ttu-id="637c5-200">**Unidad de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="637c5-200">**DVD drive** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>

<span data-ttu-id="637c5-201">**Unidad de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="637c5-201">**Disk Drive** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>

<span data-ttu-id="637c5-202">**Unidad de** cinta (18)</span><span class="sxs-lookup"><span data-stu-id="637c5-202">**Tape Drive** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>

<span data-ttu-id="637c5-203">**Extensión de almacenamiento** (19)</span><span class="sxs-lookup"><span data-stu-id="637c5-203">**Storage Extent** (19)</span></span>


</dt> <dd></dd> <dt>

<span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>

<span data-ttu-id="637c5-204">**Otro dispositivo de almacenamiento** (20)</span><span class="sxs-lookup"><span data-stu-id="637c5-204">**Other storage device** (20)</span></span>


</dt> <dd></dd> <dt>

<span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>

<span data-ttu-id="637c5-205">**Puerto serie** (21)</span><span class="sxs-lookup"><span data-stu-id="637c5-205">**Serial port** (21)</span></span>


</dt> <dd></dd> <dt>

<span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>

<span data-ttu-id="637c5-206">**Puerto paralelo** (22)</span><span class="sxs-lookup"><span data-stu-id="637c5-206">**Parallel port** (22)</span></span>


</dt> <dd></dd> <dt>

<span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>

<span data-ttu-id="637c5-207">**Controlador USB** (23)</span><span class="sxs-lookup"><span data-stu-id="637c5-207">**USB Controller** (23)</span></span>


</dt> <dd></dd> <dt>

<span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>

<span data-ttu-id="637c5-208">**Controlador de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="637c5-208">**Graphics controller** (24)</span></span>


</dt> <dd></dd> <dt>

<span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>

<span data-ttu-id="637c5-209">**IEEE 1394 controlador** (25)</span><span class="sxs-lookup"><span data-stu-id="637c5-209">**IEEE 1394 Controller** (25)</span></span>


</dt> <dd></dd> <dt>

<span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>

<span data-ttu-id="637c5-210">**Unidad particionable** (26)</span><span class="sxs-lookup"><span data-stu-id="637c5-210">**Partitionable Unit** (26)</span></span>


</dt> <dd></dd> <dt>

<span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>

<span data-ttu-id="637c5-211">**Unidad base particionable** (27)</span><span class="sxs-lookup"><span data-stu-id="637c5-211">**Base Partitionable Unit** (27)</span></span>


</dt> <dd></dd> <dt>

<span id="Power"></span><span id="power"></span><span id="POWER"></span>

<span data-ttu-id="637c5-212">**Potencia** (28)</span><span class="sxs-lookup"><span data-stu-id="637c5-212">**Power** (28)</span></span>


</dt> <dd></dd> <dt>

<span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>

<span data-ttu-id="637c5-213">**Capacidad de refrigeración** (29)</span><span class="sxs-lookup"><span data-stu-id="637c5-213">**Cooling Capacity** (29)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>

<span data-ttu-id="637c5-214">**Puerto de conmutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="637c5-214">**Ethernet Switch Port** (30)</span></span>


</dt> <dd></dd> <dt>

<span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>

<span data-ttu-id="637c5-215">**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="637c5-215">**Logical Disk** (31)</span></span>


</dt> <dd></dd> <dt>

<span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>

<span data-ttu-id="637c5-216">**Volumen de almacenamiento** (32)</span><span class="sxs-lookup"><span data-stu-id="637c5-216">**Storage Volume** (32)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>

<span data-ttu-id="637c5-217">**Conexión Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="637c5-217">**Ethernet Connection** (33)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="637c5-218">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="637c5-218">**DMTF reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="637c5-219">**Proveedor reservado** (0x8000.. 0xFFFF)</span><span class="sxs-lookup"><span data-stu-id="637c5-219">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


<span data-ttu-id="637c5-220"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="637c5-220"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="637c5-221">Requisitos</span><span class="sxs-lookup"><span data-stu-id="637c5-221">Requirements</span></span>



| <span data-ttu-id="637c5-222">Requisito</span><span class="sxs-lookup"><span data-stu-id="637c5-222">Requirement</span></span> | <span data-ttu-id="637c5-223">Valor</span><span class="sxs-lookup"><span data-stu-id="637c5-223">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="637c5-224">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="637c5-224">Minimum supported client</span></span><br/> | <span data-ttu-id="637c5-225">Windows 8 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="637c5-225">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="637c5-226">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="637c5-226">Minimum supported server</span></span><br/> | <span data-ttu-id="637c5-227">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="637c5-227">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="637c5-228">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="637c5-228">Namespace</span></span><br/>                | <span data-ttu-id="637c5-229">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="637c5-229">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="637c5-230">MOF</span><span class="sxs-lookup"><span data-stu-id="637c5-230">MOF</span></span><br/>                      | <dl> <span data-ttu-id="637c5-231"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="637c5-231"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="637c5-232">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="637c5-232">DLL</span></span><br/>                      | <dl> <span data-ttu-id="637c5-233"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="637c5-233"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

