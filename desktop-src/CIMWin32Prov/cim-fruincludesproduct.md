---
description: La \_ clase CIM FRUIncludesProduct indica que una unidad reemplazable en campo (FRU) puede estar formada por otros productos.
ms.assetid: e57dc7f5-4c5b-4ec4-9300-e080053955cb
ms.tgt_platform: multiple
title: CIM_FRUIncludesProduct (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUIncludesProduct
- CIM_FRUIncludesProduct.Component
- CIM_FRUIncludesProduct.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 196f0cc1f2e81312e5e695c34e0a492ac7c05389
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104279805"
---
# <a name="cim_fruincludesproduct-class"></a><span data-ttu-id="3e598-103">\_Clase FRUIncludesProduct de CIM</span><span class="sxs-lookup"><span data-stu-id="3e598-103">CIM\_FRUIncludesProduct class</span></span>

<span data-ttu-id="3e598-104">La clase **CIM \_ FRUIncludesProduct** indica que una unidad reemplazable en campo (FRU) puede estar formada por otros productos.</span><span class="sxs-lookup"><span data-stu-id="3e598-104">The **CIM\_FRUIncludesProduct** class indicates that a field replaceable unit (FRU) may be composed of other products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3e598-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="3e598-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3e598-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3e598-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3e598-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3e598-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3e598-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3e598-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e598-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3e598-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{87FEEDCA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUIncludesProduct
{
  CIM_Product REF Component;
  CIM_FRU     REF FRU;
};
```

## <a name="members"></a><span data-ttu-id="3e598-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="3e598-110">Members</span></span>

<span data-ttu-id="3e598-111">La clase **CIM \_ FRUIncludesProduct** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3e598-111">The **CIM\_FRUIncludesProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="3e598-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3e598-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3e598-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3e598-113">Properties</span></span>

<span data-ttu-id="3e598-114">La clase **CIM \_ FRUIncludesProduct** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3e598-114">The **CIM\_FRUIncludesProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3e598-115">**Componente**</span><span class="sxs-lookup"><span data-stu-id="3e598-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e598-116">Tipo de datos: **CIM \_ Product**</span><span class="sxs-lookup"><span data-stu-id="3e598-116">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="3e598-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e598-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3e598-118">Referencia al producto que forma parte de la FRU.</span><span class="sxs-lookup"><span data-stu-id="3e598-118">Reference to the product that is a part of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="3e598-119">**FRU**</span><span class="sxs-lookup"><span data-stu-id="3e598-119">**FRU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3e598-120">Tipo de datos **: \_ FRU de CIM**</span><span class="sxs-lookup"><span data-stu-id="3e598-120">Data type: **CIM\_FRU**</span></span>
</dt> <dt>

<span data-ttu-id="3e598-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3e598-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3e598-122">Calificadores: [**agregado**](/windows/desktop/WmiSdk/standard-qualifiers), [**máximo**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="3e598-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="3e598-123">Referencia a la FRU.</span><span class="sxs-lookup"><span data-stu-id="3e598-123">Reference to the FRU.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e598-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3e598-124">Remarks</span></span>

<span data-ttu-id="3e598-125">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="3e598-125">WMI does not implement this class.</span></span>

<span data-ttu-id="3e598-126">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="3e598-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3e598-127">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="3e598-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e598-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e598-128">Requirements</span></span>



| <span data-ttu-id="3e598-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e598-129">Requirement</span></span> | <span data-ttu-id="3e598-130">Value</span><span class="sxs-lookup"><span data-stu-id="3e598-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3e598-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e598-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3e598-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e598-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3e598-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e598-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3e598-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e598-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3e598-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3e598-135">Namespace</span></span><br/>                | <span data-ttu-id="3e598-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3e598-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3e598-137">MOF</span><span class="sxs-lookup"><span data-stu-id="3e598-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3e598-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3e598-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3e598-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3e598-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e598-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e598-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

