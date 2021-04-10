---
description: La \_ Asociación PackageInSlot de CIM representa la relación entre las tarjetas de dispositivo y el chasis en el que se montan.
ms.assetid: 439f28a8-24fd-4a53-9d42-48fabb58e84a
ms.tgt_platform: multiple
title: CIM_PackageInSlot (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInSlot
- CIM_PackageInSlot.Dependent
- CIM_PackageInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a17e133f16f838d6353b6d74ee2054bd5ec52cd0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152876"
---
# <a name="cim_packageinslot-class"></a><span data-ttu-id="00272-103">\_Clase PackageInSlot de CIM</span><span class="sxs-lookup"><span data-stu-id="00272-103">CIM\_PackageInSlot class</span></span>

<span data-ttu-id="00272-104">La **Asociación \_ PackageInSlot de CIM** representa la relación entre las tarjetas de dispositivo y el chasis en el que se montan.</span><span class="sxs-lookup"><span data-stu-id="00272-104">The **CIM\_PackageInSlot** association represents the relationship between device cards and the chassis in which they are mounted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="00272-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="00272-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="00272-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="00272-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="00272-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="00272-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="00272-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="00272-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="00272-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00272-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B89-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInSlot : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_Slot            REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="00272-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="00272-110">Members</span></span>

<span data-ttu-id="00272-111">La clase **CIM \_ PackageInSlot** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="00272-111">The **CIM\_PackageInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="00272-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="00272-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="00272-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="00272-113">Properties</span></span>

<span data-ttu-id="00272-114">La clase **CIM \_ PackageInSlot** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="00272-114">The **CIM\_PackageInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="00272-115">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="00272-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00272-116">Tipo de datos **: \_ ranura CIM**</span><span class="sxs-lookup"><span data-stu-id="00272-116">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="00272-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00272-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00272-118">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="00272-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="00272-119">Una [**\_ ranura CIM**](cim-slot.md) que describe la ranura en la que se inserta el paquete físico.</span><span class="sxs-lookup"><span data-stu-id="00272-119">A [**CIM\_Slot**](cim-slot.md) describing the slot into which the physical package is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="00272-120">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="00272-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="00272-121">Tipo de datos: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="00272-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="00272-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="00272-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="00272-123">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="00272-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="00272-124">Un [**\_ PhysicalPackage de CIM**](cim-physicalpackage.md) que describe el paquete en la ranura.</span><span class="sxs-lookup"><span data-stu-id="00272-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the package in the slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="00272-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00272-125">Remarks</span></span>

<span data-ttu-id="00272-126">**CIM \_ PackageInSlot** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="00272-126">**CIM\_PackageInSlot** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="00272-127">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="00272-127">WMI does not implement this class.</span></span>

<span data-ttu-id="00272-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="00272-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="00272-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="00272-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="00272-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00272-130">Requirements</span></span>



| <span data-ttu-id="00272-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="00272-131">Requirement</span></span> | <span data-ttu-id="00272-132">Value</span><span class="sxs-lookup"><span data-stu-id="00272-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="00272-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00272-133">Minimum supported client</span></span><br/> | <span data-ttu-id="00272-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="00272-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="00272-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00272-135">Minimum supported server</span></span><br/> | <span data-ttu-id="00272-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00272-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="00272-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="00272-137">Namespace</span></span><br/>                | <span data-ttu-id="00272-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="00272-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="00272-139">MOF</span><span class="sxs-lookup"><span data-stu-id="00272-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00272-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="00272-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="00272-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="00272-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00272-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00272-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00272-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="00272-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00272-144">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="00272-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

