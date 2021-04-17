---
description: La \_ Asociación ElementsLinked de CIM representa los elementos físicos que están cableados juntos por un vínculo físico.
ms.assetid: b9e1d11e-6f89-4d7a-9b5c-01161e7c1bdf
ms.tgt_platform: multiple
title: CIM_ElementsLinked (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementsLinked
- CIM_ElementsLinked.Dependent
- CIM_ElementsLinked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353809056d1ca3bae710272b02c2636a3f02eef1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659604"
---
# <a name="cim_elementslinked-class"></a><span data-ttu-id="616de-103">\_Clase ElementsLinked de CIM</span><span class="sxs-lookup"><span data-stu-id="616de-103">CIM\_ElementsLinked class</span></span>

<span data-ttu-id="616de-104">La **Asociación \_ ElementsLinked de CIM** representa los elementos físicos que están cableados juntos por un vínculo físico.</span><span class="sxs-lookup"><span data-stu-id="616de-104">The **CIM\_ElementsLinked** association represents physical elements that are cabled together by a physical link.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="616de-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="616de-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="616de-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="616de-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="616de-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="616de-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="616de-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="616de-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="616de-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="616de-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B83-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementsLinked : CIM_Dependency
{
  CIM_PhysicalElement REF Dependent;
  CIM_PhysicalLink    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="616de-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="616de-110">Members</span></span>

<span data-ttu-id="616de-111">La clase **CIM \_ ElementsLinked** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="616de-111">The **CIM\_ElementsLinked** class has these types of members:</span></span>

-   [<span data-ttu-id="616de-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="616de-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="616de-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="616de-113">Properties</span></span>

<span data-ttu-id="616de-114">La clase **CIM \_ ElementsLinked** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="616de-114">The **CIM\_ElementsLinked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="616de-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="616de-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="616de-116">Tipo de datos: **CIM \_ PhysicalLink**</span><span class="sxs-lookup"><span data-stu-id="616de-116">Data type: **CIM\_PhysicalLink**</span></span>
</dt> <dt>

<span data-ttu-id="616de-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="616de-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="616de-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="616de-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="616de-119">[**\_ PhysicalLink CIM**](cim-physicallink.md) que describe el vínculo físico.</span><span class="sxs-lookup"><span data-stu-id="616de-119">A [**CIM\_PhysicalLink**](cim-physicallink.md) that describes the physical link.</span></span>

</dd> <dt>

<span data-ttu-id="616de-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="616de-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="616de-121">Tipo de datos: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="616de-121">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="616de-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="616de-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="616de-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="616de-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="616de-124">[**\_ PhysicalElement CIM**](cim-physicalelement.md) que describe el elemento físico que está vinculado.</span><span class="sxs-lookup"><span data-stu-id="616de-124">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical element that is linked.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="616de-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="616de-125">Remarks</span></span>

<span data-ttu-id="616de-126">La clase **CIM \_ ElementsLinked** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="616de-126">The **CIM\_ElementsLinked** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="616de-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="616de-127">WMI does not implement this class.</span></span>

<span data-ttu-id="616de-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="616de-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="616de-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="616de-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="616de-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="616de-130">Requirements</span></span>



| <span data-ttu-id="616de-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="616de-131">Requirement</span></span> | <span data-ttu-id="616de-132">Value</span><span class="sxs-lookup"><span data-stu-id="616de-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="616de-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="616de-133">Minimum supported client</span></span><br/> | <span data-ttu-id="616de-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="616de-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="616de-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="616de-135">Minimum supported server</span></span><br/> | <span data-ttu-id="616de-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="616de-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="616de-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="616de-137">Namespace</span></span><br/>                | <span data-ttu-id="616de-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="616de-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="616de-139">MOF</span><span class="sxs-lookup"><span data-stu-id="616de-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="616de-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="616de-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="616de-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="616de-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="616de-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="616de-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="616de-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="616de-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="616de-144">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="616de-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

