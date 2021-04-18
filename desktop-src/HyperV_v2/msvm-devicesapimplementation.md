---
description: Una asociación entre un punto de acceso al servicio (SAP) y cómo se implementa.
ms.assetid: 36108521-A699-4498-A962-DC0801D9EE81
title: Msvm_DeviceSAPImplementation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DeviceSAPImplementation
- Msvm_DeviceSAPImplementation.Antecedent
- Msvm_DeviceSAPImplementation.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9551d4409edfdfca18b66e3a3b86d6adcb28b19c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667821"
---
# <a name="msvm_devicesapimplementation-class"></a><span data-ttu-id="9c2b7-103">MSVM \_ DeviceSAPImplementation (clase)</span><span class="sxs-lookup"><span data-stu-id="9c2b7-103">Msvm\_DeviceSAPImplementation class</span></span>

<span data-ttu-id="9c2b7-104">Una asociación entre un punto de acceso al servicio (SAP) y cómo se implementa.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="9c2b7-105">La cardinalidad de esta asociación es de varios a varios.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="9c2b7-106">Un SAP puede ser proporcionado por más de un dispositivo lógico, que funciona conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="9c2b7-107">Cualquier dispositivo puede proporcionar más de un SAP.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="9c2b7-108">Cuando muchos dispositivos lógicos están asociados a un único SAP, se supone que estos elementos funcionan conjuntamente para proporcionar el punto de acceso.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="9c2b7-109">Si existen implementaciones diferentes de un SAP, cada una de estas implementaciones produciría instancias individuales del objeto SAP.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="9c2b7-110">Estas creaciones de instancias individuales tendrían asociaciones con las implementaciones únicas.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="9c2b7-111">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c2b7-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9c2b7-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="9c2b7-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="9c2b7-113">Members</span></span>

<span data-ttu-id="9c2b7-114">La clase **MSVM \_ DeviceSAPImplementation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9c2b7-114">The **Msvm\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="9c2b7-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9c2b7-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9c2b7-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9c2b7-116">Properties</span></span>

<span data-ttu-id="9c2b7-117">La clase **MSVM \_ DeviceSAPImplementation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-117">The **Msvm\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9c2b7-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="9c2b7-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c2b7-119">Tipo de datos: **[ **\_ LogicalDevice de CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="9c2b7-119">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="9c2b7-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c2b7-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c2b7-121">El dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-121">The logical device.</span></span> <span data-ttu-id="9c2b7-122">Esta propiedad se hereda de [**\_ DeviceSAPImplementation CIM**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span><span class="sxs-lookup"><span data-stu-id="9c2b7-122">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> <dt>

<span data-ttu-id="9c2b7-123">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="9c2b7-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9c2b7-124">Tipo de datos: **[ **CIM \_ punto**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span><span class="sxs-lookup"><span data-stu-id="9c2b7-124">Data type: **[**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span></span>
</dt> <dt>

<span data-ttu-id="9c2b7-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9c2b7-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9c2b7-126">El punto de acceso al servicio implementado mediante el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-126">The service access point implemented using the logical device.</span></span> <span data-ttu-id="9c2b7-127">Esta propiedad se hereda de [**\_ DeviceSAPImplementation CIM**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span><span class="sxs-lookup"><span data-stu-id="9c2b7-127">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9c2b7-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9c2b7-128">Remarks</span></span>

<span data-ttu-id="9c2b7-129">El acceso a la clase **MSVM \_ DeviceSAPImplementation** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="9c2b7-129">Access to the **Msvm\_DeviceSAPImplementation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="9c2b7-130">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="9c2b7-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="9c2b7-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9c2b7-131">Examples</span></span>

<span data-ttu-id="9c2b7-132">Consulte [consultar objetos de red](querying-networking-objects.md).</span><span class="sxs-lookup"><span data-stu-id="9c2b7-132">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9c2b7-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9c2b7-133">Requirements</span></span>



| <span data-ttu-id="9c2b7-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="9c2b7-134">Requirement</span></span> | <span data-ttu-id="9c2b7-135">Value</span><span class="sxs-lookup"><span data-stu-id="9c2b7-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c2b7-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c2b7-136">Minimum supported client</span></span><br/> | <span data-ttu-id="9c2b7-137">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c2b7-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9c2b7-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9c2b7-138">Minimum supported server</span></span><br/> | <span data-ttu-id="9c2b7-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="9c2b7-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9c2b7-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9c2b7-140">Namespace</span></span><br/>                | <span data-ttu-id="9c2b7-141">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="9c2b7-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9c2b7-142">MOF</span><span class="sxs-lookup"><span data-stu-id="9c2b7-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9c2b7-143"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9c2b7-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9c2b7-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9c2b7-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c2b7-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9c2b7-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="9c2b7-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="9c2b7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c2b7-147">**\_DEVICESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="9c2b7-147">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dt>

[<span data-ttu-id="9c2b7-148">**\_DEVICESAPIMPLEMENTATION CIM**</span><span class="sxs-lookup"><span data-stu-id="9c2b7-148">**CIM\_DeviceSAPImplementation**</span></span>](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 

