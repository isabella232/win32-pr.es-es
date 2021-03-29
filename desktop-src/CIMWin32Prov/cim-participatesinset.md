---
description: La \_ clase CIM ParticipatesInSet identifica los elementos físicos que se deben reemplazar juntos.
ms.assetid: 417607a3-6682-4745-a5ca-0538a0d4853d
ms.tgt_platform: multiple
title: CIM_ParticipatesInSet (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ParticipatesInSet
- CIM_ParticipatesInSet.Element
- CIM_ParticipatesInSet.Set
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e1a581452ad6ce032dcb8d3ec5c6c0caa505f7bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907362"
---
# <a name="cim_participatesinset-class"></a><span data-ttu-id="fc020-103">\_Clase ParticipatesInSet de CIM</span><span class="sxs-lookup"><span data-stu-id="fc020-103">CIM\_ParticipatesInSet class</span></span>

<span data-ttu-id="fc020-104">La clase **CIM \_ ParticipatesInSet** identifica los elementos físicos que se deben reemplazar juntos.</span><span class="sxs-lookup"><span data-stu-id="fc020-104">The **CIM\_ParticipatesInSet** class identifies physical elements that should be replaced together.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="fc020-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="fc020-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="fc020-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="fc020-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="fc020-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="fc020-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="fc020-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="fc020-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc020-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fc020-109">Syntax</span></span>

``` syntax
[Abstract, Association, Aggregation, UUID("{FAF76B6D-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ParticipatesInSet
{
  CIM_PhysicalElement REF Element;
  CIM_ReplacementSet  REF Set;
};
```

## <a name="members"></a><span data-ttu-id="fc020-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="fc020-110">Members</span></span>

<span data-ttu-id="fc020-111">La clase **CIM \_ ParticipatesInSet** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="fc020-111">The **CIM\_ParticipatesInSet** class has these types of members:</span></span>

-   [<span data-ttu-id="fc020-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc020-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fc020-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="fc020-113">Properties</span></span>

<span data-ttu-id="fc020-114">La clase **CIM \_ ParticipatesInSet** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="fc020-114">The **CIM\_ParticipatesInSet** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fc020-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="fc020-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc020-116">Tipo de datos: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="fc020-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="fc020-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc020-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="fc020-118">Referencia al elemento físico que debe reemplazarse por otros elementos, como un conjunto.</span><span class="sxs-lookup"><span data-stu-id="fc020-118">Reference to the physical element that should be replaced with other elements, as a set.</span></span>

</dd> <dt>

<span data-ttu-id="fc020-119">**Establecimiento**</span><span class="sxs-lookup"><span data-stu-id="fc020-119">**Set**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fc020-120">Tipo de datos: **CIM \_ ReplacementSet**</span><span class="sxs-lookup"><span data-stu-id="fc020-120">Data type: **CIM\_ReplacementSet**</span></span>
</dt> <dt>

<span data-ttu-id="fc020-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="fc020-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fc020-122">Calificadores: [ **agregado**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="fc020-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="fc020-123">Referencia al conjunto de elementos de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="fc020-123">Reference to the replacement set of elements.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc020-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fc020-124">Remarks</span></span>

<span data-ttu-id="fc020-125">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="fc020-125">WMI does not implement this class.</span></span>

<span data-ttu-id="fc020-126">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="fc020-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="fc020-127">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="fc020-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc020-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fc020-128">Requirements</span></span>



| <span data-ttu-id="fc020-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="fc020-129">Requirement</span></span> | <span data-ttu-id="fc020-130">Value</span><span class="sxs-lookup"><span data-stu-id="fc020-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc020-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc020-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fc020-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc020-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fc020-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fc020-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fc020-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc020-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fc020-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="fc020-135">Namespace</span></span><br/>                | <span data-ttu-id="fc020-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="fc020-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fc020-137">MOF</span><span class="sxs-lookup"><span data-stu-id="fc020-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc020-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc020-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc020-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="fc020-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc020-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc020-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

