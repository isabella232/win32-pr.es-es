---
description: Obtiene la propiedad del archivo de paginación lógico especificado en la ruta de acceso del objeto. Este método es una versión extendida del método TakeOwnerShip.
ms.assetid: 6c359910-713a-441e-b2e1-949929c07e93
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx de la clase Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b0f4662b4884da227a64768cc29bce4c615f8f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104274837"
---
# <a name="takeownershipex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="1a738-104">Método TakeOwnerShipEx de la clase de archivo de \_ paginación Win32</span><span class="sxs-lookup"><span data-stu-id="1a738-104">TakeOwnerShipEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="1a738-105">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** obtiene la propiedad del archivo de paginación lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="1a738-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical paging file specified in the object path.</span></span> <span data-ttu-id="1a738-106">Este método es una versión extendida del método [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="1a738-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="1a738-107">Si el archivo lógico es realmente un directorio, este método actúa de forma recursiva y toma la propiedad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="1a738-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="1a738-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="1a738-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="1a738-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="1a738-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="1a738-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a738-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="1a738-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a738-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a738-112">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1a738-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1a738-113">Nombre del archivo o directorio en el que se produjo un error en el método **TakeOwnerShipEx** .</span><span class="sxs-lookup"><span data-stu-id="1a738-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="1a738-114">Este parámetro será **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="1a738-114">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="1a738-115">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1a738-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1a738-116">Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **TakeOwnerShipEx**. El parámetro *StartFileName* es normalmente el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="1a738-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="1a738-117">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="1a738-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="1a738-118">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="1a738-118">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="1a738-119">Si **es true**, el cambio de propiedad se aplicará de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="1a738-119">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="1a738-120">En el caso de las instancias de archivo, se omite el parámetro *Recursive* .</span><span class="sxs-lookup"><span data-stu-id="1a738-120">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a738-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a738-121">Return value</span></span>

<span data-ttu-id="1a738-122">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="1a738-122">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="1a738-123">**0**</span><span class="sxs-lookup"><span data-stu-id="1a738-123">**0**</span></span>
</dt> <dd>

<span data-ttu-id="1a738-124">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="1a738-124">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="1a738-125">**2**</span><span class="sxs-lookup"><span data-stu-id="1a738-125">**2**</span></span>
</dt> <dd>

<span data-ttu-id="1a738-126">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="1a738-126">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="1a738-127">**8**</span><span class="sxs-lookup"><span data-stu-id="1a738-127">**8**</span></span>
</dt> <dd>

<span data-ttu-id="1a738-128">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="1a738-128">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="1a738-129">**9**</span><span class="sxs-lookup"><span data-stu-id="1a738-129">**9**</span></span>
</dt> <dd>

<span data-ttu-id="1a738-130">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="1a738-130">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1a738-131">**10**</span><span class="sxs-lookup"><span data-stu-id="1a738-131">**10**</span></span>
</dt> <dd>

<span data-ttu-id="1a738-132">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="1a738-132">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="1a738-133">**11**</span><span class="sxs-lookup"><span data-stu-id="1a738-133">**11**</span></span>
</dt> <dd>

<span data-ttu-id="1a738-134">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="1a738-134">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="1a738-135">**12**</span><span class="sxs-lookup"><span data-stu-id="1a738-135">**12**</span></span>
</dt> <dd>

<span data-ttu-id="1a738-136">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="1a738-136">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="1a738-137">**13**</span><span class="sxs-lookup"><span data-stu-id="1a738-137">**13**</span></span>
</dt> <dd>

<span data-ttu-id="1a738-138">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="1a738-138">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="1a738-139">**14**</span><span class="sxs-lookup"><span data-stu-id="1a738-139">**14**</span></span>
</dt> <dd>

<span data-ttu-id="1a738-140">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="1a738-140">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="1a738-141">**15**</span><span class="sxs-lookup"><span data-stu-id="1a738-141">**15**</span></span>
</dt> <dd>

<span data-ttu-id="1a738-142">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="1a738-142">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="1a738-143">**16**</span><span class="sxs-lookup"><span data-stu-id="1a738-143">**16**</span></span>
</dt> <dd>

<span data-ttu-id="1a738-144">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="1a738-144">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="1a738-145">**17**</span><span class="sxs-lookup"><span data-stu-id="1a738-145">**17**</span></span>
</dt> <dd>

<span data-ttu-id="1a738-146">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="1a738-146">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="1a738-147">**21**</span><span class="sxs-lookup"><span data-stu-id="1a738-147">**21**</span></span>
</dt> <dd>

<span data-ttu-id="1a738-148">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="1a738-148">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1a738-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a738-149">Requirements</span></span>



| <span data-ttu-id="1a738-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a738-150">Requirement</span></span> | <span data-ttu-id="1a738-151">Value</span><span class="sxs-lookup"><span data-stu-id="1a738-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a738-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a738-152">Minimum supported client</span></span><br/> | <span data-ttu-id="1a738-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1a738-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1a738-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a738-154">Minimum supported server</span></span><br/> | <span data-ttu-id="1a738-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1a738-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1a738-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1a738-156">Namespace</span></span><br/>                | <span data-ttu-id="1a738-157">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1a738-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1a738-158">MOF</span><span class="sxs-lookup"><span data-stu-id="1a738-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1a738-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1a738-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1a738-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1a738-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a738-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a738-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a738-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a738-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a738-163">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1a738-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="1a738-164">**Archivo de \_ paginación Win32**</span><span class="sxs-lookup"><span data-stu-id="1a738-164">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

