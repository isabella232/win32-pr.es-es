---
description: Describe los códigos de error 1000-1299 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: 0061feb6-e1a0-4fcd-8f80-954087c799d7
title: Códigos de error del sistema (1000-1299) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 592bd5c6653526d87fed05d6ec76f739355ae359
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104538938"
---
# <a name="system-error-codes-1000-1299"></a><span data-ttu-id="298d3-103">Códigos de error del sistema (1000-1299)</span><span class="sxs-lookup"><span data-stu-id="298d3-103">System Error Codes (1000-1299)</span></span>

> [!NOTE]
> <span data-ttu-id="298d3-104">Esta información está destinada a los desarrolladores que depuran errores del sistema.</span><span class="sxs-lookup"><span data-stu-id="298d3-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="298d3-105">En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="298d3-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="298d3-106">En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) para los errores 1000 a 1299.</span><span class="sxs-lookup"><span data-stu-id="298d3-106">The following list describes [system error codes](system-error-codes.md) for errors 1000 to 1299.</span></span> <span data-ttu-id="298d3-107">La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones.</span><span class="sxs-lookup"><span data-stu-id="298d3-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="298d3-108">Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.</span><span class="sxs-lookup"><span data-stu-id="298d3-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="298d3-109"><span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**\_desbordamiento de pila de errores \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-109"><span id="ERROR_STACK_OVERFLOW"></span><span id="error_stack_overflow"></span>**ERROR\_STACK\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-110">1001 (0x3E9)</span><span class="sxs-lookup"><span data-stu-id="298d3-110">1001 (0x3E9)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-111">Recursividad demasiado profunda; desbordamiento de la pila.</span><span class="sxs-lookup"><span data-stu-id="298d3-111">Recursion too deep; the stack overflowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-112"><span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**ERROR \_ de \_ mensaje no válido**</span><span class="sxs-lookup"><span data-stu-id="298d3-112"><span id="ERROR_INVALID_MESSAGE"></span><span id="error_invalid_message"></span>**ERROR\_INVALID\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-113">1002 (0x3EA)</span><span class="sxs-lookup"><span data-stu-id="298d3-113">1002 (0x3EA)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-114">La ventana no puede actuar sobre el mensaje enviado.</span><span class="sxs-lookup"><span data-stu-id="298d3-114">The window cannot act on the sent message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-115"><span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**\_no se \_ puede \_ completar el error**</span><span class="sxs-lookup"><span data-stu-id="298d3-115"><span id="ERROR_CAN_NOT_COMPLETE"></span><span id="error_can_not_complete"></span>**ERROR\_CAN\_NOT\_COMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-116">1003 (0x3EB)</span><span class="sxs-lookup"><span data-stu-id="298d3-116">1003 (0x3EB)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-117">No se puede completar esta función.</span><span class="sxs-lookup"><span data-stu-id="298d3-117">Cannot complete this function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-118"><span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**ERROR de \_ marcas no válidas \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-118"><span id="ERROR_INVALID_FLAGS"></span><span id="error_invalid_flags"></span>**ERROR\_INVALID\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-119">1004 (0x3EC)</span><span class="sxs-lookup"><span data-stu-id="298d3-119">1004 (0x3EC)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-120">Marcas no válidas.</span><span class="sxs-lookup"><span data-stu-id="298d3-120">Invalid flags.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-121"><span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERROR de \_ \_ volumen desconocido**</span><span class="sxs-lookup"><span data-stu-id="298d3-121"><span id="ERROR_UNRECOGNIZED_VOLUME"></span><span id="error_unrecognized_volume"></span>**ERROR\_UNRECOGNIZED\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-122">1005 (0x3ED)</span><span class="sxs-lookup"><span data-stu-id="298d3-122">1005 (0x3ED)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-123">El volumen no contiene un sistema de archivos reconocido.</span><span class="sxs-lookup"><span data-stu-id="298d3-123">The volume does not contain a recognized file system.</span></span> <span data-ttu-id="298d3-124">Asegúrese de que todos los controladores del sistema de archivos necesarios estén cargados y de que el volumen no esté dañado.</span><span class="sxs-lookup"><span data-stu-id="298d3-124">Please make sure that all required file system drivers are loaded and that the volume is not corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-125"><span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**archivo de ERROR \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="298d3-125"><span id="ERROR_FILE_INVALID"></span><span id="error_file_invalid"></span>**ERROR\_FILE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-126">1006 (0x3EE)</span><span class="sxs-lookup"><span data-stu-id="298d3-126">1006 (0x3EE)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-127">El volumen de un archivo se ha modificado externamente, por lo que el archivo abierto ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-127">The volume for a file has been externally altered so that the opened file is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-128"><span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**ERROR en \_ modo de pantalla completa \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-128"><span id="ERROR_FULLSCREEN_MODE"></span><span id="error_fullscreen_mode"></span>**ERROR\_FULLSCREEN\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-129">1007 (0x3EF)</span><span class="sxs-lookup"><span data-stu-id="298d3-129">1007 (0x3EF)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-130">La operación solicitada no se puede realizar en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="298d3-130">The requested operation cannot be performed in full-screen mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-131"><span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERROR: \_ no hay \_ token**</span><span class="sxs-lookup"><span data-stu-id="298d3-131"><span id="ERROR_NO_TOKEN"></span><span id="error_no_token"></span>**ERROR\_NO\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-132">1008 (0x3F0)</span><span class="sxs-lookup"><span data-stu-id="298d3-132">1008 (0x3F0)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-133">Se ha intentado hacer referencia a un token que no existe.</span><span class="sxs-lookup"><span data-stu-id="298d3-133">An attempt was made to reference a token that does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-134"><span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERROR \_ BADDB**</span><span class="sxs-lookup"><span data-stu-id="298d3-134"><span id="ERROR_BADDB"></span><span id="error_baddb"></span>**ERROR\_BADDB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-135">1009 (0x3F1)</span><span class="sxs-lookup"><span data-stu-id="298d3-135">1009 (0x3F1)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-136">La base de datos del registro de configuración está dañada.</span><span class="sxs-lookup"><span data-stu-id="298d3-136">The configuration registry database is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-137"><span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERROR \_ BADKEY**</span><span class="sxs-lookup"><span data-stu-id="298d3-137"><span id="ERROR_BADKEY"></span><span id="error_badkey"></span>**ERROR\_BADKEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-138">1010 (0x3F2)</span><span class="sxs-lookup"><span data-stu-id="298d3-138">1010 (0x3F2)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-139">La clave del registro de configuración no es válida.</span><span class="sxs-lookup"><span data-stu-id="298d3-139">The configuration registry key is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-140"><span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERROR \_ CANTOPEN**</span><span class="sxs-lookup"><span data-stu-id="298d3-140"><span id="ERROR_CANTOPEN"></span><span id="error_cantopen"></span>**ERROR\_CANTOPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-141">1011 (0x3F3)</span><span class="sxs-lookup"><span data-stu-id="298d3-141">1011 (0x3F3)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-142">No se pudo abrir la clave del registro de configuración.</span><span class="sxs-lookup"><span data-stu-id="298d3-142">The configuration registry key could not be opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-143"><span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERROR \_ CANTREAD**</span><span class="sxs-lookup"><span data-stu-id="298d3-143"><span id="ERROR_CANTREAD"></span><span id="error_cantread"></span>**ERROR\_CANTREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-144">1012 (0x3F4)</span><span class="sxs-lookup"><span data-stu-id="298d3-144">1012 (0x3F4)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-145">No se pudo leer la clave del registro de configuración.</span><span class="sxs-lookup"><span data-stu-id="298d3-145">The configuration registry key could not be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-146"><span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERROR \_ CANTWRITE**</span><span class="sxs-lookup"><span data-stu-id="298d3-146"><span id="ERROR_CANTWRITE"></span><span id="error_cantwrite"></span>**ERROR\_CANTWRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-147">1013 (0x3F5)</span><span class="sxs-lookup"><span data-stu-id="298d3-147">1013 (0x3F5)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-148">No se pudo escribir la clave del registro de configuración.</span><span class="sxs-lookup"><span data-stu-id="298d3-148">The configuration registry key could not be written.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-149"><span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**registro de errores \_ \_ recuperado**</span><span class="sxs-lookup"><span data-stu-id="298d3-149"><span id="ERROR_REGISTRY_RECOVERED"></span><span id="error_registry_recovered"></span>**ERROR\_REGISTRY\_RECOVERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-150">1014 (0x3F6)</span><span class="sxs-lookup"><span data-stu-id="298d3-150">1014 (0x3F6)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-151">Uno de los archivos de la base de datos del registro tenía que recuperarse mediante el uso de un registro o una copia alternativa.</span><span class="sxs-lookup"><span data-stu-id="298d3-151">One of the files in the registry database had to be recovered by use of a log or alternate copy.</span></span> <span data-ttu-id="298d3-152">La recuperación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="298d3-152">The recovery was successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-153"><span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**registro de errores \_ \_ dañado**</span><span class="sxs-lookup"><span data-stu-id="298d3-153"><span id="ERROR_REGISTRY_CORRUPT"></span><span id="error_registry_corrupt"></span>**ERROR\_REGISTRY\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-154">1015 (0x3F7)</span><span class="sxs-lookup"><span data-stu-id="298d3-154">1015 (0x3F7)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-155">El registro está dañado.</span><span class="sxs-lookup"><span data-stu-id="298d3-155">The registry is corrupted.</span></span> <span data-ttu-id="298d3-156">La estructura de uno de los archivos que contiene datos del registro está dañada o la imagen de memoria del sistema del archivo está dañada, o bien no se pudo recuperar el archivo porque la copia o el registro alternativos no estaban presentes o estaban dañados.</span><span class="sxs-lookup"><span data-stu-id="298d3-156">The structure of one of the files containing registry data is corrupted, or the system's memory image of the file is corrupted, or the file could not be recovered because the alternate copy or log was absent or corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-157"><span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**ERROR \_ de \_ e/s del registro de errores \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-157"><span id="ERROR_REGISTRY_IO_FAILED"></span><span id="error_registry_io_failed"></span>**ERROR\_REGISTRY\_IO\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-158">1016 (0x3F8)</span><span class="sxs-lookup"><span data-stu-id="298d3-158">1016 (0x3F8)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-159">Error irrecuperable en una operación de e/s iniciada por el registro.</span><span class="sxs-lookup"><span data-stu-id="298d3-159">An I/O operation initiated by the registry failed unrecoverably.</span></span> <span data-ttu-id="298d3-160">El registro no pudo leer, escribir o vaciar, uno de los archivos que contienen la imagen del sistema del registro.</span><span class="sxs-lookup"><span data-stu-id="298d3-160">The registry could not read in, or write out, or flush, one of the files that contain the system's image of the registry.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-161"><span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**no se pudo obtener el \_ \_ archivo de registro \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-161"><span id="ERROR_NOT_REGISTRY_FILE"></span><span id="error_not_registry_file"></span>**ERROR\_NOT\_REGISTRY\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-162">1017 (0x3F9)</span><span class="sxs-lookup"><span data-stu-id="298d3-162">1017 (0x3F9)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-163">El sistema intentó cargar o restaurar un archivo en el registro, pero el archivo especificado no se encuentra en un formato de archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="298d3-163">The system has attempted to load or restore a file into the registry, but the specified file is not in a registry file format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-164"><span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**clave de ERROR \_ \_ eliminada**</span><span class="sxs-lookup"><span data-stu-id="298d3-164"><span id="ERROR_KEY_DELETED"></span><span id="error_key_deleted"></span>**ERROR\_KEY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-165">1018 (0x3FA)</span><span class="sxs-lookup"><span data-stu-id="298d3-165">1018 (0x3FA)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-166">Se intentó realizar una operación no válida en una clave del registro que se ha marcado para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="298d3-166">Illegal operation attempted on a registry key that has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-167"><span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERROR: \_ no hay \_ espacio de registro \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-167"><span id="ERROR_NO_LOG_SPACE"></span><span id="error_no_log_space"></span>**ERROR\_NO\_LOG\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-168">1019 (0x3FB)</span><span class="sxs-lookup"><span data-stu-id="298d3-168">1019 (0x3FB)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-169">El sistema no pudo asignar el espacio necesario en un registro del registro.</span><span class="sxs-lookup"><span data-stu-id="298d3-169">System could not allocate the required space in a registry log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-170"><span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**la \_ clave de error \_ tiene \_ elementos secundarios**</span><span class="sxs-lookup"><span data-stu-id="298d3-170"><span id="ERROR_KEY_HAS_CHILDREN"></span><span id="error_key_has_children"></span>**ERROR\_KEY\_HAS\_CHILDREN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-171">1020 (0x3FC)</span><span class="sxs-lookup"><span data-stu-id="298d3-171">1020 (0x3FC)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-172">No se puede crear un vínculo simbólico en una clave del registro que ya tiene subclaves o valores.</span><span class="sxs-lookup"><span data-stu-id="298d3-172">Cannot create a symbolic link in a registry key that already has subkeys or values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-173"><span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**el \_ secundario del error \_ debe \_ ser \_ volátil**</span><span class="sxs-lookup"><span data-stu-id="298d3-173"><span id="ERROR_CHILD_MUST_BE_VOLATILE"></span><span id="error_child_must_be_volatile"></span>**ERROR\_CHILD\_MUST\_BE\_VOLATILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-174">1021 (0x3FD)</span><span class="sxs-lookup"><span data-stu-id="298d3-174">1021 (0x3FD)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-175">No se puede crear una subclave estable en una clave primaria volátil.</span><span class="sxs-lookup"><span data-stu-id="298d3-175">Cannot create a stable subkey under a volatile parent key.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-176"><span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERROR de \_ notificación de \_ enumeración \_ dir**</span><span class="sxs-lookup"><span data-stu-id="298d3-176"><span id="ERROR_NOTIFY_ENUM_DIR"></span><span id="error_notify_enum_dir"></span>**ERROR\_NOTIFY\_ENUM\_DIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-177">1022 (0x3FE)</span><span class="sxs-lookup"><span data-stu-id="298d3-177">1022 (0x3FE)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-178">Se está completando una solicitud de notificación de cambio y la información no se devuelve en el búfer del llamador.</span><span class="sxs-lookup"><span data-stu-id="298d3-178">A notify change request is being completed and the information is not being returned in the caller's buffer.</span></span> <span data-ttu-id="298d3-179">Ahora, el autor de la llamada necesita enumerar los archivos para buscar los cambios.</span><span class="sxs-lookup"><span data-stu-id="298d3-179">The caller now needs to enumerate the files to find the changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-180"><span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**\_servicios dependientes de errores en \_ \_ ejecución**</span><span class="sxs-lookup"><span data-stu-id="298d3-180"><span id="ERROR_DEPENDENT_SERVICES_RUNNING"></span><span id="error_dependent_services_running"></span>**ERROR\_DEPENDENT\_SERVICES\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-181">1051 (0x41B)</span><span class="sxs-lookup"><span data-stu-id="298d3-181">1051 (0x41B)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-182">Se ha enviado un control de detención a un servicio del que dependen otros servicios en ejecución.</span><span class="sxs-lookup"><span data-stu-id="298d3-182">A stop control has been sent to a service that other running services are dependent on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-183"><span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERROR \_ de \_ control de servicio no válido \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-183"><span id="ERROR_INVALID_SERVICE_CONTROL"></span><span id="error_invalid_service_control"></span>**ERROR\_INVALID\_SERVICE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-184">1052 (0x41C)</span><span class="sxs-lookup"><span data-stu-id="298d3-184">1052 (0x41C)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-185">El control solicitado no es válido para este servicio.</span><span class="sxs-lookup"><span data-stu-id="298d3-185">The requested control is not valid for this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-186"><span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**\_tiempo de \_ espera de solicitud de servicio de error \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-186"><span id="ERROR_SERVICE_REQUEST_TIMEOUT"></span><span id="error_service_request_timeout"></span>**ERROR\_SERVICE\_REQUEST\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-187">1053 (0x41D)</span><span class="sxs-lookup"><span data-stu-id="298d3-187">1053 (0x41D)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-188">El servicio no respondió a la petición de inicio o control de manera oportuna.</span><span class="sxs-lookup"><span data-stu-id="298d3-188">The service did not respond to the start or control request in a timely fashion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-189"><span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**ERROR de \_ servicio \_ sin \_ subproceso**</span><span class="sxs-lookup"><span data-stu-id="298d3-189"><span id="ERROR_SERVICE_NO_THREAD"></span><span id="error_service_no_thread"></span>**ERROR\_SERVICE\_NO\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-190">1054 (0x41E)</span><span class="sxs-lookup"><span data-stu-id="298d3-190">1054 (0x41E)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-191">No se pudo crear un subproceso para el servicio.</span><span class="sxs-lookup"><span data-stu-id="298d3-191">A thread could not be created for the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-192"><span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**base de datos de servicio de ERROR \_ \_ \_ bloqueada**</span><span class="sxs-lookup"><span data-stu-id="298d3-192"><span id="ERROR_SERVICE_DATABASE_LOCKED"></span><span id="error_service_database_locked"></span>**ERROR\_SERVICE\_DATABASE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-193">1055 (0x41F)</span><span class="sxs-lookup"><span data-stu-id="298d3-193">1055 (0x41F)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-194">La base de datos del servicio está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="298d3-194">The service database is locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-195"><span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**el \_ servicio de error \_ ya se \_ está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="298d3-195"><span id="ERROR_SERVICE_ALREADY_RUNNING"></span><span id="error_service_already_running"></span>**ERROR\_SERVICE\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-196">1056 (0x420)</span><span class="sxs-lookup"><span data-stu-id="298d3-196">1056 (0x420)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-197">Ya se está ejecutando una instancia del servicio.</span><span class="sxs-lookup"><span data-stu-id="298d3-197">An instance of the service is already running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-198"><span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERROR \_ de \_ cuenta de servicio no válida \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-198"><span id="ERROR_INVALID_SERVICE_ACCOUNT"></span><span id="error_invalid_service_account"></span>**ERROR\_INVALID\_SERVICE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-199">1057 (0x421)</span><span class="sxs-lookup"><span data-stu-id="298d3-199">1057 (0x421)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-200">El nombre de cuenta no es válido o no existe o la contraseña no es válida para el nombre de cuenta especificado.</span><span class="sxs-lookup"><span data-stu-id="298d3-200">The account name is invalid or does not exist, or the password is invalid for the account name specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-201"><span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**servicio de ERROR \_ \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="298d3-201"><span id="ERROR_SERVICE_DISABLED"></span><span id="error_service_disabled"></span>**ERROR\_SERVICE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-202">1058 (0x422)</span><span class="sxs-lookup"><span data-stu-id="298d3-202">1058 (0x422)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-203">No se puede iniciar el servicio porque está deshabilitado o porque no tiene ningún dispositivo habilitado asociado.</span><span class="sxs-lookup"><span data-stu-id="298d3-203">The service cannot be started, either because it is disabled or because it has no enabled devices associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-204"><span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**ERROR \_ de \_ dependencia circular**</span><span class="sxs-lookup"><span data-stu-id="298d3-204"><span id="ERROR_CIRCULAR_DEPENDENCY"></span><span id="error_circular_dependency"></span>**ERROR\_CIRCULAR\_DEPENDENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-205">1059 (0x423)</span><span class="sxs-lookup"><span data-stu-id="298d3-205">1059 (0x423)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-206">Se especificó una dependencia de servicio circular.</span><span class="sxs-lookup"><span data-stu-id="298d3-206">Circular service dependency was specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-207"><span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**el servicio de ERROR no \_ \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="298d3-207"><span id="ERROR_SERVICE_DOES_NOT_EXIST"></span><span id="error_service_does_not_exist"></span>**ERROR\_SERVICE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-208">1060 (0x424)</span><span class="sxs-lookup"><span data-stu-id="298d3-208">1060 (0x424)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-209">El servicio especificado no existe como servicio instalado.</span><span class="sxs-lookup"><span data-stu-id="298d3-209">The specified service does not exist as an installed service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-210"><span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**el \_ servicio de error \_ no puede \_ Aceptar \_ Ctrl**</span><span class="sxs-lookup"><span data-stu-id="298d3-210"><span id="ERROR_SERVICE_CANNOT_ACCEPT_CTRL"></span><span id="error_service_cannot_accept_ctrl"></span>**ERROR\_SERVICE\_CANNOT\_ACCEPT\_CTRL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-211">1061 (0x425)</span><span class="sxs-lookup"><span data-stu-id="298d3-211">1061 (0x425)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-212">El servicio no puede aceptar mensajes de control en este momento.</span><span class="sxs-lookup"><span data-stu-id="298d3-212">The service cannot accept control messages at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-213"><span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**servicio de ERROR \_ \_ no \_ activo**</span><span class="sxs-lookup"><span data-stu-id="298d3-213"><span id="ERROR_SERVICE_NOT_ACTIVE"></span><span id="error_service_not_active"></span>**ERROR\_SERVICE\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-214">1062 (0x426 al)</span><span class="sxs-lookup"><span data-stu-id="298d3-214">1062 (0x426)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-215">El servicio no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="298d3-215">The service has not been started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-216"><span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERROR \_ al \_ \_ conectar el controlador de servicio \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-216"><span id="ERROR_FAILED_SERVICE_CONTROLLER_CONNECT"></span><span id="error_failed_service_controller_connect"></span>**ERROR\_FAILED\_SERVICE\_CONTROLLER\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-217">1063 (0x427)</span><span class="sxs-lookup"><span data-stu-id="298d3-217">1063 (0x427)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-218">El proceso de servicio no se pudo conectar al controlador de servicio.</span><span class="sxs-lookup"><span data-stu-id="298d3-218">The service process could not connect to the service controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-219"><span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**\_excepción \_ de error en el \_ servicio**</span><span class="sxs-lookup"><span data-stu-id="298d3-219"><span id="ERROR_EXCEPTION_IN_SERVICE"></span><span id="error_exception_in_service"></span>**ERROR\_EXCEPTION\_IN\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-220">1064 (0x428)</span><span class="sxs-lookup"><span data-stu-id="298d3-220">1064 (0x428)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-221">Se produjo una excepción en el servicio al controlar la solicitud de control.</span><span class="sxs-lookup"><span data-stu-id="298d3-221">An exception occurred in the service when handling the control request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-222"><span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**la base de datos de errores no \_ \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="298d3-222"><span id="ERROR_DATABASE_DOES_NOT_EXIST"></span><span id="error_database_does_not_exist"></span>**ERROR\_DATABASE\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-223">1065 (0x429)</span><span class="sxs-lookup"><span data-stu-id="298d3-223">1065 (0x429)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-224">La base de datos especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="298d3-224">The database specified does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-225"><span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**\_ \_ error específico del servicio de error \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-225"><span id="ERROR_SERVICE_SPECIFIC_ERROR"></span><span id="error_service_specific_error"></span>**ERROR\_SERVICE\_SPECIFIC\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-226">1066 (0x42A)</span><span class="sxs-lookup"><span data-stu-id="298d3-226">1066 (0x42A)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-227">El servicio ha devuelto un código de error específico del servicio.</span><span class="sxs-lookup"><span data-stu-id="298d3-227">The service has returned a service-specific error code.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-228"><span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**ERROR en el \_ proceso \_ anulado**</span><span class="sxs-lookup"><span data-stu-id="298d3-228"><span id="ERROR_PROCESS_ABORTED"></span><span id="error_process_aborted"></span>**ERROR\_PROCESS\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-229">1067 (0x42B)</span><span class="sxs-lookup"><span data-stu-id="298d3-229">1067 (0x42B)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-230">El proceso finalizó inesperadamente.</span><span class="sxs-lookup"><span data-stu-id="298d3-230">The process terminated unexpectedly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-231"><span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**ERROR de \_ dependencia de servicio de error \_ \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-231"><span id="ERROR_SERVICE_DEPENDENCY_FAIL"></span><span id="error_service_dependency_fail"></span>**ERROR\_SERVICE\_DEPENDENCY\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-232">1068 (0x42C)</span><span class="sxs-lookup"><span data-stu-id="298d3-232">1068 (0x42C)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-233">No se pudo iniciar el servicio o grupo de dependencia.</span><span class="sxs-lookup"><span data-stu-id="298d3-233">The dependency service or group failed to start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-234"><span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**ERROR \_ de \_ Inicio de sesión del servicio \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-234"><span id="ERROR_SERVICE_LOGON_FAILED"></span><span id="error_service_logon_failed"></span>**ERROR\_SERVICE\_LOGON\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-235">1069 (0x42D)</span><span class="sxs-lookup"><span data-stu-id="298d3-235">1069 (0x42D)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-236">El servicio no se inició debido a un error de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="298d3-236">The service did not start due to a logon failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-237"><span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**ERROR al \_ iniciar el servicio de error \_ \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-237"><span id="ERROR_SERVICE_START_HANG"></span><span id="error_service_start_hang"></span>**ERROR\_SERVICE\_START\_HANG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-238">1070 (0x42E)</span><span class="sxs-lookup"><span data-stu-id="298d3-238">1070 (0x42E)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-239">Después de iniciarse, el servicio permanece en estado pendiente de inicio.</span><span class="sxs-lookup"><span data-stu-id="298d3-239">After starting, the service hung in a start-pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-240"><span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERROR \_ de \_ bloqueo de servicio no válido \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-240"><span id="ERROR_INVALID_SERVICE_LOCK"></span><span id="error_invalid_service_lock"></span>**ERROR\_INVALID\_SERVICE\_LOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-241">1071 (0x42F)</span><span class="sxs-lookup"><span data-stu-id="298d3-241">1071 (0x42F)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-242">El bloqueo de la base de datos del servicio especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-242">The specified service database lock is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-243"><span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**\_servicio \_ de error marcado \_ para \_ eliminación**</span><span class="sxs-lookup"><span data-stu-id="298d3-243"><span id="ERROR_SERVICE_MARKED_FOR_DELETE"></span><span id="error_service_marked_for_delete"></span>**ERROR\_SERVICE\_MARKED\_FOR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-244">1072 (0x430)</span><span class="sxs-lookup"><span data-stu-id="298d3-244">1072 (0x430)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-245">El servicio especificado se ha marcado para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="298d3-245">The specified service has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-246"><span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**el \_ servicio de error \_ existe**</span><span class="sxs-lookup"><span data-stu-id="298d3-246"><span id="ERROR_SERVICE_EXISTS"></span><span id="error_service_exists"></span>**ERROR\_SERVICE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-247">1073 (0x431)</span><span class="sxs-lookup"><span data-stu-id="298d3-247">1073 (0x431)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-248">El servicio especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="298d3-248">The specified service already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-249"><span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**ERROR \_ al \_ ejecutar \_ válida conocida**</span><span class="sxs-lookup"><span data-stu-id="298d3-249"><span id="ERROR_ALREADY_RUNNING_LKG"></span><span id="error_already_running_lkg"></span>**ERROR\_ALREADY\_RUNNING\_LKG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-250">1074 (0x432)</span><span class="sxs-lookup"><span data-stu-id="298d3-250">1074 (0x432)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-251">El sistema se está ejecutando actualmente con la última configuración válida conocida.</span><span class="sxs-lookup"><span data-stu-id="298d3-251">The system is currently running with the last-known-good configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-252"><span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**dependencia de servicio de ERROR \_ \_ \_ eliminada**</span><span class="sxs-lookup"><span data-stu-id="298d3-252"><span id="ERROR_SERVICE_DEPENDENCY_DELETED"></span><span id="error_service_dependency_deleted"></span>**ERROR\_SERVICE\_DEPENDENCY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-253">1075 (0x433)</span><span class="sxs-lookup"><span data-stu-id="298d3-253">1075 (0x433)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-254">El servicio de dependencia no existe o se ha marcado para su eliminación.</span><span class="sxs-lookup"><span data-stu-id="298d3-254">The dependency service does not exist or has been marked for deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-255"><span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**el \_ Inicio de error \_ ya se \_ aceptó**</span><span class="sxs-lookup"><span data-stu-id="298d3-255"><span id="ERROR_BOOT_ALREADY_ACCEPTED"></span><span id="error_boot_already_accepted"></span>**ERROR\_BOOT\_ALREADY\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-256">1076 (0x434)</span><span class="sxs-lookup"><span data-stu-id="298d3-256">1076 (0x434)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-257">El arranque actual ya se aceptó para su uso como el último conjunto de control válido conocido.</span><span class="sxs-lookup"><span data-stu-id="298d3-257">The current boot has already been accepted for use as the last-known-good control set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-258"><span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**no \_ se \_ ha iniciado nunca el servicio de errores \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-258"><span id="ERROR_SERVICE_NEVER_STARTED"></span><span id="error_service_never_started"></span>**ERROR\_SERVICE\_NEVER\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-259">1077 (0x435)</span><span class="sxs-lookup"><span data-stu-id="298d3-259">1077 (0x435)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-260">No se ha realizado ningún intento de iniciar el servicio desde el último arranque.</span><span class="sxs-lookup"><span data-stu-id="298d3-260">No attempts to start the service have been made since the last boot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-261"><span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**ERROR \_ de \_ nombre de servicio duplicado \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-261"><span id="ERROR_DUPLICATE_SERVICE_NAME"></span><span id="error_duplicate_service_name"></span>**ERROR\_DUPLICATE\_SERVICE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-262">1078 (0x436)</span><span class="sxs-lookup"><span data-stu-id="298d3-262">1078 (0x436)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-263">El nombre ya está en uso como nombre de servicio o como nombre para mostrar del servicio.</span><span class="sxs-lookup"><span data-stu-id="298d3-263">The name is already in use as either a service name or a service display name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-264"><span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERROR \_ de \_ cuenta de servicio diferente \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-264"><span id="ERROR_DIFFERENT_SERVICE_ACCOUNT"></span><span id="error_different_service_account"></span>**ERROR\_DIFFERENT\_SERVICE\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-265">1079 (0x437)</span><span class="sxs-lookup"><span data-stu-id="298d3-265">1079 (0x437)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-266">La cuenta especificada para este servicio es diferente de la cuenta especificada para otros servicios que se ejecutan en el mismo proceso.</span><span class="sxs-lookup"><span data-stu-id="298d3-266">The account specified for this service is different from the account specified for other services running in the same process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-267"><span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**ERROR: \_ no se puede \_ detectar el \_ error del controlador \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-267"><span id="ERROR_CANNOT_DETECT_DRIVER_FAILURE"></span><span id="error_cannot_detect_driver_failure"></span>**ERROR\_CANNOT\_DETECT\_DRIVER\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-268">1080 (0x438)</span><span class="sxs-lookup"><span data-stu-id="298d3-268">1080 (0x438)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-269">Las acciones de error solo se pueden establecer para los servicios de Win32, no para los controladores.</span><span class="sxs-lookup"><span data-stu-id="298d3-269">Failure actions can only be set for Win32 services, not for drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-270"><span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERROR \_ no se puede \_ detectar la \_ \_ anulación del proceso**</span><span class="sxs-lookup"><span data-stu-id="298d3-270"><span id="ERROR_CANNOT_DETECT_PROCESS_ABORT"></span><span id="error_cannot_detect_process_abort"></span>**ERROR\_CANNOT\_DETECT\_PROCESS\_ABORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-271">1081 (0x439)</span><span class="sxs-lookup"><span data-stu-id="298d3-271">1081 (0x439)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-272">Este servicio se ejecuta en el mismo proceso que el administrador de control de servicios.</span><span class="sxs-lookup"><span data-stu-id="298d3-272">This service runs in the same process as the service control manager.</span></span> <span data-ttu-id="298d3-273">Por lo tanto, el administrador de control de servicios no puede tomar medidas si el proceso de este servicio finaliza de forma inesperada.</span><span class="sxs-lookup"><span data-stu-id="298d3-273">Therefore, the service control manager cannot take action if this service's process terminates unexpectedly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-274"><span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERROR: \_ no hay \_ programa de recuperación \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-274"><span id="ERROR_NO_RECOVERY_PROGRAM"></span><span id="error_no_recovery_program"></span>**ERROR\_NO\_RECOVERY\_PROGRAM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-275">1082 (0x43A)</span><span class="sxs-lookup"><span data-stu-id="298d3-275">1082 (0x43A)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-276">No se ha configurado ningún programa de recuperación para este servicio.</span><span class="sxs-lookup"><span data-stu-id="298d3-276">No recovery program has been configured for this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-277"><span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**ERROR el \_ servicio \_ no está en el \_ \_ archivo exe**</span><span class="sxs-lookup"><span data-stu-id="298d3-277"><span id="ERROR_SERVICE_NOT_IN_EXE"></span><span id="error_service_not_in_exe"></span>**ERROR\_SERVICE\_NOT\_IN\_EXE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-278">1083 (0x43B)</span><span class="sxs-lookup"><span data-stu-id="298d3-278">1083 (0x43B)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-279">El programa ejecutable para el que este servicio está configurado para ejecutarse no implementa el servicio.</span><span class="sxs-lookup"><span data-stu-id="298d3-279">The executable program that this service is configured to run in does not implement the service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-280"><span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERROR \_ no \_ \_ servicio SafeBoot**</span><span class="sxs-lookup"><span data-stu-id="298d3-280"><span id="ERROR_NOT_SAFEBOOT_SERVICE"></span><span id="error_not_safeboot_service"></span>**ERROR\_NOT\_SAFEBOOT\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-281">1084 (0x43C)</span><span class="sxs-lookup"><span data-stu-id="298d3-281">1084 (0x43C)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-282">Este servicio no se puede iniciar en modo seguro.</span><span class="sxs-lookup"><span data-stu-id="298d3-282">This service cannot be started in Safe Mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-283"><span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**\_fin \_ del error de \_ medio**</span><span class="sxs-lookup"><span data-stu-id="298d3-283"><span id="ERROR_END_OF_MEDIA"></span><span id="error_end_of_media"></span>**ERROR\_END\_OF\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-284">1100 (0x44C)</span><span class="sxs-lookup"><span data-stu-id="298d3-284">1100 (0x44C)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-285">Se ha alcanzado el final físico de la cinta.</span><span class="sxs-lookup"><span data-stu-id="298d3-285">The physical end of the tape has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-286"><span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**marca de ERROR de ERROR \_ \_ detectada**</span><span class="sxs-lookup"><span data-stu-id="298d3-286"><span id="ERROR_FILEMARK_DETECTED"></span><span id="error_filemark_detected"></span>**ERROR\_FILEMARK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-287">1101 (0x44D)</span><span class="sxs-lookup"><span data-stu-id="298d3-287">1101 (0x44D)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-288">Un acceso a cinta ha alcanzado una marca de acceso.</span><span class="sxs-lookup"><span data-stu-id="298d3-288">A tape access reached a filemark.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-289"><span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERROR al \_ iniciar el \_ \_ medio**</span><span class="sxs-lookup"><span data-stu-id="298d3-289"><span id="ERROR_BEGINNING_OF_MEDIA"></span><span id="error_beginning_of_media"></span>**ERROR\_BEGINNING\_OF\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-290">1102 (0x44E)</span><span class="sxs-lookup"><span data-stu-id="298d3-290">1102 (0x44E)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-291">Se encontró el principio de la cinta o una partición.</span><span class="sxs-lookup"><span data-stu-id="298d3-291">The beginning of the tape or a partition was encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-292"><span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**ERROR \_ SETMARK \_ detectado**</span><span class="sxs-lookup"><span data-stu-id="298d3-292"><span id="ERROR_SETMARK_DETECTED"></span><span id="error_setmark_detected"></span>**ERROR\_SETMARK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-293">1103 (0x44F)</span><span class="sxs-lookup"><span data-stu-id="298d3-293">1103 (0x44F)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-294">Un acceso a cinta llegó al final de un conjunto de archivos.</span><span class="sxs-lookup"><span data-stu-id="298d3-294">A tape access reached the end of a set of files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-295"><span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERROR \_ no \_ se \_ detectó ningún dato**</span><span class="sxs-lookup"><span data-stu-id="298d3-295"><span id="ERROR_NO_DATA_DETECTED"></span><span id="error_no_data_detected"></span>**ERROR\_NO\_DATA\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-296">1104 (0x450)</span><span class="sxs-lookup"><span data-stu-id="298d3-296">1104 (0x450)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-297">No hay más datos en la cinta.</span><span class="sxs-lookup"><span data-stu-id="298d3-297">No more data is on the tape.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-298"><span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**ERROR de \_ partición \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-298"><span id="ERROR_PARTITION_FAILURE"></span><span id="error_partition_failure"></span>**ERROR\_PARTITION\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-299">1105 (0x451)</span><span class="sxs-lookup"><span data-stu-id="298d3-299">1105 (0x451)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-300">No se pudo crear la partición de la cinta.</span><span class="sxs-lookup"><span data-stu-id="298d3-300">Tape could not be partitioned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-301"><span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERROR \_ de \_ longitud de bloque no válida \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-301"><span id="ERROR_INVALID_BLOCK_LENGTH"></span><span id="error_invalid_block_length"></span>**ERROR\_INVALID\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-302">1106 (0x452)</span><span class="sxs-lookup"><span data-stu-id="298d3-302">1106 (0x452)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-303">Al acceder a una nueva cinta de una partición multivolumen, el tamaño de bloque actual es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="298d3-303">When accessing a new tape of a multivolume partition, the current block size is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-304"><span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**el \_ dispositivo de error \_ no tiene \_ particiones**</span><span class="sxs-lookup"><span data-stu-id="298d3-304"><span id="ERROR_DEVICE_NOT_PARTITIONED"></span><span id="error_device_not_partitioned"></span>**ERROR\_DEVICE\_NOT\_PARTITIONED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-305">1107 (0x453)</span><span class="sxs-lookup"><span data-stu-id="298d3-305">1107 (0x453)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-306">No se encontró la información de la partición de cinta al cargar una cinta.</span><span class="sxs-lookup"><span data-stu-id="298d3-306">Tape partition information could not be found when loading a tape.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-307"><span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERROR \_ no se puede \_ \_ bloquear el \_ medio**</span><span class="sxs-lookup"><span data-stu-id="298d3-307"><span id="ERROR_UNABLE_TO_LOCK_MEDIA"></span><span id="error_unable_to_lock_media"></span>**ERROR\_UNABLE\_TO\_LOCK\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-308">1108 (0x454)</span><span class="sxs-lookup"><span data-stu-id="298d3-308">1108 (0x454)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-309">No se puede bloquear el mecanismo de expulsión de medios.</span><span class="sxs-lookup"><span data-stu-id="298d3-309">Unable to lock the media eject mechanism.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-310"><span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**ERROR: \_ no se puede \_ descargar el \_ \_ medio**</span><span class="sxs-lookup"><span data-stu-id="298d3-310"><span id="ERROR_UNABLE_TO_UNLOAD_MEDIA"></span><span id="error_unable_to_unload_media"></span>**ERROR\_UNABLE\_TO\_UNLOAD\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-311">1109 (0x455)</span><span class="sxs-lookup"><span data-stu-id="298d3-311">1109 (0x455)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-312">No se puede descargar el medio.</span><span class="sxs-lookup"><span data-stu-id="298d3-312">Unable to unload the media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-313"><span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**medios de ERROR \_ \_ modificados**</span><span class="sxs-lookup"><span data-stu-id="298d3-313"><span id="ERROR_MEDIA_CHANGED"></span><span id="error_media_changed"></span>**ERROR\_MEDIA\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-314">1110 (0x456)</span><span class="sxs-lookup"><span data-stu-id="298d3-314">1110 (0x456)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-315">Es posible que el medio de la unidad haya cambiado.</span><span class="sxs-lookup"><span data-stu-id="298d3-315">The media in the drive may have changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-316"><span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**\_restablecimiento del bus de error \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-316"><span id="ERROR_BUS_RESET"></span><span id="error_bus_reset"></span>**ERROR\_BUS\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-317">1111 (0x457)</span><span class="sxs-lookup"><span data-stu-id="298d3-317">1111 (0x457)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-318">Se restableció el bus de e/s.</span><span class="sxs-lookup"><span data-stu-id="298d3-318">The I/O bus was reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-319"><span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERROR: \_ no hay \_ medios \_ en la \_ unidad**</span><span class="sxs-lookup"><span data-stu-id="298d3-319"><span id="ERROR_NO_MEDIA_IN_DRIVE"></span><span id="error_no_media_in_drive"></span>**ERROR\_NO\_MEDIA\_IN\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-320">1112 (0x458)</span><span class="sxs-lookup"><span data-stu-id="298d3-320">1112 (0x458)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-321">No hay medios en la unidad.</span><span class="sxs-lookup"><span data-stu-id="298d3-321">No media in drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-322"><span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERROR \_ sin \_ traducción Unicode \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-322"><span id="ERROR_NO_UNICODE_TRANSLATION"></span><span id="error_no_unicode_translation"></span>**ERROR\_NO\_UNICODE\_TRANSLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-323">1113 (0x459)</span><span class="sxs-lookup"><span data-stu-id="298d3-323">1113 (0x459)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-324">No existe ninguna asignación para el carácter Unicode en la página de códigos multibyte de destino.</span><span class="sxs-lookup"><span data-stu-id="298d3-324">No mapping for the Unicode character exists in the target multi-byte code page.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-325"><span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**ERROR \_ \_ al inicializar el archivo dll \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-325"><span id="ERROR_DLL_INIT_FAILED"></span><span id="error_dll_init_failed"></span>**ERROR\_DLL\_INIT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-326">1114 (0x45A)</span><span class="sxs-lookup"><span data-stu-id="298d3-326">1114 (0x45A)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-327">Error en una rutina de inicialización de la biblioteca de vínculos dinámicos (DLL).</span><span class="sxs-lookup"><span data-stu-id="298d3-327">A dynamic link library (DLL) initialization routine failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-328"><span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ERROR \_ \_ de apagado en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="298d3-328"><span id="ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="error_shutdown_in_progress"></span>**ERROR\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-329">1115 (0x45B)</span><span class="sxs-lookup"><span data-stu-id="298d3-329">1115 (0x45B)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-330">Está en curso un cierre del sistema.</span><span class="sxs-lookup"><span data-stu-id="298d3-330">A system shutdown is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-331"><span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERROR: \_ no hay ningún \_ apagado \_ en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="298d3-331"><span id="ERROR_NO_SHUTDOWN_IN_PROGRESS"></span><span id="error_no_shutdown_in_progress"></span>**ERROR\_NO\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-332">1116 (0x45C)</span><span class="sxs-lookup"><span data-stu-id="298d3-332">1116 (0x45C)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-333">No se puede anular el cierre del sistema porque no había ningún cierre en curso.</span><span class="sxs-lookup"><span data-stu-id="298d3-333">Unable to abort the system shutdown because no shutdown was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-334"><span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**ERROR de \_ dispositivo de e/s \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-334"><span id="ERROR_IO_DEVICE"></span><span id="error_io_device"></span>**ERROR\_IO\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-335">1117 (0x45D)</span><span class="sxs-lookup"><span data-stu-id="298d3-335">1117 (0x45D)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-336">La solicitud no se pudo realizar debido a un error de dispositivo de E/S.</span><span class="sxs-lookup"><span data-stu-id="298d3-336">The request could not be performed because of an I/O device error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-337"><span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERROR de \_ serie \_ sin \_ dispositivo**</span><span class="sxs-lookup"><span data-stu-id="298d3-337"><span id="ERROR_SERIAL_NO_DEVICE"></span><span id="error_serial_no_device"></span>**ERROR\_SERIAL\_NO\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-338">1118 (0x45E)</span><span class="sxs-lookup"><span data-stu-id="298d3-338">1118 (0x45E)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-339">No se inicializó correctamente ningún dispositivo serie.</span><span class="sxs-lookup"><span data-stu-id="298d3-339">No serial device was successfully initialized.</span></span> <span data-ttu-id="298d3-340">El controlador serie se descargará.</span><span class="sxs-lookup"><span data-stu-id="298d3-340">The serial driver will unload.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-341"><span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**IRQ de ERROR \_ \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="298d3-341"><span id="ERROR_IRQ_BUSY"></span><span id="error_irq_busy"></span>**ERROR\_IRQ\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-342">1119 (0x45F)</span><span class="sxs-lookup"><span data-stu-id="298d3-342">1119 (0x45F)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-343">No se puede abrir un dispositivo que compartía una solicitud de interrupción (IRQ) con otros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="298d3-343">Unable to open a device that was sharing an interrupt request (IRQ) with other devices.</span></span> <span data-ttu-id="298d3-344">Al menos otro dispositivo que utiliza esa IRQ ya estaba abierto.</span><span class="sxs-lookup"><span data-stu-id="298d3-344">At least one other device that uses that IRQ was already opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-345"><span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**ERRORES \_ más \_ escrituras**</span><span class="sxs-lookup"><span data-stu-id="298d3-345"><span id="ERROR_MORE_WRITES"></span><span id="error_more_writes"></span>**ERROR\_MORE\_WRITES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-346">1120 (0x460)</span><span class="sxs-lookup"><span data-stu-id="298d3-346">1120 (0x460)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-347">Una operación de e/s en serie se completó mediante otra escritura en el puerto serie.</span><span class="sxs-lookup"><span data-stu-id="298d3-347">A serial I/O operation was completed by another write to the serial port.</span></span> <span data-ttu-id="298d3-348">El \_ \_ contador XOFF serie ioctl llegó a \_ cero.)</span><span class="sxs-lookup"><span data-stu-id="298d3-348">The IOCTL\_SERIAL\_XOFF\_COUNTER reached zero.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-349"><span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**tiempo de espera del \_ contador de errores \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-349"><span id="ERROR_COUNTER_TIMEOUT"></span><span id="error_counter_timeout"></span>**ERROR\_COUNTER\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-350">1121 (0x461)</span><span class="sxs-lookup"><span data-stu-id="298d3-350">1121 (0x461)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-351">Se completó una operación de e/s en serie porque expiró el período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="298d3-351">A serial I/O operation completed because the timeout period expired.</span></span> <span data-ttu-id="298d3-352">El \_ \_ contador XOFF serie ioctl \_ no llegó a cero.)</span><span class="sxs-lookup"><span data-stu-id="298d3-352">The IOCTL\_SERIAL\_XOFF\_COUNTER did not reach zero.)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-353"><span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**ERROR de \_ marca de ID. de disquete \_ \_ \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="298d3-353"><span id="ERROR_FLOPPY_ID_MARK_NOT_FOUND"></span><span id="error_floppy_id_mark_not_found"></span>**ERROR\_FLOPPY\_ID\_MARK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-354">1122 (0x462)</span><span class="sxs-lookup"><span data-stu-id="298d3-354">1122 (0x462)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-355">No se encontró ninguna marca de dirección de identificador en el disquete.</span><span class="sxs-lookup"><span data-stu-id="298d3-355">No ID address mark was found on the floppy disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-356"><span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERROR de \_ cilindro de disquete \_ incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-356"><span id="ERROR_FLOPPY_WRONG_CYLINDER"></span><span id="error_floppy_wrong_cylinder"></span>**ERROR\_FLOPPY\_WRONG\_CYLINDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-357">1123 (0x463)</span><span class="sxs-lookup"><span data-stu-id="298d3-357">1123 (0x463)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-358">Discrepancia entre el campo ID. de sector de disquete y la dirección de pista de la controladora de disquete.</span><span class="sxs-lookup"><span data-stu-id="298d3-358">Mismatch between the floppy disk sector ID field and the floppy disk controller track address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-359"><span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**error \_ desconocido en el disquete \_ \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-359"><span id="ERROR_FLOPPY_UNKNOWN_ERROR"></span><span id="error_floppy_unknown_error"></span>**ERROR\_FLOPPY\_UNKNOWN\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-360">1124 (0x464)</span><span class="sxs-lookup"><span data-stu-id="298d3-360">1124 (0x464)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-361">El controlador de disquete ha detectado un error no reconocido por el controlador de disquete.</span><span class="sxs-lookup"><span data-stu-id="298d3-361">The floppy disk controller reported an error that is not recognized by the floppy disk driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-362"><span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**ERROR de \_ \_ registros incorrectos de disquete \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-362"><span id="ERROR_FLOPPY_BAD_REGISTERS"></span><span id="error_floppy_bad_registers"></span>**ERROR\_FLOPPY\_BAD\_REGISTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-363">1125 (0x465)</span><span class="sxs-lookup"><span data-stu-id="298d3-363">1125 (0x465)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-364">El controlador de disquete devolvió resultados incoherentes en sus registros.</span><span class="sxs-lookup"><span data-stu-id="298d3-364">The floppy disk controller returned inconsistent results in its registers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-365"><span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**ERROR en la \_ \_ recalibración del disco \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-365"><span id="ERROR_DISK_RECALIBRATE_FAILED"></span><span id="error_disk_recalibrate_failed"></span>**ERROR\_DISK\_RECALIBRATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-366">1126 (0x466)</span><span class="sxs-lookup"><span data-stu-id="298d3-366">1126 (0x466)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-367">Al tener acceso al disco duro, se produjo un error en la operación de recalibración, incluso después de los reintentos.</span><span class="sxs-lookup"><span data-stu-id="298d3-367">While accessing the hard disk, a recalibrate operation failed, even after retries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-368"><span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**ERROR en la \_ operación de disco \_ \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-368"><span id="ERROR_DISK_OPERATION_FAILED"></span><span id="error_disk_operation_failed"></span>**ERROR\_DISK\_OPERATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-369">1127 (0x467)</span><span class="sxs-lookup"><span data-stu-id="298d3-369">1127 (0x467)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-370">Al tener acceso al disco duro, se produjo un error en una operación de disco incluso después de los reintentos.</span><span class="sxs-lookup"><span data-stu-id="298d3-370">While accessing the hard disk, a disk operation failed even after retries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-371"><span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERROR \_ \_ al restablecer el disco \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-371"><span id="ERROR_DISK_RESET_FAILED"></span><span id="error_disk_reset_failed"></span>**ERROR\_DISK\_RESET\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-372">1128 (0x468)</span><span class="sxs-lookup"><span data-stu-id="298d3-372">1128 (0x468)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-373">Al tener acceso al disco duro, se necesitaba un restablecimiento del controlador de disco, pero se produjo un error.</span><span class="sxs-lookup"><span data-stu-id="298d3-373">While accessing the hard disk, a disk controller reset was needed, but even that failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-374"><span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**desbordamiento de ERROR \_ FDM \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-374"><span id="ERROR_EOM_OVERFLOW"></span><span id="error_eom_overflow"></span>**ERROR\_EOM\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-375">1129 (0x469)</span><span class="sxs-lookup"><span data-stu-id="298d3-375">1129 (0x469)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-376">Se encontró el final físico de la cinta.</span><span class="sxs-lookup"><span data-stu-id="298d3-376">Physical end of tape encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-377"><span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERROR \_ de \_ memoria insuficiente en el \_ servidor \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-377"><span id="ERROR_NOT_ENOUGH_SERVER_MEMORY"></span><span id="error_not_enough_server_memory"></span>**ERROR\_NOT\_ENOUGH\_SERVER\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-378">1130 (0x46A)</span><span class="sxs-lookup"><span data-stu-id="298d3-378">1130 (0x46A)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-379">No hay suficiente espacio de almacenamiento en servidores para procesar este comando.</span><span class="sxs-lookup"><span data-stu-id="298d3-379">Not enough server storage is available to process this command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-380"><span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERROR \_ de \_ interbloqueo posible**</span><span class="sxs-lookup"><span data-stu-id="298d3-380"><span id="ERROR_POSSIBLE_DEADLOCK"></span><span id="error_possible_deadlock"></span>**ERROR\_POSSIBLE\_DEADLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-381">1131 (0x46B)</span><span class="sxs-lookup"><span data-stu-id="298d3-381">1131 (0x46B)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-382">Se ha detectado una posible condición de interbloqueo.</span><span class="sxs-lookup"><span data-stu-id="298d3-382">A potential deadlock condition has been detected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-383"><span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**\_alineación asignada de error \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-383"><span id="ERROR_MAPPED_ALIGNMENT"></span><span id="error_mapped_alignment"></span>**ERROR\_MAPPED\_ALIGNMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-384">1132 (0x46C)</span><span class="sxs-lookup"><span data-stu-id="298d3-384">1132 (0x46C)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-385">La dirección base o el desplazamiento de archivo especificados no tienen la alineación adecuada.</span><span class="sxs-lookup"><span data-stu-id="298d3-385">The base address or the file offset specified does not have the proper alignment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-386"><span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**ERROR al \_ establecer el \_ Estado de energía \_ \_ vetado**</span><span class="sxs-lookup"><span data-stu-id="298d3-386"><span id="ERROR_SET_POWER_STATE_VETOED"></span><span id="error_set_power_state_vetoed"></span>**ERROR\_SET\_POWER\_STATE\_VETOED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-387">1140 (0x474)</span><span class="sxs-lookup"><span data-stu-id="298d3-387">1140 (0x474)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-388">Un intento de cambiar el estado de energía del sistema fue vetado por otra aplicación o controlador.</span><span class="sxs-lookup"><span data-stu-id="298d3-388">An attempt to change the system power state was vetoed by another application or driver.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-389"><span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**ERROR \_ al establecer el \_ Estado de energía \_ \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-389"><span id="ERROR_SET_POWER_STATE_FAILED"></span><span id="error_set_power_state_failed"></span>**ERROR\_SET\_POWER\_STATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-390">1141 (0x475)</span><span class="sxs-lookup"><span data-stu-id="298d3-390">1141 (0x475)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-391">Error del BIOS del sistema al intentar cambiar el estado de energía del sistema.</span><span class="sxs-lookup"><span data-stu-id="298d3-391">The system BIOS failed an attempt to change the system power state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-392"><span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERROR \_ demasiados \_ \_ vínculos**</span><span class="sxs-lookup"><span data-stu-id="298d3-392"><span id="ERROR_TOO_MANY_LINKS"></span><span id="error_too_many_links"></span>**ERROR\_TOO\_MANY\_LINKS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-393">1142 (0x476)</span><span class="sxs-lookup"><span data-stu-id="298d3-393">1142 (0x476)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-394">Se intentó crear más vínculos en un archivo de los que admite el sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="298d3-394">An attempt was made to create more links on a file than the file system supports.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-395"><span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERROR \_ de \_ versión anterior de Win \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-395"><span id="ERROR_OLD_WIN_VERSION"></span><span id="error_old_win_version"></span>**ERROR\_OLD\_WIN\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-396">1150 (0x47E)</span><span class="sxs-lookup"><span data-stu-id="298d3-396">1150 (0x47E)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-397">El programa especificado requiere una versión más reciente de Windows.</span><span class="sxs-lookup"><span data-stu-id="298d3-397">The specified program requires a newer version of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-398"><span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**ERROR \_ de \_ aplicación \_ del sistema operativo incorrecto**</span><span class="sxs-lookup"><span data-stu-id="298d3-398"><span id="ERROR_APP_WRONG_OS"></span><span id="error_app_wrong_os"></span>**ERROR\_APP\_WRONG\_OS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-399">1151 (0x47F)</span><span class="sxs-lookup"><span data-stu-id="298d3-399">1151 (0x47F)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-400">El programa especificado no es un programa para Windows o MS-DOS.</span><span class="sxs-lookup"><span data-stu-id="298d3-400">The specified program is not a Windows or MS-DOS program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-401"><span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**ERROR \_ de \_ aplicación de instancia única \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-401"><span id="ERROR_SINGLE_INSTANCE_APP"></span><span id="error_single_instance_app"></span>**ERROR\_SINGLE\_INSTANCE\_APP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-402">1152 (0x480)</span><span class="sxs-lookup"><span data-stu-id="298d3-402">1152 (0x480)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-403">No se puede iniciar más de una instancia del programa especificado.</span><span class="sxs-lookup"><span data-stu-id="298d3-403">Cannot start more than one instance of the specified program.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-404"><span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERROR en la \_ \_ aplicación RMODE**</span><span class="sxs-lookup"><span data-stu-id="298d3-404"><span id="ERROR_RMODE_APP"></span><span id="error_rmode_app"></span>**ERROR\_RMODE\_APP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-405">1153 (0x481)</span><span class="sxs-lookup"><span data-stu-id="298d3-405">1153 (0x481)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-406">El programa especificado se ha escrito para una versión anterior de Windows.</span><span class="sxs-lookup"><span data-stu-id="298d3-406">The specified program was written for an earlier version of Windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-407"><span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**ERROR \_ de \_ dll no válida**</span><span class="sxs-lookup"><span data-stu-id="298d3-407"><span id="ERROR_INVALID_DLL"></span><span id="error_invalid_dll"></span>**ERROR\_INVALID\_DLL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-408">1154 (0x482)</span><span class="sxs-lookup"><span data-stu-id="298d3-408">1154 (0x482)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-409">Uno de los archivos de biblioteca necesarios para ejecutar esta aplicación está dañado.</span><span class="sxs-lookup"><span data-stu-id="298d3-409">One of the library files needed to run this application is damaged.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-410"><span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERROR \_ sin \_ Asociación**</span><span class="sxs-lookup"><span data-stu-id="298d3-410"><span id="ERROR_NO_ASSOCIATION"></span><span id="error_no_association"></span>**ERROR\_NO\_ASSOCIATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-411">1155 (0x483)</span><span class="sxs-lookup"><span data-stu-id="298d3-411">1155 (0x483)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-412">No hay ninguna aplicación asociada al archivo especificado para esta operación.</span><span class="sxs-lookup"><span data-stu-id="298d3-412">No application is associated with the specified file for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-413"><span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERROR de \_ DDE \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-413"><span id="ERROR_DDE_FAIL"></span><span id="error_dde_fail"></span>**ERROR\_DDE\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-414">1156 (0x484)</span><span class="sxs-lookup"><span data-stu-id="298d3-414">1156 (0x484)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-415">Error al enviar el comando a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="298d3-415">An error occurred in sending the command to the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-416"><span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**\_ \_ no \_ se encontró el archivo dll de error**</span><span class="sxs-lookup"><span data-stu-id="298d3-416"><span id="ERROR_DLL_NOT_FOUND"></span><span id="error_dll_not_found"></span>**ERROR\_DLL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-417">1157 (0x485)</span><span class="sxs-lookup"><span data-stu-id="298d3-417">1157 (0x485)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-418">No se encuentra uno de los archivos de biblioteca necesarios para ejecutar esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="298d3-418">One of the library files needed to run this application cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-419"><span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERROR: \_ no hay \_ más \_ \_ identificadores de usuario**</span><span class="sxs-lookup"><span data-stu-id="298d3-419"><span id="ERROR_NO_MORE_USER_HANDLES"></span><span id="error_no_more_user_handles"></span>**ERROR\_NO\_MORE\_USER\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-420">1158 (0x486)</span><span class="sxs-lookup"><span data-stu-id="298d3-420">1158 (0x486)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-421">El proceso actual ha utilizado todos los identificadores del sistema para los objetos de administrador de Windows.</span><span class="sxs-lookup"><span data-stu-id="298d3-421">The current process has used all of its system allowance of handles for Window Manager objects.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-422"><span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**\_ \_ solo sincronización de mensajes de error \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-422"><span id="ERROR_MESSAGE_SYNC_ONLY"></span><span id="error_message_sync_only"></span>**ERROR\_MESSAGE\_SYNC\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-423">1159 (0x487)</span><span class="sxs-lookup"><span data-stu-id="298d3-423">1159 (0x487)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-424">El mensaje solo se puede usar con operaciones sincrónicas.</span><span class="sxs-lookup"><span data-stu-id="298d3-424">The message can be used only with synchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-425"><span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**elemento de origen de ERROR \_ \_ \_ vacío**</span><span class="sxs-lookup"><span data-stu-id="298d3-425"><span id="ERROR_SOURCE_ELEMENT_EMPTY"></span><span id="error_source_element_empty"></span>**ERROR\_SOURCE\_ELEMENT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-426">1160 (0x488)</span><span class="sxs-lookup"><span data-stu-id="298d3-426">1160 (0x488)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-427">El elemento de origen indicado no tiene ningún medio.</span><span class="sxs-lookup"><span data-stu-id="298d3-427">The indicated source element has no media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-428"><span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**elemento de destino de ERROR \_ \_ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="298d3-428"><span id="ERROR_DESTINATION_ELEMENT_FULL"></span><span id="error_destination_element_full"></span>**ERROR\_DESTINATION\_ELEMENT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-429">1161 (0x489)</span><span class="sxs-lookup"><span data-stu-id="298d3-429">1161 (0x489)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-430">El elemento de destino indicado ya contiene medios.</span><span class="sxs-lookup"><span data-stu-id="298d3-430">The indicated destination element already contains media.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-431"><span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERROR \_ de \_ dirección de elemento no válida \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-431"><span id="ERROR_ILLEGAL_ELEMENT_ADDRESS"></span><span id="error_illegal_element_address"></span>**ERROR\_ILLEGAL\_ELEMENT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-432">1162 (0x48A)</span><span class="sxs-lookup"><span data-stu-id="298d3-432">1162 (0x48A)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-433">El elemento indicado no existe.</span><span class="sxs-lookup"><span data-stu-id="298d3-433">The indicated element does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-434"><span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**ERROR \_ revista \_ no \_ presente**</span><span class="sxs-lookup"><span data-stu-id="298d3-434"><span id="ERROR_MAGAZINE_NOT_PRESENT"></span><span id="error_magazine_not_present"></span>**ERROR\_MAGAZINE\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-435">1163 (0x48B)</span><span class="sxs-lookup"><span data-stu-id="298d3-435">1163 (0x48B)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-436">El elemento indicado es parte de una revista que no está presente.</span><span class="sxs-lookup"><span data-stu-id="298d3-436">The indicated element is part of a magazine that is not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-437"><span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**ERROR \_ de \_ reinicialización de dispositivo \_ necesaria**</span><span class="sxs-lookup"><span data-stu-id="298d3-437"><span id="ERROR_DEVICE_REINITIALIZATION_NEEDED"></span><span id="error_device_reinitialization_needed"></span>**ERROR\_DEVICE\_REINITIALIZATION\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-438">1164 (0x48C)</span><span class="sxs-lookup"><span data-stu-id="298d3-438">1164 (0x48C)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-439">El dispositivo indicado requiere reinicialización debido a errores de hardware.</span><span class="sxs-lookup"><span data-stu-id="298d3-439">The indicated device requires reinitialization due to hardware errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-440"><span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**el \_ dispositivo de error \_ requiere \_ limpieza**</span><span class="sxs-lookup"><span data-stu-id="298d3-440"><span id="ERROR_DEVICE_REQUIRES_CLEANING"></span><span id="error_device_requires_cleaning"></span>**ERROR\_DEVICE\_REQUIRES\_CLEANING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-441">1165 (0x48D)</span><span class="sxs-lookup"><span data-stu-id="298d3-441">1165 (0x48D)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-442">El dispositivo ha indicado que se requiere limpieza antes de intentar realizar más operaciones.</span><span class="sxs-lookup"><span data-stu-id="298d3-442">The device has indicated that cleaning is required before further operations are attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-443"><span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERROR \_ al \_ abrir la puerta del dispositivo \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-443"><span id="ERROR_DEVICE_DOOR_OPEN"></span><span id="error_device_door_open"></span>**ERROR\_DEVICE\_DOOR\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-444">1166 (0x48E)</span><span class="sxs-lookup"><span data-stu-id="298d3-444">1166 (0x48E)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-445">El dispositivo ha indicado que la puerta está abierta.</span><span class="sxs-lookup"><span data-stu-id="298d3-445">The device has indicated that its door is open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-446"><span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**ERROR de \_ dispositivo \_ no \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="298d3-446"><span id="ERROR_DEVICE_NOT_CONNECTED"></span><span id="error_device_not_connected"></span>**ERROR\_DEVICE\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-447">1167 (0x48F)</span><span class="sxs-lookup"><span data-stu-id="298d3-447">1167 (0x48F)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-448">El dispositivo no está conectado.</span><span class="sxs-lookup"><span data-stu-id="298d3-448">The device is not connected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-449"><span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**\_no \_ se encontró el error**</span><span class="sxs-lookup"><span data-stu-id="298d3-449"><span id="ERROR_NOT_FOUND"></span><span id="error_not_found"></span>**ERROR\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-450">1168 (0x490)</span><span class="sxs-lookup"><span data-stu-id="298d3-450">1168 (0x490)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-451">Elemento no encontrado.</span><span class="sxs-lookup"><span data-stu-id="298d3-451">Element not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-452"><span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERROR \_ sin \_ coincidencia**</span><span class="sxs-lookup"><span data-stu-id="298d3-452"><span id="ERROR_NO_MATCH"></span><span id="error_no_match"></span>**ERROR\_NO\_MATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-453">1169 (0x491)</span><span class="sxs-lookup"><span data-stu-id="298d3-453">1169 (0x491)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-454">No hay ninguna coincidencia para la clave especificada en el índice.</span><span class="sxs-lookup"><span data-stu-id="298d3-454">There was no match for the specified key in the index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-455"><span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**\_ \_ no \_ se encontró el conjunto de errores**</span><span class="sxs-lookup"><span data-stu-id="298d3-455"><span id="ERROR_SET_NOT_FOUND"></span><span id="error_set_not_found"></span>**ERROR\_SET\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-456">1170 (0x492)</span><span class="sxs-lookup"><span data-stu-id="298d3-456">1170 (0x492)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-457">El conjunto de propiedades especificado no existe en el objeto.</span><span class="sxs-lookup"><span data-stu-id="298d3-457">The property set specified does not exist on the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-458"><span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**\_ \_ no \_ se encontró el punto de error**</span><span class="sxs-lookup"><span data-stu-id="298d3-458"><span id="ERROR_POINT_NOT_FOUND"></span><span id="error_point_not_found"></span>**ERROR\_POINT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-459">1171 (0x493)</span><span class="sxs-lookup"><span data-stu-id="298d3-459">1171 (0x493)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-460">El punto pasado a GetMouseMovePoints no está en el búfer.</span><span class="sxs-lookup"><span data-stu-id="298d3-460">The point passed to GetMouseMovePoints is not in the buffer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-461"><span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERROR: \_ no hay \_ servicio de seguimiento \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-461"><span id="ERROR_NO_TRACKING_SERVICE"></span><span id="error_no_tracking_service"></span>**ERROR\_NO\_TRACKING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-462">1172 (0x494)</span><span class="sxs-lookup"><span data-stu-id="298d3-462">1172 (0x494)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-463">El servicio de seguimiento (estación de trabajo) no se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="298d3-463">The tracking (workstation) service is not running.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-464"><span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERROR: \_ no hay \_ \_ ID. de volumen**</span><span class="sxs-lookup"><span data-stu-id="298d3-464"><span id="ERROR_NO_VOLUME_ID"></span><span id="error_no_volume_id"></span>**ERROR\_NO\_VOLUME\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-465">1173 (0x495)</span><span class="sxs-lookup"><span data-stu-id="298d3-465">1173 (0x495)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-466">No se pudo encontrar el ID. de volumen.</span><span class="sxs-lookup"><span data-stu-id="298d3-466">The Volume ID could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-467"><span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**\_no se \_ puede \_ quitar el \_ reemplazo**</span><span class="sxs-lookup"><span data-stu-id="298d3-467"><span id="ERROR_UNABLE_TO_REMOVE_REPLACED"></span><span id="error_unable_to_remove_replaced"></span>**ERROR\_UNABLE\_TO\_REMOVE\_REPLACED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-468">1175 (0x497)</span><span class="sxs-lookup"><span data-stu-id="298d3-468">1175 (0x497)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-469">No se puede quitar el archivo que se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="298d3-469">Unable to remove the file to be replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-470"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERROR \_ no se puede \_ \_ cambiar el \_ reemplazo**</span><span class="sxs-lookup"><span data-stu-id="298d3-470"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT"></span><span id="error_unable_to_move_replacement"></span>**ERROR\_UNABLE\_TO\_MOVE\_REPLACEMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-471">1176 (0x498)</span><span class="sxs-lookup"><span data-stu-id="298d3-471">1176 (0x498)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-472">No se puede trasladar el archivo de reemplazo al archivo que se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="298d3-472">Unable to move the replacement file to the file to be replaced.</span></span> <span data-ttu-id="298d3-473">El archivo que se va a reemplazar ha conservado su nombre original.</span><span class="sxs-lookup"><span data-stu-id="298d3-473">The file to be replaced has retained its original name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-474"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERROR \_ no se puede \_ \_ trasladar el \_ reemplazo \_ 2**</span><span class="sxs-lookup"><span data-stu-id="298d3-474"><span id="ERROR_UNABLE_TO_MOVE_REPLACEMENT_2"></span><span id="error_unable_to_move_replacement_2"></span>**ERROR\_UNABLE\_TO\_MOVE\_REPLACEMENT\_2**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-475">1177 (0x499)</span><span class="sxs-lookup"><span data-stu-id="298d3-475">1177 (0x499)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-476">No se puede trasladar el archivo de reemplazo al archivo que se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="298d3-476">Unable to move the replacement file to the file to be replaced.</span></span> <span data-ttu-id="298d3-477">Se ha cambiado el nombre del archivo que se va a reemplazar con el nombre de la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="298d3-477">The file to be replaced has been renamed using the backup name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-478"><span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**\_ \_ eliminación \_ en curso del diario de errores \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-478"><span id="ERROR_JOURNAL_DELETE_IN_PROGRESS"></span><span id="error_journal_delete_in_progress"></span>**ERROR\_JOURNAL\_DELETE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-479">1178 (0x49A)</span><span class="sxs-lookup"><span data-stu-id="298d3-479">1178 (0x49A)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-480">Se está eliminando el diario de cambios de volumen.</span><span class="sxs-lookup"><span data-stu-id="298d3-480">The volume change journal is being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-481"><span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**diario de errores \_ \_ no \_ activo**</span><span class="sxs-lookup"><span data-stu-id="298d3-481"><span id="ERROR_JOURNAL_NOT_ACTIVE"></span><span id="error_journal_not_active"></span>**ERROR\_JOURNAL\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-482">1179 (0x49B)</span><span class="sxs-lookup"><span data-stu-id="298d3-482">1179 (0x49B)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-483">El diario de cambios de volumen no está activo.</span><span class="sxs-lookup"><span data-stu-id="298d3-483">The volume change journal is not active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-484"><span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**\_ \_ se encontró un archivo potencial de error \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-484"><span id="ERROR_POTENTIAL_FILE_FOUND"></span><span id="error_potential_file_found"></span>**ERROR\_POTENTIAL\_FILE\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-485">1180 (0x49C)</span><span class="sxs-lookup"><span data-stu-id="298d3-485">1180 (0x49C)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-486">Se encontró un archivo, pero es posible que no sea el archivo correcto.</span><span class="sxs-lookup"><span data-stu-id="298d3-486">A file was found, but it may not be the correct file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-487"><span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**entrada de diario de errores \_ \_ \_ eliminada**</span><span class="sxs-lookup"><span data-stu-id="298d3-487"><span id="ERROR_JOURNAL_ENTRY_DELETED"></span><span id="error_journal_entry_deleted"></span>**ERROR\_JOURNAL\_ENTRY\_DELETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-488">1181 (0x49D)</span><span class="sxs-lookup"><span data-stu-id="298d3-488">1181 (0x49D)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-489">La entrada del diario se ha eliminado del diario.</span><span class="sxs-lookup"><span data-stu-id="298d3-489">The journal entry has been deleted from the journal.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-490"><span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**el \_ cierre de errores \_ está \_ programado**</span><span class="sxs-lookup"><span data-stu-id="298d3-490"><span id="ERROR_SHUTDOWN_IS_SCHEDULED"></span><span id="error_shutdown_is_scheduled"></span>**ERROR\_SHUTDOWN\_IS\_SCHEDULED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-491">1190 (0x4A6)</span><span class="sxs-lookup"><span data-stu-id="298d3-491">1190 (0x4A6)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-492">Ya se ha programado un cierre del sistema.</span><span class="sxs-lookup"><span data-stu-id="298d3-492">A system shutdown has already been scheduled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-493"><span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**ERROR al \_ cerrar \_ los usuarios que \_ iniciaron sesión \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-493"><span id="ERROR_SHUTDOWN_USERS_LOGGED_ON"></span><span id="error_shutdown_users_logged_on"></span>**ERROR\_SHUTDOWN\_USERS\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-494">1191 (0x4A7)</span><span class="sxs-lookup"><span data-stu-id="298d3-494">1191 (0x4A7)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-495">No se puede iniciar el apagado del sistema porque otros usuarios han iniciado sesión en el equipo.</span><span class="sxs-lookup"><span data-stu-id="298d3-495">The system shutdown cannot be initiated because there are other users logged on to the computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-496"><span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERROR \_ de \_ dispositivo incorrecto**</span><span class="sxs-lookup"><span data-stu-id="298d3-496"><span id="ERROR_BAD_DEVICE"></span><span id="error_bad_device"></span>**ERROR\_BAD\_DEVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-497">1200 (0x4B0)</span><span class="sxs-lookup"><span data-stu-id="298d3-497">1200 (0x4B0)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-498">El nombre de dispositivo especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-498">The specified device name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-499"><span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**ERROR de \_ conexión sin \_ DISP.**</span><span class="sxs-lookup"><span data-stu-id="298d3-499"><span id="ERROR_CONNECTION_UNAVAIL"></span><span id="error_connection_unavail"></span>**ERROR\_CONNECTION\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-500">1201 (0x4B1)</span><span class="sxs-lookup"><span data-stu-id="298d3-500">1201 (0x4B1)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-501">El dispositivo no está conectado actualmente, pero es una conexión recordada.</span><span class="sxs-lookup"><span data-stu-id="298d3-501">The device is not currently connected but it is a remembered connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-502"><span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**dispositivo de ERROR \_ \_ ya \_ recordado**</span><span class="sxs-lookup"><span data-stu-id="298d3-502"><span id="ERROR_DEVICE_ALREADY_REMEMBERED"></span><span id="error_device_already_remembered"></span>**ERROR\_DEVICE\_ALREADY\_REMEMBERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-503">1202 (0x4B2)</span><span class="sxs-lookup"><span data-stu-id="298d3-503">1202 (0x4B2)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-504">El nombre del dispositivo local tiene una conexión recordada a otro recurso de red.</span><span class="sxs-lookup"><span data-stu-id="298d3-504">The local device name has a remembered connection to another network resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-505"><span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**NO se ha podido obtener una \_ \_ \_ ruta de red o no \_ válida \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-505"><span id="ERROR_NO_NET_OR_BAD_PATH"></span><span id="error_no_net_or_bad_path"></span>**ERROR\_NO\_NET\_OR\_BAD\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-506">1203 (0x4B3)</span><span class="sxs-lookup"><span data-stu-id="298d3-506">1203 (0x4B3)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-507">La ruta de acceso de red se escribió incorrectamente, no existe o el proveedor de red no está disponible en este momento.</span><span class="sxs-lookup"><span data-stu-id="298d3-507">The network path was either typed incorrectly, does not exist, or the network provider is not currently available.</span></span> <span data-ttu-id="298d3-508">Vuelva a escribir la ruta de acceso o póngase en contacto con el administrador de red.</span><span class="sxs-lookup"><span data-stu-id="298d3-508">Please try retyping the path or contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-509"><span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERROR \_ de \_ proveedor incorrecto**</span><span class="sxs-lookup"><span data-stu-id="298d3-509"><span id="ERROR_BAD_PROVIDER"></span><span id="error_bad_provider"></span>**ERROR\_BAD\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-510">1204 (0x4B4)</span><span class="sxs-lookup"><span data-stu-id="298d3-510">1204 (0x4B4)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-511">El nombre de proveedor de red especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-511">The specified network provider name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-512"><span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERROR \_ no se puede \_ abrir el \_ Perfil**</span><span class="sxs-lookup"><span data-stu-id="298d3-512"><span id="ERROR_CANNOT_OPEN_PROFILE"></span><span id="error_cannot_open_profile"></span>**ERROR\_CANNOT\_OPEN\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-513">1205 (0x4B5)</span><span class="sxs-lookup"><span data-stu-id="298d3-513">1205 (0x4B5)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-514">No se puede abrir el perfil de conexión de red.</span><span class="sxs-lookup"><span data-stu-id="298d3-514">Unable to open the network connection profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-515"><span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERROR \_ de \_ perfil incorrecto**</span><span class="sxs-lookup"><span data-stu-id="298d3-515"><span id="ERROR_BAD_PROFILE"></span><span id="error_bad_profile"></span>**ERROR\_BAD\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-516">1206 (0x4B6)</span><span class="sxs-lookup"><span data-stu-id="298d3-516">1206 (0x4B6)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-517">El perfil de conexión de red está dañado.</span><span class="sxs-lookup"><span data-stu-id="298d3-517">The network connection profile is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-518"><span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERROR \_ no \_ contenedor**</span><span class="sxs-lookup"><span data-stu-id="298d3-518"><span id="ERROR_NOT_CONTAINER"></span><span id="error_not_container"></span>**ERROR\_NOT\_CONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-519">1207 (0x4B7)</span><span class="sxs-lookup"><span data-stu-id="298d3-519">1207 (0x4B7)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-520">No se puede enumerar un contenedor.</span><span class="sxs-lookup"><span data-stu-id="298d3-520">Cannot enumerate a noncontainer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-521"><span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**error de ERROR \_ extendido \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-521"><span id="ERROR_EXTENDED_ERROR"></span><span id="error_extended_error"></span>**ERROR\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-522">1208 (0x4B8)</span><span class="sxs-lookup"><span data-stu-id="298d3-522">1208 (0x4B8)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-523">Se ha producido un error extendido.</span><span class="sxs-lookup"><span data-stu-id="298d3-523">An extended error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-524"><span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERROR \_ de \_ GROUPNAME no válido**</span><span class="sxs-lookup"><span data-stu-id="298d3-524"><span id="ERROR_INVALID_GROUPNAME"></span><span id="error_invalid_groupname"></span>**ERROR\_INVALID\_GROUPNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-525">1209 (0x4B9)</span><span class="sxs-lookup"><span data-stu-id="298d3-525">1209 (0x4B9)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-526">El formato del nombre de grupo especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-526">The format of the specified group name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-527"><span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERROR \_ de \_ nombre de equipo no válido**</span><span class="sxs-lookup"><span data-stu-id="298d3-527"><span id="ERROR_INVALID_COMPUTERNAME"></span><span id="error_invalid_computername"></span>**ERROR\_INVALID\_COMPUTERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-528">1210 (0x4BA)</span><span class="sxs-lookup"><span data-stu-id="298d3-528">1210 (0x4BA)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-529">El formato del nombre de equipo especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-529">The format of the specified computer name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-530"><span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERROR \_ EVENTNAME no válido \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-530"><span id="ERROR_INVALID_EVENTNAME"></span><span id="error_invalid_eventname"></span>**ERROR\_INVALID\_EVENTNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-531">1211 (0x4BB)</span><span class="sxs-lookup"><span data-stu-id="298d3-531">1211 (0x4BB)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-532">El formato del nombre de evento especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-532">The format of the specified event name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-533"><span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERROR \_ domainname no válido \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-533"><span id="ERROR_INVALID_DOMAINNAME"></span><span id="error_invalid_domainname"></span>**ERROR\_INVALID\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-534">1212 (0x4BC)</span><span class="sxs-lookup"><span data-stu-id="298d3-534">1212 (0x4BC)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-535">El formato del nombre de dominio especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-535">The format of the specified domain name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-536"><span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERROR \_ de \_ ServiceName no válido**</span><span class="sxs-lookup"><span data-stu-id="298d3-536"><span id="ERROR_INVALID_SERVICENAME"></span><span id="error_invalid_servicename"></span>**ERROR\_INVALID\_SERVICENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-537">1213 (0x4BD)</span><span class="sxs-lookup"><span data-stu-id="298d3-537">1213 (0x4BD)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-538">El formato del nombre de servicio especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-538">The format of the specified service name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-539"><span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERROR \_ de \_ la**</span><span class="sxs-lookup"><span data-stu-id="298d3-539"><span id="ERROR_INVALID_NETNAME"></span><span id="error_invalid_netname"></span>**ERROR\_INVALID\_NETNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-540">1214 (0x4BE)</span><span class="sxs-lookup"><span data-stu-id="298d3-540">1214 (0x4BE)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-541">El formato del nombre de red especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-541">The format of the specified network name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-542"><span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERROR \_ SHARENAME no válido \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-542"><span id="ERROR_INVALID_SHARENAME"></span><span id="error_invalid_sharename"></span>**ERROR\_INVALID\_SHARENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-543">1215 (0x4BF)</span><span class="sxs-lookup"><span data-stu-id="298d3-543">1215 (0x4BF)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-544">El formato del nombre de recurso compartido especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-544">The format of the specified share name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-545"><span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERROR \_ PASSWORDNAME no válido \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-545"><span id="ERROR_INVALID_PASSWORDNAME"></span><span id="error_invalid_passwordname"></span>**ERROR\_INVALID\_PASSWORDNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-546">1216 (0x4C0)</span><span class="sxs-lookup"><span data-stu-id="298d3-546">1216 (0x4C0)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-547">El formato de la contraseña especificada no es válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-547">The format of the specified password is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-548"><span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**ERROR \_ de \_ MESSAGENAME no válido**</span><span class="sxs-lookup"><span data-stu-id="298d3-548"><span id="ERROR_INVALID_MESSAGENAME"></span><span id="error_invalid_messagename"></span>**ERROR\_INVALID\_MESSAGENAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-549">1217 (0x4C1)</span><span class="sxs-lookup"><span data-stu-id="298d3-549">1217 (0x4C1)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-550">El formato del nombre de mensaje especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-550">The format of the specified message name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-551"><span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERROR \_ MESSAGEDEST no válido \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-551"><span id="ERROR_INVALID_MESSAGEDEST"></span><span id="error_invalid_messagedest"></span>**ERROR\_INVALID\_MESSAGEDEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-552">1218 (0x4C2)</span><span class="sxs-lookup"><span data-stu-id="298d3-552">1218 (0x4C2)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-553">El formato del destino del mensaje especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-553">The format of the specified message destination is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-554"><span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**\_conflicto de \_ credenciales de sesión de error \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-554"><span id="ERROR_SESSION_CREDENTIAL_CONFLICT"></span><span id="error_session_credential_conflict"></span>**ERROR\_SESSION\_CREDENTIAL\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-555">1219 (0x4C3)</span><span class="sxs-lookup"><span data-stu-id="298d3-555">1219 (0x4C3)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-556">No se permiten varias conexiones a un servidor o recurso compartido por el mismo usuario, usando más de un nombre de usuario.</span><span class="sxs-lookup"><span data-stu-id="298d3-556">Multiple connections to a server or shared resource by the same user, using more than one user name, are not allowed.</span></span> <span data-ttu-id="298d3-557">Desconecte todas las conexiones anteriores al servidor o recurso compartido e inténtelo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="298d3-557">Disconnect all previous connections to the server or shared resource and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-558"><span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**ERROR \_ de \_ límite de sesión remota \_ \_ superado**</span><span class="sxs-lookup"><span data-stu-id="298d3-558"><span id="ERROR_REMOTE_SESSION_LIMIT_EXCEEDED"></span><span id="error_remote_session_limit_exceeded"></span>**ERROR\_REMOTE\_SESSION\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-559">1220 (0x4C4)</span><span class="sxs-lookup"><span data-stu-id="298d3-559">1220 (0x4C4)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-560">Se intentó establecer una sesión en un servidor de red, pero ya hay demasiadas sesiones establecidas en ese servidor.</span><span class="sxs-lookup"><span data-stu-id="298d3-560">An attempt was made to establish a session to a network server, but there are already too many sessions established to that server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-561"><span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERROR \_ DUP \_ nombreDominio**</span><span class="sxs-lookup"><span data-stu-id="298d3-561"><span id="ERROR_DUP_DOMAINNAME"></span><span id="error_dup_domainname"></span>**ERROR\_DUP\_DOMAINNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-562">1221 (0x4C5)</span><span class="sxs-lookup"><span data-stu-id="298d3-562">1221 (0x4C5)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-563">El nombre de grupo de trabajo o dominio ya está siendo utilizado por otro equipo de la red.</span><span class="sxs-lookup"><span data-stu-id="298d3-563">The workgroup or domain name is already in use by another computer on the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-564"><span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERROR: \_ no hay \_ red**</span><span class="sxs-lookup"><span data-stu-id="298d3-564"><span id="ERROR_NO_NETWORK"></span><span id="error_no_network"></span>**ERROR\_NO\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-565">1222 (0x4C6)</span><span class="sxs-lookup"><span data-stu-id="298d3-565">1222 (0x4C6)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-566">La red no está presente o no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="298d3-566">The network is not present or not started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-567"><span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERROR \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="298d3-567"><span id="ERROR_CANCELLED"></span><span id="error_cancelled"></span>**ERROR\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-568">1223 (0x4C7)</span><span class="sxs-lookup"><span data-stu-id="298d3-568">1223 (0x4C7)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-569">El usuario canceló la operación.</span><span class="sxs-lookup"><span data-stu-id="298d3-569">The operation was canceled by the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-570"><span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**\_ \_ archivo asignado al usuario con errores \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-570"><span id="ERROR_USER_MAPPED_FILE"></span><span id="error_user_mapped_file"></span>**ERROR\_USER\_MAPPED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-571">1224 (0x4C8)</span><span class="sxs-lookup"><span data-stu-id="298d3-571">1224 (0x4C8)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-572">La operación solicitada no se puede realizar en un archivo con una sección asignada por el usuario abierta.</span><span class="sxs-lookup"><span data-stu-id="298d3-572">The requested operation cannot be performed on a file with a user-mapped section open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-573"><span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**ERROR de \_ conexión \_ rechazada**</span><span class="sxs-lookup"><span data-stu-id="298d3-573"><span id="ERROR_CONNECTION_REFUSED"></span><span id="error_connection_refused"></span>**ERROR\_CONNECTION\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-574">1225 (0x4C9)</span><span class="sxs-lookup"><span data-stu-id="298d3-574">1225 (0x4C9)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-575">El equipo remoto rechazó la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="298d3-575">The remote computer refused the network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-576"><span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**ERROR \_ de \_ desconexión correcta**</span><span class="sxs-lookup"><span data-stu-id="298d3-576"><span id="ERROR_GRACEFUL_DISCONNECT"></span><span id="error_graceful_disconnect"></span>**ERROR\_GRACEFUL\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-577">1226 (0x4CA)</span><span class="sxs-lookup"><span data-stu-id="298d3-577">1226 (0x4CA)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-578">La conexión de red se cerró correctamente.</span><span class="sxs-lookup"><span data-stu-id="298d3-578">The network connection was gracefully closed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-579"><span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**Dirección de ERROR \_ \_ ya \_ asociada**</span><span class="sxs-lookup"><span data-stu-id="298d3-579"><span id="ERROR_ADDRESS_ALREADY_ASSOCIATED"></span><span id="error_address_already_associated"></span>**ERROR\_ADDRESS\_ALREADY\_ASSOCIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-580">1227 (0x4CB)</span><span class="sxs-lookup"><span data-stu-id="298d3-580">1227 (0x4CB)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-581">El punto de conexión de transporte de red ya tiene una dirección asociada.</span><span class="sxs-lookup"><span data-stu-id="298d3-581">The network transport endpoint already has an address associated with it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-582"><span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**Dirección de ERROR \_ \_ no \_ asociada**</span><span class="sxs-lookup"><span data-stu-id="298d3-582"><span id="ERROR_ADDRESS_NOT_ASSOCIATED"></span><span id="error_address_not_associated"></span>**ERROR\_ADDRESS\_NOT\_ASSOCIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-583">1228 (0x4CC)</span><span class="sxs-lookup"><span data-stu-id="298d3-583">1228 (0x4CC)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-584">Todavía no se ha asociado una dirección al punto de conexión de la red.</span><span class="sxs-lookup"><span data-stu-id="298d3-584">An address has not yet been associated with the network endpoint.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-585"><span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**conexión de ERROR \_ \_ no válida**</span><span class="sxs-lookup"><span data-stu-id="298d3-585"><span id="ERROR_CONNECTION_INVALID"></span><span id="error_connection_invalid"></span>**ERROR\_CONNECTION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-586">1229 (0x4CD)</span><span class="sxs-lookup"><span data-stu-id="298d3-586">1229 (0x4CD)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-587">Se intentó realizar una operación en una conexión de red inexistente.</span><span class="sxs-lookup"><span data-stu-id="298d3-587">An operation was attempted on a nonexistent network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-588"><span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**ERROR de \_ conexión \_ activa**</span><span class="sxs-lookup"><span data-stu-id="298d3-588"><span id="ERROR_CONNECTION_ACTIVE"></span><span id="error_connection_active"></span>**ERROR\_CONNECTION\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-589">1230 (0x4CE)</span><span class="sxs-lookup"><span data-stu-id="298d3-589">1230 (0x4CE)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-590">Se intentó realizar una operación no válida en una conexión de red activa.</span><span class="sxs-lookup"><span data-stu-id="298d3-590">An invalid operation was attempted on an active network connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-591"><span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERROR de \_ red \_ inaccesible**</span><span class="sxs-lookup"><span data-stu-id="298d3-591"><span id="ERROR_NETWORK_UNREACHABLE"></span><span id="error_network_unreachable"></span>**ERROR\_NETWORK\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-592">1231 (0x4CF)</span><span class="sxs-lookup"><span data-stu-id="298d3-592">1231 (0x4CF)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-593">No se puede tener acceso a la ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="298d3-593">The network location cannot be reached.</span></span> <span data-ttu-id="298d3-594">Para obtener información acerca de la solución de problemas de red, consulte la ayuda de Windows.</span><span class="sxs-lookup"><span data-stu-id="298d3-594">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-595"><span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**ERROR de \_ host no \_ accesible**</span><span class="sxs-lookup"><span data-stu-id="298d3-595"><span id="ERROR_HOST_UNREACHABLE"></span><span id="error_host_unreachable"></span>**ERROR\_HOST\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-596">1232 (0x4D0)</span><span class="sxs-lookup"><span data-stu-id="298d3-596">1232 (0x4D0)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-597">No se puede tener acceso a la ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="298d3-597">The network location cannot be reached.</span></span> <span data-ttu-id="298d3-598">Para obtener información acerca de la solución de problemas de red, consulte la ayuda de Windows.</span><span class="sxs-lookup"><span data-stu-id="298d3-598">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-599"><span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**Protocolo de ERROR \_ \_ inaccesible**</span><span class="sxs-lookup"><span data-stu-id="298d3-599"><span id="ERROR_PROTOCOL_UNREACHABLE"></span><span id="error_protocol_unreachable"></span>**ERROR\_PROTOCOL\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-600">1233 (0x4D1)</span><span class="sxs-lookup"><span data-stu-id="298d3-600">1233 (0x4D1)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-601">No se puede tener acceso a la ubicación de red.</span><span class="sxs-lookup"><span data-stu-id="298d3-601">The network location cannot be reached.</span></span> <span data-ttu-id="298d3-602">Para obtener información acerca de la solución de problemas de red, consulte la ayuda de Windows.</span><span class="sxs-lookup"><span data-stu-id="298d3-602">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-603"><span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**no \_ se \_ puede tener acceso al puerto de error**</span><span class="sxs-lookup"><span data-stu-id="298d3-603"><span id="ERROR_PORT_UNREACHABLE"></span><span id="error_port_unreachable"></span>**ERROR\_PORT\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-604">1234 (0x4D2)</span><span class="sxs-lookup"><span data-stu-id="298d3-604">1234 (0x4D2)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-605">No hay ningún servicio funcionando en el punto de conexión de la red de destino del sistema remoto.</span><span class="sxs-lookup"><span data-stu-id="298d3-605">No service is operating at the destination network endpoint on the remote system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-606"><span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**solicitud de ERROR \_ \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="298d3-606"><span id="ERROR_REQUEST_ABORTED"></span><span id="error_request_aborted"></span>**ERROR\_REQUEST\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-607">1235 (0x4D3)</span><span class="sxs-lookup"><span data-stu-id="298d3-607">1235 (0x4D3)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-608">Se anuló la solicitud.</span><span class="sxs-lookup"><span data-stu-id="298d3-608">The request was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-609"><span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERROR de \_ conexión \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="298d3-609"><span id="ERROR_CONNECTION_ABORTED"></span><span id="error_connection_aborted"></span>**ERROR\_CONNECTION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-610">1236 (0x4D4)</span><span class="sxs-lookup"><span data-stu-id="298d3-610">1236 (0x4D4)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-611">El sistema local anuló la conexión de red.</span><span class="sxs-lookup"><span data-stu-id="298d3-611">The network connection was aborted by the local system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-612"><span id="ERROR_RETRY"></span><span id="error_retry"></span>**ERROR de \_ reintento**</span><span class="sxs-lookup"><span data-stu-id="298d3-612"><span id="ERROR_RETRY"></span><span id="error_retry"></span>**ERROR\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-613">1237 (0x4D5)</span><span class="sxs-lookup"><span data-stu-id="298d3-613">1237 (0x4D5)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-614">No se pudo completar la operación.</span><span class="sxs-lookup"><span data-stu-id="298d3-614">The operation could not be completed.</span></span> <span data-ttu-id="298d3-615">Se debe realizar un reintento.</span><span class="sxs-lookup"><span data-stu-id="298d3-615">A retry should be performed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-616"><span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**\_límite de \_ número de conexiones de error \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-616"><span id="ERROR_CONNECTION_COUNT_LIMIT"></span><span id="error_connection_count_limit"></span>**ERROR\_CONNECTION\_COUNT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-617">1238 (0x4D6)</span><span class="sxs-lookup"><span data-stu-id="298d3-617">1238 (0x4D6)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-618">No se pudo establecer una conexión con el servidor porque se ha alcanzado el límite del número de conexiones simultáneas para esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="298d3-618">A connection to the server could not be made because the limit on the number of concurrent connections for this account has been reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-619"><span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**restricción de tiempo de inicio de sesión de ERROR \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-619"><span id="ERROR_LOGIN_TIME_RESTRICTION"></span><span id="error_login_time_restriction"></span>**ERROR\_LOGIN\_TIME\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-620">1239 (0x4D7)</span><span class="sxs-lookup"><span data-stu-id="298d3-620">1239 (0x4D7)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-621">Intentando iniciar sesión durante una hora del día no autorizada para esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="298d3-621">Attempting to log in during an unauthorized time of day for this account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-622"><span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**ERROR de \_ Inicio de sesión \_ WKSTA \_ RESTRICTION**</span><span class="sxs-lookup"><span data-stu-id="298d3-622"><span id="ERROR_LOGIN_WKSTA_RESTRICTION"></span><span id="error_login_wksta_restriction"></span>**ERROR\_LOGIN\_WKSTA\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-623">1240 (0x4D8)</span><span class="sxs-lookup"><span data-stu-id="298d3-623">1240 (0x4D8)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-624">La cuenta no está autorizada para iniciar sesión desde esta estación.</span><span class="sxs-lookup"><span data-stu-id="298d3-624">The account is not authorized to log in from this station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-625"><span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERROR \_ de \_ dirección incorrecta**</span><span class="sxs-lookup"><span data-stu-id="298d3-625"><span id="ERROR_INCORRECT_ADDRESS"></span><span id="error_incorrect_address"></span>**ERROR\_INCORRECT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-626">1241 (0x4D9)</span><span class="sxs-lookup"><span data-stu-id="298d3-626">1241 (0x4D9)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-627">No se pudo usar la dirección de red para la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="298d3-627">The network address could not be used for the operation requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-628"><span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERROR \_ ya \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="298d3-628"><span id="ERROR_ALREADY_REGISTERED"></span><span id="error_already_registered"></span>**ERROR\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-629">1242 (0x4DA)</span><span class="sxs-lookup"><span data-stu-id="298d3-629">1242 (0x4DA)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-630">El servicio ya está registrado.</span><span class="sxs-lookup"><span data-stu-id="298d3-630">The service is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-631"><span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**\_ \_ no \_ se encontró el servicio de error**</span><span class="sxs-lookup"><span data-stu-id="298d3-631"><span id="ERROR_SERVICE_NOT_FOUND"></span><span id="error_service_not_found"></span>**ERROR\_SERVICE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-632">1243 (0x4DB)</span><span class="sxs-lookup"><span data-stu-id="298d3-632">1243 (0x4DB)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-633">El servicio especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="298d3-633">The specified service does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-634"><span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERROR \_ no \_ autenticado**</span><span class="sxs-lookup"><span data-stu-id="298d3-634"><span id="ERROR_NOT_AUTHENTICATED"></span><span id="error_not_authenticated"></span>**ERROR\_NOT\_AUTHENTICATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-635">1244 (0x4DC)</span><span class="sxs-lookup"><span data-stu-id="298d3-635">1244 (0x4DC)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-636">No se realizó la operación solicitada porque el usuario no se ha autenticado.</span><span class="sxs-lookup"><span data-stu-id="298d3-636">The operation being requested was not performed because the user has not been authenticated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-637"><span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERROR \_ al \_ iniciar sesión \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-637"><span id="ERROR_NOT_LOGGED_ON"></span><span id="error_not_logged_on"></span>**ERROR\_NOT\_LOGGED\_ON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-638">1245 (0x4DD)</span><span class="sxs-lookup"><span data-stu-id="298d3-638">1245 (0x4DD)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-639">No se realizó la operación solicitada porque el usuario no ha iniciado sesión en la red.</span><span class="sxs-lookup"><span data-stu-id="298d3-639">The operation being requested was not performed because the user has not logged on to the network.</span></span> <span data-ttu-id="298d3-640">El servicio especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="298d3-640">The specified service does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-641"><span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**ERROR de \_ continuación**</span><span class="sxs-lookup"><span data-stu-id="298d3-641"><span id="ERROR_CONTINUE"></span><span id="error_continue"></span>**ERROR\_CONTINUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-642">1246 (0x4DE)</span><span class="sxs-lookup"><span data-stu-id="298d3-642">1246 (0x4DE)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-643">Continúe con el trabajo en curso.</span><span class="sxs-lookup"><span data-stu-id="298d3-643">Continue with work in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-644"><span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERROR \_ ya \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="298d3-644"><span id="ERROR_ALREADY_INITIALIZED"></span><span id="error_already_initialized"></span>**ERROR\_ALREADY\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-645">1247 (0x4DF)</span><span class="sxs-lookup"><span data-stu-id="298d3-645">1247 (0x4DF)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-646">Se intentó realizar una operación de inicialización cuando ya se ha completado la inicialización.</span><span class="sxs-lookup"><span data-stu-id="298d3-646">An attempt was made to perform an initialization operation when initialization has already been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-647"><span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERROR: \_ no hay \_ más \_ dispositivos**</span><span class="sxs-lookup"><span data-stu-id="298d3-647"><span id="ERROR_NO_MORE_DEVICES"></span><span id="error_no_more_devices"></span>**ERROR\_NO\_MORE\_DEVICES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-648">1248 (0x4E0)</span><span class="sxs-lookup"><span data-stu-id="298d3-648">1248 (0x4E0)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-649">No hay más dispositivos locales.</span><span class="sxs-lookup"><span data-stu-id="298d3-649">No more local devices.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-650"><span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**NO se ha podido \_ \_ este \_ sitio**</span><span class="sxs-lookup"><span data-stu-id="298d3-650"><span id="ERROR_NO_SUCH_SITE"></span><span id="error_no_such_site"></span>**ERROR\_NO\_SUCH\_SITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-651">1249 (0x4E1)</span><span class="sxs-lookup"><span data-stu-id="298d3-651">1249 (0x4E1)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-652">El sitio especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="298d3-652">The specified site does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-653"><span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**\_existe un \_ controlador de dominio de error \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-653"><span id="ERROR_DOMAIN_CONTROLLER_EXISTS"></span><span id="error_domain_controller_exists"></span>**ERROR\_DOMAIN\_CONTROLLER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-654">1250 (0x4E2)</span><span class="sxs-lookup"><span data-stu-id="298d3-654">1250 (0x4E2)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-655">Ya existe un controlador de dominio con el nombre especificado.</span><span class="sxs-lookup"><span data-stu-id="298d3-655">A domain controller with the specified name already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-656"><span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERROR \_ solo \_ si \_ está conectado**</span><span class="sxs-lookup"><span data-stu-id="298d3-656"><span id="ERROR_ONLY_IF_CONNECTED"></span><span id="error_only_if_connected"></span>**ERROR\_ONLY\_IF\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-657">1251 (0x4E3)</span><span class="sxs-lookup"><span data-stu-id="298d3-657">1251 (0x4E3)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-658">Esta operación solo se admite cuando se está conectado al servidor.</span><span class="sxs-lookup"><span data-stu-id="298d3-658">This operation is supported only when you are connected to the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-659"><span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERROR al \_ invalidar \_ nochanges**</span><span class="sxs-lookup"><span data-stu-id="298d3-659"><span id="ERROR_OVERRIDE_NOCHANGES"></span><span id="error_override_nochanges"></span>**ERROR\_OVERRIDE\_NOCHANGES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-660">1252 (0x4E4)</span><span class="sxs-lookup"><span data-stu-id="298d3-660">1252 (0x4E4)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-661">El marco de directiva de grupo debe llamar a la extensión incluso si no hay ningún cambio.</span><span class="sxs-lookup"><span data-stu-id="298d3-661">The group policy framework should call the extension even if there are no changes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-662"><span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERROR \_ de \_ Perfil de usuario incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-662"><span id="ERROR_BAD_USER_PROFILE"></span><span id="error_bad_user_profile"></span>**ERROR\_BAD\_USER\_PROFILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-663">1253 (0x4E5)</span><span class="sxs-lookup"><span data-stu-id="298d3-663">1253 (0x4E5)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-664">El usuario especificado no tiene un perfil válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-664">The specified user does not have a valid profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-665"><span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERROR \_ no \_ compatible \_ con \_ SBS**</span><span class="sxs-lookup"><span data-stu-id="298d3-665"><span id="ERROR_NOT_SUPPORTED_ON_SBS"></span><span id="error_not_supported_on_sbs"></span>**ERROR\_NOT\_SUPPORTED\_ON\_SBS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-666">1254 (0x4E6)</span><span class="sxs-lookup"><span data-stu-id="298d3-666">1254 (0x4E6)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-667">Esta operación no se admite en un equipo que ejecute Windows Server 2003 para Small Business Server.</span><span class="sxs-lookup"><span data-stu-id="298d3-667">This operation is not supported on a computer running Windows Server 2003 for Small Business Server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-668"><span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**ERROR \_ \_ de apagado \_ del servidor en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="298d3-668"><span id="ERROR_SERVER_SHUTDOWN_IN_PROGRESS"></span><span id="error_server_shutdown_in_progress"></span>**ERROR\_SERVER\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-669">1255 (0x4E7)</span><span class="sxs-lookup"><span data-stu-id="298d3-669">1255 (0x4E7)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-670">El equipo servidor se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="298d3-670">The server machine is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-671"><span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERROR de \_ host \_ inactivo**</span><span class="sxs-lookup"><span data-stu-id="298d3-671"><span id="ERROR_HOST_DOWN"></span><span id="error_host_down"></span>**ERROR\_HOST\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-672">1256 (0x4E8)</span><span class="sxs-lookup"><span data-stu-id="298d3-672">1256 (0x4E8)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-673">El sistema remoto no está disponible.</span><span class="sxs-lookup"><span data-stu-id="298d3-673">The remote system is not available.</span></span> <span data-ttu-id="298d3-674">Para obtener información acerca de la solución de problemas de red, consulte la ayuda de Windows.</span><span class="sxs-lookup"><span data-stu-id="298d3-674">For information about network troubleshooting, see Windows Help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-675"><span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**ERROR \_ de \_ SID sin cuenta \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-675"><span id="ERROR_NON_ACCOUNT_SID"></span><span id="error_non_account_sid"></span>**ERROR\_NON\_ACCOUNT\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-676">1257 (0x4E9)</span><span class="sxs-lookup"><span data-stu-id="298d3-676">1257 (0x4E9)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-677">El identificador de seguridad proporcionado no procede de un dominio de cuenta.</span><span class="sxs-lookup"><span data-stu-id="298d3-677">The security identifier provided is not from an account domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-678"><span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERROR \_ de \_ SID sin dominio \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-678"><span id="ERROR_NON_DOMAIN_SID"></span><span id="error_non_domain_sid"></span>**ERROR\_NON\_DOMAIN\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-679">1258 (0x4EA)</span><span class="sxs-lookup"><span data-stu-id="298d3-679">1258 (0x4EA)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-680">El identificador de seguridad proporcionado no tiene un componente de dominio.</span><span class="sxs-lookup"><span data-stu-id="298d3-680">The security identifier provided does not have a domain component.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-681"><span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**ERROR de el \_ \_ bloque APPHELP**</span><span class="sxs-lookup"><span data-stu-id="298d3-681"><span id="ERROR_APPHELP_BLOCK"></span><span id="error_apphelp_block"></span>**ERROR\_APPHELP\_BLOCK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-682">1259 (0x4EB)</span><span class="sxs-lookup"><span data-stu-id="298d3-682">1259 (0x4EB)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-683">Cuadro de diálogo de AppHelp cancelado, lo que impide que se inicie la aplicación.</span><span class="sxs-lookup"><span data-stu-id="298d3-683">AppHelp dialog canceled thus preventing the application from starting.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-684"><span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**ERROR \_ \_ de acceso deshabilitado \_ por \_ Directiva**</span><span class="sxs-lookup"><span data-stu-id="298d3-684"><span id="ERROR_ACCESS_DISABLED_BY_POLICY"></span><span id="error_access_disabled_by_policy"></span>**ERROR\_ACCESS\_DISABLED\_BY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-685">1260 (0x4EC)</span><span class="sxs-lookup"><span data-stu-id="298d3-685">1260 (0x4EC)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-686">Este programa está bloqueado por la Directiva de grupo.</span><span class="sxs-lookup"><span data-stu-id="298d3-686">This program is blocked by group policy.</span></span> <span data-ttu-id="298d3-687">Para obtener más información, póngase en contacto con el administrador del sistema.</span><span class="sxs-lookup"><span data-stu-id="298d3-687">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-688"><span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERROR de \_ registro de NAT de reg \_ \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-688"><span id="ERROR_REG_NAT_CONSUMPTION"></span><span id="error_reg_nat_consumption"></span>**ERROR\_REG\_NAT\_CONSUMPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-689">1261 (0x4ED)</span><span class="sxs-lookup"><span data-stu-id="298d3-689">1261 (0x4ED)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-690">Un programa intenta utilizar un valor de registro no válido.</span><span class="sxs-lookup"><span data-stu-id="298d3-690">A program attempt to use an invalid register value.</span></span> <span data-ttu-id="298d3-691">Normalmente causado por un registro no inicializado.</span><span class="sxs-lookup"><span data-stu-id="298d3-691">Normally caused by an uninitialized register.</span></span> <span data-ttu-id="298d3-692">Este error es específico de Itanium.</span><span class="sxs-lookup"><span data-stu-id="298d3-692">This error is Itanium specific.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-693"><span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERROR \_ CSCSHARE \_ sin conexión**</span><span class="sxs-lookup"><span data-stu-id="298d3-693"><span id="ERROR_CSCSHARE_OFFLINE"></span><span id="error_cscshare_offline"></span>**ERROR\_CSCSHARE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-694">1262 (0x4EE)</span><span class="sxs-lookup"><span data-stu-id="298d3-694">1262 (0x4EE)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-695">El recurso compartido está actualmente sin conexión o no existe.</span><span class="sxs-lookup"><span data-stu-id="298d3-695">The share is currently offline or does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-696"><span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**ERROR \_ PKINIT \_ error**</span><span class="sxs-lookup"><span data-stu-id="298d3-696"><span id="ERROR_PKINIT_FAILURE"></span><span id="error_pkinit_failure"></span>**ERROR\_PKINIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-697">1263 (0x4EF)</span><span class="sxs-lookup"><span data-stu-id="298d3-697">1263 (0x4EF)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-698">El protocolo Kerberos encontró un error al validar el certificado KDC durante el inicio de sesión de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="298d3-698">The Kerberos protocol encountered an error while validating the KDC certificate during smartcard logon.</span></span> <span data-ttu-id="298d3-699">Hay más información en el registro de eventos del sistema.</span><span class="sxs-lookup"><span data-stu-id="298d3-699">There is more information in the system event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-700"><span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**ERROR en el \_ \_ subsistema de tarjeta inteligente \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-700"><span id="ERROR_SMARTCARD_SUBSYSTEM_FAILURE"></span><span id="error_smartcard_subsystem_failure"></span>**ERROR\_SMARTCARD\_SUBSYSTEM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-701">1264 (0x4F0)</span><span class="sxs-lookup"><span data-stu-id="298d3-701">1264 (0x4F0)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-702">El protocolo Kerberos encontró un error al intentar el uso del subsistema de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="298d3-702">The Kerberos protocol encountered an error while attempting to utilize the smartcard subsystem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-703"><span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**ERROR de \_ degradación \_ detectado**</span><span class="sxs-lookup"><span data-stu-id="298d3-703"><span id="ERROR_DOWNGRADE_DETECTED"></span><span id="error_downgrade_detected"></span>**ERROR\_DOWNGRADE\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-704">1265 (0x4F1)</span><span class="sxs-lookup"><span data-stu-id="298d3-704">1265 (0x4F1)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-705">El sistema no puede ponerse en contacto con un controlador de dominio para atender la solicitud de autenticación.</span><span class="sxs-lookup"><span data-stu-id="298d3-705">The system cannot contact a domain controller to service the authentication request.</span></span> <span data-ttu-id="298d3-706">Vuelva a intentarlo más tarde.</span><span class="sxs-lookup"><span data-stu-id="298d3-706">Please try again later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-707"><span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**máquina de ERROR \_ \_ bloqueada**</span><span class="sxs-lookup"><span data-stu-id="298d3-707"><span id="ERROR_MACHINE_LOCKED"></span><span id="error_machine_locked"></span>**ERROR\_MACHINE\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-708">1271 (0x4F7)</span><span class="sxs-lookup"><span data-stu-id="298d3-708">1271 (0x4F7)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-709">El equipo está bloqueado y no se puede apagar sin la opción Force.</span><span class="sxs-lookup"><span data-stu-id="298d3-709">The machine is locked and cannot be shut down without the force option.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-710"><span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**la \_ devolución de llamada de error \_ proporcionó \_ datos no válidos \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-710"><span id="ERROR_CALLBACK_SUPPLIED_INVALID_DATA"></span><span id="error_callback_supplied_invalid_data"></span>**ERROR\_CALLBACK\_SUPPLIED\_INVALID\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-711">1273 (0x4F9)</span><span class="sxs-lookup"><span data-stu-id="298d3-711">1273 (0x4F9)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-712">Una devolución de llamada definida por la aplicación proporcionó datos no válidos cuando se llamó a.</span><span class="sxs-lookup"><span data-stu-id="298d3-712">An application-defined callback gave invalid data when called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-713"><span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**ERROR en la \_ sincronización en \_ primer plano \_ \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-713"><span id="ERROR_SYNC_FOREGROUND_REFRESH_REQUIRED"></span><span id="error_sync_foreground_refresh_required"></span>**ERROR\_SYNC\_FOREGROUND\_REFRESH\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-714">1274 (0x4FA)</span><span class="sxs-lookup"><span data-stu-id="298d3-714">1274 (0x4FA)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-715">El marco de directiva de grupo debe llamar a la extensión en la actualización sincrónica de la Directiva de primer plano.</span><span class="sxs-lookup"><span data-stu-id="298d3-715">The group policy framework should call the extension in the synchronous foreground policy refresh.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-716"><span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**controlador de ERROR \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="298d3-716"><span id="ERROR_DRIVER_BLOCKED"></span><span id="error_driver_blocked"></span>**ERROR\_DRIVER\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-717">1275 (0x4FB)</span><span class="sxs-lookup"><span data-stu-id="298d3-717">1275 (0x4FB)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-718">Se ha bloqueado la carga de este controlador.</span><span class="sxs-lookup"><span data-stu-id="298d3-718">This driver has been blocked from loading.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-719"><span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**ERROR \_ \_ de importación no válida \_ de un \_ \_ archivo no dll**</span><span class="sxs-lookup"><span data-stu-id="298d3-719"><span id="ERROR_INVALID_IMPORT_OF_NON_DLL"></span><span id="error_invalid_import_of_non_dll"></span>**ERROR\_INVALID\_IMPORT\_OF\_NON\_DLL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-720">1276 (0x4FC)</span><span class="sxs-lookup"><span data-stu-id="298d3-720">1276 (0x4FC)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-721">Una biblioteca de vínculos dinámicos (DLL) hacía referencia a un módulo que no era un archivo DLL ni la imagen ejecutable del proceso.</span><span class="sxs-lookup"><span data-stu-id="298d3-721">A dynamic link library (DLL) referenced a module that was neither a DLL nor the process's executable image.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-722"><span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ERROR de \_ acceso a \_ WebBlade deshabilitado \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-722"><span id="ERROR_ACCESS_DISABLED_WEBBLADE"></span><span id="error_access_disabled_webblade"></span>**ERROR\_ACCESS\_DISABLED\_WEBBLADE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-723">1277 (0x4FD)</span><span class="sxs-lookup"><span data-stu-id="298d3-723">1277 (0x4FD)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-724">Windows no puede abrir este programa porque se ha deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="298d3-724">Windows cannot open this program since it has been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-725"><span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ERROR de \_ acceso a la \_ manipulación de \_ WebBlade deshabilitada \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-725"><span id="ERROR_ACCESS_DISABLED_WEBBLADE_TAMPER"></span><span id="error_access_disabled_webblade_tamper"></span>**ERROR\_ACCESS\_DISABLED\_WEBBLADE\_TAMPER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-726">1278 (0x4FE)</span><span class="sxs-lookup"><span data-stu-id="298d3-726">1278 (0x4FE)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-727">Windows no puede abrir este programa porque el sistema de cumplimiento de licencias se ha manipulado o dañado.</span><span class="sxs-lookup"><span data-stu-id="298d3-727">Windows cannot open this program because the license enforcement system has been tampered with or become corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-728"><span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**ERROR de recuperación de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-728"><span id="ERROR_RECOVERY_FAILURE"></span><span id="error_recovery_failure"></span>**ERROR\_RECOVERY\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-729">1279 (0x4FF)</span><span class="sxs-lookup"><span data-stu-id="298d3-729">1279 (0x4FF)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-730">Error en la recuperación de la transacción.</span><span class="sxs-lookup"><span data-stu-id="298d3-730">A transaction recover failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-731"><span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERROR \_ ya \_ Fiber**</span><span class="sxs-lookup"><span data-stu-id="298d3-731"><span id="ERROR_ALREADY_FIBER"></span><span id="error_already_fiber"></span>**ERROR\_ALREADY\_FIBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-732">1280 (0x500)</span><span class="sxs-lookup"><span data-stu-id="298d3-732">1280 (0x500)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-733">El subproceso actual ya se ha convertido en una fibra.</span><span class="sxs-lookup"><span data-stu-id="298d3-733">The current thread has already been converted to a fiber.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-734"><span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERROR \_ ya \_ subproceso**</span><span class="sxs-lookup"><span data-stu-id="298d3-734"><span id="ERROR_ALREADY_THREAD"></span><span id="error_already_thread"></span>**ERROR\_ALREADY\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-735">1281 (0x501)</span><span class="sxs-lookup"><span data-stu-id="298d3-735">1281 (0x501)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-736">El subproceso actual ya se ha convertido a partir de una fibra.</span><span class="sxs-lookup"><span data-stu-id="298d3-736">The current thread has already been converted from a fiber.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-737"><span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**\_saturación del \_ búfer de pila de errores \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-737"><span id="ERROR_STACK_BUFFER_OVERRUN"></span><span id="error_stack_buffer_overrun"></span>**ERROR\_STACK\_BUFFER\_OVERRUN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-738">1282 (0x502)</span><span class="sxs-lookup"><span data-stu-id="298d3-738">1282 (0x502)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-739">El sistema detectó un desbordamiento de un búfer basado en la pila en esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="298d3-739">The system detected an overrun of a stack-based buffer in this application.</span></span> <span data-ttu-id="298d3-740">Esta saturación podría permitir que un usuario malintencionado gane el control de esta aplicación.</span><span class="sxs-lookup"><span data-stu-id="298d3-740">This overrun could potentially allow a malicious user to gain control of this application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-741"><span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**cuota de parámetro de ERROR \_ \_ \_ superada**</span><span class="sxs-lookup"><span data-stu-id="298d3-741"><span id="ERROR_PARAMETER_QUOTA_EXCEEDED"></span><span id="error_parameter_quota_exceeded"></span>**ERROR\_PARAMETER\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-742">1283 (0x503)</span><span class="sxs-lookup"><span data-stu-id="298d3-742">1283 (0x503)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-743">Los datos presentes en uno de los parámetros son más de lo que puede funcionar en la función.</span><span class="sxs-lookup"><span data-stu-id="298d3-743">Data present in one of the parameters is more than the function can operate on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-744"><span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**depurador de errores \_ \_ inactivo**</span><span class="sxs-lookup"><span data-stu-id="298d3-744"><span id="ERROR_DEBUGGER_INACTIVE"></span><span id="error_debugger_inactive"></span>**ERROR\_DEBUGGER\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-745">1284 (0x504)</span><span class="sxs-lookup"><span data-stu-id="298d3-745">1284 (0x504)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-746">Error al intentar realizar una operación en un objeto de depuración porque el objeto está en proceso de eliminación.</span><span class="sxs-lookup"><span data-stu-id="298d3-746">An attempt to do an operation on a debug object failed because the object is in the process of being deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-747"><span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**ERROR \_ \_ al cargar el retraso de errores \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-747"><span id="ERROR_DELAY_LOAD_FAILED"></span><span id="error_delay_load_failed"></span>**ERROR\_DELAY\_LOAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-748">1285 (0x505)</span><span class="sxs-lookup"><span data-stu-id="298d3-748">1285 (0x505)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-749">Error al tratar de cargar con retraso un archivo. dll u obtener una dirección de función en un archivo. dll de carga retrasada.</span><span class="sxs-lookup"><span data-stu-id="298d3-749">An attempt to delay-load a .dll or get a function address in a delay-loaded .dll failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-750"><span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERROR \_ VDM no \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="298d3-750"><span id="ERROR_VDM_DISALLOWED"></span><span id="error_vdm_disallowed"></span>**ERROR\_VDM\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-751">1286 (0x506)</span><span class="sxs-lookup"><span data-stu-id="298d3-751">1286 (0x506)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-752">%1 es una aplicación de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="298d3-752">%1 is a 16-bit application.</span></span> <span data-ttu-id="298d3-753">No tiene permisos para ejecutar aplicaciones de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="298d3-753">You do not have permissions to execute 16-bit applications.</span></span> <span data-ttu-id="298d3-754">Compruebe los permisos del administrador del sistema.</span><span class="sxs-lookup"><span data-stu-id="298d3-754">Check your permissions with your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-755"><span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**error no \_ identificado \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-755"><span id="ERROR_UNIDENTIFIED_ERROR"></span><span id="error_unidentified_error"></span>**ERROR\_UNIDENTIFIED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-756">1287 (0x507)</span><span class="sxs-lookup"><span data-stu-id="298d3-756">1287 (0x507)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-757">Existe información insuficiente para identificar la causa del error.</span><span class="sxs-lookup"><span data-stu-id="298d3-757">Insufficient information exists to identify the cause of failure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-758"><span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERROR en el \_ \_ parámetro CRUNTIME no válido \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-758"><span id="ERROR_INVALID_CRUNTIME_PARAMETER"></span><span id="error_invalid_cruntime_parameter"></span>**ERROR\_INVALID\_CRUNTIME\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-759">1288 (0x508)</span><span class="sxs-lookup"><span data-stu-id="298d3-759">1288 (0x508)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-760">El parámetro pasado a una función en tiempo de ejecución de C es incorrecto.</span><span class="sxs-lookup"><span data-stu-id="298d3-760">The parameter passed to a C runtime function is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-761"><span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERROR \_ más allá de \_ VDL**</span><span class="sxs-lookup"><span data-stu-id="298d3-761"><span id="ERROR_BEYOND_VDL"></span><span id="error_beyond_vdl"></span>**ERROR\_BEYOND\_VDL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-762">1289 (0x509)</span><span class="sxs-lookup"><span data-stu-id="298d3-762">1289 (0x509)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-763">La operación se produjo más allá de la longitud de datos válida del archivo.</span><span class="sxs-lookup"><span data-stu-id="298d3-763">The operation occurred beyond the valid data length of the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-764"><span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERROR de \_ tipo de SID de servicio no compatible \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-764"><span id="ERROR_INCOMPATIBLE_SERVICE_SID_TYPE"></span><span id="error_incompatible_service_sid_type"></span>**ERROR\_INCOMPATIBLE\_SERVICE\_SID\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-765">1290 (0x50A)</span><span class="sxs-lookup"><span data-stu-id="298d3-765">1290 (0x50A)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-766">No se pudo iniciar el servicio porque uno o varios servicios del mismo proceso tienen una configuración de tipo de SID de servicio no compatible.</span><span class="sxs-lookup"><span data-stu-id="298d3-766">The service start failed since one or more services in the same process have an incompatible service SID type setting.</span></span> <span data-ttu-id="298d3-767">Un servicio con tipo de SID de servicio restringido solo puede coexistir en el mismo proceso con otros servicios con un tipo de SID restringido.</span><span class="sxs-lookup"><span data-stu-id="298d3-767">A service with restricted service SID type can only coexist in the same process with other services with a restricted SID type.</span></span> <span data-ttu-id="298d3-768">Si se acaba de configurar el tipo de SID de servicio para este servicio, el proceso de hospedaje debe reiniciarse para iniciar este servicio.</span><span class="sxs-lookup"><span data-stu-id="298d3-768">If the service SID type for this service was just configured, the hosting process must be restarted in order to start this service.</span></span>

<span data-ttu-id="298d3-769">En Windows Server 2003 y Windows XP, un servicio sin restricciones no puede coexistir en el mismo proceso con otros servicios.</span><span class="sxs-lookup"><span data-stu-id="298d3-769">On Windows Server 2003 and Windows XP, an unrestricted service cannot coexist in the same process with other services.</span></span> <span data-ttu-id="298d3-770">El servicio con el tipo de SID de servicio sin restricciones debe moverse a un proceso de propiedad para poder iniciar este servicio.</span><span class="sxs-lookup"><span data-stu-id="298d3-770">The service with the unrestricted service SID type must be moved to an owned process in order to start this service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-771"><span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**proceso de controlador de ERROR \_ \_ \_ finalizado**</span><span class="sxs-lookup"><span data-stu-id="298d3-771"><span id="ERROR_DRIVER_PROCESS_TERMINATED"></span><span id="error_driver_process_terminated"></span>**ERROR\_DRIVER\_PROCESS\_TERMINATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-772">1291 (0x50B)</span><span class="sxs-lookup"><span data-stu-id="298d3-772">1291 (0x50B)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-773">El proceso que hospeda el controlador de este dispositivo ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="298d3-773">The process hosting the driver for this device has been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-774"><span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**\_límite de implementación de errores \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-774"><span id="ERROR_IMPLEMENTATION_LIMIT"></span><span id="error_implementation_limit"></span>**ERROR\_IMPLEMENTATION\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-775">1292 (0x50C)</span><span class="sxs-lookup"><span data-stu-id="298d3-775">1292 (0x50C)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-776">Una operación intentó superar un límite definido por la implementación.</span><span class="sxs-lookup"><span data-stu-id="298d3-776">An operation attempted to exceed an implementation-defined limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-777"><span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**el \_ proceso de error \_ está \_ protegido**</span><span class="sxs-lookup"><span data-stu-id="298d3-777"><span id="ERROR_PROCESS_IS_PROTECTED"></span><span id="error_process_is_protected"></span>**ERROR\_PROCESS\_IS\_PROTECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-778">1293 (0x50D)</span><span class="sxs-lookup"><span data-stu-id="298d3-778">1293 (0x50D)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-779">El proceso de destino o el proceso que contiene el subproceso de destino es un proceso protegido.</span><span class="sxs-lookup"><span data-stu-id="298d3-779">Either the target process, or the target thread's containing process, is a protected process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-780"><span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**ERROR del \_ servicio de \_ notificación de \_ cliente \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-780"><span id="ERROR_SERVICE_NOTIFY_CLIENT_LAGGING"></span><span id="error_service_notify_client_lagging"></span>**ERROR\_SERVICE\_NOTIFY\_CLIENT\_LAGGING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-781">1294 (0x50E)</span><span class="sxs-lookup"><span data-stu-id="298d3-781">1294 (0x50E)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-782">El cliente de notificación de servicio se atrasa demasiado detrás del estado actual de los servicios de la máquina.</span><span class="sxs-lookup"><span data-stu-id="298d3-782">The service notification client is lagging too far behind the current state of services in the machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-783"><span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**cuota de disco de ERROR \_ \_ \_ superada**</span><span class="sxs-lookup"><span data-stu-id="298d3-783"><span id="ERROR_DISK_QUOTA_EXCEEDED"></span><span id="error_disk_quota_exceeded"></span>**ERROR\_DISK\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-784">1295 (0x50F)</span><span class="sxs-lookup"><span data-stu-id="298d3-784">1295 (0x50F)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-785">No se pudo realizar la operación de archivo solicitada porque se superó la cuota de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="298d3-785">The requested file operation failed because the storage quota was exceeded.</span></span> <span data-ttu-id="298d3-786">Para liberar espacio en disco, mueva los archivos a otra ubicación o elimine los archivos innecesarios.</span><span class="sxs-lookup"><span data-stu-id="298d3-786">To free up disk space, move files to a different location or delete unnecessary files.</span></span> <span data-ttu-id="298d3-787">Para obtener más información, póngase en contacto con el administrador del sistema.</span><span class="sxs-lookup"><span data-stu-id="298d3-787">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-788"><span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**contenido de ERROR \_ \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="298d3-788"><span id="ERROR_CONTENT_BLOCKED"></span><span id="error_content_blocked"></span>**ERROR\_CONTENT\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-789">1296 (0x510)</span><span class="sxs-lookup"><span data-stu-id="298d3-789">1296 (0x510)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-790">No se pudo realizar la operación de archivo solicitada porque la Directiva de almacenamiento bloquea ese tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="298d3-790">The requested file operation failed because the storage policy blocks that type of file.</span></span> <span data-ttu-id="298d3-791">Para obtener más información, póngase en contacto con el administrador del sistema.</span><span class="sxs-lookup"><span data-stu-id="298d3-791">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-792"><span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**ERROR de privilegio de servicio no \_ compatible \_ \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-792"><span id="ERROR_INCOMPATIBLE_SERVICE_PRIVILEGE"></span><span id="error_incompatible_service_privilege"></span>**ERROR\_INCOMPATIBLE\_SERVICE\_PRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-793">1297 (0x511)</span><span class="sxs-lookup"><span data-stu-id="298d3-793">1297 (0x511)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-794">Un privilegio que el servicio necesita para funcionar correctamente no existe en la configuración de la cuenta de servicio.</span><span class="sxs-lookup"><span data-stu-id="298d3-794">A privilege that the service requires to function properly does not exist in the service account configuration.</span></span> <span data-ttu-id="298d3-795">Puede usar el complemento Servicios de Microsoft Management Console (MMC) (Services. msc) y el complemento MMC configuración de seguridad local (SECPOL. msc) para ver la configuración del servicio y la configuración de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="298d3-795">You may use the Services Microsoft Management Console (MMC) snap-in (services.msc) and the Local Security Settings MMC snap-in (secpol.msc) to view the service configuration and the account configuration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-796"><span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**ERROR de la aplicación de ERROR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="298d3-796"><span id="ERROR_APP_HANG"></span><span id="error_app_hang"></span>**ERROR\_APP\_HANG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-797">1298 (0x512)</span><span class="sxs-lookup"><span data-stu-id="298d3-797">1298 (0x512)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-798">Parece que un subproceso implicado en esta operación no responde.</span><span class="sxs-lookup"><span data-stu-id="298d3-798">A thread involved in this operation appears to be unresponsive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="298d3-799"><span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**ERROR \_ de \_ etiqueta no válida**</span><span class="sxs-lookup"><span data-stu-id="298d3-799"><span id="ERROR_INVALID_LABEL"></span><span id="error_invalid_label"></span>**ERROR\_INVALID\_LABEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="298d3-800">1299 (0x513)</span><span class="sxs-lookup"><span data-stu-id="298d3-800">1299 (0x513)</span></span>
</dt> <dt>



<span data-ttu-id="298d3-801">Indica que un determinado identificador de seguridad no se puede asignar como etiqueta de un objeto.</span><span class="sxs-lookup"><span data-stu-id="298d3-801">Indicates a particular Security ID may not be assigned as the label of an object.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="298d3-802">Requisitos</span><span class="sxs-lookup"><span data-stu-id="298d3-802">Requirements</span></span>



| <span data-ttu-id="298d3-803">Requisito</span><span class="sxs-lookup"><span data-stu-id="298d3-803">Requirement</span></span> | <span data-ttu-id="298d3-804">Value</span><span class="sxs-lookup"><span data-stu-id="298d3-804">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="298d3-805">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="298d3-805">Minimum supported client</span></span><br/> | <span data-ttu-id="298d3-806">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="298d3-806">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="298d3-807">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="298d3-807">Minimum supported server</span></span><br/> | <span data-ttu-id="298d3-808">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="298d3-808">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="298d3-809">Encabezado</span><span class="sxs-lookup"><span data-stu-id="298d3-809">Header</span></span><br/>                   | <dl> <span data-ttu-id="298d3-810"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="298d3-810"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="298d3-811">Vea también</span><span class="sxs-lookup"><span data-stu-id="298d3-811">See also</span></span>

<dl> <dt>

[<span data-ttu-id="298d3-812">Códigos de error del sistema</span><span class="sxs-lookup"><span data-stu-id="298d3-812">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




