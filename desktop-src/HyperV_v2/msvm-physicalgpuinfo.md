---
description: Contiene información sobre una unidad de procesamiento de gráficos (GPU) física de RemoteFX.
ms.assetid: 86B47AAE-DBFF-43EF-88C6-44836D6C3AFA
title: Msvm_PhysicalGPUInfo (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PhysicalGPUInfo
- Msvm_PhysicalGPUInfo.InstanceID
- Msvm_PhysicalGPUInfo.Caption
- Msvm_PhysicalGPUInfo.Description
- Msvm_PhysicalGPUInfo.ElementName
- Msvm_PhysicalGPUInfo.Name
- Msvm_PhysicalGPUInfo.ID
- Msvm_PhysicalGPUInfo.TotalVideoMemory
- Msvm_PhysicalGPUInfo.AvailableVideoMemory
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cd4ccf65b364620e84063ea6398c59dd0e467f67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669761"
---
# <a name="msvm_physicalgpuinfo-class"></a><span data-ttu-id="d9690-103">MSVM \_ PhysicalGPUInfo (clase)</span><span class="sxs-lookup"><span data-stu-id="d9690-103">Msvm\_PhysicalGPUInfo class</span></span>

<span data-ttu-id="d9690-104">Contiene información sobre una unidad de procesamiento de gráficos (GPU) física de RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="d9690-104">Contains information about a RemoteFX physical graphics processing unit (GPU).</span></span>

<span data-ttu-id="d9690-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="d9690-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9690-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d9690-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PhysicalGPUInfo : CIM_ManagedElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  string ID;
  uint64 TotalVideoMemory;
  uint64 AvailableVideoMemory;
};
```

## <a name="members"></a><span data-ttu-id="d9690-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d9690-107">Members</span></span>

<span data-ttu-id="d9690-108">La clase **MSVM \_ PhysicalGPUInfo** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d9690-108">The **Msvm\_PhysicalGPUInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="d9690-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9690-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d9690-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d9690-110">Properties</span></span>

<span data-ttu-id="d9690-111">La clase **MSVM \_ PhysicalGPUInfo** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d9690-111">The **Msvm\_PhysicalGPUInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d9690-112">**AvailableVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="d9690-112">**AvailableVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9690-113">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d9690-113">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d9690-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d9690-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9690-115">La cantidad de memoria de vídeo sin usar, en bytes, en la GPU física que puede usar RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="d9690-115">The amount of unused video memory, in bytes, on the physical GPU that can be used by RemoteFX.</span></span>

</dd> <dt>

<span data-ttu-id="d9690-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="d9690-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9690-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d9690-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9690-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d9690-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9690-119">Breve descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d9690-119">A short description of the object.</span></span> <span data-ttu-id="d9690-120">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d9690-120">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d9690-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="d9690-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9690-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d9690-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9690-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d9690-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9690-124">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="d9690-124">A description of the object.</span></span> <span data-ttu-id="d9690-125">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d9690-125">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d9690-126">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="d9690-126">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9690-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d9690-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9690-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d9690-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9690-129">Nombre para mostrar del objeto.</span><span class="sxs-lookup"><span data-stu-id="d9690-129">A display name for the object.</span></span> <span data-ttu-id="d9690-130">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d9690-130">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d9690-131">**Id**</span><span class="sxs-lookup"><span data-stu-id="d9690-131">**ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9690-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d9690-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9690-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d9690-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9690-134">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="d9690-134">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="d9690-135">Identificador único de la GPU física.</span><span class="sxs-lookup"><span data-stu-id="d9690-135">The unique identifier of the physical GPU.</span></span>

</dd> <dt>

<span data-ttu-id="d9690-136">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="d9690-136">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9690-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d9690-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9690-138">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d9690-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9690-139">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="d9690-139">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="d9690-140">Cadena que identifica de forma única una instancia de esta clase.</span><span class="sxs-lookup"><span data-stu-id="d9690-140">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="d9690-141">Esta propiedad se hereda de [**\_ ManagedElement de CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="d9690-141">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="d9690-142">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="d9690-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9690-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="d9690-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="d9690-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d9690-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d9690-145">Calificadores: [**Maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="d9690-145">Qualifiers: [**MAXLEN**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="d9690-146">Nombre para mostrar de la GPU física.</span><span class="sxs-lookup"><span data-stu-id="d9690-146">The display name of the physical GPU.</span></span>

</dd> <dt>

<span data-ttu-id="d9690-147">**TotalVideoMemory**</span><span class="sxs-lookup"><span data-stu-id="d9690-147">**TotalVideoMemory**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d9690-148">Tipo de datos: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="d9690-148">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="d9690-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="d9690-149">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="d9690-150">La cantidad total de memoria de vídeo, en bytes, en la GPU física que puede usar RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="d9690-150">The total amount of video memory, in bytes, on the physical GPU that can be used by RemoteFX.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9690-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d9690-151">Requirements</span></span>



| <span data-ttu-id="d9690-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9690-152">Requirement</span></span> | <span data-ttu-id="d9690-153">Value</span><span class="sxs-lookup"><span data-stu-id="d9690-153">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9690-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9690-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d9690-155">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9690-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d9690-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d9690-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d9690-157">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d9690-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d9690-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d9690-158">Namespace</span></span><br/>                | <span data-ttu-id="d9690-159">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="d9690-159">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="d9690-160">MOF</span><span class="sxs-lookup"><span data-stu-id="d9690-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9690-161"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9690-161"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9690-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d9690-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9690-163"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d9690-163"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d9690-164">Vea también</span><span class="sxs-lookup"><span data-stu-id="d9690-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9690-165">**ManagedElement de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="d9690-165">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

