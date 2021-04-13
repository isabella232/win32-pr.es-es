---
description: El método TakeOwnerShip obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto. Si el archivo lógico es un directorio, este método actúa de forma recursiva y toma la propiedad de todos los archivos y subdirectorios que contiene el directorio.
ms.assetid: 5db62da0-ac93-4a8c-af17-306e02bfa756
ms.tgt_platform: multiple
title: Método TakeOwnerShip de la clase CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.TakeOwnerShip
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7cdd9515a5e947a3e707464dcbd524c875f7785f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538415"
---
# <a name="takeownership-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="c018e-104">Método TakeOwnerShip de la \_ clase LogicalFile de CIM</span><span class="sxs-lookup"><span data-stu-id="c018e-104">TakeOwnerShip method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="c018e-105">El método **TakeOwnerShip** obtiene la propiedad del archivo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="c018e-105">The **TakeOwnerShip** method obtains ownership of the logical file specified in the object path.</span></span> <span data-ttu-id="c018e-106">Si el archivo lógico es un directorio, este método actúa de forma recursiva y toma la propiedad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="c018e-106">If the logical file is a directory, then this method acts recursively, taking ownership of all files and sub-directories that the directory contains.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c018e-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="c018e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c018e-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c018e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c018e-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c018e-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c018e-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c018e-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c018e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c018e-111">Syntax</span></span>


```mof
uint32 TakeOwnerShip();
```



## <a name="parameters"></a><span data-ttu-id="c018e-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c018e-112">Parameters</span></span>

<span data-ttu-id="c018e-113">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c018e-113">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c018e-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c018e-114">Return value</span></span>

<span data-ttu-id="c018e-115">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="c018e-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c018e-116">**Success**</span><span class="sxs-lookup"><span data-stu-id="c018e-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="c018e-117">0</span><span class="sxs-lookup"><span data-stu-id="c018e-117">0</span></span>

<span data-ttu-id="c018e-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="c018e-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="c018e-119">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="c018e-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="c018e-120">2</span><span class="sxs-lookup"><span data-stu-id="c018e-120">2</span></span>

<span data-ttu-id="c018e-121">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="c018e-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="c018e-122">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="c018e-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="c018e-123">8</span><span class="sxs-lookup"><span data-stu-id="c018e-123">8</span></span>

<span data-ttu-id="c018e-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="c018e-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="c018e-125">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="c018e-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="c018e-126">9</span><span class="sxs-lookup"><span data-stu-id="c018e-126">9</span></span>

<span data-ttu-id="c018e-127">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="c018e-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="c018e-128">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="c018e-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="c018e-129">10</span><span class="sxs-lookup"><span data-stu-id="c018e-129">10</span></span>

<span data-ttu-id="c018e-130">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="c018e-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c018e-131">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="c018e-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="c018e-132">11</span><span class="sxs-lookup"><span data-stu-id="c018e-132">11</span></span>

<span data-ttu-id="c018e-133">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="c018e-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c018e-134">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="c018e-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="c018e-135">12</span><span class="sxs-lookup"><span data-stu-id="c018e-135">12</span></span>

<span data-ttu-id="c018e-136">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="c018e-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c018e-137">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="c018e-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="c018e-138">13</span><span class="sxs-lookup"><span data-stu-id="c018e-138">13</span></span>

<span data-ttu-id="c018e-139">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="c018e-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c018e-140">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="c018e-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="c018e-141">14</span><span class="sxs-lookup"><span data-stu-id="c018e-141">14</span></span>

<span data-ttu-id="c018e-142">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="c018e-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c018e-143">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="c018e-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="c018e-144">15</span><span class="sxs-lookup"><span data-stu-id="c018e-144">15</span></span>

<span data-ttu-id="c018e-145">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="c018e-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c018e-146">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="c018e-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="c018e-147">16</span><span class="sxs-lookup"><span data-stu-id="c018e-147">16</span></span>

<span data-ttu-id="c018e-148">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="c018e-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="c018e-149">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="c018e-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="c018e-150">17</span><span class="sxs-lookup"><span data-stu-id="c018e-150">17</span></span>

<span data-ttu-id="c018e-151">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="c018e-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="c018e-152">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="c018e-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c018e-153">21</span><span class="sxs-lookup"><span data-stu-id="c018e-153">21</span></span>

<span data-ttu-id="c018e-154">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="c018e-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c018e-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c018e-155">Remarks</span></span>

<span data-ttu-id="c018e-156">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="c018e-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="c018e-157">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="c018e-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="c018e-158">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="c018e-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c018e-159">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="c018e-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c018e-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c018e-160">Requirements</span></span>



| <span data-ttu-id="c018e-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="c018e-161">Requirement</span></span> | <span data-ttu-id="c018e-162">Value</span><span class="sxs-lookup"><span data-stu-id="c018e-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c018e-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c018e-163">Minimum supported client</span></span><br/> | <span data-ttu-id="c018e-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c018e-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c018e-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c018e-165">Minimum supported server</span></span><br/> | <span data-ttu-id="c018e-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c018e-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c018e-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c018e-167">Namespace</span></span><br/>                | <span data-ttu-id="c018e-168">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c018e-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c018e-169">MOF</span><span class="sxs-lookup"><span data-stu-id="c018e-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c018e-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c018e-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c018e-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c018e-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c018e-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c018e-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c018e-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="c018e-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c018e-174">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="c018e-174">CIM\_LogicalFile</span></span>](takeownership-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="c018e-175">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="c018e-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

