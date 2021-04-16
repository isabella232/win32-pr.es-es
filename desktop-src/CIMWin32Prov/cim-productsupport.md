---
description: La \_ clase CIM ProductSupport representa una asociación entre el producto y el acceso de soporte que muestra cómo se obtiene la compatibilidad con el producto.
ms.assetid: 61c62556-0cf3-438c-b9c7-152505bf7ed6
ms.tgt_platform: multiple
title: CIM_ProductSupport (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSupport
- CIM_ProductSupport.Product
- CIM_ProductSupport.Support
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8d1b39e1eef8f9686eee66c629120feaea51c778
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659446"
---
# <a name="cim_productsupport-class"></a><span data-ttu-id="c15be-103">\_Clase ProductSupport de CIM</span><span class="sxs-lookup"><span data-stu-id="c15be-103">CIM\_ProductSupport class</span></span>

<span data-ttu-id="c15be-104">La clase **CIM \_ ProductSupport** representa una asociación entre el producto y el acceso de soporte que muestra cómo se obtiene la compatibilidad con el producto.</span><span class="sxs-lookup"><span data-stu-id="c15be-104">The **CIM\_ProductSupport** class represents an association between product and support access that conveys how support is obtained for the product.</span></span> <span data-ttu-id="c15be-105">Hay varios tipos de soporte técnico disponibles para un producto; el mismo objeto de soporte técnico puede proporcionar asistencia para varios productos.</span><span class="sxs-lookup"><span data-stu-id="c15be-105">Various types of support are available for a product; the same support object can provide assistance for multiple products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c15be-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="c15be-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c15be-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c15be-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c15be-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c15be-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c15be-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="c15be-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c15be-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c15be-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{8D6D6880-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductSupport
{
  CIM_Product       REF Product;
  CIM_SupportAccess REF Support;
};
```

## <a name="members"></a><span data-ttu-id="c15be-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="c15be-111">Members</span></span>

<span data-ttu-id="c15be-112">La clase **CIM \_ ProductSupport** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c15be-112">The **CIM\_ProductSupport** class has these types of members:</span></span>

-   [<span data-ttu-id="c15be-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c15be-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c15be-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c15be-114">Properties</span></span>

<span data-ttu-id="c15be-115">La clase **CIM \_ ProductSupport** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c15be-115">The **CIM\_ProductSupport** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c15be-116">**Producto**</span><span class="sxs-lookup"><span data-stu-id="c15be-116">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c15be-117">Tipo de datos: **CIM \_ Product**</span><span class="sxs-lookup"><span data-stu-id="c15be-117">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="c15be-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c15be-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c15be-119">Referencia al producto.</span><span class="sxs-lookup"><span data-stu-id="c15be-119">Reference to the product.</span></span>

</dd> <dt>

<span data-ttu-id="c15be-120">**Soporte técnico**</span><span class="sxs-lookup"><span data-stu-id="c15be-120">**Support**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c15be-121">Tipo de datos: **CIM \_ SupportAccess**</span><span class="sxs-lookup"><span data-stu-id="c15be-121">Data type: **CIM\_SupportAccess**</span></span>
</dt> <dt>

<span data-ttu-id="c15be-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c15be-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c15be-123">Referencia al soporte técnico del producto.</span><span class="sxs-lookup"><span data-stu-id="c15be-123">Reference to the product support.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c15be-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c15be-124">Remarks</span></span>

<span data-ttu-id="c15be-125">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="c15be-125">WMI does not implement this class.</span></span>

<span data-ttu-id="c15be-126">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c15be-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c15be-127">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c15be-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c15be-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c15be-128">Requirements</span></span>



| <span data-ttu-id="c15be-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="c15be-129">Requirement</span></span> | <span data-ttu-id="c15be-130">Value</span><span class="sxs-lookup"><span data-stu-id="c15be-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c15be-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c15be-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c15be-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c15be-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c15be-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c15be-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c15be-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c15be-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c15be-135">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c15be-135">Namespace</span></span><br/>                | <span data-ttu-id="c15be-136">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c15be-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c15be-137">MOF</span><span class="sxs-lookup"><span data-stu-id="c15be-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c15be-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c15be-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c15be-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c15be-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c15be-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c15be-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




