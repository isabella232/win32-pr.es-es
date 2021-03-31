---
description: Asocia una instancia de máquina virtual con el servicio de administración que controla su estado.
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Msvm_ServiceAffectsElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceAffectsElement
- Msvm_ServiceAffectsElement.AffectedElement
- Msvm_ServiceAffectsElement.AffectingElement
- Msvm_ServiceAffectsElement.ElementEffects
- Msvm_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eadb9f33015091999776b73c83d792ccd29396b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154845"
---
# <a name="msvm_serviceaffectselement-class"></a><span data-ttu-id="ffbe1-103">MSVM \_ ServiceAffectsElement (clase)</span><span class="sxs-lookup"><span data-stu-id="ffbe1-103">Msvm\_ServiceAffectsElement class</span></span>

<span data-ttu-id="ffbe1-104">Asocia una instancia de máquina virtual con el servicio de administración que controla su estado.</span><span class="sxs-lookup"><span data-stu-id="ffbe1-104">Associates a virtual machine instance with the management service that controls its state.</span></span>

<span data-ttu-id="ffbe1-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="ffbe1-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffbe1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ffbe1-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceAffectsElement : CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[] = 5;
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="ffbe1-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="ffbe1-107">Members</span></span>

<span data-ttu-id="ffbe1-108">La clase **MSVM \_ ServiceAffectsElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="ffbe1-108">The **Msvm\_ServiceAffectsElement** class has these types of members:</span></span>

-   [<span data-ttu-id="ffbe1-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ffbe1-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ffbe1-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="ffbe1-110">Properties</span></span>

<span data-ttu-id="ffbe1-111">La clase **MSVM \_ ServiceAffectsElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="ffbe1-111">The **Msvm\_ServiceAffectsElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ffbe1-112">**AffectedElement**</span><span class="sxs-lookup"><span data-stu-id="ffbe1-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffbe1-113">Tipo de datos: **[ **CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="ffbe1-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="ffbe1-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ffbe1-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffbe1-115">Referencia a la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ffbe1-115">A reference to the virtual machine.</span></span> <span data-ttu-id="ffbe1-116">Esta propiedad se hereda de [**\_ ServiceAffectsElement CIM**](/previous-versions//cc136907(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ffbe1-116">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ffbe1-117">**AffectingElement**</span><span class="sxs-lookup"><span data-stu-id="ffbe1-117">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffbe1-118">Tipo de datos: **[ **\_ servicio CIM**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="ffbe1-118">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="ffbe1-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ffbe1-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffbe1-120">Referencia al servicio que controla la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="ffbe1-120">A reference to the service that controls the virtual machine.</span></span> <span data-ttu-id="ffbe1-121">Esta propiedad se hereda de [**\_ ServiceAffectsElement CIM**](/previous-versions//cc136907(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="ffbe1-121">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="ffbe1-122">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="ffbe1-122">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffbe1-123">Tipo de datos: matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="ffbe1-123">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="ffbe1-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ffbe1-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffbe1-125">Especifica el tipo de control que representa la asociación.</span><span class="sxs-lookup"><span data-stu-id="ffbe1-125">Specifies the type of control that the association represents.</span></span> <span data-ttu-id="ffbe1-126">Esta propiedad se hereda de [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))y siempre se establece en el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="ffbe1-126">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)), and it is always set to the following value.</span></span>



| <span data-ttu-id="ffbe1-127">Value</span><span class="sxs-lookup"><span data-stu-id="ffbe1-127">Value</span></span>                                                                        | <span data-ttu-id="ffbe1-128">Significado</span><span class="sxs-lookup"><span data-stu-id="ffbe1-128">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="ffbe1-129"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="ffbe1-129"><dt>5</dt></span></span> </dl> | <span data-ttu-id="ffbe1-130">Administra</span><span class="sxs-lookup"><span data-stu-id="ffbe1-130">Manages</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="ffbe1-131">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="ffbe1-131">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffbe1-132">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="ffbe1-132">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="ffbe1-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="ffbe1-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ffbe1-134">Los detalles del tipo de asociación en la posición de la matriz correspondiente en la matriz de propiedades **ElementAffects** .</span><span class="sxs-lookup"><span data-stu-id="ffbe1-134">The details for the type of association at the corresponding array position in the **ElementAffects** property array.</span></span> <span data-ttu-id="ffbe1-135">Esta información es necesaria si **ElementAffects** está establecido en 1 (otro).</span><span class="sxs-lookup"><span data-stu-id="ffbe1-135">This information is required if **ElementAffects** is set to 1 (Other).</span></span> <span data-ttu-id="ffbe1-136">Esta propiedad se hereda de [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))y siempre está establecida en **null**.</span><span class="sxs-lookup"><span data-stu-id="ffbe1-136">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ffbe1-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ffbe1-137">Remarks</span></span>

<span data-ttu-id="ffbe1-138">El acceso a la clase **MSVM \_ ServiceAffectsElement** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="ffbe1-138">Access to the **Msvm\_ServiceAffectsElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="ffbe1-139">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="ffbe1-139">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="ffbe1-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffbe1-140">Requirements</span></span>



| <span data-ttu-id="ffbe1-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffbe1-141">Requirement</span></span> | <span data-ttu-id="ffbe1-142">Value</span><span class="sxs-lookup"><span data-stu-id="ffbe1-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffbe1-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffbe1-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ffbe1-144">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="ffbe1-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ffbe1-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ffbe1-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ffbe1-146">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="ffbe1-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ffbe1-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ffbe1-147">Namespace</span></span><br/>                | <span data-ttu-id="ffbe1-148">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="ffbe1-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ffbe1-149">MOF</span><span class="sxs-lookup"><span data-stu-id="ffbe1-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ffbe1-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ffbe1-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ffbe1-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ffbe1-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffbe1-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ffbe1-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ffbe1-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="ffbe1-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffbe1-154">**\_SERVICEAFFECTSELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="ffbe1-154">**CIM\_ServiceAffectsElement**</span></span>](cim-serviceaffectselement.md)
</dt> <dt>

<span data-ttu-id="ffbe1-155">[**\_SERVICEAFFECTSELEMENT CIM**](/previous-versions//cc136907(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ffbe1-155">[**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))</span></span>
</dt> </dl>

 

