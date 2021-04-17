---
description: El método Delete elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.
ms.assetid: 04d43ac5-b7e6-409f-999a-577232539c15
ms.tgt_platform: multiple
title: Método Delete de la clase CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d8462d097834015883d47ec3da0d70e517a4ead0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659728"
---
# <a name="delete-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="6a628-103">Método Delete de la \_ clase CIM LogicalFile</span><span class="sxs-lookup"><span data-stu-id="6a628-103">Delete method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="6a628-104">El método **Delete** elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="6a628-104">The **Delete** method deletes the logical file (or directory) specified in the object path.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6a628-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="6a628-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6a628-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6a628-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6a628-107">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="6a628-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6a628-108">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6a628-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a628-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a628-109">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="6a628-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6a628-110">Parameters</span></span>

<span data-ttu-id="6a628-111">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="6a628-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6a628-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6a628-112">Return value</span></span>

<span data-ttu-id="6a628-113">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="6a628-113">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="6a628-114">**Success**</span><span class="sxs-lookup"><span data-stu-id="6a628-114">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="6a628-115">0</span><span class="sxs-lookup"><span data-stu-id="6a628-115">0</span></span>

<span data-ttu-id="6a628-116">Correcto.</span><span class="sxs-lookup"><span data-stu-id="6a628-116">Success.</span></span>

</dd> <dt>

<span data-ttu-id="6a628-117">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="6a628-117">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="6a628-118">2</span><span class="sxs-lookup"><span data-stu-id="6a628-118">2</span></span>

<span data-ttu-id="6a628-119">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="6a628-119">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="6a628-120">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="6a628-120">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="6a628-121">8</span><span class="sxs-lookup"><span data-stu-id="6a628-121">8</span></span>

<span data-ttu-id="6a628-122">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="6a628-122">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="6a628-123">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="6a628-123">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="6a628-124">9</span><span class="sxs-lookup"><span data-stu-id="6a628-124">9</span></span>

<span data-ttu-id="6a628-125">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="6a628-125">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="6a628-126">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="6a628-126">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="6a628-127">10</span><span class="sxs-lookup"><span data-stu-id="6a628-127">10</span></span>

<span data-ttu-id="6a628-128">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="6a628-128">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6a628-129">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="6a628-129">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="6a628-130">11</span><span class="sxs-lookup"><span data-stu-id="6a628-130">11</span></span>

<span data-ttu-id="6a628-131">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="6a628-131">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="6a628-132">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="6a628-132">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="6a628-133">12</span><span class="sxs-lookup"><span data-stu-id="6a628-133">12</span></span>

<span data-ttu-id="6a628-134">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="6a628-134">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="6a628-135">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="6a628-135">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="6a628-136">13</span><span class="sxs-lookup"><span data-stu-id="6a628-136">13</span></span>

<span data-ttu-id="6a628-137">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="6a628-137">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="6a628-138">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="6a628-138">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="6a628-139">14</span><span class="sxs-lookup"><span data-stu-id="6a628-139">14</span></span>

<span data-ttu-id="6a628-140">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="6a628-140">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="6a628-141">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="6a628-141">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="6a628-142">15</span><span class="sxs-lookup"><span data-stu-id="6a628-142">15</span></span>

<span data-ttu-id="6a628-143">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="6a628-143">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="6a628-144">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="6a628-144">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="6a628-145">16</span><span class="sxs-lookup"><span data-stu-id="6a628-145">16</span></span>

<span data-ttu-id="6a628-146">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="6a628-146">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="6a628-147">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="6a628-147">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="6a628-148">17</span><span class="sxs-lookup"><span data-stu-id="6a628-148">17</span></span>

<span data-ttu-id="6a628-149">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="6a628-149">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="6a628-150">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="6a628-150">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="6a628-151">21</span><span class="sxs-lookup"><span data-stu-id="6a628-151">21</span></span>

<span data-ttu-id="6a628-152">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="6a628-152">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a628-153">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a628-153">Remarks</span></span>

<span data-ttu-id="6a628-154">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="6a628-154">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="6a628-155">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="6a628-155">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="6a628-156">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="6a628-156">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6a628-157">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="6a628-157">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a628-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a628-158">Requirements</span></span>



| <span data-ttu-id="6a628-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a628-159">Requirement</span></span> | <span data-ttu-id="6a628-160">Value</span><span class="sxs-lookup"><span data-stu-id="6a628-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a628-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a628-161">Minimum supported client</span></span><br/> | <span data-ttu-id="6a628-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6a628-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6a628-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a628-163">Minimum supported server</span></span><br/> | <span data-ttu-id="6a628-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6a628-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6a628-165">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6a628-165">Namespace</span></span><br/>                | <span data-ttu-id="6a628-166">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6a628-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6a628-167">MOF</span><span class="sxs-lookup"><span data-stu-id="6a628-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6a628-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6a628-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6a628-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6a628-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a628-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a628-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a628-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a628-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a628-172">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="6a628-172">CIM\_LogicalFile</span></span>](delete-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="6a628-173">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="6a628-173">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

