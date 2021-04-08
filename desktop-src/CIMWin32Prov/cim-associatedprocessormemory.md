---
description: La \_ clase AssociatedProcessorMemory de CIM asocia el procesador y la memoria del sistema, o la memoria caché de un procesador.
ms.assetid: a4c28a0a-e4cc-4db2-bd77-b7b5023eace6
ms.tgt_platform: multiple
title: CIM_AssociatedProcessorMemory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedProcessorMemory
- CIM_AssociatedProcessorMemory.Antecedent
- CIM_AssociatedProcessorMemory.Dependent
- CIM_AssociatedProcessorMemory.BusSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f35cdca92cb15e1c6fff215ff1363844e0d47012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000697"
---
# <a name="cim_associatedprocessormemory-class"></a><span data-ttu-id="e200e-103">\_Clase AssociatedProcessorMemory de CIM</span><span class="sxs-lookup"><span data-stu-id="e200e-103">CIM\_AssociatedProcessorMemory class</span></span>

<span data-ttu-id="e200e-104">La **clase \_ AssociatedProcessorMemory de CIM** asocia el procesador y la memoria del sistema, o la memoria caché de un procesador.</span><span class="sxs-lookup"><span data-stu-id="e200e-104">The **CIM\_AssociatedProcessorMemory** class associates the processor and system memory, or a processor's cache.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e200e-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="e200e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e200e-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e200e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e200e-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e200e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="e200e-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="e200e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e200e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e200e-109">Syntax</span></span>

``` syntax
[abstract, UUID("{464FFAB1-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedProcessorMemory : CIM_AssociatedMemory
{
  CIM_Memory    REF Antecedent;
  CIM_Processor REF Dependent;
  uint32            BusSpeed;
};
```

## <a name="members"></a><span data-ttu-id="e200e-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="e200e-110">Members</span></span>

<span data-ttu-id="e200e-111">La clase **CIM \_ AssociatedProcessorMemory** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e200e-111">The **CIM\_AssociatedProcessorMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="e200e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e200e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e200e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e200e-113">Properties</span></span>

<span data-ttu-id="e200e-114">La clase **CIM \_ AssociatedProcessorMemory** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e200e-114">The **CIM\_AssociatedProcessorMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e200e-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="e200e-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e200e-116">Tipo de datos **: \_ memoria CIM**</span><span class="sxs-lookup"><span data-stu-id="e200e-116">Data type: **CIM\_Memory**</span></span>
</dt> <dt>

<span data-ttu-id="e200e-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e200e-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e200e-118">[**\_ Memoria de CIM**](cim-memory.md) que describe la memoria instalada en o asociada a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e200e-118">A [**CIM\_Memory**](cim-memory.md) that describes the memory installed on or associated with a device.</span></span>

<span data-ttu-id="e200e-119">Esta propiedad se hereda de [**\_ AssociatedMemory CIM**](cim-associatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="e200e-119">This property is inherited from [**CIM\_AssociatedMemory**](cim-associatedmemory.md).</span></span>

</dd> <dt>

<span data-ttu-id="e200e-120">**BusSpeed**</span><span class="sxs-lookup"><span data-stu-id="e200e-120">**BusSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e200e-121">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="e200e-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="e200e-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e200e-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e200e-123">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahercios")</span><span class="sxs-lookup"><span data-stu-id="e200e-123">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")</span></span>
</dt> </dl>

<span data-ttu-id="e200e-124">Velocidad del bus, en megahercios (MHz), entre el procesador y la memoria.</span><span class="sxs-lookup"><span data-stu-id="e200e-124">Speed of the bus, in megahertz (MHz), between the processor and memory.</span></span>

</dd> <dt>

<span data-ttu-id="e200e-125">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="e200e-125">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e200e-126">Tipo de datos **: \_ procesador CIM**</span><span class="sxs-lookup"><span data-stu-id="e200e-126">Data type: **CIM\_Processor**</span></span>
</dt> <dt>

<span data-ttu-id="e200e-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e200e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e200e-128">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="e200e-128">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="e200e-129">Un [**\_ procesador CIM**](cim-processor.md) que describe el procesador que tiene acceso a la memoria o utiliza la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="e200e-129">A [**CIM\_Processor**](cim-processor.md) describing the processor that accesses the memory or uses the cache.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e200e-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e200e-130">Remarks</span></span>

<span data-ttu-id="e200e-131">La clase **CIM \_ AssociatedProcessorMemory** se deriva de [**\_ AssociatedMemory de CIM**](cim-associatedmemory.md).</span><span class="sxs-lookup"><span data-stu-id="e200e-131">The **CIM\_AssociatedProcessorMemory** class is derived from [**CIM\_AssociatedMemory**](cim-associatedmemory.md).</span></span>

<span data-ttu-id="e200e-132">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="e200e-132">WMI does not implement this class.</span></span> <span data-ttu-id="e200e-133">Para obtener más información sobre las clases derivadas de **CIM \_ AssociatedProcessorMemory**, vea [Win32 classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e200e-133">For more information about classes derived from **CIM\_AssociatedProcessorMemory**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e200e-134">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="e200e-134">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e200e-135">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="e200e-135">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e200e-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e200e-136">Requirements</span></span>



| <span data-ttu-id="e200e-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="e200e-137">Requirement</span></span> | <span data-ttu-id="e200e-138">Value</span><span class="sxs-lookup"><span data-stu-id="e200e-138">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e200e-139">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e200e-139">Minimum supported client</span></span><br/> | <span data-ttu-id="e200e-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e200e-140">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e200e-141">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e200e-141">Minimum supported server</span></span><br/> | <span data-ttu-id="e200e-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e200e-142">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e200e-143">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e200e-143">Namespace</span></span><br/>                | <span data-ttu-id="e200e-144">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e200e-144">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e200e-145">MOF</span><span class="sxs-lookup"><span data-stu-id="e200e-145">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e200e-146"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e200e-146"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e200e-147">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e200e-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e200e-148"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e200e-148"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e200e-149">Vea también</span><span class="sxs-lookup"><span data-stu-id="e200e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e200e-150">**\_ASSOCIATEDMEMORY CIM**</span><span class="sxs-lookup"><span data-stu-id="e200e-150">**CIM\_AssociatedMemory**</span></span>](cim-associatedmemory.md)
</dt> </dl>

 

