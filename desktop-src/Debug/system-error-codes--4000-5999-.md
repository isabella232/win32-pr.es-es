---
description: Describe los códigos de error 4000-5999 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: 1d2f7160-6322-4c75-abbc-4a882bbdf7ce
title: Códigos de error del sistema (4000-5999) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: bfd39042489f2a92ff2eb13df92a22e392c5405e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153133"
---
# <a name="system-error-codes-4000-5999"></a><span data-ttu-id="41c75-103">Códigos de error del sistema (4000-5999)</span><span class="sxs-lookup"><span data-stu-id="41c75-103">System Error Codes (4000-5999)</span></span>

> [!NOTE]
> <span data-ttu-id="41c75-104">Esta información está destinada a los desarrolladores que depuran errores del sistema.</span><span class="sxs-lookup"><span data-stu-id="41c75-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="41c75-105">En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="41c75-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="41c75-106">En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) para los errores 4000 a 5999.</span><span class="sxs-lookup"><span data-stu-id="41c75-106">The following list describes [system error codes](system-error-codes.md) for errors 4000 to 5999.</span></span> <span data-ttu-id="41c75-107">La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones.</span><span class="sxs-lookup"><span data-stu-id="41c75-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="41c75-108">Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.</span><span class="sxs-lookup"><span data-stu-id="41c75-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="41c75-109"><span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**ERROR \_ WINS \_ interno**</span><span class="sxs-lookup"><span data-stu-id="41c75-109"><span id="ERROR_WINS_INTERNAL"></span><span id="error_wins_internal"></span>**ERROR\_WINS\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-110">4000 (0xFA0)</span><span class="sxs-lookup"><span data-stu-id="41c75-110">4000 (0xFA0)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-111">WINS encontró un error al procesar el comando.</span><span class="sxs-lookup"><span data-stu-id="41c75-111">WINS encountered an error while processing the command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-112"><span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**no se puede eliminar el \_ \_ \_ \_ \_ servidor WINS local**</span><span class="sxs-lookup"><span data-stu-id="41c75-112"><span id="ERROR_CAN_NOT_DEL_LOCAL_WINS"></span><span id="error_can_not_del_local_wins"></span>**ERROR\_CAN\_NOT\_DEL\_LOCAL\_WINS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-113">4001 (0xFA1)</span><span class="sxs-lookup"><span data-stu-id="41c75-113">4001 (0xFA1)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-114">No se puede eliminar el WINS local.</span><span class="sxs-lookup"><span data-stu-id="41c75-114">The local WINS cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-115"><span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**ERROR \_ de \_ inicialización estática**</span><span class="sxs-lookup"><span data-stu-id="41c75-115"><span id="ERROR_STATIC_INIT"></span><span id="error_static_init"></span>**ERROR\_STATIC\_INIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-116">4002 (0xFA2)</span><span class="sxs-lookup"><span data-stu-id="41c75-116">4002 (0xFA2)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-117">Error en la importación del archivo.</span><span class="sxs-lookup"><span data-stu-id="41c75-117">The importation from the file failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-118"><span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**copia de seguridad de ERROR \_ Inc \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-118"><span id="ERROR_INC_BACKUP"></span><span id="error_inc_backup"></span>**ERROR\_INC\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-119">4003 (0xFA3)</span><span class="sxs-lookup"><span data-stu-id="41c75-119">4003 (0xFA3)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-120">Error en la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="41c75-120">The backup failed.</span></span> <span data-ttu-id="41c75-121">¿Se realizó una copia de seguridad completa antes?</span><span class="sxs-lookup"><span data-stu-id="41c75-121">Was a full backup done before?</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-122"><span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**ERROR \_ de \_ copia de seguridad completa**</span><span class="sxs-lookup"><span data-stu-id="41c75-122"><span id="ERROR_FULL_BACKUP"></span><span id="error_full_backup"></span>**ERROR\_FULL\_BACKUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-123">4004 (0xFA4)</span><span class="sxs-lookup"><span data-stu-id="41c75-123">4004 (0xFA4)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-124">Error en la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="41c75-124">The backup failed.</span></span> <span data-ttu-id="41c75-125">Compruebe el directorio en el que va a realizar la copia de seguridad de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="41c75-125">Check the directory to which you are backing the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-126"><span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**ERROR \_ rec \_ \_ inexistente**</span><span class="sxs-lookup"><span data-stu-id="41c75-126"><span id="ERROR_REC_NON_EXISTENT"></span><span id="error_rec_non_existent"></span>**ERROR\_REC\_NON\_EXISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-127">4005 (0xFA5)</span><span class="sxs-lookup"><span data-stu-id="41c75-127">4005 (0xFA5)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-128">El nombre no existe en la base de datos WINS.</span><span class="sxs-lookup"><span data-stu-id="41c75-128">The name does not exist in the WINS database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-129"><span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**\_no se \_ \_ permite RPL de error**</span><span class="sxs-lookup"><span data-stu-id="41c75-129"><span id="ERROR_RPL_NOT_ALLOWED"></span><span id="error_rpl_not_allowed"></span>**ERROR\_RPL\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-130">4006 (0xFA6)</span><span class="sxs-lookup"><span data-stu-id="41c75-130">4006 (0xFA6)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-131">No se permite la replicación con un asociado no configurado.</span><span class="sxs-lookup"><span data-stu-id="41c75-131">Replication with a nonconfigured partner is not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-132"><span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**\_versión CONTENTINFO de error de PEERDIST \_ \_ \_ no compatible**</span><span class="sxs-lookup"><span data-stu-id="41c75-132"><span id="PEERDIST_ERROR_CONTENTINFO_VERSION_UNSUPPORTED"></span><span id="peerdist_error_contentinfo_version_unsupported"></span>**PEERDIST\_ERROR\_CONTENTINFO\_VERSION\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-133">4050 (0xFD2)</span><span class="sxs-lookup"><span data-stu-id="41c75-133">4050 (0xFD2)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-134">No se admite la versión de la información de contenido proporcionada.</span><span class="sxs-lookup"><span data-stu-id="41c75-134">The version of the supplied content information is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-135"><span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**ERROR de PEERDIST \_ \_ no se puede \_ analizar \_ CONTENTINFO**</span><span class="sxs-lookup"><span data-stu-id="41c75-135"><span id="PEERDIST_ERROR_CANNOT_PARSE_CONTENTINFO"></span><span id="peerdist_error_cannot_parse_contentinfo"></span>**PEERDIST\_ERROR\_CANNOT\_PARSE\_CONTENTINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-136">4051 (0xFD3)</span><span class="sxs-lookup"><span data-stu-id="41c75-136">4051 (0xFD3)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-137">La información de contenido proporcionada tiene un formato incorrecto.</span><span class="sxs-lookup"><span data-stu-id="41c75-137">The supplied content information is malformed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-138"><span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**\_ \_ faltan datos en el error de PEERDIST \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-138"><span id="PEERDIST_ERROR_MISSING_DATA"></span><span id="peerdist_error_missing_data"></span>**PEERDIST\_ERROR\_MISSING\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-139">4052 (0xFD4)</span><span class="sxs-lookup"><span data-stu-id="41c75-139">4052 (0xFD4)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-140">Los datos solicitados no se encuentran en las cachés locales o del mismo nivel.</span><span class="sxs-lookup"><span data-stu-id="41c75-140">The requested data cannot be found in local or peer caches.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-141"><span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**ERROR de PEERDIST \_ : \_ no \_ más**</span><span class="sxs-lookup"><span data-stu-id="41c75-141"><span id="PEERDIST_ERROR_NO_MORE"></span><span id="peerdist_error_no_more"></span>**PEERDIST\_ERROR\_NO\_MORE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-142">4053 (0xFD5)</span><span class="sxs-lookup"><span data-stu-id="41c75-142">4053 (0xFD5)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-143">No hay más datos disponibles o necesarios.</span><span class="sxs-lookup"><span data-stu-id="41c75-143">No more data is available or required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-144"><span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**ERROR de PEERDIST \_ \_ no \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="41c75-144"><span id="PEERDIST_ERROR_NOT_INITIALIZED"></span><span id="peerdist_error_not_initialized"></span>**PEERDIST\_ERROR\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-145">4054 (0xFD6)</span><span class="sxs-lookup"><span data-stu-id="41c75-145">4054 (0xFD6)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-146">No se ha inicializado el objeto proporcionado.</span><span class="sxs-lookup"><span data-stu-id="41c75-146">The supplied object has not been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-147"><span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**ERROR de PEERDIST \_ \_ ya \_ inicializado**</span><span class="sxs-lookup"><span data-stu-id="41c75-147"><span id="PEERDIST_ERROR_ALREADY_INITIALIZED"></span><span id="peerdist_error_already_initialized"></span>**PEERDIST\_ERROR\_ALREADY\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-148">4055 (0xFD7)</span><span class="sxs-lookup"><span data-stu-id="41c75-148">4055 (0xFD7)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-149">El objeto proporcionado ya se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="41c75-149">The supplied object has already been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-150"><span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**\_error \_ de apagado \_ de PEERDIST en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="41c75-150"><span id="PEERDIST_ERROR_SHUTDOWN_IN_PROGRESS"></span><span id="peerdist_error_shutdown_in_progress"></span>**PEERDIST\_ERROR\_SHUTDOWN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-151">4056 (0xFD8)</span><span class="sxs-lookup"><span data-stu-id="41c75-151">4056 (0xFD8)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-152">Ya hay una operación de apagado en curso.</span><span class="sxs-lookup"><span data-stu-id="41c75-152">A shutdown operation is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-153"><span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**ERROR de PEERDIST \_ \_ invalidado**</span><span class="sxs-lookup"><span data-stu-id="41c75-153"><span id="PEERDIST_ERROR_INVALIDATED"></span><span id="peerdist_error_invalidated"></span>**PEERDIST\_ERROR\_INVALIDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-154">4057 (0xFD9)</span><span class="sxs-lookup"><span data-stu-id="41c75-154">4057 (0xFD9)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-155">El objeto proporcionado ya se ha invalidado.</span><span class="sxs-lookup"><span data-stu-id="41c75-155">The supplied object has already been invalidated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-156"><span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**el \_ error de PEERDIST \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="41c75-156"><span id="PEERDIST_ERROR_ALREADY_EXISTS"></span><span id="peerdist_error_already_exists"></span>**PEERDIST\_ERROR\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-157">4058 (0xFDA)</span><span class="sxs-lookup"><span data-stu-id="41c75-157">4058 (0xFDA)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-158">Ya existe un elemento y no se ha reemplazado.</span><span class="sxs-lookup"><span data-stu-id="41c75-158">An element already exists and was not replaced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-159"><span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**ERROR de la \_ \_ operación de \_ NOTFOUND de PEERDIST**</span><span class="sxs-lookup"><span data-stu-id="41c75-159"><span id="PEERDIST_ERROR_OPERATION_NOTFOUND"></span><span id="peerdist_error_operation_notfound"></span>**PEERDIST\_ERROR\_OPERATION\_NOTFOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-160">4059 (0xFDB)</span><span class="sxs-lookup"><span data-stu-id="41c75-160">4059 (0xFDB)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-161">No se puede cancelar la operación solicitada porque ya se ha completado.</span><span class="sxs-lookup"><span data-stu-id="41c75-161">Can not cancel the requested operation as it has already been completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-162"><span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**ERROR de PEERDIST \_ \_ ya \_ completado**</span><span class="sxs-lookup"><span data-stu-id="41c75-162"><span id="PEERDIST_ERROR_ALREADY_COMPLETED"></span><span id="peerdist_error_already_completed"></span>**PEERDIST\_ERROR\_ALREADY\_COMPLETED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-163">4060 (0xFDC)</span><span class="sxs-lookup"><span data-stu-id="41c75-163">4060 (0xFDC)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-164">No se puede realizar la operación solicita porque ya se ha realizado.</span><span class="sxs-lookup"><span data-stu-id="41c75-164">Can not perform the reqested operation because it has already been carried out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-165"><span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**\_error \_ de PEERDIST fuera de los \_ \_ límites**</span><span class="sxs-lookup"><span data-stu-id="41c75-165"><span id="PEERDIST_ERROR_OUT_OF_BOUNDS"></span><span id="peerdist_error_out_of_bounds"></span>**PEERDIST\_ERROR\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-166">4061 (0xFDD)</span><span class="sxs-lookup"><span data-stu-id="41c75-166">4061 (0xFDD)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-167">Una operación a datos más allá de los límites de datos válidos.</span><span class="sxs-lookup"><span data-stu-id="41c75-167">An operation accessed data beyond the bounds of valid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-168"><span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**versión de error de PEERDIST \_ \_ \_ no admitida**</span><span class="sxs-lookup"><span data-stu-id="41c75-168"><span id="PEERDIST_ERROR_VERSION_UNSUPPORTED"></span><span id="peerdist_error_version_unsupported"></span>**PEERDIST\_ERROR\_VERSION\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-169">4062 (0xFDE)</span><span class="sxs-lookup"><span data-stu-id="41c75-169">4062 (0xFDE)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-170">No se admite la versión solicitada.</span><span class="sxs-lookup"><span data-stu-id="41c75-170">The requested version is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-171"><span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**\_error de \_ configuración no válida \_ de PEERDIST**</span><span class="sxs-lookup"><span data-stu-id="41c75-171"><span id="PEERDIST_ERROR_INVALID_CONFIGURATION"></span><span id="peerdist_error_invalid_configuration"></span>**PEERDIST\_ERROR\_INVALID\_CONFIGURATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-172">4063 (0xFDF)</span><span class="sxs-lookup"><span data-stu-id="41c75-172">4063 (0xFDF)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-173">Un valor de configuración no es válido.</span><span class="sxs-lookup"><span data-stu-id="41c75-173">A configuration value is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-174"><span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**ERROR de PEERDIST \_ \_ sin \_ licencia**</span><span class="sxs-lookup"><span data-stu-id="41c75-174"><span id="PEERDIST_ERROR_NOT_LICENSED"></span><span id="peerdist_error_not_licensed"></span>**PEERDIST\_ERROR\_NOT\_LICENSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-175">4064 (0xFE0)</span><span class="sxs-lookup"><span data-stu-id="41c75-175">4064 (0xFE0)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-176">La SKU no tiene licencia.</span><span class="sxs-lookup"><span data-stu-id="41c75-176">The SKU is not licensed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-177"><span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**servicio de errores de PEERDIST \_ \_ \_ no disponible**</span><span class="sxs-lookup"><span data-stu-id="41c75-177"><span id="PEERDIST_ERROR_SERVICE_UNAVAILABLE"></span><span id="peerdist_error_service_unavailable"></span>**PEERDIST\_ERROR\_SERVICE\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-178">4065 (0xFE1)</span><span class="sxs-lookup"><span data-stu-id="41c75-178">4065 (0xFE1)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-179">El servicio de PeerDist todavía se está inicializando y estará disponible en breve.</span><span class="sxs-lookup"><span data-stu-id="41c75-179">PeerDist Service is still initializing and will be available shortly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-180"><span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**error de \_ confianza de error de PEERDIST \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-180"><span id="PEERDIST_ERROR_TRUST_FAILURE"></span><span id="peerdist_error_trust_failure"></span>**PEERDIST\_ERROR\_TRUST\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-181">4066 (0xFE2)</span><span class="sxs-lookup"><span data-stu-id="41c75-181">4066 (0xFE2)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-182">La comunicación con uno o más equipos se bloqueará temporalmente debido a errores recientes.</span><span class="sxs-lookup"><span data-stu-id="41c75-182">Communication with one or more computers will be temporarily blocked due to recent errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-183"><span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**ERROR \_ de \_ conflicto de direcciones DHCP \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-183"><span id="ERROR_DHCP_ADDRESS_CONFLICT"></span><span id="error_dhcp_address_conflict"></span>**ERROR\_DHCP\_ADDRESS\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-184">4100 (0x1004)</span><span class="sxs-lookup"><span data-stu-id="41c75-184">4100 (0x1004)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-185">El cliente DHCP ha obtenido una dirección IP que ya está en uso en la red.</span><span class="sxs-lookup"><span data-stu-id="41c75-185">The DHCP client has obtained an IP address that is already in use on the network.</span></span> <span data-ttu-id="41c75-186">La interfaz local se deshabilitará hasta que el cliente DHCP pueda obtener una nueva dirección.</span><span class="sxs-lookup"><span data-stu-id="41c75-186">The local interface will be disabled until the DHCP client can obtain a new address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-187"><span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**\_ \_ \_ no \_ se encontró el GUID de WMI de error**</span><span class="sxs-lookup"><span data-stu-id="41c75-187"><span id="ERROR_WMI_GUID_NOT_FOUND"></span><span id="error_wmi_guid_not_found"></span>**ERROR\_WMI\_GUID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-188">4200 (0x1068)</span><span class="sxs-lookup"><span data-stu-id="41c75-188">4200 (0x1068)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-189">Un proveedor de datos WMI no reconoció como válido el GUID que se ha pasado.</span><span class="sxs-lookup"><span data-stu-id="41c75-189">The GUID passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-190"><span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**ERROR \_ de \_ instancia de WMI \_ no \_ encontrada**</span><span class="sxs-lookup"><span data-stu-id="41c75-190"><span id="ERROR_WMI_INSTANCE_NOT_FOUND"></span><span id="error_wmi_instance_not_found"></span>**ERROR\_WMI\_INSTANCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-191">4201 (0x1069)</span><span class="sxs-lookup"><span data-stu-id="41c75-191">4201 (0x1069)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-192">El nombre de instancia pasado no se reconoció como válido por un proveedor de datos WMI.</span><span class="sxs-lookup"><span data-stu-id="41c75-192">The instance name passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-193"><span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ERROR \_ WMI \_ ITEMID \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="41c75-193"><span id="ERROR_WMI_ITEMID_NOT_FOUND"></span><span id="error_wmi_itemid_not_found"></span>**ERROR\_WMI\_ITEMID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-194">4202 (0x106A)</span><span class="sxs-lookup"><span data-stu-id="41c75-194">4202 (0x106A)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-195">Un proveedor de datos WMI no reconoció como válido el ID. de elemento de datos pasado.</span><span class="sxs-lookup"><span data-stu-id="41c75-195">The data item ID passed was not recognized as valid by a WMI data provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-196"><span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**ERROR de \_ WMI \_ inténtelo de \_ nuevo**</span><span class="sxs-lookup"><span data-stu-id="41c75-196"><span id="ERROR_WMI_TRY_AGAIN"></span><span id="error_wmi_try_again"></span>**ERROR\_WMI\_TRY\_AGAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-197">4203 (0x106B)</span><span class="sxs-lookup"><span data-stu-id="41c75-197">4203 (0x106B)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-198">No se pudo completar la solicitud WMI y se debe reintentar.</span><span class="sxs-lookup"><span data-stu-id="41c75-198">The WMI request could not be completed and should be retried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-199"><span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**ERROR de \_ WMI \_ DP \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="41c75-199"><span id="ERROR_WMI_DP_NOT_FOUND"></span><span id="error_wmi_dp_not_found"></span>**ERROR\_WMI\_DP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-200">4204 (0x106C)</span><span class="sxs-lookup"><span data-stu-id="41c75-200">4204 (0x106C)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-201">No se pudo encontrar el proveedor de datos WMI.</span><span class="sxs-lookup"><span data-stu-id="41c75-201">The WMI data provider could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-202"><span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**ERROR \_ de \_ referencia de instancia sin resolver de WMI \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-202"><span id="ERROR_WMI_UNRESOLVED_INSTANCE_REF"></span><span id="error_wmi_unresolved_instance_ref"></span>**ERROR\_WMI\_UNRESOLVED\_INSTANCE\_REF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-203">4205 (0x106D)</span><span class="sxs-lookup"><span data-stu-id="41c75-203">4205 (0x106D)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-204">El proveedor de datos WMI hace referencia a un conjunto de instancias que no se ha registrado.</span><span class="sxs-lookup"><span data-stu-id="41c75-204">The WMI data provider references an instance set that has not been registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-205"><span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**ERROR \_ WMI \_ ya \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="41c75-205"><span id="ERROR_WMI_ALREADY_ENABLED"></span><span id="error_wmi_already_enabled"></span>**ERROR\_WMI\_ALREADY\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-206">4206 (0x106E)</span><span class="sxs-lookup"><span data-stu-id="41c75-206">4206 (0x106E)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-207">Ya se ha habilitado el bloque de datos WMI o la notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="41c75-207">The WMI data block or event notification has already been enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-208"><span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**ERROR \_ de \_ GUID de WMI \_ desconectado**</span><span class="sxs-lookup"><span data-stu-id="41c75-208"><span id="ERROR_WMI_GUID_DISCONNECTED"></span><span id="error_wmi_guid_disconnected"></span>**ERROR\_WMI\_GUID\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-209">4207 (0x106F)</span><span class="sxs-lookup"><span data-stu-id="41c75-209">4207 (0x106F)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-210">El bloque de datos WMI ya no está disponible.</span><span class="sxs-lookup"><span data-stu-id="41c75-210">The WMI data block is no longer available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-211"><span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**ERROR \_ de \_ servidor WMI \_ no disponible**</span><span class="sxs-lookup"><span data-stu-id="41c75-211"><span id="ERROR_WMI_SERVER_UNAVAILABLE"></span><span id="error_wmi_server_unavailable"></span>**ERROR\_WMI\_SERVER\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-212">4208 (0x1070)</span><span class="sxs-lookup"><span data-stu-id="41c75-212">4208 (0x1070)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-213">El servicio de datos WMI no está disponible.</span><span class="sxs-lookup"><span data-stu-id="41c75-213">The WMI data service is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-214"><span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**ERROR de \_ WMI \_ DP \_ erróneo**</span><span class="sxs-lookup"><span data-stu-id="41c75-214"><span id="ERROR_WMI_DP_FAILED"></span><span id="error_wmi_dp_failed"></span>**ERROR\_WMI\_DP\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-215">4209 (0x1071)</span><span class="sxs-lookup"><span data-stu-id="41c75-215">4209 (0x1071)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-216">El proveedor de datos WMI no pudo llevar a cabo la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41c75-216">The WMI data provider failed to carry out the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-217"><span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**ERROR \_ \_ MOF no válido de WMI \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-217"><span id="ERROR_WMI_INVALID_MOF"></span><span id="error_wmi_invalid_mof"></span>**ERROR\_WMI\_INVALID\_MOF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-218">4210 (0x1072)</span><span class="sxs-lookup"><span data-stu-id="41c75-218">4210 (0x1072)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-219">La información MOF de WMI no es válida.</span><span class="sxs-lookup"><span data-stu-id="41c75-219">The WMI MOF information is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-220"><span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**ERROR de \_ WMI \_ no válido \_ REGINFO**</span><span class="sxs-lookup"><span data-stu-id="41c75-220"><span id="ERROR_WMI_INVALID_REGINFO"></span><span id="error_wmi_invalid_reginfo"></span>**ERROR\_WMI\_INVALID\_REGINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-221">4211 (0x1073)</span><span class="sxs-lookup"><span data-stu-id="41c75-221">4211 (0x1073)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-222">La información de registro de WMI no es válida.</span><span class="sxs-lookup"><span data-stu-id="41c75-222">The WMI registration information is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-223"><span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**ERROR \_ WMI \_ ya \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="41c75-223"><span id="ERROR_WMI_ALREADY_DISABLED"></span><span id="error_wmi_already_disabled"></span>**ERROR\_WMI\_ALREADY\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-224">4212 (0x1074)</span><span class="sxs-lookup"><span data-stu-id="41c75-224">4212 (0x1074)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-225">Ya se ha deshabilitado el bloque de datos WMI o la notificación de eventos.</span><span class="sxs-lookup"><span data-stu-id="41c75-225">The WMI data block or event notification has already been disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-226"><span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**ERROR \_ de \_ solo lectura de WMI \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-226"><span id="ERROR_WMI_READ_ONLY"></span><span id="error_wmi_read_only"></span>**ERROR\_WMI\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-227">4213 (0x1075)</span><span class="sxs-lookup"><span data-stu-id="41c75-227">4213 (0x1075)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-228">El elemento de datos WMI o el bloque de datos es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="41c75-228">The WMI data item or data block is read only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-229"><span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**ERROR \_ de \_ conjunto de WMI \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-229"><span id="ERROR_WMI_SET_FAILURE"></span><span id="error_wmi_set_failure"></span>**ERROR\_WMI\_SET\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-230">4214 (0x1076)</span><span class="sxs-lookup"><span data-stu-id="41c75-230">4214 (0x1076)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-231">No se pudo cambiar el elemento de datos WMI o el bloque de datos.</span><span class="sxs-lookup"><span data-stu-id="41c75-231">The WMI data item or data block could not be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-232"><span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**ERROR \_ no \_ APPCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="41c75-232"><span id="ERROR_NOT_APPCONTAINER"></span><span id="error_not_appcontainer"></span>**ERROR\_NOT\_APPCONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-233">4250 (0x109A)</span><span class="sxs-lookup"><span data-stu-id="41c75-233">4250 (0x109A)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-234">Esta operación solo es válida en el contexto de un contenedor de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="41c75-234">This operation is only valid in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-235"><span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**ERROR de \_ APPCONTAINER \_ requerido**</span><span class="sxs-lookup"><span data-stu-id="41c75-235"><span id="ERROR_APPCONTAINER_REQUIRED"></span><span id="error_appcontainer_required"></span>**ERROR\_APPCONTAINER\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-236">4251 (0x109B)</span><span class="sxs-lookup"><span data-stu-id="41c75-236">4251 (0x109B)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-237">Esta aplicación solo se puede ejecutar en el contexto de un contenedor de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="41c75-237">This application can only run in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-238"><span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**ERROR \_ no \_ compatible \_ con \_ APPCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="41c75-238"><span id="ERROR_NOT_SUPPORTED_IN_APPCONTAINER"></span><span id="error_not_supported_in_appcontainer"></span>**ERROR\_NOT\_SUPPORTED\_IN\_APPCONTAINER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-239">4252 (0x109C)</span><span class="sxs-lookup"><span data-stu-id="41c75-239">4252 (0x109C)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-240">Esta funcionalidad no se admite en el contexto de un contenedor de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="41c75-240">This functionality is not supported in the context of an app container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-241"><span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**ERROR \_ de \_ \_ longitud de SID de paquete no válida \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-241"><span id="ERROR_INVALID_PACKAGE_SID_LENGTH"></span><span id="error_invalid_package_sid_length"></span>**ERROR\_INVALID\_PACKAGE\_SID\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-242">4253 (0x109D)</span><span class="sxs-lookup"><span data-stu-id="41c75-242">4253 (0x109D)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-243">La longitud del SID proporcionado no es una longitud válida para los SID de contenedor de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="41c75-243">The length of the SID supplied is not a valid length for app container SIDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-244"><span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**ERROR \_ de \_ medio no válido**</span><span class="sxs-lookup"><span data-stu-id="41c75-244"><span id="ERROR_INVALID_MEDIA"></span><span id="error_invalid_media"></span>**ERROR\_INVALID\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-245">4300 (0x10CC)</span><span class="sxs-lookup"><span data-stu-id="41c75-245">4300 (0x10CC)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-246">El identificador de medios no representa un medio válido.</span><span class="sxs-lookup"><span data-stu-id="41c75-246">The media identifier does not represent a valid medium.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-247"><span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**ERROR \_ de \_ biblioteca no válida**</span><span class="sxs-lookup"><span data-stu-id="41c75-247"><span id="ERROR_INVALID_LIBRARY"></span><span id="error_invalid_library"></span>**ERROR\_INVALID\_LIBRARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-248">4301 (0x10CD)</span><span class="sxs-lookup"><span data-stu-id="41c75-248">4301 (0x10CD)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-249">El identificador de biblioteca no representa una biblioteca válida.</span><span class="sxs-lookup"><span data-stu-id="41c75-249">The library identifier does not represent a valid library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-250"><span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**ERROR \_ de \_ grupo de medios no válido \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-250"><span id="ERROR_INVALID_MEDIA_POOL"></span><span id="error_invalid_media_pool"></span>**ERROR\_INVALID\_MEDIA\_POOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-251">4302 (0x10CE)</span><span class="sxs-lookup"><span data-stu-id="41c75-251">4302 (0x10CE)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-252">El identificador del grupo de medios no representa un grupo de medios válido.</span><span class="sxs-lookup"><span data-stu-id="41c75-252">The media pool identifier does not represent a valid media pool.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-253"><span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**ERROR \_ de \_ coincidencia de medios de unidad \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-253"><span id="ERROR_DRIVE_MEDIA_MISMATCH"></span><span id="error_drive_media_mismatch"></span>**ERROR\_DRIVE\_MEDIA\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-254">4303 (0x10CF)</span><span class="sxs-lookup"><span data-stu-id="41c75-254">4303 (0x10CF)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-255">La unidad y el medio no son compatibles o existen en bibliotecas diferentes.</span><span class="sxs-lookup"><span data-stu-id="41c75-255">The drive and medium are not compatible or exist in different libraries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-256"><span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**medios de ERROR \_ \_ sin conexión**</span><span class="sxs-lookup"><span data-stu-id="41c75-256"><span id="ERROR_MEDIA_OFFLINE"></span><span id="error_media_offline"></span>**ERROR\_MEDIA\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-257">4304 (0x10D0)</span><span class="sxs-lookup"><span data-stu-id="41c75-257">4304 (0x10D0)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-258">El medio existe actualmente en una biblioteca sin conexión y debe estar en línea para realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="41c75-258">The medium currently exists in an offline library and must be online to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-259"><span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**Biblioteca de errores \_ \_ sin conexión**</span><span class="sxs-lookup"><span data-stu-id="41c75-259"><span id="ERROR_LIBRARY_OFFLINE"></span><span id="error_library_offline"></span>**ERROR\_LIBRARY\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-260">4305 (0x10D1)</span><span class="sxs-lookup"><span data-stu-id="41c75-260">4305 (0x10D1)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-261">La operación no se puede realizar en una biblioteca sin conexión.</span><span class="sxs-lookup"><span data-stu-id="41c75-261">The operation cannot be performed on an offline library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-262"><span id="ERROR_EMPTY"></span><span id="error_empty"></span>**ERROR \_ vacío**</span><span class="sxs-lookup"><span data-stu-id="41c75-262"><span id="ERROR_EMPTY"></span><span id="error_empty"></span>**ERROR\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-263">4306 (0x10D2)</span><span class="sxs-lookup"><span data-stu-id="41c75-263">4306 (0x10D2)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-264">La biblioteca, la unidad o el grupo de medios están vacíos.</span><span class="sxs-lookup"><span data-stu-id="41c75-264">The library, drive, or media pool is empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-265"><span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**ERROR \_ no \_ vacío**</span><span class="sxs-lookup"><span data-stu-id="41c75-265"><span id="ERROR_NOT_EMPTY"></span><span id="error_not_empty"></span>**ERROR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-266">4307 (0x10D3)</span><span class="sxs-lookup"><span data-stu-id="41c75-266">4307 (0x10D3)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-267">La biblioteca, la unidad o el grupo de medios deben estar vacíos para realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="41c75-267">The library, drive, or media pool must be empty to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-268"><span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**medio de ERROR \_ \_ no disponible**</span><span class="sxs-lookup"><span data-stu-id="41c75-268"><span id="ERROR_MEDIA_UNAVAILABLE"></span><span id="error_media_unavailable"></span>**ERROR\_MEDIA\_UNAVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-269">4308 (0x10D4)</span><span class="sxs-lookup"><span data-stu-id="41c75-269">4308 (0x10D4)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-270">Actualmente no hay ningún medio disponible en este grupo de medios o biblioteca.</span><span class="sxs-lookup"><span data-stu-id="41c75-270">No media is currently available in this media pool or library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-271"><span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**recurso de ERROR \_ \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="41c75-271"><span id="ERROR_RESOURCE_DISABLED"></span><span id="error_resource_disabled"></span>**ERROR\_RESOURCE\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-272">4309 (0x10D5)</span><span class="sxs-lookup"><span data-stu-id="41c75-272">4309 (0x10D5)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-273">Un recurso necesario para esta operación está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="41c75-273">A resource required for this operation is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-274"><span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**ERROR \_ de \_ limpiador no válido**</span><span class="sxs-lookup"><span data-stu-id="41c75-274"><span id="ERROR_INVALID_CLEANER"></span><span id="error_invalid_cleaner"></span>**ERROR\_INVALID\_CLEANER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-275">4310 (0x10D6)</span><span class="sxs-lookup"><span data-stu-id="41c75-275">4310 (0x10D6)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-276">El identificador de medios no representa un limpiador válido.</span><span class="sxs-lookup"><span data-stu-id="41c75-276">The media identifier does not represent a valid cleaner.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-277"><span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**ERROR \_ \_ al \_ limpiar**</span><span class="sxs-lookup"><span data-stu-id="41c75-277"><span id="ERROR_UNABLE_TO_CLEAN"></span><span id="error_unable_to_clean"></span>**ERROR\_UNABLE\_TO\_CLEAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-278">4311 (0x10D7)</span><span class="sxs-lookup"><span data-stu-id="41c75-278">4311 (0x10D7)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-279">No se puede limpiar la unidad o no admite la limpieza.</span><span class="sxs-lookup"><span data-stu-id="41c75-279">The drive cannot be cleaned or does not support cleaning.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-280"><span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**\_ \_ no \_ se encontró el objeto de error**</span><span class="sxs-lookup"><span data-stu-id="41c75-280"><span id="ERROR_OBJECT_NOT_FOUND"></span><span id="error_object_not_found"></span>**ERROR\_OBJECT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-281">4312 (0x10D8)</span><span class="sxs-lookup"><span data-stu-id="41c75-281">4312 (0x10D8)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-282">El identificador de objeto no representa un objeto válido.</span><span class="sxs-lookup"><span data-stu-id="41c75-282">The object identifier does not represent a valid object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-283"><span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**ERROR de base de datos de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-283"><span id="ERROR_DATABASE_FAILURE"></span><span id="error_database_failure"></span>**ERROR\_DATABASE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-284">4313 (0x10D9)</span><span class="sxs-lookup"><span data-stu-id="41c75-284">4313 (0x10D9)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-285">No se puede leer o escribir en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="41c75-285">Unable to read from or write to the database.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-286"><span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**base de datos de ERROR \_ \_ completa**</span><span class="sxs-lookup"><span data-stu-id="41c75-286"><span id="ERROR_DATABASE_FULL"></span><span id="error_database_full"></span>**ERROR\_DATABASE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-287">4314 (0x10DA)</span><span class="sxs-lookup"><span data-stu-id="41c75-287">4314 (0x10DA)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-288">La base de datos está llena.</span><span class="sxs-lookup"><span data-stu-id="41c75-288">The database is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-289"><span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**medio de ERROR no \_ \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="41c75-289"><span id="ERROR_MEDIA_INCOMPATIBLE"></span><span id="error_media_incompatible"></span>**ERROR\_MEDIA\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-290">4315 (0x10DB)</span><span class="sxs-lookup"><span data-stu-id="41c75-290">4315 (0x10DB)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-291">El medio no es compatible con el dispositivo o el grupo de medios.</span><span class="sxs-lookup"><span data-stu-id="41c75-291">The medium is not compatible with the device or media pool.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-292"><span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**el \_ recurso de error \_ no \_ está presente**</span><span class="sxs-lookup"><span data-stu-id="41c75-292"><span id="ERROR_RESOURCE_NOT_PRESENT"></span><span id="error_resource_not_present"></span>**ERROR\_RESOURCE\_NOT\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-293">4316 (0x10DC)</span><span class="sxs-lookup"><span data-stu-id="41c75-293">4316 (0x10DC)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-294">El recurso necesario para esta operación no existe.</span><span class="sxs-lookup"><span data-stu-id="41c75-294">The resource required for this operation does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-295"><span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**ERROR \_ de \_ operación no válida**</span><span class="sxs-lookup"><span data-stu-id="41c75-295"><span id="ERROR_INVALID_OPERATION"></span><span id="error_invalid_operation"></span>**ERROR\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-296">4317 (0x10DD)</span><span class="sxs-lookup"><span data-stu-id="41c75-296">4317 (0x10DD)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-297">El identificador de la operación no es válido.</span><span class="sxs-lookup"><span data-stu-id="41c75-297">The operation identifier is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-298"><span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**los \_ medios de error \_ no \_ están disponibles**</span><span class="sxs-lookup"><span data-stu-id="41c75-298"><span id="ERROR_MEDIA_NOT_AVAILABLE"></span><span id="error_media_not_available"></span>**ERROR\_MEDIA\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-299">4318 (0x10DE)</span><span class="sxs-lookup"><span data-stu-id="41c75-299">4318 (0x10DE)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-300">El medio no está montado o listo para su uso.</span><span class="sxs-lookup"><span data-stu-id="41c75-300">The media is not mounted or ready for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-301"><span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**el \_ dispositivo de error \_ no \_ está disponible**</span><span class="sxs-lookup"><span data-stu-id="41c75-301"><span id="ERROR_DEVICE_NOT_AVAILABLE"></span><span id="error_device_not_available"></span>**ERROR\_DEVICE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-302">4319 (0x10DF)</span><span class="sxs-lookup"><span data-stu-id="41c75-302">4319 (0x10DF)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-303">El dispositivo no está listo para su uso.</span><span class="sxs-lookup"><span data-stu-id="41c75-303">The device is not ready for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-304"><span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**solicitud de ERROR \_ \_ rechazada**</span><span class="sxs-lookup"><span data-stu-id="41c75-304"><span id="ERROR_REQUEST_REFUSED"></span><span id="error_request_refused"></span>**ERROR\_REQUEST\_REFUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-305">4320 (0x10E0)</span><span class="sxs-lookup"><span data-stu-id="41c75-305">4320 (0x10E0)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-306">El operador o administrador ha rechazado la solicitud.</span><span class="sxs-lookup"><span data-stu-id="41c75-306">The operator or administrator has refused the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-307"><span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**ERROR \_ de \_ objeto de unidad no válida \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-307"><span id="ERROR_INVALID_DRIVE_OBJECT"></span><span id="error_invalid_drive_object"></span>**ERROR\_INVALID\_DRIVE\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-308">4321 (0x10E1)</span><span class="sxs-lookup"><span data-stu-id="41c75-308">4321 (0x10E1)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-309">El identificador de unidad no representa una unidad válida.</span><span class="sxs-lookup"><span data-stu-id="41c75-309">The drive identifier does not represent a valid drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-310"><span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**Biblioteca de errores \_ \_ completa**</span><span class="sxs-lookup"><span data-stu-id="41c75-310"><span id="ERROR_LIBRARY_FULL"></span><span id="error_library_full"></span>**ERROR\_LIBRARY\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-311">4322 (0x10E2)</span><span class="sxs-lookup"><span data-stu-id="41c75-311">4322 (0x10E2)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-312">La biblioteca está llena.</span><span class="sxs-lookup"><span data-stu-id="41c75-312">Library is full.</span></span> <span data-ttu-id="41c75-313">No hay ninguna ranura disponible para su uso.</span><span class="sxs-lookup"><span data-stu-id="41c75-313">No slot is available for use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-314"><span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**ERROR \_ medio \_ no \_ accesible**</span><span class="sxs-lookup"><span data-stu-id="41c75-314"><span id="ERROR_MEDIUM_NOT_ACCESSIBLE"></span><span id="error_medium_not_accessible"></span>**ERROR\_MEDIUM\_NOT\_ACCESSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-315">4323 (0x10E3)</span><span class="sxs-lookup"><span data-stu-id="41c75-315">4323 (0x10E3)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-316">El transporte no puede obtener acceso al medio.</span><span class="sxs-lookup"><span data-stu-id="41c75-316">The transport cannot access the medium.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-317"><span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**ERROR: \_ no se puede \_ cargar el \_ \_ medio**</span><span class="sxs-lookup"><span data-stu-id="41c75-317"><span id="ERROR_UNABLE_TO_LOAD_MEDIUM"></span><span id="error_unable_to_load_medium"></span>**ERROR\_UNABLE\_TO\_LOAD\_MEDIUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-318">4324 (0x10E4)</span><span class="sxs-lookup"><span data-stu-id="41c75-318">4324 (0x10E4)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-319">No se puede cargar el medio en la unidad.</span><span class="sxs-lookup"><span data-stu-id="41c75-319">Unable to load the medium into the drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-320"><span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**ERROR \_ \_ al \_ inventariar la \_ unidad**</span><span class="sxs-lookup"><span data-stu-id="41c75-320"><span id="ERROR_UNABLE_TO_INVENTORY_DRIVE"></span><span id="error_unable_to_inventory_drive"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_DRIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-321">4325 (0x10E5)</span><span class="sxs-lookup"><span data-stu-id="41c75-321">4325 (0x10E5)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-322">No se puede recuperar el estado de la unidad.</span><span class="sxs-lookup"><span data-stu-id="41c75-322">Unable to retrieve the drive status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-323"><span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**ERROR \_ al no se puede \_ \_ inventariar la \_ ranura**</span><span class="sxs-lookup"><span data-stu-id="41c75-323"><span id="ERROR_UNABLE_TO_INVENTORY_SLOT"></span><span id="error_unable_to_inventory_slot"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_SLOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-324">4326 (0x10E6)</span><span class="sxs-lookup"><span data-stu-id="41c75-324">4326 (0x10E6)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-325">No se puede recuperar el estado de la ranura.</span><span class="sxs-lookup"><span data-stu-id="41c75-325">Unable to retrieve the slot status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-326"><span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**ERROR \_ \_ al \_ transportar el inventario \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-326"><span id="ERROR_UNABLE_TO_INVENTORY_TRANSPORT"></span><span id="error_unable_to_inventory_transport"></span>**ERROR\_UNABLE\_TO\_INVENTORY\_TRANSPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-327">4327 (0x10E7)</span><span class="sxs-lookup"><span data-stu-id="41c75-327">4327 (0x10E7)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-328">No se puede recuperar el estado del transporte.</span><span class="sxs-lookup"><span data-stu-id="41c75-328">Unable to retrieve status about the transport.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-329"><span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**ERROR de \_ transporte \_ completo**</span><span class="sxs-lookup"><span data-stu-id="41c75-329"><span id="ERROR_TRANSPORT_FULL"></span><span id="error_transport_full"></span>**ERROR\_TRANSPORT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-330">4328 (0x10E8)</span><span class="sxs-lookup"><span data-stu-id="41c75-330">4328 (0x10E8)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-331">No se puede usar el transporte porque ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="41c75-331">Cannot use the transport because it is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-332"><span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**ERROR al \_ controlar \_ IEPORT**</span><span class="sxs-lookup"><span data-stu-id="41c75-332"><span id="ERROR_CONTROLLING_IEPORT"></span><span id="error_controlling_ieport"></span>**ERROR\_CONTROLLING\_IEPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-333">4329 (0x10E9)</span><span class="sxs-lookup"><span data-stu-id="41c75-333">4329 (0x10E9)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-334">No se puede abrir o cerrar el puerto de inserción y expulsión.</span><span class="sxs-lookup"><span data-stu-id="41c75-334">Unable to open or close the inject/eject port.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-335"><span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**ERROR \_ \_ al \_ extraer el \_ \_ medio montado**</span><span class="sxs-lookup"><span data-stu-id="41c75-335"><span id="ERROR_UNABLE_TO_EJECT_MOUNTED_MEDIA"></span><span id="error_unable_to_eject_mounted_media"></span>**ERROR\_UNABLE\_TO\_EJECT\_MOUNTED\_MEDIA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-336">4330 (0x10EA)</span><span class="sxs-lookup"><span data-stu-id="41c75-336">4330 (0x10EA)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-337">No se puede expulsar el medio porque está en una unidad.</span><span class="sxs-lookup"><span data-stu-id="41c75-337">Unable to eject the medium because it is in a drive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-338"><span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**\_conjunto de \_ ranuras del limpiador de errores \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-338"><span id="ERROR_CLEANER_SLOT_SET"></span><span id="error_cleaner_slot_set"></span>**ERROR\_CLEANER\_SLOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-339">4331 (0x10EB)</span><span class="sxs-lookup"><span data-stu-id="41c75-339">4331 (0x10EB)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-340">Una ranura de limpiador ya está reservada.</span><span class="sxs-lookup"><span data-stu-id="41c75-340">A cleaner slot is already reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-341"><span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**ranura de limpiador de errores \_ \_ \_ no \_ establecida**</span><span class="sxs-lookup"><span data-stu-id="41c75-341"><span id="ERROR_CLEANER_SLOT_NOT_SET"></span><span id="error_cleaner_slot_not_set"></span>**ERROR\_CLEANER\_SLOT\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-342">4332 (0x10EC)</span><span class="sxs-lookup"><span data-stu-id="41c75-342">4332 (0x10EC)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-343">Una ranura de limpiador no está reservada.</span><span class="sxs-lookup"><span data-stu-id="41c75-343">A cleaner slot is not reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-344"><span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**cartucho de limpiador de errores \_ \_ \_ invertido**</span><span class="sxs-lookup"><span data-stu-id="41c75-344"><span id="ERROR_CLEANER_CARTRIDGE_SPENT"></span><span id="error_cleaner_cartridge_spent"></span>**ERROR\_CLEANER\_CARTRIDGE\_SPENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-345">4333 (0x10ED)</span><span class="sxs-lookup"><span data-stu-id="41c75-345">4333 (0x10ED)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-346">El cartucho de limpieza ha realizado el número máximo de limpiezas de la unidad.</span><span class="sxs-lookup"><span data-stu-id="41c75-346">The cleaner cartridge has performed the maximum number of drive cleanings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-347"><span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**ERROR de \_ Omid inesperado \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-347"><span id="ERROR_UNEXPECTED_OMID"></span><span id="error_unexpected_omid"></span>**ERROR\_UNEXPECTED\_OMID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-348">4334 (0x10EE)</span><span class="sxs-lookup"><span data-stu-id="41c75-348">4334 (0x10EE)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-349">Identificador en el medio inesperado.</span><span class="sxs-lookup"><span data-stu-id="41c75-349">Unexpected on-medium identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-350"><span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**ERROR no se pudo \_ \_ eliminar el \_ último \_ elemento**</span><span class="sxs-lookup"><span data-stu-id="41c75-350"><span id="ERROR_CANT_DELETE_LAST_ITEM"></span><span id="error_cant_delete_last_item"></span>**ERROR\_CANT\_DELETE\_LAST\_ITEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-351">4335 (0x10EF)</span><span class="sxs-lookup"><span data-stu-id="41c75-351">4335 (0x10EF)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-352">No se puede eliminar el último elemento restante de este grupo o recurso.</span><span class="sxs-lookup"><span data-stu-id="41c75-352">The last remaining item in this group or resource cannot be deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-353"><span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**\_el mensaje de error \_ supera \_ \_ el tamaño máximo**</span><span class="sxs-lookup"><span data-stu-id="41c75-353"><span id="ERROR_MESSAGE_EXCEEDS_MAX_SIZE"></span><span id="error_message_exceeds_max_size"></span>**ERROR\_MESSAGE\_EXCEEDS\_MAX\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-354">4336 (0x10F0)</span><span class="sxs-lookup"><span data-stu-id="41c75-354">4336 (0x10F0)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-355">El mensaje proporcionado supera el tamaño máximo permitido para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="41c75-355">The message provided exceeds the maximum size allowed for this parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-356"><span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**el \_ volumen de error \_ contiene \_ \_ archivos sys**</span><span class="sxs-lookup"><span data-stu-id="41c75-356"><span id="ERROR_VOLUME_CONTAINS_SYS_FILES"></span><span id="error_volume_contains_sys_files"></span>**ERROR\_VOLUME\_CONTAINS\_SYS\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-357">4337 (0x10F1)</span><span class="sxs-lookup"><span data-stu-id="41c75-357">4337 (0x10F1)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-358">El volumen contiene archivos de paginación o del sistema.</span><span class="sxs-lookup"><span data-stu-id="41c75-358">The volume contains system or paging files.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-359"><span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**\_tipo autóctono de error \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-359"><span id="ERROR_INDIGENOUS_TYPE"></span><span id="error_indigenous_type"></span>**ERROR\_INDIGENOUS\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-360">4338 (0x10F2)</span><span class="sxs-lookup"><span data-stu-id="41c75-360">4338 (0x10F2)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-361">No se puede quitar el tipo de medio de esta biblioteca porque al menos una unidad de la biblioteca informa de que puede admitir este tipo de medio.</span><span class="sxs-lookup"><span data-stu-id="41c75-361">The media type cannot be removed from this library since at least one drive in the library reports it can support this media type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-362"><span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**ERROR: \_ no se \_ admiten \_ unidades**</span><span class="sxs-lookup"><span data-stu-id="41c75-362"><span id="ERROR_NO_SUPPORTING_DRIVES"></span><span id="error_no_supporting_drives"></span>**ERROR\_NO\_SUPPORTING\_DRIVES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-363">4339 (0x10F3)</span><span class="sxs-lookup"><span data-stu-id="41c75-363">4339 (0x10F3)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-364">Este medio sin conexión no se puede montar en este sistema porque no hay ninguna unidad habilitada presente que se pueda usar.</span><span class="sxs-lookup"><span data-stu-id="41c75-364">This offline media cannot be mounted on this system since no enabled drives are present which can be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-365"><span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**cartucho de limpiador de errores \_ \_ \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="41c75-365"><span id="ERROR_CLEANER_CARTRIDGE_INSTALLED"></span><span id="error_cleaner_cartridge_installed"></span>**ERROR\_CLEANER\_CARTRIDGE\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-366">4340 (0x10F4)</span><span class="sxs-lookup"><span data-stu-id="41c75-366">4340 (0x10F4)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-367">Hay un cartucho de limpieza en la biblioteca de cintas.</span><span class="sxs-lookup"><span data-stu-id="41c75-367">A cleaner cartridge is present in the tape library.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-368"><span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**ERROR \_ IEPORT \_ completo**</span><span class="sxs-lookup"><span data-stu-id="41c75-368"><span id="ERROR_IEPORT_FULL"></span><span id="error_ieport_full"></span>**ERROR\_IEPORT\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-369">4341 (0x10F5)</span><span class="sxs-lookup"><span data-stu-id="41c75-369">4341 (0x10F5)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-370">No se puede usar el puerto de inserción y expulsión porque no está vacío.</span><span class="sxs-lookup"><span data-stu-id="41c75-370">Cannot use the inject/eject port because it is not empty.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-371"><span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**archivo de ERROR \_ \_ sin conexión**</span><span class="sxs-lookup"><span data-stu-id="41c75-371"><span id="ERROR_FILE_OFFLINE"></span><span id="error_file_offline"></span>**ERROR\_FILE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-372">4350 (0x10FE)</span><span class="sxs-lookup"><span data-stu-id="41c75-372">4350 (0x10FE)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-373">Este archivo no está disponible actualmente para su uso en este equipo.</span><span class="sxs-lookup"><span data-stu-id="41c75-373">This file is currently not available for use on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-374"><span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**ERROR \_ de \_ almacenamiento remoto \_ no \_ activo**</span><span class="sxs-lookup"><span data-stu-id="41c75-374"><span id="ERROR_REMOTE_STORAGE_NOT_ACTIVE"></span><span id="error_remote_storage_not_active"></span>**ERROR\_REMOTE\_STORAGE\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-375">4351 (0x10FF)</span><span class="sxs-lookup"><span data-stu-id="41c75-375">4351 (0x10FF)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-376">El servicio de almacenamiento remoto no está operativo en este momento.</span><span class="sxs-lookup"><span data-stu-id="41c75-376">The remote storage service is not operational at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-377"><span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**error \_ de \_ medio de almacenamiento remoto \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-377"><span id="ERROR_REMOTE_STORAGE_MEDIA_ERROR"></span><span id="error_remote_storage_media_error"></span>**ERROR\_REMOTE\_STORAGE\_MEDIA\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-378">4352 (0x1100)</span><span class="sxs-lookup"><span data-stu-id="41c75-378">4352 (0x1100)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-379">El servicio de almacenamiento remoto ha encontrado un error de medio.</span><span class="sxs-lookup"><span data-stu-id="41c75-379">The remote storage service encountered a media error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-380"><span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**ERROR \_ no es \_ un punto de \_ análisis \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-380"><span id="ERROR_NOT_A_REPARSE_POINT"></span><span id="error_not_a_reparse_point"></span>**ERROR\_NOT\_A\_REPARSE\_POINT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-381">4390 (0x1126)</span><span class="sxs-lookup"><span data-stu-id="41c75-381">4390 (0x1126)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-382">El archivo o directorio no es un punto de análisis.</span><span class="sxs-lookup"><span data-stu-id="41c75-382">The file or directory is not a reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-383"><span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**\_conflicto de REanálisis de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-383"><span id="ERROR_REPARSE_ATTRIBUTE_CONFLICT"></span><span id="error_reparse_attribute_conflict"></span>**ERROR\_REPARSE\_ATTRIBUTE\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-384">4391 (0x1127)</span><span class="sxs-lookup"><span data-stu-id="41c75-384">4391 (0x1127)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-385">No se puede establecer el atributo de punto de reanálisis porque entra en conflicto con un atributo existente.</span><span class="sxs-lookup"><span data-stu-id="41c75-385">The reparse point attribute cannot be set because it conflicts with an existing attribute.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-386"><span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**ERROR \_ al \_ analizar \_ datos no válidos**</span><span class="sxs-lookup"><span data-stu-id="41c75-386"><span id="ERROR_INVALID_REPARSE_DATA"></span><span id="error_invalid_reparse_data"></span>**ERROR\_INVALID\_REPARSE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-387">4392 (0x1128)</span><span class="sxs-lookup"><span data-stu-id="41c75-387">4392 (0x1128)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-388">Los datos presentes en el búfer de puntos de reanálisis no son válidos.</span><span class="sxs-lookup"><span data-stu-id="41c75-388">The data present in the reparse point buffer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-389"><span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**\_etiqueta de REanálisis de error \_ \_ no válida**</span><span class="sxs-lookup"><span data-stu-id="41c75-389"><span id="ERROR_REPARSE_TAG_INVALID"></span><span id="error_reparse_tag_invalid"></span>**ERROR\_REPARSE\_TAG\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-390">4393 (0x1129)</span><span class="sxs-lookup"><span data-stu-id="41c75-390">4393 (0x1129)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-391">La etiqueta presente en el búfer del punto de reanálisis no es válida.</span><span class="sxs-lookup"><span data-stu-id="41c75-391">The tag present in the reparse point buffer is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-392"><span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**ERROR de \_ coincidencia de etiqueta de REanálisis \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-392"><span id="ERROR_REPARSE_TAG_MISMATCH"></span><span id="error_reparse_tag_mismatch"></span>**ERROR\_REPARSE\_TAG\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-393">4394 (0x112A)</span><span class="sxs-lookup"><span data-stu-id="41c75-393">4394 (0x112A)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-394">Hay una discrepancia entre la etiqueta especificada en la solicitud y la etiqueta presente en el punto de reanálisis.</span><span class="sxs-lookup"><span data-stu-id="41c75-394">There is a mismatch between the tag specified in the request and the tag present in the reparse point.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-395"><span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**\_ \_ \_ no \_ se encontraron datos de la aplicación de error**</span><span class="sxs-lookup"><span data-stu-id="41c75-395"><span id="ERROR_APP_DATA_NOT_FOUND"></span><span id="error_app_data_not_found"></span>**ERROR\_APP\_DATA\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-396">4400 (0x1130)</span><span class="sxs-lookup"><span data-stu-id="41c75-396">4400 (0x1130)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-397">No se encuentran los datos de caché rápidos.</span><span class="sxs-lookup"><span data-stu-id="41c75-397">Fast Cache data not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-398"><span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**datos de la aplicación de ERROR \_ \_ \_ expirados**</span><span class="sxs-lookup"><span data-stu-id="41c75-398"><span id="ERROR_APP_DATA_EXPIRED"></span><span id="error_app_data_expired"></span>**ERROR\_APP\_DATA\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-399">4401 (0x1131)</span><span class="sxs-lookup"><span data-stu-id="41c75-399">4401 (0x1131)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-400">Los datos de caché rápidos expiraron.</span><span class="sxs-lookup"><span data-stu-id="41c75-400">Fast Cache data expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-401"><span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**datos de la aplicación de ERROR \_ \_ \_ dañados**</span><span class="sxs-lookup"><span data-stu-id="41c75-401"><span id="ERROR_APP_DATA_CORRUPT"></span><span id="error_app_data_corrupt"></span>**ERROR\_APP\_DATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-402">4402 (0x1132)</span><span class="sxs-lookup"><span data-stu-id="41c75-402">4402 (0x1132)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-403">Los datos de caché rápidos están dañados.</span><span class="sxs-lookup"><span data-stu-id="41c75-403">Fast Cache data corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-404"><span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**límite de datos de la aplicación de ERROR \_ \_ \_ \_ superado**</span><span class="sxs-lookup"><span data-stu-id="41c75-404"><span id="ERROR_APP_DATA_LIMIT_EXCEEDED"></span><span id="error_app_data_limit_exceeded"></span>**ERROR\_APP\_DATA\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-405">4403 (0x1133)</span><span class="sxs-lookup"><span data-stu-id="41c75-405">4403 (0x1133)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-406">Los datos de caché rápidos han superado su tamaño máximo y no se pueden actualizar.</span><span class="sxs-lookup"><span data-stu-id="41c75-406">Fast Cache data has exceeded its max size and cannot be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-407"><span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**ERROR \_ de \_ \_ reinicio de datos de la aplicación de error \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-407"><span id="ERROR_APP_DATA_REBOOT_REQUIRED"></span><span id="error_app_data_reboot_required"></span>**ERROR\_APP\_DATA\_REBOOT\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-408">4404 (0x1134)</span><span class="sxs-lookup"><span data-stu-id="41c75-408">4404 (0x1134)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-409">La memoria caché rápida se ha rearmado y requiere un reinicio hasta que se puede actualizar.</span><span class="sxs-lookup"><span data-stu-id="41c75-409">Fast Cache has been ReArmed and requires a reboot until it can be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-410"><span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**ERROR \_ de \_ reversión de SECUREBOOT \_ detectado**</span><span class="sxs-lookup"><span data-stu-id="41c75-410"><span id="ERROR_SECUREBOOT_ROLLBACK_DETECTED"></span><span id="error_secureboot_rollback_detected"></span>**ERROR\_SECUREBOOT\_ROLLBACK\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-411">4420 (0x1144)</span><span class="sxs-lookup"><span data-stu-id="41c75-411">4420 (0x1144)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-412">El arranque seguro detectó que se ha intentado revertir los datos protegidos.</span><span class="sxs-lookup"><span data-stu-id="41c75-412">Secure Boot detected that rollback of protected data has been attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-413"><span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**ERROR \_ de \_ infracción de la Directiva de SECUREBOOT \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-413"><span id="ERROR_SECUREBOOT_POLICY_VIOLATION"></span><span id="error_secureboot_policy_violation"></span>**ERROR\_SECUREBOOT\_POLICY\_VIOLATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-414">4421 (0x1145)</span><span class="sxs-lookup"><span data-stu-id="41c75-414">4421 (0x1145)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-415">El valor está protegido por la Directiva de arranque seguro y no se puede modificar ni eliminar.</span><span class="sxs-lookup"><span data-stu-id="41c75-415">The value is protected by Secure Boot policy and cannot be modified or deleted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-416"><span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**ERROR de \_ Directiva de SECUREBOOT \_ no válida \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-416"><span id="ERROR_SECUREBOOT_INVALID_POLICY"></span><span id="error_secureboot_invalid_policy"></span>**ERROR\_SECUREBOOT\_INVALID\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-417">4422 (0x1146)</span><span class="sxs-lookup"><span data-stu-id="41c75-417">4422 (0x1146)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-418">La Directiva de arranque seguro no es válida.</span><span class="sxs-lookup"><span data-stu-id="41c75-418">The Secure Boot policy is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-419"><span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**ERROR \_ \_ \_ \_ no \_ se encontró el editor de directivas de SECUREBOOT**</span><span class="sxs-lookup"><span data-stu-id="41c75-419"><span id="ERROR_SECUREBOOT_POLICY_PUBLISHER_NOT_FOUND"></span><span id="error_secureboot_policy_publisher_not_found"></span>**ERROR\_SECUREBOOT\_POLICY\_PUBLISHER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-420">4423 (0x1147)</span><span class="sxs-lookup"><span data-stu-id="41c75-420">4423 (0x1147)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-421">Una nueva Directiva de arranque seguro no contenía el publicador actual en su lista de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="41c75-421">A new Secure Boot policy did not contain the current publisher on its update list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-422"><span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**ERROR de la \_ Directiva de SECUREBOOT \_ \_ no \_ firmada**</span><span class="sxs-lookup"><span data-stu-id="41c75-422"><span id="ERROR_SECUREBOOT_POLICY_NOT_SIGNED"></span><span id="error_secureboot_policy_not_signed"></span>**ERROR\_SECUREBOOT\_POLICY\_NOT\_SIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-423">4424 (0x1148)</span><span class="sxs-lookup"><span data-stu-id="41c75-423">4424 (0x1148)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-424">La Directiva de arranque seguro no está firmada o está firmada por un firmante que no es de confianza.</span><span class="sxs-lookup"><span data-stu-id="41c75-424">The Secure Boot policy is either not signed or is signed by a non-trusted signer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-425"><span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**ERROR de \_ SECUREBOOT \_ no \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="41c75-425"><span id="ERROR_SECUREBOOT_NOT_ENABLED"></span><span id="error_secureboot_not_enabled"></span>**ERROR\_SECUREBOOT\_NOT\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-426">4425 (0x1149)</span><span class="sxs-lookup"><span data-stu-id="41c75-426">4425 (0x1149)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-427">El arranque seguro no está habilitado en esta máquina.</span><span class="sxs-lookup"><span data-stu-id="41c75-427">Secure Boot is not enabled on this machine.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-428"><span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**ERROR \_ de \_ archivo SECUREBOOT \_ reemplazado**</span><span class="sxs-lookup"><span data-stu-id="41c75-428"><span id="ERROR_SECUREBOOT_FILE_REPLACED"></span><span id="error_secureboot_file_replaced"></span>**ERROR\_SECUREBOOT\_FILE\_REPLACED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-429">4426 (0x114A)</span><span class="sxs-lookup"><span data-stu-id="41c75-429">4426 (0x114A)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-430">El arranque seguro requiere que determinados archivos y controladores no se reemplacen por otros archivos o controladores.</span><span class="sxs-lookup"><span data-stu-id="41c75-430">Secure Boot requires that certain files and drivers are not replaced by other files or drivers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-431"><span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**no se admite la descarga de errores de \_ \_ lectura de \_ FLT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-431"><span id="ERROR_OFFLOAD_READ_FLT_NOT_SUPPORTED"></span><span id="error_offload_read_flt_not_supported"></span>**ERROR\_OFFLOAD\_READ\_FLT\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-432">4440 (0x1158)</span><span class="sxs-lookup"><span data-stu-id="41c75-432">4440 (0x1158)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-433">No se admite la operación de lectura de descarga de copia en un filtro.</span><span class="sxs-lookup"><span data-stu-id="41c75-433">The copy offload read operation is not supported by a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-434"><span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**ERROR de escritura de la descarga de errores de \_ \_ \_ \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="41c75-434"><span id="ERROR_OFFLOAD_WRITE_FLT_NOT_SUPPORTED"></span><span id="error_offload_write_flt_not_supported"></span>**ERROR\_OFFLOAD\_WRITE\_FLT\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-435">4441 (0x1159)</span><span class="sxs-lookup"><span data-stu-id="41c75-435">4441 (0x1159)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-436">No se admite la operación de escritura de descarga de copia en un filtro.</span><span class="sxs-lookup"><span data-stu-id="41c75-436">The copy offload write operation is not supported by a filter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-437"><span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**ERROR al \_ descargar el \_ archivo de lectura \_ \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="41c75-437"><span id="ERROR_OFFLOAD_READ_FILE_NOT_SUPPORTED"></span><span id="error_offload_read_file_not_supported"></span>**ERROR\_OFFLOAD\_READ\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-438">4442 (0x115A)</span><span class="sxs-lookup"><span data-stu-id="41c75-438">4442 (0x115A)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-439">No se admite la operación de lectura de descarga de copia para el archivo.</span><span class="sxs-lookup"><span data-stu-id="41c75-439">The copy offload read operation is not supported for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-440"><span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**no se admite la descarga de \_ \_ archivos de escritura \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-440"><span id="ERROR_OFFLOAD_WRITE_FILE_NOT_SUPPORTED"></span><span id="error_offload_write_file_not_supported"></span>**ERROR\_OFFLOAD\_WRITE\_FILE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-441">4443 (0x115B)</span><span class="sxs-lookup"><span data-stu-id="41c75-441">4443 (0x115B)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-442">No se admite la operación de escritura de descarga de copia en el archivo.</span><span class="sxs-lookup"><span data-stu-id="41c75-442">The copy offload write operation is not supported for the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-443"><span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**volumen de ERROR \_ \_ no \_ SIS \_ habilitado**</span><span class="sxs-lookup"><span data-stu-id="41c75-443"><span id="ERROR_VOLUME_NOT_SIS_ENABLED"></span><span id="error_volume_not_sis_enabled"></span>**ERROR\_VOLUME\_NOT\_SIS\_ENABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-444">4500 (0x1194)</span><span class="sxs-lookup"><span data-stu-id="41c75-444">4500 (0x1194)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-445">El almacenamiento de instancia única no está disponible en este volumen.</span><span class="sxs-lookup"><span data-stu-id="41c75-445">Single Instance Storage is not available on this volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-446"><span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**\_existe un \_ recurso \_ dependiente del error**</span><span class="sxs-lookup"><span data-stu-id="41c75-446"><span id="ERROR_DEPENDENT_RESOURCE_EXISTS"></span><span id="error_dependent_resource_exists"></span>**ERROR\_DEPENDENT\_RESOURCE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-447">5001 (0x1389)</span><span class="sxs-lookup"><span data-stu-id="41c75-447">5001 (0x1389)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-448">No se puede completar la operación porque otros recursos dependen de este recurso.</span><span class="sxs-lookup"><span data-stu-id="41c75-448">The operation cannot be completed because other resources are dependent on this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-449"><span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**\_ \_ no \_ se encontró la dependencia de error**</span><span class="sxs-lookup"><span data-stu-id="41c75-449"><span id="ERROR_DEPENDENCY_NOT_FOUND"></span><span id="error_dependency_not_found"></span>**ERROR\_DEPENDENCY\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-450">5002 (0x138A)</span><span class="sxs-lookup"><span data-stu-id="41c75-450">5002 (0x138A)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-451">No se encuentra la dependencia de recursos de clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-451">The cluster resource dependency cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-452"><span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**la \_ dependencia de error \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="41c75-452"><span id="ERROR_DEPENDENCY_ALREADY_EXISTS"></span><span id="error_dependency_already_exists"></span>**ERROR\_DEPENDENCY\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-453">5003 (0x138B)</span><span class="sxs-lookup"><span data-stu-id="41c75-453">5003 (0x138B)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-454">No se puede hacer que el recurso de clúster dependa del recurso especificado porque ya depende de él.</span><span class="sxs-lookup"><span data-stu-id="41c75-454">The cluster resource cannot be made dependent on the specified resource because it is already dependent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-455"><span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**el \_ recurso de error \_ no está \_ en línea**</span><span class="sxs-lookup"><span data-stu-id="41c75-455"><span id="ERROR_RESOURCE_NOT_ONLINE"></span><span id="error_resource_not_online"></span>**ERROR\_RESOURCE\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-456">5004 (0x138C)</span><span class="sxs-lookup"><span data-stu-id="41c75-456">5004 (0x138C)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-457">El recurso de clúster no está en línea.</span><span class="sxs-lookup"><span data-stu-id="41c75-457">The cluster resource is not online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-458"><span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**el \_ nodo de host de error \_ \_ no \_ está disponible**</span><span class="sxs-lookup"><span data-stu-id="41c75-458"><span id="ERROR_HOST_NODE_NOT_AVAILABLE"></span><span id="error_host_node_not_available"></span>**ERROR\_HOST\_NODE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-459">5005 (0x138D)</span><span class="sxs-lookup"><span data-stu-id="41c75-459">5005 (0x138D)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-460">Un nodo de clúster no está disponible para esta operación.</span><span class="sxs-lookup"><span data-stu-id="41c75-460">A cluster node is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-461"><span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**recurso de ERROR \_ \_ no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="41c75-461"><span id="ERROR_RESOURCE_NOT_AVAILABLE"></span><span id="error_resource_not_available"></span>**ERROR\_RESOURCE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-462">5006 (0x138E)</span><span class="sxs-lookup"><span data-stu-id="41c75-462">5006 (0x138E)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-463">El recurso de clúster no está disponible.</span><span class="sxs-lookup"><span data-stu-id="41c75-463">The cluster resource is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-464"><span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**\_ \_ no \_ se encontró el recurso de error**</span><span class="sxs-lookup"><span data-stu-id="41c75-464"><span id="ERROR_RESOURCE_NOT_FOUND"></span><span id="error_resource_not_found"></span>**ERROR\_RESOURCE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-465">5007 (0x138F)</span><span class="sxs-lookup"><span data-stu-id="41c75-465">5007 (0x138F)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-466">No se encontró el recurso de clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-466">The cluster resource could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-467"><span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**ERROR al \_ cerrar el \_ clúster**</span><span class="sxs-lookup"><span data-stu-id="41c75-467"><span id="ERROR_SHUTDOWN_CLUSTER"></span><span id="error_shutdown_cluster"></span>**ERROR\_SHUTDOWN\_CLUSTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-468">5008 (0x1390)</span><span class="sxs-lookup"><span data-stu-id="41c75-468">5008 (0x1390)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-469">El clúster se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="41c75-469">The cluster is being shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-470"><span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**ERROR no se pudo \_ \_ expulsar el \_ \_ nodo activo**</span><span class="sxs-lookup"><span data-stu-id="41c75-470"><span id="ERROR_CANT_EVICT_ACTIVE_NODE"></span><span id="error_cant_evict_active_node"></span>**ERROR\_CANT\_EVICT\_ACTIVE\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-471">5009 (0x1391)</span><span class="sxs-lookup"><span data-stu-id="41c75-471">5009 (0x1391)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-472">Un nodo de clúster no se puede desalojar del clúster a menos que el nodo esté inactivo o sea el último nodo.</span><span class="sxs-lookup"><span data-stu-id="41c75-472">A cluster node cannot be evicted from the cluster unless the node is down or it is the last node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-473"><span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**el \_ objeto de error \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="41c75-473"><span id="ERROR_OBJECT_ALREADY_EXISTS"></span><span id="error_object_already_exists"></span>**ERROR\_OBJECT\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-474">5010 (0x1392)</span><span class="sxs-lookup"><span data-stu-id="41c75-474">5010 (0x1392)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-475">El objeto ya existe.</span><span class="sxs-lookup"><span data-stu-id="41c75-475">The object already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-476"><span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**\_objeto \_ de error en la \_ lista**</span><span class="sxs-lookup"><span data-stu-id="41c75-476"><span id="ERROR_OBJECT_IN_LIST"></span><span id="error_object_in_list"></span>**ERROR\_OBJECT\_IN\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-477">5011 (0x1393)</span><span class="sxs-lookup"><span data-stu-id="41c75-477">5011 (0x1393)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-478">El objeto ya está en la lista.</span><span class="sxs-lookup"><span data-stu-id="41c75-478">The object is already in the list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-479"><span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**Grupo de errores \_ \_ no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="41c75-479"><span id="ERROR_GROUP_NOT_AVAILABLE"></span><span id="error_group_not_available"></span>**ERROR\_GROUP\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-480">5012 (0x1394)</span><span class="sxs-lookup"><span data-stu-id="41c75-480">5012 (0x1394)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-481">El grupo de clústeres no está disponible para las nuevas solicitudes.</span><span class="sxs-lookup"><span data-stu-id="41c75-481">The cluster group is not available for any new requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-482"><span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**\_ \_ no \_ se encontró el grupo de errores**</span><span class="sxs-lookup"><span data-stu-id="41c75-482"><span id="ERROR_GROUP_NOT_FOUND"></span><span id="error_group_not_found"></span>**ERROR\_GROUP\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-483">5013 (0x1395)</span><span class="sxs-lookup"><span data-stu-id="41c75-483">5013 (0x1395)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-484">No se encontró el grupo de clústeres.</span><span class="sxs-lookup"><span data-stu-id="41c75-484">The cluster group could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-485"><span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**Grupo de errores \_ \_ no \_ en línea**</span><span class="sxs-lookup"><span data-stu-id="41c75-485"><span id="ERROR_GROUP_NOT_ONLINE"></span><span id="error_group_not_online"></span>**ERROR\_GROUP\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-486">5014 (0x1396)</span><span class="sxs-lookup"><span data-stu-id="41c75-486">5014 (0x1396)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-487">No se pudo completar la operación porque el grupo de clústeres no está en línea.</span><span class="sxs-lookup"><span data-stu-id="41c75-487">The operation could not be completed because the cluster group is not online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-488"><span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**ERROR \_ de \_ nodo \_ host \_ no \_ propietario de recursos**</span><span class="sxs-lookup"><span data-stu-id="41c75-488"><span id="ERROR_HOST_NODE_NOT_RESOURCE_OWNER"></span><span id="error_host_node_not_resource_owner"></span>**ERROR\_HOST\_NODE\_NOT\_RESOURCE\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-489">5015 (0x1397)</span><span class="sxs-lookup"><span data-stu-id="41c75-489">5015 (0x1397)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-490">Se produjo un error en la operación porque el nodo de clúster especificado no es el propietario del recurso o el nodo no es un posible propietario del recurso.</span><span class="sxs-lookup"><span data-stu-id="41c75-490">The operation failed because either the specified cluster node is not the owner of the resource, or the node is not a possible owner of the resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-491"><span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**ERROR \_ del \_ nodo \_ host \_ no \_ propietario del grupo**</span><span class="sxs-lookup"><span data-stu-id="41c75-491"><span id="ERROR_HOST_NODE_NOT_GROUP_OWNER"></span><span id="error_host_node_not_group_owner"></span>**ERROR\_HOST\_NODE\_NOT\_GROUP\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-492">5016 (0x1398)</span><span class="sxs-lookup"><span data-stu-id="41c75-492">5016 (0x1398)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-493">Error en la operación; el nodo de clúster especificado no es el propietario del grupo o el nodo no es un propietario posible del grupo.</span><span class="sxs-lookup"><span data-stu-id="41c75-493">The operation failed because either the specified cluster node is not the owner of the group, or the node is not a possible owner of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-494"><span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**ERROR \_ \_ al crear \_ RESMON**</span><span class="sxs-lookup"><span data-stu-id="41c75-494"><span id="ERROR_RESMON_CREATE_FAILED"></span><span id="error_resmon_create_failed"></span>**ERROR\_RESMON\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-495">5017 (0x1399)</span><span class="sxs-lookup"><span data-stu-id="41c75-495">5017 (0x1399)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-496">No se pudo crear el recurso de clúster en el monitor de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="41c75-496">The cluster resource could not be created in the specified resource monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-497"><span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**ERROR \_ RESMON \_ online \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-497"><span id="ERROR_RESMON_ONLINE_FAILED"></span><span id="error_resmon_online_failed"></span>**ERROR\_RESMON\_ONLINE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-498">5018 (0x139A)</span><span class="sxs-lookup"><span data-stu-id="41c75-498">5018 (0x139A)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-499">El monitor de recursos no pudo conectar el recurso de clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-499">The cluster resource could not be brought online by the resource monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-500"><span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**recurso de ERROR \_ \_ en línea**</span><span class="sxs-lookup"><span data-stu-id="41c75-500"><span id="ERROR_RESOURCE_ONLINE"></span><span id="error_resource_online"></span>**ERROR\_RESOURCE\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-501">5019 (0x139B)</span><span class="sxs-lookup"><span data-stu-id="41c75-501">5019 (0x139B)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-502">No se pudo completar la operación porque el recurso de clúster está en línea.</span><span class="sxs-lookup"><span data-stu-id="41c75-502">The operation could not be completed because the cluster resource is online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-503"><span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**\_recurso de cuórum de error \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-503"><span id="ERROR_QUORUM_RESOURCE"></span><span id="error_quorum_resource"></span>**ERROR\_QUORUM\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-504">5020 (0x139C)</span><span class="sxs-lookup"><span data-stu-id="41c75-504">5020 (0x139C)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-505">No se pudo eliminar o desconectar el recurso de clúster porque es el recurso de quórum.</span><span class="sxs-lookup"><span data-stu-id="41c75-505">The cluster resource could not be deleted or brought offline because it is the quorum resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-506"><span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**ERROR \_ no \_ compatible con cuórum \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-506"><span id="ERROR_NOT_QUORUM_CAPABLE"></span><span id="error_not_quorum_capable"></span>**ERROR\_NOT\_QUORUM\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-507">5021 (0x139D)</span><span class="sxs-lookup"><span data-stu-id="41c75-507">5021 (0x139D)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-508">El clúster no pudo convertir el recurso especificado en un recurso de quórum porque no es capaz de ser un recurso de quórum.</span><span class="sxs-lookup"><span data-stu-id="41c75-508">The cluster could not make the specified resource a quorum resource because it is not capable of being a quorum resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-509"><span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**ERROR \_ al \_ apagar el \_ clúster**</span><span class="sxs-lookup"><span data-stu-id="41c75-509"><span id="ERROR_CLUSTER_SHUTTING_DOWN"></span><span id="error_cluster_shutting_down"></span>**ERROR\_CLUSTER\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-510">5022 (0x139E)</span><span class="sxs-lookup"><span data-stu-id="41c75-510">5022 (0x139E)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-511">El software de clúster se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="41c75-511">The cluster software is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-512"><span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**ERROR \_ de \_ Estado no válido**</span><span class="sxs-lookup"><span data-stu-id="41c75-512"><span id="ERROR_INVALID_STATE"></span><span id="error_invalid_state"></span>**ERROR\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-513">5023 (0x139F)</span><span class="sxs-lookup"><span data-stu-id="41c75-513">5023 (0x139F)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-514">El grupo o recurso no está en el estado correcto para realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="41c75-514">The group or resource is not in the correct state to perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-515"><span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**propiedades de recursos de ERROR \_ \_ \_ almacenadas**</span><span class="sxs-lookup"><span data-stu-id="41c75-515"><span id="ERROR_RESOURCE_PROPERTIES_STORED"></span><span id="error_resource_properties_stored"></span>**ERROR\_RESOURCE\_PROPERTIES\_STORED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-516">5024 (0x13A0)</span><span class="sxs-lookup"><span data-stu-id="41c75-516">5024 (0x13A0)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-517">Se almacenaron las propiedades, pero no todos los cambios surtirán efecto hasta la próxima vez que el recurso se ponga en línea.</span><span class="sxs-lookup"><span data-stu-id="41c75-517">The properties were stored but not all changes will take effect until the next time the resource is brought online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-518"><span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**ERROR \_ de \_ clase de cuórum \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-518"><span id="ERROR_NOT_QUORUM_CLASS"></span><span id="error_not_quorum_class"></span>**ERROR\_NOT\_QUORUM\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-519">5025 (0x13A1)</span><span class="sxs-lookup"><span data-stu-id="41c75-519">5025 (0x13A1)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-520">El clúster no pudo convertir el recurso especificado en un recurso de quórum porque no pertenece a una clase de almacenamiento compartida.</span><span class="sxs-lookup"><span data-stu-id="41c75-520">The cluster could not make the specified resource a quorum resource because it does not belong to a shared storage class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-521"><span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**ERROR \_ de \_ recurso Core**</span><span class="sxs-lookup"><span data-stu-id="41c75-521"><span id="ERROR_CORE_RESOURCE"></span><span id="error_core_resource"></span>**ERROR\_CORE\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-522">5026 (0x13A2)</span><span class="sxs-lookup"><span data-stu-id="41c75-522">5026 (0x13A2)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-523">No se pudo eliminar el recurso de clúster porque es un recurso principal.</span><span class="sxs-lookup"><span data-stu-id="41c75-523">The cluster resource could not be deleted since it is a core resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-524"><span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**ERROR de \_ recurso de cuórum con \_ \_ conexión \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-524"><span id="ERROR_QUORUM_RESOURCE_ONLINE_FAILED"></span><span id="error_quorum_resource_online_failed"></span>**ERROR\_QUORUM\_RESOURCE\_ONLINE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-525">5027 (0x13A3)</span><span class="sxs-lookup"><span data-stu-id="41c75-525">5027 (0x13A3)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-526">No se pudo conectar el recurso de cuórum.</span><span class="sxs-lookup"><span data-stu-id="41c75-526">The quorum resource failed to come online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-527"><span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**ERROR \_ \_ al abrir \_ QUORUMLOG**</span><span class="sxs-lookup"><span data-stu-id="41c75-527"><span id="ERROR_QUORUMLOG_OPEN_FAILED"></span><span id="error_quorumlog_open_failed"></span>**ERROR\_QUORUMLOG\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-528">5028 (0x13A4)</span><span class="sxs-lookup"><span data-stu-id="41c75-528">5028 (0x13A4)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-529">No se pudo crear o montar correctamente el registro de cuórum.</span><span class="sxs-lookup"><span data-stu-id="41c75-529">The quorum log could not be created or mounted successfully.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-530"><span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**ERROR \_ CLUSTERLOG \_ dañado**</span><span class="sxs-lookup"><span data-stu-id="41c75-530"><span id="ERROR_CLUSTERLOG_CORRUPT"></span><span id="error_clusterlog_corrupt"></span>**ERROR\_CLUSTERLOG\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-531">5029 (0x13A5)</span><span class="sxs-lookup"><span data-stu-id="41c75-531">5029 (0x13A5)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-532">El registro del clúster está dañado.</span><span class="sxs-lookup"><span data-stu-id="41c75-532">The cluster log is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-533"><span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**el \_ registro de error CLUSTERLOG \_ \_ supera \_ MaxSize**</span><span class="sxs-lookup"><span data-stu-id="41c75-533"><span id="ERROR_CLUSTERLOG_RECORD_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_record_exceeds_maxsize"></span>**ERROR\_CLUSTERLOG\_RECORD\_EXCEEDS\_MAXSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-534">5030 (0x13A6)</span><span class="sxs-lookup"><span data-stu-id="41c75-534">5030 (0x13A6)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-535">No se pudo escribir el registro en el registro del clúster, ya que supera el tamaño máximo.</span><span class="sxs-lookup"><span data-stu-id="41c75-535">The record could not be written to the cluster log since it exceeds the maximum size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-536"><span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**el ERROR \_ CLUSTERLOG \_ supera \_ MaxSize**</span><span class="sxs-lookup"><span data-stu-id="41c75-536"><span id="ERROR_CLUSTERLOG_EXCEEDS_MAXSIZE"></span><span id="error_clusterlog_exceeds_maxsize"></span>**ERROR\_CLUSTERLOG\_EXCEEDS\_MAXSIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-537">5031 (0x13A7)</span><span class="sxs-lookup"><span data-stu-id="41c75-537">5031 (0x13A7)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-538">El registro del clúster supera su tamaño máximo.</span><span class="sxs-lookup"><span data-stu-id="41c75-538">The cluster log exceeds its maximum size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-539"><span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**ERROR \_ CLUSTERLOG \_ CHKPOINT \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="41c75-539"><span id="ERROR_CLUSTERLOG_CHKPOINT_NOT_FOUND"></span><span id="error_clusterlog_chkpoint_not_found"></span>**ERROR\_CLUSTERLOG\_CHKPOINT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-540">5032 (0x13A8)</span><span class="sxs-lookup"><span data-stu-id="41c75-540">5032 (0x13A8)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-541">No se encontró ningún registro de punto de comprobación en el registro del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-541">No checkpoint record was found in the cluster log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-542"><span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**ERROR \_ CLUSTERLOG \_ no \_ hay suficiente \_ espacio**</span><span class="sxs-lookup"><span data-stu-id="41c75-542"><span id="ERROR_CLUSTERLOG_NOT_ENOUGH_SPACE"></span><span id="error_clusterlog_not_enough_space"></span>**ERROR\_CLUSTERLOG\_NOT\_ENOUGH\_SPACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-543">5033 (0x13A9)</span><span class="sxs-lookup"><span data-stu-id="41c75-543">5033 (0x13A9)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-544">El espacio en disco mínimo necesario para el registro no está disponible.</span><span class="sxs-lookup"><span data-stu-id="41c75-544">The minimum required disk space needed for logging is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-545"><span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**ERROR \_ del \_ propietario del cuórum \_ activo**</span><span class="sxs-lookup"><span data-stu-id="41c75-545"><span id="ERROR_QUORUM_OWNER_ALIVE"></span><span id="error_quorum_owner_alive"></span>**ERROR\_QUORUM\_OWNER\_ALIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-546">5034 (0x13AA)</span><span class="sxs-lookup"><span data-stu-id="41c75-546">5034 (0x13AA)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-547">El nodo de clúster no pudo tomar el control del recurso de cuórum porque el recurso pertenece a otro nodo activo.</span><span class="sxs-lookup"><span data-stu-id="41c75-547">The cluster node failed to take control of the quorum resource because the resource is owned by another active node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-548"><span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**la \_ red de errores \_ no \_ está disponible**</span><span class="sxs-lookup"><span data-stu-id="41c75-548"><span id="ERROR_NETWORK_NOT_AVAILABLE"></span><span id="error_network_not_available"></span>**ERROR\_NETWORK\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-549">5035 (0x13AB)</span><span class="sxs-lookup"><span data-stu-id="41c75-549">5035 (0x13AB)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-550">Una red de clústeres no está disponible para esta operación.</span><span class="sxs-lookup"><span data-stu-id="41c75-550">A cluster network is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-551"><span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**nodo de ERROR \_ \_ no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="41c75-551"><span id="ERROR_NODE_NOT_AVAILABLE"></span><span id="error_node_not_available"></span>**ERROR\_NODE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-552">5036 (0x13AC)</span><span class="sxs-lookup"><span data-stu-id="41c75-552">5036 (0x13AC)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-553">Un nodo de clúster no está disponible para esta operación.</span><span class="sxs-lookup"><span data-stu-id="41c75-553">A cluster node is not available for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-554"><span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**ERROR: \_ todos los \_ nodos \_ no \_ están disponibles**</span><span class="sxs-lookup"><span data-stu-id="41c75-554"><span id="ERROR_ALL_NODES_NOT_AVAILABLE"></span><span id="error_all_nodes_not_available"></span>**ERROR\_ALL\_NODES\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-555">5037 (0x13AD)</span><span class="sxs-lookup"><span data-stu-id="41c75-555">5037 (0x13AD)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-556">Todos los nodos del clúster deben estar en ejecución para realizar esta operación.</span><span class="sxs-lookup"><span data-stu-id="41c75-556">All cluster nodes must be running to perform this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-557"><span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**ERROR de recurso de ERROR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-557"><span id="ERROR_RESOURCE_FAILED"></span><span id="error_resource_failed"></span>**ERROR\_RESOURCE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-558">5038 (0x13AE)</span><span class="sxs-lookup"><span data-stu-id="41c75-558">5038 (0x13AE)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-559">error en un recurso de clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-559">A cluster resource failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-560"><span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**ERROR \_ de \_ nodo no válido del clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-560"><span id="ERROR_CLUSTER_INVALID_NODE"></span><span id="error_cluster_invalid_node"></span>**ERROR\_CLUSTER\_INVALID\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-561">5039 (0x13AF)</span><span class="sxs-lookup"><span data-stu-id="41c75-561">5039 (0x13AF)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-562">El nodo de clúster no es válido.</span><span class="sxs-lookup"><span data-stu-id="41c75-562">The cluster node is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-563"><span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**\_existe un \_ nodo de clúster de error \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-563"><span id="ERROR_CLUSTER_NODE_EXISTS"></span><span id="error_cluster_node_exists"></span>**ERROR\_CLUSTER\_NODE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-564">5040 (0x13B0)</span><span class="sxs-lookup"><span data-stu-id="41c75-564">5040 (0x13B0)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-565">El nodo de clúster ya existe.</span><span class="sxs-lookup"><span data-stu-id="41c75-565">The cluster node already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-566"><span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**\_ \_ combinación de clústeres de error \_ en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="41c75-566"><span id="ERROR_CLUSTER_JOIN_IN_PROGRESS"></span><span id="error_cluster_join_in_progress"></span>**ERROR\_CLUSTER\_JOIN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-567">5041 (0x13B1)</span><span class="sxs-lookup"><span data-stu-id="41c75-567">5041 (0x13B1)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-568">Un nodo está en el proceso de unirse al clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-568">A node is in the process of joining the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-569"><span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**\_ \_ \_ no \_ se encontró el nodo de clúster de error**</span><span class="sxs-lookup"><span data-stu-id="41c75-569"><span id="ERROR_CLUSTER_NODE_NOT_FOUND"></span><span id="error_cluster_node_not_found"></span>**ERROR\_CLUSTER\_NODE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-570">5042 (0x13B2)</span><span class="sxs-lookup"><span data-stu-id="41c75-570">5042 (0x13B2)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-571">No se encontró el nodo de clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-571">The cluster node was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-572"><span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**\_ \_ \_ \_ no se encontró el nodo \_ local del clúster de errores**</span><span class="sxs-lookup"><span data-stu-id="41c75-572"><span id="ERROR_CLUSTER_LOCAL_NODE_NOT_FOUND"></span><span id="error_cluster_local_node_not_found"></span>**ERROR\_CLUSTER\_LOCAL\_NODE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-573">5043 (0x13B3)</span><span class="sxs-lookup"><span data-stu-id="41c75-573">5043 (0x13B3)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-574">No se encontró la información del nodo local del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-574">The cluster local node information was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-575"><span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**ERROR en la \_ red de clústeres \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-575"><span id="ERROR_CLUSTER_NETWORK_EXISTS"></span><span id="error_cluster_network_exists"></span>**ERROR\_CLUSTER\_NETWORK\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-576">5044 (0x13B4)</span><span class="sxs-lookup"><span data-stu-id="41c75-576">5044 (0x13B4)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-577">La red de clústeres ya existe.</span><span class="sxs-lookup"><span data-stu-id="41c75-577">The cluster network already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-578"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**\_ \_ \_ no \_ se encontró la red de clústeres de errores**</span><span class="sxs-lookup"><span data-stu-id="41c75-578"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND"></span><span id="error_cluster_network_not_found"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-579">5045 (0x13B5)</span><span class="sxs-lookup"><span data-stu-id="41c75-579">5045 (0x13B5)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-580">No se encontró la red de clústeres.</span><span class="sxs-lookup"><span data-stu-id="41c75-580">The cluster network was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-581"><span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**ERROR en el \_ clúster \_ NETINTERFACE \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-581"><span id="ERROR_CLUSTER_NETINTERFACE_EXISTS"></span><span id="error_cluster_netinterface_exists"></span>**ERROR\_CLUSTER\_NETINTERFACE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-582">5046 (0x13B6)</span><span class="sxs-lookup"><span data-stu-id="41c75-582">5046 (0x13B6)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-583">La interfaz de red de clústeres ya existe.</span><span class="sxs-lookup"><span data-stu-id="41c75-583">The cluster network interface already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-584"><span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**ERROR de \_ clúster \_ NETINTERFACE \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="41c75-584"><span id="ERROR_CLUSTER_NETINTERFACE_NOT_FOUND"></span><span id="error_cluster_netinterface_not_found"></span>**ERROR\_CLUSTER\_NETINTERFACE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-585">5047 (0x13B7)</span><span class="sxs-lookup"><span data-stu-id="41c75-585">5047 (0x13B7)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-586">No se encontró la interfaz de red del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-586">The cluster network interface was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-587"><span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**ERROR de \_ solicitud de clúster \_ no válida \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-587"><span id="ERROR_CLUSTER_INVALID_REQUEST"></span><span id="error_cluster_invalid_request"></span>**ERROR\_CLUSTER\_INVALID\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-588">5048 (0x13B8)</span><span class="sxs-lookup"><span data-stu-id="41c75-588">5048 (0x13B8)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-589">La solicitud de clúster no es válida para este objeto.</span><span class="sxs-lookup"><span data-stu-id="41c75-589">The cluster request is not valid for this object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-590"><span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**ERROR \_ de \_ \_ proveedor de red no válido en el clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-590"><span id="ERROR_CLUSTER_INVALID_NETWORK_PROVIDER"></span><span id="error_cluster_invalid_network_provider"></span>**ERROR\_CLUSTER\_INVALID\_NETWORK\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-591">5049 (0x13B9)</span><span class="sxs-lookup"><span data-stu-id="41c75-591">5049 (0x13B9)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-592">El proveedor de red de clústeres no es válido.</span><span class="sxs-lookup"><span data-stu-id="41c75-592">The cluster network provider is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-593"><span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**ERROR en el \_ nodo de clúster \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-593"><span id="ERROR_CLUSTER_NODE_DOWN"></span><span id="error_cluster_node_down"></span>**ERROR\_CLUSTER\_NODE\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-594">5050 (0x13BA)</span><span class="sxs-lookup"><span data-stu-id="41c75-594">5050 (0x13BA)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-595">El nodo de clúster está inactivo.</span><span class="sxs-lookup"><span data-stu-id="41c75-595">The cluster node is down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-596"><span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**no \_ se \_ \_ puede tener acceso al nodo de clúster de errores**</span><span class="sxs-lookup"><span data-stu-id="41c75-596"><span id="ERROR_CLUSTER_NODE_UNREACHABLE"></span><span id="error_cluster_node_unreachable"></span>**ERROR\_CLUSTER\_NODE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-597">5051 (0x13BB)</span><span class="sxs-lookup"><span data-stu-id="41c75-597">5051 (0x13BB)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-598">No se puede obtener acceso al nodo de clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-598">The cluster node is not reachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-599"><span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**ERROR \_ de \_ nodo de clúster \_ no \_ miembro**</span><span class="sxs-lookup"><span data-stu-id="41c75-599"><span id="ERROR_CLUSTER_NODE_NOT_MEMBER"></span><span id="error_cluster_node_not_member"></span>**ERROR\_CLUSTER\_NODE\_NOT\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-600">5052 (0x13BC)</span><span class="sxs-lookup"><span data-stu-id="41c75-600">5052 (0x13BC)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-601">El nodo de clúster no es un miembro del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-601">The cluster node is not a member of the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-602"><span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**\_ \_ combinación de clústeres de errores \_ no \_ en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="41c75-602"><span id="ERROR_CLUSTER_JOIN_NOT_IN_PROGRESS"></span><span id="error_cluster_join_not_in_progress"></span>**ERROR\_CLUSTER\_JOIN\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-603">5053 (0x13BD)</span><span class="sxs-lookup"><span data-stu-id="41c75-603">5053 (0x13BD)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-604">Una operación de unión al clúster no está en curso.</span><span class="sxs-lookup"><span data-stu-id="41c75-604">A cluster join operation is not in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-605"><span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**ERROR \_ de \_ red no válida del clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-605"><span id="ERROR_CLUSTER_INVALID_NETWORK"></span><span id="error_cluster_invalid_network"></span>**ERROR\_CLUSTER\_INVALID\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-606">5054 (0x13BE)</span><span class="sxs-lookup"><span data-stu-id="41c75-606">5054 (0x13BE)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-607">La red de clústeres no es válida.</span><span class="sxs-lookup"><span data-stu-id="41c75-607">The cluster network is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-608"><span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**ERROR en el \_ \_ nodo \_ de clúster**</span><span class="sxs-lookup"><span data-stu-id="41c75-608"><span id="ERROR_CLUSTER_NODE_UP"></span><span id="error_cluster_node_up"></span>**ERROR\_CLUSTER\_NODE\_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-609">5056 (0x13C0)</span><span class="sxs-lookup"><span data-stu-id="41c75-609">5056 (0x13C0)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-610">El nodo de clúster está activo.</span><span class="sxs-lookup"><span data-stu-id="41c75-610">The cluster node is up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-611"><span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**ERROR \_ \_ de DirIP \_ de clúster en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="41c75-611"><span id="ERROR_CLUSTER_IPADDR_IN_USE"></span><span id="error_cluster_ipaddr_in_use"></span>**ERROR\_CLUSTER\_IPADDR\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-612">5057 (0x13C1)</span><span class="sxs-lookup"><span data-stu-id="41c75-612">5057 (0x13C1)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-613">La dirección IP del clúster ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="41c75-613">The cluster IP address is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-614"><span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**nodo de clúster de ERROR \_ \_ \_ no \_ pausado**</span><span class="sxs-lookup"><span data-stu-id="41c75-614"><span id="ERROR_CLUSTER_NODE_NOT_PAUSED"></span><span id="error_cluster_node_not_paused"></span>**ERROR\_CLUSTER\_NODE\_NOT\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-615">5058 (0x13C2)</span><span class="sxs-lookup"><span data-stu-id="41c75-615">5058 (0x13C2)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-616">El nodo de clúster no está en pausa.</span><span class="sxs-lookup"><span data-stu-id="41c75-616">The cluster node is not paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-617"><span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**ERROR \_ de \_ clúster \_ sin \_ contexto de seguridad**</span><span class="sxs-lookup"><span data-stu-id="41c75-617"><span id="ERROR_CLUSTER_NO_SECURITY_CONTEXT"></span><span id="error_cluster_no_security_context"></span>**ERROR\_CLUSTER\_NO\_SECURITY\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-618">5059 (0x13C3)</span><span class="sxs-lookup"><span data-stu-id="41c75-618">5059 (0x13C3)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-619">No hay ningún contexto de seguridad de clúster disponible.</span><span class="sxs-lookup"><span data-stu-id="41c75-619">No cluster security context is available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-620"><span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**ERROR de \_ red de clústeres \_ \_ no \_ interna**</span><span class="sxs-lookup"><span data-stu-id="41c75-620"><span id="ERROR_CLUSTER_NETWORK_NOT_INTERNAL"></span><span id="error_cluster_network_not_internal"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-621">5060 (0x13C4)</span><span class="sxs-lookup"><span data-stu-id="41c75-621">5060 (0x13C4)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-622">La red de clústeres no está configurada para la comunicación interna del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-622">The cluster network is not configured for internal cluster communication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-623"><span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**el \_ \_ nodo \_ de clúster de error ya está \_ activo**</span><span class="sxs-lookup"><span data-stu-id="41c75-623"><span id="ERROR_CLUSTER_NODE_ALREADY_UP"></span><span id="error_cluster_node_already_up"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_UP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-624">5061 (0x13C5)</span><span class="sxs-lookup"><span data-stu-id="41c75-624">5061 (0x13C5)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-625">El nodo de clúster ya está activo.</span><span class="sxs-lookup"><span data-stu-id="41c75-625">The cluster node is already up.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-626"><span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**el \_ nodo de clúster de errores \_ \_ ya está \_ inactivo**</span><span class="sxs-lookup"><span data-stu-id="41c75-626"><span id="ERROR_CLUSTER_NODE_ALREADY_DOWN"></span><span id="error_cluster_node_already_down"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-627">5062 (0x13C6)</span><span class="sxs-lookup"><span data-stu-id="41c75-627">5062 (0x13C6)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-628">El nodo de clúster ya está inactivo.</span><span class="sxs-lookup"><span data-stu-id="41c75-628">The cluster node is already down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-629"><span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**la \_ red de clústeres de errores \_ \_ ya está \_ en línea**</span><span class="sxs-lookup"><span data-stu-id="41c75-629"><span id="ERROR_CLUSTER_NETWORK_ALREADY_ONLINE"></span><span id="error_cluster_network_already_online"></span>**ERROR\_CLUSTER\_NETWORK\_ALREADY\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-630">5063 (0x13C7)</span><span class="sxs-lookup"><span data-stu-id="41c75-630">5063 (0x13C7)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-631">La red de clústeres ya está en línea.</span><span class="sxs-lookup"><span data-stu-id="41c75-631">The cluster network is already online.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-632"><span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**la \_ red de clústeres de errores \_ \_ ya está \_ sin conexión**</span><span class="sxs-lookup"><span data-stu-id="41c75-632"><span id="ERROR_CLUSTER_NETWORK_ALREADY_OFFLINE"></span><span id="error_cluster_network_already_offline"></span>**ERROR\_CLUSTER\_NETWORK\_ALREADY\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-633">5064 (0x13C8)</span><span class="sxs-lookup"><span data-stu-id="41c75-633">5064 (0x13C8)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-634">La red de clústeres ya está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="41c75-634">The cluster network is already offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-635"><span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**el \_ nodo de clúster de error \_ ya es \_ \_ miembro**</span><span class="sxs-lookup"><span data-stu-id="41c75-635"><span id="ERROR_CLUSTER_NODE_ALREADY_MEMBER"></span><span id="error_cluster_node_already_member"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-636">5065 (0x13C9)</span><span class="sxs-lookup"><span data-stu-id="41c75-636">5065 (0x13C9)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-637">El nodo de clúster ya es miembro del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-637">The cluster node is already a member of the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-638"><span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**\_ \_ última \_ red interna de clúster de errores \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-638"><span id="ERROR_CLUSTER_LAST_INTERNAL_NETWORK"></span><span id="error_cluster_last_internal_network"></span>**ERROR\_CLUSTER\_LAST\_INTERNAL\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-639">5066 (0x13CA)</span><span class="sxs-lookup"><span data-stu-id="41c75-639">5066 (0x13CA)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-640">La red de clústeres es la única que se configura para la comunicación interna del clúster entre dos o más nodos de clúster activos.</span><span class="sxs-lookup"><span data-stu-id="41c75-640">The cluster network is the only one configured for internal cluster communication between two or more active cluster nodes.</span></span> <span data-ttu-id="41c75-641">No se puede quitar la funcionalidad de comunicación interna de la red.</span><span class="sxs-lookup"><span data-stu-id="41c75-641">The internal communication capability cannot be removed from the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-642"><span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**ERROR: la \_ red de clústeres \_ \_ tiene \_ dependientes**</span><span class="sxs-lookup"><span data-stu-id="41c75-642"><span id="ERROR_CLUSTER_NETWORK_HAS_DEPENDENTS"></span><span id="error_cluster_network_has_dependents"></span>**ERROR\_CLUSTER\_NETWORK\_HAS\_DEPENDENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-643">5067 (0x13CB)</span><span class="sxs-lookup"><span data-stu-id="41c75-643">5067 (0x13CB)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-644">Uno o más recursos de clúster dependen de la red para proporcionar servicio a los clientes.</span><span class="sxs-lookup"><span data-stu-id="41c75-644">One or more cluster resources depend on the network to provide service to clients.</span></span> <span data-ttu-id="41c75-645">No se puede quitar la funcionalidad de acceso de cliente de la red.</span><span class="sxs-lookup"><span data-stu-id="41c75-645">The client access capability cannot be removed from the network.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-646"><span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**ERROR \_ en una operación no válida \_ \_ en el \_ cuórum**</span><span class="sxs-lookup"><span data-stu-id="41c75-646"><span id="ERROR_INVALID_OPERATION_ON_QUORUM"></span><span id="error_invalid_operation_on_quorum"></span>**ERROR\_INVALID\_OPERATION\_ON\_QUORUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-647">5068 (0x13CC)</span><span class="sxs-lookup"><span data-stu-id="41c75-647">5068 (0x13CC)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-648">Esta operación no se puede realizar en el recurso de clúster como el recurso de cuórum.</span><span class="sxs-lookup"><span data-stu-id="41c75-648">This operation cannot be performed on the cluster resource as it the quorum resource.</span></span> <span data-ttu-id="41c75-649">No se puede desconectar el recurso de cuórum ni modificar su lista de posibles propietarios.</span><span class="sxs-lookup"><span data-stu-id="41c75-649">You may not bring the quorum resource offline or modify its possible owners list.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-650"><span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**\_no se \_ \_ permite la dependencia de error**</span><span class="sxs-lookup"><span data-stu-id="41c75-650"><span id="ERROR_DEPENDENCY_NOT_ALLOWED"></span><span id="error_dependency_not_allowed"></span>**ERROR\_DEPENDENCY\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-651">5069 (0x13CD)</span><span class="sxs-lookup"><span data-stu-id="41c75-651">5069 (0x13CD)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-652">El recurso de cuórum de clúster no puede tener ninguna dependencia.</span><span class="sxs-lookup"><span data-stu-id="41c75-652">The cluster quorum resource is not allowed to have any dependencies.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-653"><span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**ERROR de \_ nodo de clúster en \_ \_ pausa**</span><span class="sxs-lookup"><span data-stu-id="41c75-653"><span id="ERROR_CLUSTER_NODE_PAUSED"></span><span id="error_cluster_node_paused"></span>**ERROR\_CLUSTER\_NODE\_PAUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-654">5070 (0x13CE)</span><span class="sxs-lookup"><span data-stu-id="41c75-654">5070 (0x13CE)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-655">El nodo de clúster está en pausa.</span><span class="sxs-lookup"><span data-stu-id="41c75-655">The cluster node is paused.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-656"><span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**el nodo de ERROR no tiene \_ \_ \_ recursos de host \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-656"><span id="ERROR_NODE_CANT_HOST_RESOURCE"></span><span id="error_node_cant_host_resource"></span>**ERROR\_NODE\_CANT\_HOST\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-657">5071 (0x13CF)</span><span class="sxs-lookup"><span data-stu-id="41c75-657">5071 (0x13CF)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-658">No se puede poner en línea el recurso de clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-658">The cluster resource cannot be brought online.</span></span> <span data-ttu-id="41c75-659">El nodo propietario no puede ejecutar este recurso.</span><span class="sxs-lookup"><span data-stu-id="41c75-659">The owner node cannot run this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-660"><span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**ERROR \_ de \_ nodo de clúster \_ no \_ preparado**</span><span class="sxs-lookup"><span data-stu-id="41c75-660"><span id="ERROR_CLUSTER_NODE_NOT_READY"></span><span id="error_cluster_node_not_ready"></span>**ERROR\_CLUSTER\_NODE\_NOT\_READY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-661">5072 (0x13D0)</span><span class="sxs-lookup"><span data-stu-id="41c75-661">5072 (0x13D0)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-662">El nodo de clúster no está listo para realizar la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="41c75-662">The cluster node is not ready to perform the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-663"><span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**ERROR \_ al \_ cerrar el nodo de clúster \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-663"><span id="ERROR_CLUSTER_NODE_SHUTTING_DOWN"></span><span id="error_cluster_node_shutting_down"></span>**ERROR\_CLUSTER\_NODE\_SHUTTING\_DOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-664">5073 (0x13D1)</span><span class="sxs-lookup"><span data-stu-id="41c75-664">5073 (0x13D1)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-665">El nodo de clúster se está cerrando.</span><span class="sxs-lookup"><span data-stu-id="41c75-665">The cluster node is shutting down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-666"><span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**ERROR \_ de \_ Unión de clúster \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="41c75-666"><span id="ERROR_CLUSTER_JOIN_ABORTED"></span><span id="error_cluster_join_aborted"></span>**ERROR\_CLUSTER\_JOIN\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-667">5074 (0x13D2)</span><span class="sxs-lookup"><span data-stu-id="41c75-667">5074 (0x13D2)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-668">Se anuló la operación de combinación del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-668">The cluster join operation was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-669"><span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**ERROR \_ en \_ las versiones incompatibles del clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-669"><span id="ERROR_CLUSTER_INCOMPATIBLE_VERSIONS"></span><span id="error_cluster_incompatible_versions"></span>**ERROR\_CLUSTER\_INCOMPATIBLE\_VERSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-670">5075 (0x13D3)</span><span class="sxs-lookup"><span data-stu-id="41c75-670">5075 (0x13D3)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-671">No se pudo realizar la operación de unión al clúster debido a versiones de software incompatibles entre el nodo de Unión y su patrocinador.</span><span class="sxs-lookup"><span data-stu-id="41c75-671">The cluster join operation failed due to incompatible software versions between the joining node and its sponsor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-672"><span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**ERROR en el \_ clúster \_ MAXNUM \_ de \_ recursos \_ superado**</span><span class="sxs-lookup"><span data-stu-id="41c75-672"><span id="ERROR_CLUSTER_MAXNUM_OF_RESOURCES_EXCEEDED"></span><span id="error_cluster_maxnum_of_resources_exceeded"></span>**ERROR\_CLUSTER\_MAXNUM\_OF\_RESOURCES\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-673">5076 (0x13D4)</span><span class="sxs-lookup"><span data-stu-id="41c75-673">5076 (0x13D4)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-674">Este recurso no se puede crear porque el clúster ha alcanzado el límite en el número de recursos que puede supervisar.</span><span class="sxs-lookup"><span data-stu-id="41c75-674">This resource cannot be created because the cluster has reached the limit on the number of resources it can monitor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-675"><span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**ERROR en la \_ \_ configuración del sistema de clústeres \_ \_ modificada**</span><span class="sxs-lookup"><span data-stu-id="41c75-675"><span id="ERROR_CLUSTER_SYSTEM_CONFIG_CHANGED"></span><span id="error_cluster_system_config_changed"></span>**ERROR\_CLUSTER\_SYSTEM\_CONFIG\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-676">5077 (0x13D5)</span><span class="sxs-lookup"><span data-stu-id="41c75-676">5077 (0x13D5)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-677">La configuración del sistema ha cambiado durante la operación de combinación o de forma de clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-677">The system configuration changed during the cluster join or form operation.</span></span> <span data-ttu-id="41c75-678">Se anuló la operación de combinación o de formulario.</span><span class="sxs-lookup"><span data-stu-id="41c75-678">The join or form operation was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-679"><span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**\_ \_ \_ \_ no se encontró el tipo \_ de recurso de clúster de error**</span><span class="sxs-lookup"><span data-stu-id="41c75-679"><span id="ERROR_CLUSTER_RESOURCE_TYPE_NOT_FOUND"></span><span id="error_cluster_resource_type_not_found"></span>**ERROR\_CLUSTER\_RESOURCE\_TYPE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-680">5078 (0x13D6)</span><span class="sxs-lookup"><span data-stu-id="41c75-680">5078 (0x13D6)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-681">No se encontró el tipo de recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="41c75-681">The specified resource type was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-682"><span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**RESTYPE de clúster de ERROR \_ \_ \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="41c75-682"><span id="ERROR_CLUSTER_RESTYPE_NOT_SUPPORTED"></span><span id="error_cluster_restype_not_supported"></span>**ERROR\_CLUSTER\_RESTYPE\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-683">5079 (0x13D7)</span><span class="sxs-lookup"><span data-stu-id="41c75-683">5079 (0x13D7)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-684">El nodo especificado no admite un recurso de este tipo.</span><span class="sxs-lookup"><span data-stu-id="41c75-684">The specified node does not support a resource of this type.</span></span> <span data-ttu-id="41c75-685">Esto puede deberse a incoherencias de versión o a la ausencia del archivo DLL de recursos en este nodo.</span><span class="sxs-lookup"><span data-stu-id="41c75-685">This may be due to version inconsistencies or due to the absence of the resource DLL on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-686"><span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**\_ \_ \_ no \_ se encontró el clúster de error RESNAME**</span><span class="sxs-lookup"><span data-stu-id="41c75-686"><span id="ERROR_CLUSTER_RESNAME_NOT_FOUND"></span><span id="error_cluster_resname_not_found"></span>**ERROR\_CLUSTER\_RESNAME\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-687">5080 (0x13D8)</span><span class="sxs-lookup"><span data-stu-id="41c75-687">5080 (0x13D8)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-688">Este archivo DLL de recursos no admite el nombre de recurso especificado.</span><span class="sxs-lookup"><span data-stu-id="41c75-688">The specified resource name is not supported by this resource DLL.</span></span> <span data-ttu-id="41c75-689">Esto puede deberse a un nombre incorrecto (o cambiado) proporcionado a la DLL de recursos.</span><span class="sxs-lookup"><span data-stu-id="41c75-689">This may be due to a bad (or changed) name supplied to the resource DLL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-690"><span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**ERROR de \_ clúster no se ha \_ \_ registrado ningún \_ paquete RPC \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-690"><span id="ERROR_CLUSTER_NO_RPC_PACKAGES_REGISTERED"></span><span id="error_cluster_no_rpc_packages_registered"></span>**ERROR\_CLUSTER\_NO\_RPC\_PACKAGES\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-691">5081 (0x13D9)</span><span class="sxs-lookup"><span data-stu-id="41c75-691">5081 (0x13D9)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-692">No se pudo registrar ningún paquete de autenticación con el servidor RPC.</span><span class="sxs-lookup"><span data-stu-id="41c75-692">No authentication package could be registered with the RPC server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-693"><span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**ERROR \_ el \_ propietario del clúster no está \_ \_ en \_ PREFLIST**</span><span class="sxs-lookup"><span data-stu-id="41c75-693"><span id="ERROR_CLUSTER_OWNER_NOT_IN_PREFLIST"></span><span id="error_cluster_owner_not_in_preflist"></span>**ERROR\_CLUSTER\_OWNER\_NOT\_IN\_PREFLIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-694">5082 (0x13DA)</span><span class="sxs-lookup"><span data-stu-id="41c75-694">5082 (0x13DA)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-695">No se puede poner en línea el grupo porque el propietario del grupo no está en la lista preferida para el grupo.</span><span class="sxs-lookup"><span data-stu-id="41c75-695">You cannot bring the group online because the owner of the group is not in the preferred list for the group.</span></span> <span data-ttu-id="41c75-696">Para cambiar el nodo propietario del grupo, mueva el grupo.</span><span class="sxs-lookup"><span data-stu-id="41c75-696">To change the owner node for the group, move the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-697"><span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**ERROR \_ de \_ base de datos de clúster \_ SEQMISMATCH**</span><span class="sxs-lookup"><span data-stu-id="41c75-697"><span id="ERROR_CLUSTER_DATABASE_SEQMISMATCH"></span><span id="error_cluster_database_seqmismatch"></span>**ERROR\_CLUSTER\_DATABASE\_SEQMISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-698">5083 (0x13DB)</span><span class="sxs-lookup"><span data-stu-id="41c75-698">5083 (0x13DB)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-699">No se pudo realizar la operación de combinación porque el número de secuencia de la base de datos del clúster ha cambiado o es incompatible con el nodo del bloqueo.</span><span class="sxs-lookup"><span data-stu-id="41c75-699">The join operation failed because the cluster database sequence number has changed or is incompatible with the locker node.</span></span> <span data-ttu-id="41c75-700">Esto puede ocurrir durante una operación de combinación si la base de datos del clúster cambió durante la combinación.</span><span class="sxs-lookup"><span data-stu-id="41c75-700">This may happen during a join operation if the cluster database was changing during the join.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-701"><span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**ERROR \_ RESMON \_ Estado no válido \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-701"><span id="ERROR_RESMON_INVALID_STATE"></span><span id="error_resmon_invalid_state"></span>**ERROR\_RESMON\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-702">5084 (0x13DC)</span><span class="sxs-lookup"><span data-stu-id="41c75-702">5084 (0x13DC)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-703">El monitor de recursos no permitirá que se realice la operación de error mientras el recurso está en su estado actual.</span><span class="sxs-lookup"><span data-stu-id="41c75-703">The resource monitor will not allow the fail operation to be performed while the resource is in its current state.</span></span> <span data-ttu-id="41c75-704">Esto puede ocurrir si el recurso está en estado pendiente.</span><span class="sxs-lookup"><span data-stu-id="41c75-704">This may happen if the resource is in a pending state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-705"><span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**ERROR \_ de \_ \_ almacén de clústeres de errores \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-705"><span id="ERROR_CLUSTER_GUM_NOT_LOCKER"></span><span id="error_cluster_gum_not_locker"></span>**ERROR\_CLUSTER\_GUM\_NOT\_LOCKER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-706">5085 (0x13DD)</span><span class="sxs-lookup"><span data-stu-id="41c75-706">5085 (0x13DD)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-707">Un código que no es de bloqueo ha recibido una solicitud para reservar el bloqueo para hacer actualizaciones globales.</span><span class="sxs-lookup"><span data-stu-id="41c75-707">A non locker code got a request to reserve the lock for making global updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-708"><span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**\_ \_ \_ no \_ se encontró el disco de cuórum de error**</span><span class="sxs-lookup"><span data-stu-id="41c75-708"><span id="ERROR_QUORUM_DISK_NOT_FOUND"></span><span id="error_quorum_disk_not_found"></span>**ERROR\_QUORUM\_DISK\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-709">5086 (0x13DE)</span><span class="sxs-lookup"><span data-stu-id="41c75-709">5086 (0x13DE)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-710">El servicio de Cluster Server no pudo encontrar el disco de quórum.</span><span class="sxs-lookup"><span data-stu-id="41c75-710">The quorum disk could not be located by the cluster service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-711"><span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**ERROR de \_ copia de seguridad de base de datos \_ \_ dañado**</span><span class="sxs-lookup"><span data-stu-id="41c75-711"><span id="ERROR_DATABASE_BACKUP_CORRUPT"></span><span id="error_database_backup_corrupt"></span>**ERROR\_DATABASE\_BACKUP\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-712">5087 (0x13DF)</span><span class="sxs-lookup"><span data-stu-id="41c75-712">5087 (0x13DF)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-713">La base de datos de clúster de copia de seguridad podría estar dañada.</span><span class="sxs-lookup"><span data-stu-id="41c75-713">The backed up cluster database is possibly corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-714"><span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**el \_ nodo de clúster de errores \_ \_ ya \_ tiene una \_ \_ raíz DFS**</span><span class="sxs-lookup"><span data-stu-id="41c75-714"><span id="ERROR_CLUSTER_NODE_ALREADY_HAS_DFS_ROOT"></span><span id="error_cluster_node_already_has_dfs_root"></span>**ERROR\_CLUSTER\_NODE\_ALREADY\_HAS\_DFS\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-715">5088 (0x13E0)</span><span class="sxs-lookup"><span data-stu-id="41c75-715">5088 (0x13E0)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-716">Ya existe una raíz DFS en este nodo de clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-716">A DFS root already exists in this cluster node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-717"><span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**propiedad de recurso de ERROR \_ \_ \_ inalterable**</span><span class="sxs-lookup"><span data-stu-id="41c75-717"><span id="ERROR_RESOURCE_PROPERTY_UNCHANGEABLE"></span><span id="error_resource_property_unchangeable"></span>**ERROR\_RESOURCE\_PROPERTY\_UNCHANGEABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-718">5089 (0x13E1)</span><span class="sxs-lookup"><span data-stu-id="41c75-718">5089 (0x13E1)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-719">Error al intentar modificar una propiedad de recurso porque entra en conflicto con otra propiedad existente.</span><span class="sxs-lookup"><span data-stu-id="41c75-719">An attempt to modify a resource property failed because it conflicts with another existing property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-720"><span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**ERROR \_ de \_ \_ Estado no válido de pertenencia al clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-720"><span id="ERROR_CLUSTER_MEMBERSHIP_INVALID_STATE"></span><span id="error_cluster_membership_invalid_state"></span>**ERROR\_CLUSTER\_MEMBERSHIP\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-721">5890 (0x1702)</span><span class="sxs-lookup"><span data-stu-id="41c75-721">5890 (0x1702)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-722">Se intentó realizar una operación que no es compatible con el estado de pertenencia actual del nodo.</span><span class="sxs-lookup"><span data-stu-id="41c75-722">An operation was attempted that is incompatible with the current membership state of the node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-723"><span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**\_ \_ \_ no \_ se encontró el clúster de error QUORUMLOG**</span><span class="sxs-lookup"><span data-stu-id="41c75-723"><span id="ERROR_CLUSTER_QUORUMLOG_NOT_FOUND"></span><span id="error_cluster_quorumlog_not_found"></span>**ERROR\_CLUSTER\_QUORUMLOG\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-724">5891 (0x1703)</span><span class="sxs-lookup"><span data-stu-id="41c75-724">5891 (0x1703)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-725">El recurso de cuórum no contiene el registro de cuórum.</span><span class="sxs-lookup"><span data-stu-id="41c75-725">The quorum resource does not contain the quorum log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-726"><span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**ERROR \_ de \_ pertenencia al clúster \_ detenida**</span><span class="sxs-lookup"><span data-stu-id="41c75-726"><span id="ERROR_CLUSTER_MEMBERSHIP_HALT"></span><span id="error_cluster_membership_halt"></span>**ERROR\_CLUSTER\_MEMBERSHIP\_HALT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-727">5892 (0x1704)</span><span class="sxs-lookup"><span data-stu-id="41c75-727">5892 (0x1704)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-728">El motor de pertenencia solicitó el cierre del servicio de clúster en este nodo.</span><span class="sxs-lookup"><span data-stu-id="41c75-728">The membership engine requested shutdown of the cluster service on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-729"><span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de ID. de instancia de clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-729"><span id="ERROR_CLUSTER_INSTANCE_ID_MISMATCH"></span><span id="error_cluster_instance_id_mismatch"></span>**ERROR\_CLUSTER\_INSTANCE\_ID\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-730">5893 (0x1705)</span><span class="sxs-lookup"><span data-stu-id="41c75-730">5893 (0x1705)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-731">No se pudo realizar la operación de combinación porque el ID. de instancia de clúster del nodo de Unión no coincide con el ID. de instancia de clúster del nodo de patrocinador.</span><span class="sxs-lookup"><span data-stu-id="41c75-731">The join operation failed because the cluster instance ID of the joining node does not match the cluster instance ID of the sponsor node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-732"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**\_ \_ \_ no se encuentra la red de clústeres \_ de errores \_ para \_ IP**</span><span class="sxs-lookup"><span data-stu-id="41c75-732"><span id="ERROR_CLUSTER_NETWORK_NOT_FOUND_FOR_IP"></span><span id="error_cluster_network_not_found_for_ip"></span>**ERROR\_CLUSTER\_NETWORK\_NOT\_FOUND\_FOR\_IP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-733">5894 (0x1706)</span><span class="sxs-lookup"><span data-stu-id="41c75-733">5894 (0x1706)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-734">No se encontró ninguna red de clústeres correspondiente para la dirección IP especificada.</span><span class="sxs-lookup"><span data-stu-id="41c75-734">A matching cluster network for the specified IP address could not be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-735"><span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de \_ tipo de datos \_ de la propiedad de clúster**</span><span class="sxs-lookup"><span data-stu-id="41c75-735"><span id="ERROR_CLUSTER_PROPERTY_DATA_TYPE_MISMATCH"></span><span id="error_cluster_property_data_type_mismatch"></span>**ERROR\_CLUSTER\_PROPERTY\_DATA\_TYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-736">5895 (0x1707)</span><span class="sxs-lookup"><span data-stu-id="41c75-736">5895 (0x1707)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-737">El tipo de datos real de la propiedad no coincidía con el tipo de datos esperado de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="41c75-737">The actual data type of the property did not match the expected data type of the property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-738"><span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**ERROR \_ al \_ expulsar el clúster \_ sin \_ limpieza**</span><span class="sxs-lookup"><span data-stu-id="41c75-738"><span id="ERROR_CLUSTER_EVICT_WITHOUT_CLEANUP"></span><span id="error_cluster_evict_without_cleanup"></span>**ERROR\_CLUSTER\_EVICT\_WITHOUT\_CLEANUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-739">5896 (0x1708)</span><span class="sxs-lookup"><span data-stu-id="41c75-739">5896 (0x1708)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-740">El nodo de clúster se expulsó del clúster correctamente, pero el nodo no se limpió.</span><span class="sxs-lookup"><span data-stu-id="41c75-740">The cluster node was evicted from the cluster successfully, but the node was not cleaned up.</span></span> <span data-ttu-id="41c75-741">Para determinar qué pasos de limpieza no se han realizado correctamente y cómo recuperarlos, consulte el registro de eventos de la aplicación de clústeres de conmutación por error mediante Visor de eventos.</span><span class="sxs-lookup"><span data-stu-id="41c75-741">To determine what cleanup steps failed and how to recover, see the Failover Clustering application event log using Event Viewer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-742"><span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**ERROR \_ de \_ coincidencia de parámetro de clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-742"><span id="ERROR_CLUSTER_PARAMETER_MISMATCH"></span><span id="error_cluster_parameter_mismatch"></span>**ERROR\_CLUSTER\_PARAMETER\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-743">5897 (0x1709)</span><span class="sxs-lookup"><span data-stu-id="41c75-743">5897 (0x1709)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-744">Dos o más valores de parámetro especificados para las propiedades de un recurso están en conflicto.</span><span class="sxs-lookup"><span data-stu-id="41c75-744">Two or more parameter values specified for a resource's properties are in conflict.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-745"><span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**el \_ nodo de error \_ no se puede \_ \_ agrupar en clúster**</span><span class="sxs-lookup"><span data-stu-id="41c75-745"><span id="ERROR_NODE_CANNOT_BE_CLUSTERED"></span><span id="error_node_cannot_be_clustered"></span>**ERROR\_NODE\_CANNOT\_BE\_CLUSTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-746">5898 (0x170A)</span><span class="sxs-lookup"><span data-stu-id="41c75-746">5898 (0x170A)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-747">Este equipo no se puede convertir en miembro de un clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-747">This computer cannot be made a member of a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-748"><span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**ERROR \_ de \_ versión incorrecta del \_ sistema operativo del clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-748"><span id="ERROR_CLUSTER_WRONG_OS_VERSION"></span><span id="error_cluster_wrong_os_version"></span>**ERROR\_CLUSTER\_WRONG\_OS\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-749">5899 (0x170B)</span><span class="sxs-lookup"><span data-stu-id="41c75-749">5899 (0x170B)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-750">Este equipo no se puede convertir en miembro de un clúster porque no tiene instalada la versión correcta de Windows.</span><span class="sxs-lookup"><span data-stu-id="41c75-750">This computer cannot be made a member of a cluster because it does not have the correct version of Windows installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-751"><span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**ERROR clúster no se pudo \_ \_ \_ crear \_ \_ el nombre del clúster duplicado \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-751"><span id="ERROR_CLUSTER_CANT_CREATE_DUP_CLUSTER_NAME"></span><span id="error_cluster_cant_create_dup_cluster_name"></span>**ERROR\_CLUSTER\_CANT\_CREATE\_DUP\_CLUSTER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-752">5900 (0x170C)</span><span class="sxs-lookup"><span data-stu-id="41c75-752">5900 (0x170C)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-753">No se puede crear un clúster con el nombre de clúster especificado porque ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="41c75-753">A cluster cannot be created with the specified cluster name because that cluster name is already in use.</span></span> <span data-ttu-id="41c75-754">Especifique un nombre diferente para el clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-754">Specify a different name for the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-755"><span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**ERROR \_ CLUSCFG \_ ya \_ confirmado**</span><span class="sxs-lookup"><span data-stu-id="41c75-755"><span id="ERROR_CLUSCFG_ALREADY_COMMITTED"></span><span id="error_cluscfg_already_committed"></span>**ERROR\_CLUSCFG\_ALREADY\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-756">5901 (0x170D)</span><span class="sxs-lookup"><span data-stu-id="41c75-756">5901 (0x170D)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-757">La acción de configuración del clúster ya se ha confirmado.</span><span class="sxs-lookup"><span data-stu-id="41c75-757">The cluster configuration action has already been committed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-758"><span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**ERROR \_ de \_ reversión de CLUSCFG \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-758"><span id="ERROR_CLUSCFG_ROLLBACK_FAILED"></span><span id="error_cluscfg_rollback_failed"></span>**ERROR\_CLUSCFG\_ROLLBACK\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-759">5902 (0x170E)</span><span class="sxs-lookup"><span data-stu-id="41c75-759">5902 (0x170E)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-760">No se pudo revertir la acción de configuración del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-760">The cluster configuration action could not be rolled back.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-761"><span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**ERROR \_ CLUSCFG \_ \_ conflicto de \_ Letras de unidad de disco del \_ sistema \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-761"><span id="ERROR_CLUSCFG_SYSTEM_DISK_DRIVE_LETTER_CONFLICT"></span><span id="error_cluscfg_system_disk_drive_letter_conflict"></span>**ERROR\_CLUSCFG\_SYSTEM\_DISK\_DRIVE\_LETTER\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-762">5903 (0x170F)</span><span class="sxs-lookup"><span data-stu-id="41c75-762">5903 (0x170F)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-763">La letra de unidad asignada a un disco del sistema en un nodo en conflicto con la letra de unidad asignada a un disco en otro nodo.</span><span class="sxs-lookup"><span data-stu-id="41c75-763">The drive letter assigned to a system disk on one node conflicted with the drive letter assigned to a disk on another node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-764"><span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**\_versión anterior del clúster de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-764"><span id="ERROR_CLUSTER_OLD_VERSION"></span><span id="error_cluster_old_version"></span>**ERROR\_CLUSTER\_OLD\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-765">5904 (0x1710)</span><span class="sxs-lookup"><span data-stu-id="41c75-765">5904 (0x1710)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-766">Uno o más nodos del clúster están ejecutando una versión de Windows que no admite esta operación.</span><span class="sxs-lookup"><span data-stu-id="41c75-766">One or more nodes in the cluster are running a version of Windows that does not support this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-767"><span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**ERROR de nombre de cuenta de \_ equipo no coincidente del clúster \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-767"><span id="ERROR_CLUSTER_MISMATCHED_COMPUTER_ACCT_NAME"></span><span id="error_cluster_mismatched_computer_acct_name"></span>**ERROR\_CLUSTER\_MISMATCHED\_COMPUTER\_ACCT\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-768">5905 (0x1711)</span><span class="sxs-lookup"><span data-stu-id="41c75-768">5905 (0x1711)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-769">El nombre de la cuenta de equipo correspondiente no coincide con el nombre de red de este recurso.</span><span class="sxs-lookup"><span data-stu-id="41c75-769">The name of the corresponding computer account doesn't match the Network Name for this resource.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-770"><span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**ERROR en el \_ clúster: \_ no hay \_ adaptadores de red \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-770"><span id="ERROR_CLUSTER_NO_NET_ADAPTERS"></span><span id="error_cluster_no_net_adapters"></span>**ERROR\_CLUSTER\_NO\_NET\_ADAPTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-771">5906 (0x1712)</span><span class="sxs-lookup"><span data-stu-id="41c75-771">5906 (0x1712)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-772">No hay adaptadores de red disponibles.</span><span class="sxs-lookup"><span data-stu-id="41c75-772">No network adapters are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-773"><span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**ERROR de \_ clúster \_ erróneo**</span><span class="sxs-lookup"><span data-stu-id="41c75-773"><span id="ERROR_CLUSTER_POISONED"></span><span id="error_cluster_poisoned"></span>**ERROR\_CLUSTER\_POISONED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-774">5907 (0x1713)</span><span class="sxs-lookup"><span data-stu-id="41c75-774">5907 (0x1713)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-775">Se ha dañado el nodo de clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-775">The cluster node has been poisoned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-776"><span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**ERROR \_ al \_ mover el grupo de clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-776"><span id="ERROR_CLUSTER_GROUP_MOVING"></span><span id="error_cluster_group_moving"></span>**ERROR\_CLUSTER\_GROUP\_MOVING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-777">5908 (0x1714)</span><span class="sxs-lookup"><span data-stu-id="41c75-777">5908 (0x1714)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-778">El grupo no puede aceptar la solicitud porque se está moviendo a otro nodo.</span><span class="sxs-lookup"><span data-stu-id="41c75-778">The group is unable to accept the request since it is moving to another node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-779"><span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**ERROR \_ de \_ tipo de recurso de clúster \_ \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="41c75-779"><span id="ERROR_CLUSTER_RESOURCE_TYPE_BUSY"></span><span id="error_cluster_resource_type_busy"></span>**ERROR\_CLUSTER\_RESOURCE\_TYPE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-780">5909 (0x1715)</span><span class="sxs-lookup"><span data-stu-id="41c75-780">5909 (0x1715)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-781">El tipo de recurso no puede aceptar la solicitud porque está demasiado ocupado realizando otra operación.</span><span class="sxs-lookup"><span data-stu-id="41c75-781">The resource type cannot accept the request since is too busy performing another operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-782"><span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**se \_ \_ \_ agotó el tiempo de \_ espera de la llamada de recurso de error**</span><span class="sxs-lookup"><span data-stu-id="41c75-782"><span id="ERROR_RESOURCE_CALL_TIMED_OUT"></span><span id="error_resource_call_timed_out"></span>**ERROR\_RESOURCE\_CALL\_TIMED\_OUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-783">5910 (0x1716)</span><span class="sxs-lookup"><span data-stu-id="41c75-783">5910 (0x1716)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-784">Se agotó el tiempo de espera de la llamada a la DLL de recursos del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-784">The call to the cluster resource DLL timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-785"><span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**ERROR \_ de \_ \_ dirección IPv6 de clúster no válida \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-785"><span id="ERROR_INVALID_CLUSTER_IPV6_ADDRESS"></span><span id="error_invalid_cluster_ipv6_address"></span>**ERROR\_INVALID\_CLUSTER\_IPV6\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-786">5911 (0x1717)</span><span class="sxs-lookup"><span data-stu-id="41c75-786">5911 (0x1717)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-787">La dirección no es válida para un recurso de dirección IPv6.</span><span class="sxs-lookup"><span data-stu-id="41c75-787">The address is not valid for an IPv6 Address resource.</span></span> <span data-ttu-id="41c75-788">Se requiere una dirección IPv6 global y debe coincidir con una red de clústeres.</span><span class="sxs-lookup"><span data-stu-id="41c75-788">A global IPv6 address is required, and it must match a cluster network.</span></span> <span data-ttu-id="41c75-789">No se permiten direcciones de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="41c75-789">Compatibility addresses are not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-790"><span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**ERROR \_ interno de la \_ \_ función no válida \_ del clúster**</span><span class="sxs-lookup"><span data-stu-id="41c75-790"><span id="ERROR_CLUSTER_INTERNAL_INVALID_FUNCTION"></span><span id="error_cluster_internal_invalid_function"></span>**ERROR\_CLUSTER\_INTERNAL\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-791">5912 (0x1718)</span><span class="sxs-lookup"><span data-stu-id="41c75-791">5912 (0x1718)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-792">Se produjo un error interno del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-792">An internal cluster error occurred.</span></span> <span data-ttu-id="41c75-793">Se intentó realizar una llamada a una función no válida.</span><span class="sxs-lookup"><span data-stu-id="41c75-793">A call to an invalid function was attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-794"><span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**\_ \_ parámetro de clúster \_ de error fuera \_ de los \_ límites**</span><span class="sxs-lookup"><span data-stu-id="41c75-794"><span id="ERROR_CLUSTER_PARAMETER_OUT_OF_BOUNDS"></span><span id="error_cluster_parameter_out_of_bounds"></span>**ERROR\_CLUSTER\_PARAMETER\_OUT\_OF\_BOUNDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-795">5913 (0x1719)</span><span class="sxs-lookup"><span data-stu-id="41c75-795">5913 (0x1719)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-796">Un valor de parámetro está fuera del intervalo aceptable.</span><span class="sxs-lookup"><span data-stu-id="41c75-796">A parameter value is out of acceptable range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-797"><span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**ERROR \_ de \_ envío parcial de clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-797"><span id="ERROR_CLUSTER_PARTIAL_SEND"></span><span id="error_cluster_partial_send"></span>**ERROR\_CLUSTER\_PARTIAL\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-798">5914 (0x171A)</span><span class="sxs-lookup"><span data-stu-id="41c75-798">5914 (0x171A)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-799">Se produjo un error de red al enviar datos a otro nodo del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-799">A network error occurred while sending data to another node in the cluster.</span></span> <span data-ttu-id="41c75-800">El número de bytes transmitidos era menor que el necesario.</span><span class="sxs-lookup"><span data-stu-id="41c75-800">The number of bytes transmitted was less than required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-801"><span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**ERROR \_ \_ del registro del clúster \_ función no válida \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-801"><span id="ERROR_CLUSTER_REGISTRY_INVALID_FUNCTION"></span><span id="error_cluster_registry_invalid_function"></span>**ERROR\_CLUSTER\_REGISTRY\_INVALID\_FUNCTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-802">5915 (0x171B)</span><span class="sxs-lookup"><span data-stu-id="41c75-802">5915 (0x171B)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-803">Se intentó realizar una operación no válida del registro del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-803">An invalid cluster registry operation was attempted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-804"><span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**ERROR \_ de \_ \_ terminación de cadena no válida del clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-804"><span id="ERROR_CLUSTER_INVALID_STRING_TERMINATION"></span><span id="error_cluster_invalid_string_termination"></span>**ERROR\_CLUSTER\_INVALID\_STRING\_TERMINATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-805">5916 (0x171C)</span><span class="sxs-lookup"><span data-stu-id="41c75-805">5916 (0x171C)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-806">Una cadena de caracteres de entrada no finaliza correctamente.</span><span class="sxs-lookup"><span data-stu-id="41c75-806">An input string of characters is not properly terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-807"><span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**ERROR \_ de \_ \_ formato de cadena no válido en el clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-807"><span id="ERROR_CLUSTER_INVALID_STRING_FORMAT"></span><span id="error_cluster_invalid_string_format"></span>**ERROR\_CLUSTER\_INVALID\_STRING\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-808">5917 (0x171D)</span><span class="sxs-lookup"><span data-stu-id="41c75-808">5917 (0x171D)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-809">Una cadena de caracteres de entrada no tiene un formato válido para los datos que representa.</span><span class="sxs-lookup"><span data-stu-id="41c75-809">An input string of characters is not in a valid format for the data it represents.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-810"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**\_ \_ \_ transacción \_ de base de datos de clúster de errores en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="41c75-810"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_IN_PROGRESS"></span><span id="error_cluster_database_transaction_in_progress"></span>**ERROR\_CLUSTER\_DATABASE\_TRANSACTION\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-811">5918 (0x171E)</span><span class="sxs-lookup"><span data-stu-id="41c75-811">5918 (0x171E)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-812">Se produjo un error interno del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-812">An internal cluster error occurred.</span></span> <span data-ttu-id="41c75-813">Se intentó una transacción de base de datos de clúster mientras una transacción ya estaba en curso.</span><span class="sxs-lookup"><span data-stu-id="41c75-813">A cluster database transaction was attempted while a transaction was already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-814"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**la \_ \_ transacción de la base de datos del clúster \_ de errores no está \_ \_ en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="41c75-814"><span id="ERROR_CLUSTER_DATABASE_TRANSACTION_NOT_IN_PROGRESS"></span><span id="error_cluster_database_transaction_not_in_progress"></span>**ERROR\_CLUSTER\_DATABASE\_TRANSACTION\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-815">5919 (0x171F)</span><span class="sxs-lookup"><span data-stu-id="41c75-815">5919 (0x171F)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-816">Se produjo un error interno del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-816">An internal cluster error occurred.</span></span> <span data-ttu-id="41c75-817">Se intentó confirmar una transacción de base de datos de clúster mientras no había ninguna transacción en curso.</span><span class="sxs-lookup"><span data-stu-id="41c75-817">There was an attempt to commit a cluster database transaction while no transaction was in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-818"><span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**ERROR \_ de \_ datos nulos del clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-818"><span id="ERROR_CLUSTER_NULL_DATA"></span><span id="error_cluster_null_data"></span>**ERROR\_CLUSTER\_NULL\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-819">5920 (0x1720)</span><span class="sxs-lookup"><span data-stu-id="41c75-819">5920 (0x1720)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-820">Se produjo un error interno del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-820">An internal cluster error occurred.</span></span> <span data-ttu-id="41c75-821">Los datos no se inicializaron correctamente.</span><span class="sxs-lookup"><span data-stu-id="41c75-821">Data was not properly initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-822"><span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**ERROR \_ de \_ lectura parcial del clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-822"><span id="ERROR_CLUSTER_PARTIAL_READ"></span><span id="error_cluster_partial_read"></span>**ERROR\_CLUSTER\_PARTIAL\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-823">5921 (0x1721)</span><span class="sxs-lookup"><span data-stu-id="41c75-823">5921 (0x1721)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-824">Se produjo un error al leer de un flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="41c75-824">An error occurred while reading from a stream of data.</span></span> <span data-ttu-id="41c75-825">Se devolvió un número inesperado de bytes.</span><span class="sxs-lookup"><span data-stu-id="41c75-825">An unexpected number of bytes was returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-826"><span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**ERROR \_ de \_ escritura parcial del clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-826"><span id="ERROR_CLUSTER_PARTIAL_WRITE"></span><span id="error_cluster_partial_write"></span>**ERROR\_CLUSTER\_PARTIAL\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-827">5922 (0x1722)</span><span class="sxs-lookup"><span data-stu-id="41c75-827">5922 (0x1722)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-828">Se produjo un error al escribir en un flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="41c75-828">An error occurred while writing to a stream of data.</span></span> <span data-ttu-id="41c75-829">No se pudo escribir el número necesario de bytes.</span><span class="sxs-lookup"><span data-stu-id="41c75-829">The required number of bytes could not be written.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-830"><span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**ERROR Cluster no se pudo \_ \_ \_ deserializar \_ datos**</span><span class="sxs-lookup"><span data-stu-id="41c75-830"><span id="ERROR_CLUSTER_CANT_DESERIALIZE_DATA"></span><span id="error_cluster_cant_deserialize_data"></span>**ERROR\_CLUSTER\_CANT\_DESERIALIZE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-831">5923 (0x1723)</span><span class="sxs-lookup"><span data-stu-id="41c75-831">5923 (0x1723)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-832">Se produjo un error al deserializar una secuencia de datos del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-832">An error occurred while deserializing a stream of cluster data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-833"><span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**\_conflicto de \_ propiedades de recursos dependientes de \_ error \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-833"><span id="ERROR_DEPENDENT_RESOURCE_PROPERTY_CONFLICT"></span><span id="error_dependent_resource_property_conflict"></span>**ERROR\_DEPENDENT\_RESOURCE\_PROPERTY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-834">5924 (0x1724)</span><span class="sxs-lookup"><span data-stu-id="41c75-834">5924 (0x1724)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-835">Uno o más valores de propiedad de este recurso están en conflicto con uno o varios valores de propiedad asociados a sus recursos dependientes.</span><span class="sxs-lookup"><span data-stu-id="41c75-835">One or more property values for this resource are in conflict with one or more property values associated with its dependent resource(s).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-836"><span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**ERROR de \_ clúster \_ sin \_ cuórum**</span><span class="sxs-lookup"><span data-stu-id="41c75-836"><span id="ERROR_CLUSTER_NO_QUORUM"></span><span id="error_cluster_no_quorum"></span>**ERROR\_CLUSTER\_NO\_QUORUM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-837">5925 (0x1725)</span><span class="sxs-lookup"><span data-stu-id="41c75-837">5925 (0x1725)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-838">No se ha encontrado un cuórum de nodos de clúster para formar un clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-838">A quorum of cluster nodes was not present to form a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-839"><span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**ERROR en la \_ \_ \_ red IPv6 no válida del clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-839"><span id="ERROR_CLUSTER_INVALID_IPV6_NETWORK"></span><span id="error_cluster_invalid_ipv6_network"></span>**ERROR\_CLUSTER\_INVALID\_IPV6\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-840">5926 (0x1726)</span><span class="sxs-lookup"><span data-stu-id="41c75-840">5926 (0x1726)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-841">La red de clústeres no es válida para un recurso de dirección IPv6 o no coincide con la dirección configurada.</span><span class="sxs-lookup"><span data-stu-id="41c75-841">The cluster network is not valid for an IPv6 Address resource, or it does not match the configured address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-842"><span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**ERROR \_ de \_ \_ red de \_ túnel \_ IPv6 no válida del clúster**</span><span class="sxs-lookup"><span data-stu-id="41c75-842"><span id="ERROR_CLUSTER_INVALID_IPV6_TUNNEL_NETWORK"></span><span id="error_cluster_invalid_ipv6_tunnel_network"></span>**ERROR\_CLUSTER\_INVALID\_IPV6\_TUNNEL\_NETWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-843">5927 (0x1727)</span><span class="sxs-lookup"><span data-stu-id="41c75-843">5927 (0x1727)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-844">La red de clústeres no es válida para un recurso de túnel IPv6.</span><span class="sxs-lookup"><span data-stu-id="41c75-844">The cluster network is not valid for an IPv6 Tunnel resource.</span></span> <span data-ttu-id="41c75-845">Compruebe la configuración del recurso de dirección IP del que depende el recurso de túnel IPv6.</span><span class="sxs-lookup"><span data-stu-id="41c75-845">Check the configuration of the IP Address resource on which the IPv6 Tunnel resource depends.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-846"><span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**\_cuórum \_ de error no \_ permitido \_ en \_ este \_ Grupo**</span><span class="sxs-lookup"><span data-stu-id="41c75-846"><span id="ERROR_QUORUM_NOT_ALLOWED_IN_THIS_GROUP"></span><span id="error_quorum_not_allowed_in_this_group"></span>**ERROR\_QUORUM\_NOT\_ALLOWED\_IN\_THIS\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-847">5928 (0x1728)</span><span class="sxs-lookup"><span data-stu-id="41c75-847">5928 (0x1728)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-848">El recurso de cuórum no puede residir en el grupo de almacenamiento disponible.</span><span class="sxs-lookup"><span data-stu-id="41c75-848">Quorum resource cannot reside in the Available Storage group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-849"><span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**\_árbol de dependencias de error \_ \_ demasiado \_ complejo**</span><span class="sxs-lookup"><span data-stu-id="41c75-849"><span id="ERROR_DEPENDENCY_TREE_TOO_COMPLEX"></span><span id="error_dependency_tree_too_complex"></span>**ERROR\_DEPENDENCY\_TREE\_TOO\_COMPLEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-850">5929 (0x1729)</span><span class="sxs-lookup"><span data-stu-id="41c75-850">5929 (0x1729)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-851">Las dependencias de este recurso están demasiado anidadas.</span><span class="sxs-lookup"><span data-stu-id="41c75-851">The dependencies for this resource are nested too deeply.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-852"><span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**\_excepción \_ de error en la \_ llamada de recurso \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-852"><span id="ERROR_EXCEPTION_IN_RESOURCE_CALL"></span><span id="error_exception_in_resource_call"></span>**ERROR\_EXCEPTION\_IN\_RESOURCE\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-853">5930 (0x172A)</span><span class="sxs-lookup"><span data-stu-id="41c75-853">5930 (0x172A)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-854">La llamada a la DLL de recursos produjo una excepción no controlada.</span><span class="sxs-lookup"><span data-stu-id="41c75-854">The call into the resource DLL raised an unhandled exception.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-855"><span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**ERROR \_ de \_ \_ inicialización de RHS del clúster de errores \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-855"><span id="ERROR_CLUSTER_RHS_FAILED_INITIALIZATION"></span><span id="error_cluster_rhs_failed_initialization"></span>**ERROR\_CLUSTER\_RHS\_FAILED\_INITIALIZATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-856">5931 (0x172B)</span><span class="sxs-lookup"><span data-stu-id="41c75-856">5931 (0x172B)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-857">No se pudo inicializar el proceso RHS.</span><span class="sxs-lookup"><span data-stu-id="41c75-857">The RHS process failed to initialize.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-858"><span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**clúster de errores \_ \_ no \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="41c75-858"><span id="ERROR_CLUSTER_NOT_INSTALLED"></span><span id="error_cluster_not_installed"></span>**ERROR\_CLUSTER\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-859">5932 (0x172C)</span><span class="sxs-lookup"><span data-stu-id="41c75-859">5932 (0x172C)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-860">La característica de clúster de conmutación por error no está instalada en este nodo.</span><span class="sxs-lookup"><span data-stu-id="41c75-860">The Failover Clustering feature is not installed on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-861"><span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**\_ \_ los recursos \_ de clúster de error deben estar en \_ \_ línea \_ en \_ el \_ mismo \_ nodo**</span><span class="sxs-lookup"><span data-stu-id="41c75-861"><span id="ERROR_CLUSTER_RESOURCES_MUST_BE_ONLINE_ON_THE_SAME_NODE"></span><span id="error_cluster_resources_must_be_online_on_the_same_node"></span>**ERROR\_CLUSTER\_RESOURCES\_MUST\_BE\_ONLINE\_ON\_THE\_SAME\_NODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-862">5933 (0x172D)</span><span class="sxs-lookup"><span data-stu-id="41c75-862">5933 (0x172D)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-863">Los recursos deben estar en línea en el mismo nodo para esta operación.</span><span class="sxs-lookup"><span data-stu-id="41c75-863">The resources must be online on the same node for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-864"><span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**\_ \_ número máximo \_ de nodos \_ de clúster de errores en el \_ clúster**</span><span class="sxs-lookup"><span data-stu-id="41c75-864"><span id="ERROR_CLUSTER_MAX_NODES_IN_CLUSTER"></span><span id="error_cluster_max_nodes_in_cluster"></span>**ERROR\_CLUSTER\_MAX\_NODES\_IN\_CLUSTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-865">5934 (0x172E)</span><span class="sxs-lookup"><span data-stu-id="41c75-865">5934 (0x172E)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-866">No se puede Agregar un nuevo nodo porque este clúster ya tiene el número máximo de nodos.</span><span class="sxs-lookup"><span data-stu-id="41c75-866">A new node can not be added since this cluster is already at its maximum number of nodes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-867"><span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**ERROR en el \_ clúster de \_ demasiados \_ \_ nodos**</span><span class="sxs-lookup"><span data-stu-id="41c75-867"><span id="ERROR_CLUSTER_TOO_MANY_NODES"></span><span id="error_cluster_too_many_nodes"></span>**ERROR\_CLUSTER\_TOO\_MANY\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-868">5935 (0x172F)</span><span class="sxs-lookup"><span data-stu-id="41c75-868">5935 (0x172F)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-869">Este clúster no se puede crear porque el número de nodos especificado supera el límite máximo permitido.</span><span class="sxs-lookup"><span data-stu-id="41c75-869">This cluster can not be created since the specified number of nodes exceeds the maximum allowed limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-870"><span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**el \_ objeto de clúster de error \_ \_ ya está en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="41c75-870"><span id="ERROR_CLUSTER_OBJECT_ALREADY_USED"></span><span id="error_cluster_object_already_used"></span>**ERROR\_CLUSTER\_OBJECT\_ALREADY\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-871">5936 (0x1730)</span><span class="sxs-lookup"><span data-stu-id="41c75-871">5936 (0x1730)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-872">Error al tratar de usar el nombre de clúster especificado porque ya existe un objeto de equipo habilitado con el nombre especificado en el dominio.</span><span class="sxs-lookup"><span data-stu-id="41c75-872">An attempt to use the specified cluster name failed because an enabled computer object with the given name already exists in the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-873"><span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**ERROR al \_ \_ Buscar grupos \_ no principales**</span><span class="sxs-lookup"><span data-stu-id="41c75-873"><span id="ERROR_NONCORE_GROUPS_FOUND"></span><span id="error_noncore_groups_found"></span>**ERROR\_NONCORE\_GROUPS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-874">5937 (0x1731)</span><span class="sxs-lookup"><span data-stu-id="41c75-874">5937 (0x1731)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-875">No se puede destruir este clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-875">This cluster cannot be destroyed.</span></span> <span data-ttu-id="41c75-876">Tiene grupos de aplicaciones no principales que deben eliminarse antes de que se pueda destruir el clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-876">It has non-core application groups which must be deleted before the cluster can be destroyed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-877"><span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**conflicto de recursos de recurso \_ compartido de archivos de error \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-877"><span id="ERROR_FILE_SHARE_RESOURCE_CONFLICT"></span><span id="error_file_share_resource_conflict"></span>**ERROR\_FILE\_SHARE\_RESOURCE\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-878">5938 (0x1732)</span><span class="sxs-lookup"><span data-stu-id="41c75-878">5938 (0x1732)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-879">No se puede hospedar el recurso compartido de archivos asociado al recurso de testigo del recurso compartido de archivos en este clúster ni en ninguno de sus nodos.</span><span class="sxs-lookup"><span data-stu-id="41c75-879">File share associated with file share witness resource cannot be hosted by this cluster or any of its nodes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-880"><span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**ERROR \_ al \_ desalojar el clúster de la \_ solicitud no válida \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-880"><span id="ERROR_CLUSTER_EVICT_INVALID_REQUEST"></span><span id="error_cluster_evict_invalid_request"></span>**ERROR\_CLUSTER\_EVICT\_INVALID\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-881">5939 (0x1733)</span><span class="sxs-lookup"><span data-stu-id="41c75-881">5939 (0x1733)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-882">La expulsión de este nodo no es válida en este momento.</span><span class="sxs-lookup"><span data-stu-id="41c75-882">Eviction of this node is invalid at this time.</span></span> <span data-ttu-id="41c75-883">Debido a los requisitos de quórum, la expulsión de nodo producirá el cierre del clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-883">Due to quorum requirements node eviction will result in cluster shutdown.</span></span> <span data-ttu-id="41c75-884">Si es el último nodo del clúster, se debe usar el comando destruir clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-884">If it is the last node in the cluster, destroy cluster command should be used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-885"><span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**\_ \_ recurso singleton de clúster de errores \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-885"><span id="ERROR_CLUSTER_SINGLETON_RESOURCE"></span><span id="error_cluster_singleton_resource"></span>**ERROR\_CLUSTER\_SINGLETON\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-886">5940 (0x1734)</span><span class="sxs-lookup"><span data-stu-id="41c75-886">5940 (0x1734)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-887">Solo se permite una instancia de este tipo de recurso en el clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-887">Only one instance of this resource type is allowed in the cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-888"><span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**\_ \_ recurso singleton de grupo de clústeres de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-888"><span id="ERROR_CLUSTER_GROUP_SINGLETON_RESOURCE"></span><span id="error_cluster_group_singleton_resource"></span>**ERROR\_CLUSTER\_GROUP\_SINGLETON\_RESOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-889">5941 (0x1735)</span><span class="sxs-lookup"><span data-stu-id="41c75-889">5941 (0x1735)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-890">Solo se permite una instancia de este tipo de recurso por grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="41c75-890">Only one instance of this resource type is allowed per resource group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-891"><span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**ERROR en el \_ proveedor de recursos del clúster \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-891"><span id="ERROR_CLUSTER_RESOURCE_PROVIDER_FAILED"></span><span id="error_cluster_resource_provider_failed"></span>**ERROR\_CLUSTER\_RESOURCE\_PROVIDER\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-892">5942 (0x1736)</span><span class="sxs-lookup"><span data-stu-id="41c75-892">5942 (0x1736)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-893">El recurso no pudo conectarse debido a un error de uno o varios recursos del proveedor.</span><span class="sxs-lookup"><span data-stu-id="41c75-893">The resource failed to come online due to the failure of one or more provider resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-894"><span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**error \_ de \_ configuración de recursos de clúster \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-894"><span id="ERROR_CLUSTER_RESOURCE_CONFIGURATION_ERROR"></span><span id="error_cluster_resource_configuration_error"></span>**ERROR\_CLUSTER\_RESOURCE\_CONFIGURATION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-895">5943 (0x1737)</span><span class="sxs-lookup"><span data-stu-id="41c75-895">5943 (0x1737)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-896">El recurso ha indicado que no puede conectarse en ningún nodo.</span><span class="sxs-lookup"><span data-stu-id="41c75-896">The resource has indicated that it cannot come online on any node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-897"><span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**\_grupo de clústeres de errores \_ \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="41c75-897"><span id="ERROR_CLUSTER_GROUP_BUSY"></span><span id="error_cluster_group_busy"></span>**ERROR\_CLUSTER\_GROUP\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-898">5944 (0x1738)</span><span class="sxs-lookup"><span data-stu-id="41c75-898">5944 (0x1738)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-899">La operación actual no se puede realizar en este grupo en este momento.</span><span class="sxs-lookup"><span data-stu-id="41c75-899">The current operation cannot be performed on this group at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-900"><span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**\_volumen de clúster \_ no \_ compartido \_ de errores**</span><span class="sxs-lookup"><span data-stu-id="41c75-900"><span id="ERROR_CLUSTER_NOT_SHARED_VOLUME"></span><span id="error_cluster_not_shared_volume"></span>**ERROR\_CLUSTER\_NOT\_SHARED\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-901">5945 (0x1739)</span><span class="sxs-lookup"><span data-stu-id="41c75-901">5945 (0x1739)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-902">El directorio o el archivo no se encuentra en un volumen compartido de clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-902">The directory or file is not located on a cluster shared volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-903"><span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**ERROR \_ de \_ \_ descriptor de seguridad no válido del clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-903"><span id="ERROR_CLUSTER_INVALID_SECURITY_DESCRIPTOR"></span><span id="error_cluster_invalid_security_descriptor"></span>**ERROR\_CLUSTER\_INVALID\_SECURITY\_DESCRIPTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-904">5946 (0x173A)</span><span class="sxs-lookup"><span data-stu-id="41c75-904">5946 (0x173A)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-905">El descriptor de seguridad no cumple los requisitos de un clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-905">The Security Descriptor does not meet the requirements for a cluster.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-906"><span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**\_ \_ volúmenes compartidos \_ de clúster de error \_ en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="41c75-906"><span id="ERROR_CLUSTER_SHARED_VOLUMES_IN_USE"></span><span id="error_cluster_shared_volumes_in_use"></span>**ERROR\_CLUSTER\_SHARED\_VOLUMES\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-907">5947 (0x173B)</span><span class="sxs-lookup"><span data-stu-id="41c75-907">5947 (0x173B)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-908">Hay uno o varios recursos de volúmenes compartidos configurados en el clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-908">There is one or more shared volumes resources configured in the cluster.</span></span> <span data-ttu-id="41c75-909">Esos recursos se deben migrar al almacenamiento disponible para que la operación se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="41c75-909">Those resources must be moved to available storage in order for operation to succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-910"><span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**ERROR en el \_ clúster de \_ uso de \_ volúmenes compartidos \_ \_ API**</span><span class="sxs-lookup"><span data-stu-id="41c75-910"><span id="ERROR_CLUSTER_USE_SHARED_VOLUMES_API"></span><span id="error_cluster_use_shared_volumes_api"></span>**ERROR\_CLUSTER\_USE\_SHARED\_VOLUMES\_API**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-911">5948 (0x173C)</span><span class="sxs-lookup"><span data-stu-id="41c75-911">5948 (0x173C)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-912">No se puede manipular directamente este grupo o recurso.</span><span class="sxs-lookup"><span data-stu-id="41c75-912">This group or resource cannot be directly manipulated.</span></span> <span data-ttu-id="41c75-913">Use las API de volumen compartido para realizar la operación deseada.</span><span class="sxs-lookup"><span data-stu-id="41c75-913">Use shared volume APIs to perform desired operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-914"><span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**ERROR \_ \_ de copia \_ de seguridad de clúster en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="41c75-914"><span id="ERROR_CLUSTER_BACKUP_IN_PROGRESS"></span><span id="error_cluster_backup_in_progress"></span>**ERROR\_CLUSTER\_BACKUP\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-915">5949 (0x173D)</span><span class="sxs-lookup"><span data-stu-id="41c75-915">5949 (0x173D)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-916">La copia de seguridad está en curso.</span><span class="sxs-lookup"><span data-stu-id="41c75-916">Back up is in progress.</span></span> <span data-ttu-id="41c75-917">Espere a que finalice la copia de seguridad antes de volver a intentar esta operación.</span><span class="sxs-lookup"><span data-stu-id="41c75-917">Please wait for backup completion before trying this operation again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-918"><span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**ERROR \_ de \_ ruta de acceso no CSV \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-918"><span id="ERROR_NON_CSV_PATH"></span><span id="error_non_csv_path"></span>**ERROR\_NON\_CSV\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-919">5950 (0x173E)</span><span class="sxs-lookup"><span data-stu-id="41c75-919">5950 (0x173E)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-920">La ruta de acceso no pertenece a un volumen compartido de clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-920">The path does not belong to a cluster shared volume.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-921"><span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**ERROR en el \_ \_ volumen CSV \_ no \_ local**</span><span class="sxs-lookup"><span data-stu-id="41c75-921"><span id="ERROR_CSV_VOLUME_NOT_LOCAL"></span><span id="error_csv_volume_not_local"></span>**ERROR\_CSV\_VOLUME\_NOT\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-922">5951 (0x173F)</span><span class="sxs-lookup"><span data-stu-id="41c75-922">5951 (0x173F)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-923">El volumen compartido de clúster no está montado localmente en este nodo.</span><span class="sxs-lookup"><span data-stu-id="41c75-923">The cluster shared volume is not locally mounted on this node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-924"><span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**ERROR de \_ guardián del clúster de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-924"><span id="ERROR_CLUSTER_WATCHDOG_TERMINATING"></span><span id="error_cluster_watchdog_terminating"></span>**ERROR\_CLUSTER\_WATCHDOG\_TERMINATING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-925">5952 (0x1740)</span><span class="sxs-lookup"><span data-stu-id="41c75-925">5952 (0x1740)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-926">El guardián del clúster está finalizando.</span><span class="sxs-lookup"><span data-stu-id="41c75-926">The cluster watchdog is terminating.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-927"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**el \_ recurso de clúster de error \_ \_ \_ Desplace los \_ nodos incompatibles \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-927"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_INCOMPATIBLE_NODES"></span><span id="error_cluster_resource_vetoed_move_incompatible_nodes"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_INCOMPATIBLE\_NODES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-928">5953 (0x1741)</span><span class="sxs-lookup"><span data-stu-id="41c75-928">5953 (0x1741)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-929">Un recurso veta un movimiento entre dos nodos porque no son compatibles.</span><span class="sxs-lookup"><span data-stu-id="41c75-929">A resource vetoed a move between two nodes because they are incompatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-930"><span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**\_peso de \_ nodo no válido de clúster \_ de errores \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-930"><span id="ERROR_CLUSTER_INVALID_NODE_WEIGHT"></span><span id="error_cluster_invalid_node_weight"></span>**ERROR\_CLUSTER\_INVALID\_NODE\_WEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-931">5954 (0x1742)</span><span class="sxs-lookup"><span data-stu-id="41c75-931">5954 (0x1742)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-932">La solicitud no es válida porque no se puede cambiar el peso del nodo mientras el clúster está en modo de cuórum solo de disco, o porque el cambio de peso del nodo infringiría los requisitos mínimos de cuórum de clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-932">The request is invalid either because node weight cannot be changed while the cluster is in disk-only quorum mode, or because changing the node weight would violate the minimum cluster quorum requirements.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-933"><span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**ERROR en la \_ \_ \_ llamada vetada a recursos del clúster \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-933"><span id="ERROR_CLUSTER_RESOURCE_VETOED_CALL"></span><span id="error_cluster_resource_vetoed_call"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_CALL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-934">5955 (0x1743)</span><span class="sxs-lookup"><span data-stu-id="41c75-934">5955 (0x1743)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-935">El recurso vetó la llamada.</span><span class="sxs-lookup"><span data-stu-id="41c75-935">The resource vetoed the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-936"><span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**ERROR \_ RESMON \_ recursos del sistema que \_ \_ faltan**</span><span class="sxs-lookup"><span data-stu-id="41c75-936"><span id="ERROR_RESMON_SYSTEM_RESOURCES_LACKING"></span><span id="error_resmon_system_resources_lacking"></span>**ERROR\_RESMON\_SYSTEM\_RESOURCES\_LACKING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-937">5956 (0x1744)</span><span class="sxs-lookup"><span data-stu-id="41c75-937">5956 (0x1744)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-938">No se pudo iniciar o ejecutar el recurso porque no pudo reservar suficientes recursos del sistema.</span><span class="sxs-lookup"><span data-stu-id="41c75-938">Resource could not start or run because it could not reserve sufficient system resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-939"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**el \_ recurso de clúster de error \_ \_ \_ \_ no ha movido \_ suficientes \_ recursos \_ en el \_ destino**</span><span class="sxs-lookup"><span data-stu-id="41c75-939"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_DESTINATION"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_destination"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_NOT\_ENOUGH\_RESOURCES\_ON\_DESTINATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-940">5957 (0x1745)</span><span class="sxs-lookup"><span data-stu-id="41c75-940">5957 (0x1745)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-941">Un recurso veta un movimiento entre dos nodos porque el destino no tiene recursos suficientes para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="41c75-941">A resource vetoed a move between two nodes because the destination currently does not have enough resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-942"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**el \_ recurso de clúster de error \_ \_ \_ \_ no ha movido \_ suficientes \_ recursos \_ en el \_ origen**</span><span class="sxs-lookup"><span data-stu-id="41c75-942"><span id="ERROR_CLUSTER_RESOURCE_VETOED_MOVE_NOT_ENOUGH_RESOURCES_ON_SOURCE"></span><span id="error_cluster_resource_vetoed_move_not_enough_resources_on_source"></span>**ERROR\_CLUSTER\_RESOURCE\_VETOED\_MOVE\_NOT\_ENOUGH\_RESOURCES\_ON\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-943">5958 (0x1746)</span><span class="sxs-lookup"><span data-stu-id="41c75-943">5958 (0x1746)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-944">Un recurso veta un movimiento entre dos nodos porque el origen no tiene recursos suficientes para completar la operación.</span><span class="sxs-lookup"><span data-stu-id="41c75-944">A resource vetoed a move between two nodes because the source currently does not have enough resources to complete the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-945"><span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**ERROR \_ en el grupo de clústeres \_ \_ en cola**</span><span class="sxs-lookup"><span data-stu-id="41c75-945"><span id="ERROR_CLUSTER_GROUP_QUEUED"></span><span id="error_cluster_group_queued"></span>**ERROR\_CLUSTER\_GROUP\_QUEUED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-946">5959 (0x1747)</span><span class="sxs-lookup"><span data-stu-id="41c75-946">5959 (0x1747)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-947">No se puede completar la operación solicitada porque el grupo está en cola para una operación.</span><span class="sxs-lookup"><span data-stu-id="41c75-947">The requested operation can not be completed because the group is queued for an operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-948"><span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**ERROR \_ de \_ Estado de recurso de clúster \_ bloqueado \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-948"><span id="ERROR_CLUSTER_RESOURCE_LOCKED_STATUS"></span><span id="error_cluster_resource_locked_status"></span>**ERROR\_CLUSTER\_RESOURCE\_LOCKED\_STATUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-949">5960 (0x1748)</span><span class="sxs-lookup"><span data-stu-id="41c75-949">5960 (0x1748)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-950">No se puede completar la operación solicitada porque un recurso tiene el estado bloqueado.</span><span class="sxs-lookup"><span data-stu-id="41c75-950">The requested operation can not be completed because a resource has locked status.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-951"><span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**ERROR \_ de \_ conmutación por error de volumen compartido de clúster \_ \_ \_ no \_ permitida**</span><span class="sxs-lookup"><span data-stu-id="41c75-951"><span id="ERROR_CLUSTER_SHARED_VOLUME_FAILOVER_NOT_ALLOWED"></span><span id="error_cluster_shared_volume_failover_not_allowed"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_FAILOVER\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-952">5961 (0x1749)</span><span class="sxs-lookup"><span data-stu-id="41c75-952">5961 (0x1749)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-953">El recurso no se puede trasladar a otro nodo porque un volumen compartido del clúster ha vetado la operación.</span><span class="sxs-lookup"><span data-stu-id="41c75-953">The resource cannot move to another node because a cluster shared volume vetoed the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-954"><span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**ERROR \_ \_ \_ \_ de purga de nodo de clúster en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="41c75-954"><span id="ERROR_CLUSTER_NODE_DRAIN_IN_PROGRESS"></span><span id="error_cluster_node_drain_in_progress"></span>**ERROR\_CLUSTER\_NODE\_DRAIN\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-955">5962 (0x174A)</span><span class="sxs-lookup"><span data-stu-id="41c75-955">5962 (0x174A)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-956">Ya hay una purga de nodo en curso.</span><span class="sxs-lookup"><span data-stu-id="41c75-956">A node drain is already in progress.</span></span>

<span data-ttu-id="41c75-957">Este valor también se denomina **la \_ \_ \_ evacuación del nodo \_ de clúster de error en \_ curso** .</span><span class="sxs-lookup"><span data-stu-id="41c75-957">This value was also named **ERROR\_CLUSTER\_NODE\_EVACUATION\_IN\_PROGRESS**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-958"><span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**ERROR \_ de \_ disco de clúster \_ no \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="41c75-958"><span id="ERROR_CLUSTER_DISK_NOT_CONNECTED"></span><span id="error_cluster_disk_not_connected"></span>**ERROR\_CLUSTER\_DISK\_NOT\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-959">5963 (0x174B)</span><span class="sxs-lookup"><span data-stu-id="41c75-959">5963 (0x174B)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-960">El almacenamiento en clúster no está conectado al nodo.</span><span class="sxs-lookup"><span data-stu-id="41c75-960">Clustered storage is not connected to the node.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-961"><span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**ERROR \_ de \_ disco \_ no \_ compatible con CSV**</span><span class="sxs-lookup"><span data-stu-id="41c75-961"><span id="ERROR_DISK_NOT_CSV_CAPABLE"></span><span id="error_disk_not_csv_capable"></span>**ERROR\_DISK\_NOT\_CSV\_CAPABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-962">5964 (0x174C)</span><span class="sxs-lookup"><span data-stu-id="41c75-962">5964 (0x174C)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-963">El disco no está configurado de forma que se pueda usar con CSV.</span><span class="sxs-lookup"><span data-stu-id="41c75-963">The disk is not configured in a way to be used with CSV.</span></span> <span data-ttu-id="41c75-964">Los discos CSV deben tener al menos una partición con formato NTFS.</span><span class="sxs-lookup"><span data-stu-id="41c75-964">CSV disks must have at least one partition that is formatted with NTFS.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-965"><span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**el \_ recurso \_ de error no \_ está en el \_ \_ almacenamiento disponible**</span><span class="sxs-lookup"><span data-stu-id="41c75-965"><span id="ERROR_RESOURCE_NOT_IN_AVAILABLE_STORAGE"></span><span id="error_resource_not_in_available_storage"></span>**ERROR\_RESOURCE\_NOT\_IN\_AVAILABLE\_STORAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-966">5965 (0x174D)</span><span class="sxs-lookup"><span data-stu-id="41c75-966">5965 (0x174D)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-967">Para completar esta acción, el recurso debe ser parte del grupo de almacenamiento disponible.</span><span class="sxs-lookup"><span data-stu-id="41c75-967">The resource must be part of the Available Storage group to complete this action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-968"><span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**\_volumen compartido de clúster de errores \_ \_ \_ Redirigido**</span><span class="sxs-lookup"><span data-stu-id="41c75-968"><span id="ERROR_CLUSTER_SHARED_VOLUME_REDIRECTED"></span><span id="error_cluster_shared_volume_redirected"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-969">5966 (0x174E)</span><span class="sxs-lookup"><span data-stu-id="41c75-969">5966 (0x174E)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-970">Error de la operación CSVFS porque el volumen está en modo redirigido.</span><span class="sxs-lookup"><span data-stu-id="41c75-970">CSVFS failed operation as volume is in redirected mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-971"><span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**\_volumen compartido de clúster de error \_ \_ \_ no \_ Redirigido**</span><span class="sxs-lookup"><span data-stu-id="41c75-971"><span id="ERROR_CLUSTER_SHARED_VOLUME_NOT_REDIRECTED"></span><span id="error_cluster_shared_volume_not_redirected"></span>**ERROR\_CLUSTER\_SHARED\_VOLUME\_NOT\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-972">5967 (0x174F)</span><span class="sxs-lookup"><span data-stu-id="41c75-972">5967 (0x174F)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-973">Error de la operación CSVFS porque el volumen no está en modo redirigido.</span><span class="sxs-lookup"><span data-stu-id="41c75-973">CSVFS failed operation as volume is not in redirected mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-974"><span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**el \_ clúster de errores \_ no puede \_ devolver \_ propiedades**</span><span class="sxs-lookup"><span data-stu-id="41c75-974"><span id="ERROR_CLUSTER_CANNOT_RETURN_PROPERTIES"></span><span id="error_cluster_cannot_return_properties"></span>**ERROR\_CLUSTER\_CANNOT\_RETURN\_PROPERTIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-975">5968 (0x1750)</span><span class="sxs-lookup"><span data-stu-id="41c75-975">5968 (0x1750)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-976">No se pueden devolver propiedades de clúster en este momento.</span><span class="sxs-lookup"><span data-stu-id="41c75-976">Cluster properties cannot be returned at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-977"><span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**el \_ \_ recurso \_ de clúster de errores contiene un \_ \_ área de diferencia no compatible \_ \_ para \_ volúmenes compartidos \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-977"><span id="ERROR_CLUSTER_RESOURCE_CONTAINS_UNSUPPORTED_DIFF_AREA_FOR_SHARED_VOLUMES"></span><span id="error_cluster_resource_contains_unsupported_diff_area_for_shared_volumes"></span>**ERROR\_CLUSTER\_RESOURCE\_CONTAINS\_UNSUPPORTED\_DIFF\_AREA\_FOR\_SHARED\_VOLUMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-978">5969 (0x1751)</span><span class="sxs-lookup"><span data-stu-id="41c75-978">5969 (0x1751)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-979">El recurso de disco en clúster contiene el área de diferencia de instantáneas de software que no se admite para los volúmenes compartidos de clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-979">The clustered disk resource contains software snapshot diff area that are not supported for Cluster Shared Volumes.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-980"><span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**el \_ \_ recurso \_ de clúster de errores está \_ en \_ modo de mantenimiento \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-980"><span id="ERROR_CLUSTER_RESOURCE_IS_IN_MAINTENANCE_MODE"></span><span id="error_cluster_resource_is_in_maintenance_mode"></span>**ERROR\_CLUSTER\_RESOURCE\_IS\_IN\_MAINTENANCE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-981">5970 (0x1752)</span><span class="sxs-lookup"><span data-stu-id="41c75-981">5970 (0x1752)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-982">No se puede completar la operación porque el recurso está en modo de mantenimiento.</span><span class="sxs-lookup"><span data-stu-id="41c75-982">The operation cannot be completed because the resource is in maintenance mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-983"><span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**\_conflicto de afinidad de clústeres de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-983"><span id="ERROR_CLUSTER_AFFINITY_CONFLICT"></span><span id="error_cluster_affinity_conflict"></span>**ERROR\_CLUSTER\_AFFINITY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-984">5971 (0x1753)</span><span class="sxs-lookup"><span data-stu-id="41c75-984">5971 (0x1753)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-985">No se puede completar la operación debido a conflictos de afinidad de clúster.</span><span class="sxs-lookup"><span data-stu-id="41c75-985">The operation cannot be completed because of cluster affinity conflicts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="41c75-986"><span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**el \_ recurso de clúster de errores \_ es una \_ \_ \_ máquina virtual de réplica \_**</span><span class="sxs-lookup"><span data-stu-id="41c75-986"><span id="ERROR_CLUSTER_RESOURCE_IS_REPLICA_VIRTUAL_MACHINE"></span><span id="error_cluster_resource_is_replica_virtual_machine"></span>**ERROR\_CLUSTER\_RESOURCE\_IS\_REPLICA\_VIRTUAL\_MACHINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="41c75-987">5972 (0x1754)</span><span class="sxs-lookup"><span data-stu-id="41c75-987">5972 (0x1754)</span></span>
</dt> <dt>



<span data-ttu-id="41c75-988">No se puede completar la operación porque el recurso es una máquina virtual de réplica.</span><span class="sxs-lookup"><span data-stu-id="41c75-988">The operation cannot be completed because the resource is a replica virtual machine.</span></span>


</dt> </dl> </dd> </dl>


## <a name="requirements"></a><span data-ttu-id="41c75-989">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41c75-989">Requirements</span></span>



| <span data-ttu-id="41c75-990">Requisito</span><span class="sxs-lookup"><span data-stu-id="41c75-990">Requirement</span></span> | <span data-ttu-id="41c75-991">Value</span><span class="sxs-lookup"><span data-stu-id="41c75-991">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41c75-992">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41c75-992">Minimum supported client</span></span><br/> | <span data-ttu-id="41c75-993">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="41c75-993">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="41c75-994">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41c75-994">Minimum supported server</span></span><br/> | <span data-ttu-id="41c75-995">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="41c75-995">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41c75-996">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41c75-996">Header</span></span><br/>                   | <dl> <span data-ttu-id="41c75-997"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="41c75-997"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41c75-998">Consulte también</span><span class="sxs-lookup"><span data-stu-id="41c75-998">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41c75-999">Códigos de error del sistema</span><span class="sxs-lookup"><span data-stu-id="41c75-999">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




