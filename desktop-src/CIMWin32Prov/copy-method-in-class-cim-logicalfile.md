---
description: El método de copia copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.
ms.assetid: 643946e4-5d32-4839-ae1f-80ec7cede429
ms.tgt_platform: multiple
title: Método de copia de la clase CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4a69107bd173be0aa853c1541a1e1365148c2e59
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080212"
---
# <a name="copy-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="9caf3-103">Método de copia de la \_ clase LogicalFile de CIM</span><span class="sxs-lookup"><span data-stu-id="9caf3-103">Copy method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="9caf3-104">El método de **copia** copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="9caf3-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9caf3-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="9caf3-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9caf3-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9caf3-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9caf3-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="9caf3-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="9caf3-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="9caf3-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="9caf3-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9caf3-109">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="9caf3-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9caf3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9caf3-111">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="9caf3-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9caf3-112">Nombre completo del archivo de destino (o directorio).</span><span class="sxs-lookup"><span data-stu-id="9caf3-112">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="9caf3-113">Ejemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="9caf3-113">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9caf3-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9caf3-114">Return value</span></span>

<span data-ttu-id="9caf3-115">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="9caf3-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="9caf3-116">**Success**</span><span class="sxs-lookup"><span data-stu-id="9caf3-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="9caf3-117">0</span><span class="sxs-lookup"><span data-stu-id="9caf3-117">0</span></span>

<span data-ttu-id="9caf3-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="9caf3-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="9caf3-119">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="9caf3-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="9caf3-120">2</span><span class="sxs-lookup"><span data-stu-id="9caf3-120">2</span></span>

<span data-ttu-id="9caf3-121">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="9caf3-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="9caf3-122">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="9caf3-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="9caf3-123">8</span><span class="sxs-lookup"><span data-stu-id="9caf3-123">8</span></span>

<span data-ttu-id="9caf3-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="9caf3-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="9caf3-125">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="9caf3-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="9caf3-126">9</span><span class="sxs-lookup"><span data-stu-id="9caf3-126">9</span></span>

<span data-ttu-id="9caf3-127">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="9caf3-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="9caf3-128">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="9caf3-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="9caf3-129">10</span><span class="sxs-lookup"><span data-stu-id="9caf3-129">10</span></span>

<span data-ttu-id="9caf3-130">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="9caf3-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="9caf3-131">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="9caf3-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="9caf3-132">11</span><span class="sxs-lookup"><span data-stu-id="9caf3-132">11</span></span>

<span data-ttu-id="9caf3-133">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="9caf3-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="9caf3-134">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="9caf3-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="9caf3-135">12</span><span class="sxs-lookup"><span data-stu-id="9caf3-135">12</span></span>

<span data-ttu-id="9caf3-136">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="9caf3-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="9caf3-137">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="9caf3-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="9caf3-138">13</span><span class="sxs-lookup"><span data-stu-id="9caf3-138">13</span></span>

<span data-ttu-id="9caf3-139">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="9caf3-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="9caf3-140">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="9caf3-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="9caf3-141">14</span><span class="sxs-lookup"><span data-stu-id="9caf3-141">14</span></span>

<span data-ttu-id="9caf3-142">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="9caf3-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="9caf3-143">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="9caf3-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="9caf3-144">15</span><span class="sxs-lookup"><span data-stu-id="9caf3-144">15</span></span>

<span data-ttu-id="9caf3-145">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="9caf3-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="9caf3-146">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="9caf3-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="9caf3-147">16</span><span class="sxs-lookup"><span data-stu-id="9caf3-147">16</span></span>

<span data-ttu-id="9caf3-148">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="9caf3-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="9caf3-149">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="9caf3-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="9caf3-150">17</span><span class="sxs-lookup"><span data-stu-id="9caf3-150">17</span></span>

<span data-ttu-id="9caf3-151">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="9caf3-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="9caf3-152">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="9caf3-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="9caf3-153">21</span><span class="sxs-lookup"><span data-stu-id="9caf3-153">21</span></span>

<span data-ttu-id="9caf3-154">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="9caf3-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9caf3-155">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9caf3-155">Remarks</span></span>

<span data-ttu-id="9caf3-156">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="9caf3-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="9caf3-157">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="9caf3-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="9caf3-158">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="9caf3-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9caf3-159">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="9caf3-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9caf3-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9caf3-160">Requirements</span></span>



| <span data-ttu-id="9caf3-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="9caf3-161">Requirement</span></span> | <span data-ttu-id="9caf3-162">Value</span><span class="sxs-lookup"><span data-stu-id="9caf3-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9caf3-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9caf3-163">Minimum supported client</span></span><br/> | <span data-ttu-id="9caf3-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9caf3-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9caf3-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9caf3-165">Minimum supported server</span></span><br/> | <span data-ttu-id="9caf3-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9caf3-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9caf3-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9caf3-167">Namespace</span></span><br/>                | <span data-ttu-id="9caf3-168">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9caf3-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9caf3-169">MOF</span><span class="sxs-lookup"><span data-stu-id="9caf3-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9caf3-170"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9caf3-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9caf3-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9caf3-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9caf3-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9caf3-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9caf3-173">Vea también</span><span class="sxs-lookup"><span data-stu-id="9caf3-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9caf3-174">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="9caf3-174">CIM\_LogicalFile</span></span>](copy-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="9caf3-175">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="9caf3-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

