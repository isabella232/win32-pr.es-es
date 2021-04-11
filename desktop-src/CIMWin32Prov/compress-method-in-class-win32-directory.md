---
description: Comprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto.
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: Método compress de la clase Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea694c09e11e5801016a4ea85b9774448c542991
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104152868"
---
# <a name="compress-method-of-the-win32_directory-class"></a><span data-ttu-id="8234d-103">Método compress de la \_ clase de directorio Win32</span><span class="sxs-lookup"><span data-stu-id="8234d-103">Compress method of the Win32\_Directory class</span></span>

<span data-ttu-id="8234d-104">El método **compress** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) comprime el archivo de entrada de directorio lógico (o directorio) especificado en la ruta de acceso del objeto.</span><span class="sxs-lookup"><span data-stu-id="8234d-104">The **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical directory entry file (or directory) specified in the object path.</span></span>

<span data-ttu-id="8234d-105">En este tema se usa la sintaxis de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="8234d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8234d-106">Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="8234d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8234d-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8234d-107">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="8234d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8234d-108">Parameters</span></span>

<span data-ttu-id="8234d-109">Este método no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="8234d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8234d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8234d-110">Return value</span></span>

<span data-ttu-id="8234d-111">Devuelve un valor de 0 (cero) si el archivo se ha comprimido correctamente y cualquier otro número para indicar un error.</span><span class="sxs-lookup"><span data-stu-id="8234d-111">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="8234d-112">**0**</span><span class="sxs-lookup"><span data-stu-id="8234d-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="8234d-113">La solicitud fue correcta.</span><span class="sxs-lookup"><span data-stu-id="8234d-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="8234d-114">**2**</span><span class="sxs-lookup"><span data-stu-id="8234d-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="8234d-115">Se denegó el acceso.</span><span class="sxs-lookup"><span data-stu-id="8234d-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="8234d-116">**8**</span><span class="sxs-lookup"><span data-stu-id="8234d-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="8234d-117">Se produjo un error no especificado.</span><span class="sxs-lookup"><span data-stu-id="8234d-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="8234d-118">**9**</span><span class="sxs-lookup"><span data-stu-id="8234d-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="8234d-119">El nombre especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="8234d-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8234d-120">**10**</span><span class="sxs-lookup"><span data-stu-id="8234d-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="8234d-121">El objeto especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="8234d-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8234d-122">**11**</span><span class="sxs-lookup"><span data-stu-id="8234d-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="8234d-123">El sistema de archivos no es NTFS.</span><span class="sxs-lookup"><span data-stu-id="8234d-123">The file system is not an NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="8234d-124">**12**</span><span class="sxs-lookup"><span data-stu-id="8234d-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="8234d-125">La plataforma no es Windows.</span><span class="sxs-lookup"><span data-stu-id="8234d-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8234d-126">**13**</span><span class="sxs-lookup"><span data-stu-id="8234d-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="8234d-127">La unidad no es la misma.</span><span class="sxs-lookup"><span data-stu-id="8234d-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="8234d-128">**14**</span><span class="sxs-lookup"><span data-stu-id="8234d-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="8234d-129">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="8234d-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="8234d-130">**15**</span><span class="sxs-lookup"><span data-stu-id="8234d-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="8234d-131">Se ha producido una infracción de uso compartido.</span><span class="sxs-lookup"><span data-stu-id="8234d-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="8234d-132">**16**</span><span class="sxs-lookup"><span data-stu-id="8234d-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="8234d-133">El archivo de inicio especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="8234d-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8234d-134">**17**</span><span class="sxs-lookup"><span data-stu-id="8234d-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="8234d-135">No se mantiene un privilegio necesario para la operación.</span><span class="sxs-lookup"><span data-stu-id="8234d-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="8234d-136">**21**</span><span class="sxs-lookup"><span data-stu-id="8234d-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="8234d-137">Un parámetro especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="8234d-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8234d-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8234d-138">Remarks</span></span>

<span data-ttu-id="8234d-139">La compresión proporciona una forma de liberar espacio de almacenamiento adicional en una unidad de disco sin necesidad de adquirir hardware nuevo y sin quitar archivos o carpetas.</span><span class="sxs-lookup"><span data-stu-id="8234d-139">Compression provides a way to free additional storage space on a disk drive without purchasing new hardware and without removing files or folders.</span></span> <span data-ttu-id="8234d-140">En función del tamaño del disco duro y del tipo de archivos almacenados en ese disco, es posible que pueda recuperar cientos de megabytes de espacio en disco y, por lo tanto, no tenga que adquirir una nueva unidad de disco duro y dejar el equipo sin conexión hasta que se instale la nueva unidad.</span><span class="sxs-lookup"><span data-stu-id="8234d-140">Depending on the size of your hard disk and the type of files stored on that disk, you might be able to recover hundreds of megabytes of disk space and thus preclude the need to purchase a new hard drive and to take the computer offline until the new drive is installed.</span></span>

<span data-ttu-id="8234d-141">El método compress comprime todos los archivos y subcarpetas de una carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="8234d-141">The Compress method compresses all the files and subfolders within a specified folder.</span></span> <span data-ttu-id="8234d-142">Además, la clase también incluye un método UNCOMPRESS que quita la compresión de todos los archivos y subcarpetas de una carpeta.</span><span class="sxs-lookup"><span data-stu-id="8234d-142">In addition, the class also includes an Uncompress method that removes compression from all the files and subfolders in a folder.</span></span> <span data-ttu-id="8234d-143">También se proporcionan métodos similares con la \_ clase de archivo de archivos CIM.</span><span class="sxs-lookup"><span data-stu-id="8234d-143">Similar methods are also provided with the CIM\_Datafile class.</span></span> <span data-ttu-id="8234d-144">Esto le permite comprimir o descomprimir archivos específicos de una carpeta de forma selectiva.</span><span class="sxs-lookup"><span data-stu-id="8234d-144">This allows you to selectively compress or uncompress specific files within a folder.</span></span>

<span data-ttu-id="8234d-145">Dado que la compresión es una ligera disminución del rendimiento, no se recomienda para los archivos o carpetas a los que se tiene acceso de forma rutinaria. por ejemplo, es probable que no desee comprimir archivos de base de datos, archivos de registro o carpetas de perfiles de usuario.</span><span class="sxs-lookup"><span data-stu-id="8234d-145">Because compression imparts a slight performance penalty, it is not recommended for files or folders that are accessed on a routine basis; for example, you probably do not want to compress database files, log files, or user profile folders.</span></span> <span data-ttu-id="8234d-146">Los mejores candidatos para la compresión son los archivos y las carpetas a los que no se tiene acceso con mucha frecuencia.</span><span class="sxs-lookup"><span data-stu-id="8234d-146">Better candidates for compression are files and folders that are not accessed very often.</span></span> <span data-ttu-id="8234d-147">Por ejemplo, puede escribir un script para devolver una colección de carpetas de una unidad a la que no se ha accedido durante un mes o más y, a continuación, comprimir cada una de esas carpetas.</span><span class="sxs-lookup"><span data-stu-id="8234d-147">For example, you might write a script to return a collection of folders on a drive that have not been accessed for a month or more and then compress each of those folders.</span></span>

<span data-ttu-id="8234d-148">La cantidad de espacio en disco liberado por las carpetas de compresión varía en función del tipo de archivos almacenados en esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="8234d-148">The amount of disk space freed by compressing folders varies depending on the type of files stored in that folder.</span></span> <span data-ttu-id="8234d-149">Por ejemplo, los archivos. jpg ya están comprimidos y la compresión adicional tiene poco efecto en el tamaño del archivo.</span><span class="sxs-lookup"><span data-stu-id="8234d-149">For example, .jpg files are already compressed, and further compression has little effect on the size of the file.</span></span> <span data-ttu-id="8234d-150">Con otros tipos de archivo, sin embargo, el ahorro puede ser considerable.</span><span class="sxs-lookup"><span data-stu-id="8234d-150">With other file types, however, the savings can be considerable.</span></span> <span data-ttu-id="8234d-151">Por ejemplo, se ha creado una nueva carpeta en un equipo de prueba basado en Windows 2000 y 33 documentos de Microsoft Word, con un total de 15 megabytes (MB) de espacio en disco, que se han copiado en esa carpeta.</span><span class="sxs-lookup"><span data-stu-id="8234d-151">For example, a new folder was created on a Windows 2000-based test computer, and 33 Microsoft Word documents, taking up a total of 15 megabytes (MB) of disk space, were copied into that folder.</span></span> <span data-ttu-id="8234d-152">Cuando se comprimen los documentos, la carpeta solo tenía 7 MB de espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="8234d-152">When the documents were compressed, the folder took up only 7 MB of disk space.</span></span>

## <a name="examples"></a><span data-ttu-id="8234d-153">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="8234d-153">Examples</span></span>

<span data-ttu-id="8234d-154">El siguiente ejemplo de VBScript comprime la carpeta C: \\ scripts.</span><span class="sxs-lookup"><span data-stu-id="8234d-154">The following VBScript sample compresses the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Compress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="8234d-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8234d-155">Requirements</span></span>



| <span data-ttu-id="8234d-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="8234d-156">Requirement</span></span> | <span data-ttu-id="8234d-157">Value</span><span class="sxs-lookup"><span data-stu-id="8234d-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8234d-158">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8234d-158">Minimum supported client</span></span><br/> | <span data-ttu-id="8234d-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8234d-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8234d-160">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8234d-160">Minimum supported server</span></span><br/> | <span data-ttu-id="8234d-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8234d-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8234d-162">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="8234d-162">Namespace</span></span><br/>                | <span data-ttu-id="8234d-163">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="8234d-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8234d-164">MOF</span><span class="sxs-lookup"><span data-stu-id="8234d-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8234d-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="8234d-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8234d-166">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="8234d-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8234d-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8234d-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8234d-168">Vea también</span><span class="sxs-lookup"><span data-stu-id="8234d-168">See also</span></span>

<dl> <dt>

<span data-ttu-id="8234d-169">[Clases de sistema operativo](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="8234d-169">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="8234d-170">**\_Directorio Win32**</span><span class="sxs-lookup"><span data-stu-id="8234d-170">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> <dt>

[<span data-ttu-id="8234d-171">**Descomprimir**</span><span class="sxs-lookup"><span data-stu-id="8234d-171">**Uncompress**</span></span>](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

