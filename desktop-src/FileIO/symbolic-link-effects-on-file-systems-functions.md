---
description: Cómo afectan los vínculos simbólicos a las funciones de archivo estándar que usan nombres de ruta de acceso para especificar uno o varios archivos.
ms.assetid: afda53eb-d0db-4844-9dd0-8a7d93ca341f
title: Efectos simbólicos de los vínculos en las funciones del sistema de archivos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4a2fe1696bf5260a0c55ba8b6e4f107270d6da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668370"
---
# <a name="symbolic-link-effects-on-file-systems-functions"></a><span data-ttu-id="665bb-103">Efectos simbólicos de los vínculos en las funciones del sistema de archivos</span><span class="sxs-lookup"><span data-stu-id="665bb-103">Symbolic Link Effects on File Systems Functions</span></span>

<span data-ttu-id="665bb-104">Varias funciones de archivo estándar que utilizan nombres de ruta de acceso para especificar uno o varios archivos se ven afectadas por el uso de vínculos simbólicos.</span><span class="sxs-lookup"><span data-stu-id="665bb-104">Several standard file functions that use path names to specify one or more files are affected by the use of symbolic links.</span></span> <span data-ttu-id="665bb-105">En este tema se enumeran las funciones y se describen los cambios de comportamiento:</span><span class="sxs-lookup"><span data-stu-id="665bb-105">This topic lists those functions and describes the changes in behavior:</span></span>

-   [<span data-ttu-id="665bb-106">CopyFile y CopyFileTransacted</span><span class="sxs-lookup"><span data-stu-id="665bb-106">CopyFile and CopyFileTransacted</span></span>](#copyfile-and-copyfiletransacted)
-   [<span data-ttu-id="665bb-107">CopyFileEx</span><span class="sxs-lookup"><span data-stu-id="665bb-107">CopyFileEx</span></span>](#copyfileex)
-   [<span data-ttu-id="665bb-108">CreateFile y CreateFileTransacted</span><span class="sxs-lookup"><span data-stu-id="665bb-108">CreateFile and CreateFileTransacted</span></span>](#createfile-and-createfiletransacted)
-   [<span data-ttu-id="665bb-109">CreateHardLink y CreateHardLinkTransacted</span><span class="sxs-lookup"><span data-stu-id="665bb-109">CreateHardLink and CreateHardLinkTransacted</span></span>](#createhardlink-and-createhardlinktransacted)
-   [<span data-ttu-id="665bb-110">DeleteFile y DeleteFileTransacted</span><span class="sxs-lookup"><span data-stu-id="665bb-110">DeleteFile and DeleteFileTransacted</span></span>](#deletefile-and-deletefiletransacted)
-   [<span data-ttu-id="665bb-111">FindFirstChangeNotification</span><span class="sxs-lookup"><span data-stu-id="665bb-111">FindFirstChangeNotification</span></span>](#findfirstchangenotification)
-   [<span data-ttu-id="665bb-112">FindFirstFile y FindFirstFileTransacted</span><span class="sxs-lookup"><span data-stu-id="665bb-112">FindFirstFile and FindFirstFileTransacted</span></span>](#findfirstfile-and-findfirstfiletransacted)
-   [<span data-ttu-id="665bb-113">FindFirstFileEx</span><span class="sxs-lookup"><span data-stu-id="665bb-113">FindFirstFileEx</span></span>](#findfirstfileex)
-   [<span data-ttu-id="665bb-114">FindNextFile</span><span class="sxs-lookup"><span data-stu-id="665bb-114">FindNextFile</span></span>](#findnextfile)
-   [<span data-ttu-id="665bb-115">GetBinaryType</span><span class="sxs-lookup"><span data-stu-id="665bb-115">GetBinaryType</span></span>](#getbinarytype)
-   [<span data-ttu-id="665bb-116">GetCompressedFileSize y GetCompressedFileSizeTransacted</span><span class="sxs-lookup"><span data-stu-id="665bb-116">GetCompressedFileSize and GetCompressedFileSizeTransacted</span></span>](#getcompressedfilesize-and-getcompressedfilesizetransacted)
-   [<span data-ttu-id="665bb-117">GetDiskFreeSpace</span><span class="sxs-lookup"><span data-stu-id="665bb-117">GetDiskFreeSpace</span></span>](#getdiskfreespaceex)
-   [<span data-ttu-id="665bb-118">GetDiskFreeSpaceEx</span><span class="sxs-lookup"><span data-stu-id="665bb-118">GetDiskFreeSpaceEx</span></span>](#getdiskfreespaceex)
-   [<span data-ttu-id="665bb-119">GetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="665bb-119">GetFileAttributes</span></span>](#getfileattributesex)
-   [<span data-ttu-id="665bb-120">GetFileAttributesEx</span><span class="sxs-lookup"><span data-stu-id="665bb-120">GetFileAttributesEx</span></span>](#getfileattributesex)
-   [<span data-ttu-id="665bb-121">GetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="665bb-121">GetFileSecurity</span></span>](#getfilesecurity)
-   [<span data-ttu-id="665bb-122">GetTempPath</span><span class="sxs-lookup"><span data-stu-id="665bb-122">GetTempPath</span></span>](#gettemppath)
-   [<span data-ttu-id="665bb-123">GetVolumeInformation</span><span class="sxs-lookup"><span data-stu-id="665bb-123">GetVolumeInformation</span></span>](#getvolumeinformation)
-   [<span data-ttu-id="665bb-124">SetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="665bb-124">SetFileAttributes</span></span>](#setfileattributes)
-   [<span data-ttu-id="665bb-125">SetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="665bb-125">SetFileSecurity</span></span>](#setfilesecurity)
-   [<span data-ttu-id="665bb-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="665bb-126">Related topics</span></span>](#related-topics)

<span data-ttu-id="665bb-127">En las siguientes descripciones, se usan los términos siguientes:</span><span class="sxs-lookup"><span data-stu-id="665bb-127">In the descriptions below, the following terms are used:</span></span>

-   <span data-ttu-id="665bb-128">Archivo de origen: el archivo original que se va a copiar.</span><span class="sxs-lookup"><span data-stu-id="665bb-128">Source file—The original file that is to be copied.</span></span>
-   <span data-ttu-id="665bb-129">Archivo de destino: la copia recién creada del archivo.</span><span class="sxs-lookup"><span data-stu-id="665bb-129">Destination file—The newly created copy of the file.</span></span>
-   <span data-ttu-id="665bb-130">Destino: la entidad a la que apunta un vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="665bb-130">Target—The entity that a symbolic link points to.</span></span>

> [!Note]  
> <span data-ttu-id="665bb-131">El comportamiento de las funciones que aceptan un identificador creado con la función [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) , como la función [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) , variará en función de si se llamó a la función **CreateFile** mediante la marca de **\_ \_ \_ \_ punto de reanálisis de la marca de archivo abierta** .</span><span class="sxs-lookup"><span data-stu-id="665bb-131">The behavior of functions that accept a handle created using the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function, such as the [**GetFileTime**](/windows/desktop/api/fileapi/nf-fileapi-getfiletime) function, will differ based on whether or not the **CreateFile** function was called using the **FILE\_FLAG\_OPEN\_REPARSE\_POINT** flag.</span></span> <span data-ttu-id="665bb-132">Para obtener más información, vea [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) y la siguiente sección de [CreateFile y CreateFileTransacted](#createfile-and-createfiletransacted) .</span><span class="sxs-lookup"><span data-stu-id="665bb-132">For more information, see [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and the following [CreateFile and CreateFileTransacted](#createfile-and-createfiletransacted) section.</span></span>

 

## <a name="copyfile-and-copyfiletransacted"></a><span data-ttu-id="665bb-133">CopyFile y CopyFileTransacted</span><span class="sxs-lookup"><span data-stu-id="665bb-133">CopyFile and CopyFileTransacted</span></span>

<span data-ttu-id="665bb-134">Si el archivo de origen es un vínculo simbólico, el archivo que se ha copiado es el destino del vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="665bb-134">If the source file is a symbolic link, the actual file copied is the target of the symbolic link.</span></span>

<span data-ttu-id="665bb-135">Si el archivo de destino ya existe y es un vínculo simbólico, el archivo de código fuente sobrescribe el vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="665bb-135">If the destination file already exists and is a symbolic link, the symbolic link is overwritten by the source file.</span></span>

## <a name="copyfileex"></a><span data-ttu-id="665bb-136">CopyFileEx</span><span class="sxs-lookup"><span data-stu-id="665bb-136">CopyFileEx</span></span>

<span data-ttu-id="665bb-137">Si se especifica **Copy \_ file \_ Copy \_ SYMLINK** y:</span><span class="sxs-lookup"><span data-stu-id="665bb-137">If **COPY\_FILE\_COPY\_SYMLINK** is specified and:</span></span>

-   <span data-ttu-id="665bb-138">Si el archivo de origen es un vínculo simbólico, se copia el vínculo simbólico, no el archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-138">If the source file is a symbolic link, the symbolic link is copied, not the target file.</span></span>
-   <span data-ttu-id="665bb-139">Si el archivo de origen no es un vínculo simbólico, no hay ningún cambio en el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="665bb-139">If the source file is not a symbolic link, there is no change in behavior.</span></span>
-   <span data-ttu-id="665bb-140">Si el archivo de destino es un vínculo simbólico existente, se sobrescribe el vínculo simbólico, no el archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-140">If the destination file is an existing symbolic link, the symbolic link is overwritten, not the target file.</span></span>
-   <span data-ttu-id="665bb-141">Si también se especifica la operación de **copia de \_ archivo \_ \_ si \_ existe** y el archivo de destino es un vínculo simbólico existente, se produce un error en la operación en todos los casos.</span><span class="sxs-lookup"><span data-stu-id="665bb-141">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is also specified, and the destination file is an existing symbolic link, the operation fails in all cases.</span></span>

<span data-ttu-id="665bb-142">Si no se especifica **Copy \_ file \_ Copy \_ SYMLINK** y:</span><span class="sxs-lookup"><span data-stu-id="665bb-142">If **COPY\_FILE\_COPY\_SYMLINK** is not specified and:</span></span>

-   <span data-ttu-id="665bb-143">Si también se especifica la operación de **copia de \_ archivo \_ \_ si \_ existe** , y el archivo de destino es un vínculo simbólico existente, se produce un error en la operación solo si existe el destino del vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="665bb-143">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is also specified, and the destination file is an existing symbolic link, the operation fails only if the target of the symbolic link exists.</span></span>
-   <span data-ttu-id="665bb-144">Si no se especifica **Copy File si no se especifica \_ \_ \_ \_ EXISTS** , no se produce ningún cambio en el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="665bb-144">If **COPY\_FILE\_FAIL\_IF\_EXISTS** is not specified, there is no change in behavior.</span></span>

<span data-ttu-id="665bb-145">**Windows Server 2003 y Windows XP:** No se admite la marca de **\_ \_ \_ SYMLINK copiar archivo** .</span><span class="sxs-lookup"><span data-stu-id="665bb-145">**Windows Server 2003 and Windows XP:** The **COPY\_FILE\_COPY\_SYMLINK** flag is not supported.</span></span> <span data-ttu-id="665bb-146">Si el archivo de origen es un vínculo simbólico, el archivo que se ha copiado es el destino del vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="665bb-146">If the source file is a symbolic link, the actual file copied is the target of the symbolic link.</span></span>

## <a name="createfile-and-createfiletransacted"></a><span data-ttu-id="665bb-147">CreateFile y CreateFileTransacted</span><span class="sxs-lookup"><span data-stu-id="665bb-147">CreateFile and CreateFileTransacted</span></span>

<span data-ttu-id="665bb-148">Si la llamada a esta función crea un nuevo archivo, no hay ningún cambio en el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="665bb-148">If the call to this function creates a new file, there is no change in behavior.</span></span>

<span data-ttu-id="665bb-149">Si se especifica el **marcador de archivo, abra el \_ \_ \_ \_ punto de reanálisis** y:</span><span class="sxs-lookup"><span data-stu-id="665bb-149">If **FILE\_FLAG\_OPEN\_REPARSE\_POINT** is specified and:</span></span>

-   <span data-ttu-id="665bb-150">Si se abre un archivo existente y es un vínculo simbólico, el identificador devuelto es un identificador del vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="665bb-150">If an existing file is opened and it is a symbolic link, the handle returned is a handle to the symbolic link.</span></span>
-   <span data-ttu-id="665bb-151">Si **crear \_ siempre**, **truncar \_ existente** o **\_ \_ Borrar marca de archivo \_ al \_ cerrar** se especifican, el archivo afectado es un vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="665bb-151">If **CREATE\_ALWAYS**, **TRUNCATE\_EXISTING**, or **FILE\_FLAG\_DELETE\_ON\_CLOSE** are specified, the file affected is a symbolic link.</span></span>

<span data-ttu-id="665bb-152">Si no se especifica el **marcador de archivo, abra el \_ \_ \_ \_ punto de reanálisis** y:</span><span class="sxs-lookup"><span data-stu-id="665bb-152">If **FILE\_FLAG\_OPEN\_REPARSE\_POINT** is not specified and:</span></span>

-   <span data-ttu-id="665bb-153">Si se abre un archivo existente y es un vínculo simbólico, el identificador devuelto es un identificador del destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-153">If an existing file is opened and it is a symbolic link, the handle returned is a handle to the target.</span></span>
-   <span data-ttu-id="665bb-154">Si **crear \_ siempre**, **truncar \_ existente** o **\_ \_ Borrar marca de archivo \_ al \_ cerrar** se especifican, el archivo afectado es el destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-154">If **CREATE\_ALWAYS**, **TRUNCATE\_EXISTING**, or **FILE\_FLAG\_DELETE\_ON\_CLOSE** are specified, the file affected is the target.</span></span>

## <a name="createhardlink-and-createhardlinktransacted"></a><span data-ttu-id="665bb-155">CreateHardLink y CreateHardLinkTransacted</span><span class="sxs-lookup"><span data-stu-id="665bb-155">CreateHardLink and CreateHardLinkTransacted</span></span>

<span data-ttu-id="665bb-156">Si la ruta de acceso apunta a un vínculo simbólico, la función crea un vínculo físico al destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-156">If the path points to a symbolic link, the function creates a hard link to the target.</span></span>

## <a name="deletefile-and-deletefiletransacted"></a><span data-ttu-id="665bb-157">DeleteFile y DeleteFileTransacted</span><span class="sxs-lookup"><span data-stu-id="665bb-157">DeleteFile and DeleteFileTransacted</span></span>

<span data-ttu-id="665bb-158">Si la ruta de acceso apunta a un vínculo simbólico, se elimina el vínculo simbólico, no el destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-158">If the path points to a symbolic link, the symbolic link is deleted, not the target.</span></span> <span data-ttu-id="665bb-159">Para eliminar un destino, debe llamar a [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) y especificar **el \_ marcador \_ de archivo eliminar \_ al \_ cerrar**.</span><span class="sxs-lookup"><span data-stu-id="665bb-159">To delete a target, you must call [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) and specify **FILE\_FLAG\_DELETE\_ON\_CLOSE**.</span></span>

## <a name="findfirstchangenotification"></a><span data-ttu-id="665bb-160">FindFirstChangeNotification</span><span class="sxs-lookup"><span data-stu-id="665bb-160">FindFirstChangeNotification</span></span>

<span data-ttu-id="665bb-161">Si la ruta de acceso apunta a un vínculo simbólico, se crea el identificador de notificación para el destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-161">If the path points to a symbolic link, the notification handle is created for the target.</span></span> <span data-ttu-id="665bb-162">Si una aplicación se ha registrado para recibir notificaciones de cambio para un directorio que contiene vínculos simbólicos, solo se notificará a la aplicación cuando se hayan cambiado los vínculos simbólicos, no los archivos de destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-162">If an application has registered to receive change notifications for a directory that contains symbolic links, the application is only notified when the symbolic links have been changed, not the target files.</span></span>

## <a name="findfirstfile-and-findfirstfiletransacted"></a><span data-ttu-id="665bb-163">FindFirstFile y FindFirstFileTransacted</span><span class="sxs-lookup"><span data-stu-id="665bb-163">FindFirstFile and FindFirstFileTransacted</span></span>

<span data-ttu-id="665bb-164">Si la ruta de acceso apunta a un vínculo simbólico, el búfer de [**\_ \_ búsqueda de Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contiene información sobre el vínculo simbólico, no el destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-164">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="findfirstfileex"></a><span data-ttu-id="665bb-165">FindFirstFileEx</span><span class="sxs-lookup"><span data-stu-id="665bb-165">FindFirstFileEx</span></span>

<span data-ttu-id="665bb-166">Si la ruta de acceso apunta a un vínculo simbólico, el búfer de [**\_ \_ búsqueda de Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contiene información sobre el vínculo simbólico, no el destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-166">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="findnextfile"></a><span data-ttu-id="665bb-167">FindNextFile</span><span class="sxs-lookup"><span data-stu-id="665bb-167">FindNextFile</span></span>

<span data-ttu-id="665bb-168">Si la ruta de acceso apunta a un vínculo simbólico, el búfer de [**\_ \_ búsqueda de Win32**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) contiene información sobre el vínculo simbólico, no el destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-168">If the path points to a symbolic link, the [**WIN32\_FIND\_DATA**](/windows/desktop/api/MinWinBase/ns-minwinbase-win32_find_dataa) buffer contains information about the symbolic link, not the target.</span></span>

## <a name="getbinarytype"></a><span data-ttu-id="665bb-169">GetBinaryType</span><span class="sxs-lookup"><span data-stu-id="665bb-169">GetBinaryType</span></span>

<span data-ttu-id="665bb-170">Si la ruta de acceso apunta a un vínculo simbólico, se utiliza el archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-170">If the path points to a symbolic link, the target file is used.</span></span>

## <a name="getcompressedfilesize-and-getcompressedfilesizetransacted"></a><span data-ttu-id="665bb-171">GetCompressedFileSize y GetCompressedFileSizeTransacted</span><span class="sxs-lookup"><span data-stu-id="665bb-171">GetCompressedFileSize and GetCompressedFileSizeTransacted</span></span>

<span data-ttu-id="665bb-172">Si la ruta de acceso apunta a un vínculo simbólico, la función devuelve el tamaño del archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-172">If the path points to a symbolic link, the function returns the file size of the target.</span></span>

## <a name="getdiskfreespace"></a><span data-ttu-id="665bb-173">GetDiskFreeSpace</span><span class="sxs-lookup"><span data-stu-id="665bb-173">GetDiskFreeSpace</span></span>

<span data-ttu-id="665bb-174">Si la ruta de acceso apunta a un vínculo simbólico, la operación se realiza en el destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-174">If the path points to a symbolic link, the operation is performed on the target.</span></span>

## <a name="getdiskfreespaceex"></a><span data-ttu-id="665bb-175">GetDiskFreeSpaceEx</span><span class="sxs-lookup"><span data-stu-id="665bb-175">GetDiskFreeSpaceEx</span></span>

<span data-ttu-id="665bb-176">Si la ruta de acceso apunta a un vínculo simbólico, la operación se realiza en el destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-176">If the path points to a symbolic link, the operation is performed on the target.</span></span>

## <a name="getfileattributes"></a><span data-ttu-id="665bb-177">GetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="665bb-177">GetFileAttributes</span></span>

<span data-ttu-id="665bb-178">Si la ruta de acceso apunta a un vínculo simbólico, la función devuelve atributos para el vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="665bb-178">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="getfileattributesex"></a><span data-ttu-id="665bb-179">GetFileAttributesEx</span><span class="sxs-lookup"><span data-stu-id="665bb-179">GetFileAttributesEx</span></span>

<span data-ttu-id="665bb-180">Si la ruta de acceso apunta a un vínculo simbólico, la función devuelve atributos para el vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="665bb-180">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="getfilesecurity"></a><span data-ttu-id="665bb-181">GetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="665bb-181">GetFileSecurity</span></span>

<span data-ttu-id="665bb-182">Si la ruta de acceso apunta a un vínculo simbólico, la función devuelve atributos para el vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="665bb-182">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="gettemppath"></a><span data-ttu-id="665bb-183">GetTempPath</span><span class="sxs-lookup"><span data-stu-id="665bb-183">GetTempPath</span></span>

<span data-ttu-id="665bb-184">Si la ruta de acceso apunta a un vínculo simbólico, el nombre de la ruta de acceso temporal mantiene los vínculos simbólicos.</span><span class="sxs-lookup"><span data-stu-id="665bb-184">If the path points to a symbolic link, the temp path name maintains any symbolic links.</span></span>

## <a name="getvolumeinformation"></a><span data-ttu-id="665bb-185">GetVolumeInformation</span><span class="sxs-lookup"><span data-stu-id="665bb-185">GetVolumeInformation</span></span>

<span data-ttu-id="665bb-186">Si la ruta de acceso apunta a un vínculo simbólico, la función devuelve información del volumen para el destino.</span><span class="sxs-lookup"><span data-stu-id="665bb-186">If the path points to a symbolic link, the function returns volume information for the target.</span></span>

## <a name="setfileattributes"></a><span data-ttu-id="665bb-187">SetFileAttributes</span><span class="sxs-lookup"><span data-stu-id="665bb-187">SetFileAttributes</span></span>

<span data-ttu-id="665bb-188">Si la ruta de acceso apunta a un vínculo simbólico, la función recupera atributos para el vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="665bb-188">If the path points to a symbolic link, the function retrieves attributes for the symbolic link.</span></span>

## <a name="setfilesecurity"></a><span data-ttu-id="665bb-189">SetFileSecurity</span><span class="sxs-lookup"><span data-stu-id="665bb-189">SetFileSecurity</span></span>

<span data-ttu-id="665bb-190">Si la ruta de acceso apunta a un vínculo simbólico, la función devuelve atributos para el vínculo simbólico.</span><span class="sxs-lookup"><span data-stu-id="665bb-190">If the path points to a symbolic link, the function returns attributes for the symbolic link.</span></span>

## <a name="related-topics"></a><span data-ttu-id="665bb-191">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="665bb-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="665bb-192">**CopyFile**</span><span class="sxs-lookup"><span data-stu-id="665bb-192">**CopyFile**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfile)
</dt> <dt>

[<span data-ttu-id="665bb-193">**CopyFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="665bb-193">**CopyFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfiletransacteda)
</dt> <dt>

[<span data-ttu-id="665bb-194">**CopyFileEx**</span><span class="sxs-lookup"><span data-stu-id="665bb-194">**CopyFileEx**</span></span>](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
</dt> <dt>

[<span data-ttu-id="665bb-195">**CreateFile**</span><span class="sxs-lookup"><span data-stu-id="665bb-195">**CreateFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[<span data-ttu-id="665bb-196">**CreateFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="665bb-196">**CreateFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[<span data-ttu-id="665bb-197">**CreateHardLink**</span><span class="sxs-lookup"><span data-stu-id="665bb-197">**CreateHardLink**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createhardlinka)
</dt> <dt>

[<span data-ttu-id="665bb-198">**CreateHardLinkTransacted**</span><span class="sxs-lookup"><span data-stu-id="665bb-198">**CreateHardLinkTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-createhardlinktransacteda)
</dt> <dt>

[<span data-ttu-id="665bb-199">**DeleteFile**</span><span class="sxs-lookup"><span data-stu-id="665bb-199">**DeleteFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea)
</dt> <dt>

[<span data-ttu-id="665bb-200">**DeleteFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="665bb-200">**DeleteFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-deletefiletransacteda)
</dt> <dt>

[<span data-ttu-id="665bb-201">**FindFirstChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="665bb-201">**FindFirstChangeNotification**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstchangenotificationa)
</dt> <dt>

[<span data-ttu-id="665bb-202">**FindFirstFile**</span><span class="sxs-lookup"><span data-stu-id="665bb-202">**FindFirstFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfilea)
</dt> <dt>

[<span data-ttu-id="665bb-203">**FindFirstFileEx**</span><span class="sxs-lookup"><span data-stu-id="665bb-203">**FindFirstFileEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findfirstfileexa)
</dt> <dt>

[<span data-ttu-id="665bb-204">**FindFirstFileTransacted**</span><span class="sxs-lookup"><span data-stu-id="665bb-204">**FindFirstFileTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-findfirstfiletransacteda)
</dt> <dt>

[<span data-ttu-id="665bb-205">**FindNextFile**</span><span class="sxs-lookup"><span data-stu-id="665bb-205">**FindNextFile**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-findnextfilea)
</dt> <dt>

[<span data-ttu-id="665bb-206">**GetBinaryType**</span><span class="sxs-lookup"><span data-stu-id="665bb-206">**GetBinaryType**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getbinarytypea)
</dt> <dt>

[<span data-ttu-id="665bb-207">**GetCompressedFileSize**</span><span class="sxs-lookup"><span data-stu-id="665bb-207">**GetCompressedFileSize**</span></span>](/windows/desktop/api/fileapi/nf-fileapi-getcompressedfilesizea)
</dt> <dt>

[<span data-ttu-id="665bb-208">**GetCompressedFileSizeTransacted**</span><span class="sxs-lookup"><span data-stu-id="665bb-208">**GetCompressedFileSizeTransacted**</span></span>](/windows/desktop/api/WinBase/nf-winbase-getcompressedfilesizetransacteda)
</dt> <dt>

[<span data-ttu-id="665bb-209">**GetDiskFreeSpace**</span><span class="sxs-lookup"><span data-stu-id="665bb-209">**GetDiskFreeSpace**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespacea)
</dt> <dt>

[<span data-ttu-id="665bb-210">**GetDiskFreeSpaceEx**</span><span class="sxs-lookup"><span data-stu-id="665bb-210">**GetDiskFreeSpaceEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa)
</dt> <dt>

[<span data-ttu-id="665bb-211">**GetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="665bb-211">**GetFileAttributes**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[<span data-ttu-id="665bb-212">**GetFileAttributesEx**</span><span class="sxs-lookup"><span data-stu-id="665bb-212">**GetFileAttributesEx**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[<span data-ttu-id="665bb-213">**GetFileSecurity**</span><span class="sxs-lookup"><span data-stu-id="665bb-213">**GetFileSecurity**</span></span>](/windows/desktop/api/winbase/nf-winbase-getfilesecuritya)
</dt> <dt>

[<span data-ttu-id="665bb-214">**GetTempPath**</span><span class="sxs-lookup"><span data-stu-id="665bb-214">**GetTempPath**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-gettemppatha)
</dt> <dt>

[<span data-ttu-id="665bb-215">**GetVolumeInformation**</span><span class="sxs-lookup"><span data-stu-id="665bb-215">**GetVolumeInformation**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa)
</dt> <dt>

[<span data-ttu-id="665bb-216">**SetFileAttributes**</span><span class="sxs-lookup"><span data-stu-id="665bb-216">**SetFileAttributes**</span></span>](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[<span data-ttu-id="665bb-217">**SetFileSecurity**</span><span class="sxs-lookup"><span data-stu-id="665bb-217">**SetFileSecurity**</span></span>](/windows/desktop/api/winbase/nf-winbase-setfilesecuritya)
</dt> </dl>

 

 
