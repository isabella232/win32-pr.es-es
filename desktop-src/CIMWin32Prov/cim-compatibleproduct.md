---
description: La \_ clase CIM CompatibleProduct representa una asociación entre productos que indica si dos productos a los que se hace referencia son interoperables, por ejemplo, si se pueden instalar juntos o si puede ser el contenedor físico del otro, etc.
ms.assetid: d822b052-981a-4a66-8404-b4f5f4681502
ms.tgt_platform: multiple
title: CIM_CompatibleProduct (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CompatibleProduct
- CIM_CompatibleProduct.CompatibilityDescription
- CIM_CompatibleProduct.CompatibleProduct
- CIM_CompatibleProduct.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 94969b1f2e45a27e402e132a0b9593de413a653b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907335"
---
# <a name="cim_compatibleproduct-class"></a><span data-ttu-id="b6a5c-103">\_Clase CompatibleProduct de CIM</span><span class="sxs-lookup"><span data-stu-id="b6a5c-103">CIM\_CompatibleProduct class</span></span>

<span data-ttu-id="b6a5c-104">La clase **CIM \_ CompatibleProduct** representa una asociación entre productos que indica si dos productos a los que se hace referencia son interoperables, por ejemplo, si se pueden instalar juntos o si puede ser el contenedor físico del otro, etc.</span><span class="sxs-lookup"><span data-stu-id="b6a5c-104">The **CIM\_CompatibleProduct** class represents an association between products that indicates whether two referenced products are interoperable, such as whether they can be installed together, or whether one can be the physical container for the other, and so on.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b6a5c-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="b6a5c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b6a5c-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b6a5c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b6a5c-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b6a5c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b6a5c-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="b6a5c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6a5c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b6a5c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{2F648FBA-DB22-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_CompatibleProduct
{
  string          CompatibilityDescription;
  CIM_Product REF CompatibleProduct;
  CIM_Product REF Product;
};
```

## <a name="members"></a><span data-ttu-id="b6a5c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="b6a5c-110">Members</span></span>

<span data-ttu-id="b6a5c-111">La clase **CIM \_ CompatibleProduct** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b6a5c-111">The **CIM\_CompatibleProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="b6a5c-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6a5c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b6a5c-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b6a5c-113">Properties</span></span>

<span data-ttu-id="b6a5c-114">La clase **CIM \_ CompatibleProduct** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b6a5c-114">The **CIM\_CompatibleProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b6a5c-115">**CompatibilityDescription**</span><span class="sxs-lookup"><span data-stu-id="b6a5c-115">**CompatibilityDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6a5c-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b6a5c-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b6a5c-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6a5c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6a5c-118">Cadena de forma libre que define el modo en que los dos productos a los que se hace referencia son interoperables, compatibles y si existen limitaciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="b6a5c-118">Free-form string that defines how the two referenced products are interoperable, compatible, and whether there are compatibility limitations.</span></span>

</dd> <dt>

<span data-ttu-id="b6a5c-119">**CompatibleProduct**</span><span class="sxs-lookup"><span data-stu-id="b6a5c-119">**CompatibleProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6a5c-120">Tipo de datos: **CIM \_ Product**</span><span class="sxs-lookup"><span data-stu-id="b6a5c-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="b6a5c-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6a5c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6a5c-122">Referencia al producto compatible.</span><span class="sxs-lookup"><span data-stu-id="b6a5c-122">Reference to the compatible product.</span></span>

</dd> <dt>

<span data-ttu-id="b6a5c-123">**Producto**</span><span class="sxs-lookup"><span data-stu-id="b6a5c-123">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b6a5c-124">Tipo de datos: **CIM \_ Product**</span><span class="sxs-lookup"><span data-stu-id="b6a5c-124">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="b6a5c-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b6a5c-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b6a5c-126">Referencia al producto para el que se definen las ofertas compatibles.</span><span class="sxs-lookup"><span data-stu-id="b6a5c-126">Reference to the product for which compatible offerings are defined.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b6a5c-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6a5c-127">Remarks</span></span>

<span data-ttu-id="b6a5c-128">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="b6a5c-128">WMI does not implement this class.</span></span>

<span data-ttu-id="b6a5c-129">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="b6a5c-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b6a5c-130">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="b6a5c-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6a5c-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6a5c-131">Requirements</span></span>



| <span data-ttu-id="b6a5c-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6a5c-132">Requirement</span></span> | <span data-ttu-id="b6a5c-133">Value</span><span class="sxs-lookup"><span data-stu-id="b6a5c-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6a5c-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6a5c-134">Minimum supported client</span></span><br/> | <span data-ttu-id="b6a5c-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b6a5c-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b6a5c-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6a5c-136">Minimum supported server</span></span><br/> | <span data-ttu-id="b6a5c-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b6a5c-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b6a5c-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b6a5c-138">Namespace</span></span><br/>                | <span data-ttu-id="b6a5c-139">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b6a5c-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b6a5c-140">MOF</span><span class="sxs-lookup"><span data-stu-id="b6a5c-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b6a5c-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b6a5c-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b6a5c-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b6a5c-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b6a5c-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b6a5c-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




