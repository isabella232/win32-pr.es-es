---
description: La \_ clase CIM FRUPhysicalElements representa los elementos físicos que componen una unidad reemplazable en campo (FRU).
ms.assetid: ecdb19a8-5169-4370-8d2d-a21a0021ea5b
ms.tgt_platform: multiple
title: CIM_FRUPhysicalElements (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUPhysicalElements
- CIM_FRUPhysicalElements.Component
- CIM_FRUPhysicalElements.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5c47160b9053a323f693d76f5b84d922c5120992
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000618"
---
# <a name="cim_fruphysicalelements-class"></a><span data-ttu-id="a348e-103">\_Clase FRUPhysicalElements de CIM</span><span class="sxs-lookup"><span data-stu-id="a348e-103">CIM\_FRUPhysicalElements class</span></span>

<span data-ttu-id="a348e-104">La clase **CIM \_ FRUPhysicalElements** representa los elementos físicos que componen una unidad reemplazable en campo (FRU).</span><span class="sxs-lookup"><span data-stu-id="a348e-104">The **CIM\_FRUPhysicalElements** class represents the physical elements that make up a field replaceable unit (FRU).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a348e-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="a348e-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a348e-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a348e-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a348e-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a348e-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a348e-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="a348e-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a348e-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a348e-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{977E36CA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_FRU             REF FRU;
};
```

## <a name="members"></a><span data-ttu-id="a348e-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="a348e-110">Members</span></span>

<span data-ttu-id="a348e-111">La clase **CIM \_ FRUPhysicalElements** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a348e-111">The **CIM\_FRUPhysicalElements** class has these types of members:</span></span>

-   [<span data-ttu-id="a348e-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a348e-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a348e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a348e-113">Properties</span></span>

<span data-ttu-id="a348e-114">La clase **CIM \_ FRUPhysicalElements** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a348e-114">The **CIM\_FRUPhysicalElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a348e-115">**Componente**</span><span class="sxs-lookup"><span data-stu-id="a348e-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a348e-116">Tipo de datos: **CIM \_ PhysicalElement**</span><span class="sxs-lookup"><span data-stu-id="a348e-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="a348e-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a348e-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a348e-118">Referencia a un elemento físico que forma parte de la FRU.</span><span class="sxs-lookup"><span data-stu-id="a348e-118">Reference to a physical element that is a part of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="a348e-119">**FRU**</span><span class="sxs-lookup"><span data-stu-id="a348e-119">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a348e-120">Tipo de datos **: \_ FRU de CIM**</span><span class="sxs-lookup"><span data-stu-id="a348e-120">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="a348e-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a348e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a348e-122">Calificadores: [**agregado**](/windows/desktop/WmiSdk/standard-qualifiers), [**máximo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="a348e-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="a348e-123">Referencia a la FRU.</span><span class="sxs-lookup"><span data-stu-id="a348e-123">Reference to the FRU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a348e-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a348e-124">Remarks</span></span>

<span data-ttu-id="a348e-125">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="a348e-125">WMI does not implement this class.</span></span>

<span data-ttu-id="a348e-126">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="a348e-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a348e-127">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="a348e-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a348e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a348e-128">Requirements</span></span>



| <span data-ttu-id="a348e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="a348e-129">Requirement</span></span> | <span data-ttu-id="a348e-130">Value</span><span class="sxs-lookup"><span data-stu-id="a348e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a348e-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a348e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="a348e-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a348e-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a348e-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a348e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="a348e-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a348e-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a348e-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a348e-135">Namespace</span></span><br/>                | <span data-ttu-id="a348e-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a348e-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a348e-137">MOF</span><span class="sxs-lookup"><span data-stu-id="a348e-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a348e-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a348e-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a348e-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a348e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a348e-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a348e-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

