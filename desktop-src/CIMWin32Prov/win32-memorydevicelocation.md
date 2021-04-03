---
description: La \_ clase WMI MemoryDeviceLocation Association de Win32 relaciona un dispositivo de memoria y la memoria física en la que existe.
ms.assetid: 6fef916e-44e2-4b9f-94b7-c7204259004a
ms.tgt_platform: multiple
title: Win32_MemoryDeviceLocation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_MemoryDeviceLocation
- Win32_MemoryDeviceLocation.Dependent
- Win32_MemoryDeviceLocation.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5cf1ba93a2574810892443aefa43e1c7c501636c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998154"
---
# <a name="win32_memorydevicelocation-class"></a><span data-ttu-id="9615f-103">\_Clase Win32 MemoryDeviceLocation</span><span class="sxs-lookup"><span data-stu-id="9615f-103">Win32\_MemoryDeviceLocation class</span></span>

<span data-ttu-id="9615f-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ MemoryDeviceLocation** Association de Win32 relaciona un dispositivo de memoria y la memoria física en la que existe.</span><span class="sxs-lookup"><span data-stu-id="9615f-104">The **Win32\_MemoryDeviceLocation** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a memory device and the physical memory on which it exists.</span></span>

<span data-ttu-id="9615f-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9615f-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="9615f-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9615f-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9615f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9615f-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B9C-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_MemoryDeviceLocation : CIM_Realizes
{
  Win32_MemoryDevice   REF Dependent;
  Win32_PhysicalMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="9615f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="9615f-108">Members</span></span>

<span data-ttu-id="9615f-109">La **clase \_ MemoryDeviceLocation de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9615f-109">The **Win32\_MemoryDeviceLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="9615f-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9615f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9615f-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9615f-111">Properties</span></span>

<span data-ttu-id="9615f-112">La **clase \_ MemoryDeviceLocation de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9615f-112">The **Win32\_MemoryDeviceLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9615f-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="9615f-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9615f-114">Tipo de datos: **Win32 \_ PhysicalMemory**</span><span class="sxs-lookup"><span data-stu-id="9615f-114">Data type: **Win32\_PhysicalMemory**</span></span>
</dt> <dt>

<span data-ttu-id="9615f-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9615f-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9615f-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ PhysicalMemory")</span><span class="sxs-lookup"><span data-stu-id="9615f-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_PhysicalMemory")</span></span>
</dt> </dl>

<span data-ttu-id="9615f-117">[**\_ PhysicalMemory de Win32**](win32-physicalmemory.md) que representa la memoria física que contiene el dispositivo de memoria.</span><span class="sxs-lookup"><span data-stu-id="9615f-117">A [**Win32\_PhysicalMemory**](win32-physicalmemory.md) that represents the physical memory containing the memory device.</span></span>

</dd> <dt>

<span data-ttu-id="9615f-118">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="9615f-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9615f-119">Tipo de datos: **Win32 \_ MemoryDevice**</span><span class="sxs-lookup"><span data-stu-id="9615f-119">Data type: **Win32\_MemoryDevice**</span></span>
</dt> <dt>

<span data-ttu-id="9615f-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9615f-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9615f-121">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ MemoryDevice")</span><span class="sxs-lookup"><span data-stu-id="9615f-121">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_MemoryDevice")</span></span>
</dt> </dl>

<span data-ttu-id="9615f-122">**\_ MemoryDeviceLocation de Win32** que representa el dispositivo de memoria existente en la memoria física.</span><span class="sxs-lookup"><span data-stu-id="9615f-122">A **Win32\_MemoryDeviceLocation** that represents the memory device existing in the physical memory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9615f-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9615f-123">Remarks</span></span>

<span data-ttu-id="9615f-124">La **clase \_ MemoryDeviceLocation de Win32** se deriva de los [**\_ beneficios de CIM**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="9615f-124">The **Win32\_MemoryDeviceLocation** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9615f-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9615f-125">Requirements</span></span>



| <span data-ttu-id="9615f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="9615f-126">Requirement</span></span> | <span data-ttu-id="9615f-127">Value</span><span class="sxs-lookup"><span data-stu-id="9615f-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9615f-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9615f-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9615f-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9615f-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9615f-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9615f-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9615f-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9615f-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9615f-132">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9615f-132">Namespace</span></span><br/>                | <span data-ttu-id="9615f-133">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9615f-133">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9615f-134">MOF</span><span class="sxs-lookup"><span data-stu-id="9615f-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9615f-135"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9615f-135"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9615f-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9615f-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9615f-137"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9615f-137"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9615f-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="9615f-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9615f-139">**Contrataciones \_ de CIM**</span><span class="sxs-lookup"><span data-stu-id="9615f-139">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> <dt>

[<span data-ttu-id="9615f-140">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="9615f-140">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

