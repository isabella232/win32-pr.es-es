---
description: Obtiene la propiedad del archivo de acceso directo lógico especificado en la ruta de acceso del objeto. Este método es una versión extendida del método TakeOwnerShip.
ms.assetid: 1345562c-343e-4e3a-b6ed-3b64a7260c89
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx de la clase Win32_ShortcutFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ShortcutFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 69988c7995ee295297c92bbabf0ee83059304a94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659358"
---
# <a name="takeownershipex-method-of-the-win32_shortcutfile-class"></a><span data-ttu-id="516c9-104">Método TakeOwnerShipEx de la \_ clase ShortcutFile de Win32</span><span class="sxs-lookup"><span data-stu-id="516c9-104">TakeOwnerShipEx method of the Win32\_ShortcutFile class</span></span>

<span data-ttu-id="516c9-105">El método de [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** obtiene la propiedad del archivo de acceso directo lógico especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="516c9-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical shortcut file specified in the object path.</span></span> <span data-ttu-id="516c9-106">Este método es una versión extendida del método [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="516c9-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="516c9-107">Si el archivo lógico es realmente un directorio, este método actúa de forma recursiva y toma la propiedad de todos los archivos y subdirectorios que contiene el directorio.</span><span class="sxs-lookup"><span data-stu-id="516c9-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="516c9-108">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="516c9-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="516c9-109">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="516c9-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="516c9-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="516c9-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="516c9-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="516c9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="516c9-112">*StopFileName* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="516c9-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="516c9-113">Nombre del archivo o directorio en el que se produjo un error en el método **TakeOwnerShipEx** .</span><span class="sxs-lookup"><span data-stu-id="516c9-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="516c9-114">Este parámetro será **null** si el método se ejecuta correctamente.</span><span class="sxs-lookup"><span data-stu-id="516c9-114">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="516c9-115">*StartFileName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="516c9-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="516c9-116">Asigna un nombre al archivo o directorio secundario que se va a usar como punto de partida para **TakeOwnerShipEx**.</span><span class="sxs-lookup"><span data-stu-id="516c9-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.</span></span> <span data-ttu-id="516c9-117">El parámetro *StartFileName* es normalmente el parámetro *StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior.</span><span class="sxs-lookup"><span data-stu-id="516c9-117">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="516c9-118">Si este parámetro es **null**, la operación se realiza en el archivo o directorio especificado en la llamada ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="516c9-118">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="516c9-119">*Recursivo* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="516c9-119">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="516c9-120">Si **es true**, el cambio de propiedad se aplicará de forma recursiva a los archivos y directorios del directorio especificado por la instancia de [**\_ LogicalFile de CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="516c9-120">If **true**, the change of ownership will be applied recursively to files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="516c9-121">En el caso de las instancias de archivo, se omite el parámetro *Recursive* .</span><span class="sxs-lookup"><span data-stu-id="516c9-121">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="516c9-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="516c9-122">Return value</span></span>

<span data-ttu-id="516c9-123">Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="516c9-123">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="516c9-124">**0**</span><span class="sxs-lookup"><span data-stu-id="516c9-124">**0**</span></span>
</dt> <dd>

<span data-ttu-id="516c9-125">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="516c9-125">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="516c9-126">**2**</span><span class="sxs-lookup"><span data-stu-id="516c9-126">**2**</span></span>
</dt> <dd>

<span data-ttu-id="516c9-127">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="516c9-127">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="516c9-128">**8**</span><span class="sxs-lookup"><span data-stu-id="516c9-128">**8**</span></span>
</dt> <dd>

<span data-ttu-id="516c9-129">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="516c9-129">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="516c9-130">**9**</span><span class="sxs-lookup"><span data-stu-id="516c9-130">**9**</span></span>
</dt> <dd>

<span data-ttu-id="516c9-131">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="516c9-131">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="516c9-132">**10**</span><span class="sxs-lookup"><span data-stu-id="516c9-132">**10**</span></span>
</dt> <dd>

<span data-ttu-id="516c9-133">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="516c9-133">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="516c9-134">**11**</span><span class="sxs-lookup"><span data-stu-id="516c9-134">**11**</span></span>
</dt> <dd>

<span data-ttu-id="516c9-135">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="516c9-135">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="516c9-136">**12**</span><span class="sxs-lookup"><span data-stu-id="516c9-136">**12**</span></span>
</dt> <dd>

<span data-ttu-id="516c9-137">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="516c9-137">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="516c9-138">**13**</span><span class="sxs-lookup"><span data-stu-id="516c9-138">**13**</span></span>
</dt> <dd>

<span data-ttu-id="516c9-139">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="516c9-139">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="516c9-140">**14**</span><span class="sxs-lookup"><span data-stu-id="516c9-140">**14**</span></span>
</dt> <dd>

<span data-ttu-id="516c9-141">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="516c9-141">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="516c9-142">**15**</span><span class="sxs-lookup"><span data-stu-id="516c9-142">**15**</span></span>
</dt> <dd>

<span data-ttu-id="516c9-143">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="516c9-143">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="516c9-144">**16**</span><span class="sxs-lookup"><span data-stu-id="516c9-144">**16**</span></span>
</dt> <dd>

<span data-ttu-id="516c9-145">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="516c9-145">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="516c9-146">**17**</span><span class="sxs-lookup"><span data-stu-id="516c9-146">**17**</span></span>
</dt> <dd>

<span data-ttu-id="516c9-147">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="516c9-147">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="516c9-148">**21**</span><span class="sxs-lookup"><span data-stu-id="516c9-148">**21**</span></span>
</dt> <dd>

<span data-ttu-id="516c9-149">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="516c9-149">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="516c9-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="516c9-150">Requirements</span></span>



| <span data-ttu-id="516c9-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="516c9-151">Requirement</span></span> | <span data-ttu-id="516c9-152">Value</span><span class="sxs-lookup"><span data-stu-id="516c9-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="516c9-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="516c9-153">Minimum supported client</span></span><br/> | <span data-ttu-id="516c9-154">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="516c9-154">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="516c9-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="516c9-155">Minimum supported server</span></span><br/> | <span data-ttu-id="516c9-156">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="516c9-156">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="516c9-157">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="516c9-157">Namespace</span></span><br/>                | <span data-ttu-id="516c9-158">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="516c9-158">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="516c9-159">MOF</span><span class="sxs-lookup"><span data-stu-id="516c9-159">MOF</span></span><br/>                      | <dl> <span data-ttu-id="516c9-160"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="516c9-160"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="516c9-161">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="516c9-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="516c9-162"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="516c9-162"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="516c9-163">Vea también</span><span class="sxs-lookup"><span data-stu-id="516c9-163">See also</span></span>

<dl> <dt>

<span data-ttu-id="516c9-164">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="516c9-164">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="516c9-165">**Win32 \_ ShortcutFile**</span><span class="sxs-lookup"><span data-stu-id="516c9-165">**Win32\_ShortcutFile**</span></span>](win32-shortcutfile.md)
</dt> </dl>

 

