---
description: El método DeleteEx elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del método Delete.
ms.assetid: 53785f2e-8796-446c-8228-9abc2d9a0d68
ms.tgt_platform: multiple
title: Método DeleteEx de la clase CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.DeleteEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4f9799513111ff53bb97c14feaf70c922dfb085
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538703"
---
# <a name="deleteex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="dc215-104">Método DeleteEx de la \_ clase LogicalFile de CIM</span><span class="sxs-lookup"><span data-stu-id="dc215-104">DeleteEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="dc215-105">El método **DeleteEx** elimina el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="dc215-105">The **DeleteEx** method deletes the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="dc215-106">Este método es una versión extendida del método [**Delete**](delete-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="dc215-106">This method is an extended version of the [**Delete**](delete-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dc215-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="dc215-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="dc215-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="dc215-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="dc215-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="dc215-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="dc215-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="dc215-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="dc215-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dc215-111">Syntax</span></span>


```mof
uint32 DeleteEx(
  [out]          string StopFileName,
  [in, optional] string StartFileName
);
```



## <a name="parameters"></a><span data-ttu-id="dc215-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc215-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc215-113">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="dc215-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc215-114">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="dc215-114">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="dc215-115">Este parámetro es NULL si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="dc215-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="dc215-116">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="dc215-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="dc215-117">Cadena que nombra el archivo secundario (o directorio) que se va a utilizar como punto de partida para el método.</span><span class="sxs-lookup"><span data-stu-id="dc215-117">String that names the child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="dc215-118">Normalmente, este parámetro es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="dc215-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="dc215-119">Si este parámetro es null, la operación se realiza en el archivo o directorio especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="dc215-119">If this parameter is null, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc215-120">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc215-120">Return value</span></span>

<span data-ttu-id="dc215-121">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="dc215-121">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="dc215-122">**Success**</span><span class="sxs-lookup"><span data-stu-id="dc215-122">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="dc215-123">0</span><span class="sxs-lookup"><span data-stu-id="dc215-123">0</span></span>

<span data-ttu-id="dc215-124">Correcto.</span><span class="sxs-lookup"><span data-stu-id="dc215-124">Success.</span></span>

</dd> <dt>

<span data-ttu-id="dc215-125">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="dc215-125">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="dc215-126">2</span><span class="sxs-lookup"><span data-stu-id="dc215-126">2</span></span>

<span data-ttu-id="dc215-127">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="dc215-127">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="dc215-128">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="dc215-128">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="dc215-129">8</span><span class="sxs-lookup"><span data-stu-id="dc215-129">8</span></span>

<span data-ttu-id="dc215-130">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="dc215-130">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="dc215-131">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="dc215-131">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="dc215-132">9</span><span class="sxs-lookup"><span data-stu-id="dc215-132">9</span></span>

<span data-ttu-id="dc215-133">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="dc215-133">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="dc215-134">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="dc215-134">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="dc215-135">10</span><span class="sxs-lookup"><span data-stu-id="dc215-135">10</span></span>

<span data-ttu-id="dc215-136">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="dc215-136">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="dc215-137">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="dc215-137">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="dc215-138">11</span><span class="sxs-lookup"><span data-stu-id="dc215-138">11</span></span>

<span data-ttu-id="dc215-139">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="dc215-139">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="dc215-140">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="dc215-140">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="dc215-141">12</span><span class="sxs-lookup"><span data-stu-id="dc215-141">12</span></span>

<span data-ttu-id="dc215-142">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="dc215-142">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="dc215-143">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="dc215-143">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="dc215-144">13</span><span class="sxs-lookup"><span data-stu-id="dc215-144">13</span></span>

<span data-ttu-id="dc215-145">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="dc215-145">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="dc215-146">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="dc215-146">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="dc215-147">14</span><span class="sxs-lookup"><span data-stu-id="dc215-147">14</span></span>

<span data-ttu-id="dc215-148">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="dc215-148">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="dc215-149">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="dc215-149">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="dc215-150">15</span><span class="sxs-lookup"><span data-stu-id="dc215-150">15</span></span>

<span data-ttu-id="dc215-151">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="dc215-151">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="dc215-152">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="dc215-152">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="dc215-153">16</span><span class="sxs-lookup"><span data-stu-id="dc215-153">16</span></span>

<span data-ttu-id="dc215-154">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="dc215-154">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="dc215-155">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="dc215-155">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="dc215-156">17</span><span class="sxs-lookup"><span data-stu-id="dc215-156">17</span></span>

<span data-ttu-id="dc215-157">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="dc215-157">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="dc215-158">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="dc215-158">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="dc215-159">21</span><span class="sxs-lookup"><span data-stu-id="dc215-159">21</span></span>

<span data-ttu-id="dc215-160">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="dc215-160">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dc215-161">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc215-161">Remarks</span></span>

<span data-ttu-id="dc215-162">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="dc215-162">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="dc215-163">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="dc215-163">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="dc215-164">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="dc215-164">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="dc215-165">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="dc215-165">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc215-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc215-166">Requirements</span></span>



| <span data-ttu-id="dc215-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc215-167">Requirement</span></span> | <span data-ttu-id="dc215-168">Value</span><span class="sxs-lookup"><span data-stu-id="dc215-168">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc215-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc215-169">Minimum supported client</span></span><br/> | <span data-ttu-id="dc215-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="dc215-170">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="dc215-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc215-171">Minimum supported server</span></span><br/> | <span data-ttu-id="dc215-172">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="dc215-172">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="dc215-173">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="dc215-173">Namespace</span></span><br/>                | <span data-ttu-id="dc215-174">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="dc215-174">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="dc215-175">MOF</span><span class="sxs-lookup"><span data-stu-id="dc215-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="dc215-176"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="dc215-176"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="dc215-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="dc215-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc215-178"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc215-178"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc215-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc215-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc215-180">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="dc215-180">CIM\_LogicalFile</span></span>](deleteex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="dc215-181">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="dc215-181">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

