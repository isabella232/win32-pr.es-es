---
description: El método Delete WMI Class eliminará el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.
ms.assetid: 5663b8a8-3089-475b-8a36-454a7315bfca
ms.tgt_platform: multiple
title: Método Delete de la clase Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 843583698c11c1b9ad8f08e83aa6e4b894b55db8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659765"
---
# <a name="delete-method-of-the-win32_directory-class"></a><span data-ttu-id="c69d6-103">Método Delete de la \_ clase de directorio Win32</span><span class="sxs-lookup"><span data-stu-id="c69d6-103">Delete method of the Win32\_Directory class</span></span>

<span data-ttu-id="c69d6-104">El método **Delete** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) eliminará el archivo lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="c69d6-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical file (or directory) specified in the object path.</span></span>

<span data-ttu-id="c69d6-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="c69d6-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c69d6-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c69d6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c69d6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c69d6-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="c69d6-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c69d6-108">Parameters</span></span>

<span data-ttu-id="c69d6-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="c69d6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c69d6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c69d6-110">Return value</span></span>

<span data-ttu-id="c69d6-111">Devuelve un valor de 0 (cero) si el archivo se eliminó correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="c69d6-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c69d6-112">**0**</span><span class="sxs-lookup"><span data-stu-id="c69d6-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c69d6-113">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="c69d6-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="c69d6-114">**2**</span><span class="sxs-lookup"><span data-stu-id="c69d6-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c69d6-115">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="c69d6-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="c69d6-116">**8**</span><span class="sxs-lookup"><span data-stu-id="c69d6-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c69d6-117">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="c69d6-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c69d6-118">**9**</span><span class="sxs-lookup"><span data-stu-id="c69d6-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c69d6-119">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="c69d6-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c69d6-120">**10**</span><span class="sxs-lookup"><span data-stu-id="c69d6-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c69d6-121">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="c69d6-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c69d6-122">**11**</span><span class="sxs-lookup"><span data-stu-id="c69d6-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c69d6-123">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="c69d6-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c69d6-124">**12**</span><span class="sxs-lookup"><span data-stu-id="c69d6-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c69d6-125">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="c69d6-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c69d6-126">**13**</span><span class="sxs-lookup"><span data-stu-id="c69d6-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c69d6-127">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="c69d6-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c69d6-128">**14**</span><span class="sxs-lookup"><span data-stu-id="c69d6-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c69d6-129">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="c69d6-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c69d6-130">**15**</span><span class="sxs-lookup"><span data-stu-id="c69d6-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c69d6-131">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="c69d6-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c69d6-132">**16**</span><span class="sxs-lookup"><span data-stu-id="c69d6-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c69d6-133">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="c69d6-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c69d6-134">**17**</span><span class="sxs-lookup"><span data-stu-id="c69d6-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c69d6-135">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="c69d6-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="c69d6-136">**21**</span><span class="sxs-lookup"><span data-stu-id="c69d6-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c69d6-137">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="c69d6-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c69d6-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c69d6-138">Remarks</span></span>

<span data-ttu-id="c69d6-139">Las carpetas no son necesariamente adiciones permanentes a un sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="c69d6-139">Folders are not necessarily permanent additions to a file system.</span></span> <span data-ttu-id="c69d6-140">En algún momento, es posible que sea necesario eliminar carpetas, quizás porque ya no son necesarias, ya que el rol del equipo ha cambiado o porque las carpetas se crearon por equivocación.</span><span class="sxs-lookup"><span data-stu-id="c69d6-140">At some point, folders might need to be deleted, perhaps because they are no longer required, because the role of the computer has changed, or because the folders were created by mistake.</span></span>

<span data-ttu-id="c69d6-141">Eliminar permite eliminar carpetas: simplemente se enlaza a la carpeta en cuestión y, a continuación, se llama al método Delete.</span><span class="sxs-lookup"><span data-stu-id="c69d6-141">Delete allows you to delete folders: you simply bind to the folder in question and then call the Delete method.</span></span> <span data-ttu-id="c69d6-142">Después de llamar al método Delete, la carpeta se quita permanentemente del sistema de archivos; no se envía a la papelera de reciclaje.</span><span class="sxs-lookup"><span data-stu-id="c69d6-142">After the Delete method is called, the folder is permanently removed from the file system; it is not sent to the Recycle Bin.</span></span> <span data-ttu-id="c69d6-143">Además, no hay ningún aviso de confirmación ("¿está seguro de que desea eliminar esta carpeta?").</span><span class="sxs-lookup"><span data-stu-id="c69d6-143">In addition, no confirmation notice ("Are you sure you want to delete this folder?") is issued.</span></span> <span data-ttu-id="c69d6-144">En su lugar, la carpeta se quita inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="c69d6-144">Instead, the folder is immediately removed.</span></span>

<span data-ttu-id="c69d6-145">No se pueden eliminar carpetas de solo lectura mediante FileSystemObject; sin embargo, esto se puede hacer mediante WMI.</span><span class="sxs-lookup"><span data-stu-id="c69d6-145">You cannot delete read-only folders using the FileSystemObject; however, this can be done using WMI.</span></span> <span data-ttu-id="c69d6-146">Si el script usa WMI y no desea quitar una carpeta de solo lectura, debe usar la propiedad legible para comprobar el estado de la carpeta antes de eliminarla.</span><span class="sxs-lookup"><span data-stu-id="c69d6-146">If your script uses WMI and you do not want to remove a read-only folder, you must use the Readable property to check the folder status before deleting it.</span></span>

## <a name="examples"></a><span data-ttu-id="c69d6-147">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="c69d6-147">Examples</span></span>

<span data-ttu-id="c69d6-148">El siguiente ejemplo de código de VBScript elimina la carpeta C: \\ scripts.</span><span class="sxs-lookup"><span data-stu-id="c69d6-148">The following VBScript code sample deletes the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Delete
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="c69d6-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c69d6-149">Requirements</span></span>



| <span data-ttu-id="c69d6-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="c69d6-150">Requirement</span></span> | <span data-ttu-id="c69d6-151">Value</span><span class="sxs-lookup"><span data-stu-id="c69d6-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c69d6-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c69d6-152">Minimum supported client</span></span><br/> | <span data-ttu-id="c69d6-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c69d6-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c69d6-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c69d6-154">Minimum supported server</span></span><br/> | <span data-ttu-id="c69d6-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c69d6-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c69d6-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c69d6-156">Namespace</span></span><br/>                | <span data-ttu-id="c69d6-157">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c69d6-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c69d6-158">MOF</span><span class="sxs-lookup"><span data-stu-id="c69d6-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c69d6-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c69d6-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c69d6-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c69d6-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c69d6-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c69d6-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c69d6-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="c69d6-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="c69d6-163">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c69d6-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c69d6-164">**\_Directorio Win32**</span><span class="sxs-lookup"><span data-stu-id="c69d6-164">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

