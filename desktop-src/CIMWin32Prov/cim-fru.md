---
description: La \_ clase CIM FRU representa una colección definida por el proveedor de productos y elementos físicos que están asociados a una unidad reemplazable en campo (FRU) para admitir, mantener o actualizar un producto en la ubicación del cliente.
ms.assetid: 4464ec3a-5509-4e15-9020-4abb2edd2570
ms.tgt_platform: multiple
title: CIM_FRU (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRU
- CIM_FRU.Caption
- CIM_FRU.Description
- CIM_FRU.FRUNumber
- CIM_FRU.IdentifyingNumber
- CIM_FRU.Name
- CIM_FRU.RevisionLevel
- CIM_FRU.Vendor
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d163c3c223159ad8e09aa6e36d63187ff0aa97f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807501"
---
# <a name="cim_fru-class"></a><span data-ttu-id="f4eec-103">Clase de FRU de CIM \_</span><span class="sxs-lookup"><span data-stu-id="f4eec-103">CIM\_FRU class</span></span>

<span data-ttu-id="f4eec-104">La clase **CIM \_ FRU** representa una colección definida por el proveedor de productos y elementos físicos que están asociados a una unidad reemplazable en campo (FRU) para admitir, mantener o actualizar un producto en la ubicación del cliente.</span><span class="sxs-lookup"><span data-stu-id="f4eec-104">The **CIM\_FRU** class represents a vendor-defined collection of products and physical elements that are associated with a field replaceable unit (FRU) to support, maintain, or upgrade a product at the customer's location.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f4eec-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="f4eec-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f4eec-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f4eec-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f4eec-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f4eec-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="f4eec-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="f4eec-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4eec-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4eec-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{778C74EE-DB2A-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_FRU
{
  string Caption;
  string Description;
  string FRUNumber;
  string IdentifyingNumber;
  string Name;
  string RevisionLevel;
  string Vendor;
};
```

## <a name="members"></a><span data-ttu-id="f4eec-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f4eec-110">Members</span></span>

<span data-ttu-id="f4eec-111">La clase de **\_ FRU de CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f4eec-111">The **CIM\_FRU** class has these types of members:</span></span>

-   [<span data-ttu-id="f4eec-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f4eec-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4eec-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f4eec-113">Properties</span></span>

<span data-ttu-id="f4eec-114">La clase de **\_ FRU de CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f4eec-114">The **CIM\_FRU** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4eec-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="f4eec-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4eec-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f4eec-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4eec-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4eec-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4eec-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f4eec-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f4eec-119">Breve descripción textual de la FRU.</span><span class="sxs-lookup"><span data-stu-id="f4eec-119">Short textual description for the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="f4eec-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="f4eec-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4eec-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f4eec-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4eec-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4eec-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4eec-123">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|FRU 002,3 de DMTF \| ")</span><span class="sxs-lookup"><span data-stu-id="f4eec-123">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.3")</span></span>
</dt> </dl>

<span data-ttu-id="f4eec-124">Descripción de la FRU.</span><span class="sxs-lookup"><span data-stu-id="f4eec-124">Description of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="f4eec-125">**FRUNumber**</span><span class="sxs-lookup"><span data-stu-id="f4eec-125">**FRUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4eec-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f4eec-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4eec-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4eec-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4eec-128">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|FRU \| 002,6 de DMTF "), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f4eec-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.6"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f4eec-129">Información de ordenación de FRU.</span><span class="sxs-lookup"><span data-stu-id="f4eec-129">FRU ordering information.</span></span>

</dd> <dt>

<span data-ttu-id="f4eec-130">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="f4eec-130">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4eec-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f4eec-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4eec-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4eec-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4eec-133">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|FRU \| 002,7 de DMTF "), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f4eec-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.7"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f4eec-134">Identificación del software, como un número de serie o un número de matriz en un chip de hardware.</span><span class="sxs-lookup"><span data-stu-id="f4eec-134">Identification on software, such as a serial number, or a die number on a hardware chip.</span></span>

</dd> <dt>

<span data-ttu-id="f4eec-135">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f4eec-135">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4eec-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f4eec-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4eec-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4eec-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4eec-138">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f4eec-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f4eec-139">Etiqueta por la que se conoce el objeto.</span><span class="sxs-lookup"><span data-stu-id="f4eec-139">Label by which the object is known.</span></span>

</dd> <dt>

<span data-ttu-id="f4eec-140">**RevisionLevel**</span><span class="sxs-lookup"><span data-stu-id="f4eec-140">**RevisionLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4eec-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f4eec-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4eec-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4eec-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4eec-143">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|FRU \| 002,8 de DMTF "), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="f4eec-143">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.8"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="f4eec-144">Nivel de revisión de la FRU.</span><span class="sxs-lookup"><span data-stu-id="f4eec-144">Revision level of the FRU.</span></span>

</dd> <dt>

<span data-ttu-id="f4eec-145">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="f4eec-145">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4eec-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f4eec-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f4eec-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f4eec-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f4eec-148">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|FRU \| 002,4 de DMTF "), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="f4eec-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|FRU\|002.4"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="f4eec-149">Nombre del proveedor.</span><span class="sxs-lookup"><span data-stu-id="f4eec-149">Name of the supplier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4eec-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f4eec-150">Remarks</span></span>

<span data-ttu-id="f4eec-151">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="f4eec-151">WMI does not implement this class.</span></span>

<span data-ttu-id="f4eec-152">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="f4eec-152">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f4eec-153">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="f4eec-153">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4eec-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4eec-154">Requirements</span></span>



| <span data-ttu-id="f4eec-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="f4eec-155">Requirement</span></span> | <span data-ttu-id="f4eec-156">Value</span><span class="sxs-lookup"><span data-stu-id="f4eec-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4eec-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4eec-157">Minimum supported client</span></span><br/> | <span data-ttu-id="f4eec-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4eec-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f4eec-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f4eec-159">Minimum supported server</span></span><br/> | <span data-ttu-id="f4eec-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4eec-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f4eec-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f4eec-161">Namespace</span></span><br/>                | <span data-ttu-id="f4eec-162">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f4eec-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f4eec-163">MOF</span><span class="sxs-lookup"><span data-stu-id="f4eec-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4eec-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4eec-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4eec-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f4eec-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4eec-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4eec-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

