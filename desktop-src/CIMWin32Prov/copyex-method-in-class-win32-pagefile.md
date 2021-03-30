---
description: Copia el archivo de paginación lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro FileName. Este método es una versión extendida del método de copia.
ms.assetid: a8376dc8-eb73-4097-b84c-839432ac3a25
ms.tgt_platform: multiple
title: Método CopyEx de la clase Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 810f1d3bcf878d33756930f6bd3b6799c3513dc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907543"
---
# <a name="copyex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="aad22-104">Método CopyEx de la clase de archivo de \_ paginación Win32</span><span class="sxs-lookup"><span data-stu-id="aad22-104">CopyEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="aad22-105">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CopyEx** copia el archivo de paginación lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="aad22-105">The **CopyEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical paging file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="aad22-106">Este método es una versión extendida del método de [**copia**](copy-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="aad22-106">This method is an extended version of the [**Copy**](copy-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="aad22-107">No se admite una copia si se requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="aad22-107">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="aad22-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="aad22-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="aad22-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="aad22-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="aad22-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="aad22-110">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="aad22-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="aad22-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aad22-112">*Nombre de archivo* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="aad22-112">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aad22-113">Nombre completo de la copia del archivo (o directorio).</span><span class="sxs-lookup"><span data-stu-id="aad22-113">Fully qualified name of the copy of the file (or directory).</span></span>

<span data-ttu-id="aad22-114">Ejemplo: c: \\ temp \\ newdirectory</span><span class="sxs-lookup"><span data-stu-id="aad22-114">Example: c:\\temp\\newdirectory</span></span>

</dd> <dt>

<span data-ttu-id="aad22-115">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="aad22-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aad22-116">Nombre del archivo o directorio en el que se produjo un error en el método **CopyEx** .</span><span class="sxs-lookup"><span data-stu-id="aad22-116">Name of the file or directory where the **CopyEx** method failed.</span></span> <span data-ttu-id="aad22-117">Este parámetro es **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="aad22-117">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="aad22-118">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="aad22-118">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aad22-119">Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **CopyEx**.</span><span class="sxs-lookup"><span data-stu-id="aad22-119">Names the child file or directory to use as a starting point for **CopyEx**.</span></span> <span data-ttu-id="aad22-120">El parámetro *StartFileName* es normalmente el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="aad22-120">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="aad22-121">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="aad22-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="aad22-122">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="aad22-122">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="aad22-123">Si **es true**, el cambio de propiedad se aplicará de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="aad22-123">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="aad22-124">En el caso de las instancias de archivo, se omite el parámetro *Recursive* .</span><span class="sxs-lookup"><span data-stu-id="aad22-124">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aad22-125">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="aad22-125">Return value</span></span>

<span data-ttu-id="aad22-126">Devuelve un valor de 0 (cero) si el archivo se ha copiado correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="aad22-126">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="aad22-127">**0**</span><span class="sxs-lookup"><span data-stu-id="aad22-127">**0**</span></span>
</dt> <dd>

<span data-ttu-id="aad22-128">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="aad22-128">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="aad22-129">**2**</span><span class="sxs-lookup"><span data-stu-id="aad22-129">**2**</span></span>
</dt> <dd>

<span data-ttu-id="aad22-130">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="aad22-130">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="aad22-131">**8**</span><span class="sxs-lookup"><span data-stu-id="aad22-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="aad22-132">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="aad22-132">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="aad22-133">**9**</span><span class="sxs-lookup"><span data-stu-id="aad22-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="aad22-134">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="aad22-134">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="aad22-135">**10**</span><span class="sxs-lookup"><span data-stu-id="aad22-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="aad22-136">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="aad22-136">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="aad22-137">**11**</span><span class="sxs-lookup"><span data-stu-id="aad22-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="aad22-138">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="aad22-138">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="aad22-139">**12**</span><span class="sxs-lookup"><span data-stu-id="aad22-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="aad22-140">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="aad22-140">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="aad22-141">**13**</span><span class="sxs-lookup"><span data-stu-id="aad22-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="aad22-142">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="aad22-142">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="aad22-143">**14**</span><span class="sxs-lookup"><span data-stu-id="aad22-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="aad22-144">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="aad22-144">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="aad22-145">**15**</span><span class="sxs-lookup"><span data-stu-id="aad22-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="aad22-146">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="aad22-146">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="aad22-147">**16**</span><span class="sxs-lookup"><span data-stu-id="aad22-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="aad22-148">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="aad22-148">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="aad22-149">**17**</span><span class="sxs-lookup"><span data-stu-id="aad22-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="aad22-150">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="aad22-150">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="aad22-151">**21**</span><span class="sxs-lookup"><span data-stu-id="aad22-151">**21**</span></span>
</dt> <dd>

<span data-ttu-id="aad22-152">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="aad22-152">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aad22-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aad22-153">Requirements</span></span>



| <span data-ttu-id="aad22-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="aad22-154">Requirement</span></span> | <span data-ttu-id="aad22-155">Value</span><span class="sxs-lookup"><span data-stu-id="aad22-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aad22-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aad22-156">Minimum supported client</span></span><br/> | <span data-ttu-id="aad22-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aad22-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aad22-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aad22-158">Minimum supported server</span></span><br/> | <span data-ttu-id="aad22-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aad22-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aad22-160">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="aad22-160">Namespace</span></span><br/>                | <span data-ttu-id="aad22-161">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="aad22-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aad22-162">MOF</span><span class="sxs-lookup"><span data-stu-id="aad22-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aad22-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aad22-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aad22-164">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="aad22-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aad22-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aad22-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aad22-166">Vea también</span><span class="sxs-lookup"><span data-stu-id="aad22-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="aad22-167">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aad22-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="aad22-168">**Archivo de \_ paginación Win32**</span><span class="sxs-lookup"><span data-stu-id="aad22-168">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

