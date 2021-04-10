---
description: El método Rename cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto. No se admite el cambio de nombre si el destino está en otra unidad o si se requiere sobrescribir un archivo lógico existente.
ms.assetid: 5a62ff64-d1d2-43a2-997c-0ad46896b31f
ms.tgt_platform: multiple
title: Cambiar el nombre del método de la clase CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0da38020d7b22dceb6f1d061f8feaf858eeb5f04
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153370"
---
# <a name="rename-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="ee963-104">Cambiar el nombre del método de la \_ clase CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="ee963-104">Rename method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="ee963-105">El método **Rename** cambia el nombre del archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="ee963-105">The **Rename** method renames the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="ee963-106">No se admite el cambio de nombre si el destino está en otra unidad o si se requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="ee963-106">Renaming is not supported if the destination is on another drive, or overwriting an existing logical file is required.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ee963-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="ee963-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="ee963-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="ee963-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="ee963-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="ee963-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ee963-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="ee963-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ee963-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ee963-111">Syntax</span></span>


```mof
uint32 Rename(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="ee963-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ee963-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee963-113">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ee963-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ee963-114">Nuevo nombre de archivo (o directorio) completo.</span><span class="sxs-lookup"><span data-stu-id="ee963-114">Fully qualified new file (or directory) name.</span></span>

<span data-ttu-id="ee963-115">Ejemplo: "c: \\ temp \\newfile.txt"</span><span class="sxs-lookup"><span data-stu-id="ee963-115">Example: "c:\\temp\\newfile.txt"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee963-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ee963-116">Return value</span></span>

<span data-ttu-id="ee963-117">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="ee963-117">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="ee963-118">**Success**</span><span class="sxs-lookup"><span data-stu-id="ee963-118">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="ee963-119">0</span><span class="sxs-lookup"><span data-stu-id="ee963-119">0</span></span>

<span data-ttu-id="ee963-120">Correcto.</span><span class="sxs-lookup"><span data-stu-id="ee963-120">Success.</span></span>

</dd> <dt>

<span data-ttu-id="ee963-121">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="ee963-121">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="ee963-122">2</span><span class="sxs-lookup"><span data-stu-id="ee963-122">2</span></span>

<span data-ttu-id="ee963-123">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="ee963-123">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="ee963-124">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="ee963-124">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="ee963-125">8</span><span class="sxs-lookup"><span data-stu-id="ee963-125">8</span></span>

<span data-ttu-id="ee963-126">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="ee963-126">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="ee963-127">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="ee963-127">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="ee963-128">9</span><span class="sxs-lookup"><span data-stu-id="ee963-128">9</span></span>

<span data-ttu-id="ee963-129">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="ee963-129">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="ee963-130">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="ee963-130">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="ee963-131">10</span><span class="sxs-lookup"><span data-stu-id="ee963-131">10</span></span>

<span data-ttu-id="ee963-132">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="ee963-132">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ee963-133">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="ee963-133">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="ee963-134">11</span><span class="sxs-lookup"><span data-stu-id="ee963-134">11</span></span>

<span data-ttu-id="ee963-135">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="ee963-135">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="ee963-136">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="ee963-136">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="ee963-137">12</span><span class="sxs-lookup"><span data-stu-id="ee963-137">12</span></span>

<span data-ttu-id="ee963-138">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="ee963-138">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="ee963-139">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="ee963-139">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="ee963-140">13</span><span class="sxs-lookup"><span data-stu-id="ee963-140">13</span></span>

<span data-ttu-id="ee963-141">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="ee963-141">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="ee963-142">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="ee963-142">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="ee963-143">14</span><span class="sxs-lookup"><span data-stu-id="ee963-143">14</span></span>

<span data-ttu-id="ee963-144">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="ee963-144">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="ee963-145">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="ee963-145">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="ee963-146">15</span><span class="sxs-lookup"><span data-stu-id="ee963-146">15</span></span>

<span data-ttu-id="ee963-147">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="ee963-147">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="ee963-148">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="ee963-148">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="ee963-149">16</span><span class="sxs-lookup"><span data-stu-id="ee963-149">16</span></span>

<span data-ttu-id="ee963-150">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="ee963-150">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="ee963-151">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="ee963-151">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="ee963-152">17</span><span class="sxs-lookup"><span data-stu-id="ee963-152">17</span></span>

<span data-ttu-id="ee963-153">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="ee963-153">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="ee963-154">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="ee963-154">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ee963-155">21</span><span class="sxs-lookup"><span data-stu-id="ee963-155">21</span></span>

<span data-ttu-id="ee963-156">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="ee963-156">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee963-157">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee963-157">Remarks</span></span>

<span data-ttu-id="ee963-158">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="ee963-158">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="ee963-159">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="ee963-159">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="ee963-160">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="ee963-160">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="ee963-161">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="ee963-161">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee963-162">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee963-162">Requirements</span></span>



| <span data-ttu-id="ee963-163">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee963-163">Requirement</span></span> | <span data-ttu-id="ee963-164">Value</span><span class="sxs-lookup"><span data-stu-id="ee963-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee963-165">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee963-165">Minimum supported client</span></span><br/> | <span data-ttu-id="ee963-166">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ee963-166">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ee963-167">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ee963-167">Minimum supported server</span></span><br/> | <span data-ttu-id="ee963-168">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee963-168">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ee963-169">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="ee963-169">Namespace</span></span><br/>                | <span data-ttu-id="ee963-170">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="ee963-170">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ee963-171">MOF</span><span class="sxs-lookup"><span data-stu-id="ee963-171">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee963-172"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ee963-172"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee963-173">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ee963-173">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee963-174"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee963-174"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee963-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="ee963-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee963-176">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="ee963-176">CIM\_LogicalFile</span></span>](rename-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="ee963-177">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="ee963-177">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

