---
description: La \_ clase de estadísticas CIM representa una asociación que relaciona los elementos del sistema administrados con los grupos estadísticos que se aplican a ellos.
ms.assetid: fc75991b-adcd-4e47-b610-7503f6bb7c03
ms.tgt_platform: multiple
title: CIM_Statistics (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Statistics
- CIM_Statistics.Element
- CIM_Statistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b35299a52c771ee3bcb76673ef1e2164af3b3180
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998131"
---
# <a name="cim_statistics-class"></a><span data-ttu-id="be98c-103">CIM \_ Statistics (clase)</span><span class="sxs-lookup"><span data-stu-id="be98c-103">CIM\_Statistics class</span></span>

<span data-ttu-id="be98c-104">La clase de **\_ estadísticas CIM** representa una asociación que relaciona los elementos del sistema administrados con los grupos estadísticos que se aplican a ellos.</span><span class="sxs-lookup"><span data-stu-id="be98c-104">The **CIM\_Statistics** class represents an association that relates managed system elements to the statistical groups that apply to them.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be98c-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="be98c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="be98c-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="be98c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="be98c-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="be98c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="be98c-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="be98c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="be98c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="be98c-109">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{956597A3-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_Statistics
{
  CIM_ManagedSystemElement   REF Element;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a><span data-ttu-id="be98c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="be98c-110">Members</span></span>

<span data-ttu-id="be98c-111">La clase de **\_ estadísticas CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="be98c-111">The **CIM\_Statistics** class has these types of members:</span></span>

-   [<span data-ttu-id="be98c-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="be98c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="be98c-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="be98c-113">Properties</span></span>

<span data-ttu-id="be98c-114">La clase de **\_ estadísticas CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="be98c-114">The **CIM\_Statistics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="be98c-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="be98c-115">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be98c-116">Tipo de datos **: \_ ManagedSystemElement de CIM**</span><span class="sxs-lookup"><span data-stu-id="be98c-116">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="be98c-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be98c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be98c-118">Referencia a la clase de [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) para la que se definen datos estadísticos o métricos.</span><span class="sxs-lookup"><span data-stu-id="be98c-118">Reference to the [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) class for which statistical or metric data is defined.</span></span>

</dd> <dt>

<span data-ttu-id="be98c-119">**Stats**</span><span class="sxs-lookup"><span data-stu-id="be98c-119">**Stats**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="be98c-120">Tipo de datos: **CIM \_ StatisticalInformation**</span><span class="sxs-lookup"><span data-stu-id="be98c-120">Data type: **CIM\_StatisticalInformation**</span></span>
</dt> <dt>

<span data-ttu-id="be98c-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="be98c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="be98c-122">Referencia a la información estadística u objeto.</span><span class="sxs-lookup"><span data-stu-id="be98c-122">Reference to the statistical information or object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="be98c-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="be98c-123">Remarks</span></span>

<span data-ttu-id="be98c-124">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="be98c-124">WMI does not implement this class.</span></span>

<span data-ttu-id="be98c-125">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="be98c-125">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="be98c-126">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="be98c-126">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="be98c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be98c-127">Requirements</span></span>



| <span data-ttu-id="be98c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="be98c-128">Requirement</span></span> | <span data-ttu-id="be98c-129">Value</span><span class="sxs-lookup"><span data-stu-id="be98c-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="be98c-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be98c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="be98c-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be98c-131">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="be98c-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be98c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="be98c-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be98c-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="be98c-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="be98c-134">Namespace</span></span><br/>                | <span data-ttu-id="be98c-135">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="be98c-135">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="be98c-136">MOF</span><span class="sxs-lookup"><span data-stu-id="be98c-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="be98c-137"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="be98c-137"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="be98c-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="be98c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be98c-139"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be98c-139"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




