---
description: 'Método copy de la clase CIM_LogicalFile : el método Copy copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto a la ubicación especificada por el parámetro de entrada.'
ms.assetid: 643946e4-5d32-4839-ae1f-80ec7cede429
ms.tgt_platform: multiple
title: Método Copy de la clase CIM_LogicalFile copia
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
ms.openlocfilehash: 10ba9c28bde9d909d947e5a73241ce1aa8f1e956
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089733"
---
# <a name="copy-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="24e17-103">Método Copy de la clase \_ LogicalFile de CIM</span><span class="sxs-lookup"><span data-stu-id="24e17-103">Copy method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="24e17-104">El **método Copy** copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto a la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="24e17-104">The **Copy** method copies the logical file (or directory) specified in the object path to the location specified by the input parameter.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="24e17-105">Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI.</span><span class="sxs-lookup"><span data-stu-id="24e17-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="24e17-106">WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="24e17-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="24e17-107">En este tema se usa Managed Object Format sintaxis MOF .</span><span class="sxs-lookup"><span data-stu-id="24e17-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="24e17-108">Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="24e17-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="24e17-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="24e17-109">Syntax</span></span>


```mof
uint32 Copy(
  [in] string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="24e17-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="24e17-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24e17-111">*FileName* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="24e17-111">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24e17-112">Nombre completo del archivo de destino (o directorio).</span><span class="sxs-lookup"><span data-stu-id="24e17-112">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="24e17-113">Ejemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="24e17-113">Example: "c:\\temp\\newdirectory"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24e17-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="24e17-114">Return value</span></span>

<span data-ttu-id="24e17-115">Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="24e17-115">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="24e17-116">**Success**</span><span class="sxs-lookup"><span data-stu-id="24e17-116">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="24e17-117">0</span><span class="sxs-lookup"><span data-stu-id="24e17-117">0</span></span>

<span data-ttu-id="24e17-118">Correcto.</span><span class="sxs-lookup"><span data-stu-id="24e17-118">Success.</span></span>

</dd> <dt>

<span data-ttu-id="24e17-119">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="24e17-119">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="24e17-120">2</span><span class="sxs-lookup"><span data-stu-id="24e17-120">2</span></span>

<span data-ttu-id="24e17-121">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="24e17-121">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="24e17-122">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="24e17-122">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="24e17-123">8</span><span class="sxs-lookup"><span data-stu-id="24e17-123">8</span></span>

<span data-ttu-id="24e17-124">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="24e17-124">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="24e17-125">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="24e17-125">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="24e17-126">9</span><span class="sxs-lookup"><span data-stu-id="24e17-126">9</span></span>

<span data-ttu-id="24e17-127">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="24e17-127">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="24e17-128">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="24e17-128">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="24e17-129">10</span><span class="sxs-lookup"><span data-stu-id="24e17-129">10</span></span>

<span data-ttu-id="24e17-130">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="24e17-130">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="24e17-131">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="24e17-131">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="24e17-132">11</span><span class="sxs-lookup"><span data-stu-id="24e17-132">11</span></span>

<span data-ttu-id="24e17-133">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="24e17-133">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="24e17-134">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="24e17-134">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="24e17-135">12</span><span class="sxs-lookup"><span data-stu-id="24e17-135">12</span></span>

<span data-ttu-id="24e17-136">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="24e17-136">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="24e17-137">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="24e17-137">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="24e17-138">13</span><span class="sxs-lookup"><span data-stu-id="24e17-138">13</span></span>

<span data-ttu-id="24e17-139">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="24e17-139">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="24e17-140">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="24e17-140">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="24e17-141">14</span><span class="sxs-lookup"><span data-stu-id="24e17-141">14</span></span>

<span data-ttu-id="24e17-142">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="24e17-142">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="24e17-143">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="24e17-143">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="24e17-144">15</span><span class="sxs-lookup"><span data-stu-id="24e17-144">15</span></span>

<span data-ttu-id="24e17-145">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="24e17-145">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="24e17-146">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="24e17-146">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="24e17-147">16</span><span class="sxs-lookup"><span data-stu-id="24e17-147">16</span></span>

<span data-ttu-id="24e17-148">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="24e17-148">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="24e17-149">**Privilegios no mantenidos**</span><span class="sxs-lookup"><span data-stu-id="24e17-149">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="24e17-150">17</span><span class="sxs-lookup"><span data-stu-id="24e17-150">17</span></span>

<span data-ttu-id="24e17-151">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="24e17-151">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="24e17-152">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="24e17-152">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="24e17-153">21</span><span class="sxs-lookup"><span data-stu-id="24e17-153">21</span></span>

<span data-ttu-id="24e17-154">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="24e17-154">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="24e17-155">Comentarios</span><span class="sxs-lookup"><span data-stu-id="24e17-155">Remarks</span></span>

<span data-ttu-id="24e17-156">Wmi no implementa actualmente este método.</span><span class="sxs-lookup"><span data-stu-id="24e17-156">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="24e17-157">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="24e17-157">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="24e17-158">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="24e17-158">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="24e17-159">Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="24e17-159">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="24e17-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24e17-160">Requirements</span></span>



| <span data-ttu-id="24e17-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="24e17-161">Requirement</span></span> | <span data-ttu-id="24e17-162">Valor</span><span class="sxs-lookup"><span data-stu-id="24e17-162">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24e17-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24e17-163">Minimum supported client</span></span><br/> | <span data-ttu-id="24e17-164">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="24e17-164">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="24e17-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="24e17-165">Minimum supported server</span></span><br/> | <span data-ttu-id="24e17-166">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="24e17-166">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="24e17-167">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="24e17-167">Namespace</span></span><br/>                | <span data-ttu-id="24e17-168">\\CIMV2 raíz</span><span class="sxs-lookup"><span data-stu-id="24e17-168">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="24e17-169">MOF</span><span class="sxs-lookup"><span data-stu-id="24e17-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24e17-170"><dt>CIMWin32.mof</dt></span><span class="sxs-lookup"><span data-stu-id="24e17-170"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="24e17-171">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="24e17-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24e17-172"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24e17-172"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24e17-173">Consulte también</span><span class="sxs-lookup"><span data-stu-id="24e17-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24e17-174">CIM \_ LogicalFile</span><span class="sxs-lookup"><span data-stu-id="24e17-174">CIM\_LogicalFile</span></span>](copy-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="24e17-175">**CIM \_ LogicalFile**</span><span class="sxs-lookup"><span data-stu-id="24e17-175">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

