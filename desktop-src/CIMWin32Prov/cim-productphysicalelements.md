---
description: La \_ clase CIM ProductPhysicalElements representa los elementos físicos que componen un producto.
ms.assetid: cf23098a-f61e-4778-883e-1a5138af3da0
ms.tgt_platform: multiple
title: CIM_ProductPhysicalElements (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductPhysicalElements
- CIM_ProductPhysicalElements.Component
- CIM_ProductPhysicalElements.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a581293426c421de0dd76636a9f446f245f6ab32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152930"
---
# <a name="cim_productphysicalelements-class"></a><span data-ttu-id="dcfad-103">\_Clase ProductPhysicalElements de CIM</span><span class="sxs-lookup"><span data-stu-id="dcfad-103">CIM\_ProductPhysicalElements class</span></span>

<span data-ttu-id="dcfad-104">La clase **CIM \_ ProductPhysicalElements** representa los elementos físicos que componen un producto.</span><span class="sxs-lookup"><span data-stu-id="dcfad-104">The **CIM\_ProductPhysicalElements** class represents the physical elements that make up a product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dcfad-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="dcfad-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dcfad-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dcfad-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dcfad-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="dcfad-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="dcfad-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="dcfad-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcfad-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dcfad-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{502F00A0-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a><span data-ttu-id="dcfad-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="dcfad-110">Members</span></span>

<span data-ttu-id="dcfad-111">La clase **CIM \_ ProductPhysicalElements** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="dcfad-111">The **CIM\_ProductPhysicalElements** class has these types of members:</span></span>

-   [<span data-ttu-id="dcfad-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dcfad-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="dcfad-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="dcfad-113">Properties</span></span>

<span data-ttu-id="dcfad-114">La clase **CIM \_ ProductPhysicalElements** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="dcfad-114">The **CIM\_ProductPhysicalElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="dcfad-115">**Componente**</span><span class="sxs-lookup"><span data-stu-id="dcfad-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfad-116">Tipo de datos: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="dcfad-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="dcfad-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dcfad-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="dcfad-118">Referencia al elemento físico que forma parte del producto.</span><span class="sxs-lookup"><span data-stu-id="dcfad-118">Reference to the physical element that is part of the product.</span></span>

</dd> <dt>

<span data-ttu-id="dcfad-119">**Producto**</span><span class="sxs-lookup"><span data-stu-id="dcfad-119">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="dcfad-120">Tipo de datos: **CIM \_ Product**</span><span class="sxs-lookup"><span data-stu-id="dcfad-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="dcfad-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="dcfad-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="dcfad-122">Calificadores: [**agregado**](/windows/desktop/WmiSdk/standard-qualifiers), [**máximo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="dcfad-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="dcfad-123">Referencia al producto.</span><span class="sxs-lookup"><span data-stu-id="dcfad-123">Reference to the product.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dcfad-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dcfad-124">Remarks</span></span>

<span data-ttu-id="dcfad-125">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="dcfad-125">WMI does not implement this class.</span></span>

<span data-ttu-id="dcfad-126">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="dcfad-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dcfad-127">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="dcfad-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcfad-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dcfad-128">Requirements</span></span>



| <span data-ttu-id="dcfad-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcfad-129">Requirement</span></span> | <span data-ttu-id="dcfad-130">Value</span><span class="sxs-lookup"><span data-stu-id="dcfad-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcfad-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcfad-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dcfad-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dcfad-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dcfad-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dcfad-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dcfad-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dcfad-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dcfad-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dcfad-135">Namespace</span></span><br/>                | <span data-ttu-id="dcfad-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dcfad-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dcfad-137">MOF</span><span class="sxs-lookup"><span data-stu-id="dcfad-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dcfad-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dcfad-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dcfad-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dcfad-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dcfad-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcfad-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

