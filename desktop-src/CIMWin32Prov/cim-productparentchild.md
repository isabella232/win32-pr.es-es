---
description: La \_ Asociación ProductParentChild de CIM define una jerarquía de elementos primarios y secundarios entre productos. Por ejemplo, un producto puede estar incluido en otros productos.
ms.assetid: 244576fd-8dae-4554-b80b-0cac58c93037
ms.tgt_platform: multiple
title: CIM_ProductParentChild (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductParentChild
- CIM_ProductParentChild.Child
- CIM_ProductParentChild.Parent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3a5fd34cc3dffc6d5c8df7f7a76d9cada7856d57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538560"
---
# <a name="cim_productparentchild-class"></a><span data-ttu-id="5c7fc-104">\_Clase ProductParentChild de CIM</span><span class="sxs-lookup"><span data-stu-id="5c7fc-104">CIM\_ProductParentChild class</span></span>

<span data-ttu-id="5c7fc-105">La **Asociación \_ ProductParentChild de CIM** define una jerarquía de elementos primarios y secundarios entre productos.</span><span class="sxs-lookup"><span data-stu-id="5c7fc-105">The **CIM\_ProductParentChild** association defines a parent-child hierarchy among products.</span></span> <span data-ttu-id="5c7fc-106">Por ejemplo, un producto puede estar incluido en otros productos.</span><span class="sxs-lookup"><span data-stu-id="5c7fc-106">For example, a product can come bundled with other products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5c7fc-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="5c7fc-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="5c7fc-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="5c7fc-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="5c7fc-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5c7fc-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="5c7fc-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="5c7fc-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c7fc-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5c7fc-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{3E24D5A6-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductParentChild
{
  CIM_Product REF Child;
  CIM_Product REF Parent;
};
```

## <a name="members"></a><span data-ttu-id="5c7fc-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="5c7fc-112">Members</span></span>

<span data-ttu-id="5c7fc-113">La clase **CIM \_ ProductParentChild** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5c7fc-113">The **CIM\_ProductParentChild** class has these types of members:</span></span>

-   [<span data-ttu-id="5c7fc-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c7fc-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5c7fc-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5c7fc-115">Properties</span></span>

<span data-ttu-id="5c7fc-116">La clase **CIM \_ ProductParentChild** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5c7fc-116">The **CIM\_ProductParentChild** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="5c7fc-117">**Elemento secundario**</span><span class="sxs-lookup"><span data-stu-id="5c7fc-117">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c7fc-118">Tipo de datos: **CIM \_ Product**</span><span class="sxs-lookup"><span data-stu-id="5c7fc-118">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="5c7fc-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c7fc-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="5c7fc-120">Referencia al producto secundario en la asociación.</span><span class="sxs-lookup"><span data-stu-id="5c7fc-120">Reference to the child product in the association.</span></span>

</dd> <dt>

<span data-ttu-id="5c7fc-121">**Parent**</span><span class="sxs-lookup"><span data-stu-id="5c7fc-121">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5c7fc-122">Tipo de datos: **CIM \_ Product**</span><span class="sxs-lookup"><span data-stu-id="5c7fc-122">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="5c7fc-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5c7fc-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5c7fc-124">Calificadores: [ **agregado**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="5c7fc-124">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="5c7fc-125">Referencia al producto primario de la asociación.</span><span class="sxs-lookup"><span data-stu-id="5c7fc-125">Reference to the parent product in the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c7fc-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5c7fc-126">Remarks</span></span>

<span data-ttu-id="5c7fc-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="5c7fc-127">WMI does not implement this class.</span></span>

<span data-ttu-id="5c7fc-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="5c7fc-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="5c7fc-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="5c7fc-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c7fc-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c7fc-130">Requirements</span></span>



| <span data-ttu-id="5c7fc-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c7fc-131">Requirement</span></span> | <span data-ttu-id="5c7fc-132">Value</span><span class="sxs-lookup"><span data-stu-id="5c7fc-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c7fc-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c7fc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="5c7fc-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c7fc-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c7fc-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5c7fc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="5c7fc-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c7fc-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c7fc-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5c7fc-137">Namespace</span></span><br/>                | <span data-ttu-id="5c7fc-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5c7fc-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5c7fc-139">MOF</span><span class="sxs-lookup"><span data-stu-id="5c7fc-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c7fc-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c7fc-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c7fc-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5c7fc-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c7fc-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c7fc-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

