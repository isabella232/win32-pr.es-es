---
description: Cambia el nombre del archivo de entrada de directorio especificado en la ruta de acceso del objeto.
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Cambiar el nombre del método de la clase Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 874151e1ff8c9feca375df3eb441665863d1070d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659326"
---
# <a name="rename-method-of-the-win32_directory-class"></a><span data-ttu-id="5d0f2-103">Cambiar el nombre del método de la \_ clase de directorio Win32</span><span class="sxs-lookup"><span data-stu-id="5d0f2-103">Rename method of the Win32\_Directory class</span></span>

<span data-ttu-id="5d0f2-104">El método **Rename** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) cambia el nombre del archivo de entrada de directorio especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the directory entry file specified in the object path.</span></span> <span data-ttu-id="5d0f2-105">No se admite el cambio de nombre si el destino está en otra unidad o si se requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="5d0f2-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="5d0f2-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5d0f2-107">Para obtener más información sobre el uso de este método, vea [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5d0f2-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d0f2-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5d0f2-108">Syntax</span></span>


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="5d0f2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5d0f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d0f2-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="5d0f2-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="5d0f2-111">Nuevo nombre completo del archivo (o directorio).</span><span class="sxs-lookup"><span data-stu-id="5d0f2-111">Fully qualified new name of the file (or directory).</span></span> <span data-ttu-id="5d0f2-112">Ejemplo: c: \\ temp \\newfile.txt.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-112">Example: c:\\temp\\newfile.txt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d0f2-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5d0f2-113">Return value</span></span>

<span data-ttu-id="5d0f2-114">Devuelve un valor de 0 (cero) si se cambió el nombre del archivo correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-114">Returns a value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5d0f2-115">**0**</span><span class="sxs-lookup"><span data-stu-id="5d0f2-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5d0f2-116">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="5d0f2-117">**2**</span><span class="sxs-lookup"><span data-stu-id="5d0f2-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5d0f2-118">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="5d0f2-119">**8**</span><span class="sxs-lookup"><span data-stu-id="5d0f2-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5d0f2-120">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5d0f2-121">**9**</span><span class="sxs-lookup"><span data-stu-id="5d0f2-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5d0f2-122">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5d0f2-123">**10**</span><span class="sxs-lookup"><span data-stu-id="5d0f2-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5d0f2-124">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5d0f2-125">**11**</span><span class="sxs-lookup"><span data-stu-id="5d0f2-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5d0f2-126">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="5d0f2-127">**12**</span><span class="sxs-lookup"><span data-stu-id="5d0f2-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5d0f2-128">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="5d0f2-129">**13**</span><span class="sxs-lookup"><span data-stu-id="5d0f2-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5d0f2-130">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="5d0f2-131">**14**</span><span class="sxs-lookup"><span data-stu-id="5d0f2-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5d0f2-132">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="5d0f2-133">**15**</span><span class="sxs-lookup"><span data-stu-id="5d0f2-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5d0f2-134">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="5d0f2-135">**16**</span><span class="sxs-lookup"><span data-stu-id="5d0f2-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5d0f2-136">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5d0f2-137">**17**</span><span class="sxs-lookup"><span data-stu-id="5d0f2-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5d0f2-138">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="5d0f2-139">**21**</span><span class="sxs-lookup"><span data-stu-id="5d0f2-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5d0f2-140">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5d0f2-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5d0f2-141">Remarks</span></span>

<span data-ttu-id="5d0f2-142">Para cambiar el nombre de una carpeta, primero Enlace a la carpeta en cuestión y, a continuación, llame al método Rename.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-142">To rename a folder, first bind to the folder in question and then call the Rename method.</span></span> <span data-ttu-id="5d0f2-143">Como único parámetro del método, pase el nuevo nombre de la carpeta como un nombre de ruta de acceso completo.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-143">As the sole parameter to the method, pass the new name for the folder as a complete path name.</span></span> <span data-ttu-id="5d0f2-144">Por ejemplo, si la carpeta de la copia de \\ seguridad de registros c: scripts \\ se va a cambiar de nombre \\ c: \\ scripts \\ , debe pasar c: \\ scripts \\ Archive como el nombre completo de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-144">For example, if the folder in the C:\\Scripts\\Logs\\Backup is to be renamed C:\\Scripts\\Archive, you must pass C:\\Scripts\\Archive as the complete folder name.</span></span> <span data-ttu-id="5d0f2-145">Al pasar solo el nombre de la carpeta-Archive, se produce un error de ruta de acceso no válido.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-145">Passing only the folder name - Archive - results in an Invalid path error.</span></span>

<span data-ttu-id="5d0f2-146">La clase de directorio Win32 no \_ proporciona un método de un solo paso para mover carpetas.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-146">The Win32\_Directory class does not provide a one-step method for moving folders.</span></span> <span data-ttu-id="5d0f2-147">En su lugar, mover una carpeta normalmente implica dos pasos:</span><span class="sxs-lookup"><span data-stu-id="5d0f2-147">Instead, moving a folder generally involves two steps:</span></span>

<dl> 1. <span data-ttu-id="5d0f2-148">Copiar la carpeta en su nueva ubicación</span><span class="sxs-lookup"><span data-stu-id="5d0f2-148">Copying the folder to its new location</span></span>  
2. <span data-ttu-id="5d0f2-149">Eliminar la carpeta original</span><span class="sxs-lookup"><span data-stu-id="5d0f2-149">Deleting the original folder</span></span>  
</dl>

<span data-ttu-id="5d0f2-150">La única excepción a este proceso de dos pasos consiste en mover una carpeta a una nueva ubicación en la misma unidad.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-150">The one exception to this two-step process involves moving a folder to a new location on the same drive.</span></span> <span data-ttu-id="5d0f2-151">Por ejemplo, supongamos que desea trasladar C: \\ temp a c: \\ scripts \\ archivo de archivos temporales \\ .</span><span class="sxs-lookup"><span data-stu-id="5d0f2-151">For example, suppose you want to move C:\\Temp to C:\\Scripts\\Temporary Files\\Archive.</span></span> <span data-ttu-id="5d0f2-152">Siempre que la ubicación actual y la nueva ubicación estén en la misma unidad, puede mover la carpeta simplemente llamando al método Rename y pasando la nueva ubicación como parámetro de método.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-152">As long as the current location and the new location are on the same drive, you can move the folder by simply calling the Rename method and passing the new location as the method parameter.</span></span> <span data-ttu-id="5d0f2-153">Este enfoque permite desplazar la carpeta en un solo paso.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-153">This approach effectively allows you to move the folder in a single step.</span></span> <span data-ttu-id="5d0f2-154">Sin embargo, se produce un error en el script si la unidad actual y la nueva unidad son diferentes.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-154">However, the script fails if the current drive and the new drive are different.</span></span> <span data-ttu-id="5d0f2-155">Se produce un error al intentar cambiar el nombre de C: \\ temp a D: \\ Temp con un error "la unidad no es el mismo".</span><span class="sxs-lookup"><span data-stu-id="5d0f2-155">An attempt to rename C:\\Temp to D:\\Temp fails with a "Drive not the same" error.</span></span>

## <a name="examples"></a><span data-ttu-id="5d0f2-156">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5d0f2-156">Examples</span></span>

<span data-ttu-id="5d0f2-157">En el código siguiente, en el ejemplo de [migración de una carpeta mediante WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript en la galería de TechNet, se usa el método Rename para trasladar la carpeta c: \\ scripts a c: \\ documentos de Admins \\ \\ archivo \\ VBScript.</span><span class="sxs-lookup"><span data-stu-id="5d0f2-157">The following code, from the [Move a Folder Using WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript sample on TechNet Gallery, uses the Rename method to move the folder C:\\Scripts to C:\\Admins\\Documents\\Archive\\VBScript.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery _ 
    ("Select * from Win32_Directory where name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename("C:\Admins\Documents\Archive\VBScript") 
Next
```



## <a name="requirements"></a><span data-ttu-id="5d0f2-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d0f2-158">Requirements</span></span>



| <span data-ttu-id="5d0f2-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d0f2-159">Requirement</span></span> | <span data-ttu-id="5d0f2-160">Value</span><span class="sxs-lookup"><span data-stu-id="5d0f2-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d0f2-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d0f2-161">Minimum supported client</span></span><br/> | <span data-ttu-id="5d0f2-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5d0f2-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5d0f2-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d0f2-163">Minimum supported server</span></span><br/> | <span data-ttu-id="5d0f2-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5d0f2-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5d0f2-165">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5d0f2-165">Namespace</span></span><br/>                | <span data-ttu-id="5d0f2-166">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5d0f2-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5d0f2-167">MOF</span><span class="sxs-lookup"><span data-stu-id="5d0f2-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5d0f2-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5d0f2-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5d0f2-169">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5d0f2-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d0f2-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d0f2-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d0f2-171">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d0f2-171">See also</span></span>

<dl> <dt>

<span data-ttu-id="5d0f2-172">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5d0f2-172">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5d0f2-173">**\_Directorio Win32**</span><span class="sxs-lookup"><span data-stu-id="5d0f2-173">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

