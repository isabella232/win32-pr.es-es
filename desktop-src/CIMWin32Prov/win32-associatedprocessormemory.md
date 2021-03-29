---
description: La \_ clase WMI AssociatedProcessorMemory Association de Win32 relaciona un procesador y su memoria caché.
ms.assetid: 23da2a9d-772e-4258-9489-07d47801b2d8
ms.tgt_platform: multiple
title: Win32_AssociatedProcessorMemory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_AssociatedProcessorMemory
- Win32_AssociatedProcessorMemory.BusSpeed
- Win32_AssociatedProcessorMemory.Dependent
- Win32_AssociatedProcessorMemory.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3737dca869c539d1414c4399f35fb8f107697b70
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000760"
---
# <a name="win32_associatedprocessormemory-class"></a><span data-ttu-id="3cbf1-103">\_Clase Win32 AssociatedProcessorMemory</span><span class="sxs-lookup"><span data-stu-id="3cbf1-103">Win32\_AssociatedProcessorMemory class</span></span>

<span data-ttu-id="3cbf1-104">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ AssociatedProcessorMemory** Association de Win32 relaciona un procesador y su memoria caché.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-104">The **Win32\_AssociatedProcessorMemory** association [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) relates a processor and its cache memory.</span></span>

<span data-ttu-id="3cbf1-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3cbf1-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cbf1-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3cbf1-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{074737F0-ACBC-11d2-ABF6-00805F538618}"), AMENDMENT]
class Win32_AssociatedProcessorMemory : CIM_AssociatedProcessorMemory
{
  uint32                BusSpeed;
  Win32_Processor   REF Dependent;
  Win32_CacheMemory REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="3cbf1-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="3cbf1-108">Members</span></span>

<span data-ttu-id="3cbf1-109">La **clase \_ AssociatedProcessorMemory de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3cbf1-109">The **Win32\_AssociatedProcessorMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="3cbf1-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3cbf1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3cbf1-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3cbf1-111">Properties</span></span>

<span data-ttu-id="3cbf1-112">La **clase \_ AssociatedProcessorMemory de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-112">The **Win32\_AssociatedProcessorMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3cbf1-113">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="3cbf1-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cbf1-114">Tipo de datos: **Win32 \_ CacheMemory**</span><span class="sxs-lookup"><span data-stu-id="3cbf1-114">Data type: **Win32\_CacheMemory**</span></span>
</dt> <dt>

<span data-ttu-id="3cbf1-115">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cbf1-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cbf1-116">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ CacheMemory")</span><span class="sxs-lookup"><span data-stu-id="3cbf1-116">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_CacheMemory")</span></span>
</dt> </dl>

<span data-ttu-id="3cbf1-117">[**\_ CacheMemory de Win32**](win32-cachememory.md) que describe la memoria caché disponible para el procesador.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-117">A [**Win32\_CacheMemory**](win32-cachememory.md) that describes the cache memory available to the processor.</span></span>

</dd> <dt>

<span data-ttu-id="3cbf1-118">**BusSpeed**</span><span class="sxs-lookup"><span data-stu-id="3cbf1-118">**BusSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cbf1-119">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3cbf1-119">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3cbf1-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cbf1-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cbf1-121">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahercios")</span><span class="sxs-lookup"><span data-stu-id="3cbf1-121">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="3cbf1-122">Velocidad del bus, en megahercios (MHz), entre el procesador y la memoria.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-122">Speed of the bus, in megahertz (MHz), between the processor and memory.</span></span>

<span data-ttu-id="3cbf1-123">Esta propiedad se hereda de [**\_ AssociatedProcessorMemory CIM**](cim-associatedprocessormemory.md).</span><span class="sxs-lookup"><span data-stu-id="3cbf1-123">This property is inherited from [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="3cbf1-124">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="3cbf1-124">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3cbf1-125">Tipo de datos **: \_ procesador Win32**</span><span class="sxs-lookup"><span data-stu-id="3cbf1-125">Data type: **Win32\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="3cbf1-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3cbf1-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3cbf1-127">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) (" \| procesador Win32 de WMI \_ ")</span><span class="sxs-lookup"><span data-stu-id="3cbf1-127">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI\|Win32\_Processor")</span></span>
</dt> </dl>

<span data-ttu-id="3cbf1-128">[**\_ Procesador Win32**](win32-processor.md) que describe el procesador que está utilizando la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="3cbf1-128">A [**Win32\_Processor**](win32-processor.md) that describes the processor that is using the cache memory.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3cbf1-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3cbf1-129">Remarks</span></span>

<span data-ttu-id="3cbf1-130">La **clase \_ AssociatedProcessorMemory de Win32** se deriva de [**\_ AssociatedProcessorMemory de CIM**](cim-associatedprocessormemory.md).</span><span class="sxs-lookup"><span data-stu-id="3cbf1-130">The **Win32\_AssociatedProcessorMemory** class is derived from [**CIM\_AssociatedProcessorMemory**](cim-associatedprocessormemory.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3cbf1-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3cbf1-131">Requirements</span></span>



| <span data-ttu-id="3cbf1-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cbf1-132">Requirement</span></span> | <span data-ttu-id="3cbf1-133">Value</span><span class="sxs-lookup"><span data-stu-id="3cbf1-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3cbf1-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cbf1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3cbf1-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3cbf1-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3cbf1-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3cbf1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3cbf1-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3cbf1-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3cbf1-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3cbf1-138">Namespace</span></span><br/>                | <span data-ttu-id="3cbf1-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3cbf1-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3cbf1-140">MOF</span><span class="sxs-lookup"><span data-stu-id="3cbf1-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3cbf1-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3cbf1-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3cbf1-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3cbf1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3cbf1-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3cbf1-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cbf1-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="3cbf1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cbf1-145">**\_ASSOCIATEDPROCESSORMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="3cbf1-145">**CIM\_AssociatedProcessorMemory**</span></span>](cim-associatedprocessormemory.md)
</dt> <dt>

[<span data-ttu-id="3cbf1-146">Clases de hardware de sistema del equipo</span><span class="sxs-lookup"><span data-stu-id="3cbf1-146">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> </dl>

 

