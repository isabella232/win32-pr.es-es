---
description: La \_ Asociación ProductSoftwareFeatures de CIM identifica las características de software para un producto determinado.
ms.assetid: cd6190f8-d86e-44c8-b506-48016a7c22e1
ms.tgt_platform: multiple
title: CIM_ProductSoftwareFeatures (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSoftwareFeatures
- CIM_ProductSoftwareFeatures.Component
- CIM_ProductSoftwareFeatures.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2d891d9465688d92c016217cecd8324588026535
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659447"
---
# <a name="cim_productsoftwarefeatures-class"></a><span data-ttu-id="39f03-103">\_Clase ProductSoftwareFeatures de CIM</span><span class="sxs-lookup"><span data-stu-id="39f03-103">CIM\_ProductSoftwareFeatures class</span></span>

<span data-ttu-id="39f03-104">La **Asociación \_ ProductSoftwareFeatures de CIM** identifica las características de software para un producto determinado.</span><span class="sxs-lookup"><span data-stu-id="39f03-104">The **CIM\_ProductSoftwareFeatures** association identifies the software features for a particular product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="39f03-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="39f03-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="39f03-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="39f03-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="39f03-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="39f03-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="39f03-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="39f03-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="39f03-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="39f03-109">Syntax</span></span>

``` syntax
[UUID("{7C39D12A-DB2B-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_ProductSoftwareFeatures
{
  CIM_SoftwareFeature REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a><span data-ttu-id="39f03-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="39f03-110">Members</span></span>

<span data-ttu-id="39f03-111">La clase **CIM \_ ProductSoftwareFeatures** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="39f03-111">The **CIM\_ProductSoftwareFeatures** class has these types of members:</span></span>

-   [<span data-ttu-id="39f03-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39f03-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="39f03-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="39f03-113">Properties</span></span>

<span data-ttu-id="39f03-114">La clase **CIM \_ ProductSoftwareFeatures** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="39f03-114">The **CIM\_ProductSoftwareFeatures** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="39f03-115">**Componente**</span><span class="sxs-lookup"><span data-stu-id="39f03-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f03-116">Tipo de datos: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="39f03-116">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="39f03-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39f03-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f03-118">Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39f03-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39f03-119">Referencia al componente.</span><span class="sxs-lookup"><span data-stu-id="39f03-119">Reference to the component.</span></span>

</dd> <dt>

<span data-ttu-id="39f03-120">**Producto**</span><span class="sxs-lookup"><span data-stu-id="39f03-120">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="39f03-121">Tipo de datos: **CIM \_ Product**</span><span class="sxs-lookup"><span data-stu-id="39f03-121">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="39f03-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="39f03-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="39f03-123">Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="39f03-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="39f03-124">Referencia al producto.</span><span class="sxs-lookup"><span data-stu-id="39f03-124">Reference to the product.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39f03-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39f03-125">Remarks</span></span>

<span data-ttu-id="39f03-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="39f03-126">WMI does not implement this class.</span></span> <span data-ttu-id="39f03-127">Para las clases WMI derivadas de **CIM \_ ProductSoftwareFeatures**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="39f03-127">For WMI classes derived from **CIM\_ProductSoftwareFeatures**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="39f03-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="39f03-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="39f03-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="39f03-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="39f03-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39f03-130">Requirements</span></span>



| <span data-ttu-id="39f03-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="39f03-131">Requirement</span></span> | <span data-ttu-id="39f03-132">Value</span><span class="sxs-lookup"><span data-stu-id="39f03-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39f03-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39f03-133">Minimum supported client</span></span><br/> | <span data-ttu-id="39f03-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="39f03-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="39f03-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39f03-135">Minimum supported server</span></span><br/> | <span data-ttu-id="39f03-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39f03-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="39f03-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="39f03-137">Namespace</span></span><br/>                | <span data-ttu-id="39f03-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="39f03-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="39f03-139">MOF</span><span class="sxs-lookup"><span data-stu-id="39f03-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39f03-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="39f03-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="39f03-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="39f03-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39f03-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39f03-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

