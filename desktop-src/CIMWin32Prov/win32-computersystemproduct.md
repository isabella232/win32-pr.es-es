---
description: Representa un producto. Esto incluye el software y el hardware utilizados en este equipo.
ms.assetid: 6241e703-4ce9-435f-bf36-4388e38a3ea5
ms.tgt_platform: multiple
title: Win32_ComputerSystemProduct (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystemProduct
- Win32_ComputerSystemProduct.Caption
- Win32_ComputerSystemProduct.Description
- Win32_ComputerSystemProduct.IdentifyingNumber
- Win32_ComputerSystemProduct.Name
- Win32_ComputerSystemProduct.SKUNumber
- Win32_ComputerSystemProduct.Vendor
- Win32_ComputerSystemProduct.Version
- Win32_ComputerSystemProduct.UUID
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8cab3dc8679c606076eca2f5cf704867aa9833c9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152916"
---
# <a name="win32_computersystemproduct-class"></a><span data-ttu-id="3084a-104">\_Clase Win32 ComputerSystemProduct</span><span class="sxs-lookup"><span data-stu-id="3084a-104">Win32\_ComputerSystemProduct class</span></span>

<span data-ttu-id="3084a-105">La [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **\_ ComputerSystemProduct de Win32** representa un producto.</span><span class="sxs-lookup"><span data-stu-id="3084a-105">The **Win32\_ComputerSystemProduct** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) represents a product.</span></span> <span data-ttu-id="3084a-106">Esto incluye el software y el hardware utilizados en este equipo.</span><span class="sxs-lookup"><span data-stu-id="3084a-106">This includes software and hardware used on this computer system.</span></span>

<span data-ttu-id="3084a-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="3084a-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="3084a-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="3084a-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3084a-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3084a-109">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{FAF76B96-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class Win32_ComputerSystemProduct : CIM_Product
{
  string Caption;
  string Description;
  string IdentifyingNumber;
  string Name;
  string SKUNumber;
  string Vendor;
  string Version;
  string UUID;
};
```

## <a name="members"></a><span data-ttu-id="3084a-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="3084a-110">Members</span></span>

<span data-ttu-id="3084a-111">La **clase \_ ComputerSystemProduct de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="3084a-111">The **Win32\_ComputerSystemProduct** class has these types of members:</span></span>

-   [<span data-ttu-id="3084a-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3084a-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3084a-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="3084a-113">Properties</span></span>

<span data-ttu-id="3084a-114">La **clase \_ ComputerSystemProduct de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="3084a-114">The **Win32\_ComputerSystemProduct** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3084a-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="3084a-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3084a-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3084a-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3084a-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3084a-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3084a-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3084a-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3084a-119">Breve descripción textual del producto.</span><span class="sxs-lookup"><span data-stu-id="3084a-119">Short textual description for the product.</span></span>

<span data-ttu-id="3084a-120">Esta propiedad se hereda del [**\_ producto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="3084a-120">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="3084a-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="3084a-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3084a-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3084a-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3084a-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3084a-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3084a-124">Descripción textual del producto.</span><span class="sxs-lookup"><span data-stu-id="3084a-124">Textual description of the product.</span></span>

<span data-ttu-id="3084a-125">Esta propiedad se hereda del [**\_ producto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="3084a-125">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="3084a-126">**IdentifyingNumber**</span><span class="sxs-lookup"><span data-stu-id="3084a-126">**IdentifyingNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3084a-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3084a-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3084a-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3084a-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3084a-129">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,4 ")</span><span class="sxs-lookup"><span data-stu-id="3084a-129">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.4")</span></span>
</dt> </dl>

<span data-ttu-id="3084a-130">Identificación del producto, como un número de serie en el software, un número de matriz en un chip de hardware o (para productos no comerciales) de un número de proyecto.</span><span class="sxs-lookup"><span data-stu-id="3084a-130">Product identification, such as a serial number on software, a die number on a hardware chip, or (for noncommercial products) a project number.</span></span>

<span data-ttu-id="3084a-131">Esta propiedad se hereda del [**\_ producto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="3084a-131">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="3084a-132">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="3084a-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3084a-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3084a-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3084a-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3084a-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3084a-135">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,2 ")</span><span class="sxs-lookup"><span data-stu-id="3084a-135">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="3084a-136">Nombre de producto usado comúnmente.</span><span class="sxs-lookup"><span data-stu-id="3084a-136">Commonly used product name.</span></span>

<span data-ttu-id="3084a-137">Esta propiedad se hereda del [**\_ producto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="3084a-137">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="3084a-138">**SKUNumber**</span><span class="sxs-lookup"><span data-stu-id="3084a-138">**SKUNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3084a-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3084a-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3084a-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3084a-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3084a-141">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="3084a-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="3084a-142">Información de la referencia de almacén (SKU) del producto.</span><span class="sxs-lookup"><span data-stu-id="3084a-142">Product's stock-keeping unit (SKU) information.</span></span>

<span data-ttu-id="3084a-143">Esta propiedad se hereda del [**\_ producto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="3084a-143">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="3084a-144">**UUID**</span><span class="sxs-lookup"><span data-stu-id="3084a-144">**UUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3084a-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3084a-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3084a-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3084a-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3084a-147">Calificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS \| tipo 1 \| UUID")</span><span class="sxs-lookup"><span data-stu-id="3084a-147">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("SMBIOS\|Type 1\|UUID")</span></span>
</dt> </dl>

<span data-ttu-id="3084a-148">Identificador único universal (UUID) de este producto.</span><span class="sxs-lookup"><span data-stu-id="3084a-148">Universally unique identifier (UUID) for this product.</span></span> <span data-ttu-id="3084a-149">Un UUID es un identificador de 128 bits que se garantiza que es diferente de otro UUID generado.</span><span class="sxs-lookup"><span data-stu-id="3084a-149">A UUID is a 128-bit identifier that is guaranteed to be different from other generated UUIDs.</span></span> <span data-ttu-id="3084a-150">Si no hay ningún UUID disponible, se usa un UUID de todos los ceros.</span><span class="sxs-lookup"><span data-stu-id="3084a-150">If a UUID is not available, a UUID of all zeros is used.</span></span>

<span data-ttu-id="3084a-151">Este valor procede del miembro **UUID** de la estructura de **información del sistema** en la información de SMBIOS.</span><span class="sxs-lookup"><span data-stu-id="3084a-151">This value comes from the **UUID** member of the **System Information** structure in the SMBIOS information.</span></span>

</dd> <dt>

<span data-ttu-id="3084a-152">**Proveedor**</span><span class="sxs-lookup"><span data-stu-id="3084a-152">**Vendor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3084a-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3084a-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3084a-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3084a-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3084a-155">Calificadores: [**\_ clave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,1 ")</span><span class="sxs-lookup"><span data-stu-id="3084a-155">Qualifiers: [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.1")</span></span>
</dt> </dl>

<span data-ttu-id="3084a-156">Nombre del proveedor del producto o entidad que vende el producto (el fabricante, el reseller, el OEM, etc.).</span><span class="sxs-lookup"><span data-stu-id="3084a-156">Name of the product's supplier, or the entity selling the product (the manufacturer, reseller, OEM, and so on).</span></span>

<span data-ttu-id="3084a-157">Esta propiedad se hereda del [**\_ producto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="3084a-157">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> <dt>

<span data-ttu-id="3084a-158">**Versión**</span><span class="sxs-lookup"><span data-stu-id="3084a-158">**Version**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3084a-159">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="3084a-159">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3084a-160">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="3084a-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3084a-161">Calificadores: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,3 ")</span><span class="sxs-lookup"><span data-stu-id="3084a-161">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="3084a-162">Información de versión del producto.</span><span class="sxs-lookup"><span data-stu-id="3084a-162">Product version information.</span></span>

<span data-ttu-id="3084a-163">Esta propiedad se hereda del [**\_ producto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="3084a-163">This property is inherited from [**CIM\_Product**](cim-product.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3084a-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3084a-164">Remarks</span></span>

<span data-ttu-id="3084a-165">La **clase \_ ComputerSystemProduct de Win32** se deriva [**del \_ producto CIM**](cim-product.md).</span><span class="sxs-lookup"><span data-stu-id="3084a-165">The **Win32\_ComputerSystemProduct** class is derived from [**CIM\_Product**](cim-product.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3084a-166">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="3084a-166">Examples</span></span>

<span data-ttu-id="3084a-167">En el ejemplo de PowerShell de [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) en la galería de TechNet se usa to **Win32 \_ ComputerSystemProduct** para recuperar una lista de hardware que no funciona mediante WMI.</span><span class="sxs-lookup"><span data-stu-id="3084a-167">The [Get-BrokenHardware.ps1](https://Gallery.TechNet.Microsoft.Com/dbb678f4-b95b-45c3-bc8b-2ae2d052448e) PowerShell sample on TechNet Gallery uses to **Win32\_ComputerSystemProduct** to retrieve a list of non-working hardware using WMI.</span></span>

## <a name="requirements"></a><span data-ttu-id="3084a-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3084a-168">Requirements</span></span>



| <span data-ttu-id="3084a-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="3084a-169">Requirement</span></span> | <span data-ttu-id="3084a-170">Value</span><span class="sxs-lookup"><span data-stu-id="3084a-170">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3084a-171">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3084a-171">Minimum supported client</span></span><br/> | <span data-ttu-id="3084a-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3084a-172">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3084a-173">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3084a-173">Minimum supported server</span></span><br/> | <span data-ttu-id="3084a-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3084a-174">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3084a-175">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="3084a-175">Namespace</span></span><br/>                | <span data-ttu-id="3084a-176">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3084a-176">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3084a-177">MOF</span><span class="sxs-lookup"><span data-stu-id="3084a-177">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3084a-178"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3084a-178"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3084a-179">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3084a-179">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3084a-180"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3084a-180"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3084a-181">Vea también</span><span class="sxs-lookup"><span data-stu-id="3084a-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3084a-182">**\_Producto CIM**</span><span class="sxs-lookup"><span data-stu-id="3084a-182">**CIM\_Product**</span></span>](cim-product.md)
</dt> <dt>

<span data-ttu-id="3084a-183">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3084a-183">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> </dl>

 

