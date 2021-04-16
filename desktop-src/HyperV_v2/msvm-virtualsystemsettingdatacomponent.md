---
description: Asociación genérica que se usa para establecer parte de las relaciones entre una instancia de CIM \_ VirtualSystemSettingData y una o más instancias de ResourceAllocationSettingData de CIM \_ .
ms.assetid: 936B41E7-1B3B-4A7B-86F0-E2F4497CE610
title: Msvm_VirtualSystemSettingDataComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingDataComponent
- Msvm_VirtualSystemSettingDataComponent.GroupComponent
- Msvm_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfff3981d6fdb9fdb0368fa887c559026fc10af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666321"
---
# <a name="msvm_virtualsystemsettingdatacomponent-class"></a><span data-ttu-id="0c31d-103">MSVM \_ VirtualSystemSettingDataComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="0c31d-103">Msvm\_VirtualSystemSettingDataComponent class</span></span>

<span data-ttu-id="0c31d-104">Una asociación genérica que se usa para establecer relaciones de ' parte de ' entre una instancia de [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) y una o más instancias de [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span><span class="sxs-lookup"><span data-stu-id="0c31d-104">A generic association used to establish 'part of' relationships between one instance of [**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) and one or more instances of [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

<span data-ttu-id="0c31d-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0c31d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c31d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0c31d-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingDataComponent : CIM_VirtualSystemSettingDataComponent
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="0c31d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="0c31d-107">Members</span></span>

<span data-ttu-id="0c31d-108">La clase **MSVM \_ VirtualSystemSettingDataComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0c31d-108">The **Msvm\_VirtualSystemSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="0c31d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c31d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0c31d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0c31d-110">Properties</span></span>

<span data-ttu-id="0c31d-111">La clase **MSVM \_ VirtualSystemSettingDataComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0c31d-111">The **Msvm\_VirtualSystemSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0c31d-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="0c31d-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c31d-113">Tipo de datos: **[ **CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="0c31d-113">Data type: **[**CIM\_VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))**</span></span>
</dt> <dt>

<span data-ttu-id="0c31d-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c31d-114">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0c31d-115">Calificadores: **override**, **min** (1), **Max** (1)</span><span class="sxs-lookup"><span data-stu-id="0c31d-115">Qualifiers: **Override**, **Min** (1), **Max** (1)</span></span>
</dt> </dl>

<span data-ttu-id="0c31d-116">Elemento primario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="0c31d-116">The parent element in the association.</span></span> <span data-ttu-id="0c31d-117">Esta propiedad se hereda de [**\_ VirtualSystemSettingDataComponent CIM**](/previous-versions//cc150674(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0c31d-117">This property is inherited from [**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="0c31d-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="0c31d-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0c31d-119">Tipo de datos: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span><span class="sxs-lookup"><span data-stu-id="0c31d-119">Data type: **[**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**</span></span>
</dt> <dt>

<span data-ttu-id="0c31d-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0c31d-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0c31d-121">Elemento secundario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="0c31d-121">The child element in the association.</span></span> <span data-ttu-id="0c31d-122">Esta propiedad se hereda de [**\_ VirtualSystemSettingDataComponent CIM**](/previous-versions//cc150674(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="0c31d-122">This property is inherited from [**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0c31d-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0c31d-123">Remarks</span></span>

<span data-ttu-id="0c31d-124">El acceso a la clase **MSVM \_ VirtualSystemSettingDataComponent** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="0c31d-124">Access to the **Msvm\_VirtualSystemSettingDataComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="0c31d-125">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="0c31d-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="0c31d-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c31d-126">Requirements</span></span>



| <span data-ttu-id="0c31d-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c31d-127">Requirement</span></span> | <span data-ttu-id="0c31d-128">Value</span><span class="sxs-lookup"><span data-stu-id="0c31d-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c31d-129">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c31d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0c31d-130">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0c31d-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="0c31d-131">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c31d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0c31d-132">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0c31d-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0c31d-133">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0c31d-133">Namespace</span></span><br/>                | <span data-ttu-id="0c31d-134">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="0c31d-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="0c31d-135">MOF</span><span class="sxs-lookup"><span data-stu-id="0c31d-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0c31d-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0c31d-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0c31d-137">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0c31d-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0c31d-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0c31d-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0c31d-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c31d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c31d-140">**\_VIRTUALSYSTEMSETTINGDATACOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="0c31d-140">**CIM\_VirtualSystemSettingDataComponent**</span></span>](cim-virtualsystemsettingdatacomponent.md)
</dt> <dt>

<span data-ttu-id="0c31d-141">[**\_VIRTUALSYSTEMSETTINGDATACOMPONENT CIM**](/previous-versions//cc150674(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0c31d-141">[**CIM\_VirtualSystemSettingDataComponent**](/previous-versions//cc150674(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="0c31d-142">Clases de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="0c31d-142">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

