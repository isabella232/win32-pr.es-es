---
description: La \_ agregación StorageDefect de CIM recopila los errores de almacenamiento para una extensión de almacenamiento.
ms.assetid: 7acd3d25-4691-43cb-badc-662684989345
ms.tgt_platform: multiple
title: CIM_StorageDefect (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_StorageDefect
- CIM_StorageDefect.Error
- CIM_StorageDefect.Extent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e6c2be45fe2f44afa407dc72e3ae90c486593ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000774"
---
# <a name="cim_storagedefect-class"></a><span data-ttu-id="01c34-103">\_Clase StorageDefect de CIM</span><span class="sxs-lookup"><span data-stu-id="01c34-103">CIM\_StorageDefect class</span></span>

<span data-ttu-id="01c34-104">La agregación **\_ StorageDefect de CIM** recopila los errores de almacenamiento para una extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="01c34-104">The **CIM\_StorageDefect** aggregation collects the storage errors for a storage extent.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="01c34-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="01c34-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="01c34-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="01c34-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="01c34-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="01c34-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="01c34-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="01c34-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="01c34-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="01c34-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{5CC70817-DB31-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_StorageDefect
{
  CIM_StorageError  REF Error;
  CIM_StorageExtent REF Extent;
};
```

## <a name="members"></a><span data-ttu-id="01c34-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="01c34-110">Members</span></span>

<span data-ttu-id="01c34-111">La clase **CIM \_ StorageDefect** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="01c34-111">The **CIM\_StorageDefect** class has these types of members:</span></span>

-   [<span data-ttu-id="01c34-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01c34-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="01c34-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="01c34-113">Properties</span></span>

<span data-ttu-id="01c34-114">La clase **CIM \_ StorageDefect** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="01c34-114">The **CIM\_StorageDefect** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="01c34-115">**Error**</span><span class="sxs-lookup"><span data-stu-id="01c34-115">**Error**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01c34-116">Tipo de datos: **CIM \_ StorageError**</span><span class="sxs-lookup"><span data-stu-id="01c34-116">Data type: **CIM\_StorageError**</span></span>
</dt> <dt>

<span data-ttu-id="01c34-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01c34-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01c34-118">Calificadores: [ **débil**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="01c34-118">Qualifiers: [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="01c34-119">Referencia al objeto de error, que define las direcciones inicial y final que se asignan fuera de la extensión de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="01c34-119">Reference to the error object, which defines the starting and ending addresses that are mapped out of the storage extent.</span></span>

</dd> <dt>

<span data-ttu-id="01c34-120">**Extensión**</span><span class="sxs-lookup"><span data-stu-id="01c34-120">**Extent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="01c34-121">Tipo de datos: **CIM \_ StorageExtent**</span><span class="sxs-lookup"><span data-stu-id="01c34-121">Data type: **CIM\_StorageExtent**</span></span>
</dt> <dt>

<span data-ttu-id="01c34-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="01c34-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="01c34-123">Calificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="01c34-123">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="01c34-124">Referencia a la extensión de almacenamiento en la que se produjeron los errores.</span><span class="sxs-lookup"><span data-stu-id="01c34-124">Reference to the storage extent on which the errors occurred.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="01c34-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="01c34-125">Remarks</span></span>

<span data-ttu-id="01c34-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="01c34-126">WMI does not implement this class.</span></span>

<span data-ttu-id="01c34-127">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="01c34-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="01c34-128">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="01c34-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="01c34-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01c34-129">Requirements</span></span>



| <span data-ttu-id="01c34-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="01c34-130">Requirement</span></span> | <span data-ttu-id="01c34-131">Value</span><span class="sxs-lookup"><span data-stu-id="01c34-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="01c34-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01c34-132">Minimum supported client</span></span><br/> | <span data-ttu-id="01c34-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="01c34-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="01c34-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="01c34-134">Minimum supported server</span></span><br/> | <span data-ttu-id="01c34-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="01c34-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="01c34-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="01c34-136">Namespace</span></span><br/>                | <span data-ttu-id="01c34-137">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="01c34-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="01c34-138">MOF</span><span class="sxs-lookup"><span data-stu-id="01c34-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="01c34-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="01c34-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="01c34-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="01c34-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="01c34-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="01c34-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

