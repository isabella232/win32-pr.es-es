---
description: La \_ clase PhysicalElementLocation de CIM asocia un elemento físico a un \_ objeto de ubicación CIM para fines de inventario o de reemplazo.
ms.assetid: d1698c1a-0eda-4e32-9a29-fb741b987671
ms.tgt_platform: multiple
title: CIM_PhysicalElementLocation (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalElementLocation
- CIM_PhysicalElementLocation.Element
- CIM_PhysicalElementLocation.PhysicalLocation
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5e47460a3563d9b7a86aa6ee65704fcb0a422c39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153379"
---
# <a name="cim_physicalelementlocation-class"></a><span data-ttu-id="8bd20-103">\_Clase PhysicalElementLocation de CIM</span><span class="sxs-lookup"><span data-stu-id="8bd20-103">CIM\_PhysicalElementLocation class</span></span>

<span data-ttu-id="8bd20-104">La **clase \_ PhysicalElementLocation de CIM** asocia un elemento físico a un objeto de [**\_ Ubicación CIM**](cim-location.md) para fines de inventario o de reemplazo.</span><span class="sxs-lookup"><span data-stu-id="8bd20-104">The **CIM\_PhysicalElementLocation** class associates a physical element with a [**CIM\_Location**](cim-location.md) object for inventory or replacement purposes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8bd20-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="8bd20-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="8bd20-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="8bd20-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="8bd20-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="8bd20-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="8bd20-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="8bd20-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="8bd20-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8bd20-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B68-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalElementLocation
{
  CIM_PhysicalElement REF Element;
  CIM_Location        REF PhysicalLocation;
};
```

## <a name="members"></a><span data-ttu-id="8bd20-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="8bd20-110">Members</span></span>

<span data-ttu-id="8bd20-111">La clase **CIM \_ PhysicalElementLocation** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="8bd20-111">The **CIM\_PhysicalElementLocation** class has these types of members:</span></span>

-   [<span data-ttu-id="8bd20-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8bd20-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8bd20-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="8bd20-113">Properties</span></span>

<span data-ttu-id="8bd20-114">La clase **CIM \_ PhysicalElementLocation** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="8bd20-114">The **CIM\_PhysicalElementLocation** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="8bd20-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="8bd20-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bd20-116">Tipo de datos: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="8bd20-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="8bd20-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8bd20-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="8bd20-118">Referencia al elemento físico cuya ubicación se especifica.</span><span class="sxs-lookup"><span data-stu-id="8bd20-118">Reference to the physical element whose location is specified.</span></span>

</dd> <dt>

<span data-ttu-id="8bd20-119">**PhysicalLocation**</span><span class="sxs-lookup"><span data-stu-id="8bd20-119">**PhysicalLocation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="8bd20-120">Tipo de datos **: \_ Ubicación CIM**</span><span class="sxs-lookup"><span data-stu-id="8bd20-120">Data type: **CIM\_Location**</span></span>
</dt> <dt>

<span data-ttu-id="8bd20-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="8bd20-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="8bd20-122">Calificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="8bd20-122">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="8bd20-123">Referencia a la ubicación del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="8bd20-123">Reference to the physical element's location.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8bd20-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8bd20-124">Remarks</span></span>

<span data-ttu-id="8bd20-125">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="8bd20-125">WMI does not implement this class.</span></span>

<span data-ttu-id="8bd20-126">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="8bd20-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="8bd20-127">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="8bd20-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="8bd20-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8bd20-128">Requirements</span></span>



| <span data-ttu-id="8bd20-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8bd20-129">Requirement</span></span> | <span data-ttu-id="8bd20-130">Value</span><span class="sxs-lookup"><span data-stu-id="8bd20-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8bd20-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bd20-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8bd20-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8bd20-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8bd20-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8bd20-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8bd20-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8bd20-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8bd20-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8bd20-135">Namespace</span></span><br/>                | <span data-ttu-id="8bd20-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8bd20-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8bd20-137">MOF</span><span class="sxs-lookup"><span data-stu-id="8bd20-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8bd20-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8bd20-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8bd20-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8bd20-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8bd20-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8bd20-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

