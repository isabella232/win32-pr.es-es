---
description: Copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro FileName.
ms.assetid: 534d8b73-fc22-4a42-b8e6-24a54353bb14
ms.tgt_platform: multiple
title: Método CopyEx de la clase CIM_LogicalFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ec7c44ec3fc01074a0f4af70249236aa366d64bf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659767"
---
# <a name="copyex-method-of-the-cim_logicalfile-class"></a><span data-ttu-id="bef9e-103">Método CopyEx de la \_ clase LogicalFile de CIM</span><span class="sxs-lookup"><span data-stu-id="bef9e-103">CopyEx method of the CIM\_LogicalFile class</span></span>

<span data-ttu-id="bef9e-104">El método **CopyEx** copia el archivo lógico (o directorio) especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="bef9e-104">The **CopyEx** method copies the logical file (or directory) specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="bef9e-105">No se admite una copia si se requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="bef9e-105">A copy is not supported if overwriting an existing logical file is required.</span></span> <span data-ttu-id="bef9e-106">Este método es una versión extendida del método de [**copia**](copy-method-in-class-cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="bef9e-106">This method is an extended version of the [**Copy**](copy-method-in-class-cim-logicalfile.md) method.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="bef9e-107">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="bef9e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="bef9e-108">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="bef9e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="bef9e-109">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="bef9e-109">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="bef9e-110">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="bef9e-110">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="bef9e-111">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bef9e-111">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="bef9e-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="bef9e-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bef9e-113">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="bef9e-113">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-114">Nombre completo del archivo de destino (o directorio).</span><span class="sxs-lookup"><span data-stu-id="bef9e-114">Fully qualified name of the destination file (or directory).</span></span>

<span data-ttu-id="bef9e-115">Ejemplo: "c: \\ temp \\ newdirectory"</span><span class="sxs-lookup"><span data-stu-id="bef9e-115">Example: "c:\\temp\\newdirectory"</span></span>

</dd> <dt>

<span data-ttu-id="bef9e-116">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="bef9e-116">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-117">Cadena que representa el nombre del archivo (o directorio) donde se produjo un error en el método.</span><span class="sxs-lookup"><span data-stu-id="bef9e-117">String that represents the name of the file (or directory) where the method failed.</span></span> <span data-ttu-id="bef9e-118">Este parámetro es **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="bef9e-118">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="bef9e-119">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bef9e-119">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-120">Cadena que nombra el archivo secundario (o directorio) que se va a utilizar como punto de partida para este método.</span><span class="sxs-lookup"><span data-stu-id="bef9e-120">String that names the child file (or directory) to use as a starting point for this method.</span></span> <span data-ttu-id="bef9e-121">Normalmente, el parámetro *StartFileName* es el parámetro *StopFileName* que especifica el archivo (o directorio) en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="bef9e-121">Typically, the *StartFileName* parameter is the *StopFileName* parameter specifying the file (or directory) at which an error occurred from the previous method call.</span></span> <span data-ttu-id="bef9e-122">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) .</span><span class="sxs-lookup"><span data-stu-id="bef9e-122">If this parameter is **null**, the operation is performed on the file or directory specified in the [**ExecMethod**](/windows/desktop/WmiSdk/swbemservices-execmethod) call.</span></span>

</dd> <dt>

<span data-ttu-id="bef9e-123">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="bef9e-123">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-124">Si es TRUE, el método también se aplica de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="bef9e-124">If TRUE, the method is also applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="bef9e-125">En el caso de las instancias de archivo, este parámetro se omite.</span><span class="sxs-lookup"><span data-stu-id="bef9e-125">For file instances, this parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bef9e-126">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="bef9e-126">Return value</span></span>

<span data-ttu-id="bef9e-127">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="bef9e-127">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="bef9e-128">**Success**</span><span class="sxs-lookup"><span data-stu-id="bef9e-128">**Success**</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-129">0</span><span class="sxs-lookup"><span data-stu-id="bef9e-129">0</span></span>

<span data-ttu-id="bef9e-130">Correcto.</span><span class="sxs-lookup"><span data-stu-id="bef9e-130">Success.</span></span>

</dd> <dt>

<span data-ttu-id="bef9e-131">**Acceso denegado**</span><span class="sxs-lookup"><span data-stu-id="bef9e-131">**Access Denied**</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-132">2</span><span class="sxs-lookup"><span data-stu-id="bef9e-132">2</span></span>

<span data-ttu-id="bef9e-133">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="bef9e-133">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="bef9e-134">**Error no especificado**</span><span class="sxs-lookup"><span data-stu-id="bef9e-134">**Unspecified failure**</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-135">8</span><span class="sxs-lookup"><span data-stu-id="bef9e-135">8</span></span>

<span data-ttu-id="bef9e-136">Error no especificado.</span><span class="sxs-lookup"><span data-stu-id="bef9e-136">Unspecified failure.</span></span>

</dd> <dt>

<span data-ttu-id="bef9e-137">**Objeto no válido**</span><span class="sxs-lookup"><span data-stu-id="bef9e-137">**Invalid object**</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-138">9</span><span class="sxs-lookup"><span data-stu-id="bef9e-138">9</span></span>

<span data-ttu-id="bef9e-139">Objeto no válido.</span><span class="sxs-lookup"><span data-stu-id="bef9e-139">Invalid object.</span></span>

</dd> <dt>

<span data-ttu-id="bef9e-140">**El objeto ya existe**</span><span class="sxs-lookup"><span data-stu-id="bef9e-140">**Object already exists**</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-141">10</span><span class="sxs-lookup"><span data-stu-id="bef9e-141">10</span></span>

<span data-ttu-id="bef9e-142">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="bef9e-142">Object already exists.</span></span>

</dd> <dt>

<span data-ttu-id="bef9e-143">**Sistema de archivos no NTFS**</span><span class="sxs-lookup"><span data-stu-id="bef9e-143">**File system not NTFS**</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-144">11</span><span class="sxs-lookup"><span data-stu-id="bef9e-144">11</span></span>

<span data-ttu-id="bef9e-145">Sistema de archivos no NTFS.</span><span class="sxs-lookup"><span data-stu-id="bef9e-145">File system not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="bef9e-146">**Plataforma no NT/Windows 2000**</span><span class="sxs-lookup"><span data-stu-id="bef9e-146">**Platform not NT/Windows 2000**</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-147">12</span><span class="sxs-lookup"><span data-stu-id="bef9e-147">12</span></span>

<span data-ttu-id="bef9e-148">Plataforma no Windows.</span><span class="sxs-lookup"><span data-stu-id="bef9e-148">Platform not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="bef9e-149">**La unidad no es la misma**</span><span class="sxs-lookup"><span data-stu-id="bef9e-149">**Drive not the same**</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-150">13</span><span class="sxs-lookup"><span data-stu-id="bef9e-150">13</span></span>

<span data-ttu-id="bef9e-151">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="bef9e-151">Drive not the same.</span></span>

</dd> <dt>

<span data-ttu-id="bef9e-152">**El directorio no está vacío**</span><span class="sxs-lookup"><span data-stu-id="bef9e-152">**Directory not empty**</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-153">14</span><span class="sxs-lookup"><span data-stu-id="bef9e-153">14</span></span>

<span data-ttu-id="bef9e-154">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="bef9e-154">Directory not empty.</span></span>

</dd> <dt>

<span data-ttu-id="bef9e-155">**Infracción de uso compartido**</span><span class="sxs-lookup"><span data-stu-id="bef9e-155">**Sharing violation**</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-156">15</span><span class="sxs-lookup"><span data-stu-id="bef9e-156">15</span></span>

<span data-ttu-id="bef9e-157">Infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="bef9e-157">Sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="bef9e-158">**Archivo de inicio no válido**</span><span class="sxs-lookup"><span data-stu-id="bef9e-158">**Invalid start file**</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-159">16</span><span class="sxs-lookup"><span data-stu-id="bef9e-159">16</span></span>

<span data-ttu-id="bef9e-160">Archivo de inicio no válido.</span><span class="sxs-lookup"><span data-stu-id="bef9e-160">Invalid start file.</span></span>

</dd> <dt>

<span data-ttu-id="bef9e-161">**Privilegio no mantenido**</span><span class="sxs-lookup"><span data-stu-id="bef9e-161">**Privilege not held**</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-162">17</span><span class="sxs-lookup"><span data-stu-id="bef9e-162">17</span></span>

<span data-ttu-id="bef9e-163">Privilegio no mantenido.</span><span class="sxs-lookup"><span data-stu-id="bef9e-163">Privilege not held.</span></span>

</dd> <dt>

<span data-ttu-id="bef9e-164">**parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="bef9e-164">**Invalid parameter**</span></span>
</dt> <dd>

<span data-ttu-id="bef9e-165">21</span><span class="sxs-lookup"><span data-stu-id="bef9e-165">21</span></span>

<span data-ttu-id="bef9e-166">Parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="bef9e-166">Invalid parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bef9e-167">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bef9e-167">Remarks</span></span>

<span data-ttu-id="bef9e-168">Este método no está implementado actualmente por WMI.</span><span class="sxs-lookup"><span data-stu-id="bef9e-168">This method is currently not implemented by WMI.</span></span> <span data-ttu-id="bef9e-169">Para usar este método, debe implementarlo en su propio proveedor.</span><span class="sxs-lookup"><span data-stu-id="bef9e-169">To use this method, you must implement it in your own provider.</span></span>

<span data-ttu-id="bef9e-170">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="bef9e-170">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="bef9e-171">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="bef9e-171">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="bef9e-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bef9e-172">Requirements</span></span>



| <span data-ttu-id="bef9e-173">Requisito</span><span class="sxs-lookup"><span data-stu-id="bef9e-173">Requirement</span></span> | <span data-ttu-id="bef9e-174">Value</span><span class="sxs-lookup"><span data-stu-id="bef9e-174">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bef9e-175">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bef9e-175">Minimum supported client</span></span><br/> | <span data-ttu-id="bef9e-176">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bef9e-176">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bef9e-177">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bef9e-177">Minimum supported server</span></span><br/> | <span data-ttu-id="bef9e-178">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bef9e-178">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bef9e-179">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="bef9e-179">Namespace</span></span><br/>                | <span data-ttu-id="bef9e-180">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="bef9e-180">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="bef9e-181">MOF</span><span class="sxs-lookup"><span data-stu-id="bef9e-181">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bef9e-182"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="bef9e-182"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="bef9e-183">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="bef9e-183">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bef9e-184"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bef9e-184"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bef9e-185">Vea también</span><span class="sxs-lookup"><span data-stu-id="bef9e-185">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bef9e-186">\_LOGICALFILE CIM</span><span class="sxs-lookup"><span data-stu-id="bef9e-186">CIM\_LogicalFile</span></span>](copyex-method-in-class-cim-logicalfile.md)
</dt> <dt>

[<span data-ttu-id="bef9e-187">**\_LOGICALFILE CIM**</span><span class="sxs-lookup"><span data-stu-id="bef9e-187">**CIM\_LogicalFile**</span></span>](cim-logicalfile.md)
</dt> </dl>

 

