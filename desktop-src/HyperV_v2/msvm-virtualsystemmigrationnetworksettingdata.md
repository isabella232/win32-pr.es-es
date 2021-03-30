---
description: Representa la red en la que el servicio de migración del sistema virtual está escuchando la migración de sistema virtual entrante.
ms.assetid: 24458602-ff5c-45c2-8053-00315b59d3bb
title: Msvm_VirtualSystemMigrationNetworkSettingData (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationNetworkSettingData
- Msvm_VirtualSystemMigrationNetworkSettingData.InstanceID
- Msvm_VirtualSystemMigrationNetworkSettingData.Caption
- Msvm_VirtualSystemMigrationNetworkSettingData.Description
- Msvm_VirtualSystemMigrationNetworkSettingData.ElementName
- Msvm_VirtualSystemMigrationNetworkSettingData.SubnetNumber
- Msvm_VirtualSystemMigrationNetworkSettingData.PrefixLength
- Msvm_VirtualSystemMigrationNetworkSettingData.Metric
- Msvm_VirtualSystemMigrationNetworkSettingData.Tags
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4f7c24bb754148fa8ede12292f308164512af646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907695"
---
# <a name="msvm_virtualsystemmigrationnetworksettingdata-class"></a><span data-ttu-id="87341-103">MSVM \_ VirtualSystemMigrationNetworkSettingData (clase)</span><span class="sxs-lookup"><span data-stu-id="87341-103">Msvm\_VirtualSystemMigrationNetworkSettingData class</span></span>

<span data-ttu-id="87341-104">Representa la red en la que el servicio de migración del sistema virtual está escuchando la migración de sistema virtual entrante.</span><span class="sxs-lookup"><span data-stu-id="87341-104">Represents the network on which the virtual system migration service is listening for incoming virtual system migration.</span></span>

<span data-ttu-id="87341-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="87341-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="87341-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="87341-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationNetworkSettingData : CIM_SettingData
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string SubnetNumber;
  uint8  PrefixLength;
  uint32 Metric;
  string Tags[];
};
```

## <a name="members"></a><span data-ttu-id="87341-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="87341-107">Members</span></span>

<span data-ttu-id="87341-108">La clase **MSVM \_ VirtualSystemMigrationNetworkSettingData** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="87341-108">The **Msvm\_VirtualSystemMigrationNetworkSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="87341-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="87341-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="87341-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="87341-110">Properties</span></span>

<span data-ttu-id="87341-111">La clase **MSVM \_ VirtualSystemMigrationNetworkSettingData** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="87341-111">The **Msvm\_VirtualSystemMigrationNetworkSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="87341-112">**Caption**</span><span class="sxs-lookup"><span data-stu-id="87341-112">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87341-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87341-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87341-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87341-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87341-115">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="87341-115">A short description of the object.</span></span> <span data-ttu-id="87341-116">Esta propiedad se hereda de la clase [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) .</span><span class="sxs-lookup"><span data-stu-id="87341-116">This property is inherited from the [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) class.</span></span>

</dd> <dt>

<span data-ttu-id="87341-117">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="87341-117">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87341-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87341-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87341-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87341-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87341-120">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="87341-120">A description of the object.</span></span> <span data-ttu-id="87341-121">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="87341-121">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="87341-122">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="87341-122">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87341-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87341-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87341-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87341-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87341-125">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="87341-125">A display name for the object.</span></span> <span data-ttu-id="87341-126">Esta propiedad se hereda del [**\_ SettingData de CIM**](/previous-versions//cc136911(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="87341-126">This property is inherited from [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="87341-127">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="87341-127">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87341-128">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87341-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87341-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87341-129">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="87341-130">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="87341-130">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="87341-131">Identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="87341-131">Uniquely identifies an instance of this class.</span></span> <span data-ttu-id="87341-132">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="87341-132">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="87341-133">**Métrica**</span><span class="sxs-lookup"><span data-stu-id="87341-133">**Metric**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87341-134">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="87341-134">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="87341-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87341-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87341-136">La métrica de prioridad de esta red para la migración.</span><span class="sxs-lookup"><span data-stu-id="87341-136">The priority metric of this network for migration.</span></span> <span data-ttu-id="87341-137">Los valores más bajos tienen mayor prioridad.</span><span class="sxs-lookup"><span data-stu-id="87341-137">Lower values are higher in priority.</span></span>

</dd> <dt>

<span data-ttu-id="87341-138">**PrefixLength**</span><span class="sxs-lookup"><span data-stu-id="87341-138">**PrefixLength**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87341-139">Tipo de datos: **Uint8**</span><span class="sxs-lookup"><span data-stu-id="87341-139">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="87341-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87341-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87341-141">La longitud del prefijo de subred de la red de migración.</span><span class="sxs-lookup"><span data-stu-id="87341-141">The migration network subnet prefix length.</span></span>

</dd> <dt>

<span data-ttu-id="87341-142">**SubnetNumber**</span><span class="sxs-lookup"><span data-stu-id="87341-142">**SubnetNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87341-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="87341-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="87341-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87341-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87341-145">El número de subred de la red de migración.</span><span class="sxs-lookup"><span data-stu-id="87341-145">The migration network subnet number.</span></span>

</dd> <dt>

<span data-ttu-id="87341-146">**Etiquetas**</span><span class="sxs-lookup"><span data-stu-id="87341-146">**Tags**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="87341-147">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="87341-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="87341-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="87341-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="87341-149">Una matriz de etiquetas para representar el sistema de administración que ha configurado esta red para el servicio de migración de sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="87341-149">An array of tags to represent which management system has set this network for virtual system migration service.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="87341-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87341-150">Requirements</span></span>



| <span data-ttu-id="87341-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="87341-151">Requirement</span></span> | <span data-ttu-id="87341-152">Value</span><span class="sxs-lookup"><span data-stu-id="87341-152">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87341-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87341-153">Minimum supported client</span></span><br/> | <span data-ttu-id="87341-154">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="87341-154">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="87341-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="87341-155">Minimum supported server</span></span><br/> | <span data-ttu-id="87341-156">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="87341-156">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="87341-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="87341-157">Namespace</span></span><br/>                | <span data-ttu-id="87341-158">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="87341-158">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="87341-159">MOF</span><span class="sxs-lookup"><span data-stu-id="87341-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="87341-160"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="87341-160"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="87341-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="87341-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87341-162"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="87341-162"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="87341-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="87341-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87341-164">**SettingData de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="87341-164">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> <dt>

[<span data-ttu-id="87341-165">**ModifyNetworkSettings**</span><span class="sxs-lookup"><span data-stu-id="87341-165">**ModifyNetworkSettings**</span></span>](modifynetworksettings-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

