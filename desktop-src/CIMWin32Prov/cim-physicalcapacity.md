---
description: La \_ clase CIM PhysicalCapacity es una clase abstracta que representa los requisitos mínimo y máximo de un elemento físico y su capacidad para admitir distintos tipos de hardware.
ms.assetid: e422aec0-1830-464e-ac52-2911652165a2
ms.tgt_platform: multiple
title: CIM_PhysicalCapacity (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalCapacity
- CIM_PhysicalCapacity.Caption
- CIM_PhysicalCapacity.Description
- CIM_PhysicalCapacity.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50f928f69d34600c0f90865a4df44a5d7697fc89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000660"
---
# <a name="cim_physicalcapacity-class"></a><span data-ttu-id="c4ac9-103">\_Clase PhysicalCapacity de CIM</span><span class="sxs-lookup"><span data-stu-id="c4ac9-103">CIM\_PhysicalCapacity class</span></span>

<span data-ttu-id="c4ac9-104">La clase **CIM \_ PhysicalCapacity** es una clase abstracta que representa los requisitos mínimo y máximo de un elemento físico y su capacidad para admitir distintos tipos de hardware.</span><span class="sxs-lookup"><span data-stu-id="c4ac9-104">The **CIM\_PhysicalCapacity** class is an abstract class that represents a physical element's minimum and maximum requirements and its ability to support different types of hardware.</span></span> <span data-ttu-id="c4ac9-105">Por ejemplo, los requisitos de memoria mínima y máxima se pueden modelar como una subclase de **\_ PhysicalCapacity de CIM**.</span><span class="sxs-lookup"><span data-stu-id="c4ac9-105">For example, minimum and maximum memory requirements can be modeled as a subclass of **CIM\_PhysicalCapacity**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c4ac9-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="c4ac9-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c4ac9-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c4ac9-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c4ac9-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c4ac9-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c4ac9-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c4ac9-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4ac9-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c4ac9-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B69-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="c4ac9-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="c4ac9-111">Members</span></span>

<span data-ttu-id="c4ac9-112">La clase **CIM \_ PhysicalCapacity** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c4ac9-112">The **CIM\_PhysicalCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="c4ac9-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c4ac9-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c4ac9-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c4ac9-114">Properties</span></span>

<span data-ttu-id="c4ac9-115">La clase **CIM \_ PhysicalCapacity** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c4ac9-115">The **CIM\_PhysicalCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c4ac9-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c4ac9-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4ac9-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c4ac9-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4ac9-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c4ac9-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4ac9-119">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c4ac9-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c4ac9-120">Breve descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c4ac9-120">Short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="c4ac9-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c4ac9-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4ac9-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c4ac9-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4ac9-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c4ac9-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c4ac9-124">Descripción textual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c4ac9-124">Textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="c4ac9-125">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c4ac9-125">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c4ac9-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c4ac9-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c4ac9-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c4ac9-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c4ac9-128">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="c4ac9-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="c4ac9-129">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="c4ac9-129">Label by which the object is known.</span></span> <span data-ttu-id="c4ac9-130">Cuando se subclasen, esta propiedad se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="c4ac9-130">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c4ac9-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c4ac9-131">Remarks</span></span>

<span data-ttu-id="c4ac9-132">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="c4ac9-132">WMI does not implement this class.</span></span>

<span data-ttu-id="c4ac9-133">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c4ac9-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c4ac9-134">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c4ac9-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4ac9-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4ac9-135">Requirements</span></span>



| <span data-ttu-id="c4ac9-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4ac9-136">Requirement</span></span> | <span data-ttu-id="c4ac9-137">Value</span><span class="sxs-lookup"><span data-stu-id="c4ac9-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ac9-138">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4ac9-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c4ac9-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c4ac9-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c4ac9-140">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c4ac9-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c4ac9-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c4ac9-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c4ac9-142">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c4ac9-142">Namespace</span></span><br/>                | <span data-ttu-id="c4ac9-143">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c4ac9-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c4ac9-144">MOF</span><span class="sxs-lookup"><span data-stu-id="c4ac9-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c4ac9-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c4ac9-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c4ac9-146">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c4ac9-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4ac9-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4ac9-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

