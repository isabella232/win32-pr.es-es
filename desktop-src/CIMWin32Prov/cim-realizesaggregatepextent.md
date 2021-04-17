---
description: La \_ Asociación RealizesAggregatePExtent de CIM representa la relación en la que \_ se realiza la clase AGGREGATEPEXTENT de CIM en un medio físico.
ms.assetid: 420dde1d-daa8-4cd3-b3fd-c2aefdc1e217
ms.tgt_platform: multiple
title: CIM_RealizesAggregatePExtent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesAggregatePExtent
- CIM_RealizesAggregatePExtent.Dependent
- CIM_RealizesAggregatePExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb80414134534d09a4030e2e87003a660e69fd9f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659519"
---
# <a name="cim_realizesaggregatepextent-class"></a><span data-ttu-id="9b14a-103">\_Clase RealizesAggregatePExtent de CIM</span><span class="sxs-lookup"><span data-stu-id="9b14a-103">CIM\_RealizesAggregatePExtent class</span></span>

<span data-ttu-id="9b14a-104">La **Asociación \_ RealizesAggregatePExtent de CIM** representa la relación en la que se realiza la clase [**\_ AggregatePExtent de CIM**](cim-aggregatepextent.md) en un medio físico.</span><span class="sxs-lookup"><span data-stu-id="9b14a-104">The **CIM\_RealizesAggregatePExtent** association represents the relationship in which the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class is realized on a physical media.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b14a-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="9b14a-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9b14a-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9b14a-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9b14a-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9b14a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9b14a-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="9b14a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b14a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9b14a-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B81-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesAggregatePExtent : CIM_Realizes
{
  CIM_AggregatePExtent REF Dependent;
  CIM_PhysicalMedia    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="9b14a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="9b14a-110">Members</span></span>

<span data-ttu-id="9b14a-111">La clase **CIM \_ RealizesAggregatePExtent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9b14a-111">The **CIM\_RealizesAggregatePExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="9b14a-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b14a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b14a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9b14a-113">Properties</span></span>

<span data-ttu-id="9b14a-114">La clase **CIM \_ RealizesAggregatePExtent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9b14a-114">The **CIM\_RealizesAggregatePExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b14a-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="9b14a-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b14a-116">Tipo de datos: **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="9b14a-116">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="9b14a-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b14a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b14a-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="9b14a-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="9b14a-119">[**\_ PhysicalMedia CIM**](cim-physicalmedia.md) que describe el medio físico en el que se realiza la extensión.</span><span class="sxs-lookup"><span data-stu-id="9b14a-119">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="9b14a-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="9b14a-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b14a-121">Tipo de datos: **CIM \_ AggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="9b14a-121">Data type: **CIM\_AggregatePExtent**</span></span>
</dt> <dt>

<span data-ttu-id="9b14a-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9b14a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b14a-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="9b14a-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="9b14a-124">[**\_ AggregatePExtent CIM**](cim-aggregatepextent.md) que se encuentra en el medio.</span><span class="sxs-lookup"><span data-stu-id="9b14a-124">The [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) that is located on the media.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b14a-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9b14a-125">Remarks</span></span>

<span data-ttu-id="9b14a-126">La clase **CIM \_ RealizesAggregatePExtent** se deriva de las contrataciones de [**CIM \_**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="9b14a-126">The **CIM\_RealizesAggregatePExtent** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="9b14a-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="9b14a-127">WMI does not implement this class.</span></span>

<span data-ttu-id="9b14a-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="9b14a-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9b14a-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="9b14a-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b14a-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b14a-130">Requirements</span></span>



| <span data-ttu-id="9b14a-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b14a-131">Requirement</span></span> | <span data-ttu-id="9b14a-132">Value</span><span class="sxs-lookup"><span data-stu-id="9b14a-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b14a-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b14a-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9b14a-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b14a-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b14a-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9b14a-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9b14a-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b14a-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b14a-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9b14a-137">Namespace</span></span><br/>                | <span data-ttu-id="9b14a-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9b14a-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9b14a-139">MOF</span><span class="sxs-lookup"><span data-stu-id="9b14a-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b14a-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b14a-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b14a-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9b14a-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b14a-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b14a-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b14a-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="9b14a-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b14a-144">**Contrataciones \_ de CIM**</span><span class="sxs-lookup"><span data-stu-id="9b14a-144">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

