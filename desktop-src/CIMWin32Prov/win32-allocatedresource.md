---
description: La \_ clase WMI AllocatedResource Association de Win32 relaciona un dispositivo lógico con un recurso del sistema. Esta clase se usa para detectar qué recursos, como IRQ o canales DMA, están en uso por un dispositivo específico.
ms.assetid: cfac1209-1405-4fee-847c-8a61504bfac1
ms.tgt_platform: multiple
title: Win32_AllocatedResource (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AllocatedResource
- Win32_AllocatedResource.Dependent
- Win32_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 87a57e53a85e4433ae325fc2ed441211db75b79f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000761"
---
# <a name="win32_allocatedresource-class"></a><span data-ttu-id="bea7e-104">\_Clase Win32 AllocatedResource</span><span class="sxs-lookup"><span data-stu-id="bea7e-104">Win32\_AllocatedResource class</span></span>

<span data-ttu-id="bea7e-105">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ AllocatedResource** Association de Win32 relaciona un dispositivo lógico con un recurso del sistema.</span><span class="sxs-lookup"><span data-stu-id="bea7e-105">The **Win32\_AllocatedResource** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a logical device to a system resource.</span></span> <span data-ttu-id="bea7e-106">Esta clase se usa para detectar qué recursos, como IRQ o canales DMA, están en uso por un dispositivo específico.</span><span class="sxs-lookup"><span data-stu-id="bea7e-106">This class is used to discover which resources, such as IRQs or DMA channels, are in use by a specific device.</span></span>

<span data-ttu-id="bea7e-107">Esta clase está obsoleta.</span><span class="sxs-lookup"><span data-stu-id="bea7e-107">This class is obsolete.</span></span> <span data-ttu-id="bea7e-108">En lugar de esta clase, debe utilizar las propiedades de la clase [**\_ PNPAllocatedResource de Win32**](win32-pnpallocatedresource.md) .</span><span class="sxs-lookup"><span data-stu-id="bea7e-108">In place of this class, you should use the properties in the [**Win32\_PNPAllocatedResource**](win32-pnpallocatedresource.md) class.</span></span>

<span data-ttu-id="bea7e-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="bea7e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="bea7e-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="bea7e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bea7e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bea7e-111">Syntax</span></span>

``` syntax
[DEPRECATED, Dynamic, Provider("CIMWin32"), UUID("{8502C50D-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="bea7e-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="bea7e-112">Members</span></span>

<span data-ttu-id="bea7e-113">La **clase \_ AllocatedResource de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bea7e-113">The **Win32\_AllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="bea7e-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bea7e-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bea7e-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bea7e-115">Properties</span></span>

<span data-ttu-id="bea7e-116">La **clase \_ AllocatedResource de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bea7e-116">The **Win32\_AllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bea7e-117">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="bea7e-117">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea7e-118">Tipo de datos: **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="bea7e-118">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="bea7e-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bea7e-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bea7e-120">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \| CIM \_ SystemResource")</span><span class="sxs-lookup"><span data-stu-id="bea7e-120">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_SystemResource")</span></span>
</dt> </dl>

<span data-ttu-id="bea7e-121">Un [**\_ SystemResource de CIM**](cim-systemresource.md) que describe las propiedades de un recurso del sistema disponible para el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="bea7e-121">A [**CIM\_SystemResource**](cim-systemresource.md) that describes the properties of a system resource available to the logical device.</span></span>

</dd> <dt>

<span data-ttu-id="bea7e-122">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="bea7e-122">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bea7e-123">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="bea7e-123">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="bea7e-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bea7e-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bea7e-125">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| lógico CIM CIM \_ ")</span><span class="sxs-lookup"><span data-stu-id="bea7e-125">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\|CIM\_LogicalDevice")</span></span>
</dt> </dl>

<span data-ttu-id="bea7e-126">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que representa las propiedades del dispositivo lógico que está usando los recursos del sistema asignados a él.</span><span class="sxs-lookup"><span data-stu-id="bea7e-126">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that represents the properties of the logical device that is using the system resources assigned to it.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bea7e-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bea7e-127">Remarks</span></span>

<span data-ttu-id="bea7e-128">La **clase \_ AllocatedResource de Win32** se deriva de la [**\_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="bea7e-128">The **Win32\_AllocatedResource** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bea7e-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bea7e-129">Requirements</span></span>



| <span data-ttu-id="bea7e-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="bea7e-130">Requirement</span></span> | <span data-ttu-id="bea7e-131">Value</span><span class="sxs-lookup"><span data-stu-id="bea7e-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bea7e-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bea7e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bea7e-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bea7e-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bea7e-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bea7e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bea7e-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bea7e-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bea7e-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bea7e-136">Namespace</span></span><br/>                | <span data-ttu-id="bea7e-137">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bea7e-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bea7e-138">MOF</span><span class="sxs-lookup"><span data-stu-id="bea7e-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bea7e-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bea7e-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bea7e-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bea7e-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bea7e-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bea7e-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bea7e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="bea7e-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bea7e-143">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="bea7e-143">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> <dt>

[<span data-ttu-id="bea7e-144">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="bea7e-144">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

