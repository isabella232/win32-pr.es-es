---
description: Copia el archivo de entrada de directorio lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.
ms.assetid: 038e23d7-71db-4db6-8fb1-e84e972510c9
ms.tgt_platform: multiple
title: Método de copia de la clase Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 25568167d9532303a7cbee794757bc674a378b39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153149"
---
# <a name="copy-method-of-the-win32_directory-class"></a><span data-ttu-id="d2a1f-103">Método de copia de la \_ clase de directorio Win32</span><span class="sxs-lookup"><span data-stu-id="d2a1f-103">Copy method of the Win32\_Directory class</span></span>

<span data-ttu-id="d2a1f-104">El método **copiar** [clase WMI](/windows/desktop/WmiSdk/retrieving-a-class) copia el archivo de entrada de directorio lógico o el directorio especificado en la ruta de acceso del objeto en la ubicación especificada por el parámetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical directory entry file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="d2a1f-105">No se admite una copia si se requiere sobrescribir un archivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="d2a1f-106">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="d2a1f-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d2a1f-107">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d2a1f-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d2a1f-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d2a1f-108">Syntax</span></span>


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="d2a1f-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d2a1f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2a1f-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="d2a1f-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="d2a1f-111">Nombre completo de la copia del archivo (o directorio).</span><span class="sxs-lookup"><span data-stu-id="d2a1f-111">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="d2a1f-112">Ejemplo: c: \\ temp \\ newdirectory</span><span class="sxs-lookup"><span data-stu-id="d2a1f-112">Example: c:\\temp\\newdirectory</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2a1f-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2a1f-113">Return value</span></span>

<span data-ttu-id="d2a1f-114">Devuelve un valor de 0 (cero) si el archivo se ha copiado correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-114">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d2a1f-115">**0**</span><span class="sxs-lookup"><span data-stu-id="d2a1f-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d2a1f-116">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="d2a1f-117">**2**</span><span class="sxs-lookup"><span data-stu-id="d2a1f-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d2a1f-118">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="d2a1f-119">**8**</span><span class="sxs-lookup"><span data-stu-id="d2a1f-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d2a1f-120">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d2a1f-121">**9**</span><span class="sxs-lookup"><span data-stu-id="d2a1f-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d2a1f-122">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d2a1f-123">**10**</span><span class="sxs-lookup"><span data-stu-id="d2a1f-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d2a1f-124">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d2a1f-125">**11**</span><span class="sxs-lookup"><span data-stu-id="d2a1f-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d2a1f-126">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d2a1f-127">**12**</span><span class="sxs-lookup"><span data-stu-id="d2a1f-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d2a1f-128">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d2a1f-129">**13**</span><span class="sxs-lookup"><span data-stu-id="d2a1f-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d2a1f-130">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d2a1f-131">**14**</span><span class="sxs-lookup"><span data-stu-id="d2a1f-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d2a1f-132">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d2a1f-133">**15**</span><span class="sxs-lookup"><span data-stu-id="d2a1f-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d2a1f-134">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d2a1f-135">**16**</span><span class="sxs-lookup"><span data-stu-id="d2a1f-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d2a1f-136">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d2a1f-137">**17**</span><span class="sxs-lookup"><span data-stu-id="d2a1f-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d2a1f-138">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="d2a1f-139">**21**</span><span class="sxs-lookup"><span data-stu-id="d2a1f-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d2a1f-140">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d2a1f-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d2a1f-141">Remarks</span></span>

<span data-ttu-id="d2a1f-142">A menudo es necesario copiar las carpetas de una ubicación a otra.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-142">Folders often need to be copied from one location to another.</span></span> <span data-ttu-id="d2a1f-143">Por ejemplo, puede copiar una carpeta de un servidor a otro para crear una copia de seguridad de esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-143">For example, you might copy a folder from one server to another to create a backup copy of that folder.</span></span> <span data-ttu-id="d2a1f-144">O bien, es posible que tenga una carpeta plantillas que deba copiarse en estaciones de trabajo de usuario o una carpeta de scripts que debe copiarse en todos los servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-144">Or you might have a templates folder that needs to be copied to user workstations, or a scripts folder that should be copied to all of your DNS servers.</span></span>

<span data-ttu-id="d2a1f-145">El \_ método de copia de directorios de Win32 permite copiar una carpeta de una ubicación a otra, ya sea en el mismo equipo (por ejemplo, copiando una carpeta de la unidad C a la unidad D) o en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-145">The Win32\_Directory Copy method enables you to copy a folder from one location to another, either on the same computer (for example, copying a folder from drive C to drive D) or on a remote computer.</span></span> <span data-ttu-id="d2a1f-146">Para copiar una carpeta, se devuelve una instancia de la carpeta que se va a copiar y, a continuación, se llama al método de copia, pasando como parámetro la ubicación de destino para la nueva copia de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-146">To copy a folder, you return an instance of the folder to be copied and then call the Copy method, passing as a parameter the target location for the new copy of the folder.</span></span> <span data-ttu-id="d2a1f-147">Por ejemplo, esta línea de código copia una carpeta en la carpeta scripts de la unidad F:</span><span class="sxs-lookup"><span data-stu-id="d2a1f-147">For example, this line of code copies a folder to the Scripts folder on drive F:</span></span>

`objFolder.Copy("F:\Scripts")`

<span data-ttu-id="d2a1f-148">WMI no sobrescribirá una carpeta existente al ejecutar el método de copia.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-148">WMI will not overwrite an existing folder when executing the Copy method.</span></span> <span data-ttu-id="d2a1f-149">Esto significa que se produce un error en la operación de copia si existe la carpeta de destino.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-149">This means that the copy operation fails if the destination folder exists.</span></span> <span data-ttu-id="d2a1f-150">Por ejemplo, supongamos que tiene una carpeta denominada scripts e intenta copiar esa carpeta en un recurso compartido remoto denominado \\ \\ archivo ATL-FS-01 \\ .</span><span class="sxs-lookup"><span data-stu-id="d2a1f-150">For example, suppose you have a folder named Scripts and you attempt to copy that folder to a remote share named \\\\atl-fs-01\\archive.</span></span> <span data-ttu-id="d2a1f-151">Si ya existe una carpeta con el nombre scripts en ese recurso compartido, se produce un error en la operación de copia.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-151">If a folder named Scripts already exists on that share, the copy operation fails.</span></span>

## <a name="examples"></a><span data-ttu-id="d2a1f-152">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d2a1f-152">Examples</span></span>

<span data-ttu-id="d2a1f-153">El ejemplo de código siguientes, tomado de la [copia de una carpeta mediante WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2), usa el método de copia para copiar la carpeta C: \\ scripts en D: \\ Archive.</span><span class="sxs-lookup"><span data-stu-id="d2a1f-153">The followng code sample, taken from the [Copy a Folder Using WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2), uses the Copy method to copy the folder C:\\Scripts to D:\\Archive.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery( _ 
    "Select * from Win32_Directory where Name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy("D:\Archive") 
Next
```



## <a name="requirements"></a><span data-ttu-id="d2a1f-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d2a1f-154">Requirements</span></span>



| <span data-ttu-id="d2a1f-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="d2a1f-155">Requirement</span></span> | <span data-ttu-id="d2a1f-156">Value</span><span class="sxs-lookup"><span data-stu-id="d2a1f-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d2a1f-157">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2a1f-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d2a1f-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d2a1f-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d2a1f-159">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d2a1f-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d2a1f-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d2a1f-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d2a1f-161">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="d2a1f-161">Namespace</span></span><br/>                | <span data-ttu-id="d2a1f-162">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d2a1f-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d2a1f-163">MOF</span><span class="sxs-lookup"><span data-stu-id="d2a1f-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d2a1f-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d2a1f-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d2a1f-165">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d2a1f-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2a1f-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d2a1f-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2a1f-167">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2a1f-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="d2a1f-168">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d2a1f-168">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d2a1f-169">**\_Directorio Win32**</span><span class="sxs-lookup"><span data-stu-id="d2a1f-169">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

