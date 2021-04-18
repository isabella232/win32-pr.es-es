---
description: La \_ clase AssociateMemory de CIM asocia la memoria instalada o asociada, como la memoria caché con un dispositivo lógico.
ms.assetid: b108d0cc-9353-4940-a5f6-34bb93330a62
ms.tgt_platform: multiple
title: CIM_AssociatedMemory (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedMemory
- CIM_AssociatedMemory.Dependent
- CIM_AssociatedMemory.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cb1443f54ab273ef6c114b8645e5322c24785f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496481"
---
# <a name="cim_associatedmemory-class"></a><span data-ttu-id="bfcfc-103">\_Clase AssociatedMemory de CIM</span><span class="sxs-lookup"><span data-stu-id="bfcfc-103">CIM\_AssociatedMemory class</span></span>

<span data-ttu-id="bfcfc-104">La **clase \_ AssociateMemory de CIM** asocia la memoria instalada o asociada, como la memoria caché con un dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-104">The **CIM\_AssociateMemory** class associates installed or associated memory, such as cache memory with a logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bfcfc-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bfcfc-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bfcfc-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bfcfc-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="bfcfc-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bfcfc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bfcfc-109">Syntax</span></span>

``` syntax
[abstract, UUID("{464FFAB0-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedMemory : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Memory        REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="bfcfc-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="bfcfc-110">Members</span></span>

<span data-ttu-id="bfcfc-111">La clase **CIM \_ AssociatedMemory** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bfcfc-111">The **CIM\_AssociatedMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="bfcfc-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bfcfc-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bfcfc-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bfcfc-113">Properties</span></span>

<span data-ttu-id="bfcfc-114">La clase **CIM \_ AssociatedMemory** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-114">The **CIM\_AssociatedMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bfcfc-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="bfcfc-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfcfc-116">Tipo de datos **: \_ memoria CIM**</span><span class="sxs-lookup"><span data-stu-id="bfcfc-116">Data type: **CIM\_Memory**</span></span>
</dt> <dt>

<span data-ttu-id="bfcfc-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfcfc-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfcfc-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="bfcfc-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="bfcfc-119">[**\_ Memoria de CIM**](cim-memory.md) que describe la memoria instalada en o asociada a un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-119">A [**CIM\_Memory**](cim-memory.md) that describes the memory installed on or associated with a device.</span></span>

</dd> <dt>

<span data-ttu-id="bfcfc-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="bfcfc-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bfcfc-121">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="bfcfc-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="bfcfc-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bfcfc-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bfcfc-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="bfcfc-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="bfcfc-124">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que describe el dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bfcfc-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfcfc-125">Remarks</span></span>

<span data-ttu-id="bfcfc-126">La clase **CIM \_ AssociatedMemory** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="bfcfc-126">The **CIM\_AssociatedMemory** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="bfcfc-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-127">WMI does not implement this class.</span></span>

<span data-ttu-id="bfcfc-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bfcfc-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="bfcfc-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bfcfc-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bfcfc-130">Requirements</span></span>



| <span data-ttu-id="bfcfc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bfcfc-131">Requirement</span></span> | <span data-ttu-id="bfcfc-132">Value</span><span class="sxs-lookup"><span data-stu-id="bfcfc-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfcfc-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfcfc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bfcfc-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bfcfc-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bfcfc-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bfcfc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bfcfc-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bfcfc-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bfcfc-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bfcfc-137">Namespace</span></span><br/>                | <span data-ttu-id="bfcfc-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bfcfc-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bfcfc-139">MOF</span><span class="sxs-lookup"><span data-stu-id="bfcfc-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bfcfc-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bfcfc-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bfcfc-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bfcfc-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bfcfc-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bfcfc-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bfcfc-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="bfcfc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfcfc-144">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="bfcfc-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

