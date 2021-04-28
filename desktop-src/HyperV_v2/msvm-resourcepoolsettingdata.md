---
description: 'Msvm_ResourcePoolSettingData clase : representa la configuración de una instancia de ResourcePool de Msvm \_ que no está relacionada con la asignación.'
ms.assetid: 32e0066c-7e14-454c-8aa9-06e093ef8072
title: Msvm_ResourcePoolSettingData clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolSettingData
- Msvm_ResourcePoolSettingData.InstanceID
- Msvm_ResourcePoolSettingData.Caption
- Msvm_ResourcePoolSettingData.Description
- Msvm_ResourcePoolSettingData.ElementName
- Msvm_ResourcePoolSettingData.PoolID
- Msvm_ResourcePoolSettingData.ResourceType
- Msvm_ResourcePoolSettingData.OtherResourceType
- Msvm_ResourcePoolSettingData.ResourceSubType
- Msvm_ResourcePoolSettingData.LoadBalancingBehavior
- Msvm_ResourcePoolSettingData.MappingBehavior
- Msvm_ResourcePoolSettingData.MappingOrder
- Msvm_ResourcePoolSettingData.Notes
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4fba27ec5c12e0c3cb18b8a6dfd4a863e59cad62
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111513"
---
# <a name="msvm_resourcepoolsettingdata-class"></a><span data-ttu-id="687a5-103">Clase \_ ResourcePoolSettingData de Msvm</span><span class="sxs-lookup"><span data-stu-id="687a5-103">Msvm\_ResourcePoolSettingData class</span></span>

<span data-ttu-id="687a5-104">Representa la configuración de una instancia [**de \_ ResourcePool de Msvm**](msvm-resourcepool.md) que no está relacionada con la asignación.</span><span class="sxs-lookup"><span data-stu-id="687a5-104">Represents the settings of a [**Msvm\_ResourcePool**](msvm-resourcepool.md) instance that are not allocation related.</span></span>

<span data-ttu-id="687a5-105">La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="687a5-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="687a5-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="687a5-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ResourcePoolSettingData : Msvm_AbstractResourcePoolSettingData
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

## <a name="members"></a><span data-ttu-id="687a5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="687a5-107">Members</span></span>

<span data-ttu-id="687a5-108">La **clase \_ ResourcePoolSettingData de Msvm** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="687a5-108">The **Msvm\_ResourcePoolSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="687a5-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="687a5-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="687a5-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="687a5-110">Properties</span></span>

<span data-ttu-id="687a5-111">La **clase \_ ResourcePoolSettingData de Msvm** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="687a5-111">The **Msvm\_ResourcePoolSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="687a5-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="687a5-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a5-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="687a5-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a5-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a5-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a5-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="687a5-115">A short description of the object.</span></span> <span data-ttu-id="687a5-116">Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)</span><span class="sxs-lookup"><span data-stu-id="687a5-116">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="687a5-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="687a5-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a5-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="687a5-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a5-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a5-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a5-120">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="687a5-120">A description of the object.</span></span> <span data-ttu-id="687a5-121">Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)</span><span class="sxs-lookup"><span data-stu-id="687a5-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="687a5-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="687a5-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a5-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="687a5-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a5-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a5-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a5-125">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="687a5-125">A display name for the object.</span></span> <span data-ttu-id="687a5-126">Esta propiedad se hereda de [**\_ ManagedElement de CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)</span><span class="sxs-lookup"><span data-stu-id="687a5-126">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="687a5-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="687a5-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a5-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="687a5-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a5-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a5-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="687a5-130">Calificadores: **Clave**</span><span class="sxs-lookup"><span data-stu-id="687a5-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="687a5-131">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="687a5-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="687a5-132">Esta propiedad se hereda de [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="687a5-132">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="687a5-133">**LoadBalancingBehavior**</span><span class="sxs-lookup"><span data-stu-id="687a5-133">**LoadBalancingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a5-134">Tipo de datos: **uint16**</span><span class="sxs-lookup"><span data-stu-id="687a5-134">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="687a5-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a5-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a5-136">Especifica la estrategia de asignación que usará el grupo de recursos para equilibrar el uso de recursos entre sus recursos agregados.</span><span class="sxs-lookup"><span data-stu-id="687a5-136">Specifies the allocation strategy to be used by the resource pool to balance resource usage across its aggregated resources.</span></span> <span data-ttu-id="687a5-137">Esta propiedad se hereda de [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="687a5-137">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="687a5-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="687a5-138"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="687a5-139"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**Ninguno** (3)</span><span class="sxs-lookup"><span data-stu-id="687a5-140"><span id="None"></span><span id="none"></span><span id="NONE"></span>**None** (3)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-141"><span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>**Distribuido** (4)</span><span class="sxs-lookup"><span data-stu-id="687a5-141"><span id="Distributed"></span><span id="distributed"></span><span id="DISTRIBUTED"></span>**Distributed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-142"><span id="Consolidated_"></span><span id="consolidated_"></span><span id="CONSOLIDATED_"></span>**Consolidado** (5 )</span><span class="sxs-lookup"><span data-stu-id="687a5-142"><span id="Consolidated_"></span><span id="consolidated_"></span><span id="CONSOLIDATED_"></span>**Consolidated** (5 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="687a5-143">**MappingBehavior**</span><span class="sxs-lookup"><span data-stu-id="687a5-143">**MappingBehavior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a5-144">Tipo de datos: **uint16**</span><span class="sxs-lookup"><span data-stu-id="687a5-144">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="687a5-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a5-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a5-146">Especifica si el grupo de recursos puede intentar usar otros recursos de host para satisfacer la solicitud de asignación si no se pueden asignar los recursos deseados.</span><span class="sxs-lookup"><span data-stu-id="687a5-146">Specifies whether the resource pool can attempt to use other host resources to satisfy the allocation request if the desired resources cannot be allocated.</span></span> <span data-ttu-id="687a5-147">Esta propiedad se hereda de [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="687a5-147">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="687a5-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="687a5-148"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-149"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**No compatible** (2)</span><span class="sxs-lookup"><span data-stu-id="687a5-149"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (2)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-150"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicado** (3)</span><span class="sxs-lookup"><span data-stu-id="687a5-150"><span id="Dedicated"></span><span id="dedicated"></span><span id="DEDICATED"></span>**Dedicated** (3)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-151"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Afinidad flexible** (4)</span><span class="sxs-lookup"><span data-stu-id="687a5-151"><span id="Soft_Affinity"></span><span id="soft_affinity"></span><span id="SOFT_AFFINITY"></span>**Soft Affinity** (4)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-152"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Afinidad dura** (5)</span><span class="sxs-lookup"><span data-stu-id="687a5-152"><span id="Hard_Affinity"></span><span id="hard_affinity"></span><span id="HARD_AFFINITY"></span>**Hard Affinity** (5)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="687a5-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32767..65535)</span><span class="sxs-lookup"><span data-stu-id="687a5-154"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (32767..65535 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="687a5-155">**MappingOrder**</span><span class="sxs-lookup"><span data-stu-id="687a5-155">**MappingOrder**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a5-156">Tipo de datos: **matriz de** cadenas</span><span class="sxs-lookup"><span data-stu-id="687a5-156">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="687a5-157">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a5-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a5-158">Especifica el orden en el que se seleccionarán los recursos de host disponibles a través de este grupo al intentar satisfacer una solicitud de asignación, y el recurso host solicitado no está disponible o no se especifica ningún recurso host.</span><span class="sxs-lookup"><span data-stu-id="687a5-158">Specifies the order in which host resources available through this pool will be selected when attempting to satisfy an allocation request, and the requested host resource is not available or no host resource is specified.</span></span> <span data-ttu-id="687a5-159">Esta propiedad se hereda de [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)</span><span class="sxs-lookup"><span data-stu-id="687a5-159">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="687a5-160">**Notas**</span><span class="sxs-lookup"><span data-stu-id="687a5-160">**Notes**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a5-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="687a5-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a5-162">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a5-162">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a5-163">El usuario final proporcionó notas relacionadas con este grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="687a5-163">End-user supplied notes that are related to this resource pool.</span></span> <span data-ttu-id="687a5-164">Esta propiedad se hereda de [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)</span><span class="sxs-lookup"><span data-stu-id="687a5-164">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="687a5-165">**OtherResourceType**</span><span class="sxs-lookup"><span data-stu-id="687a5-165">**OtherResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a5-166">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="687a5-166">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a5-167">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a5-167">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a5-168">Cadena que describe el tipo de recurso cuando un valor bien definido no está disponible y **ResourceType** se establece en 0 (Otros).</span><span class="sxs-lookup"><span data-stu-id="687a5-168">A string that describes the resource type when a well defined value is not available and **ResourceType** is set to 0 (Other).</span></span> <span data-ttu-id="687a5-169">Esta propiedad se hereda de [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)</span><span class="sxs-lookup"><span data-stu-id="687a5-169">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="687a5-170">**PoolID**</span><span class="sxs-lookup"><span data-stu-id="687a5-170">**PoolID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a5-171">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="687a5-171">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a5-172">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a5-172">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a5-173">Identificador del grupo.</span><span class="sxs-lookup"><span data-stu-id="687a5-173">An identifier for the pool.</span></span> <span data-ttu-id="687a5-174">Esta propiedad se usa para proporcionar correlación entre guardar y restaurar datos de configuración en el almacenamiento persistente subyacente.</span><span class="sxs-lookup"><span data-stu-id="687a5-174">This property is used to provide correlation across save and restore of configuration data to underlying persistent storage.</span></span> <span data-ttu-id="687a5-175">Esta propiedad se hereda de [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)</span><span class="sxs-lookup"><span data-stu-id="687a5-175">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="687a5-176">**Subtipo de recurso**</span><span class="sxs-lookup"><span data-stu-id="687a5-176">**ResourceSubType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a5-177">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="687a5-177">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="687a5-178">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a5-178">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a5-179">Cadena que describe un subtipo específico de implementación para este grupo.</span><span class="sxs-lookup"><span data-stu-id="687a5-179">A string that describes an implementation-specific subtype for this pool.</span></span> <span data-ttu-id="687a5-180">Por ejemplo, esto se puede usar para distinguir distintos modelos del mismo tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="687a5-180">For example, this may be used to distinguish different models of the same resource type.</span></span> <span data-ttu-id="687a5-181">Esta propiedad se hereda de [**Msvm \_ AbstractResourcePoolSettingData.**](msvm-abstractresourcepoolsettingdata.md)</span><span class="sxs-lookup"><span data-stu-id="687a5-181">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

</dd> <dt>

<span data-ttu-id="687a5-182">**ResourceType**</span><span class="sxs-lookup"><span data-stu-id="687a5-182">**ResourceType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="687a5-183">Tipo de datos: **uint16**</span><span class="sxs-lookup"><span data-stu-id="687a5-183">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="687a5-184">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="687a5-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="687a5-185">Tipo de recurso que este grupo de recursos puede asignar.</span><span class="sxs-lookup"><span data-stu-id="687a5-185">The type of resource this resource pool can allocate.</span></span> <span data-ttu-id="687a5-186">Esta propiedad se hereda de [**Msvm \_ AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span><span class="sxs-lookup"><span data-stu-id="687a5-186">This property is inherited from [**Msvm\_AbstractResourcePoolSettingData**](msvm-abstractresourcepoolsettingdata.md).</span></span>

<dl> <dt>

<span data-ttu-id="687a5-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otros** (1)</span><span class="sxs-lookup"><span data-stu-id="687a5-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-188"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Sistema informático** (2)</span><span class="sxs-lookup"><span data-stu-id="687a5-188"><span id="Computer_System"></span><span id="computer_system"></span><span id="COMPUTER_SYSTEM"></span>**Computer System** (2)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-189"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Procesador** (3)</span><span class="sxs-lookup"><span data-stu-id="687a5-189"><span id="Processor"></span><span id="processor"></span><span id="PROCESSOR"></span>**Processor** (3)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-190"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memoria** (4)</span><span class="sxs-lookup"><span data-stu-id="687a5-190"><span id="Memory"></span><span id="memory"></span><span id="MEMORY"></span>**Memory** (4)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-191"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**Controlador IDE** (5)</span><span class="sxs-lookup"><span data-stu-id="687a5-191"><span id="IDE_Controller"></span><span id="ide_controller"></span><span id="IDE_CONTROLLER"></span>**IDE Controller** (5)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-192"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**HBA SCSI paralelo** (6)</span><span class="sxs-lookup"><span data-stu-id="687a5-192"><span id="Parallel_SCSI_HBA"></span><span id="parallel_scsi_hba"></span><span id="PARALLEL_SCSI_HBA"></span>**Parallel SCSI HBA** (6)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-193"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span><span class="sxs-lookup"><span data-stu-id="687a5-193"><span id="FC_HBA"></span><span id="fc_hba"></span>**FC HBA** (7)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-194"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**HBA iSCSI** (8)</span><span class="sxs-lookup"><span data-stu-id="687a5-194"><span id="iSCSI_HBA"></span><span id="iscsi_hba"></span><span id="ISCSI_HBA"></span>**iSCSI HBA** (8)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-195"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span><span class="sxs-lookup"><span data-stu-id="687a5-195"><span id="IB_HCA"></span><span id="ib_hca"></span>**IB HCA** (9)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-196"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Adaptador Ethernet** (10)</span><span class="sxs-lookup"><span data-stu-id="687a5-196"><span id="Ethernet_Adapter"></span><span id="ethernet_adapter"></span><span id="ETHERNET_ADAPTER"></span>**Ethernet Adapter** (10)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-197"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Otro adaptador de red** (11)</span><span class="sxs-lookup"><span data-stu-id="687a5-197"><span id="Other_Network_Adapter"></span><span id="other_network_adapter"></span><span id="OTHER_NETWORK_ADAPTER"></span>**Other Network Adapter** (11)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-198"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**Ranura de E/S** (12)</span><span class="sxs-lookup"><span data-stu-id="687a5-198"><span id="I_O_Slot"></span><span id="i_o_slot"></span><span id="I_O_SLOT"></span>**I/O Slot** (12)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-199"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**Dispositivo de E/S** (13)</span><span class="sxs-lookup"><span data-stu-id="687a5-199"><span id="I_O_Device"></span><span id="i_o_device"></span><span id="I_O_DEVICE"></span>**I/O Device** (13)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-200"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Disquete** (14)</span><span class="sxs-lookup"><span data-stu-id="687a5-200"><span id="Floppy_Drive"></span><span id="floppy_drive"></span><span id="FLOPPY_DRIVE"></span>**Floppy Drive** (14)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-201"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**Unidad de CD** (15)</span><span class="sxs-lookup"><span data-stu-id="687a5-201"><span id="CD_Drive"></span><span id="cd_drive"></span><span id="CD_DRIVE"></span>**CD Drive** (15)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-202"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**Unidad de DVD** (16)</span><span class="sxs-lookup"><span data-stu-id="687a5-202"><span id="DVD_drive"></span><span id="dvd_drive"></span><span id="DVD_DRIVE"></span>**DVD drive** (16)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-203"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Unidad de disco** (17)</span><span class="sxs-lookup"><span data-stu-id="687a5-203"><span id="Disk_Drive"></span><span id="disk_drive"></span><span id="DISK_DRIVE"></span>**Disk Drive** (17)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-204"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Unidad de** cinta (18)</span><span class="sxs-lookup"><span data-stu-id="687a5-204"><span id="Tape_Drive"></span><span id="tape_drive"></span><span id="TAPE_DRIVE"></span>**Tape Drive** (18)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-205"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Extensión de** almacenamiento (19)</span><span class="sxs-lookup"><span data-stu-id="687a5-205"><span id="Storage_Extent"></span><span id="storage_extent"></span><span id="STORAGE_EXTENT"></span>**Storage Extent** (19)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-206"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Otro dispositivo de almacenamiento** (20)</span><span class="sxs-lookup"><span data-stu-id="687a5-206"><span id="Other_storage_device"></span><span id="other_storage_device"></span><span id="OTHER_STORAGE_DEVICE"></span>**Other storage device** (20)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-207"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Puerto serie** (21)</span><span class="sxs-lookup"><span data-stu-id="687a5-207"><span id="Serial_port"></span><span id="serial_port"></span><span id="SERIAL_PORT"></span>**Serial port** (21)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-208"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Puerto paralelo** (22)</span><span class="sxs-lookup"><span data-stu-id="687a5-208"><span id="Parallel_port"></span><span id="parallel_port"></span><span id="PARALLEL_PORT"></span>**Parallel port** (22)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-209"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**Controlador USB** (23)</span><span class="sxs-lookup"><span data-stu-id="687a5-209"><span id="USB_Controller"></span><span id="usb_controller"></span><span id="USB_CONTROLLER"></span>**USB Controller** (23)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-210"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Controlador de gráficos** (24)</span><span class="sxs-lookup"><span data-stu-id="687a5-210"><span id="Graphics_controller"></span><span id="graphics_controller"></span><span id="GRAPHICS_CONTROLLER"></span>**Graphics controller** (24)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-211"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 controlador** (25)</span><span class="sxs-lookup"><span data-stu-id="687a5-211"><span id="IEEE_1394_Controller"></span><span id="ieee_1394_controller"></span><span id="IEEE_1394_CONTROLLER"></span>**IEEE 1394 Controller** (25)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-212"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Unidad particionable** (26)</span><span class="sxs-lookup"><span data-stu-id="687a5-212"><span id="Partitionable_Unit"></span><span id="partitionable_unit"></span><span id="PARTITIONABLE_UNIT"></span>**Partitionable Unit** (26)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-213"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Unidad base particionable** (27)</span><span class="sxs-lookup"><span data-stu-id="687a5-213"><span id="Base_Partitionable_Unit"></span><span id="base_partitionable_unit"></span><span id="BASE_PARTITIONABLE_UNIT"></span>**Base Partitionable Unit** (27)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-214"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Potencia** (28)</span><span class="sxs-lookup"><span data-stu-id="687a5-214"><span id="Power"></span><span id="power"></span><span id="POWER"></span>**Power** (28)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-215"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Capacidad de refrigeración** (29)</span><span class="sxs-lookup"><span data-stu-id="687a5-215"><span id="Cooling_Capacity"></span><span id="cooling_capacity"></span><span id="COOLING_CAPACITY"></span>**Cooling Capacity** (29)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-216"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Puerto de conmutador Ethernet** (30)</span><span class="sxs-lookup"><span data-stu-id="687a5-216"><span id="Ethernet_Switch_Port"></span><span id="ethernet_switch_port"></span><span id="ETHERNET_SWITCH_PORT"></span>**Ethernet Switch Port** (30)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-217"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Disco lógico** (31)</span><span class="sxs-lookup"><span data-stu-id="687a5-217"><span id="Logical_Disk"></span><span id="logical_disk"></span><span id="LOGICAL_DISK"></span>**Logical Disk** (31)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-218"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Volumen de almacenamiento** (32)</span><span class="sxs-lookup"><span data-stu-id="687a5-218"><span id="Storage_Volume"></span><span id="storage_volume"></span><span id="STORAGE_VOLUME"></span>**Storage Volume** (32)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-219"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Conexión Ethernet** (33)</span><span class="sxs-lookup"><span data-stu-id="687a5-219"><span id="Ethernet_Connection"></span><span id="ethernet_connection"></span><span id="ETHERNET_CONNECTION"></span>**Ethernet Connection** (33)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-220"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="687a5-220"><span id="DMTF_reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="687a5-221"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Proveedor reservado** (0x8000.. 0xFFFF )</span><span class="sxs-lookup"><span data-stu-id="687a5-221"><span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span>**Vendor Reserved** (0x8000..0xFFFF )</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="687a5-222">Requisitos</span><span class="sxs-lookup"><span data-stu-id="687a5-222">Requirements</span></span>



| <span data-ttu-id="687a5-223">Requisito</span><span class="sxs-lookup"><span data-stu-id="687a5-223">Requirement</span></span> | <span data-ttu-id="687a5-224">Valor</span><span class="sxs-lookup"><span data-stu-id="687a5-224">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="687a5-225">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="687a5-225">Minimum supported client</span></span><br/> | <span data-ttu-id="687a5-226">Windows 8 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="687a5-226">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="687a5-227">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="687a5-227">Minimum supported server</span></span><br/> | <span data-ttu-id="687a5-228">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="687a5-228">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="687a5-229">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="687a5-229">Namespace</span></span><br/>                | <span data-ttu-id="687a5-230">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="687a5-230">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="687a5-231">MOF</span><span class="sxs-lookup"><span data-stu-id="687a5-231">MOF</span></span><br/>                      | <dl> <span data-ttu-id="687a5-232"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="687a5-232"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="687a5-233">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="687a5-233">DLL</span></span><br/>                      | <dl> <span data-ttu-id="687a5-234"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="687a5-234"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

