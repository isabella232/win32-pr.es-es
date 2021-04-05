---
description: La \_ clase CIM ProductProductDependency representa una asociación entre dos productos, lo que indica que se debe instalar o ausente un para que el otro funcione. Es conceptualmente equivalente a la \_ Asociación ServiceServiceDependency de CIM.
ms.assetid: 898b9993-3bdc-4a7c-98c1-ed960014ace8
ms.tgt_platform: multiple
title: CIM_ProductProductDependency (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductProductDependency
- CIM_ProductProductDependency.DependentProduct
- CIM_ProductProductDependency.RequiredProduct
- CIM_ProductProductDependency.TypeOfDependency
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 094800b3a2d50d7be4039d5850f9ac1d3f236a40
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080141"
---
# <a name="cim_productproductdependency-class"></a><span data-ttu-id="62119-104">\_Clase ProductProductDependency de CIM</span><span class="sxs-lookup"><span data-stu-id="62119-104">CIM\_ProductProductDependency class</span></span>

<span data-ttu-id="62119-105">La clase **CIM \_ ProductProductDependency** representa una asociación entre dos productos, lo que indica que se debe instalar o ausente un para que el otro funcione.</span><span class="sxs-lookup"><span data-stu-id="62119-105">The **CIM\_ProductProductDependency** class represents an association between two products, which indicates that one must be installed or absent for the other to function.</span></span> <span data-ttu-id="62119-106">Es conceptualmente equivalente a la Asociación [**\_ ServiceServiceDependency de CIM**](cim-serviceservicedependency.md) .</span><span class="sxs-lookup"><span data-stu-id="62119-106">This is conceptually equivalent to the [**CIM\_ServiceServiceDependency**](cim-serviceservicedependency.md) association.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62119-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="62119-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="62119-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="62119-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="62119-109">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="62119-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="62119-110">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="62119-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="62119-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="62119-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{65878E68-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductProductDependency
{
  CIM_Product REF DependentProduct;
  CIM_Product REF RequiredProduct;
  uint16          TypeOfDependency;
};
```

## <a name="members"></a><span data-ttu-id="62119-112">Miembros</span><span class="sxs-lookup"><span data-stu-id="62119-112">Members</span></span>

<span data-ttu-id="62119-113">La clase **CIM \_ ProductProductDependency** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="62119-113">The **CIM\_ProductProductDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="62119-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="62119-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="62119-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="62119-115">Properties</span></span>

<span data-ttu-id="62119-116">La clase **CIM \_ ProductProductDependency** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="62119-116">The **CIM\_ProductProductDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="62119-117">**DependentProduct**</span><span class="sxs-lookup"><span data-stu-id="62119-117">**DependentProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62119-118">Tipo de datos: **CIM \_ Product**</span><span class="sxs-lookup"><span data-stu-id="62119-118">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="62119-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="62119-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62119-120">Referencia al producto que depende de otro producto.</span><span class="sxs-lookup"><span data-stu-id="62119-120">Reference to the product that is dependent on another product.</span></span>

</dd> <dt>

<span data-ttu-id="62119-121">**RequiredProduct**</span><span class="sxs-lookup"><span data-stu-id="62119-121">**RequiredProduct**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62119-122">Tipo de datos: **CIM \_ Product**</span><span class="sxs-lookup"><span data-stu-id="62119-122">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="62119-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="62119-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62119-124">Referencia al producto requerido.</span><span class="sxs-lookup"><span data-stu-id="62119-124">Reference to the required product.</span></span>

</dd> <dt>

<span data-ttu-id="62119-125">**TypeOfDependency**</span><span class="sxs-lookup"><span data-stu-id="62119-125">**TypeOfDependency**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="62119-126">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="62119-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="62119-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="62119-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="62119-128">Naturaleza de la dependencia del producto.</span><span class="sxs-lookup"><span data-stu-id="62119-128">Nature of the product dependency.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="62119-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconocido** (0)</span><span class="sxs-lookup"><span data-stu-id="62119-129"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="62119-130">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="62119-130">Unknown.</span></span>

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="62119-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Otro** (1)</span><span class="sxs-lookup"><span data-stu-id="62119-131"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="62119-132">Otros.</span><span class="sxs-lookup"><span data-stu-id="62119-132">Other.</span></span>

</dd> <dt>

<span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>

<span data-ttu-id="62119-133"><span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>El **producto debe estar instalado** (2)</span><span class="sxs-lookup"><span data-stu-id="62119-133"><span id="Product_Must_Be_Installed"></span><span id="product_must_be_installed"></span><span id="PRODUCT_MUST_BE_INSTALLED"></span>**Product Must Be Installed** (2)</span></span>


</dt> <dd>

<span data-ttu-id="62119-134">El producto debe estar instalado.</span><span class="sxs-lookup"><span data-stu-id="62119-134">Product must be installed.</span></span>

</dd> <dt>

<span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>

<span data-ttu-id="62119-135"><span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>El **producto no debe estar instalado** (3)</span><span class="sxs-lookup"><span data-stu-id="62119-135"><span id="Product_Must_Not_Be_Installed"></span><span id="product_must_not_be_installed"></span><span id="PRODUCT_MUST_NOT_BE_INSTALLED"></span>**Product Must Not Be Installed** (3)</span></span>


</dt> <dd>

<span data-ttu-id="62119-136">El producto no debe estar instalado.</span><span class="sxs-lookup"><span data-stu-id="62119-136">Product must not be installed.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62119-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="62119-137">Remarks</span></span>

<span data-ttu-id="62119-138">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="62119-138">WMI does not implement this class.</span></span>

<span data-ttu-id="62119-139">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="62119-139">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="62119-140">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="62119-140">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="62119-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="62119-141">Requirements</span></span>



| <span data-ttu-id="62119-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="62119-142">Requirement</span></span> | <span data-ttu-id="62119-143">Value</span><span class="sxs-lookup"><span data-stu-id="62119-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="62119-144">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62119-144">Minimum supported client</span></span><br/> | <span data-ttu-id="62119-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62119-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="62119-146">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="62119-146">Minimum supported server</span></span><br/> | <span data-ttu-id="62119-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62119-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="62119-148">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="62119-148">Namespace</span></span><br/>                | <span data-ttu-id="62119-149">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="62119-149">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="62119-150">MOF</span><span class="sxs-lookup"><span data-stu-id="62119-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="62119-151"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="62119-151"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="62119-152">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="62119-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62119-153"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62119-153"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




