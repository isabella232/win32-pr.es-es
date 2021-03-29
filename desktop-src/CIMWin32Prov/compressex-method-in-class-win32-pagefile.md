---
description: Comprime el archivo de paginación lógica (o directorio) especificado en la ruta de acceso del objeto (este método es una versión extendida del método Compress).
ms.assetid: ea99367b-4d5e-4cd2-aa89-d250d1161f8f
ms.tgt_platform: multiple
title: Método CompressEx de la clase Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2823d12fc474b5a5023890596a116062d94a045f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907022"
---
# <a name="compressex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="716ad-103">Método CompressEx de la clase de archivo de \_ paginación Win32</span><span class="sxs-lookup"><span data-stu-id="716ad-103">CompressEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="716ad-104">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CompressEx** comprime el archivo de paginación lógico (o directorio) especificado en la ruta de acceso del objeto (este método es una versión extendida del método [**compress**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="716ad-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical paging file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="716ad-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="716ad-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="716ad-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="716ad-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="716ad-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="716ad-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="716ad-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="716ad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="716ad-109">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="716ad-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="716ad-110">Nombre del archivo o directorio en el que se produjo un error en el método **CompressEx** .</span><span class="sxs-lookup"><span data-stu-id="716ad-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="716ad-111">Este parámetro es **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="716ad-111">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="716ad-112">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="716ad-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="716ad-113">Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **CompressEx**.</span><span class="sxs-lookup"><span data-stu-id="716ad-113">Names the child file or directory to use as a starting point for **CompressEx**.</span></span> <span data-ttu-id="716ad-114">El parámetro *StartFileName* es normalmente el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="716ad-114">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="716ad-115">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="716ad-115">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="716ad-116">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="716ad-116">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="716ad-117">Si **es true**, el cambio de propiedad se aplicará de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="716ad-117">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="716ad-118">En el caso de las instancias de archivo, se omite el parámetro *Recursive* .</span><span class="sxs-lookup"><span data-stu-id="716ad-118">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="716ad-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="716ad-119">Return value</span></span>

<span data-ttu-id="716ad-120">Devuelve un valor de 0 (cero) si el archivo se ha comprimido correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="716ad-120">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="716ad-121">**0**</span><span class="sxs-lookup"><span data-stu-id="716ad-121">**0**</span></span>
</dt> <dd>

<span data-ttu-id="716ad-122">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="716ad-122">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="716ad-123">**2**</span><span class="sxs-lookup"><span data-stu-id="716ad-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="716ad-124">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="716ad-124">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="716ad-125">**8**</span><span class="sxs-lookup"><span data-stu-id="716ad-125">**8**</span></span>
</dt> <dd>

<span data-ttu-id="716ad-126">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="716ad-126">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="716ad-127">**9**</span><span class="sxs-lookup"><span data-stu-id="716ad-127">**9**</span></span>
</dt> <dd>

<span data-ttu-id="716ad-128">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="716ad-128">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="716ad-129">**10**</span><span class="sxs-lookup"><span data-stu-id="716ad-129">**10**</span></span>
</dt> <dd>

<span data-ttu-id="716ad-130">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="716ad-130">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="716ad-131">**11**</span><span class="sxs-lookup"><span data-stu-id="716ad-131">**11**</span></span>
</dt> <dd>

<span data-ttu-id="716ad-132">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="716ad-132">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="716ad-133">**12**</span><span class="sxs-lookup"><span data-stu-id="716ad-133">**12**</span></span>
</dt> <dd>

<span data-ttu-id="716ad-134">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="716ad-134">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="716ad-135">**13**</span><span class="sxs-lookup"><span data-stu-id="716ad-135">**13**</span></span>
</dt> <dd>

<span data-ttu-id="716ad-136">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="716ad-136">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="716ad-137">**14**</span><span class="sxs-lookup"><span data-stu-id="716ad-137">**14**</span></span>
</dt> <dd>

<span data-ttu-id="716ad-138">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="716ad-138">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="716ad-139">**15**</span><span class="sxs-lookup"><span data-stu-id="716ad-139">**15**</span></span>
</dt> <dd>

<span data-ttu-id="716ad-140">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="716ad-140">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="716ad-141">**16**</span><span class="sxs-lookup"><span data-stu-id="716ad-141">**16**</span></span>
</dt> <dd>

<span data-ttu-id="716ad-142">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="716ad-142">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="716ad-143">**17**</span><span class="sxs-lookup"><span data-stu-id="716ad-143">**17**</span></span>
</dt> <dd>

<span data-ttu-id="716ad-144">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="716ad-144">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="716ad-145">**21**</span><span class="sxs-lookup"><span data-stu-id="716ad-145">**21**</span></span>
</dt> <dd>

<span data-ttu-id="716ad-146">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="716ad-146">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="716ad-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="716ad-147">Requirements</span></span>



| <span data-ttu-id="716ad-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="716ad-148">Requirement</span></span> | <span data-ttu-id="716ad-149">Value</span><span class="sxs-lookup"><span data-stu-id="716ad-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="716ad-150">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="716ad-150">Minimum supported client</span></span><br/> | <span data-ttu-id="716ad-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="716ad-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="716ad-152">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="716ad-152">Minimum supported server</span></span><br/> | <span data-ttu-id="716ad-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="716ad-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="716ad-154">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="716ad-154">Namespace</span></span><br/>                | <span data-ttu-id="716ad-155">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="716ad-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="716ad-156">MOF</span><span class="sxs-lookup"><span data-stu-id="716ad-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="716ad-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="716ad-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="716ad-158">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="716ad-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="716ad-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="716ad-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="716ad-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="716ad-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="716ad-161">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="716ad-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="716ad-162">**Archivo de \_ paginación Win32**</span><span class="sxs-lookup"><span data-stu-id="716ad-162">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

