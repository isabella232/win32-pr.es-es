---
description: Obtiene la propiedad del archivo de códec lógico especificado en la ruta de acceso del objeto. Este método es una versión extendida del método TakeOwnerShip.
ms.assetid: 8f3b495a-f654-4818-b0ea-dc88819d72af
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx de la clase Win32_CodecFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_CodecFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36512d48fe724da42c39c0d3d0686a706f54472d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906980"
---
# <a name="takeownershipex-method-of-the-win32_codecfile-class"></a><span data-ttu-id="eb83b-104">Método TakeOwnerShipEx de la \_ clase CodecFile de Win32</span><span class="sxs-lookup"><span data-stu-id="eb83b-104">TakeOwnerShipEx method of the Win32\_CodecFile class</span></span>

<span data-ttu-id="eb83b-105">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** obtiene la propiedad del archivo de códec lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="eb83b-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical codec file specified in the object path.</span></span> <span data-ttu-id="eb83b-106">Este método es una versión extendida del método [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="eb83b-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="eb83b-107">Si el archivo lógico es realmente un directorio, este método actúa de forma recursiva y toma la propiedad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="eb83b-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="eb83b-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="eb83b-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="eb83b-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="eb83b-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="eb83b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="eb83b-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="eb83b-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb83b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb83b-112">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="eb83b-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-113">Nombre del archivo o directorio en el que se produjo un error en el método **TakeOwnerShipEx** .</span><span class="sxs-lookup"><span data-stu-id="eb83b-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="eb83b-114">Este parámetro será **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="eb83b-114">This parameter will be **NULL** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="eb83b-115">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="eb83b-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-116">Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **TakeOwnerShipEx**. El parámetro *StartFileName* es normalmente el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="eb83b-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="eb83b-117">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="eb83b-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="eb83b-118">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="eb83b-118">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-119">Si **es true**, el cambio de propiedad se aplicará de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="eb83b-119">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span> <span data-ttu-id="eb83b-120">Nota: para las instancias de archivo, se omite el parámetro de entrada *recursivo* .</span><span class="sxs-lookup"><span data-stu-id="eb83b-120">Note: for file instances, the *Recursive* input parameter is ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb83b-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb83b-121">Return value</span></span>

<span data-ttu-id="eb83b-122">Devuelve un valor entero de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="eb83b-122">Returns an integer value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="eb83b-123">**0**</span><span class="sxs-lookup"><span data-stu-id="eb83b-123">**0**</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-124">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="eb83b-124">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="eb83b-125">**2**</span><span class="sxs-lookup"><span data-stu-id="eb83b-125">**2**</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-126">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="eb83b-126">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="eb83b-127">**8**</span><span class="sxs-lookup"><span data-stu-id="eb83b-127">**8**</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-128">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="eb83b-128">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="eb83b-129">**9**</span><span class="sxs-lookup"><span data-stu-id="eb83b-129">**9**</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-130">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="eb83b-130">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="eb83b-131">**10**</span><span class="sxs-lookup"><span data-stu-id="eb83b-131">**10**</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-132">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="eb83b-132">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="eb83b-133">**11**</span><span class="sxs-lookup"><span data-stu-id="eb83b-133">**11**</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-134">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="eb83b-134">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="eb83b-135">**12**</span><span class="sxs-lookup"><span data-stu-id="eb83b-135">**12**</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-136">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="eb83b-136">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="eb83b-137">**13**</span><span class="sxs-lookup"><span data-stu-id="eb83b-137">**13**</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-138">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="eb83b-138">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="eb83b-139">**14**</span><span class="sxs-lookup"><span data-stu-id="eb83b-139">**14**</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-140">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="eb83b-140">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="eb83b-141">**15**</span><span class="sxs-lookup"><span data-stu-id="eb83b-141">**15**</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-142">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="eb83b-142">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="eb83b-143">**16**</span><span class="sxs-lookup"><span data-stu-id="eb83b-143">**16**</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-144">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="eb83b-144">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="eb83b-145">**17**</span><span class="sxs-lookup"><span data-stu-id="eb83b-145">**17**</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-146">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="eb83b-146">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="eb83b-147">**21**</span><span class="sxs-lookup"><span data-stu-id="eb83b-147">**21**</span></span>
</dt> <dd>

<span data-ttu-id="eb83b-148">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="eb83b-148">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eb83b-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb83b-149">Requirements</span></span>



| <span data-ttu-id="eb83b-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb83b-150">Requirement</span></span> | <span data-ttu-id="eb83b-151">Value</span><span class="sxs-lookup"><span data-stu-id="eb83b-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="eb83b-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb83b-152">Minimum supported client</span></span><br/> | <span data-ttu-id="eb83b-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="eb83b-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="eb83b-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="eb83b-154">Minimum supported server</span></span><br/> | <span data-ttu-id="eb83b-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="eb83b-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="eb83b-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="eb83b-156">Namespace</span></span><br/>                | <span data-ttu-id="eb83b-157">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="eb83b-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="eb83b-158">MOF</span><span class="sxs-lookup"><span data-stu-id="eb83b-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="eb83b-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="eb83b-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="eb83b-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="eb83b-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eb83b-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eb83b-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb83b-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb83b-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="eb83b-163">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="eb83b-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="eb83b-164">**Win32 \_ CodecFile**</span><span class="sxs-lookup"><span data-stu-id="eb83b-164">**Win32\_CodecFile**</span></span>](win32-codecfile.md)
</dt> </dl>

 

