---
description: 'Msvm_DeviceSAPImplementation clase : asociación entre un punto de acceso de servicio (SAP) y cómo se implementa.'
ms.assetid: 36108521-A699-4498-A962-DC0801D9EE81
title: Msvm_DeviceSAPImplementation clase
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
ms.openlocfilehash: 6fbe3c9b85e0a8c9f0c6a07d1db03784c4ac15e6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112103"
---
# <a name="msvm_devicesapimplementation-class"></a><span data-ttu-id="b2de5-103">Clase Msvm \_ DeviceSAPImplementation</span><span class="sxs-lookup"><span data-stu-id="b2de5-103">Msvm\_DeviceSAPImplementation class</span></span>

<span data-ttu-id="b2de5-104">Asociación entre un punto de acceso de servicio (SAP) y cómo se implementa.</span><span class="sxs-lookup"><span data-stu-id="b2de5-104">An association between a service access point (SAP) and how it is implemented.</span></span> <span data-ttu-id="b2de5-105">La cardinalidad de esta asociación es de varios a varios.</span><span class="sxs-lookup"><span data-stu-id="b2de5-105">The cardinality of this association is many-to-many.</span></span> <span data-ttu-id="b2de5-106">Un SAP se puede proporcionar mediante más de un dispositivo lógico, que funciona conjuntamente.</span><span class="sxs-lookup"><span data-stu-id="b2de5-106">A SAP can be provided by more than one logical device, operating in conjunction.</span></span> <span data-ttu-id="b2de5-107">Cualquier dispositivo puede proporcionar más de un SAP.</span><span class="sxs-lookup"><span data-stu-id="b2de5-107">Any device can provide more than one SAP.</span></span> <span data-ttu-id="b2de5-108">Cuando muchos dispositivos lógicos están asociados a un único SAP, se supone que estos elementos funcionan juntos para proporcionar el punto de acceso.</span><span class="sxs-lookup"><span data-stu-id="b2de5-108">When many logical devices are associated with a single SAP, it is assumed that these elements operate in conjunction to provide the access point.</span></span> <span data-ttu-id="b2de5-109">Si existen implementaciones diferentes de un SAP, cada una de estas implementaciones daría como resultado instancias individuales del objeto de SAP.</span><span class="sxs-lookup"><span data-stu-id="b2de5-109">If different implementations of a SAP exist, each of these implementations would result in individual instantiations of the SAP object.</span></span> <span data-ttu-id="b2de5-110">Estas instancias individuales tendrían entonces asociaciones con las implementaciones únicas.</span><span class="sxs-lookup"><span data-stu-id="b2de5-110">These individual instantiations would then have associations to the unique implementations.</span></span>

<span data-ttu-id="b2de5-111">La sintaxis siguiente se simplifica Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b2de5-111">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2de5-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2de5-112">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_DeviceSAPImplementation : CIM_DeviceSAPImplementation
{
  CIM_LogicalDevice      REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="b2de5-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="b2de5-113">Members</span></span>

<span data-ttu-id="b2de5-114">La **clase Msvm \_ DeviceSAPImplementation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b2de5-114">The **Msvm\_DeviceSAPImplementation** class has these types of members:</span></span>

-   [<span data-ttu-id="b2de5-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b2de5-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b2de5-116">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b2de5-116">Properties</span></span>

<span data-ttu-id="b2de5-117">La **clase Msvm \_ DeviceSAPImplementation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b2de5-117">The **Msvm\_DeviceSAPImplementation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b2de5-118">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="b2de5-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2de5-119">Tipo de datos: **[ **\_ Cim LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span><span class="sxs-lookup"><span data-stu-id="b2de5-119">Data type: **[**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice)**</span></span>
</dt> <dt>

<span data-ttu-id="b2de5-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b2de5-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2de5-121">El dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b2de5-121">The logical device.</span></span> <span data-ttu-id="b2de5-122">Esta propiedad se hereda de [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span><span class="sxs-lookup"><span data-stu-id="b2de5-122">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> <dt>

<span data-ttu-id="b2de5-123">**Dependiente**</span><span class="sxs-lookup"><span data-stu-id="b2de5-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b2de5-124">Tipo de datos: **[ **Cim \_ ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span><span class="sxs-lookup"><span data-stu-id="b2de5-124">Data type: **[**CIM\_ServiceAccessPoint**](/windows/desktop/CIMWin32Prov/cim-serviceaccesspoint)**</span></span>
</dt> <dt>

<span data-ttu-id="b2de5-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b2de5-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b2de5-126">Punto de acceso de servicio implementado mediante el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="b2de5-126">The service access point implemented using the logical device.</span></span> <span data-ttu-id="b2de5-127">Esta propiedad se hereda de [**CIM \_ DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span><span class="sxs-lookup"><span data-stu-id="b2de5-127">This property is inherited from [**CIM\_DeviceSAPImplementation**](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b2de5-128">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b2de5-128">Remarks</span></span>

<span data-ttu-id="b2de5-129">El acceso a **la clase \_ Msvm DeviceSAPImplementation** podría estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="b2de5-129">Access to the **Msvm\_DeviceSAPImplementation** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="b2de5-130">Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="b2de5-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="b2de5-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b2de5-131">Examples</span></span>

<span data-ttu-id="b2de5-132">Consulte [Consulta de objetos de red.](querying-networking-objects.md)</span><span class="sxs-lookup"><span data-stu-id="b2de5-132">See [Querying networking objects](querying-networking-objects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b2de5-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2de5-133">Requirements</span></span>



| <span data-ttu-id="b2de5-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2de5-134">Requirement</span></span> | <span data-ttu-id="b2de5-135">Valor</span><span class="sxs-lookup"><span data-stu-id="b2de5-135">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2de5-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2de5-136">Minimum supported client</span></span><br/> | <span data-ttu-id="b2de5-137">Windows 8 solo \[ aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="b2de5-137">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b2de5-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2de5-138">Minimum supported server</span></span><br/> | <span data-ttu-id="b2de5-139">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="b2de5-139">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b2de5-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b2de5-140">Namespace</span></span><br/>                | <span data-ttu-id="b2de5-141">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="b2de5-141">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="b2de5-142">MOF</span><span class="sxs-lookup"><span data-stu-id="b2de5-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b2de5-143"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="b2de5-143"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b2de5-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b2de5-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2de5-145"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b2de5-145"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b2de5-146">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b2de5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2de5-147">**Dispositivos \_ CIMSAPImplementation**</span><span class="sxs-lookup"><span data-stu-id="b2de5-147">**CIM\_DeviceSAPImplementation**</span></span>](cim-devicesapimplementation.md)
</dt> <dt>

[<span data-ttu-id="b2de5-148">**Dispositivos \_ CIMSAPImplementation**</span><span class="sxs-lookup"><span data-stu-id="b2de5-148">**CIM\_DeviceSAPImplementation**</span></span>](/windows/desktop/CIMWin32Prov/cim-devicesapimplementation)
</dt> </dl>

 

