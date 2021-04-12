---
description: La \_ clase de ubicación CIM representa la posición y la dirección de un elemento físico.
ms.assetid: c1ec467c-a338-4beb-a8fe-1ebc5b05c754
ms.tgt_platform: multiple
title: CIM_Location (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Location
- CIM_Location.Address
- CIM_Location.Name
- CIM_Location.PhysicalPosition
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd5a1c1c23d07020b45c1c5979a941f01baff0d0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274989"
---
# <a name="cim_location-class"></a><span data-ttu-id="56d00-103">\_Clase de ubicación CIM</span><span class="sxs-lookup"><span data-stu-id="56d00-103">CIM\_Location class</span></span>

<span data-ttu-id="56d00-104">La clase de **\_ Ubicación CIM** representa la posición y la dirección de un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="56d00-104">The **CIM\_Location** class represents the position and address of a physical element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="56d00-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="56d00-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="56d00-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="56d00-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="56d00-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="56d00-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="56d00-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="56d00-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="56d00-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56d00-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B67-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Location
{
  string Address;
  string Name;
  string PhysicalPosition;
};
```

## <a name="members"></a><span data-ttu-id="56d00-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="56d00-110">Members</span></span>

<span data-ttu-id="56d00-111">La clase de **\_ Ubicación CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="56d00-111">The **CIM\_Location** class has these types of members:</span></span>

-   [<span data-ttu-id="56d00-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="56d00-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="56d00-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="56d00-113">Properties</span></span>

<span data-ttu-id="56d00-114">La clase de **\_ Ubicación CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="56d00-114">The **CIM\_Location** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="56d00-115">**Dirección**</span><span class="sxs-lookup"><span data-stu-id="56d00-115">**Address**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56d00-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="56d00-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56d00-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56d00-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56d00-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span><span class="sxs-lookup"><span data-stu-id="56d00-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (1024)</span></span>
</dt> </dl>

<span data-ttu-id="56d00-119">Cadena de forma libre que indica una calle u otro tipo de dirección para la ubicación del elemento físico.</span><span class="sxs-lookup"><span data-stu-id="56d00-119">Free-form string that indicates a street or other type of address for the physical element's location.</span></span>

</dd> <dt>

<span data-ttu-id="56d00-120">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="56d00-120">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56d00-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="56d00-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56d00-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56d00-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56d00-123">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="56d00-123">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="56d00-124">Cadena de forma libre que define una etiqueta para la ubicación y forma parte de la clave del objeto.</span><span class="sxs-lookup"><span data-stu-id="56d00-124">Free-form string that defines a label for the location and is part of the key for the object.</span></span>

</dd> <dt>

<span data-ttu-id="56d00-125">**PhysicalPosition**</span><span class="sxs-lookup"><span data-stu-id="56d00-125">**PhysicalPosition**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="56d00-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="56d00-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="56d00-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="56d00-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="56d00-128">Calificadores: [**clave**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="56d00-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="56d00-129">Cadena de forma libre que indica la posición de un elemento físico.</span><span class="sxs-lookup"><span data-stu-id="56d00-129">Free-form string that indicates the placement of a physical element.</span></span> <span data-ttu-id="56d00-130">Puede especificar la información de la ranura en un panel de hospedaje, un sitio de montaje en un archivo. cab o información de latitud y longitud.</span><span class="sxs-lookup"><span data-stu-id="56d00-130">It can specify slot information on a hosting board, mounting site in a cabinet, or latitude and longitude information.</span></span> <span data-ttu-id="56d00-131">Forma parte de la clave del objeto de **\_ Ubicación CIM** .</span><span class="sxs-lookup"><span data-stu-id="56d00-131">It is part of the key of the **CIM\_Location** object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="56d00-132">Observaciones</span><span class="sxs-lookup"><span data-stu-id="56d00-132">Remarks</span></span>

<span data-ttu-id="56d00-133">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="56d00-133">WMI does not implement this class.</span></span> <span data-ttu-id="56d00-134">Para las clases derivadas de la **\_ Ubicación CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="56d00-134">For classes derived from **CIM\_Location**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="56d00-135">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="56d00-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="56d00-136">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="56d00-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="56d00-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56d00-137">Requirements</span></span>



| <span data-ttu-id="56d00-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="56d00-138">Requirement</span></span> | <span data-ttu-id="56d00-139">Value</span><span class="sxs-lookup"><span data-stu-id="56d00-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56d00-140">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56d00-140">Minimum supported client</span></span><br/> | <span data-ttu-id="56d00-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="56d00-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="56d00-142">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="56d00-142">Minimum supported server</span></span><br/> | <span data-ttu-id="56d00-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="56d00-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="56d00-144">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="56d00-144">Namespace</span></span><br/>                | <span data-ttu-id="56d00-145">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="56d00-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="56d00-146">MOF</span><span class="sxs-lookup"><span data-stu-id="56d00-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="56d00-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="56d00-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="56d00-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="56d00-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56d00-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56d00-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

