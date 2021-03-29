---
description: El método CompressEx comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del método compress.
ms.assetid: 7d119865-c246-4cb5-9de4-48a4c42efd90
ms.tgt_platform: multiple
title: Método CompressEx de la clase CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7570cbe3ebc00708023a18da42ef35ff3306d3b0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907024"
---
# <a name="compressex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="10aa4-104">Método CompressEx de la \_ clase LogicalFile de CIM</span><span class="sxs-lookup"><span data-stu-id="10aa4-104">CompressEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="10aa4-105">El método **CompressEx** comprime el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="10aa4-105">The **CompressEx** method compresses the logical file (or directory) specified in the object path.</span></span> <span data-ttu-id="10aa4-106">Este método es una versión extendida del método [**compress**](compress-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="10aa4-106">This method is an extended version of the [**Compress**](compress-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10aa4-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="10aa4-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="10aa4-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="10aa4-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="10aa4-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="10aa4-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="10aa4-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="10aa4-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="10aa4-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10aa4-111">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="10aa4-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="10aa4-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10aa4-113">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="10aa4-113">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-114">Nombre del archivo (o directorio) en el que se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="10aa4-114">Name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="10aa4-115">Este parámetro es NULL si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="10aa4-115">This parameter is null if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="10aa4-116">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="10aa4-116">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-117">Archivo secundario (o directorio) que se va a usar como punto de partida para el método.</span><span class="sxs-lookup"><span data-stu-id="10aa4-117">Child file (or directory) to use as a starting point for the method.</span></span> <span data-ttu-id="10aa4-118">Normalmente, este parámetro es el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="10aa4-118">Typically, this parameter is the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="10aa4-119">Si este parámetro es null, la operación se realiza en el archivo (o directorio) especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="10aa4-119">If this parameter is null, the operation is performed on the file (or directory) specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="10aa4-120">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="10aa4-120">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-121">Si es **true**, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="10aa4-121">If **TRUE**, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="10aa4-122">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="10aa4-122">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10aa4-123">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="10aa4-123">Return value</span></span>

<span data-ttu-id="10aa4-124">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="10aa4-124">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="10aa4-125">**Success**</span><span class="sxs-lookup"><span data-stu-id="10aa4-125">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-126">0</span><span class="sxs-lookup"><span data-stu-id="10aa4-126">0</span></span>

<span data-ttu-id="10aa4-127">Correcto.</span><span class="sxs-lookup"><span data-stu-id="10aa4-127">Success.</span></span>

</dd> <dt>

<span data-ttu-id="10aa4-128">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="10aa4-128">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-129">2</span><span class="sxs-lookup"><span data-stu-id="10aa4-129">2</span></span>

<span data-ttu-id="10aa4-130">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="10aa4-130">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="10aa4-131">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="10aa4-131">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-132">8</span><span class="sxs-lookup"><span data-stu-id="10aa4-132">8</span></span>

<span data-ttu-id="10aa4-133">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="10aa4-133">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="10aa4-134">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="10aa4-134">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-135">9</span><span class="sxs-lookup"><span data-stu-id="10aa4-135">9</span></span>

<span data-ttu-id="10aa4-136">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="10aa4-136">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="10aa4-137">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="10aa4-137">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-138">10</span><span class="sxs-lookup"><span data-stu-id="10aa4-138">10</span></span>

<span data-ttu-id="10aa4-139">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="10aa4-139">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="10aa4-140">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="10aa4-140">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-141">11</span><span class="sxs-lookup"><span data-stu-id="10aa4-141">11</span></span>

<span data-ttu-id="10aa4-142">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="10aa4-142">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="10aa4-143">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="10aa4-143">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-144">12</span><span class="sxs-lookup"><span data-stu-id="10aa4-144">12</span></span>

<span data-ttu-id="10aa4-145">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="10aa4-145">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="10aa4-146">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="10aa4-146">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-147">13</span><span class="sxs-lookup"><span data-stu-id="10aa4-147">13</span></span>

<span data-ttu-id="10aa4-148">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="10aa4-148">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="10aa4-149">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="10aa4-149">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-150">14</span><span class="sxs-lookup"><span data-stu-id="10aa4-150">14</span></span>

<span data-ttu-id="10aa4-151">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="10aa4-151">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="10aa4-152">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="10aa4-152">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-153">15</span><span class="sxs-lookup"><span data-stu-id="10aa4-153">15</span></span>

<span data-ttu-id="10aa4-154">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="10aa4-154">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="10aa4-155">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="10aa4-155">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-156">16</span><span class="sxs-lookup"><span data-stu-id="10aa4-156">16</span></span>

<span data-ttu-id="10aa4-157">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="10aa4-157">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="10aa4-158">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="10aa4-158">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-159">17</span><span class="sxs-lookup"><span data-stu-id="10aa4-159">17</span></span>

<span data-ttu-id="10aa4-160">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="10aa4-160">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="10aa4-161">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="10aa4-161">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="10aa4-162">21</span><span class="sxs-lookup"><span data-stu-id="10aa4-162">21</span></span>

<span data-ttu-id="10aa4-163">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="10aa4-163">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="10aa4-164">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10aa4-164">Remarks</span></span>

<span data-ttu-id="10aa4-165">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="10aa4-165">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="10aa4-166">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="10aa4-166">To use this method, you must implement it in your own provider.</span></span>

## <a name="requirements"></a><span data-ttu-id="10aa4-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10aa4-167">Requirements</span></span>



| <span data-ttu-id="10aa4-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="10aa4-168">Requirement</span></span> | <span data-ttu-id="10aa4-169">Value</span><span class="sxs-lookup"><span data-stu-id="10aa4-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10aa4-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10aa4-170">Minimum supported client</span></span><br/> | <span data-ttu-id="10aa4-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10aa4-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10aa4-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="10aa4-172">Minimum supported server</span></span><br/> | <span data-ttu-id="10aa4-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10aa4-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10aa4-174">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="10aa4-174">Namespace</span></span><br/>                | <span data-ttu-id="10aa4-175">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="10aa4-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="10aa4-176">MOF</span><span class="sxs-lookup"><span data-stu-id="10aa4-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10aa4-177"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="10aa4-177"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="10aa4-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="10aa4-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10aa4-179"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10aa4-179"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10aa4-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="10aa4-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10aa4-181">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="10aa4-181">CIM\_LogicalFile</span></span>](compressex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="10aa4-182">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="10aa4-182">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

