---
description: Representa una asociación entre un trabajo y el elemento administrado que puede verse afectado por su ejecución.
ms.assetid: 125A4976-A4E3-4D7A-A43B-86045C3B00AE
title: Msvm_AffectedJobElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedJobElement
- Msvm_AffectedJobElement.AffectedElement
- Msvm_AffectedJobElement.AffectingElement
- Msvm_AffectedJobElement.ElementEffects
- Msvm_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bef667872a7afa4c726ee1b2c77a36c29649114d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688120"
---
# <a name="msvm_affectedjobelement-class"></a><span data-ttu-id="33ffd-103">MSVM \_ AffectedJobElement (clase)</span><span class="sxs-lookup"><span data-stu-id="33ffd-103">Msvm\_AffectedJobElement class</span></span>

<span data-ttu-id="33ffd-104">Representa una asociación entre un trabajo y el elemento administrado que puede verse afectado por su ejecución.</span><span class="sxs-lookup"><span data-stu-id="33ffd-104">Represents an association between a job and the managed element that may be affected by its execution.</span></span>

<span data-ttu-id="33ffd-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="33ffd-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="33ffd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33ffd-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_ConcreteJob   REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="33ffd-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="33ffd-107">Members</span></span>

<span data-ttu-id="33ffd-108">La clase **MSVM \_ AffectedJobElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="33ffd-108">The **Msvm\_AffectedJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="33ffd-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="33ffd-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="33ffd-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="33ffd-110">Properties</span></span>

<span data-ttu-id="33ffd-111">La clase **MSVM \_ AffectedJobElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="33ffd-111">The **Msvm\_AffectedJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="33ffd-112">**AffectedElement**</span><span class="sxs-lookup"><span data-stu-id="33ffd-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ffd-113">Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="33ffd-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="33ffd-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="33ffd-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33ffd-115">Elemento administrado que se ve afectado por la ejecución del trabajo.</span><span class="sxs-lookup"><span data-stu-id="33ffd-115">The managed element affected by the execution of the job.</span></span> <span data-ttu-id="33ffd-116">Esta propiedad se hereda de [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33ffd-116">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="33ffd-117">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="33ffd-117">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ffd-118">Tipo de datos: **[ **MSVM \_ ConcreteJob**](msvm-concretejob.md)**</span><span class="sxs-lookup"><span data-stu-id="33ffd-118">Data type: **[**Msvm\_ConcreteJob**](msvm-concretejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="33ffd-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="33ffd-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33ffd-120">El trabajo que afecta al elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="33ffd-120">The job that is affecting the managed element.</span></span> <span data-ttu-id="33ffd-121">Esta propiedad se hereda de [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33ffd-121">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="33ffd-122">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="33ffd-122">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ffd-123">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="33ffd-123">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="33ffd-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="33ffd-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33ffd-125">Una enumeración que describe el efecto en el elemento administrado.</span><span class="sxs-lookup"><span data-stu-id="33ffd-125">An enumeration that describes the effect on the managed element.</span></span> <span data-ttu-id="33ffd-126">Esta propiedad se hereda de [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33ffd-126">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="33ffd-127">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="33ffd-127">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="33ffd-128">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="33ffd-128">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="33ffd-129">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="33ffd-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="33ffd-130">Proporciona detalles sobre el efecto en la posición de la matriz correspondiente en **ElementEffects**.</span><span class="sxs-lookup"><span data-stu-id="33ffd-130">Provides details for the effect at the corresponding array position in **ElementEffects**.</span></span> <span data-ttu-id="33ffd-131">Esta propiedad se hereda de [**\_ AffectedJobElement CIM**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="33ffd-131">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="33ffd-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33ffd-132">Remarks</span></span>

<span data-ttu-id="33ffd-133">El acceso a la clase **MSVM \_ AffectedJobElement** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="33ffd-133">Access to the **Msvm\_AffectedJobElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="33ffd-134">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="33ffd-134">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="33ffd-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33ffd-135">Requirements</span></span>



| <span data-ttu-id="33ffd-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="33ffd-136">Requirement</span></span> | <span data-ttu-id="33ffd-137">Value</span><span class="sxs-lookup"><span data-stu-id="33ffd-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33ffd-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33ffd-138">Minimum supported client</span></span><br/> | <span data-ttu-id="33ffd-139">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="33ffd-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="33ffd-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="33ffd-140">Minimum supported server</span></span><br/> | <span data-ttu-id="33ffd-141">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="33ffd-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="33ffd-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="33ffd-142">Namespace</span></span><br/>                | <span data-ttu-id="33ffd-143">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="33ffd-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="33ffd-144">MOF</span><span class="sxs-lookup"><span data-stu-id="33ffd-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="33ffd-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="33ffd-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="33ffd-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="33ffd-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="33ffd-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="33ffd-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="33ffd-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="33ffd-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ffd-149">**\_AFFECTEDJOBELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="33ffd-149">**CIM\_AffectedJobElement**</span></span>](cim-affectedjobelement.md)
</dt> <dt>

<span data-ttu-id="33ffd-150">[**\_AFFECTEDJOBELEMENT CIM**](/previous-versions//cc150663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="33ffd-150">[**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="33ffd-151">Clases de administración de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="33ffd-151">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

