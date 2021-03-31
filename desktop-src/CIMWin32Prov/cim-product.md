---
description: La \_ clase de producto CIM es una clase concreta que representa una colección de elementos físicos, características de software y otros productos, adquiridos como una unidad.
ms.assetid: beb20f61-de39-4221-8d29-4727104518d5
ms.tgt_platform: multiple
title: CIM_Product (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Product
- CIM_Product.Caption
- CIM_Product.Description
- CIM_Product.IdentifyingNumber
- CIM_Product.Name
- CIM_Product.SKUNumber
- CIM_Product.Vendor
- CIM_Product.Version
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 16c8541a18185d721bbdcbf23acaeb67adf508c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807154"
---
# <a name="cim_product-class"></a><span data-ttu-id="bd2d5-103">CIM ( \_ clase de productos)</span><span class="sxs-lookup"><span data-stu-id="bd2d5-103">CIM\_Product class</span></span>

<span data-ttu-id="bd2d5-104">La clase de **\_ producto CIM** es una clase concreta que representa una colección de elementos físicos, características de software y otros productos, adquiridos como una unidad.</span><span class="sxs-lookup"><span data-stu-id="bd2d5-104">The **CIM\_Product** class is a concrete class that represents a collection of physical elements, software features and, other products, acquired as a unit.</span></span> <span data-ttu-id="bd2d5-105">La adquisición implica un acuerdo entre el proveedor y el consumidor, que puede tener implicaciones en las licencias, el soporte técnico y la garantía del producto.</span><span class="sxs-lookup"><span data-stu-id="bd2d5-105">Acquisition implies an agreement between the supplier and consumer, which can have implications on product licensing, support, and warranty.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bd2d5-106">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="bd2d5-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bd2d5-107">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bd2d5-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bd2d5-108">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="bd2d5-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="bd2d5-109">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="bd2d5-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd2d5-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bd2d5-110">Syntax</span></span>

``` syntax
[abstract, UUID("{FAF76B63-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
};
```

## <a name="members"></a><span data-ttu-id="bd2d5-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="bd2d5-111">Members</span></span>

<span data-ttu-id="bd2d5-112">La clase de **\_ producto CIM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="bd2d5-112">The **CIM\_Product** class has these types of members:</span></span>

-   [<span data-ttu-id="bd2d5-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bd2d5-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bd2d5-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="bd2d5-114">Properties</span></span>

<span data-ttu-id="bd2d5-115">La clase de **\_ producto CIM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="bd2d5-115">The **CIM\_Product** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="bd2d5-116">**Caption**</span><span class="sxs-lookup"><span data-stu-id="bd2d5-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd2d5-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bd2d5-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd2d5-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd2d5-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd2d5-119">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="bd2d5-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bd2d5-120">Breve descripción textual del producto.</span><span class="sxs-lookup"><span data-stu-id="bd2d5-120">Short textual description for the product.</span></span>

</dd> <dt>

<span data-ttu-id="bd2d5-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="bd2d5-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd2d5-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bd2d5-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd2d5-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd2d5-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="bd2d5-124">Descripción textual del producto.</span><span class="sxs-lookup"><span data-stu-id="bd2d5-124">Textual description of the product.</span></span>

</dd> <dt>

<span data-ttu-id="bd2d5-125">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="bd2d5-125">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd2d5-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bd2d5-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd2d5-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd2d5-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd2d5-128">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="bd2d5-128">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="bd2d5-129">Identificación del producto, como un número de serie en el software, un número de matriz en un chip de hardware o (para productos no comerciales) de un número de proyecto.</span><span class="sxs-lookup"><span data-stu-id="bd2d5-129">Product identification, such as a serial number on software, a die number on a hardware chip, or (for noncommercial products) a project number.</span></span>

</dd> <dt>

<span data-ttu-id="bd2d5-130">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="bd2d5-130">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd2d5-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bd2d5-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd2d5-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd2d5-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd2d5-133">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="bd2d5-133">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="bd2d5-134">Nombre de producto usado comúnmente.</span><span class="sxs-lookup"><span data-stu-id="bd2d5-134">Commonly used product name.</span></span>

</dd> <dt>

<span data-ttu-id="bd2d5-135">**SKUNumber**</span><span class="sxs-lookup"><span data-stu-id="bd2d5-135">**SKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd2d5-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bd2d5-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd2d5-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd2d5-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd2d5-138">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="bd2d5-138">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="bd2d5-139">Información de la referencia de almacén (SKU) del producto.</span><span class="sxs-lookup"><span data-stu-id="bd2d5-139">Product's stock-keeping unit (SKU) information.</span></span>

</dd> <dt>

<span data-ttu-id="bd2d5-140">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="bd2d5-140">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd2d5-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bd2d5-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd2d5-142">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd2d5-142">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd2d5-143">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="bd2d5-143">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="bd2d5-144">Nombre del proveedor del producto o entidad que vende el producto (el fabricante, el reseller, el OEM, etc.).</span><span class="sxs-lookup"><span data-stu-id="bd2d5-144">Name of the product's supplier, or the entity selling the product (the manufacturer, reseller, OEM, and so on).</span></span>

</dd> <dt>

<span data-ttu-id="bd2d5-145">**Versión**</span><span class="sxs-lookup"><span data-stu-id="bd2d5-145">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="bd2d5-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="bd2d5-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="bd2d5-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="bd2d5-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="bd2d5-148">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="bd2d5-148">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="bd2d5-149">Información de versión del producto.</span><span class="sxs-lookup"><span data-stu-id="bd2d5-149">Product version information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bd2d5-150">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bd2d5-150">Remarks</span></span>

<span data-ttu-id="bd2d5-151">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="bd2d5-151">WMI does not implement this class.</span></span> <span data-ttu-id="bd2d5-152">Para las clases WMI que se derivan de un **\_ producto CIM**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="bd2d5-152">For WMI classes that are derived from **CIM\_Product**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="bd2d5-153">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="bd2d5-153">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bd2d5-154">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="bd2d5-154">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd2d5-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bd2d5-155">Requirements</span></span>



| <span data-ttu-id="bd2d5-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="bd2d5-156">Requirement</span></span> | <span data-ttu-id="bd2d5-157">Value</span><span class="sxs-lookup"><span data-stu-id="bd2d5-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd2d5-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd2d5-158">Minimum supported client</span></span><br/> | <span data-ttu-id="bd2d5-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd2d5-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bd2d5-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bd2d5-160">Minimum supported server</span></span><br/> | <span data-ttu-id="bd2d5-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd2d5-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bd2d5-162">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bd2d5-162">Namespace</span></span><br/>                | <span data-ttu-id="bd2d5-163">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bd2d5-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bd2d5-164">MOF</span><span class="sxs-lookup"><span data-stu-id="bd2d5-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bd2d5-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bd2d5-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bd2d5-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bd2d5-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd2d5-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd2d5-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

