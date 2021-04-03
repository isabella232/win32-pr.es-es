---
description: Describe los códigos de error 0-499 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: cacb0aec-d438-4875-a96e-4e0239fdc6ba
title: Códigos de error del sistema (0-499) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 413d9674f511bd49df12267b60d6c6c3dac366aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907268"
---
# <a name="system-error-codes-0-499"></a><span data-ttu-id="d8867-103">Códigos de error del sistema (0-499)</span><span class="sxs-lookup"><span data-stu-id="d8867-103">System Error Codes (0-499)</span></span>

> [!NOTE]
> <span data-ttu-id="d8867-104">Esta información está destinada a los desarrolladores que depuran errores del sistema.</span><span class="sxs-lookup"><span data-stu-id="d8867-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="d8867-105">En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="d8867-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="d8867-106">En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) (errores 0 a 499).</span><span class="sxs-lookup"><span data-stu-id="d8867-106">The following list describes [system error codes](system-error-codes.md) (errors 0 to 499).</span></span> <span data-ttu-id="d8867-107">La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones.</span><span class="sxs-lookup"><span data-stu-id="d8867-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="d8867-108">Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.</span><span class="sxs-lookup"><span data-stu-id="d8867-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="d8867-109"><span id="ERROR_SUCCESS"></span><span id="error_success"></span>**ERROR \_ correcto**</span><span class="sxs-lookup"><span data-stu-id="d8867-109"><span id="ERROR_SUCCESS"></span><span id="error_success"></span>**ERROR\_SUCCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-110">0 (0X0)</span><span class="sxs-lookup"><span data-stu-id="d8867-110">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-111">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d8867-111">The operation completed successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-112"><span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**ERROR \_ de \_ función no válida**</span><span class="sxs-lookup"><span data-stu-id="d8867-112"><span id="ERROR_INVALID_FUNCTION"></span><span id="error_invalid_function"></span>**ERROR\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-113">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="d8867-113">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-114">Función incorrecta.</span><span class="sxs-lookup"><span data-stu-id="d8867-114">Incorrect function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-115"><span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**\_ \_ no \_ se encontró el archivo de error**</span><span class="sxs-lookup"><span data-stu-id="d8867-115"><span id="ERROR_FILE_NOT_FOUND"></span><span id="error_file_not_found"></span>**ERROR\_FILE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-116">2 (0X2)</span><span class="sxs-lookup"><span data-stu-id="d8867-116">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-117">El sistema no encuentra el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d8867-117">The system cannot find the file specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-118"><span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**\_ \_ no \_ se encontró la ruta de error**</span><span class="sxs-lookup"><span data-stu-id="d8867-118"><span id="ERROR_PATH_NOT_FOUND"></span><span id="error_path_not_found"></span>**ERROR\_PATH\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-119">3 (0X3)</span><span class="sxs-lookup"><span data-stu-id="d8867-119">3 (0x3)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-120">el sistema no encuentra la ruta especificada.</span><span class="sxs-lookup"><span data-stu-id="d8867-120">The system cannot find the path specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-121"><span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERROR \_ demasiados \_ \_ \_ archivos abiertos**</span><span class="sxs-lookup"><span data-stu-id="d8867-121"><span id="ERROR_TOO_MANY_OPEN_FILES"></span><span id="error_too_many_open_files"></span>**ERROR\_TOO\_MANY\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-122">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="d8867-122">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-123">El sistema no puede abrir el archivo.</span><span class="sxs-lookup"><span data-stu-id="d8867-123">The system cannot open the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-124"><span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERROR de \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="d8867-124"><span id="ERROR_ACCESS_DENIED"></span><span id="error_access_denied"></span>**ERROR\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-125">5 (0X5)</span><span class="sxs-lookup"><span data-stu-id="d8867-125">5 (0x5)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-126">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="d8867-126">Access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-127"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR \_ de \_ identificador no válido**</span><span class="sxs-lookup"><span data-stu-id="d8867-127"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-128">6 (0x6)</span><span class="sxs-lookup"><span data-stu-id="d8867-128">6 (0x6)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-129">El identificador no es válido.</span><span class="sxs-lookup"><span data-stu-id="d8867-129">The handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-130"><span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**ERROR de la \_ arena \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-130"><span id="ERROR_ARENA_TRASHED"></span><span id="error_arena_trashed"></span>**ERROR\_ARENA\_TRASHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-131">7 (0X7)</span><span class="sxs-lookup"><span data-stu-id="d8867-131">7 (0x7)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-132">Los bloques de control de almacenamiento se han destruido.</span><span class="sxs-lookup"><span data-stu-id="d8867-132">The storage control blocks were destroyed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-133"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR \_ de \_ memoria insuficiente \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-133"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-134">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="d8867-134">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-135">No hay recursos de memoria suficientes disponibles para procesar este comando.</span><span class="sxs-lookup"><span data-stu-id="d8867-135">Not enough memory resources are available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-136"><span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**ERROR \_ de \_ bloque no válido**</span><span class="sxs-lookup"><span data-stu-id="d8867-136"><span id="ERROR_INVALID_BLOCK"></span><span id="error_invalid_block"></span>**ERROR\_INVALID\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-137">9 (0x9)</span><span class="sxs-lookup"><span data-stu-id="d8867-137">9 (0x9)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-138">La dirección del bloque de control de almacenamiento no es válida.</span><span class="sxs-lookup"><span data-stu-id="d8867-138">The storage control block address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-139"><span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERROR \_ de \_ entorno incorrecto**</span><span class="sxs-lookup"><span data-stu-id="d8867-139"><span id="ERROR_BAD_ENVIRONMENT"></span><span id="error_bad_environment"></span>**ERROR\_BAD\_ENVIRONMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-140">10 (0xA)</span><span class="sxs-lookup"><span data-stu-id="d8867-140">10 (0xA)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-141">El entorno no es correcto.</span><span class="sxs-lookup"><span data-stu-id="d8867-141">The environment is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-142"><span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**ERROR \_ de \_ formato incorrecto**</span><span class="sxs-lookup"><span data-stu-id="d8867-142"><span id="ERROR_BAD_FORMAT"></span><span id="error_bad_format"></span>**ERROR\_BAD\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-143">11 (0xB)</span><span class="sxs-lookup"><span data-stu-id="d8867-143">11 (0xB)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-144">Se ha intentado cargar un programa con un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="d8867-144">An attempt was made to load a program with an incorrect format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-145"><span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERROR \_ de \_ acceso no válido**</span><span class="sxs-lookup"><span data-stu-id="d8867-145"><span id="ERROR_INVALID_ACCESS"></span><span id="error_invalid_access"></span>**ERROR\_INVALID\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-146">12 (0xC)</span><span class="sxs-lookup"><span data-stu-id="d8867-146">12 (0xC)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-147">El código de acceso no es válido.</span><span class="sxs-lookup"><span data-stu-id="d8867-147">The access code is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-148"><span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERROR de \_ datos no válidos \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-148"><span id="ERROR_INVALID_DATA"></span><span id="error_invalid_data"></span>**ERROR\_INVALID\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-149">13 (0xD)</span><span class="sxs-lookup"><span data-stu-id="d8867-149">13 (0xD)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-150">Los datos no son válidos.</span><span class="sxs-lookup"><span data-stu-id="d8867-150">The data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-151"><span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERROR \_ OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="d8867-151"><span id="ERROR_OUTOFMEMORY"></span><span id="error_outofmemory"></span>**ERROR\_OUTOFMEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-152">14 (0xE)</span><span class="sxs-lookup"><span data-stu-id="d8867-152">14 (0xE)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-153">No hay suficiente espacio de almacenamiento disponible para completar esta operación.</span><span class="sxs-lookup"><span data-stu-id="d8867-153">Not enough storage is available to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-154"><span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERROR \_ de \_ unidad no válida**</span><span class="sxs-lookup"><span data-stu-id="d8867-154"><span id="ERROR_INVALID_DRIVE"></span><span id="error_invalid_drive"></span>**ERROR\_INVALID\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-155">15 (0xF)</span><span class="sxs-lookup"><span data-stu-id="d8867-155">15 (0xF)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-156">El sistema no encuentra la unidad especificada.</span><span class="sxs-lookup"><span data-stu-id="d8867-156">The system cannot find the drive specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-157"><span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERROR en el \_ \_ directorio actual**</span><span class="sxs-lookup"><span data-stu-id="d8867-157"><span id="ERROR_CURRENT_DIRECTORY"></span><span id="error_current_directory"></span>**ERROR\_CURRENT\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-158">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="d8867-158">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-159">No se puede quitar el directorio.</span><span class="sxs-lookup"><span data-stu-id="d8867-159">The directory cannot be removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-160"><span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERROR \_ no es el \_ mismo \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="d8867-160"><span id="ERROR_NOT_SAME_DEVICE"></span><span id="error_not_same_device"></span>**ERROR\_NOT\_SAME\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-161">17 (0x11)</span><span class="sxs-lookup"><span data-stu-id="d8867-161">17 (0x11)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-162">El sistema no puede trasladar el archivo a una unidad de disco diferente.</span><span class="sxs-lookup"><span data-stu-id="d8867-162">The system cannot move the file to a different disk drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-163"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR: \_ no hay \_ más \_ archivos**</span><span class="sxs-lookup"><span data-stu-id="d8867-163"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-164">18 (0X12)</span><span class="sxs-lookup"><span data-stu-id="d8867-164">18 (0x12)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-165">No hay más archivos.</span><span class="sxs-lookup"><span data-stu-id="d8867-165">There are no more files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-166"><span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**ERROR \_ de \_ protección contra escritura**</span><span class="sxs-lookup"><span data-stu-id="d8867-166"><span id="ERROR_WRITE_PROTECT"></span><span id="error_write_protect"></span>**ERROR\_WRITE\_PROTECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-167">19 (0x13)</span><span class="sxs-lookup"><span data-stu-id="d8867-167">19 (0x13)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-168">El medio está protegido contra escritura.</span><span class="sxs-lookup"><span data-stu-id="d8867-168">The media is write protected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-169"><span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERROR \_ de \_ unidad incorrecta**</span><span class="sxs-lookup"><span data-stu-id="d8867-169"><span id="ERROR_BAD_UNIT"></span><span id="error_bad_unit"></span>**ERROR\_BAD\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-170">20 (0x14)</span><span class="sxs-lookup"><span data-stu-id="d8867-170">20 (0x14)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-171">El sistema no encuentra el dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d8867-171">The system cannot find the device specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-172"><span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERROR \_ no \_ preparado**</span><span class="sxs-lookup"><span data-stu-id="d8867-172"><span id="ERROR_NOT_READY"></span><span id="error_not_ready"></span>**ERROR\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-173">21 (0x15)</span><span class="sxs-lookup"><span data-stu-id="d8867-173">21 (0x15)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-174">El dispositivo no está listo.</span><span class="sxs-lookup"><span data-stu-id="d8867-174">The device is not ready.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-175"><span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERROR \_ de \_ comando incorrecto**</span><span class="sxs-lookup"><span data-stu-id="d8867-175"><span id="ERROR_BAD_COMMAND"></span><span id="error_bad_command"></span>**ERROR\_BAD\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-176">22 (0x16)</span><span class="sxs-lookup"><span data-stu-id="d8867-176">22 (0x16)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-177">El dispositivo no reconoce el comando.</span><span class="sxs-lookup"><span data-stu-id="d8867-177">The device does not recognize the command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-178"><span id="ERROR_CRC"></span><span id="error_crc"></span>**CRC de ERROR \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-178"><span id="ERROR_CRC"></span><span id="error_crc"></span>**ERROR\_CRC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-179">23 (0x17)</span><span class="sxs-lookup"><span data-stu-id="d8867-179">23 (0x17)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-180">Error de datos (comprobación de redundancia cíclica).</span><span class="sxs-lookup"><span data-stu-id="d8867-180">Data error (cyclic redundancy check).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-181"><span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERROR \_ de \_ longitud incorrecta**</span><span class="sxs-lookup"><span data-stu-id="d8867-181"><span id="ERROR_BAD_LENGTH"></span><span id="error_bad_length"></span>**ERROR\_BAD\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-182">24 (0x18)</span><span class="sxs-lookup"><span data-stu-id="d8867-182">24 (0x18)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-183">El programa emitió un comando pero la longitud del comando es incorrecta.</span><span class="sxs-lookup"><span data-stu-id="d8867-183">The program issued a command but the command length is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-184"><span id="ERROR_SEEK"></span><span id="error_seek"></span>**búsqueda de errores \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-184"><span id="ERROR_SEEK"></span><span id="error_seek"></span>**ERROR\_SEEK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-185">25 (0x19)</span><span class="sxs-lookup"><span data-stu-id="d8867-185">25 (0x19)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-186">La unidad no puede encontrar un área o un seguimiento específicos en el disco.</span><span class="sxs-lookup"><span data-stu-id="d8867-186">The drive cannot locate a specific area or track on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-187"><span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERROR \_ de \_ disco no dos \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-187"><span id="ERROR_NOT_DOS_DISK"></span><span id="error_not_dos_disk"></span>**ERROR\_NOT\_DOS\_DISK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-188">26 (0x1A)</span><span class="sxs-lookup"><span data-stu-id="d8867-188">26 (0x1A)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-189">No se puede tener acceso al disco o disquete especificado.</span><span class="sxs-lookup"><span data-stu-id="d8867-189">The specified disk or diskette cannot be accessed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-190"><span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**\_ \_ no \_ se encontró el sector de error**</span><span class="sxs-lookup"><span data-stu-id="d8867-190"><span id="ERROR_SECTOR_NOT_FOUND"></span><span id="error_sector_not_found"></span>**ERROR\_SECTOR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-191">27 (0x1B)</span><span class="sxs-lookup"><span data-stu-id="d8867-191">27 (0x1B)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-192">La unidad no puede encontrar el sector solicitado.</span><span class="sxs-lookup"><span data-stu-id="d8867-192">The drive cannot find the sector requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-193"><span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERROR \_ \_ de falta de \_ papel**</span><span class="sxs-lookup"><span data-stu-id="d8867-193"><span id="ERROR_OUT_OF_PAPER"></span><span id="error_out_of_paper"></span>**ERROR\_OUT\_OF\_PAPER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-194">28 (0x1C)</span><span class="sxs-lookup"><span data-stu-id="d8867-194">28 (0x1C)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-195">La impresora se ha quedado sin papel.</span><span class="sxs-lookup"><span data-stu-id="d8867-195">The printer is out of paper.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-196"><span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**ERROR de escritura de ERROR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-196"><span id="ERROR_WRITE_FAULT"></span><span id="error_write_fault"></span>**ERROR\_WRITE\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-197">29 (0x1D)</span><span class="sxs-lookup"><span data-stu-id="d8867-197">29 (0x1D)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-198">El sistema no puede escribir en el dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d8867-198">The system cannot write to the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-199"><span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**ERROR de lectura de ERROR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-199"><span id="ERROR_READ_FAULT"></span><span id="error_read_fault"></span>**ERROR\_READ\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-200">30 (0x1E)</span><span class="sxs-lookup"><span data-stu-id="d8867-200">30 (0x1E)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-201">El sistema no puede leer desde el dispositivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d8867-201">The system cannot read from the specified device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-202"><span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**ERROR de \_ gen. \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-202"><span id="ERROR_GEN_FAILURE"></span><span id="error_gen_failure"></span>**ERROR\_GEN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-203">31 (0x1F)</span><span class="sxs-lookup"><span data-stu-id="d8867-203">31 (0x1F)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-204">Un dispositivo conectado al sistema no funciona.</span><span class="sxs-lookup"><span data-stu-id="d8867-204">A device attached to the system is not functioning.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-205"><span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**infracción de \_ uso compartido de errores \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-205"><span id="ERROR_SHARING_VIOLATION"></span><span id="error_sharing_violation"></span>**ERROR\_SHARING\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-206">32 (0x20)</span><span class="sxs-lookup"><span data-stu-id="d8867-206">32 (0x20)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-207">El proceso no puede obtener acceso al archivo porque otro proceso lo está utilizando.</span><span class="sxs-lookup"><span data-stu-id="d8867-207">The process cannot access the file because it is being used by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-208"><span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**infracción de bloqueo de ERROR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-208"><span id="ERROR_LOCK_VIOLATION"></span><span id="error_lock_violation"></span>**ERROR\_LOCK\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-209">33 (0x21)</span><span class="sxs-lookup"><span data-stu-id="d8867-209">33 (0x21)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-210">El proceso no puede obtener acceso al archivo porque otro proceso ha bloqueado una parte de este.</span><span class="sxs-lookup"><span data-stu-id="d8867-210">The process cannot access the file because another process has locked a portion of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-211"><span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERROR \_ de \_ disco incorrecto**</span><span class="sxs-lookup"><span data-stu-id="d8867-211"><span id="ERROR_WRONG_DISK"></span><span id="error_wrong_disk"></span>**ERROR\_WRONG\_DISK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-212">34 (0x22)</span><span class="sxs-lookup"><span data-stu-id="d8867-212">34 (0x22)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-213">El disco incorrecto está en la unidad.</span><span class="sxs-lookup"><span data-stu-id="d8867-213">The wrong diskette is in the drive.</span></span> <span data-ttu-id="d8867-214">Inserte %2 (número de serie del volumen: %3) en la unidad %1.</span><span class="sxs-lookup"><span data-stu-id="d8867-214">Insert %2 (Volume Serial Number: %3) into drive %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-215"><span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**se \_ \_ superó el búfer de uso compartido de errores \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-215"><span id="ERROR_SHARING_BUFFER_EXCEEDED"></span><span id="error_sharing_buffer_exceeded"></span>**ERROR\_SHARING\_BUFFER\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-216">36 (0x24)</span><span class="sxs-lookup"><span data-stu-id="d8867-216">36 (0x24)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-217">Demasiados archivos abiertos para compartir.</span><span class="sxs-lookup"><span data-stu-id="d8867-217">Too many files opened for sharing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-218"><span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**ERROR de \_ control de \_ EOF**</span><span class="sxs-lookup"><span data-stu-id="d8867-218"><span id="ERROR_HANDLE_EOF"></span><span id="error_handle_eof"></span>**ERROR\_HANDLE\_EOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-219">38 (0x26)</span><span class="sxs-lookup"><span data-stu-id="d8867-219">38 (0x26)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-220">Llegó al final del archivo.</span><span class="sxs-lookup"><span data-stu-id="d8867-220">Reached the end of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-221"><span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**ERROR al \_ controlar el \_ disco \_ lleno**</span><span class="sxs-lookup"><span data-stu-id="d8867-221"><span id="ERROR_HANDLE_DISK_FULL"></span><span id="error_handle_disk_full"></span>**ERROR\_HANDLE\_DISK\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-222">39 (0x27)</span><span class="sxs-lookup"><span data-stu-id="d8867-222">39 (0x27)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-223">El disco está lleno.</span><span class="sxs-lookup"><span data-stu-id="d8867-223">The disk is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-224"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR \_ no \_ admitido**</span><span class="sxs-lookup"><span data-stu-id="d8867-224"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-225">50 (bajo la letra)</span><span class="sxs-lookup"><span data-stu-id="d8867-225">50 (0x32)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-226">No se admite la solicitud.</span><span class="sxs-lookup"><span data-stu-id="d8867-226">The request is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-227"><span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERROR \_ REM \_ no \_ lista**</span><span class="sxs-lookup"><span data-stu-id="d8867-227"><span id="ERROR_REM_NOT_LIST"></span><span id="error_rem_not_list"></span>**ERROR\_REM\_NOT\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-228">51 (0x33)</span><span class="sxs-lookup"><span data-stu-id="d8867-228">51 (0x33)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-229">Windows no puede encontrar la ruta de acceso de red.</span><span class="sxs-lookup"><span data-stu-id="d8867-229">Windows cannot find the network path.</span></span> <span data-ttu-id="d8867-230">Compruebe que la ruta de acceso de red es correcta y que el equipo de destino no está ocupado o desactivado.</span><span class="sxs-lookup"><span data-stu-id="d8867-230">Verify that the network path is correct and the destination computer is not busy or turned off.</span></span> <span data-ttu-id="d8867-231">Si Windows todavía no encuentra la ruta de acceso de red, póngase en contacto con el administrador de red.</span><span class="sxs-lookup"><span data-stu-id="d8867-231">If Windows still cannot find the network path, contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-232"><span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**ERROR \_ de \_ nombre DUP**</span><span class="sxs-lookup"><span data-stu-id="d8867-232"><span id="ERROR_DUP_NAME"></span><span id="error_dup_name"></span>**ERROR\_DUP\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-233">52 (0x34)</span><span class="sxs-lookup"><span data-stu-id="d8867-233">52 (0x34)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-234">No estaba conectado porque existe un nombre duplicado en la red.</span><span class="sxs-lookup"><span data-stu-id="d8867-234">You were not connected because a duplicate name exists on the network.</span></span> <span data-ttu-id="d8867-235">Si se une a un dominio, vaya a sistema en el panel de control para cambiar el nombre del equipo e inténtelo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="d8867-235">If joining a domain, go to System in Control Panel to change the computer name and try again.</span></span> <span data-ttu-id="d8867-236">Si se une a un grupo de trabajo, elija otro nombre de grupo de trabajo.</span><span class="sxs-lookup"><span data-stu-id="d8867-236">If joining a workgroup, choose another workgroup name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-237"><span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERROR \_ \_ NETPATH incorrecto**</span><span class="sxs-lookup"><span data-stu-id="d8867-237"><span id="ERROR_BAD_NETPATH"></span><span id="error_bad_netpath"></span>**ERROR\_BAD\_NETPATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-238">53 (0x35)</span><span class="sxs-lookup"><span data-stu-id="d8867-238">53 (0x35)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-239">No se ha encontrado la ruta de acceso de la red.</span><span class="sxs-lookup"><span data-stu-id="d8867-239">The network path was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-240"><span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERROR de \_ red \_ ocupada**</span><span class="sxs-lookup"><span data-stu-id="d8867-240"><span id="ERROR_NETWORK_BUSY"></span><span id="error_network_busy"></span>**ERROR\_NETWORK\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-241">54 (0x36)</span><span class="sxs-lookup"><span data-stu-id="d8867-241">54 (0x36)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-242">La red está ocupada.</span><span class="sxs-lookup"><span data-stu-id="d8867-242">The network is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-243"><span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**\_ \_ no existe el desarrollador de errores \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-243"><span id="ERROR_DEV_NOT_EXIST"></span><span id="error_dev_not_exist"></span>**ERROR\_DEV\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-244">55 (0x37)</span><span class="sxs-lookup"><span data-stu-id="d8867-244">55 (0x37)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-245">El recurso o el dispositivo de red especificado ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="d8867-245">The specified network resource or device is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-246"><span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERROR \_ demasiados comandos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-246"><span id="ERROR_TOO_MANY_CMDS"></span><span id="error_too_many_cmds"></span>**ERROR\_TOO\_MANY\_CMDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-247">56 (0x38)</span><span class="sxs-lookup"><span data-stu-id="d8867-247">56 (0x38)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-248">Se ha alcanzado el límite del comando de BIOS de red.</span><span class="sxs-lookup"><span data-stu-id="d8867-248">The network BIOS command limit has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-249"><span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERROR \_ ADAP \_ HDW \_ error**</span><span class="sxs-lookup"><span data-stu-id="d8867-249"><span id="ERROR_ADAP_HDW_ERR"></span><span id="error_adap_hdw_err"></span>**ERROR\_ADAP\_HDW\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-250">57 (0x39)</span><span class="sxs-lookup"><span data-stu-id="d8867-250">57 (0x39)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-251">Se ha producido un error de hardware en el adaptador de red.</span><span class="sxs-lookup"><span data-stu-id="d8867-251">A network adapter hardware error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-252"><span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERROR \_ de \_ net \_ resp**</span><span class="sxs-lookup"><span data-stu-id="d8867-252"><span id="ERROR_BAD_NET_RESP"></span><span id="error_bad_net_resp"></span>**ERROR\_BAD\_NET\_RESP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-253">58 (0x3A)</span><span class="sxs-lookup"><span data-stu-id="d8867-253">58 (0x3A)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-254">El servidor especificado no puede ejecutar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="d8867-254">The specified server cannot perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-255"><span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERROR \_ UNEXP \_ net \_ Err**</span><span class="sxs-lookup"><span data-stu-id="d8867-255"><span id="ERROR_UNEXP_NET_ERR"></span><span id="error_unexp_net_err"></span>**ERROR\_UNEXP\_NET\_ERR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-256">59 (0x3B)</span><span class="sxs-lookup"><span data-stu-id="d8867-256">59 (0x3B)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-257">Se produjo un error de red inesperado.</span><span class="sxs-lookup"><span data-stu-id="d8867-257">An unexpected network error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-258"><span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERROR \_ \_ PEND. \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-258"><span id="ERROR_BAD_REM_ADAP"></span><span id="error_bad_rem_adap"></span>**ERROR\_BAD\_REM\_ADAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-259">60 (0x3C)</span><span class="sxs-lookup"><span data-stu-id="d8867-259">60 (0x3C)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-260">El adaptador remoto no es compatible.</span><span class="sxs-lookup"><span data-stu-id="d8867-260">The remote adapter is not compatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-261"><span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERROR \_ PRINTQ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="d8867-261"><span id="ERROR_PRINTQ_FULL"></span><span id="error_printq_full"></span>**ERROR\_PRINTQ\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-262">61 (0x3D)</span><span class="sxs-lookup"><span data-stu-id="d8867-262">61 (0x3D)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-263">La cola de impresión está llena.</span><span class="sxs-lookup"><span data-stu-id="d8867-263">The printer queue is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-264"><span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERROR: \_ no hay \_ espacio en cola de impresión \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-264"><span id="ERROR_NO_SPOOL_SPACE"></span><span id="error_no_spool_space"></span>**ERROR\_NO\_SPOOL\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-265">62 (0x3E)</span><span class="sxs-lookup"><span data-stu-id="d8867-265">62 (0x3E)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-266">El espacio para almacenar el archivo en espera de ser impreso no está disponible en el servidor.</span><span class="sxs-lookup"><span data-stu-id="d8867-266">Space to store the file waiting to be printed is not available on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-267"><span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERROR de \_ impresión \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="d8867-267"><span id="ERROR_PRINT_CANCELLED"></span><span id="error_print_cancelled"></span>**ERROR\_PRINT\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-268">63 (0x3F)</span><span class="sxs-lookup"><span data-stu-id="d8867-268">63 (0x3F)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-269">El archivo en espera de ser impreso se ha eliminado.</span><span class="sxs-lookup"><span data-stu-id="d8867-269">Your file waiting to be printed was deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-270"><span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**se \_ eliminó el error de la \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-270"><span id="ERROR_NETNAME_DELETED"></span><span id="error_netname_deleted"></span>**ERROR\_NETNAME\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-271">64 (0x40)</span><span class="sxs-lookup"><span data-stu-id="d8867-271">64 (0x40)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-272">El nombre de red especificado ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="d8867-272">The specified network name is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-273"><span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERROR \_ de \_ acceso a la red \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="d8867-273"><span id="ERROR_NETWORK_ACCESS_DENIED"></span><span id="error_network_access_denied"></span>**ERROR\_NETWORK\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-274">65 (0x41)</span><span class="sxs-lookup"><span data-stu-id="d8867-274">65 (0x41)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-275">Se denegó el acceso a la red.</span><span class="sxs-lookup"><span data-stu-id="d8867-275">Network access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-276"><span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERROR \_ de \_ tipo de desarrollo incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-276"><span id="ERROR_BAD_DEV_TYPE"></span><span id="error_bad_dev_type"></span>**ERROR\_BAD\_DEV\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-277">66 (0x42)</span><span class="sxs-lookup"><span data-stu-id="d8867-277">66 (0x42)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-278">El tipo de recurso de red no es correcto.</span><span class="sxs-lookup"><span data-stu-id="d8867-278">The network resource type is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-279"><span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERROR \_ de \_ nombre de red incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-279"><span id="ERROR_BAD_NET_NAME"></span><span id="error_bad_net_name"></span>**ERROR\_BAD\_NET\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-280">67 (0X43)</span><span class="sxs-lookup"><span data-stu-id="d8867-280">67 (0x43)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-281">No se encuentra el nombre de red especificado.</span><span class="sxs-lookup"><span data-stu-id="d8867-281">The network name cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-282"><span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERROR \_ demasiados \_ \_ nombres**</span><span class="sxs-lookup"><span data-stu-id="d8867-282"><span id="ERROR_TOO_MANY_NAMES"></span><span id="error_too_many_names"></span>**ERROR\_TOO\_MANY\_NAMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-283">68 (0X44)</span><span class="sxs-lookup"><span data-stu-id="d8867-283">68 (0x44)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-284">Se superó el límite de nombres para la tarjeta de adaptador de red del equipo local.</span><span class="sxs-lookup"><span data-stu-id="d8867-284">The name limit for the local computer network adapter card was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-285"><span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERROR \_ demasiados \_ \_ SESS**</span><span class="sxs-lookup"><span data-stu-id="d8867-285"><span id="ERROR_TOO_MANY_SESS"></span><span id="error_too_many_sess"></span>**ERROR\_TOO\_MANY\_SESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-286">69 (0x45)</span><span class="sxs-lookup"><span data-stu-id="d8867-286">69 (0x45)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-287">Se superó el límite de sesión de BIOS de red.</span><span class="sxs-lookup"><span data-stu-id="d8867-287">The network BIOS session limit was exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-288"><span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**uso compartido de errores en \_ \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="d8867-288"><span id="ERROR_SHARING_PAUSED"></span><span id="error_sharing_paused"></span>**ERROR\_SHARING\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-289">70 (0x46)</span><span class="sxs-lookup"><span data-stu-id="d8867-289">70 (0x46)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-290">El servidor remoto se ha pausado o está en proceso de iniciarse.</span><span class="sxs-lookup"><span data-stu-id="d8867-290">The remote server has been paused or is in the process of being started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-291"><span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**ERROR \_ req \_ no \_ ACCEP**</span><span class="sxs-lookup"><span data-stu-id="d8867-291"><span id="ERROR_REQ_NOT_ACCEP"></span><span id="error_req_not_accep"></span>**ERROR\_REQ\_NOT\_ACCEP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-292">71 (0x47)</span><span class="sxs-lookup"><span data-stu-id="d8867-292">71 (0x47)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-293">No se pueden realizar más conexiones a este equipo remoto en este momento porque ya hay tantas conexiones como el equipo puede aceptar.</span><span class="sxs-lookup"><span data-stu-id="d8867-293">No more connections can be made to this remote computer at this time because there are already as many connections as the computer can accept.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-294"><span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**ERROR de \_ redir en \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="d8867-294"><span id="ERROR_REDIR_PAUSED"></span><span id="error_redir_paused"></span>**ERROR\_REDIR\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-295">72 (0x48)</span><span class="sxs-lookup"><span data-stu-id="d8867-295">72 (0x48)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-296">Se pausó la impresora o el dispositivo de disco especificado.</span><span class="sxs-lookup"><span data-stu-id="d8867-296">The specified printer or disk device has been paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-297"><span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**\_existe un archivo de error \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-297"><span id="ERROR_FILE_EXISTS"></span><span id="error_file_exists"></span>**ERROR\_FILE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-298">80 (0x50)</span><span class="sxs-lookup"><span data-stu-id="d8867-298">80 (0x50)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-299">El archivo ya existe.</span><span class="sxs-lookup"><span data-stu-id="d8867-299">The file exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-300"><span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**el ERROR \_ no se puede \_ hacer**</span><span class="sxs-lookup"><span data-stu-id="d8867-300"><span id="ERROR_CANNOT_MAKE"></span><span id="error_cannot_make"></span>**ERROR\_CANNOT\_MAKE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-301">82 (0x52)</span><span class="sxs-lookup"><span data-stu-id="d8867-301">82 (0x52)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-302">No se puede crear el directorio o el archivo.</span><span class="sxs-lookup"><span data-stu-id="d8867-302">The directory or file cannot be created.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-303"><span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERROR \_ \_ I24**</span><span class="sxs-lookup"><span data-stu-id="d8867-303"><span id="ERROR_FAIL_I24"></span><span id="error_fail_i24"></span>**ERROR\_FAIL\_I24**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-304">83 (0x53)</span><span class="sxs-lookup"><span data-stu-id="d8867-304">83 (0x53)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-305">Error en INT 24.</span><span class="sxs-lookup"><span data-stu-id="d8867-305">Fail on INT 24.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-306"><span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**ERROR \_ \_ de \_ estructuras**</span><span class="sxs-lookup"><span data-stu-id="d8867-306"><span id="ERROR_OUT_OF_STRUCTURES"></span><span id="error_out_of_structures"></span>**ERROR\_OUT\_OF\_STRUCTURES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-307">84 (0x54)</span><span class="sxs-lookup"><span data-stu-id="d8867-307">84 (0x54)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-308">El almacenamiento para procesar esta solicitud no está disponible.</span><span class="sxs-lookup"><span data-stu-id="d8867-308">Storage to process this request is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-309"><span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERROR \_ ya \_ asignado**</span><span class="sxs-lookup"><span data-stu-id="d8867-309"><span id="ERROR_ALREADY_ASSIGNED"></span><span id="error_already_assigned"></span>**ERROR\_ALREADY\_ASSIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-310">85 (0x55)</span><span class="sxs-lookup"><span data-stu-id="d8867-310">85 (0x55)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-311">El nombre del dispositivo local ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="d8867-311">The local device name is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-312"><span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**ERROR \_ de \_ contraseña no válida**</span><span class="sxs-lookup"><span data-stu-id="d8867-312"><span id="ERROR_INVALID_PASSWORD"></span><span id="error_invalid_password"></span>**ERROR\_INVALID\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-313">86 (0x56)</span><span class="sxs-lookup"><span data-stu-id="d8867-313">86 (0x56)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-314">La contraseña de red especificada no es correcta.</span><span class="sxs-lookup"><span data-stu-id="d8867-314">The specified network password is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-315"><span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**ERROR \_ de \_ parámetro no válido**</span><span class="sxs-lookup"><span data-stu-id="d8867-315"><span id="ERROR_INVALID_PARAMETER"></span><span id="error_invalid_parameter"></span>**ERROR\_INVALID\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-316">87 (0x57)</span><span class="sxs-lookup"><span data-stu-id="d8867-316">87 (0x57)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-317">El parámetro no es correcto.</span><span class="sxs-lookup"><span data-stu-id="d8867-317">The parameter is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-318"><span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**ERROR de ERROR de \_ escritura de net \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-318"><span id="ERROR_NET_WRITE_FAULT"></span><span id="error_net_write_fault"></span>**ERROR\_NET\_WRITE\_FAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-319">88 (0x58)</span><span class="sxs-lookup"><span data-stu-id="d8867-319">88 (0x58)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-320">Error de escritura en la red.</span><span class="sxs-lookup"><span data-stu-id="d8867-320">A write fault occurred on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-321"><span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**\_no hay \_ ranuras de procedimiento \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-321"><span id="ERROR_NO_PROC_SLOTS"></span><span id="error_no_proc_slots"></span>**ERROR\_NO\_PROC\_SLOTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-322">89 (0x59)</span><span class="sxs-lookup"><span data-stu-id="d8867-322">89 (0x59)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-323">El sistema no puede iniciar otro proceso en este momento.</span><span class="sxs-lookup"><span data-stu-id="d8867-323">The system cannot start another process at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-324"><span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERROR \_ demasiados \_ \_ semáforos**</span><span class="sxs-lookup"><span data-stu-id="d8867-324"><span id="ERROR_TOO_MANY_SEMAPHORES"></span><span id="error_too_many_semaphores"></span>**ERROR\_TOO\_MANY\_SEMAPHORES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-325">100 (0x64)</span><span class="sxs-lookup"><span data-stu-id="d8867-325">100 (0x64)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-326">No se puede crear otro semáforo de sistema.</span><span class="sxs-lookup"><span data-stu-id="d8867-326">Cannot create another system semaphore.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-327"><span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERROR \_ excl \_ SEM \_ ya es \_ propiedad**</span><span class="sxs-lookup"><span data-stu-id="d8867-327"><span id="ERROR_EXCL_SEM_ALREADY_OWNED"></span><span id="error_excl_sem_already_owned"></span>**ERROR\_EXCL\_SEM\_ALREADY\_OWNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-328">101 (0x65)</span><span class="sxs-lookup"><span data-stu-id="d8867-328">101 (0x65)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-329">El semáforo exclusivo es propiedad de otro proceso.</span><span class="sxs-lookup"><span data-stu-id="d8867-329">The exclusive semaphore is owned by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-330"><span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**ERROR \_ SEM \_ \_ establecido**</span><span class="sxs-lookup"><span data-stu-id="d8867-330"><span id="ERROR_SEM_IS_SET"></span><span id="error_sem_is_set"></span>**ERROR\_SEM\_IS\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-331">102 (0x66)</span><span class="sxs-lookup"><span data-stu-id="d8867-331">102 (0x66)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-332">El semáforo se establece y no se puede cerrar.</span><span class="sxs-lookup"><span data-stu-id="d8867-332">The semaphore is set and cannot be closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-333"><span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERROR \_ demasiadas \_ \_ solicitudes de SEM \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-333"><span id="ERROR_TOO_MANY_SEM_REQUESTS"></span><span id="error_too_many_sem_requests"></span>**ERROR\_TOO\_MANY\_SEM\_REQUESTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-334">103 (0x67)</span><span class="sxs-lookup"><span data-stu-id="d8867-334">103 (0x67)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-335">No se puede volver a establecer el semáforo.</span><span class="sxs-lookup"><span data-stu-id="d8867-335">The semaphore cannot be set again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-336"><span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERROR \_ no \_ válido \_ en \_ el momento de la interrupción**</span><span class="sxs-lookup"><span data-stu-id="d8867-336"><span id="ERROR_INVALID_AT_INTERRUPT_TIME"></span><span id="error_invalid_at_interrupt_time"></span>**ERROR\_INVALID\_AT\_INTERRUPT\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-337">104 (0x68)</span><span class="sxs-lookup"><span data-stu-id="d8867-337">104 (0x68)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-338">No se pueden solicitar semáforos exclusivos en el momento de la interrupción.</span><span class="sxs-lookup"><span data-stu-id="d8867-338">Cannot request exclusive semaphores at interrupt time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-339"><span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERROR \_ de \_ propietario de SEM \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-339"><span id="ERROR_SEM_OWNER_DIED"></span><span id="error_sem_owner_died"></span>**ERROR\_SEM\_OWNER\_DIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-340">105 (0x69)</span><span class="sxs-lookup"><span data-stu-id="d8867-340">105 (0x69)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-341">La propiedad anterior de este semáforo ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="d8867-341">The previous ownership of this semaphore has ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-342"><span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**\_límite de \_ usuarios de SEM de error \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-342"><span id="ERROR_SEM_USER_LIMIT"></span><span id="error_sem_user_limit"></span>**ERROR\_SEM\_USER\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-343">106 (0x6A)</span><span class="sxs-lookup"><span data-stu-id="d8867-343">106 (0x6A)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-344">Inserte el disco para la unidad %1.</span><span class="sxs-lookup"><span data-stu-id="d8867-344">Insert the diskette for drive %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-345"><span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**ERROR \_ al \_ cambiar el disco**</span><span class="sxs-lookup"><span data-stu-id="d8867-345"><span id="ERROR_DISK_CHANGE"></span><span id="error_disk_change"></span>**ERROR\_DISK\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-346">107 (0x6B)</span><span class="sxs-lookup"><span data-stu-id="d8867-346">107 (0x6B)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-347">El programa se detuvo porque no se insertó un disquete alternativo.</span><span class="sxs-lookup"><span data-stu-id="d8867-347">The program stopped because an alternate diskette was not inserted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-348"><span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**unidad de ERROR \_ \_ bloqueada**</span><span class="sxs-lookup"><span data-stu-id="d8867-348"><span id="ERROR_DRIVE_LOCKED"></span><span id="error_drive_locked"></span>**ERROR\_DRIVE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-349">108 (0x6C)</span><span class="sxs-lookup"><span data-stu-id="d8867-349">108 (0x6C)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-350">El disco está en uso o bloqueado por otro proceso.</span><span class="sxs-lookup"><span data-stu-id="d8867-350">The disk is in use or locked by another process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-351"><span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERROR \_ de \_ canalización interrumpida**</span><span class="sxs-lookup"><span data-stu-id="d8867-351"><span id="ERROR_BROKEN_PIPE"></span><span id="error_broken_pipe"></span>**ERROR\_BROKEN\_PIPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-352">109 (0x6D)</span><span class="sxs-lookup"><span data-stu-id="d8867-352">109 (0x6D)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-353">La canalización ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="d8867-353">The pipe has been ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-354"><span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**ERROR \_ al abrir el error \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-354"><span id="ERROR_OPEN_FAILED"></span><span id="error_open_failed"></span>**ERROR\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-355">110 (0x6E)</span><span class="sxs-lookup"><span data-stu-id="d8867-355">110 (0x6E)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-356">El sistema no puede abrir el dispositivo o el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d8867-356">The system cannot open the device or file specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-357"><span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**\_desbordamiento de búfer de error \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-357"><span id="ERROR_BUFFER_OVERFLOW"></span><span id="error_buffer_overflow"></span>**ERROR\_BUFFER\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-358">111 (0x6F)</span><span class="sxs-lookup"><span data-stu-id="d8867-358">111 (0x6F)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-359">El nombre de archivo es demasiado largo.</span><span class="sxs-lookup"><span data-stu-id="d8867-359">The file name is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-360"><span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**ERROR de \_ disco \_ lleno**</span><span class="sxs-lookup"><span data-stu-id="d8867-360"><span id="ERROR_DISK_FULL"></span><span id="error_disk_full"></span>**ERROR\_DISK\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-361">112 (0X70)</span><span class="sxs-lookup"><span data-stu-id="d8867-361">112 (0x70)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-362">There is not enough space on the disk.</span><span class="sxs-lookup"><span data-stu-id="d8867-362">There is not enough space on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-363"><span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERROR: \_ no hay \_ más \_ \_ identificadores de búsqueda**</span><span class="sxs-lookup"><span data-stu-id="d8867-363"><span id="ERROR_NO_MORE_SEARCH_HANDLES"></span><span id="error_no_more_search_handles"></span>**ERROR\_NO\_MORE\_SEARCH\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-364">113 (0x71)</span><span class="sxs-lookup"><span data-stu-id="d8867-364">113 (0x71)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-365">No hay más identificadores de archivo internos disponibles.</span><span class="sxs-lookup"><span data-stu-id="d8867-365">No more internal file identifiers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-366"><span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERROR \_ de \_ identificador de destino no válido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-366"><span id="ERROR_INVALID_TARGET_HANDLE"></span><span id="error_invalid_target_handle"></span>**ERROR\_INVALID\_TARGET\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-367">114 (0x72)</span><span class="sxs-lookup"><span data-stu-id="d8867-367">114 (0x72)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-368">El identificador de archivo interno de destino es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="d8867-368">The target internal file identifier is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-369"><span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**ERROR \_ de \_ categoría no válida**</span><span class="sxs-lookup"><span data-stu-id="d8867-369"><span id="ERROR_INVALID_CATEGORY"></span><span id="error_invalid_category"></span>**ERROR\_INVALID\_CATEGORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-370">117 (0x75)</span><span class="sxs-lookup"><span data-stu-id="d8867-370">117 (0x75)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-371">La llamada IOCTL realizada por el programa de la aplicación no es correcta.</span><span class="sxs-lookup"><span data-stu-id="d8867-371">The IOCTL call made by the application program is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-372"><span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERROR \_ al \_ \_ cambiar el modificador de comprobación**</span><span class="sxs-lookup"><span data-stu-id="d8867-372"><span id="ERROR_INVALID_VERIFY_SWITCH"></span><span id="error_invalid_verify_switch"></span>**ERROR\_INVALID\_VERIFY\_SWITCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-373">118 (0x76)</span><span class="sxs-lookup"><span data-stu-id="d8867-373">118 (0x76)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-374">El valor del parámetro de modificador de comprobación en escritura no es correcto.</span><span class="sxs-lookup"><span data-stu-id="d8867-374">The verify-on-write switch parameter value is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-375"><span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERROR \_ de \_ nivel de controlador incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-375"><span id="ERROR_BAD_DRIVER_LEVEL"></span><span id="error_bad_driver_level"></span>**ERROR\_BAD\_DRIVER\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-376">119 (0x77)</span><span class="sxs-lookup"><span data-stu-id="d8867-376">119 (0x77)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-377">El sistema no admite el comando solicitado.</span><span class="sxs-lookup"><span data-stu-id="d8867-377">The system does not support the command requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-378"><span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**llamada de ERROR \_ \_ no \_ implementada**</span><span class="sxs-lookup"><span data-stu-id="d8867-378"><span id="ERROR_CALL_NOT_IMPLEMENTED"></span><span id="error_call_not_implemented"></span>**ERROR\_CALL\_NOT\_IMPLEMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-379">120 (0x78)</span><span class="sxs-lookup"><span data-stu-id="d8867-379">120 (0x78)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-380">Esta función no es compatible con este sistema.</span><span class="sxs-lookup"><span data-stu-id="d8867-380">This function is not supported on this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-381"><span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**ERROR \_ de \_ tiempo de espera de SEM**</span><span class="sxs-lookup"><span data-stu-id="d8867-381"><span id="ERROR_SEM_TIMEOUT"></span><span id="error_sem_timeout"></span>**ERROR\_SEM\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-382">121 (0x79)</span><span class="sxs-lookup"><span data-stu-id="d8867-382">121 (0x79)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-383">Expiró el tiempo de espera del semáforo.</span><span class="sxs-lookup"><span data-stu-id="d8867-383">The semaphore timeout period has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-384"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR \_ de \_ búfer insuficiente**</span><span class="sxs-lookup"><span data-stu-id="d8867-384"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-385">122 (0x7A)</span><span class="sxs-lookup"><span data-stu-id="d8867-385">122 (0x7A)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-386">El área de datos que se pasa a una llamada del sistema es demasiado pequeña.</span><span class="sxs-lookup"><span data-stu-id="d8867-386">The data area passed to a system call is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-387"><span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**ERROR \_ de \_ nombre no válido**</span><span class="sxs-lookup"><span data-stu-id="d8867-387"><span id="ERROR_INVALID_NAME"></span><span id="error_invalid_name"></span>**ERROR\_INVALID\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-388">123 (0x7B)</span><span class="sxs-lookup"><span data-stu-id="d8867-388">123 (0x7B)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-389">El nombre de archivo, el nombre de directorio o la sintaxis de la etiqueta de volumen son incorrectos.</span><span class="sxs-lookup"><span data-stu-id="d8867-389">The filename, directory name, or volume label syntax is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-390"><span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**ERROR \_ de \_ nivel no válido**</span><span class="sxs-lookup"><span data-stu-id="d8867-390"><span id="ERROR_INVALID_LEVEL"></span><span id="error_invalid_level"></span>**ERROR\_INVALID\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-391">124 (0x7C)</span><span class="sxs-lookup"><span data-stu-id="d8867-391">124 (0x7C)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-392">El nivel de llamada del sistema no es correcto.</span><span class="sxs-lookup"><span data-stu-id="d8867-392">The system call level is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-393"><span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERROR: \_ no hay \_ etiqueta de volumen \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-393"><span id="ERROR_NO_VOLUME_LABEL"></span><span id="error_no_volume_label"></span>**ERROR\_NO\_VOLUME\_LABEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-394">125 (0x7D)</span><span class="sxs-lookup"><span data-stu-id="d8867-394">125 (0x7D)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-395">El disco no tiene etiqueta de volumen.</span><span class="sxs-lookup"><span data-stu-id="d8867-395">The disk has no volume label.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-396"><span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**ERROR \_ mod \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d8867-396"><span id="ERROR_MOD_NOT_FOUND"></span><span id="error_mod_not_found"></span>**ERROR\_MOD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-397">126 (0x7E)</span><span class="sxs-lookup"><span data-stu-id="d8867-397">126 (0x7E)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-398">No se pudo encontrar el módulo especificado.</span><span class="sxs-lookup"><span data-stu-id="d8867-398">The specified module could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-399"><span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**\_ \_ no \_ se encontró el procedimiento de error**</span><span class="sxs-lookup"><span data-stu-id="d8867-399"><span id="ERROR_PROC_NOT_FOUND"></span><span id="error_proc_not_found"></span>**ERROR\_PROC\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-400">127 (0x7F)</span><span class="sxs-lookup"><span data-stu-id="d8867-400">127 (0x7F)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-401">No se pudo encontrar el procedimiento especificado.</span><span class="sxs-lookup"><span data-stu-id="d8867-401">The specified procedure could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-402"><span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERROR de \_ espera \_ sin \_ elementos secundarios**</span><span class="sxs-lookup"><span data-stu-id="d8867-402"><span id="ERROR_WAIT_NO_CHILDREN"></span><span id="error_wait_no_children"></span>**ERROR\_WAIT\_NO\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-403">128 (0x80)</span><span class="sxs-lookup"><span data-stu-id="d8867-403">128 (0x80)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-404">No hay ningún proceso secundario que esperar.</span><span class="sxs-lookup"><span data-stu-id="d8867-404">There are no child processes to wait for.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-405"><span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**ERROR \_ secundario \_ no \_ completado**</span><span class="sxs-lookup"><span data-stu-id="d8867-405"><span id="ERROR_CHILD_NOT_COMPLETE"></span><span id="error_child_not_complete"></span>**ERROR\_CHILD\_NOT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-406">129 (0x81)</span><span class="sxs-lookup"><span data-stu-id="d8867-406">129 (0x81)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-407">La aplicación %1 no se puede ejecutar en modo Win32.</span><span class="sxs-lookup"><span data-stu-id="d8867-407">The %1 application cannot be run in Win32 mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-408"><span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**\_identificador de \_ acceso \_ directo de error**</span><span class="sxs-lookup"><span data-stu-id="d8867-408"><span id="ERROR_DIRECT_ACCESS_HANDLE"></span><span id="error_direct_access_handle"></span>**ERROR\_DIRECT\_ACCESS\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-409">130 (0x82)</span><span class="sxs-lookup"><span data-stu-id="d8867-409">130 (0x82)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-410">Intento de usar un identificador de archivo para una partición de disco abierta para una operación distinta de e/s de disco sin procesar.</span><span class="sxs-lookup"><span data-stu-id="d8867-410">Attempt to use a file handle to an open disk partition for an operation other than raw disk I/O.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-411"><span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**ERROR \_ de \_ búsqueda negativa**</span><span class="sxs-lookup"><span data-stu-id="d8867-411"><span id="ERROR_NEGATIVE_SEEK"></span><span id="error_negative_seek"></span>**ERROR\_NEGATIVE\_SEEK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-412">131 (0x83)</span><span class="sxs-lookup"><span data-stu-id="d8867-412">131 (0x83)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-413">Se intentó trasladar el puntero de archivo antes del principio del archivo.</span><span class="sxs-lookup"><span data-stu-id="d8867-413">An attempt was made to move the file pointer before the beginning of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-414"><span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**ERROR \_ \_ de búsqueda en el \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="d8867-414"><span id="ERROR_SEEK_ON_DEVICE"></span><span id="error_seek_on_device"></span>**ERROR\_SEEK\_ON\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-415">132 (0x84)</span><span class="sxs-lookup"><span data-stu-id="d8867-415">132 (0x84)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-416">No se puede establecer el puntero de archivo en el dispositivo o archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d8867-416">The file pointer cannot be set on the specified device or file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-417"><span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**el ERROR es el destino de la \_ \_ Unión \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-417"><span id="ERROR_IS_JOIN_TARGET"></span><span id="error_is_join_target"></span>**ERROR\_IS\_JOIN\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-418">133 (0x85)</span><span class="sxs-lookup"><span data-stu-id="d8867-418">133 (0x85)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-419">No se puede usar un comando JOIN o SUBSt para una unidad que contenga unidades Unidas previamente.</span><span class="sxs-lookup"><span data-stu-id="d8867-419">A JOIN or SUBST command cannot be used for a drive that contains previously joined drives.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-420"><span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**el ERROR \_ está \_ Unido**</span><span class="sxs-lookup"><span data-stu-id="d8867-420"><span id="ERROR_IS_JOINED"></span><span id="error_is_joined"></span>**ERROR\_IS\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-421">134 (0x86)</span><span class="sxs-lookup"><span data-stu-id="d8867-421">134 (0x86)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-422">Se intentó usar un comando JOIN o SUBSt en una unidad que ya se ha unido.</span><span class="sxs-lookup"><span data-stu-id="d8867-422">An attempt was made to use a JOIN or SUBST command on a drive that has already been joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-423"><span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**el ERROR \_ es \_ SUBSTED**</span><span class="sxs-lookup"><span data-stu-id="d8867-423"><span id="ERROR_IS_SUBSTED"></span><span id="error_is_substed"></span>**ERROR\_IS\_SUBSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-424">135 (0x87)</span><span class="sxs-lookup"><span data-stu-id="d8867-424">135 (0x87)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-425">Se intentó usar un comando JOIN o SUBSt en una unidad que ya se ha sustituido.</span><span class="sxs-lookup"><span data-stu-id="d8867-425">An attempt was made to use a JOIN or SUBST command on a drive that has already been substituted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-426"><span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERROR \_ no \_ Unido**</span><span class="sxs-lookup"><span data-stu-id="d8867-426"><span id="ERROR_NOT_JOINED"></span><span id="error_not_joined"></span>**ERROR\_NOT\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-427">136 (0x88)</span><span class="sxs-lookup"><span data-stu-id="d8867-427">136 (0x88)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-428">El sistema intentó eliminar la combinación de una unidad que no está unida.</span><span class="sxs-lookup"><span data-stu-id="d8867-428">The system tried to delete the JOIN of a drive that is not joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-429"><span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERROR \_ no \_ SUBSTED**</span><span class="sxs-lookup"><span data-stu-id="d8867-429"><span id="ERROR_NOT_SUBSTED"></span><span id="error_not_substed"></span>**ERROR\_NOT\_SUBSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-430">137 (0x89)</span><span class="sxs-lookup"><span data-stu-id="d8867-430">137 (0x89)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-431">El sistema intentó eliminar la sustitución de una unidad que no se sustituye.</span><span class="sxs-lookup"><span data-stu-id="d8867-431">The system tried to delete the substitution of a drive that is not substituted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-432"><span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**\_combinación \_ de errores para \_ unirse**</span><span class="sxs-lookup"><span data-stu-id="d8867-432"><span id="ERROR_JOIN_TO_JOIN"></span><span id="error_join_to_join"></span>**ERROR\_JOIN\_TO\_JOIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-433">138 (0x8A)</span><span class="sxs-lookup"><span data-stu-id="d8867-433">138 (0x8A)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-434">El sistema intentó unir una unidad a un directorio en una unidad unida.</span><span class="sxs-lookup"><span data-stu-id="d8867-434">The system tried to join a drive to a directory on a joined drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-435"><span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERROR \_ de SUBST \_ en \_ subst**</span><span class="sxs-lookup"><span data-stu-id="d8867-435"><span id="ERROR_SUBST_TO_SUBST"></span><span id="error_subst_to_subst"></span>**ERROR\_SUBST\_TO\_SUBST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-436">139 (0x8B)</span><span class="sxs-lookup"><span data-stu-id="d8867-436">139 (0x8B)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-437">El sistema intentó sustituir una unidad por un directorio en una unidad sustituida.</span><span class="sxs-lookup"><span data-stu-id="d8867-437">The system tried to substitute a drive to a directory on a substituted drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-438"><span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**ERROR \_ \_ al combinar con \_ subst**</span><span class="sxs-lookup"><span data-stu-id="d8867-438"><span id="ERROR_JOIN_TO_SUBST"></span><span id="error_join_to_subst"></span>**ERROR\_JOIN\_TO\_SUBST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-439">140 (0x8C)</span><span class="sxs-lookup"><span data-stu-id="d8867-439">140 (0x8C)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-440">El sistema intentó unir una unidad a un directorio en una unidad sustituida.</span><span class="sxs-lookup"><span data-stu-id="d8867-440">The system tried to join a drive to a directory on a substituted drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-441"><span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERROR \_ subst \_ a \_ join**</span><span class="sxs-lookup"><span data-stu-id="d8867-441"><span id="ERROR_SUBST_TO_JOIN"></span><span id="error_subst_to_join"></span>**ERROR\_SUBST\_TO\_JOIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-442">141 (0x8D)</span><span class="sxs-lookup"><span data-stu-id="d8867-442">141 (0x8D)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-443">El sistema intentó sustituir una unidad a un directorio en una unidad unida.</span><span class="sxs-lookup"><span data-stu-id="d8867-443">The system tried to SUBST a drive to a directory on a joined drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-444"><span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**ERROR \_ de \_ unidad ocupada**</span><span class="sxs-lookup"><span data-stu-id="d8867-444"><span id="ERROR_BUSY_DRIVE"></span><span id="error_busy_drive"></span>**ERROR\_BUSY\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-445">142 (0x8E)</span><span class="sxs-lookup"><span data-stu-id="d8867-445">142 (0x8E)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-446">El sistema no puede realizar una combinación o SUBSt en este momento.</span><span class="sxs-lookup"><span data-stu-id="d8867-446">The system cannot perform a JOIN or SUBST at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-447"><span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERROR en la \_ misma \_ unidad**</span><span class="sxs-lookup"><span data-stu-id="d8867-447"><span id="ERROR_SAME_DRIVE"></span><span id="error_same_drive"></span>**ERROR\_SAME\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-448">143 (0x8F)</span><span class="sxs-lookup"><span data-stu-id="d8867-448">143 (0x8F)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-449">El sistema no puede unir ni sustituir una unidad a o para un directorio de la misma unidad.</span><span class="sxs-lookup"><span data-stu-id="d8867-449">The system cannot join or substitute a drive to or for a directory on the same drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-450"><span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERROR de \_ directorio \_ no \_ raíz**</span><span class="sxs-lookup"><span data-stu-id="d8867-450"><span id="ERROR_DIR_NOT_ROOT"></span><span id="error_dir_not_root"></span>**ERROR\_DIR\_NOT\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-451">144 (0x90)</span><span class="sxs-lookup"><span data-stu-id="d8867-451">144 (0x90)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-452">El directorio no es un subdirectorio del directorio raíz.</span><span class="sxs-lookup"><span data-stu-id="d8867-452">The directory is not a subdirectory of the root directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-453"><span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**ERROR de \_ dir \_ no \_ vacío**</span><span class="sxs-lookup"><span data-stu-id="d8867-453"><span id="ERROR_DIR_NOT_EMPTY"></span><span id="error_dir_not_empty"></span>**ERROR\_DIR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-454">145 (0x91)</span><span class="sxs-lookup"><span data-stu-id="d8867-454">145 (0x91)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-455">El directorio no está vacío.</span><span class="sxs-lookup"><span data-stu-id="d8867-455">The directory is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-456"><span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**el ERROR \_ es \_ subst \_ path**</span><span class="sxs-lookup"><span data-stu-id="d8867-456"><span id="ERROR_IS_SUBST_PATH"></span><span id="error_is_subst_path"></span>**ERROR\_IS\_SUBST\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-457">146 (0x92)</span><span class="sxs-lookup"><span data-stu-id="d8867-457">146 (0x92)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-458">La ruta de acceso especificada se usa en un sustituto.</span><span class="sxs-lookup"><span data-stu-id="d8867-458">The path specified is being used in a substitute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-459"><span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**ERROR en la \_ \_ ruta de acceso de combinación \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-459"><span id="ERROR_IS_JOIN_PATH"></span><span id="error_is_join_path"></span>**ERROR\_IS\_JOIN\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-460">147 (0x93)</span><span class="sxs-lookup"><span data-stu-id="d8867-460">147 (0x93)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-461">No hay suficientes recursos disponibles para procesar este comando.</span><span class="sxs-lookup"><span data-stu-id="d8867-461">Not enough resources are available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-462"><span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**Ruta de acceso de ERROR \_ \_ ocupada**</span><span class="sxs-lookup"><span data-stu-id="d8867-462"><span id="ERROR_PATH_BUSY"></span><span id="error_path_busy"></span>**ERROR\_PATH\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-463">148 (0x94)</span><span class="sxs-lookup"><span data-stu-id="d8867-463">148 (0x94)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-464">La ruta de acceso especificada no se puede usar en este momento.</span><span class="sxs-lookup"><span data-stu-id="d8867-464">The path specified cannot be used at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-465"><span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**el ERROR \_ es el \_ destino de SUBST \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-465"><span id="ERROR_IS_SUBST_TARGET"></span><span id="error_is_subst_target"></span>**ERROR\_IS\_SUBST\_TARGET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-466">149 (0x95)</span><span class="sxs-lookup"><span data-stu-id="d8867-466">149 (0x95)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-467">Se intentó unir o sustituir una unidad para la que un directorio de la unidad es el destino de un sustituto anterior.</span><span class="sxs-lookup"><span data-stu-id="d8867-467">An attempt was made to join or substitute a drive for which a directory on the drive is the target of a previous substitute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-468"><span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**\_seguimiento del sistema de errores \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-468"><span id="ERROR_SYSTEM_TRACE"></span><span id="error_system_trace"></span>**ERROR\_SYSTEM\_TRACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-469">150 (0x96)</span><span class="sxs-lookup"><span data-stu-id="d8867-469">150 (0x96)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-470">No se especificó la información de seguimiento del sistema en el archivo de CONFIG.SYS o no se permite el seguimiento.</span><span class="sxs-lookup"><span data-stu-id="d8867-470">System trace information was not specified in your CONFIG.SYS file, or tracing is disallowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-471"><span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**ERROR \_ al \_ recuento de eventos no válidos \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-471"><span id="ERROR_INVALID_EVENT_COUNT"></span><span id="error_invalid_event_count"></span>**ERROR\_INVALID\_EVENT\_COUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-472">151 (0x97)</span><span class="sxs-lookup"><span data-stu-id="d8867-472">151 (0x97)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-473">El número de eventos de semáforo especificados para DosMuxSemWait no es correcto.</span><span class="sxs-lookup"><span data-stu-id="d8867-473">The number of specified semaphore events for DosMuxSemWait is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-474"><span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERROR \_ demasiados \_ \_ MUXWAITERS**</span><span class="sxs-lookup"><span data-stu-id="d8867-474"><span id="ERROR_TOO_MANY_MUXWAITERS"></span><span id="error_too_many_muxwaiters"></span>**ERROR\_TOO\_MANY\_MUXWAITERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-475">152 (0x98)</span><span class="sxs-lookup"><span data-stu-id="d8867-475">152 (0x98)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-476">No se ejecutó DosMuxSemWait; ya se han establecido demasiados semáforos.</span><span class="sxs-lookup"><span data-stu-id="d8867-476">DosMuxSemWait did not execute; too many semaphores are already set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-477"><span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**ERROR \_ de \_ formato de lista no válido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-477"><span id="ERROR_INVALID_LIST_FORMAT"></span><span id="error_invalid_list_format"></span>**ERROR\_INVALID\_LIST\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-478">153 (0x99)</span><span class="sxs-lookup"><span data-stu-id="d8867-478">153 (0x99)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-479">La lista de DosMuxSemWait no es correcta.</span><span class="sxs-lookup"><span data-stu-id="d8867-479">The DosMuxSemWait list is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-480"><span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**etiqueta de ERROR \_ \_ demasiado \_ larga**</span><span class="sxs-lookup"><span data-stu-id="d8867-480"><span id="ERROR_LABEL_TOO_LONG"></span><span id="error_label_too_long"></span>**ERROR\_LABEL\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-481">154 (0x9A)</span><span class="sxs-lookup"><span data-stu-id="d8867-481">154 (0x9A)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-482">La etiqueta de volumen especificada supera el límite de caracteres de etiqueta del sistema de archivos de destino.</span><span class="sxs-lookup"><span data-stu-id="d8867-482">The volume label you entered exceeds the label character limit of the target file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-483"><span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERROR \_ demasiados \_ \_ TCBS**</span><span class="sxs-lookup"><span data-stu-id="d8867-483"><span id="ERROR_TOO_MANY_TCBS"></span><span id="error_too_many_tcbs"></span>**ERROR\_TOO\_MANY\_TCBS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-484">155 (0x9B)</span><span class="sxs-lookup"><span data-stu-id="d8867-484">155 (0x9B)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-485">No se puede crear otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="d8867-485">Cannot create another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-486"><span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**señal de ERROR \_ \_ rechazada**</span><span class="sxs-lookup"><span data-stu-id="d8867-486"><span id="ERROR_SIGNAL_REFUSED"></span><span id="error_signal_refused"></span>**ERROR\_SIGNAL\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-487">156 (0x9C)</span><span class="sxs-lookup"><span data-stu-id="d8867-487">156 (0x9C)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-488">El proceso del destinatario ha rechazado la señal.</span><span class="sxs-lookup"><span data-stu-id="d8867-488">The recipient process has refused the signal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-489"><span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERROR \_ DEScartado**</span><span class="sxs-lookup"><span data-stu-id="d8867-489"><span id="ERROR_DISCARDED"></span><span id="error_discarded"></span>**ERROR\_DISCARDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-490">157 (0x9D)</span><span class="sxs-lookup"><span data-stu-id="d8867-490">157 (0x9D)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-491">El segmento ya se ha descartado y no se puede bloquear.</span><span class="sxs-lookup"><span data-stu-id="d8867-491">The segment is already discarded and cannot be locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-492"><span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERROR \_ no \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="d8867-492"><span id="ERROR_NOT_LOCKED"></span><span id="error_not_locked"></span>**ERROR\_NOT\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-493">158 (0x9E)</span><span class="sxs-lookup"><span data-stu-id="d8867-493">158 (0x9E)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-494">El segmento ya está desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="d8867-494">The segment is already unlocked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-495"><span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ERROR \_ de \_ THREADID erróneo \_ addr**</span><span class="sxs-lookup"><span data-stu-id="d8867-495"><span id="ERROR_BAD_THREADID_ADDR"></span><span id="error_bad_threadid_addr"></span>**ERROR\_BAD\_THREADID\_ADDR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-496">159 (0x9F)</span><span class="sxs-lookup"><span data-stu-id="d8867-496">159 (0x9F)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-497">La dirección para el ID. de subproceso no es correcta.</span><span class="sxs-lookup"><span data-stu-id="d8867-497">The address for the thread ID is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-498"><span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERROR de \_ argumentos no válidos \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-498"><span id="ERROR_BAD_ARGUMENTS"></span><span id="error_bad_arguments"></span>**ERROR\_BAD\_ARGUMENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-499">160 (0xA0)</span><span class="sxs-lookup"><span data-stu-id="d8867-499">160 (0xA0)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-500">Uno o varios argumentos no son correctos.</span><span class="sxs-lookup"><span data-stu-id="d8867-500">One or more arguments are not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-501"><span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERROR \_ de \_ ruta de nombres incorrecta**</span><span class="sxs-lookup"><span data-stu-id="d8867-501"><span id="ERROR_BAD_PATHNAME"></span><span id="error_bad_pathname"></span>**ERROR\_BAD\_PATHNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-502">161 (0xA1)</span><span class="sxs-lookup"><span data-stu-id="d8867-502">161 (0xA1)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-503">La ruta de acceso especificada no es válida.</span><span class="sxs-lookup"><span data-stu-id="d8867-503">The specified path is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-504"><span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**señal de ERROR \_ \_ pendiente**</span><span class="sxs-lookup"><span data-stu-id="d8867-504"><span id="ERROR_SIGNAL_PENDING"></span><span id="error_signal_pending"></span>**ERROR\_SIGNAL\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-505">162 (0xA2)</span><span class="sxs-lookup"><span data-stu-id="d8867-505">162 (0xA2)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-506">Ya hay una señal pendiente.</span><span class="sxs-lookup"><span data-stu-id="d8867-506">A signal is already pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-507"><span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERROR \_ máximo \_ THRDS \_ alcanzado**</span><span class="sxs-lookup"><span data-stu-id="d8867-507"><span id="ERROR_MAX_THRDS_REACHED"></span><span id="error_max_thrds_reached"></span>**ERROR\_MAX\_THRDS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-508">164 (0xA4)</span><span class="sxs-lookup"><span data-stu-id="d8867-508">164 (0xA4)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-509">No se pueden crear más subprocesos en el sistema.</span><span class="sxs-lookup"><span data-stu-id="d8867-509">No more threads can be created in the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-510"><span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**error de bloqueo de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-510"><span id="ERROR_LOCK_FAILED"></span><span id="error_lock_failed"></span>**ERROR\_LOCK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-511">167 (0xA7)</span><span class="sxs-lookup"><span data-stu-id="d8867-511">167 (0xA7)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-512">No se puede bloquear una región de un archivo.</span><span class="sxs-lookup"><span data-stu-id="d8867-512">Unable to lock a region of a file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-513"><span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERROR \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="d8867-513"><span id="ERROR_BUSY"></span><span id="error_busy"></span>**ERROR\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-514">170 (0xAA)</span><span class="sxs-lookup"><span data-stu-id="d8867-514">170 (0xAA)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-515">El recurso solicitado está en uso.</span><span class="sxs-lookup"><span data-stu-id="d8867-515">The requested resource is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-516"><span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**ERROR \_ \_ de compatibilidad \_ del dispositivo en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="d8867-516"><span id="ERROR_DEVICE_SUPPORT_IN_PROGRESS"></span><span id="error_device_support_in_progress"></span>**ERROR\_DEVICE\_SUPPORT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-517">171 (0xAB)</span><span class="sxs-lookup"><span data-stu-id="d8867-517">171 (0xAB)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-518">La detección de la compatibilidad del comando del dispositivo está en curso.</span><span class="sxs-lookup"><span data-stu-id="d8867-518">Device's command support detection is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-519"><span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERROR de \_ cancelación de \_ infracción**</span><span class="sxs-lookup"><span data-stu-id="d8867-519"><span id="ERROR_CANCEL_VIOLATION"></span><span id="error_cancel_violation"></span>**ERROR\_CANCEL\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-520">173 (0xAD)</span><span class="sxs-lookup"><span data-stu-id="d8867-520">173 (0xAD)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-521">No había una solicitud de bloqueo pendiente para la región de cancelación proporcionada.</span><span class="sxs-lookup"><span data-stu-id="d8867-521">A lock request was not outstanding for the supplied cancel region.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-522"><span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERROR \_ de \_ bloqueos atómicos \_ no \_ admitidos**</span><span class="sxs-lookup"><span data-stu-id="d8867-522"><span id="ERROR_ATOMIC_LOCKS_NOT_SUPPORTED"></span><span id="error_atomic_locks_not_supported"></span>**ERROR\_ATOMIC\_LOCKS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-523">174 (0xAE)</span><span class="sxs-lookup"><span data-stu-id="d8867-523">174 (0xAE)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-524">El sistema de archivos no admite cambios atómicos en el tipo de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="d8867-524">The file system does not support atomic changes to the lock type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-525"><span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**ERROR \_ de \_ número de segmento no válido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-525"><span id="ERROR_INVALID_SEGMENT_NUMBER"></span><span id="error_invalid_segment_number"></span>**ERROR\_INVALID\_SEGMENT\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-526">180 (0xB4)</span><span class="sxs-lookup"><span data-stu-id="d8867-526">180 (0xB4)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-527">El sistema detectó un número de segmento que no era correcto.</span><span class="sxs-lookup"><span data-stu-id="d8867-527">The system detected a segment number that was not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-528"><span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERROR \_ ordinal no válido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-528"><span id="ERROR_INVALID_ORDINAL"></span><span id="error_invalid_ordinal"></span>**ERROR\_INVALID\_ORDINAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-529">182 (0xB6)</span><span class="sxs-lookup"><span data-stu-id="d8867-529">182 (0xB6)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-530">El sistema operativo no puede ejecutar %1.</span><span class="sxs-lookup"><span data-stu-id="d8867-530">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-531"><span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**el ERROR \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="d8867-531"><span id="ERROR_ALREADY_EXISTS"></span><span id="error_already_exists"></span>**ERROR\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-532">183 (0xB7)</span><span class="sxs-lookup"><span data-stu-id="d8867-532">183 (0xB7)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-533">No se puede crear un archivo que ya existe.</span><span class="sxs-lookup"><span data-stu-id="d8867-533">Cannot create a file when that file already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-534"><span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERROR \_ de \_ número de marca no válido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-534"><span id="ERROR_INVALID_FLAG_NUMBER"></span><span id="error_invalid_flag_number"></span>**ERROR\_INVALID\_FLAG\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-535">186 (0xBA)</span><span class="sxs-lookup"><span data-stu-id="d8867-535">186 (0xBA)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-536">La marca pasada no es correcta.</span><span class="sxs-lookup"><span data-stu-id="d8867-536">The flag passed is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-537"><span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERROR \_ SEM \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d8867-537"><span id="ERROR_SEM_NOT_FOUND"></span><span id="error_sem_not_found"></span>**ERROR\_SEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-538">187 (0xBB)</span><span class="sxs-lookup"><span data-stu-id="d8867-538">187 (0xBB)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-539">No se encontró el nombre del semáforo del sistema especificado.</span><span class="sxs-lookup"><span data-stu-id="d8867-539">The specified system semaphore name was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-540"><span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**ERROR \_ de \_ Inicio de CODESEG no válido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-540"><span id="ERROR_INVALID_STARTING_CODESEG"></span><span id="error_invalid_starting_codeseg"></span>**ERROR\_INVALID\_STARTING\_CODESEG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-541">188 (0xBC)</span><span class="sxs-lookup"><span data-stu-id="d8867-541">188 (0xBC)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-542">El sistema operativo no puede ejecutar %1.</span><span class="sxs-lookup"><span data-stu-id="d8867-542">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-543"><span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERROR \_ STACKSEG no válido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-543"><span id="ERROR_INVALID_STACKSEG"></span><span id="error_invalid_stackseg"></span>**ERROR\_INVALID\_STACKSEG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-544">189 (0xBD)</span><span class="sxs-lookup"><span data-stu-id="d8867-544">189 (0xBD)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-545">El sistema operativo no puede ejecutar %1.</span><span class="sxs-lookup"><span data-stu-id="d8867-545">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-546"><span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERROR \_ de \_ MODULETYPE no válido**</span><span class="sxs-lookup"><span data-stu-id="d8867-546"><span id="ERROR_INVALID_MODULETYPE"></span><span id="error_invalid_moduletype"></span>**ERROR\_INVALID\_MODULETYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-547">190 (0xBE)</span><span class="sxs-lookup"><span data-stu-id="d8867-547">190 (0xBE)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-548">El sistema operativo no puede ejecutar %1.</span><span class="sxs-lookup"><span data-stu-id="d8867-548">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-549"><span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERROR \_ de \_ firma exe no válida \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-549"><span id="ERROR_INVALID_EXE_SIGNATURE"></span><span id="error_invalid_exe_signature"></span>**ERROR\_INVALID\_EXE\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-550">191 (0xBF)</span><span class="sxs-lookup"><span data-stu-id="d8867-550">191 (0xBF)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-551">No se puede ejecutar %1 en modo Win32.</span><span class="sxs-lookup"><span data-stu-id="d8867-551">Cannot run %1 in Win32 mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-552"><span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERROR \_ exe \_ marcado como \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="d8867-552"><span id="ERROR_EXE_MARKED_INVALID"></span><span id="error_exe_marked_invalid"></span>**ERROR\_EXE\_MARKED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-553">192 (0xC0)</span><span class="sxs-lookup"><span data-stu-id="d8867-553">192 (0xC0)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-554">El sistema operativo no puede ejecutar %1.</span><span class="sxs-lookup"><span data-stu-id="d8867-554">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-555"><span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERROR \_ de \_ formato exe incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-555"><span id="ERROR_BAD_EXE_FORMAT"></span><span id="error_bad_exe_format"></span>**ERROR\_BAD\_EXE\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-556">193 (0xC1)</span><span class="sxs-lookup"><span data-stu-id="d8867-556">193 (0xC1)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-557">%1 no es una aplicación Win32 válida.</span><span class="sxs-lookup"><span data-stu-id="d8867-557">%1 is not a valid Win32 application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-558"><span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**Los \_ datos iterados de error \_ \_ superan \_ 64k**</span><span class="sxs-lookup"><span data-stu-id="d8867-558"><span id="ERROR_ITERATED_DATA_EXCEEDS_64k"></span><span id="error_iterated_data_exceeds_64k"></span><span id="ERROR_ITERATED_DATA_EXCEEDS_64K"></span>**ERROR\_ITERATED\_DATA\_EXCEEDS\_64k**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-559">194 (0xC2)</span><span class="sxs-lookup"><span data-stu-id="d8867-559">194 (0xC2)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-560">El sistema operativo no puede ejecutar %1.</span><span class="sxs-lookup"><span data-stu-id="d8867-560">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-561"><span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERROR \_ MINALLOCSIZE no válido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-561"><span id="ERROR_INVALID_MINALLOCSIZE"></span><span id="error_invalid_minallocsize"></span>**ERROR\_INVALID\_MINALLOCSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-562">195 (0xC3)</span><span class="sxs-lookup"><span data-stu-id="d8867-562">195 (0xC3)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-563">El sistema operativo no puede ejecutar %1.</span><span class="sxs-lookup"><span data-stu-id="d8867-563">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-564"><span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERROR \_ DYNLINK \_ del \_ anillo no válido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-564"><span id="ERROR_DYNLINK_FROM_INVALID_RING"></span><span id="error_dynlink_from_invalid_ring"></span>**ERROR\_DYNLINK\_FROM\_INVALID\_RING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-565">196 (0xC4)</span><span class="sxs-lookup"><span data-stu-id="d8867-565">196 (0xC4)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-566">El sistema operativo no puede ejecutar este programa de aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8867-566">The operating system cannot run this application program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-567"><span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERROR \_ IOPL \_ no \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="d8867-567"><span id="ERROR_IOPL_NOT_ENABLED"></span><span id="error_iopl_not_enabled"></span>**ERROR\_IOPL\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-568">197 (0xC5)</span><span class="sxs-lookup"><span data-stu-id="d8867-568">197 (0xC5)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-569">El sistema operativo no está configurado actualmente para ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8867-569">The operating system is not presently configured to run this application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-570"><span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERROR \_ SEGDPL no válido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-570"><span id="ERROR_INVALID_SEGDPL"></span><span id="error_invalid_segdpl"></span>**ERROR\_INVALID\_SEGDPL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-571">198 (0xC6)</span><span class="sxs-lookup"><span data-stu-id="d8867-571">198 (0xC6)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-572">El sistema operativo no puede ejecutar %1.</span><span class="sxs-lookup"><span data-stu-id="d8867-572">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-573"><span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**El ERROR \_ AUTODATASEG \_ supera \_ 64k**</span><span class="sxs-lookup"><span data-stu-id="d8867-573"><span id="ERROR_AUTODATASEG_EXCEEDS_64k"></span><span id="error_autodataseg_exceeds_64k"></span><span id="ERROR_AUTODATASEG_EXCEEDS_64K"></span>**ERROR\_AUTODATASEG\_EXCEEDS\_64k**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-574">199 (0xC7)</span><span class="sxs-lookup"><span data-stu-id="d8867-574">199 (0xC7)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-575">El sistema operativo no puede ejecutar este programa de aplicación.</span><span class="sxs-lookup"><span data-stu-id="d8867-575">The operating system cannot run this application program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-576"><span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**El ERROR \_ RING2SEG \_ debe \_ ser \_ movible**</span><span class="sxs-lookup"><span data-stu-id="d8867-576"><span id="ERROR_RING2SEG_MUST_BE_MOVABLE"></span><span id="error_ring2seg_must_be_movable"></span>**ERROR\_RING2SEG\_MUST\_BE\_MOVABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-577">200 (0xC8)</span><span class="sxs-lookup"><span data-stu-id="d8867-577">200 (0xC8)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-578">El segmento de código no puede ser mayor o igual que 64K.</span><span class="sxs-lookup"><span data-stu-id="d8867-578">The code segment cannot be greater than or equal to 64K.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-579"><span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERROR \_ reloc \_ cadena \_ XEEDS \_ SEGLIM**</span><span class="sxs-lookup"><span data-stu-id="d8867-579"><span id="ERROR_RELOC_CHAIN_XEEDS_SEGLIM"></span><span id="error_reloc_chain_xeeds_seglim"></span>**ERROR\_RELOC\_CHAIN\_XEEDS\_SEGLIM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-580">201 (0xC9)</span><span class="sxs-lookup"><span data-stu-id="d8867-580">201 (0xC9)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-581">El sistema operativo no puede ejecutar %1.</span><span class="sxs-lookup"><span data-stu-id="d8867-581">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-582"><span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERROR \_ INFLOOP \_ en \_ la \_ cadena reloc**</span><span class="sxs-lookup"><span data-stu-id="d8867-582"><span id="ERROR_INFLOOP_IN_RELOC_CHAIN"></span><span id="error_infloop_in_reloc_chain"></span>**ERROR\_INFLOOP\_IN\_RELOC\_CHAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-583">202 (0xCA)</span><span class="sxs-lookup"><span data-stu-id="d8867-583">202 (0xCA)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-584">El sistema operativo no puede ejecutar %1.</span><span class="sxs-lookup"><span data-stu-id="d8867-584">The operating system cannot run %1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-585"><span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERROR \_ ENVVAR \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="d8867-585"><span id="ERROR_ENVVAR_NOT_FOUND"></span><span id="error_envvar_not_found"></span>**ERROR\_ENVVAR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-586">203 (0xCB)</span><span class="sxs-lookup"><span data-stu-id="d8867-586">203 (0xCB)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-587">El sistema no encontró la opción de entorno que se especificó.</span><span class="sxs-lookup"><span data-stu-id="d8867-587">The system could not find the environment option that was entered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-588"><span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERROR \_ sin \_ señal \_ enviada**</span><span class="sxs-lookup"><span data-stu-id="d8867-588"><span id="ERROR_NO_SIGNAL_SENT"></span><span id="error_no_signal_sent"></span>**ERROR\_NO\_SIGNAL\_SENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-589">205 (0xCD)</span><span class="sxs-lookup"><span data-stu-id="d8867-589">205 (0xCD)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-590">Ningún proceso en el subárbol de comandos tiene un controlador de señales.</span><span class="sxs-lookup"><span data-stu-id="d8867-590">No process in the command subtree has a signal handler.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-591"><span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERROR \_ filename \_ EXCED \_ intervalo**</span><span class="sxs-lookup"><span data-stu-id="d8867-591"><span id="ERROR_FILENAME_EXCED_RANGE"></span><span id="error_filename_exced_range"></span>**ERROR\_FILENAME\_EXCED\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-592">206 (0xCE)</span><span class="sxs-lookup"><span data-stu-id="d8867-592">206 (0xCE)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-593">El nombre de archivo o la extensión es demasiado largo.</span><span class="sxs-lookup"><span data-stu-id="d8867-593">The filename or extension is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-594"><span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**ERROR \_ \_ en la pila RING2 \_ en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="d8867-594"><span id="ERROR_RING2_STACK_IN_USE"></span><span id="error_ring2_stack_in_use"></span>**ERROR\_RING2\_STACK\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-595">207 (0xCF)</span><span class="sxs-lookup"><span data-stu-id="d8867-595">207 (0xCF)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-596">La pila de anillo 2 está en uso.</span><span class="sxs-lookup"><span data-stu-id="d8867-596">The ring 2 stack is in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-597"><span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**ERROR de \_ expansión de metadatos \_ \_ demasiado \_ largo**</span><span class="sxs-lookup"><span data-stu-id="d8867-597"><span id="ERROR_META_EXPANSION_TOO_LONG"></span><span id="error_meta_expansion_too_long"></span>**ERROR\_META\_EXPANSION\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-598">208 (0xD0)</span><span class="sxs-lookup"><span data-stu-id="d8867-598">208 (0xD0)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-599">Los caracteres de nombre de archivo globales, \* o?, se escriben incorrectamente o se han especificado demasiados caracteres de nombre de archivo globales.</span><span class="sxs-lookup"><span data-stu-id="d8867-599">The global filename characters, \* or ?, are entered incorrectly or too many global filename characters are specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-600"><span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**ERROR \_ de \_ número de señal no válida \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-600"><span id="ERROR_INVALID_SIGNAL_NUMBER"></span><span id="error_invalid_signal_number"></span>**ERROR\_INVALID\_SIGNAL\_NUMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-601">209 (0xD1)</span><span class="sxs-lookup"><span data-stu-id="d8867-601">209 (0xD1)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-602">La señal que se está enviando no es correcta.</span><span class="sxs-lookup"><span data-stu-id="d8867-602">The signal being posted is not correct.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-603"><span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**ERROR de \_ subproceso \_ 1 \_ inactivo**</span><span class="sxs-lookup"><span data-stu-id="d8867-603"><span id="ERROR_THREAD_1_INACTIVE"></span><span id="error_thread_1_inactive"></span>**ERROR\_THREAD\_1\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-604">210 (0xD2)</span><span class="sxs-lookup"><span data-stu-id="d8867-604">210 (0xD2)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-605">No se puede establecer el controlador de señal.</span><span class="sxs-lookup"><span data-stu-id="d8867-605">The signal handler cannot be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-606"><span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERROR \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="d8867-606"><span id="ERROR_LOCKED"></span><span id="error_locked"></span>**ERROR\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-607">212 (0xD4)</span><span class="sxs-lookup"><span data-stu-id="d8867-607">212 (0xD4)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-608">El segmento está bloqueado y no se puede reasignar.</span><span class="sxs-lookup"><span data-stu-id="d8867-608">The segment is locked and cannot be reallocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-609"><span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERROR \_ demasiados \_ \_ módulos**</span><span class="sxs-lookup"><span data-stu-id="d8867-609"><span id="ERROR_TOO_MANY_MODULES"></span><span id="error_too_many_modules"></span>**ERROR\_TOO\_MANY\_MODULES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-610">214 (0xD6)</span><span class="sxs-lookup"><span data-stu-id="d8867-610">214 (0xD6)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-611">Hay demasiados módulos de vínculos dinámicos asociados a este programa o módulo de vínculo dinámico.</span><span class="sxs-lookup"><span data-stu-id="d8867-611">Too many dynamic-link modules are attached to this program or dynamic-link module.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-612"><span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**\_ \_ no se permite el ANIDAMIENTO de errores \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-612"><span id="ERROR_NESTING_NOT_ALLOWED"></span><span id="error_nesting_not_allowed"></span>**ERROR\_NESTING\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-613">215 (0xD7)</span><span class="sxs-lookup"><span data-stu-id="d8867-613">215 (0xD7)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-614">No se pueden anidar llamadas a LoadModule.</span><span class="sxs-lookup"><span data-stu-id="d8867-614">Cannot nest calls to LoadModule.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-615"><span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**ERROR \_ \_ \_ no coincide el tipo de máquina exe \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-615"><span id="ERROR_EXE_MACHINE_TYPE_MISMATCH"></span><span id="error_exe_machine_type_mismatch"></span>**ERROR\_EXE\_MACHINE\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-616">216 (0xD8)</span><span class="sxs-lookup"><span data-stu-id="d8867-616">216 (0xD8)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-617">Esta versión de %1 no es compatible con la versión de Windows que se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="d8867-617">This version of %1 is not compatible with the version of Windows you're running.</span></span> <span data-ttu-id="d8867-618">Compruebe la información del sistema del equipo y, a continuación, póngase en contacto con el editor de software.</span><span class="sxs-lookup"><span data-stu-id="d8867-618">Check your computer's system information and then contact the software publisher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-619"><span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**ERROR \_ exe \_ no se puede \_ modificar el \_ \_ binario firmado**</span><span class="sxs-lookup"><span data-stu-id="d8867-619"><span id="ERROR_EXE_CANNOT_MODIFY_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_signed_binary"></span>**ERROR\_EXE\_CANNOT\_MODIFY\_SIGNED\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-620">217 (0xD9)</span><span class="sxs-lookup"><span data-stu-id="d8867-620">217 (0xD9)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-621">El archivo de imagen %1 está firmado, no se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="d8867-621">The image file %1 is signed, unable to modify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-622"><span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**ERROR \_ exe \_ no se puede \_ modificar el \_ \_ binario con firma segura \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-622"><span id="ERROR_EXE_CANNOT_MODIFY_STRONG_SIGNED_BINARY"></span><span id="error_exe_cannot_modify_strong_signed_binary"></span>**ERROR\_EXE\_CANNOT\_MODIFY\_STRONG\_SIGNED\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-623">218 (0xDA)</span><span class="sxs-lookup"><span data-stu-id="d8867-623">218 (0xDA)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-624">El archivo de imagen %1 está firmado de forma segura, no se puede modificar.</span><span class="sxs-lookup"><span data-stu-id="d8867-624">The image file %1 is strong signed, unable to modify.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-625"><span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**archivo de ERROR \_ \_ desprotegido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-625"><span id="ERROR_FILE_CHECKED_OUT"></span><span id="error_file_checked_out"></span>**ERROR\_FILE\_CHECKED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-626">220 (0xDC)</span><span class="sxs-lookup"><span data-stu-id="d8867-626">220 (0xDC)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-627">Este archivo está desprotegido o bloqueado para su edición por otro usuario.</span><span class="sxs-lookup"><span data-stu-id="d8867-627">This file is checked out or locked for editing by another user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-628"><span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**ERROR de \_ desprotección \_ necesario**</span><span class="sxs-lookup"><span data-stu-id="d8867-628"><span id="ERROR_CHECKOUT_REQUIRED"></span><span id="error_checkout_required"></span>**ERROR\_CHECKOUT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-629">221 (0xDD)</span><span class="sxs-lookup"><span data-stu-id="d8867-629">221 (0xDD)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-630">El archivo debe desprotegerse antes de guardar los cambios.</span><span class="sxs-lookup"><span data-stu-id="d8867-630">The file must be checked out before saving changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-631"><span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERROR \_ de \_ tipo de archivo incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-631"><span id="ERROR_BAD_FILE_TYPE"></span><span id="error_bad_file_type"></span>**ERROR\_BAD\_FILE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-632">222 (0xDE)</span><span class="sxs-lookup"><span data-stu-id="d8867-632">222 (0xDE)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-633">Se bloqueó el tipo de archivo que se va a guardar o recuperar.</span><span class="sxs-lookup"><span data-stu-id="d8867-633">The file type being saved or retrieved has been blocked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-634"><span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**archivo de ERROR \_ \_ demasiado \_ grande**</span><span class="sxs-lookup"><span data-stu-id="d8867-634"><span id="ERROR_FILE_TOO_LARGE"></span><span id="error_file_too_large"></span>**ERROR\_FILE\_TOO\_LARGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-635">223 (0xDF)</span><span class="sxs-lookup"><span data-stu-id="d8867-635">223 (0xDF)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-636">El tamaño del archivo supera el límite permitido y no se puede guardar.</span><span class="sxs-lookup"><span data-stu-id="d8867-636">The file size exceeds the limit allowed and cannot be saved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-637"><span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**formularios de ERROR \_ \_ auth \_ obligatorio**</span><span class="sxs-lookup"><span data-stu-id="d8867-637"><span id="ERROR_FORMS_AUTH_REQUIRED"></span><span id="error_forms_auth_required"></span>**ERROR\_FORMS\_AUTH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-638">224 (0xE0)</span><span class="sxs-lookup"><span data-stu-id="d8867-638">224 (0xE0)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-639">Acceso denegado.</span><span class="sxs-lookup"><span data-stu-id="d8867-639">Access Denied.</span></span> <span data-ttu-id="d8867-640">Antes de abrir archivos en esta ubicación, primero debe agregar el sitio web a la lista de sitios de confianza, buscar el sitio web y seleccionar la opción de inicio de sesión automático.</span><span class="sxs-lookup"><span data-stu-id="d8867-640">Before opening files in this location, you must first add the web site to your trusted sites list, browse to the web site, and select the option to login automatically.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-641"><span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**VIRUS de ERROR \_ \_ infectado**</span><span class="sxs-lookup"><span data-stu-id="d8867-641"><span id="ERROR_VIRUS_INFECTED"></span><span id="error_virus_infected"></span>**ERROR\_VIRUS\_INFECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-642">225 (0xE1)</span><span class="sxs-lookup"><span data-stu-id="d8867-642">225 (0xE1)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-643">La operación no se completó correctamente porque el archivo contiene un virus o software potencialmente no deseado.</span><span class="sxs-lookup"><span data-stu-id="d8867-643">Operation did not complete successfully because the file contains a virus or potentially unwanted software.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-644"><span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**ERROR \_ de \_ eliminación de virus**</span><span class="sxs-lookup"><span data-stu-id="d8867-644"><span id="ERROR_VIRUS_DELETED"></span><span id="error_virus_deleted"></span>**ERROR\_VIRUS\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-645">226 (0xE2)</span><span class="sxs-lookup"><span data-stu-id="d8867-645">226 (0xE2)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-646">Este archivo contiene un virus o software potencialmente no deseado y no se puede abrir.</span><span class="sxs-lookup"><span data-stu-id="d8867-646">This file contains a virus or potentially unwanted software and cannot be opened.</span></span> <span data-ttu-id="d8867-647">Debido a la naturaleza de este virus o software potencialmente no deseado, el archivo se ha quitado de esta ubicación.</span><span class="sxs-lookup"><span data-stu-id="d8867-647">Due to the nature of this virus or potentially unwanted software, the file has been removed from this location.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-648"><span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**\_canalización de errores \_ local**</span><span class="sxs-lookup"><span data-stu-id="d8867-648"><span id="ERROR_PIPE_LOCAL"></span><span id="error_pipe_local"></span>**ERROR\_PIPE\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-649">229 (0xE5)</span><span class="sxs-lookup"><span data-stu-id="d8867-649">229 (0xE5)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-650">La canalización es local.</span><span class="sxs-lookup"><span data-stu-id="d8867-650">The pipe is local.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-651"><span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**ERROR \_ de \_ Canalización incorrecta**</span><span class="sxs-lookup"><span data-stu-id="d8867-651"><span id="ERROR_BAD_PIPE"></span><span id="error_bad_pipe"></span>**ERROR\_BAD\_PIPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-652">230 (0xE6)</span><span class="sxs-lookup"><span data-stu-id="d8867-652">230 (0xE6)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-653">El estado de la canalización no es válido.</span><span class="sxs-lookup"><span data-stu-id="d8867-653">The pipe state is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-654"><span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**\_canalización de errores \_ ocupada**</span><span class="sxs-lookup"><span data-stu-id="d8867-654"><span id="ERROR_PIPE_BUSY"></span><span id="error_pipe_busy"></span>**ERROR\_PIPE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-655">231 (0xE7)</span><span class="sxs-lookup"><span data-stu-id="d8867-655">231 (0xE7)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-656">Todas las instancias de canalización están ocupadas.</span><span class="sxs-lookup"><span data-stu-id="d8867-656">All pipe instances are busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-657"><span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERROR \_ sin \_ datos**</span><span class="sxs-lookup"><span data-stu-id="d8867-657"><span id="ERROR_NO_DATA"></span><span id="error_no_data"></span>**ERROR\_NO\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-658">232 (0xE8)</span><span class="sxs-lookup"><span data-stu-id="d8867-658">232 (0xE8)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-659">La canalización se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="d8867-659">The pipe is being closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-660"><span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**\_canalización de errores \_ no \_ conectada**</span><span class="sxs-lookup"><span data-stu-id="d8867-660"><span id="ERROR_PIPE_NOT_CONNECTED"></span><span id="error_pipe_not_connected"></span>**ERROR\_PIPE\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-661">233 (0xE9)</span><span class="sxs-lookup"><span data-stu-id="d8867-661">233 (0xE9)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-662">No hay ningún proceso en el otro extremo de la canalización.</span><span class="sxs-lookup"><span data-stu-id="d8867-662">No process is on the other end of the pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-663"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR \_ más \_ datos**</span><span class="sxs-lookup"><span data-stu-id="d8867-663"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-664">234 (0xEA)</span><span class="sxs-lookup"><span data-stu-id="d8867-664">234 (0xEA)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-665">More data is available (Hyper-V no pudo generar el conjunto de instantáneas de VSS para la máquina virtual: hay más datos disponibles).</span><span class="sxs-lookup"><span data-stu-id="d8867-665">More data is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-666"><span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERROR de \_ VC \_ desconectado**</span><span class="sxs-lookup"><span data-stu-id="d8867-666"><span id="ERROR_VC_DISCONNECTED"></span><span id="error_vc_disconnected"></span>**ERROR\_VC\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-667">240 (0xF0)</span><span class="sxs-lookup"><span data-stu-id="d8867-667">240 (0xF0)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-668">Se canceló la sesión.</span><span class="sxs-lookup"><span data-stu-id="d8867-668">The session was canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-669"><span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERROR \_ de \_ nombre EA no válido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-669"><span id="ERROR_INVALID_EA_NAME"></span><span id="error_invalid_ea_name"></span>**ERROR\_INVALID\_EA\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-670">254 (0xFE)</span><span class="sxs-lookup"><span data-stu-id="d8867-670">254 (0xFE)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-671">El nombre del atributo extendido especificado no era válido.</span><span class="sxs-lookup"><span data-stu-id="d8867-671">The specified extended attribute name was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-672"><span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**lista de errores de \_ EA \_ \_ incoherente**</span><span class="sxs-lookup"><span data-stu-id="d8867-672"><span id="ERROR_EA_LIST_INCONSISTENT"></span><span id="error_ea_list_inconsistent"></span>**ERROR\_EA\_LIST\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-673">255 (0xFF)</span><span class="sxs-lookup"><span data-stu-id="d8867-673">255 (0xFF)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-674">Los atributos extendidos son incoherentes.</span><span class="sxs-lookup"><span data-stu-id="d8867-674">The extended attributes are inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-675"><span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**\_tiempo de espera agotado**</span><span class="sxs-lookup"><span data-stu-id="d8867-675"><span id="WAIT_TIMEOUT"></span><span id="wait_timeout"></span>**WAIT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-676">258 (0x102)</span><span class="sxs-lookup"><span data-stu-id="d8867-676">258 (0x102)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-677">Se agotó el tiempo de espera de la operación de espera.</span><span class="sxs-lookup"><span data-stu-id="d8867-677">The wait operation timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-678"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**\_no hay \_ más \_ elementos de error**</span><span class="sxs-lookup"><span data-stu-id="d8867-678"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-679">259 (0x103)</span><span class="sxs-lookup"><span data-stu-id="d8867-679">259 (0x103)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-680">No más datos disponibles.</span><span class="sxs-lookup"><span data-stu-id="d8867-680">No more data is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-681"><span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**\_no se puede copiar el error \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-681"><span id="ERROR_CANNOT_COPY"></span><span id="error_cannot_copy"></span>**ERROR\_CANNOT\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-682">266 (0x10A)</span><span class="sxs-lookup"><span data-stu-id="d8867-682">266 (0x10A)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-683">No se pueden usar las funciones de copia.</span><span class="sxs-lookup"><span data-stu-id="d8867-683">The copy functions cannot be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-684"><span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**directorio de errores \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-684"><span id="ERROR_DIRECTORY"></span><span id="error_directory"></span>**ERROR\_DIRECTORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-685">267 (0x10B)</span><span class="sxs-lookup"><span data-stu-id="d8867-685">267 (0x10B)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-686">El nombre del directorio no es válido.</span><span class="sxs-lookup"><span data-stu-id="d8867-686">The directory name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-687"><span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERROR \_ de \_ echará de EAS \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-687"><span id="ERROR_EAS_DIDNT_FIT"></span><span id="error_eas_didnt_fit"></span>**ERROR\_EAS\_DIDNT\_FIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-688">275 (0x113)</span><span class="sxs-lookup"><span data-stu-id="d8867-688">275 (0x113)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-689">Los atributos extendidos no caben en el búfer.</span><span class="sxs-lookup"><span data-stu-id="d8867-689">The extended attributes did not fit in the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-690"><span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**el \_ archivo EA de error \_ \_ está dañado**</span><span class="sxs-lookup"><span data-stu-id="d8867-690"><span id="ERROR_EA_FILE_CORRUPT"></span><span id="error_ea_file_corrupt"></span>**ERROR\_EA\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-691">276 (0x114)</span><span class="sxs-lookup"><span data-stu-id="d8867-691">276 (0x114)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-692">El archivo de atributo extendido del sistema de archivos montado está dañado.</span><span class="sxs-lookup"><span data-stu-id="d8867-692">The extended attribute file on the mounted file system is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-693"><span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERROR \_ de \_ tabla EA \_ completa**</span><span class="sxs-lookup"><span data-stu-id="d8867-693"><span id="ERROR_EA_TABLE_FULL"></span><span id="error_ea_table_full"></span>**ERROR\_EA\_TABLE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-694">277 (0x115)</span><span class="sxs-lookup"><span data-stu-id="d8867-694">277 (0x115)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-695">El archivo de tabla de atributos extendidos está lleno.</span><span class="sxs-lookup"><span data-stu-id="d8867-695">The extended attribute table file is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-696"><span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERROR \_ de \_ identificador EA no válido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-696"><span id="ERROR_INVALID_EA_HANDLE"></span><span id="error_invalid_ea_handle"></span>**ERROR\_INVALID\_EA\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-697">278 (0x116)</span><span class="sxs-lookup"><span data-stu-id="d8867-697">278 (0x116)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-698">El identificador de atributo extendido especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="d8867-698">The specified extended attribute handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-699"><span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERROR \_ EAS \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="d8867-699"><span id="ERROR_EAS_NOT_SUPPORTED"></span><span id="error_eas_not_supported"></span>**ERROR\_EAS\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-700">282 (0x11A)</span><span class="sxs-lookup"><span data-stu-id="d8867-700">282 (0x11A)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-701">El sistema de archivos montado no admite atributos extendidos.</span><span class="sxs-lookup"><span data-stu-id="d8867-701">The mounted file system does not support extended attributes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-702"><span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**no se pudo tener el \_ \_ propietario**</span><span class="sxs-lookup"><span data-stu-id="d8867-702"><span id="ERROR_NOT_OWNER"></span><span id="error_not_owner"></span>**ERROR\_NOT\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-703">288 (0x120)</span><span class="sxs-lookup"><span data-stu-id="d8867-703">288 (0x120)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-704">Intento de liberar la exclusión mutua que no es propiedad del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="d8867-704">Attempt to release mutex not owned by caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-705"><span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERROR \_ demasiadas \_ \_ publicaciones**</span><span class="sxs-lookup"><span data-stu-id="d8867-705"><span id="ERROR_TOO_MANY_POSTS"></span><span id="error_too_many_posts"></span>**ERROR\_TOO\_MANY\_POSTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-706">298 (0x12A)</span><span class="sxs-lookup"><span data-stu-id="d8867-706">298 (0x12A)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-707">Se han realizado demasiadas publicaciones en un semáforo.</span><span class="sxs-lookup"><span data-stu-id="d8867-707">Too many posts were made to a semaphore.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-708"><span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERROR \_ de \_ copia parcial**</span><span class="sxs-lookup"><span data-stu-id="d8867-708"><span id="ERROR_PARTIAL_COPY"></span><span id="error_partial_copy"></span>**ERROR\_PARTIAL\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-709">299 (0x12B)</span><span class="sxs-lookup"><span data-stu-id="d8867-709">299 (0x12B)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-710">Solo parte de una solicitud de ReadProcessMemory o WriteProcessMemory se ha completado.</span><span class="sxs-lookup"><span data-stu-id="d8867-710">Only part of a ReadProcessMemory or WriteProcessMemory request was completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-711"><span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERROR de \_ bloqueo oportunista \_ no \_ concedido**</span><span class="sxs-lookup"><span data-stu-id="d8867-711"><span id="ERROR_OPLOCK_NOT_GRANTED"></span><span id="error_oplock_not_granted"></span>**ERROR\_OPLOCK\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-712">300 (0x12C)</span><span class="sxs-lookup"><span data-stu-id="d8867-712">300 (0x12C)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-713">Se denegó la solicitud de bloqueo oportunista.</span><span class="sxs-lookup"><span data-stu-id="d8867-713">The oplock request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-714"><span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERROR \_ de \_ Protocolo de bloqueo oportunista no válido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-714"><span id="ERROR_INVALID_OPLOCK_PROTOCOL"></span><span id="error_invalid_oplock_protocol"></span>**ERROR\_INVALID\_OPLOCK\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-715">301 (0x12D)</span><span class="sxs-lookup"><span data-stu-id="d8867-715">301 (0x12D)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-716">El sistema recibió una confirmación de bloqueo oportunista no válida.</span><span class="sxs-lookup"><span data-stu-id="d8867-716">An invalid oplock acknowledgment was received by the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-717"><span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**el disco de ERROR está \_ \_ demasiado \_ fragmentado**</span><span class="sxs-lookup"><span data-stu-id="d8867-717"><span id="ERROR_DISK_TOO_FRAGMENTED"></span><span id="error_disk_too_fragmented"></span>**ERROR\_DISK\_TOO\_FRAGMENTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-718">302 (0x12E)</span><span class="sxs-lookup"><span data-stu-id="d8867-718">302 (0x12E)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-719">El volumen está demasiado fragmentado para completar esta operación.</span><span class="sxs-lookup"><span data-stu-id="d8867-719">The volume is too fragmented to complete this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-720"><span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERROR de \_ eliminación \_ pendiente**</span><span class="sxs-lookup"><span data-stu-id="d8867-720"><span id="ERROR_DELETE_PENDING"></span><span id="error_delete_pending"></span>**ERROR\_DELETE\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-721">303 (0x12F)</span><span class="sxs-lookup"><span data-stu-id="d8867-721">303 (0x12F)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-722">No se puede abrir el archivo porque está en proceso de eliminación.</span><span class="sxs-lookup"><span data-stu-id="d8867-722">The file cannot be opened because it is in the process of being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-723"><span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERROR \_ incompatible \_ con \_ la \_ \_ configuración de \_ registro de nombre corto global \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-723"><span id="ERROR_INCOMPATIBLE_WITH_GLOBAL_SHORT_NAME_REGISTRY_SETTING"></span><span id="error_incompatible_with_global_short_name_registry_setting"></span>**ERROR\_INCOMPATIBLE\_WITH\_GLOBAL\_SHORT\_NAME\_REGISTRY\_SETTING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-724">304 (0x130)</span><span class="sxs-lookup"><span data-stu-id="d8867-724">304 (0x130)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-725">No se puede cambiar la configuración de nombre corto en este volumen debido a la configuración del registro global.</span><span class="sxs-lookup"><span data-stu-id="d8867-725">Short name settings may not be changed on this volume due to the global registry setting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-726"><span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**\_nombres cortos \_ \_ de error no \_ habilitados \_ en el \_ volumen**</span><span class="sxs-lookup"><span data-stu-id="d8867-726"><span id="ERROR_SHORT_NAMES_NOT_ENABLED_ON_VOLUME"></span><span id="error_short_names_not_enabled_on_volume"></span>**ERROR\_SHORT\_NAMES\_NOT\_ENABLED\_ON\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-727">305 (0x131)</span><span class="sxs-lookup"><span data-stu-id="d8867-727">305 (0x131)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-728">Los nombres cortos no están habilitados en este volumen.</span><span class="sxs-lookup"><span data-stu-id="d8867-728">Short names are not enabled on this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-729"><span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**el \_ flujo de seguridad de error \_ \_ no es \_ coherente**</span><span class="sxs-lookup"><span data-stu-id="d8867-729"><span id="ERROR_SECURITY_STREAM_IS_INCONSISTENT"></span><span id="error_security_stream_is_inconsistent"></span>**ERROR\_SECURITY\_STREAM\_IS\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-730">306 (0x132)</span><span class="sxs-lookup"><span data-stu-id="d8867-730">306 (0x132)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-731">El flujo de seguridad para el volumen especificado se encuentra en un estado incoherente.</span><span class="sxs-lookup"><span data-stu-id="d8867-731">The security stream for the given volume is in an inconsistent state.</span></span> <span data-ttu-id="d8867-732">Ejecute CHKDSK en el volumen.</span><span class="sxs-lookup"><span data-stu-id="d8867-732">Please run CHKDSK on the volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-733"><span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERROR \_ de \_ intervalo de bloqueo no válido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-733"><span id="ERROR_INVALID_LOCK_RANGE"></span><span id="error_invalid_lock_range"></span>**ERROR\_INVALID\_LOCK\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-734">307 (0x133)</span><span class="sxs-lookup"><span data-stu-id="d8867-734">307 (0x133)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-735">No se puede procesar una operación de bloqueo de archivo solicitada debido a un intervalo de bytes no válido.</span><span class="sxs-lookup"><span data-stu-id="d8867-735">A requested file lock operation cannot be processed due to an invalid byte range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-736"><span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**subsistema de imagen de ERROR \_ \_ \_ no \_ presente**</span><span class="sxs-lookup"><span data-stu-id="d8867-736"><span id="ERROR_IMAGE_SUBSYSTEM_NOT_PRESENT"></span><span id="error_image_subsystem_not_present"></span>**ERROR\_IMAGE\_SUBSYSTEM\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-737">308 (0x134)</span><span class="sxs-lookup"><span data-stu-id="d8867-737">308 (0x134)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-738">El subsistema necesario para admitir el tipo de imagen no está presente.</span><span class="sxs-lookup"><span data-stu-id="d8867-738">The subsystem needed to support the image type is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-739"><span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**GUID de notificación de ERROR \_ \_ \_ ya \_ definido**</span><span class="sxs-lookup"><span data-stu-id="d8867-739"><span id="ERROR_NOTIFICATION_GUID_ALREADY_DEFINED"></span><span id="error_notification_guid_already_defined"></span>**ERROR\_NOTIFICATION\_GUID\_ALREADY\_DEFINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-740">309 (0x135)</span><span class="sxs-lookup"><span data-stu-id="d8867-740">309 (0x135)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-741">El archivo especificado ya tiene asociado un GUID de notificación.</span><span class="sxs-lookup"><span data-stu-id="d8867-741">The specified file already has a notification GUID associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-742"><span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERROR \_ de \_ controlador de excepciones no válido \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-742"><span id="ERROR_INVALID_EXCEPTION_HANDLER"></span><span id="error_invalid_exception_handler"></span>**ERROR\_INVALID\_EXCEPTION\_HANDLER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-743">310 (0x136)</span><span class="sxs-lookup"><span data-stu-id="d8867-743">310 (0x136)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-744">Se ha detectado una rutina del controlador de excepciones no válida.</span><span class="sxs-lookup"><span data-stu-id="d8867-744">An invalid exception handler routine has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-745"><span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**ERROR \_ de \_ privilegios duplicados**</span><span class="sxs-lookup"><span data-stu-id="d8867-745"><span id="ERROR_DUPLICATE_PRIVILEGES"></span><span id="error_duplicate_privileges"></span>**ERROR\_DUPLICATE\_PRIVILEGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-746">311 (0x137)</span><span class="sxs-lookup"><span data-stu-id="d8867-746">311 (0x137)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-747">Se especificaron privilegios duplicados para el token.</span><span class="sxs-lookup"><span data-stu-id="d8867-747">Duplicate privileges were specified for the token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-748"><span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERROR: \_ no se \_ \_ procesaron intervalos**</span><span class="sxs-lookup"><span data-stu-id="d8867-748"><span id="ERROR_NO_RANGES_PROCESSED"></span><span id="error_no_ranges_processed"></span>**ERROR\_NO\_RANGES\_PROCESSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-749">312 (0x138)</span><span class="sxs-lookup"><span data-stu-id="d8867-749">312 (0x138)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-750">No se pudo procesar ningún intervalo para la operación especificada.</span><span class="sxs-lookup"><span data-stu-id="d8867-750">No ranges for the specified operation were able to be processed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-751"><span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERROR \_ no \_ permitido \_ en \_ el \_ archivo del sistema**</span><span class="sxs-lookup"><span data-stu-id="d8867-751"><span id="ERROR_NOT_ALLOWED_ON_SYSTEM_FILE"></span><span id="error_not_allowed_on_system_file"></span>**ERROR\_NOT\_ALLOWED\_ON\_SYSTEM\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-752">313 (0x139)</span><span class="sxs-lookup"><span data-stu-id="d8867-752">313 (0x139)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-753">No se permite la operación en un archivo interno del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="d8867-753">Operation is not allowed on a file system internal file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-754"><span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**ERROR \_ de \_ recursos de disco \_ agotados**</span><span class="sxs-lookup"><span data-stu-id="d8867-754"><span id="ERROR_DISK_RESOURCES_EXHAUSTED"></span><span id="error_disk_resources_exhausted"></span>**ERROR\_DISK\_RESOURCES\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-755">314 (0x13A)</span><span class="sxs-lookup"><span data-stu-id="d8867-755">314 (0x13A)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-756">Se han agotado los recursos físicos de este disco.</span><span class="sxs-lookup"><span data-stu-id="d8867-756">The physical resources of this disk have been exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-757"><span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**ERROR \_ de \_ token no válido**</span><span class="sxs-lookup"><span data-stu-id="d8867-757"><span id="ERROR_INVALID_TOKEN"></span><span id="error_invalid_token"></span>**ERROR\_INVALID\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-758">315 (0x13B)</span><span class="sxs-lookup"><span data-stu-id="d8867-758">315 (0x13B)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-759">El token que representa los datos no es válido.</span><span class="sxs-lookup"><span data-stu-id="d8867-759">The token representing the data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-760"><span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**\_no se \_ admite la característica de dispositivo de error \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-760"><span id="ERROR_DEVICE_FEATURE_NOT_SUPPORTED"></span><span id="error_device_feature_not_supported"></span>**ERROR\_DEVICE\_FEATURE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-761">316 (0x13C)</span><span class="sxs-lookup"><span data-stu-id="d8867-761">316 (0x13C)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-762">El dispositivo no admite la característica de comandos.</span><span class="sxs-lookup"><span data-stu-id="d8867-762">The device does not support the command feature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-763"><span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**\_ \_ \_ no \_ se encontró el error Mr MID**</span><span class="sxs-lookup"><span data-stu-id="d8867-763"><span id="ERROR_MR_MID_NOT_FOUND"></span><span id="error_mr_mid_not_found"></span>**ERROR\_MR\_MID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-764">317 (0x13D)</span><span class="sxs-lookup"><span data-stu-id="d8867-764">317 (0x13D)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-765">El sistema no encuentra el texto del mensaje para el número de mensaje 0x %1 en el archivo de mensaje de %2.</span><span class="sxs-lookup"><span data-stu-id="d8867-765">The system cannot find message text for message number 0x%1 in the message file for %2.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-766"><span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**\_ \_ no \_ se encontró el ámbito de error**</span><span class="sxs-lookup"><span data-stu-id="d8867-766"><span id="ERROR_SCOPE_NOT_FOUND"></span><span id="error_scope_not_found"></span>**ERROR\_SCOPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-767">318 (0x13E)</span><span class="sxs-lookup"><span data-stu-id="d8867-767">318 (0x13E)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-768">No se encontró el ámbito especificado.</span><span class="sxs-lookup"><span data-stu-id="d8867-768">The scope specified was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-769"><span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**ERROR \_ sin definir \_ ámbito**</span><span class="sxs-lookup"><span data-stu-id="d8867-769"><span id="ERROR_UNDEFINED_SCOPE"></span><span id="error_undefined_scope"></span>**ERROR\_UNDEFINED\_SCOPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-770">319 (0x13F)</span><span class="sxs-lookup"><span data-stu-id="d8867-770">319 (0x13F)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-771">La Directiva de acceso central especificada no está definida en el equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="d8867-771">The Central Access Policy specified is not defined on the target machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-772"><span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**ERROR \_ de \_ Cap no válido**</span><span class="sxs-lookup"><span data-stu-id="d8867-772"><span id="ERROR_INVALID_CAP"></span><span id="error_invalid_cap"></span>**ERROR\_INVALID\_CAP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-773">320 (0x140)</span><span class="sxs-lookup"><span data-stu-id="d8867-773">320 (0x140)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-774">La Directiva de acceso central obtenida de Active Directory no es válida.</span><span class="sxs-lookup"><span data-stu-id="d8867-774">The Central Access Policy obtained from Active Directory is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-775"><span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**ERROR de \_ dispositivo \_ inaccesible**</span><span class="sxs-lookup"><span data-stu-id="d8867-775"><span id="ERROR_DEVICE_UNREACHABLE"></span><span id="error_device_unreachable"></span>**ERROR\_DEVICE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-776">321 (0x141)</span><span class="sxs-lookup"><span data-stu-id="d8867-776">321 (0x141)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-777">El dispositivo está inaccesible.</span><span class="sxs-lookup"><span data-stu-id="d8867-777">The device is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-778"><span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**ERROR de \_ dispositivo \_ sin \_ recursos**</span><span class="sxs-lookup"><span data-stu-id="d8867-778"><span id="ERROR_DEVICE_NO_RESOURCES"></span><span id="error_device_no_resources"></span>**ERROR\_DEVICE\_NO\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-779">322 (0x142)</span><span class="sxs-lookup"><span data-stu-id="d8867-779">322 (0x142)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-780">El dispositivo de destino no tiene suficientes recursos para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="d8867-780">The target device has insufficient resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-781"><span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**error \_ de \_ suma de comprobación de datos de error \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-781"><span id="ERROR_DATA_CHECKSUM_ERROR"></span><span id="error_data_checksum_error"></span>**ERROR\_DATA\_CHECKSUM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-782">323 (0x143)</span><span class="sxs-lookup"><span data-stu-id="d8867-782">323 (0x143)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-783">Se produjo un error de suma de comprobación de integridad de datos.</span><span class="sxs-lookup"><span data-stu-id="d8867-783">A data integrity checksum error occurred.</span></span> <span data-ttu-id="d8867-784">Los datos de la secuencia de archivo están dañados.</span><span class="sxs-lookup"><span data-stu-id="d8867-784">Data in the file stream is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-785"><span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERROR de la \_ \_ \_ operación EA \_ de kernel intermezclado**</span><span class="sxs-lookup"><span data-stu-id="d8867-785"><span id="ERROR_INTERMIXED_KERNEL_EA_OPERATION"></span><span id="error_intermixed_kernel_ea_operation"></span>**ERROR\_INTERMIXED\_KERNEL\_EA\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-786">324 (0x144)</span><span class="sxs-lookup"><span data-stu-id="d8867-786">324 (0x144)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-787">Se intentó modificar un KERNEL y un atributo extendido normal (EA) en la misma operación.</span><span class="sxs-lookup"><span data-stu-id="d8867-787">An attempt was made to modify both a KERNEL and normal Extended Attribute (EA) in the same operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-788"><span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**\_no se \_ admite el \_ recorte de nivel de \_ archivo \_ de errores**</span><span class="sxs-lookup"><span data-stu-id="d8867-788"><span id="ERROR_FILE_LEVEL_TRIM_NOT_SUPPORTED"></span><span id="error_file_level_trim_not_supported"></span>**ERROR\_FILE\_LEVEL\_TRIM\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-789">326 (0x146)</span><span class="sxs-lookup"><span data-stu-id="d8867-789">326 (0x146)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-790">El dispositivo no admite el recorte en el nivel de archivo.</span><span class="sxs-lookup"><span data-stu-id="d8867-790">Device does not support file-level TRIM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-791"><span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**infracción de alineación de desplazamiento de ERROR \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-791"><span id="ERROR_OFFSET_ALIGNMENT_VIOLATION"></span><span id="error_offset_alignment_violation"></span>**ERROR\_OFFSET\_ALIGNMENT\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-792">327 (0x147)</span><span class="sxs-lookup"><span data-stu-id="d8867-792">327 (0x147)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-793">El comando especificó un desplazamiento de datos que no se alinea con la granularidad o alineación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8867-793">The command specified a data offset that does not align to the device's granularity/alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-794"><span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**ERROR \_ \_ de campo no válido \_ en la \_ lista de parámetros \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-794"><span id="ERROR_INVALID_FIELD_IN_PARAMETER_LIST"></span><span id="error_invalid_field_in_parameter_list"></span>**ERROR\_INVALID\_FIELD\_IN\_PARAMETER\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-795">328 (0x148)</span><span class="sxs-lookup"><span data-stu-id="d8867-795">328 (0x148)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-796">El comando especificó un campo no válido en su lista de parámetros.</span><span class="sxs-lookup"><span data-stu-id="d8867-796">The command specified an invalid field in its parameter list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-797"><span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**\_operación \_ de error en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="d8867-797"><span id="ERROR_OPERATION_IN_PROGRESS"></span><span id="error_operation_in_progress"></span>**ERROR\_OPERATION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-798">329 (0x149)</span><span class="sxs-lookup"><span data-stu-id="d8867-798">329 (0x149)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-799">Una operación está actualmente en curso con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8867-799">An operation is currently in progress with the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-800"><span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERROR \_ de \_ ruta de acceso de dispositivo incorrecta \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-800"><span id="ERROR_BAD_DEVICE_PATH"></span><span id="error_bad_device_path"></span>**ERROR\_BAD\_DEVICE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-801">330 (0x14A)</span><span class="sxs-lookup"><span data-stu-id="d8867-801">330 (0x14A)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-802">Se intentó enviar el comando a través de una ruta de acceso no válida al dispositivo de destino.</span><span class="sxs-lookup"><span data-stu-id="d8867-802">An attempt was made to send down the command via an invalid path to the target device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-803"><span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERROR \_ demasiados \_ \_ descriptores**</span><span class="sxs-lookup"><span data-stu-id="d8867-803"><span id="ERROR_TOO_MANY_DESCRIPTORS"></span><span id="error_too_many_descriptors"></span>**ERROR\_TOO\_MANY\_DESCRIPTORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-804">331 (0x14B)</span><span class="sxs-lookup"><span data-stu-id="d8867-804">331 (0x14B)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-805">El comando especificó un número de descriptores que superó el máximo admitido por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="d8867-805">The command specified a number of descriptors that exceeded the maximum supported by the device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-806"><span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**ERROR al \_ limpiar los \_ datos \_ deshabilitados**</span><span class="sxs-lookup"><span data-stu-id="d8867-806"><span id="ERROR_SCRUB_DATA_DISABLED"></span><span id="error_scrub_data_disabled"></span>**ERROR\_SCRUB\_DATA\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-807">332 (0x14C)</span><span class="sxs-lookup"><span data-stu-id="d8867-807">332 (0x14C)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-808">La limpieza está deshabilitada en el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d8867-808">Scrub is disabled on the specified file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-809"><span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**no se pudo \_ \_ almacenar el almacenamiento redundante \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-809"><span id="ERROR_NOT_REDUNDANT_STORAGE"></span><span id="error_not_redundant_storage"></span>**ERROR\_NOT\_REDUNDANT\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-810">333 (0x14D)</span><span class="sxs-lookup"><span data-stu-id="d8867-810">333 (0x14D)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-811">El dispositivo de almacenamiento no proporciona redundancia.</span><span class="sxs-lookup"><span data-stu-id="d8867-811">The storage device does not provide redundancy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-812"><span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**\_no se \_ admite el archivo residente de \_ errores \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-812"><span id="ERROR_RESIDENT_FILE_NOT_SUPPORTED"></span><span id="error_resident_file_not_supported"></span>**ERROR\_RESIDENT\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-813">334 (0x14E)</span><span class="sxs-lookup"><span data-stu-id="d8867-813">334 (0x14E)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-814">No se admite una operación en un archivo residente.</span><span class="sxs-lookup"><span data-stu-id="d8867-814">An operation is not supported on a resident file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-815"><span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**\_no se \_ admite el archivo comprimido de \_ errores \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-815"><span id="ERROR_COMPRESSED_FILE_NOT_SUPPORTED"></span><span id="error_compressed_file_not_supported"></span>**ERROR\_COMPRESSED\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-816">335 (0x14F)</span><span class="sxs-lookup"><span data-stu-id="d8867-816">335 (0x14F)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-817">No se admite una operación en un archivo comprimido.</span><span class="sxs-lookup"><span data-stu-id="d8867-817">An operation is not supported on a compressed file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-818"><span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**\_no se \_ \_ admite el directorio de errores**</span><span class="sxs-lookup"><span data-stu-id="d8867-818"><span id="ERROR_DIRECTORY_NOT_SUPPORTED"></span><span id="error_directory_not_supported"></span>**ERROR\_DIRECTORY\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-819">336 (0x150)</span><span class="sxs-lookup"><span data-stu-id="d8867-819">336 (0x150)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-820">No se admite una operación en un directorio.</span><span class="sxs-lookup"><span data-stu-id="d8867-820">An operation is not supported on a directory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-821"><span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**ERROR \_ al \_ leer \_ la \_ copia**</span><span class="sxs-lookup"><span data-stu-id="d8867-821"><span id="ERROR_NOT_READ_FROM_COPY"></span><span id="error_not_read_from_copy"></span>**ERROR\_NOT\_READ\_FROM\_COPY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-822">337 (0x151)</span><span class="sxs-lookup"><span data-stu-id="d8867-822">337 (0x151)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-823">No se pudo leer la copia especificada de los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="d8867-823">The specified copy of the requested data could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-824"><span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**ERROR de ERROR de \_ \_ reinicio de no acción \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-824"><span id="ERROR_FAIL_NOACTION_REBOOT"></span><span id="error_fail_noaction_reboot"></span>**ERROR\_FAIL\_NOACTION\_REBOOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-825">350 (0x15E)</span><span class="sxs-lookup"><span data-stu-id="d8867-825">350 (0x15E)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-826">No se realizó ninguna acción ya que es necesario reiniciar el sistema.</span><span class="sxs-lookup"><span data-stu-id="d8867-826">No action was taken as a system reboot is required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-827"><span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**ERROR \_ de \_ apagado**</span><span class="sxs-lookup"><span data-stu-id="d8867-827"><span id="ERROR_FAIL_SHUTDOWN"></span><span id="error_fail_shutdown"></span>**ERROR\_FAIL\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-828">351 (0x15F)</span><span class="sxs-lookup"><span data-stu-id="d8867-828">351 (0x15F)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-829">No se pudo realizar la operación de cierre.</span><span class="sxs-lookup"><span data-stu-id="d8867-829">The shutdown operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-830"><span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**ERROR \_ de \_ reinicio**</span><span class="sxs-lookup"><span data-stu-id="d8867-830"><span id="ERROR_FAIL_RESTART"></span><span id="error_fail_restart"></span>**ERROR\_FAIL\_RESTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-831">352 (0x160)</span><span class="sxs-lookup"><span data-stu-id="d8867-831">352 (0x160)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-832">Error en la operación de reinicio.</span><span class="sxs-lookup"><span data-stu-id="d8867-832">The restart operation failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-833"><span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**se \_ alcanzó el número máximo de sesiones de error \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d8867-833"><span id="ERROR_MAX_SESSIONS_REACHED"></span><span id="error_max_sessions_reached"></span>**ERROR\_MAX\_SESSIONS\_REACHED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-834">353 (0x161)</span><span class="sxs-lookup"><span data-stu-id="d8867-834">353 (0x161)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-835">Se ha alcanzado el número máximo de sesiones.</span><span class="sxs-lookup"><span data-stu-id="d8867-835">The maximum number of sessions has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-836"><span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**el \_ modo de subproceso de error \_ \_ ya está \_ en segundo plano**</span><span class="sxs-lookup"><span data-stu-id="d8867-836"><span id="ERROR_THREAD_MODE_ALREADY_BACKGROUND"></span><span id="error_thread_mode_already_background"></span>**ERROR\_THREAD\_MODE\_ALREADY\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-837">400 (0x190)</span><span class="sxs-lookup"><span data-stu-id="d8867-837">400 (0x190)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-838">El subproceso ya está en modo de procesamiento en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d8867-838">The thread is already in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-839"><span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**\_modo de subproceso de error \_ \_ no \_ en segundo plano**</span><span class="sxs-lookup"><span data-stu-id="d8867-839"><span id="ERROR_THREAD_MODE_NOT_BACKGROUND"></span><span id="error_thread_mode_not_background"></span>**ERROR\_THREAD\_MODE\_NOT\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-840">401 (0x191)</span><span class="sxs-lookup"><span data-stu-id="d8867-840">401 (0x191)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-841">El subproceso no está en modo de procesamiento en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d8867-841">The thread is not in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-842"><span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**el \_ modo de proceso de error \_ \_ ya está \_ en segundo plano**</span><span class="sxs-lookup"><span data-stu-id="d8867-842"><span id="ERROR_PROCESS_MODE_ALREADY_BACKGROUND"></span><span id="error_process_mode_already_background"></span>**ERROR\_PROCESS\_MODE\_ALREADY\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-843">402 (0x192)</span><span class="sxs-lookup"><span data-stu-id="d8867-843">402 (0x192)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-844">El proceso ya está en modo de procesamiento en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d8867-844">The process is already in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-845"><span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**modo de proceso de ERROR \_ \_ \_ no \_ fondo**</span><span class="sxs-lookup"><span data-stu-id="d8867-845"><span id="ERROR_PROCESS_MODE_NOT_BACKGROUND"></span><span id="error_process_mode_not_background"></span>**ERROR\_PROCESS\_MODE\_NOT\_BACKGROUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-846">403 (0x193)</span><span class="sxs-lookup"><span data-stu-id="d8867-846">403 (0x193)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-847">El proceso no está en modo de procesamiento en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="d8867-847">The process is not in background processing mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d8867-848"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR \_ de \_ dirección no válida**</span><span class="sxs-lookup"><span data-stu-id="d8867-848"><span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**ERROR\_INVALID\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d8867-849">487 (0x1E7)</span><span class="sxs-lookup"><span data-stu-id="d8867-849">487 (0x1E7)</span></span>
</dt> <dt>



<span data-ttu-id="d8867-850">Intento de obtener acceso a una dirección no válida.</span><span class="sxs-lookup"><span data-stu-id="d8867-850">Attempt to access invalid address.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="d8867-851">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8867-851">Requirements</span></span>



| <span data-ttu-id="d8867-852">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8867-852">Requirement</span></span> | <span data-ttu-id="d8867-853">Value</span><span class="sxs-lookup"><span data-stu-id="d8867-853">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8867-854">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8867-854">Minimum supported client</span></span><br/> | <span data-ttu-id="d8867-855">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="d8867-855">Windows XP \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="d8867-856">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8867-856">Minimum supported server</span></span><br/> | <span data-ttu-id="d8867-857">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8867-857">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d8867-858">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d8867-858">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8867-859"><dt>WinError. h (incluye Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8867-859"><dt>WinError.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8867-860">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8867-860">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8867-861">Códigos de error del sistema</span><span class="sxs-lookup"><span data-stu-id="d8867-861">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




