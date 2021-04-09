---
description: La \_ Asociación AdjacentSlots de CIM describe el diseño de las ranuras en una placa de hospedaje o en una tarjeta de adaptador.
ms.assetid: d604647f-7b2f-4f99-8d98-adf115ae9dfb
ms.tgt_platform: multiple
title: CIM_AdjacentSlots (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AdjacentSlots
- CIM_AdjacentSlots.DistanceBetweenSlots
- CIM_AdjacentSlots.SharedSlots
- CIM_AdjacentSlots.SlotA
- CIM_AdjacentSlots.SlotB
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 695f9c668d6f75864e46026deac9a969993596ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153298"
---
# <a name="cim_adjacentslots-class"></a><span data-ttu-id="c91a7-103">\_Clase AdjacentSlots de CIM</span><span class="sxs-lookup"><span data-stu-id="c91a7-103">CIM\_AdjacentSlots class</span></span>

<span data-ttu-id="c91a7-104">La **Asociación \_ AdjacentSlots de CIM** describe el diseño de las ranuras en una placa de hospedaje o en una tarjeta de adaptador.</span><span class="sxs-lookup"><span data-stu-id="c91a7-104">The **CIM\_AdjacentSlots** association describes the layout of slots on a hosting board or adapter card.</span></span> <span data-ttu-id="c91a7-105">La información, como la distancia entre las ranuras y si están "compartidas" (si se ha rellenado una, no se puede usar la otra ranura), se transmite como propiedades de asociación.</span><span class="sxs-lookup"><span data-stu-id="c91a7-105">Information, such as the distance between the slots and whether they are "shared" (if one is populated, then the other slot cannot be used), is conveyed as association properties.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c91a7-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="c91a7-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c91a7-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c91a7-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c91a7-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c91a7-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="c91a7-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c91a7-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c91a7-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c91a7-110">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B88-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AdjacentSlots
{
  real32       DistanceBetweenSlots;
  boolean      SharedSlots;
  CIM_Slot REF SlotA;
  CIM_Slot REF SlotB;
};
```

## <a name="members"></a><span data-ttu-id="c91a7-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="c91a7-111">Members</span></span>

<span data-ttu-id="c91a7-112">La clase **CIM \_ AdjacentSlots** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c91a7-112">The **CIM\_AdjacentSlots** class has these types of members:</span></span>

-   [<span data-ttu-id="c91a7-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c91a7-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c91a7-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c91a7-114">Properties</span></span>

<span data-ttu-id="c91a7-115">La clase **CIM \_ AdjacentSlots** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c91a7-115">The **CIM\_AdjacentSlots** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c91a7-116">**DistanceBetweenSlots**</span><span class="sxs-lookup"><span data-stu-id="c91a7-116">**DistanceBetweenSlots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c91a7-117">Tipo de datos: **real32**</span><span class="sxs-lookup"><span data-stu-id="c91a7-117">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="c91a7-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c91a7-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c91a7-119">Calificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("pulgadas")</span><span class="sxs-lookup"><span data-stu-id="c91a7-119">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="c91a7-120">Distancia, en pulgadas, entre ranuras adyacentes.</span><span class="sxs-lookup"><span data-stu-id="c91a7-120">Distance, in inches, between adjacent slots.</span></span>

</dd> <dt>

<span data-ttu-id="c91a7-121">**SharedSlots**</span><span class="sxs-lookup"><span data-stu-id="c91a7-121">**SharedSlots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c91a7-122">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c91a7-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c91a7-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c91a7-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c91a7-124">Si es **true**, una tarjeta adaptador rellena una de las ranuras; la otra ranura debe dejarse vacía.</span><span class="sxs-lookup"><span data-stu-id="c91a7-124">If **TRUE**, one of the slots is populated by an adapter card; the other slot must be left empty.</span></span>

</dd> <dt>

<span data-ttu-id="c91a7-125">**Ranuraa**</span><span class="sxs-lookup"><span data-stu-id="c91a7-125">**SlotA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c91a7-126">Tipo de datos **: \_ ranura CIM**</span><span class="sxs-lookup"><span data-stu-id="c91a7-126">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="c91a7-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c91a7-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c91a7-128">Referencia a una de las ranuras adyacentes.</span><span class="sxs-lookup"><span data-stu-id="c91a7-128">Reference to one of the adjacent slots.</span></span>

</dd> <dt>

<span data-ttu-id="c91a7-129">**SlotB**</span><span class="sxs-lookup"><span data-stu-id="c91a7-129">**SlotB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c91a7-130">Tipo de datos **: \_ ranura CIM**</span><span class="sxs-lookup"><span data-stu-id="c91a7-130">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="c91a7-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c91a7-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c91a7-132">Referencia a la ranura adyacente "otros".</span><span class="sxs-lookup"><span data-stu-id="c91a7-132">Reference to the "other" adjacent slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c91a7-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c91a7-133">Remarks</span></span>

<span data-ttu-id="c91a7-134">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="c91a7-134">WMI does not implement this class.</span></span>

<span data-ttu-id="c91a7-135">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c91a7-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c91a7-136">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c91a7-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c91a7-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c91a7-137">Requirements</span></span>



| <span data-ttu-id="c91a7-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="c91a7-138">Requirement</span></span> | <span data-ttu-id="c91a7-139">Value</span><span class="sxs-lookup"><span data-stu-id="c91a7-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c91a7-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c91a7-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c91a7-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c91a7-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c91a7-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c91a7-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c91a7-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c91a7-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c91a7-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c91a7-144">Namespace</span></span><br/>                | <span data-ttu-id="c91a7-145">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c91a7-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c91a7-146">MOF</span><span class="sxs-lookup"><span data-stu-id="c91a7-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c91a7-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c91a7-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c91a7-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c91a7-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c91a7-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c91a7-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c91a7-150">Vea también</span><span class="sxs-lookup"><span data-stu-id="c91a7-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c91a7-151">Clases CIM</span><span class="sxs-lookup"><span data-stu-id="c91a7-151">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

