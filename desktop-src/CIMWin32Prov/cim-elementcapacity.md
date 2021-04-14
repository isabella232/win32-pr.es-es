---
description: La \_ clase ElementCapacity de CIM asocia un \_ objeto PHYSICALCAPACITY de CIM con uno o más elementos físicos. Asocia una descripción de los requisitos de hardware mínimos y máximos (o las capacidades) a los elementos físicos que se describen.
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: CIM_ElementCapacity (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapacity
- CIM_ElementCapacity.Capacity
- CIM_ElementCapacity.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c6ecac913f6d4affcd9784a30d85fa08dfe0486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496283"
---
# <a name="cim_elementcapacity-class"></a><span data-ttu-id="89ba5-104">\_Clase ElementCapacity de CIM</span><span class="sxs-lookup"><span data-stu-id="89ba5-104">CIM\_ElementCapacity class</span></span>

<span data-ttu-id="89ba5-105">La **clase \_ ElementCapacity de CIM** asocia un objeto [**\_ PhysicalCapacity de CIM**](cim-physicalcapacity.md) con uno o más elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="89ba5-105">The **CIM\_ElementCapacity** class associates a [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) object with one or more physical elements.</span></span> <span data-ttu-id="89ba5-106">Asocia una descripción de los requisitos de hardware mínimos y máximos (o las capacidades) a los elementos físicos que se describen.</span><span class="sxs-lookup"><span data-stu-id="89ba5-106">It associates a description of the minimum and maximum hardware requirements (or capabilities) to the physical elements being described.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89ba5-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="89ba5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="89ba5-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="89ba5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="89ba5-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="89ba5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="89ba5-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="89ba5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="89ba5-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="89ba5-111">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B6A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementCapacity
{
  CIM_PhysicalCapacity REF Capacity;
  CIM_PhysicalElement  REF Element;
};
```

## <a name="members"></a><span data-ttu-id="89ba5-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="89ba5-112">Members</span></span>

<span data-ttu-id="89ba5-113">La clase **CIM \_ ElementCapacity** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="89ba5-113">The **CIM\_ElementCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="89ba5-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="89ba5-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="89ba5-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="89ba5-115">Properties</span></span>

<span data-ttu-id="89ba5-116">La clase **CIM \_ ElementCapacity** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="89ba5-116">The **CIM\_ElementCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="89ba5-117">**Capacity**</span><span class="sxs-lookup"><span data-stu-id="89ba5-117">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89ba5-118">Tipo de datos: **CIM \_ PhysicalCapacity**</span><span class="sxs-lookup"><span data-stu-id="89ba5-118">Data type: **CIM\_PhysicalCapacity**</span></span>
</dt> <dt>

<span data-ttu-id="89ba5-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89ba5-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="89ba5-120">Referencia a la [**clase \_ PhysicalCapacity de CIM**](cim-physicalcapacity.md) que describe los requisitos mínimo y máximo, así como la capacidad de admitir distintos tipos de hardware para un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="89ba5-120">Reference to the [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) class that describes the minimum and maximum requirements and the ability to support different types of hardware for a physical element.</span></span>

</dd> <dt>

<span data-ttu-id="89ba5-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="89ba5-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="89ba5-122">Tipo de datos: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="89ba5-122">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="89ba5-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="89ba5-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="89ba5-124">Calificadores: [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="89ba5-124">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="89ba5-125">Referencia al elemento físico que se describe.</span><span class="sxs-lookup"><span data-stu-id="89ba5-125">Reference to the physical element being described.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="89ba5-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="89ba5-126">Remarks</span></span>

<span data-ttu-id="89ba5-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="89ba5-127">WMI does not implement this class.</span></span>

<span data-ttu-id="89ba5-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="89ba5-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="89ba5-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="89ba5-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="89ba5-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89ba5-130">Requirements</span></span>



| <span data-ttu-id="89ba5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="89ba5-131">Requirement</span></span> | <span data-ttu-id="89ba5-132">Value</span><span class="sxs-lookup"><span data-stu-id="89ba5-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="89ba5-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89ba5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="89ba5-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89ba5-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="89ba5-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="89ba5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="89ba5-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89ba5-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="89ba5-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="89ba5-137">Namespace</span></span><br/>                | <span data-ttu-id="89ba5-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="89ba5-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="89ba5-139">MOF</span><span class="sxs-lookup"><span data-stu-id="89ba5-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89ba5-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="89ba5-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="89ba5-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="89ba5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89ba5-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89ba5-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

