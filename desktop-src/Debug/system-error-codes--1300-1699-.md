---
description: Describe los códigos de error 1300-1699 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: 7b04a2ba-7bf9-4bff-93c8-cbb0060e069d
title: Códigos de error del sistema (1300-1699) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 8fa0cbc312c8d82879322f0bc0c79533ddb961ce
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496241"
---
# <a name="system-error-codes-1300-1699"></a><span data-ttu-id="e4551-103">Códigos de error del sistema (1300-1699)</span><span class="sxs-lookup"><span data-stu-id="e4551-103">System Error Codes (1300-1699)</span></span>

> [!NOTE]
> <span data-ttu-id="e4551-104">Esta información está destinada a los desarrolladores que depuran errores del sistema.</span><span class="sxs-lookup"><span data-stu-id="e4551-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="e4551-105">En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e4551-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="e4551-106">En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) para los errores 1300 a 1699.</span><span class="sxs-lookup"><span data-stu-id="e4551-106">The following list describes [system error codes](system-error-codes.md) for errors 1300 to 1699.</span></span> <span data-ttu-id="e4551-107">La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones.</span><span class="sxs-lookup"><span data-stu-id="e4551-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="e4551-108">Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.</span><span class="sxs-lookup"><span data-stu-id="e4551-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="e4551-109"><span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**\_no se \_ \_ ha asignado ningún error**</span><span class="sxs-lookup"><span data-stu-id="e4551-109"><span id="ERROR_NOT_ALL_ASSIGNED"></span><span id="error_not_all_assigned"></span>**ERROR\_NOT\_ALL\_ASSIGNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-110">1300 (0x514)</span><span class="sxs-lookup"><span data-stu-id="e4551-110">1300 (0x514)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-111">No todos los privilegios o grupos a los que se hace referencia se asignan al autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="e4551-111">Not all privileges or groups referenced are assigned to the caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-112"><span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERROR \_ algunos \_ no \_ asignados**</span><span class="sxs-lookup"><span data-stu-id="e4551-112"><span id="ERROR_SOME_NOT_MAPPED"></span><span id="error_some_not_mapped"></span>**ERROR\_SOME\_NOT\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-113">1301 (0x515)</span><span class="sxs-lookup"><span data-stu-id="e4551-113">1301 (0x515)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-114">No se ha realizado ninguna asignación entre los nombres de cuenta y los ID. de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e4551-114">Some mapping between account names and security IDs was not done.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-115"><span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERROR: \_ no hay \_ cuotas \_ para la \_ cuenta**</span><span class="sxs-lookup"><span data-stu-id="e4551-115"><span id="ERROR_NO_QUOTAS_FOR_ACCOUNT"></span><span id="error_no_quotas_for_account"></span>**ERROR\_NO\_QUOTAS\_FOR\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-116">1302 (0x516)</span><span class="sxs-lookup"><span data-stu-id="e4551-116">1302 (0x516)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-117">No se ha establecido específicamente ningún límite de cuota del sistema para esta cuenta.</span><span class="sxs-lookup"><span data-stu-id="e4551-117">No system quota limits are specifically set for this account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-118"><span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERROR en la \_ \_ clave de sesión de usuario local \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-118"><span id="ERROR_LOCAL_USER_SESSION_KEY"></span><span id="error_local_user_session_key"></span>**ERROR\_LOCAL\_USER\_SESSION\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-119">1303 (0x517)</span><span class="sxs-lookup"><span data-stu-id="e4551-119">1303 (0x517)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-120">No hay ninguna clave de cifrado disponible.</span><span class="sxs-lookup"><span data-stu-id="e4551-120">No encryption key is available.</span></span> <span data-ttu-id="e4551-121">Se devolvió una clave de cifrado conocida.</span><span class="sxs-lookup"><span data-stu-id="e4551-121">A well-known encryption key was returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-122"><span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERROR \_ : \_ contraseña de LM nula \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-122"><span id="ERROR_NULL_LM_PASSWORD"></span><span id="error_null_lm_password"></span>**ERROR\_NULL\_LM\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-123">1304 (0x518)</span><span class="sxs-lookup"><span data-stu-id="e4551-123">1304 (0x518)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-124">La contraseña es demasiado compleja para convertirse en una contraseña de administrador de LAN.</span><span class="sxs-lookup"><span data-stu-id="e4551-124">The password is too complex to be converted to a LAN Manager password.</span></span> <span data-ttu-id="e4551-125">La contraseña del administrador de LAN devuelta es una cadena **nula** .</span><span class="sxs-lookup"><span data-stu-id="e4551-125">The LAN Manager password returned is a **NULL** string.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-126"><span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**ERROR \_ de \_ revisión desconocida**</span><span class="sxs-lookup"><span data-stu-id="e4551-126"><span id="ERROR_UNKNOWN_REVISION"></span><span id="error_unknown_revision"></span>**ERROR\_UNKNOWN\_REVISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-127">1305 (0x519)</span><span class="sxs-lookup"><span data-stu-id="e4551-127">1305 (0x519)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-128">Se desconoce el nivel de revisión.</span><span class="sxs-lookup"><span data-stu-id="e4551-128">The revision level is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-129"><span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**ERROR \_ de \_ coincidencia de revisión**</span><span class="sxs-lookup"><span data-stu-id="e4551-129"><span id="ERROR_REVISION_MISMATCH"></span><span id="error_revision_mismatch"></span>**ERROR\_REVISION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-130">1306 (0x51A)</span><span class="sxs-lookup"><span data-stu-id="e4551-130">1306 (0x51A)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-131">Indica que dos niveles de revisión son incompatibles.</span><span class="sxs-lookup"><span data-stu-id="e4551-131">Indicates two revision levels are incompatible.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-132"><span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**ERROR \_ de \_ propietario no válido**</span><span class="sxs-lookup"><span data-stu-id="e4551-132"><span id="ERROR_INVALID_OWNER"></span><span id="error_invalid_owner"></span>**ERROR\_INVALID\_OWNER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-133">1307 (0x51B)</span><span class="sxs-lookup"><span data-stu-id="e4551-133">1307 (0x51B)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-134">No se puede asignar este identificador de seguridad como propietario de este objeto.</span><span class="sxs-lookup"><span data-stu-id="e4551-134">This security ID may not be assigned as the owner of this object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-135"><span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERROR \_ de \_ grupo principal no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-135"><span id="ERROR_INVALID_PRIMARY_GROUP"></span><span id="error_invalid_primary_group"></span>**ERROR\_INVALID\_PRIMARY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-136">1308 (0x51C)</span><span class="sxs-lookup"><span data-stu-id="e4551-136">1308 (0x51C)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-137">Este identificador de seguridad no se puede asignar como el grupo principal de un objeto.</span><span class="sxs-lookup"><span data-stu-id="e4551-137">This security ID may not be assigned as the primary group of an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-138"><span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERROR: \_ no hay \_ token de suplantación \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-138"><span id="ERROR_NO_IMPERSONATION_TOKEN"></span><span id="error_no_impersonation_token"></span>**ERROR\_NO\_IMPERSONATION\_TOKEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-139">1309 (0x51D)</span><span class="sxs-lookup"><span data-stu-id="e4551-139">1309 (0x51D)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-140">Se ha intentado realizar una operación en un token de suplantación por parte de un subproceso que actualmente no suplanta a un cliente.</span><span class="sxs-lookup"><span data-stu-id="e4551-140">An attempt has been made to operate on an impersonation token by a thread that is not currently impersonating a client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-141"><span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERROR no se pudo \_ \_ deshabilitar \_ obligatorio**</span><span class="sxs-lookup"><span data-stu-id="e4551-141"><span id="ERROR_CANT_DISABLE_MANDATORY"></span><span id="error_cant_disable_mandatory"></span>**ERROR\_CANT\_DISABLE\_MANDATORY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-142">1310 (0x51E)</span><span class="sxs-lookup"><span data-stu-id="e4551-142">1310 (0x51E)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-143">Es posible que el grupo no esté deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="e4551-143">The group may not be disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-144"><span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERROR: \_ no hay \_ servidores de inicio de sesión \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-144"><span id="ERROR_NO_LOGON_SERVERS"></span><span id="error_no_logon_servers"></span>**ERROR\_NO\_LOGON\_SERVERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-145">1311 (0x51F)</span><span class="sxs-lookup"><span data-stu-id="e4551-145">1311 (0x51F)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-146">Actualmente no hay ningún servidor de inicio de sesión disponible para atender la solicitud de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e4551-146">There are currently no logon servers available to service the logon request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-147"><span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERROR no se ha podido \_ \_ \_ iniciar \_ sesión**</span><span class="sxs-lookup"><span data-stu-id="e4551-147"><span id="ERROR_NO_SUCH_LOGON_SESSION"></span><span id="error_no_such_logon_session"></span>**ERROR\_NO\_SUCH\_LOGON\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-148">1312 (0x520)</span><span class="sxs-lookup"><span data-stu-id="e4551-148">1312 (0x520)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-149">Una sesión de inicio especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="e4551-149">A specified logon session does not exist.</span></span> <span data-ttu-id="e4551-150">Es posible que ya se haya terminado.</span><span class="sxs-lookup"><span data-stu-id="e4551-150">It may already have been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-151"><span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**NO se ha podido obtener \_ \_ dicho \_ privilegio**</span><span class="sxs-lookup"><span data-stu-id="e4551-151"><span id="ERROR_NO_SUCH_PRIVILEGE"></span><span id="error_no_such_privilege"></span>**ERROR\_NO\_SUCH\_PRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-152">1313 (0x521)</span><span class="sxs-lookup"><span data-stu-id="e4551-152">1313 (0x521)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-153">No existe un privilegio especificado.</span><span class="sxs-lookup"><span data-stu-id="e4551-153">A specified privilege does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-154"><span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**\_no se \_ \_ mantiene el privilegio de error**</span><span class="sxs-lookup"><span data-stu-id="e4551-154"><span id="ERROR_PRIVILEGE_NOT_HELD"></span><span id="error_privilege_not_held"></span>**ERROR\_PRIVILEGE\_NOT\_HELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-155">1314 (0x522)</span><span class="sxs-lookup"><span data-stu-id="e4551-155">1314 (0x522)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-156">El cliente no dispone de un privilegio requerido.</span><span class="sxs-lookup"><span data-stu-id="e4551-156">A required privilege is not held by the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-157"><span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**ERROR \_ de \_ nombre de cuenta no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-157"><span id="ERROR_INVALID_ACCOUNT_NAME"></span><span id="error_invalid_account_name"></span>**ERROR\_INVALID\_ACCOUNT\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-158">1315 (0x523)</span><span class="sxs-lookup"><span data-stu-id="e4551-158">1315 (0x523)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-159">El nombre proporcionado no es un nombre de cuenta formado correctamente.</span><span class="sxs-lookup"><span data-stu-id="e4551-159">The name provided is not a properly formed account name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-160"><span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**existe un ERROR de \_ usuario \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-160"><span id="ERROR_USER_EXISTS"></span><span id="error_user_exists"></span>**ERROR\_USER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-161">1316 (0x524)</span><span class="sxs-lookup"><span data-stu-id="e4551-161">1316 (0x524)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-162">La cuenta especificada ya existe.</span><span class="sxs-lookup"><span data-stu-id="e4551-162">The specified account already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-163"><span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**NO se ha podido \_ \_ este \_ usuario**</span><span class="sxs-lookup"><span data-stu-id="e4551-163"><span id="ERROR_NO_SUCH_USER"></span><span id="error_no_such_user"></span>**ERROR\_NO\_SUCH\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-164">1317 (0x525)</span><span class="sxs-lookup"><span data-stu-id="e4551-164">1317 (0x525)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-165">La cuenta especificada no existe.</span><span class="sxs-lookup"><span data-stu-id="e4551-165">The specified account does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-166"><span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**\_existe un grupo de errores \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-166"><span id="ERROR_GROUP_EXISTS"></span><span id="error_group_exists"></span>**ERROR\_GROUP\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-167">1318 (0x526)</span><span class="sxs-lookup"><span data-stu-id="e4551-167">1318 (0x526)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-168">El grupo especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="e4551-168">The specified group already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-169"><span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**NO se ha podido \_ \_ este \_ Grupo**</span><span class="sxs-lookup"><span data-stu-id="e4551-169"><span id="ERROR_NO_SUCH_GROUP"></span><span id="error_no_such_group"></span>**ERROR\_NO\_SUCH\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-170">1319 (0x527)</span><span class="sxs-lookup"><span data-stu-id="e4551-170">1319 (0x527)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-171">El grupo especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="e4551-171">The specified group does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-172"><span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**\_miembro \_ de error en \_ Grupo**</span><span class="sxs-lookup"><span data-stu-id="e4551-172"><span id="ERROR_MEMBER_IN_GROUP"></span><span id="error_member_in_group"></span>**ERROR\_MEMBER\_IN\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-173">1320 (0x528)</span><span class="sxs-lookup"><span data-stu-id="e4551-173">1320 (0x528)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-174">O bien la cuenta de usuario especificada ya es miembro del grupo especificado o el grupo especificado no se puede eliminar porque contiene un miembro.</span><span class="sxs-lookup"><span data-stu-id="e4551-174">Either the specified user account is already a member of the specified group, or the specified group cannot be deleted because it contains a member.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-175"><span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**el \_ miembro \_ de error no está \_ en el \_ Grupo**</span><span class="sxs-lookup"><span data-stu-id="e4551-175"><span id="ERROR_MEMBER_NOT_IN_GROUP"></span><span id="error_member_not_in_group"></span>**ERROR\_MEMBER\_NOT\_IN\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-176">1321 (0x529)</span><span class="sxs-lookup"><span data-stu-id="e4551-176">1321 (0x529)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-177">La cuenta de usuario especificada no es miembro de la cuenta de grupo especificada.</span><span class="sxs-lookup"><span data-stu-id="e4551-177">The specified user account is not a member of the specified group account.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-178"><span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**último ERROR de \_ \_ Administrador**</span><span class="sxs-lookup"><span data-stu-id="e4551-178"><span id="ERROR_LAST_ADMIN"></span><span id="error_last_admin"></span>**ERROR\_LAST\_ADMIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-179">1322 (0x52A)</span><span class="sxs-lookup"><span data-stu-id="e4551-179">1322 (0x52A)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-180">Esta operación no está permitida, ya que podría dar lugar a que se deshabilitara, eliminara o no se pudiera iniciar sesión en una cuenta de administración.</span><span class="sxs-lookup"><span data-stu-id="e4551-180">This operation is disallowed as it could result in an administration account being disabled, deleted or unable to log on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-181"><span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ERROR \_ de \_ contraseña incorrecta**</span><span class="sxs-lookup"><span data-stu-id="e4551-181"><span id="ERROR_WRONG_PASSWORD"></span><span id="error_wrong_password"></span>**ERROR\_WRONG\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-182">1323 (0x52B)</span><span class="sxs-lookup"><span data-stu-id="e4551-182">1323 (0x52B)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-183">No se puede actualizar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="e4551-183">Unable to update the password.</span></span> <span data-ttu-id="e4551-184">El valor proporcionado como contraseña actual no es correcto.</span><span class="sxs-lookup"><span data-stu-id="e4551-184">The value provided as the current password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-185"><span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ERROR \_ de \_ contraseña con formato incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-185"><span id="ERROR_ILL_FORMED_PASSWORD"></span><span id="error_ill_formed_password"></span>**ERROR\_ILL\_FORMED\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-186">1324 (0x52C)</span><span class="sxs-lookup"><span data-stu-id="e4551-186">1324 (0x52C)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-187">No se puede actualizar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="e4551-187">Unable to update the password.</span></span> <span data-ttu-id="e4551-188">El valor proporcionado para la nueva contraseña contiene valores que no se permiten en las contraseñas.</span><span class="sxs-lookup"><span data-stu-id="e4551-188">The value provided for the new password contains values that are not allowed in passwords.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-189"><span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**\_restricción de contraseña de error \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-189"><span id="ERROR_PASSWORD_RESTRICTION"></span><span id="error_password_restriction"></span>**ERROR\_PASSWORD\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-190">1325 (0x52D)</span><span class="sxs-lookup"><span data-stu-id="e4551-190">1325 (0x52D)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-191">No se puede actualizar la contraseña.</span><span class="sxs-lookup"><span data-stu-id="e4551-191">Unable to update the password.</span></span> <span data-ttu-id="e4551-192">El valor proporcionado para la nueva contraseña no cumple los requisitos de longitud, complejidad o historial del dominio.</span><span class="sxs-lookup"><span data-stu-id="e4551-192">The value provided for the new password does not meet the length, complexity, or history requirements of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-193"><span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**ERROR de \_ Inicio de sesión \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-193"><span id="ERROR_LOGON_FAILURE"></span><span id="error_logon_failure"></span>**ERROR\_LOGON\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-194">1326 (0x52E)</span><span class="sxs-lookup"><span data-stu-id="e4551-194">1326 (0x52E)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-195">El nombre de usuario o la contraseña son incorrectos.</span><span class="sxs-lookup"><span data-stu-id="e4551-195">The user name or password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-196"><span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**\_restricción de cuenta de error \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-196"><span id="ERROR_ACCOUNT_RESTRICTION"></span><span id="error_account_restriction"></span>**ERROR\_ACCOUNT\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-197">1327 (0x52F)</span><span class="sxs-lookup"><span data-stu-id="e4551-197">1327 (0x52F)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-198">Las restricciones de cuenta impiden que este usuario inicie sesión.</span><span class="sxs-lookup"><span data-stu-id="e4551-198">Account restrictions are preventing this user from signing in.</span></span> <span data-ttu-id="e4551-199">Por ejemplo: no se permiten contraseñas en blanco, las horas de inicio de sesión están limitadas o se ha aplicado una restricción de directiva.</span><span class="sxs-lookup"><span data-stu-id="e4551-199">For example: blank passwords aren't allowed, sign-in times are limited, or a policy restriction has been enforced.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-200"><span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**ERROR de \_ horas de inicio de sesión no válidas \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-200"><span id="ERROR_INVALID_LOGON_HOURS"></span><span id="error_invalid_logon_hours"></span>**ERROR\_INVALID\_LOGON\_HOURS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-201">1328 (0x530)</span><span class="sxs-lookup"><span data-stu-id="e4551-201">1328 (0x530)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-202">Su cuenta tiene restricciones de tiempo que le evitan iniciar sesión en este momento.</span><span class="sxs-lookup"><span data-stu-id="e4551-202">Your account has time restrictions that keep you from signing in right now.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-203"><span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERROR \_ de \_ estación de trabajo no válida**</span><span class="sxs-lookup"><span data-stu-id="e4551-203"><span id="ERROR_INVALID_WORKSTATION"></span><span id="error_invalid_workstation"></span>**ERROR\_INVALID\_WORKSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-204">1329 (0x531)</span><span class="sxs-lookup"><span data-stu-id="e4551-204">1329 (0x531)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-205">Este usuario no tiene permiso para iniciar sesión en este equipo.</span><span class="sxs-lookup"><span data-stu-id="e4551-205">This user isn't allowed to sign in to this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-206"><span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**contraseña de ERROR \_ \_ expirada**</span><span class="sxs-lookup"><span data-stu-id="e4551-206"><span id="ERROR_PASSWORD_EXPIRED"></span><span id="error_password_expired"></span>**ERROR\_PASSWORD\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-207">1330 (0x532)</span><span class="sxs-lookup"><span data-stu-id="e4551-207">1330 (0x532)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-208">La contraseña de esta cuenta ha expirado.</span><span class="sxs-lookup"><span data-stu-id="e4551-208">The password for this account has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-209"><span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**cuenta de ERROR \_ \_ deshabilitada**</span><span class="sxs-lookup"><span data-stu-id="e4551-209"><span id="ERROR_ACCOUNT_DISABLED"></span><span id="error_account_disabled"></span>**ERROR\_ACCOUNT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-210">1331 (0x533)</span><span class="sxs-lookup"><span data-stu-id="e4551-210">1331 (0x533)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-211">Este usuario no puede iniciar sesión porque esta cuenta está deshabilitada actualmente.</span><span class="sxs-lookup"><span data-stu-id="e4551-211">This user can't sign in because this account is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-212"><span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERROR \_ ninguno \_ asignado**</span><span class="sxs-lookup"><span data-stu-id="e4551-212"><span id="ERROR_NONE_MAPPED"></span><span id="error_none_mapped"></span>**ERROR\_NONE\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-213">1332 (0x534)</span><span class="sxs-lookup"><span data-stu-id="e4551-213">1332 (0x534)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-214">No se realizó ninguna asignación entre los nombres de cuenta y los ID. de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e4551-214">No mapping between account names and security IDs was done.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-215"><span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERROR \_ demasiados de \_ \_ LUID \_ solicitadas**</span><span class="sxs-lookup"><span data-stu-id="e4551-215"><span id="ERROR_TOO_MANY_LUIDS_REQUESTED"></span><span id="error_too_many_luids_requested"></span>**ERROR\_TOO\_MANY\_LUIDS\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-216">1333 (0x535)</span><span class="sxs-lookup"><span data-stu-id="e4551-216">1333 (0x535)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-217">Se solicitaron demasiados identificadores de usuario local (LUID) al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="e4551-217">Too many local user identifiers (LUIDs) were requested at one time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-218"><span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**ERROR de \_ LUID \_ agotado**</span><span class="sxs-lookup"><span data-stu-id="e4551-218"><span id="ERROR_LUIDS_EXHAUSTED"></span><span id="error_luids_exhausted"></span>**ERROR\_LUIDS\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-219">1334 (0x536)</span><span class="sxs-lookup"><span data-stu-id="e4551-219">1334 (0x536)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-220">No hay más identificadores de usuario locales (LUID) disponibles.</span><span class="sxs-lookup"><span data-stu-id="e4551-220">No more local user identifiers (LUIDs) are available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-221"><span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**ERROR \_ de \_ \_ subentidad no válida**</span><span class="sxs-lookup"><span data-stu-id="e4551-221"><span id="ERROR_INVALID_SUB_AUTHORITY"></span><span id="error_invalid_sub_authority"></span>**ERROR\_INVALID\_SUB\_AUTHORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-222">1335 (0x537)</span><span class="sxs-lookup"><span data-stu-id="e4551-222">1335 (0x537)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-223">La parte del subautor de un identificador de seguridad no es válida para este uso concreto.</span><span class="sxs-lookup"><span data-stu-id="e4551-223">The subauthority part of a security ID is invalid for this particular use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-224"><span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERROR \_ de \_ ACL no válida**</span><span class="sxs-lookup"><span data-stu-id="e4551-224"><span id="ERROR_INVALID_ACL"></span><span id="error_invalid_acl"></span>**ERROR\_INVALID\_ACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-225">1336 (0x538)</span><span class="sxs-lookup"><span data-stu-id="e4551-225">1336 (0x538)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-226">La estructura de la lista de control de acceso (ACL) no es válida.</span><span class="sxs-lookup"><span data-stu-id="e4551-226">The access control list (ACL) structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-227"><span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERROR \_ de \_ SID no válido**</span><span class="sxs-lookup"><span data-stu-id="e4551-227"><span id="ERROR_INVALID_SID"></span><span id="error_invalid_sid"></span>**ERROR\_INVALID\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-228">1337 (0x539)</span><span class="sxs-lookup"><span data-stu-id="e4551-228">1337 (0x539)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-229">La estructura de ID. de seguridad no es válida.</span><span class="sxs-lookup"><span data-stu-id="e4551-229">The security ID structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-230"><span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERROR \_ de \_ Descripción de seguridad no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-230"><span id="ERROR_INVALID_SECURITY_DESCR"></span><span id="error_invalid_security_descr"></span>**ERROR\_INVALID\_SECURITY\_DESCR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-231">1338 (0x53A)</span><span class="sxs-lookup"><span data-stu-id="e4551-231">1338 (0x53A)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-232">La estructura del descriptor de seguridad no es válida.</span><span class="sxs-lookup"><span data-stu-id="e4551-232">The security descriptor structure is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-233"><span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERROR \_ en \_ ACL de herencia incorrecta \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-233"><span id="ERROR_BAD_INHERITANCE_ACL"></span><span id="error_bad_inheritance_acl"></span>**ERROR\_BAD\_INHERITANCE\_ACL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-234">1340 (0x53C)</span><span class="sxs-lookup"><span data-stu-id="e4551-234">1340 (0x53C)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-235">No se pudo crear la lista de control de acceso (ACL) o la entrada de control de acceso (ACE) heredada.</span><span class="sxs-lookup"><span data-stu-id="e4551-235">The inherited access control list (ACL) or access control entry (ACE) could not be built.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-236"><span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**ERROR de \_ servidor \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="e4551-236"><span id="ERROR_SERVER_DISABLED"></span><span id="error_server_disabled"></span>**ERROR\_SERVER\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-237">1341 (0x53D)</span><span class="sxs-lookup"><span data-stu-id="e4551-237">1341 (0x53D)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-238">El servidor está deshabilitado actualmente.</span><span class="sxs-lookup"><span data-stu-id="e4551-238">The server is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-239"><span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**servidor de errores \_ \_ no \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="e4551-239"><span id="ERROR_SERVER_NOT_DISABLED"></span><span id="error_server_not_disabled"></span>**ERROR\_SERVER\_NOT\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-240">1342 (0x53E)</span><span class="sxs-lookup"><span data-stu-id="e4551-240">1342 (0x53E)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-241">El servidor está habilitado actualmente.</span><span class="sxs-lookup"><span data-stu-id="e4551-241">The server is currently enabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-242"><span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERROR \_ de \_ autoridad de ID. no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-242"><span id="ERROR_INVALID_ID_AUTHORITY"></span><span id="error_invalid_id_authority"></span>**ERROR\_INVALID\_ID\_AUTHORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-243">1343 (0x53F)</span><span class="sxs-lookup"><span data-stu-id="e4551-243">1343 (0x53F)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-244">El valor proporcionado era un valor no válido para una autoridad de identificador.</span><span class="sxs-lookup"><span data-stu-id="e4551-244">The value provided was an invalid value for an identifier authority.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-245"><span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**se \_ \_ \_ ha superado el espacio asignado**</span><span class="sxs-lookup"><span data-stu-id="e4551-245"><span id="ERROR_ALLOTTED_SPACE_EXCEEDED"></span><span id="error_allotted_space_exceeded"></span>**ERROR\_ALLOTTED\_SPACE\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-246">1344 (0x540)</span><span class="sxs-lookup"><span data-stu-id="e4551-246">1344 (0x540)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-247">No hay más memoria disponible para las actualizaciones de información de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e4551-247">No more memory is available for security information updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-248"><span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERROR \_ de \_ atributos de grupo no válidos \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-248"><span id="ERROR_INVALID_GROUP_ATTRIBUTES"></span><span id="error_invalid_group_attributes"></span>**ERROR\_INVALID\_GROUP\_ATTRIBUTES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-249">1345 (0x541)</span><span class="sxs-lookup"><span data-stu-id="e4551-249">1345 (0x541)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-250">Los atributos especificados no son válidos o no son compatibles con los atributos del grupo en su conjunto.</span><span class="sxs-lookup"><span data-stu-id="e4551-250">The specified attributes are invalid, or incompatible with the attributes for the group as a whole.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-251"><span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERROR \_ de \_ nivel de suplantación incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-251"><span id="ERROR_BAD_IMPERSONATION_LEVEL"></span><span id="error_bad_impersonation_level"></span>**ERROR\_BAD\_IMPERSONATION\_LEVEL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-252">1346 (0x542)</span><span class="sxs-lookup"><span data-stu-id="e4551-252">1346 (0x542)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-253">No se ha proporcionado el nivel de representación necesario o el nivel de representación no es válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-253">Either a required impersonation level was not provided, or the provided impersonation level is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-254"><span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERROR no se pudo \_ \_ abrir \_ anónimo**</span><span class="sxs-lookup"><span data-stu-id="e4551-254"><span id="ERROR_CANT_OPEN_ANONYMOUS"></span><span id="error_cant_open_anonymous"></span>**ERROR\_CANT\_OPEN\_ANONYMOUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-255">1347 (0x543)</span><span class="sxs-lookup"><span data-stu-id="e4551-255">1347 (0x543)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-256">No se puede abrir un token de seguridad de nivel anónimo.</span><span class="sxs-lookup"><span data-stu-id="e4551-256">Cannot open an anonymous level security token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-257"><span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERROR \_ de \_ clase de validación incorrecta \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-257"><span id="ERROR_BAD_VALIDATION_CLASS"></span><span id="error_bad_validation_class"></span>**ERROR\_BAD\_VALIDATION\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-258">1348 (0x544)</span><span class="sxs-lookup"><span data-stu-id="e4551-258">1348 (0x544)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-259">La clase de información de validación solicitada no es válida.</span><span class="sxs-lookup"><span data-stu-id="e4551-259">The validation information class requested was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-260"><span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**ERROR \_ de \_ tipo de token incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-260"><span id="ERROR_BAD_TOKEN_TYPE"></span><span id="error_bad_token_type"></span>**ERROR\_BAD\_TOKEN\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-261">1349 (0x545)</span><span class="sxs-lookup"><span data-stu-id="e4551-261">1349 (0x545)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-262">El tipo del token no es apropiado para su intento de uso.</span><span class="sxs-lookup"><span data-stu-id="e4551-262">The type of the token is inappropriate for its attempted use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-263"><span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERROR: \_ no hay \_ seguridad \_ en el \_ objeto**</span><span class="sxs-lookup"><span data-stu-id="e4551-263"><span id="ERROR_NO_SECURITY_ON_OBJECT"></span><span id="error_no_security_on_object"></span>**ERROR\_NO\_SECURITY\_ON\_OBJECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-264">1350 (0x546)</span><span class="sxs-lookup"><span data-stu-id="e4551-264">1350 (0x546)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-265">No se puede realizar una operación de seguridad en un objeto que no tiene ninguna seguridad asociada.</span><span class="sxs-lookup"><span data-stu-id="e4551-265">Unable to perform a security operation on an object that has no associated security.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-266"><span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ERROR: no se \_ \_ puede obtener acceso a la \_ información del dominio \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-266"><span id="ERROR_CANT_ACCESS_DOMAIN_INFO"></span><span id="error_cant_access_domain_info"></span>**ERROR\_CANT\_ACCESS\_DOMAIN\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-267">1351 (0x547)</span><span class="sxs-lookup"><span data-stu-id="e4551-267">1351 (0x547)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-268">No se pudo leer la información de configuración del controlador de dominio, ya sea porque la máquina no está disponible o porque se ha denegado el acceso.</span><span class="sxs-lookup"><span data-stu-id="e4551-268">Configuration information could not be read from the domain controller, either because the machine is unavailable, or access has been denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-269"><span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERROR \_ de \_ Estado de servidor no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-269"><span id="ERROR_INVALID_SERVER_STATE"></span><span id="error_invalid_server_state"></span>**ERROR\_INVALID\_SERVER\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-270">1352 (0x548)</span><span class="sxs-lookup"><span data-stu-id="e4551-270">1352 (0x548)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-271">El servidor de administración de cuentas de seguridad (SAM) o la autoridad de seguridad local (LSA) se encontraba en un estado incorrecto para realizar la operación de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e4551-271">The security account manager (SAM) or local security authority (LSA) server was in the wrong state to perform the security operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-272"><span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERROR \_ de \_ Estado de dominio no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-272"><span id="ERROR_INVALID_DOMAIN_STATE"></span><span id="error_invalid_domain_state"></span>**ERROR\_INVALID\_DOMAIN\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-273">1353 (0x549)</span><span class="sxs-lookup"><span data-stu-id="e4551-273">1353 (0x549)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-274">El estado del dominio era incorrecto para realizar la operación de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e4551-274">The domain was in the wrong state to perform the security operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-275"><span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERROR \_ de \_ rol de dominio no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-275"><span id="ERROR_INVALID_DOMAIN_ROLE"></span><span id="error_invalid_domain_role"></span>**ERROR\_INVALID\_DOMAIN\_ROLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-276">1354 (0x54A)</span><span class="sxs-lookup"><span data-stu-id="e4551-276">1354 (0x54A)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-277">Esta operación solo se permite para el controlador de dominio principal del dominio.</span><span class="sxs-lookup"><span data-stu-id="e4551-277">This operation is only allowed for the Primary Domain Controller of the domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-278"><span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**NO se ha podido \_ \_ este \_ dominio**</span><span class="sxs-lookup"><span data-stu-id="e4551-278"><span id="ERROR_NO_SUCH_DOMAIN"></span><span id="error_no_such_domain"></span>**ERROR\_NO\_SUCH\_DOMAIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-279">1355 (0x54B)</span><span class="sxs-lookup"><span data-stu-id="e4551-279">1355 (0x54B)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-280">El dominio especificado no existe o no se pudo establecer contacto con él.</span><span class="sxs-lookup"><span data-stu-id="e4551-280">The specified domain either does not exist or could not be contacted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-281"><span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**\_existe un dominio de error \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-281"><span id="ERROR_DOMAIN_EXISTS"></span><span id="error_domain_exists"></span>**ERROR\_DOMAIN\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-282">1356 (0x54C)</span><span class="sxs-lookup"><span data-stu-id="e4551-282">1356 (0x54C)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-283">El dominio especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="e4551-283">The specified domain already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-284"><span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**límite de dominio de ERROR \_ \_ \_ superado**</span><span class="sxs-lookup"><span data-stu-id="e4551-284"><span id="ERROR_DOMAIN_LIMIT_EXCEEDED"></span><span id="error_domain_limit_exceeded"></span>**ERROR\_DOMAIN\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-285">1357 (0x54D)</span><span class="sxs-lookup"><span data-stu-id="e4551-285">1357 (0x54D)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-286">Se intentó superar el límite en el número de dominios por servidor.</span><span class="sxs-lookup"><span data-stu-id="e4551-286">An attempt was made to exceed the limit on the number of domains per server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-287"><span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERROR \_ de \_ base de BD interna \_ dañado**</span><span class="sxs-lookup"><span data-stu-id="e4551-287"><span id="ERROR_INTERNAL_DB_CORRUPTION"></span><span id="error_internal_db_corruption"></span>**ERROR\_INTERNAL\_DB\_CORRUPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-288">1358 (0x54E)</span><span class="sxs-lookup"><span data-stu-id="e4551-288">1358 (0x54E)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-289">No se puede completar la operación solicitada debido a un error grave del medio o a una estructura de datos dañada en el disco.</span><span class="sxs-lookup"><span data-stu-id="e4551-289">Unable to complete the requested operation because of either a catastrophic media failure or a data structure corruption on the disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-290"><span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**error \_ interno de error \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-290"><span id="ERROR_INTERNAL_ERROR"></span><span id="error_internal_error"></span>**ERROR\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-291">1359 (0x54F)</span><span class="sxs-lookup"><span data-stu-id="e4551-291">1359 (0x54F)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-292">Se ha producido un error interno.</span><span class="sxs-lookup"><span data-stu-id="e4551-292">An internal error occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-293"><span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERROR \_ genérico \_ no \_ asignado**</span><span class="sxs-lookup"><span data-stu-id="e4551-293"><span id="ERROR_GENERIC_NOT_MAPPED"></span><span id="error_generic_not_mapped"></span>**ERROR\_GENERIC\_NOT\_MAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-294">1360 (0x550)</span><span class="sxs-lookup"><span data-stu-id="e4551-294">1360 (0x550)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-295">Los tipos de acceso genéricos estaban contenidos en una máscara de acceso que ya debe estar asignada a tipos no genéricos.</span><span class="sxs-lookup"><span data-stu-id="e4551-295">Generic access types were contained in an access mask which should already be mapped to nongeneric types.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-296"><span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**ERROR \_ de \_ formato de descriptor incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-296"><span id="ERROR_BAD_DESCRIPTOR_FORMAT"></span><span id="error_bad_descriptor_format"></span>**ERROR\_BAD\_DESCRIPTOR\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-297">1361 (0x551)</span><span class="sxs-lookup"><span data-stu-id="e4551-297">1361 (0x551)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-298">Un descriptor de seguridad no tiene el formato correcto (absoluto o autorelativo).</span><span class="sxs-lookup"><span data-stu-id="e4551-298">A security descriptor is not in the right format (absolute or self-relative).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-299"><span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**ERROR en el \_ \_ proceso de inicio de sesión \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-299"><span id="ERROR_NOT_LOGON_PROCESS"></span><span id="error_not_logon_process"></span>**ERROR\_NOT\_LOGON\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-300">1362 (0x552)</span><span class="sxs-lookup"><span data-stu-id="e4551-300">1362 (0x552)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-301">La acción solicitada está restringida para su uso por parte de los procesos de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e4551-301">The requested action is restricted for use by logon processes only.</span></span> <span data-ttu-id="e4551-302">El proceso de llamada no se ha registrado como un proceso de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="e4551-302">The calling process has not registered as a logon process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-303"><span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**la sesión de inicio de sesión de ERROR \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="e4551-303"><span id="ERROR_LOGON_SESSION_EXISTS"></span><span id="error_logon_session_exists"></span>**ERROR\_LOGON\_SESSION\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-304">1363 (0x553)</span><span class="sxs-lookup"><span data-stu-id="e4551-304">1363 (0x553)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-305">No se puede iniciar una nueva sesión de inicio de sesión con un identificador que ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="e4551-305">Cannot start a new logon session with an ID that is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-306"><span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**NO se ha podido \_ \_ este \_ paquete**</span><span class="sxs-lookup"><span data-stu-id="e4551-306"><span id="ERROR_NO_SUCH_PACKAGE"></span><span id="error_no_such_package"></span>**ERROR\_NO\_SUCH\_PACKAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-307">1364 (0x554)</span><span class="sxs-lookup"><span data-stu-id="e4551-307">1364 (0x554)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-308">Se desconoce un paquete de autenticación especificado.</span><span class="sxs-lookup"><span data-stu-id="e4551-308">A specified authentication package is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-309"><span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERROR \_ de \_ \_ Estado de sesión de inicio de sesión incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-309"><span id="ERROR_BAD_LOGON_SESSION_STATE"></span><span id="error_bad_logon_session_state"></span>**ERROR\_BAD\_LOGON\_SESSION\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-310">1365 (0x555)</span><span class="sxs-lookup"><span data-stu-id="e4551-310">1365 (0x555)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-311">La sesión de inicio de sesión no se encuentra en un estado coherente con la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="e4551-311">The logon session is not in a state that is consistent with the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-312"><span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**\_colisión de \_ sesión de inicio de sesión con error \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-312"><span id="ERROR_LOGON_SESSION_COLLISION"></span><span id="error_logon_session_collision"></span>**ERROR\_LOGON\_SESSION\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-313">1366 (0x556)</span><span class="sxs-lookup"><span data-stu-id="e4551-313">1366 (0x556)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-314">El identificador de la sesión de inicio de sesión ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="e4551-314">The logon session ID is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-315"><span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERROR \_ de \_ tipo de inicio de sesión no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-315"><span id="ERROR_INVALID_LOGON_TYPE"></span><span id="error_invalid_logon_type"></span>**ERROR\_INVALID\_LOGON\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-316">1367 (0x557)</span><span class="sxs-lookup"><span data-stu-id="e4551-316">1367 (0x557)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-317">Una solicitud de inicio de sesión contenía un valor de tipo de inicio de sesión no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-317">A logon request contained an invalid logon type value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-318"><span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**ERROR \_ no se puede \_ Suplantar**</span><span class="sxs-lookup"><span data-stu-id="e4551-318"><span id="ERROR_CANNOT_IMPERSONATE"></span><span id="error_cannot_impersonate"></span>**ERROR\_CANNOT\_IMPERSONATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-319">1368 (0x558)</span><span class="sxs-lookup"><span data-stu-id="e4551-319">1368 (0x558)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-320">No se puede suplantar con una canalización con nombre hasta que se hayan leído los datos de esa canalización.</span><span class="sxs-lookup"><span data-stu-id="e4551-320">Unable to impersonate using a named pipe until data has been read from that pipe.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-321"><span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERROR \_ RXACT \_ Estado no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-321"><span id="ERROR_RXACT_INVALID_STATE"></span><span id="error_rxact_invalid_state"></span>**ERROR\_RXACT\_INVALID\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-322">1369 (0x559)</span><span class="sxs-lookup"><span data-stu-id="e4551-322">1369 (0x559)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-323">El estado de la transacción de un subárbol del registro no es compatible con la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="e4551-323">The transaction state of a registry subtree is incompatible with the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-324"><span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**ERROR \_ de \_ confirmación \_ RXACT**</span><span class="sxs-lookup"><span data-stu-id="e4551-324"><span id="ERROR_RXACT_COMMIT_FAILURE"></span><span id="error_rxact_commit_failure"></span>**ERROR\_RXACT\_COMMIT\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-325">1370 (0x55A)</span><span class="sxs-lookup"><span data-stu-id="e4551-325">1370 (0x55A)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-326">Se ha producido un daño interno en la base de datos de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e4551-326">An internal security database corruption has been encountered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-327"><span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**\_cuenta especial de error \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-327"><span id="ERROR_SPECIAL_ACCOUNT"></span><span id="error_special_account"></span>**ERROR\_SPECIAL\_ACCOUNT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-328">1371 (0x55B)</span><span class="sxs-lookup"><span data-stu-id="e4551-328">1371 (0x55B)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-329">No se puede realizar esta operación en cuentas integradas.</span><span class="sxs-lookup"><span data-stu-id="e4551-329">Cannot perform this operation on built-in accounts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-330"><span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**\_grupo especial de error \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-330"><span id="ERROR_SPECIAL_GROUP"></span><span id="error_special_group"></span>**ERROR\_SPECIAL\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-331">1372 (0x55C)</span><span class="sxs-lookup"><span data-stu-id="e4551-331">1372 (0x55C)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-332">No se puede realizar esta operación en este grupo especial integrado.</span><span class="sxs-lookup"><span data-stu-id="e4551-332">Cannot perform this operation on this built-in special group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-333"><span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**ERROR \_ de \_ usuario especial**</span><span class="sxs-lookup"><span data-stu-id="e4551-333"><span id="ERROR_SPECIAL_USER"></span><span id="error_special_user"></span>**ERROR\_SPECIAL\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-334">1373 (0x55D)</span><span class="sxs-lookup"><span data-stu-id="e4551-334">1373 (0x55D)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-335">No se puede realizar esta operación en este usuario especial integrado.</span><span class="sxs-lookup"><span data-stu-id="e4551-335">Cannot perform this operation on this built-in special user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-336"><span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**miembro de ERROR: \_ \_ \_ grupo principal**</span><span class="sxs-lookup"><span data-stu-id="e4551-336"><span id="ERROR_MEMBERS_PRIMARY_GROUP"></span><span id="error_members_primary_group"></span>**ERROR\_MEMBERS\_PRIMARY\_GROUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-337">1374 (0x55E)</span><span class="sxs-lookup"><span data-stu-id="e4551-337">1374 (0x55E)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-338">No se puede quitar el usuario de un grupo porque es actualmente el grupo principal del usuario.</span><span class="sxs-lookup"><span data-stu-id="e4551-338">The user cannot be removed from a group because the group is currently the user's primary group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-339"><span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**el \_ token \_ de error ya está \_ en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="e4551-339"><span id="ERROR_TOKEN_ALREADY_IN_USE"></span><span id="error_token_already_in_use"></span>**ERROR\_TOKEN\_ALREADY\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-340">1375 (0x55F)</span><span class="sxs-lookup"><span data-stu-id="e4551-340">1375 (0x55F)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-341">El token ya se está usando como un token principal.</span><span class="sxs-lookup"><span data-stu-id="e4551-341">The token is already in use as a primary token.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-342"><span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**\_no existe \_ este \_ alias**</span><span class="sxs-lookup"><span data-stu-id="e4551-342"><span id="ERROR_NO_SUCH_ALIAS"></span><span id="error_no_such_alias"></span>**ERROR\_NO\_SUCH\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-343">1376 (0x560)</span><span class="sxs-lookup"><span data-stu-id="e4551-343">1376 (0x560)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-344">El grupo local especificado no existe.</span><span class="sxs-lookup"><span data-stu-id="e4551-344">The specified local group does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-345"><span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**el \_ miembro \_ de error no está \_ en el \_ alias**</span><span class="sxs-lookup"><span data-stu-id="e4551-345"><span id="ERROR_MEMBER_NOT_IN_ALIAS"></span><span id="error_member_not_in_alias"></span>**ERROR\_MEMBER\_NOT\_IN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-346">1377 (0x561)</span><span class="sxs-lookup"><span data-stu-id="e4551-346">1377 (0x561)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-347">El nombre de cuenta especificado no es un miembro del grupo.</span><span class="sxs-lookup"><span data-stu-id="e4551-347">The specified account name is not a member of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-348"><span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**\_miembro \_ de error en \_ alias**</span><span class="sxs-lookup"><span data-stu-id="e4551-348"><span id="ERROR_MEMBER_IN_ALIAS"></span><span id="error_member_in_alias"></span>**ERROR\_MEMBER\_IN\_ALIAS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-349">1378 (0x562)</span><span class="sxs-lookup"><span data-stu-id="e4551-349">1378 (0x562)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-350">El nombre de cuenta especificado ya es miembro del grupo.</span><span class="sxs-lookup"><span data-stu-id="e4551-350">The specified account name is already a member of the group.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-351"><span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**\_existe un alias de error \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-351"><span id="ERROR_ALIAS_EXISTS"></span><span id="error_alias_exists"></span>**ERROR\_ALIAS\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-352">1379 (0x563)</span><span class="sxs-lookup"><span data-stu-id="e4551-352">1379 (0x563)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-353">El grupo local especificado ya existe.</span><span class="sxs-lookup"><span data-stu-id="e4551-353">The specified local group already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-354"><span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERROR de \_ Inicio de sesión \_ no \_ concedido**</span><span class="sxs-lookup"><span data-stu-id="e4551-354"><span id="ERROR_LOGON_NOT_GRANTED"></span><span id="error_logon_not_granted"></span>**ERROR\_LOGON\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-355">1380 (0x564)</span><span class="sxs-lookup"><span data-stu-id="e4551-355">1380 (0x564)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-356">Error de inicio de sesión: no se ha concedido al usuario el tipo de inicio de sesión solicitado en este equipo.</span><span class="sxs-lookup"><span data-stu-id="e4551-356">Logon failure: the user has not been granted the requested logon type at this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-357"><span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERROR \_ demasiados \_ \_ secretos**</span><span class="sxs-lookup"><span data-stu-id="e4551-357"><span id="ERROR_TOO_MANY_SECRETS"></span><span id="error_too_many_secrets"></span>**ERROR\_TOO\_MANY\_SECRETS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-358">1381 (0x565)</span><span class="sxs-lookup"><span data-stu-id="e4551-358">1381 (0x565)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-359">Se ha superado el número máximo de secretos que se pueden almacenar en un solo sistema.</span><span class="sxs-lookup"><span data-stu-id="e4551-359">The maximum number of secrets that may be stored in a single system has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-360"><span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**ERROR de \_ secreto \_ demasiado \_ largo**</span><span class="sxs-lookup"><span data-stu-id="e4551-360"><span id="ERROR_SECRET_TOO_LONG"></span><span id="error_secret_too_long"></span>**ERROR\_SECRET\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-361">1382 (0x566)</span><span class="sxs-lookup"><span data-stu-id="e4551-361">1382 (0x566)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-362">La longitud de un secreto supera la longitud máxima permitida.</span><span class="sxs-lookup"><span data-stu-id="e4551-362">The length of a secret exceeds the maximum length allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-363"><span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**error \_ interno de \_ base de BD \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-363"><span id="ERROR_INTERNAL_DB_ERROR"></span><span id="error_internal_db_error"></span>**ERROR\_INTERNAL\_DB\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-364">1383 (0x567)</span><span class="sxs-lookup"><span data-stu-id="e4551-364">1383 (0x567)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-365">La base de datos de autoridad de seguridad local contiene una incoherencia interna.</span><span class="sxs-lookup"><span data-stu-id="e4551-365">The local security authority database contains an internal inconsistency.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-366"><span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERROR \_ demasiados \_ \_ \_ identificadores de contexto**</span><span class="sxs-lookup"><span data-stu-id="e4551-366"><span id="ERROR_TOO_MANY_CONTEXT_IDS"></span><span id="error_too_many_context_ids"></span>**ERROR\_TOO\_MANY\_CONTEXT\_IDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-367">1384 (0x568)</span><span class="sxs-lookup"><span data-stu-id="e4551-367">1384 (0x568)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-368">Durante un intento de inicio de sesión, el contexto de seguridad del usuario ha acumulado demasiados identificadores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e4551-368">During a logon attempt, the user's security context accumulated too many security IDs.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-369"><span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**\_no se \_ \_ \_ concedió el tipo de inicio de sesión de error**</span><span class="sxs-lookup"><span data-stu-id="e4551-369"><span id="ERROR_LOGON_TYPE_NOT_GRANTED"></span><span id="error_logon_type_not_granted"></span>**ERROR\_LOGON\_TYPE\_NOT\_GRANTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-370">1385 (0x569)</span><span class="sxs-lookup"><span data-stu-id="e4551-370">1385 (0x569)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-371">Error de inicio de sesión: no se ha concedido al usuario el tipo de inicio de sesión solicitado en este equipo.</span><span class="sxs-lookup"><span data-stu-id="e4551-371">Logon failure: the user has not been granted the requested logon type at this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-372"><span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERROR \_ de \_ cifrado cruzado de NT \_ \_ requerido**</span><span class="sxs-lookup"><span data-stu-id="e4551-372"><span id="ERROR_NT_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_nt_cross_encryption_required"></span>**ERROR\_NT\_CROSS\_ENCRYPTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-373">1386 (0x56A)</span><span class="sxs-lookup"><span data-stu-id="e4551-373">1386 (0x56A)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-374">Es necesaria una contraseña con cifrado cruzado para cambiar la contraseña de un usuario.</span><span class="sxs-lookup"><span data-stu-id="e4551-374">A cross-encrypted password is necessary to change a user password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-375"><span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**NO se ha podido \_ \_ este \_ miembro**</span><span class="sxs-lookup"><span data-stu-id="e4551-375"><span id="ERROR_NO_SUCH_MEMBER"></span><span id="error_no_such_member"></span>**ERROR\_NO\_SUCH\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-376">1387 (0x56B)</span><span class="sxs-lookup"><span data-stu-id="e4551-376">1387 (0x56B)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-377">No se pudo agregar o quitar un miembro del grupo local porque el miembro no existe.</span><span class="sxs-lookup"><span data-stu-id="e4551-377">A member could not be added to or removed from the local group because the member does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-378"><span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**ERROR \_ de \_ miembro no válido**</span><span class="sxs-lookup"><span data-stu-id="e4551-378"><span id="ERROR_INVALID_MEMBER"></span><span id="error_invalid_member"></span>**ERROR\_INVALID\_MEMBER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-379">1388 (0x56C)</span><span class="sxs-lookup"><span data-stu-id="e4551-379">1388 (0x56C)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-380">No se pudo agregar un nuevo miembro a un grupo local porque el miembro tiene un tipo de cuenta incorrecto.</span><span class="sxs-lookup"><span data-stu-id="e4551-380">A new member could not be added to a local group because the member has the wrong account type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-381"><span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERROR \_ demasiados \_ \_ SID**</span><span class="sxs-lookup"><span data-stu-id="e4551-381"><span id="ERROR_TOO_MANY_SIDS"></span><span id="error_too_many_sids"></span>**ERROR\_TOO\_MANY\_SIDS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-382">1389 (0x56D)</span><span class="sxs-lookup"><span data-stu-id="e4551-382">1389 (0x56D)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-383">Se han especificado demasiados identificadores de seguridad.</span><span class="sxs-lookup"><span data-stu-id="e4551-383">Too many security IDs have been specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-384"><span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERROR \_ de \_ \_ cifrado cruzado LM \_ requerido**</span><span class="sxs-lookup"><span data-stu-id="e4551-384"><span id="ERROR_LM_CROSS_ENCRYPTION_REQUIRED"></span><span id="error_lm_cross_encryption_required"></span>**ERROR\_LM\_CROSS\_ENCRYPTION\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-385">1390 (0x56E)</span><span class="sxs-lookup"><span data-stu-id="e4551-385">1390 (0x56E)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-386">Se necesita una contraseña con cifrado cruzado para cambiar esta contraseña de usuario.</span><span class="sxs-lookup"><span data-stu-id="e4551-386">A cross-encrypted password is necessary to change this user password.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-387"><span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERROR \_ sin \_ herencia**</span><span class="sxs-lookup"><span data-stu-id="e4551-387"><span id="ERROR_NO_INHERITANCE"></span><span id="error_no_inheritance"></span>**ERROR\_NO\_INHERITANCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-388">1391 (0x56F)</span><span class="sxs-lookup"><span data-stu-id="e4551-388">1391 (0x56F)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-389">Indica que una ACL no contiene componentes heredables.</span><span class="sxs-lookup"><span data-stu-id="e4551-389">Indicates an ACL contains no inheritable components.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-390"><span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**archivo de ERROR \_ \_ dañado**</span><span class="sxs-lookup"><span data-stu-id="e4551-390"><span id="ERROR_FILE_CORRUPT"></span><span id="error_file_corrupt"></span>**ERROR\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-391">1392 (0x570)</span><span class="sxs-lookup"><span data-stu-id="e4551-391">1392 (0x570)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-392">El archivo o directorio está dañado y no se pudo leer.</span><span class="sxs-lookup"><span data-stu-id="e4551-392">The file or directory is corrupted and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-393"><span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**ERROR de \_ disco \_ dañado**</span><span class="sxs-lookup"><span data-stu-id="e4551-393"><span id="ERROR_DISK_CORRUPT"></span><span id="error_disk_corrupt"></span>**ERROR\_DISK\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-394">1393 (0x571)</span><span class="sxs-lookup"><span data-stu-id="e4551-394">1393 (0x571)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-395">La estructura del disco está dañada y es ilegible.</span><span class="sxs-lookup"><span data-stu-id="e4551-395">The disk structure is corrupted and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-396"><span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERROR \_ sin \_ \_ clave de sesión de usuario \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-396"><span id="ERROR_NO_USER_SESSION_KEY"></span><span id="error_no_user_session_key"></span>**ERROR\_NO\_USER\_SESSION\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-397">1394 (0x572)</span><span class="sxs-lookup"><span data-stu-id="e4551-397">1394 (0x572)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-398">No hay ninguna clave de sesión de usuario para la sesión de inicio de sesión especificada.</span><span class="sxs-lookup"><span data-stu-id="e4551-398">There is no user session key for the specified logon session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-399"><span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**cuota de licencia de ERROR \_ \_ \_ superada**</span><span class="sxs-lookup"><span data-stu-id="e4551-399"><span id="ERROR_LICENSE_QUOTA_EXCEEDED"></span><span id="error_license_quota_exceeded"></span>**ERROR\_LICENSE\_QUOTA\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-400">1395 (0x573)</span><span class="sxs-lookup"><span data-stu-id="e4551-400">1395 (0x573)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-401">El servicio al que se está accediendo tiene una licencia para un número determinado de conexiones.</span><span class="sxs-lookup"><span data-stu-id="e4551-401">The service being accessed is licensed for a particular number of connections.</span></span> <span data-ttu-id="e4551-402">No se pueden realizar más conexiones al servicio en este momento porque ya hay tantas conexiones como el servicio puede aceptar.</span><span class="sxs-lookup"><span data-stu-id="e4551-402">No more connections can be made to the service at this time because there are already as many connections as the service can accept.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-403"><span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERROR \_ de \_ nombre de destino incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-403"><span id="ERROR_WRONG_TARGET_NAME"></span><span id="error_wrong_target_name"></span>**ERROR\_WRONG\_TARGET\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-404">1396 (0x574)</span><span class="sxs-lookup"><span data-stu-id="e4551-404">1396 (0x574)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-405">El nombre de la cuenta de destino no es correcto.</span><span class="sxs-lookup"><span data-stu-id="e4551-405">The target account name is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-406"><span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERROR \_ de \_ autenticación mutua \_ errónea**</span><span class="sxs-lookup"><span data-stu-id="e4551-406"><span id="ERROR_MUTUAL_AUTH_FAILED"></span><span id="error_mutual_auth_failed"></span>**ERROR\_MUTUAL\_AUTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-407">1397 (0x575)</span><span class="sxs-lookup"><span data-stu-id="e4551-407">1397 (0x575)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-408">Error de autenticación mutua.</span><span class="sxs-lookup"><span data-stu-id="e4551-408">Mutual Authentication failed.</span></span> <span data-ttu-id="e4551-409">La contraseña del servidor no está actualizada en el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="e4551-409">The server's password is out of date at the domain controller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-410"><span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**\_sesgo de tiempo de error \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-410"><span id="ERROR_TIME_SKEW"></span><span id="error_time_skew"></span>**ERROR\_TIME\_SKEW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-411">1398 (0x576)</span><span class="sxs-lookup"><span data-stu-id="e4551-411">1398 (0x576)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-412">Hay una diferencia de hora y/o fecha entre el cliente y el servidor.</span><span class="sxs-lookup"><span data-stu-id="e4551-412">There is a time and/or date difference between the client and server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-413"><span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERROR \_ \_ dominio actual \_ no \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="e4551-413"><span id="ERROR_CURRENT_DOMAIN_NOT_ALLOWED"></span><span id="error_current_domain_not_allowed"></span>**ERROR\_CURRENT\_DOMAIN\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-414">1399 (0x577)</span><span class="sxs-lookup"><span data-stu-id="e4551-414">1399 (0x577)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-415">Esta operación no se puede realizar en el dominio actual.</span><span class="sxs-lookup"><span data-stu-id="e4551-415">This operation cannot be performed on the current domain.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-416"><span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERROR \_ de \_ identificador de ventana no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-416"><span id="ERROR_INVALID_WINDOW_HANDLE"></span><span id="error_invalid_window_handle"></span>**ERROR\_INVALID\_WINDOW\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-417">1400 (0x578)</span><span class="sxs-lookup"><span data-stu-id="e4551-417">1400 (0x578)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-418">Identificador de ventana no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-418">Invalid window handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-419"><span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERROR \_ de \_ identificador de menú no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-419"><span id="ERROR_INVALID_MENU_HANDLE"></span><span id="error_invalid_menu_handle"></span>**ERROR\_INVALID\_MENU\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-420">1401 (0x579)</span><span class="sxs-lookup"><span data-stu-id="e4551-420">1401 (0x579)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-421">Identificador de menú no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-421">Invalid menu handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-422"><span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERROR \_ de \_ identificador de cursor no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-422"><span id="ERROR_INVALID_CURSOR_HANDLE"></span><span id="error_invalid_cursor_handle"></span>**ERROR\_INVALID\_CURSOR\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-423">1402 (0x57A)</span><span class="sxs-lookup"><span data-stu-id="e4551-423">1402 (0x57A)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-424">Identificador de cursor no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-424">Invalid cursor handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-425"><span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERROR \_ de \_ controlador de aceleración no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-425"><span id="ERROR_INVALID_ACCEL_HANDLE"></span><span id="error_invalid_accel_handle"></span>**ERROR\_INVALID\_ACCEL\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-426">1403 (0x57B)</span><span class="sxs-lookup"><span data-stu-id="e4551-426">1403 (0x57B)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-427">Identificador de tabla de aceleradores no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-427">Invalid accelerator table handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-428"><span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERROR \_ de \_ identificador de enlace no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-428"><span id="ERROR_INVALID_HOOK_HANDLE"></span><span id="error_invalid_hook_handle"></span>**ERROR\_INVALID\_HOOK\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-429">1404 (0x57C)</span><span class="sxs-lookup"><span data-stu-id="e4551-429">1404 (0x57C)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-430">Identificador de enlace no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-430">Invalid hook handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-431"><span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERROR \_ de \_ identificador DWP no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-431"><span id="ERROR_INVALID_DWP_HANDLE"></span><span id="error_invalid_dwp_handle"></span>**ERROR\_INVALID\_DWP\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-432">1405 (0x57D)</span><span class="sxs-lookup"><span data-stu-id="e4551-432">1405 (0x57D)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-433">Identificador no válido para una estructura de posición de varias ventanas.</span><span class="sxs-lookup"><span data-stu-id="e4551-433">Invalid handle to a multiple-window position structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-434"><span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERROR \_ TLW \_ con \_ WSCHILD**</span><span class="sxs-lookup"><span data-stu-id="e4551-434"><span id="ERROR_TLW_WITH_WSCHILD"></span><span id="error_tlw_with_wschild"></span>**ERROR\_TLW\_WITH\_WSCHILD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-435">1406 (0x57E)</span><span class="sxs-lookup"><span data-stu-id="e4551-435">1406 (0x57E)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-436">No se puede crear una ventana secundaria de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="e4551-436">Cannot create a top-level child window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-437"><span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**ERROR \_ no se \_ encuentra la \_ \_ clase WND**</span><span class="sxs-lookup"><span data-stu-id="e4551-437"><span id="ERROR_CANNOT_FIND_WND_CLASS"></span><span id="error_cannot_find_wnd_class"></span>**ERROR\_CANNOT\_FIND\_WND\_CLASS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-438">1407 (0x57F)</span><span class="sxs-lookup"><span data-stu-id="e4551-438">1407 (0x57F)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-439">No se encuentra la clase de ventana.</span><span class="sxs-lookup"><span data-stu-id="e4551-439">Cannot find window class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-440"><span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**\_ventana \_ de error de \_ otro \_ subproceso**</span><span class="sxs-lookup"><span data-stu-id="e4551-440"><span id="ERROR_WINDOW_OF_OTHER_THREAD"></span><span id="error_window_of_other_thread"></span>**ERROR\_WINDOW\_OF\_OTHER\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-441">1408 (0x580)</span><span class="sxs-lookup"><span data-stu-id="e4551-441">1408 (0x580)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-442">Ventana no válida; pertenece a otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="e4551-442">Invalid window; it belongs to other thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-443"><span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**la \_ tecla de error \_ ya está \_ registrada**</span><span class="sxs-lookup"><span data-stu-id="e4551-443"><span id="ERROR_HOTKEY_ALREADY_REGISTERED"></span><span id="error_hotkey_already_registered"></span>**ERROR\_HOTKEY\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-444">1409 (0x581)</span><span class="sxs-lookup"><span data-stu-id="e4551-444">1409 (0x581)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-445">La tecla de acceso rápido ya está registrada.</span><span class="sxs-lookup"><span data-stu-id="e4551-445">Hot key is already registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-446"><span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**la \_ clase de error \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="e4551-446"><span id="ERROR_CLASS_ALREADY_EXISTS"></span><span id="error_class_already_exists"></span>**ERROR\_CLASS\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-447">1410 (0x582)</span><span class="sxs-lookup"><span data-stu-id="e4551-447">1410 (0x582)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-448">La clase ya existe.</span><span class="sxs-lookup"><span data-stu-id="e4551-448">Class already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-449"><span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**la clase de ERROR no \_ \_ \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="e4551-449"><span id="ERROR_CLASS_DOES_NOT_EXIST"></span><span id="error_class_does_not_exist"></span>**ERROR\_CLASS\_DOES\_NOT\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-450">1411 (0x583)</span><span class="sxs-lookup"><span data-stu-id="e4551-450">1411 (0x583)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-451">La clase no existe.</span><span class="sxs-lookup"><span data-stu-id="e4551-451">Class does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-452"><span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**la \_ clase de error \_ tiene \_ Windows**</span><span class="sxs-lookup"><span data-stu-id="e4551-452"><span id="ERROR_CLASS_HAS_WINDOWS"></span><span id="error_class_has_windows"></span>**ERROR\_CLASS\_HAS\_WINDOWS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-453">1412 (0x584)</span><span class="sxs-lookup"><span data-stu-id="e4551-453">1412 (0x584)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-454">La clase todavía tiene ventanas abiertas.</span><span class="sxs-lookup"><span data-stu-id="e4551-454">Class still has open windows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-455"><span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERROR \_ de \_ índice no válido**</span><span class="sxs-lookup"><span data-stu-id="e4551-455"><span id="ERROR_INVALID_INDEX"></span><span id="error_invalid_index"></span>**ERROR\_INVALID\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-456">1413 (0x585)</span><span class="sxs-lookup"><span data-stu-id="e4551-456">1413 (0x585)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-457">Índice no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-457">Invalid index.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-458"><span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**ERROR \_ de \_ identificador de icono no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-458"><span id="ERROR_INVALID_ICON_HANDLE"></span><span id="error_invalid_icon_handle"></span>**ERROR\_INVALID\_ICON\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-459">1414 (0x586)</span><span class="sxs-lookup"><span data-stu-id="e4551-459">1414 (0x586)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-460">Identificador de icono no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-460">Invalid icon handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-461"><span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**ERROR \_ de \_ Índice de cuadro de diálogo privado \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-461"><span id="ERROR_PRIVATE_DIALOG_INDEX"></span><span id="error_private_dialog_index"></span>**ERROR\_PRIVATE\_DIALOG\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-462">1415 (0x587)</span><span class="sxs-lookup"><span data-stu-id="e4551-462">1415 (0x587)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-463">Usar palabras privadas de la ventana de cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e4551-463">Using private DIALOG window words.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-464"><span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**\_ \_ \_ no \_ se encontró el identificador del cuadro de lista de errores**</span><span class="sxs-lookup"><span data-stu-id="e4551-464"><span id="ERROR_LISTBOX_ID_NOT_FOUND"></span><span id="error_listbox_id_not_found"></span>**ERROR\_LISTBOX\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-465">1416 (0x588)</span><span class="sxs-lookup"><span data-stu-id="e4551-465">1416 (0x588)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-466">No se encontró el identificador del cuadro de lista.</span><span class="sxs-lookup"><span data-stu-id="e4551-466">The list box identifier was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-467"><span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERROR: \_ no hay \_ \_ caracteres comodín**</span><span class="sxs-lookup"><span data-stu-id="e4551-467"><span id="ERROR_NO_WILDCARD_CHARACTERS"></span><span id="error_no_wildcard_characters"></span>**ERROR\_NO\_WILDCARD\_CHARACTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-468">1417 (0x589)</span><span class="sxs-lookup"><span data-stu-id="e4551-468">1417 (0x589)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-469">No se encontraron caracteres comodín.</span><span class="sxs-lookup"><span data-stu-id="e4551-469">No wildcards were found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-470"><span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**ERROR de \_ portapapeles \_ \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="e4551-470"><span id="ERROR_CLIPBOARD_NOT_OPEN"></span><span id="error_clipboard_not_open"></span>**ERROR\_CLIPBOARD\_NOT\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-471">1418 (0x58A)</span><span class="sxs-lookup"><span data-stu-id="e4551-471">1418 (0x58A)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-472">El subproceso no tiene abierto un portapapeles.</span><span class="sxs-lookup"><span data-stu-id="e4551-472">Thread does not have a clipboard open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-473"><span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**la \_ tecla de error \_ no está \_ registrada**</span><span class="sxs-lookup"><span data-stu-id="e4551-473"><span id="ERROR_HOTKEY_NOT_REGISTERED"></span><span id="error_hotkey_not_registered"></span>**ERROR\_HOTKEY\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-474">1419 (0x58B)</span><span class="sxs-lookup"><span data-stu-id="e4551-474">1419 (0x58B)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-475">La tecla de acceso rápido no está registrada.</span><span class="sxs-lookup"><span data-stu-id="e4551-475">Hot key is not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-476"><span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**\_cuadro de \_ \_ diálogo ventana de error**</span><span class="sxs-lookup"><span data-stu-id="e4551-476"><span id="ERROR_WINDOW_NOT_DIALOG"></span><span id="error_window_not_dialog"></span>**ERROR\_WINDOW\_NOT\_DIALOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-477">1420 (0x58C)</span><span class="sxs-lookup"><span data-stu-id="e4551-477">1420 (0x58C)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-478">La ventana no es una ventana de cuadro de diálogo válida.</span><span class="sxs-lookup"><span data-stu-id="e4551-478">The window is not a valid dialog window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-479"><span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**\_ \_ \_ no \_ se encontró el identificador de control de errores**</span><span class="sxs-lookup"><span data-stu-id="e4551-479"><span id="ERROR_CONTROL_ID_NOT_FOUND"></span><span id="error_control_id_not_found"></span>**ERROR\_CONTROL\_ID\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-480">1421 (0x58D)</span><span class="sxs-lookup"><span data-stu-id="e4551-480">1421 (0x58D)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-481">No se encontró el identificador de control.</span><span class="sxs-lookup"><span data-stu-id="e4551-481">Control ID not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-482"><span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**ERROR \_ de \_ mensaje de cuadro combinado no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-482"><span id="ERROR_INVALID_COMBOBOX_MESSAGE"></span><span id="error_invalid_combobox_message"></span>**ERROR\_INVALID\_COMBOBOX\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-483">1422 (0x58E)</span><span class="sxs-lookup"><span data-stu-id="e4551-483">1422 (0x58E)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-484">Mensaje no válido para un cuadro combinado porque no tiene un control de edición.</span><span class="sxs-lookup"><span data-stu-id="e4551-484">Invalid message for a combo box because it does not have an edit control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-485"><span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**ventana de ERROR \_ \_ no \_ ComboBox**</span><span class="sxs-lookup"><span data-stu-id="e4551-485"><span id="ERROR_WINDOW_NOT_COMBOBOX"></span><span id="error_window_not_combobox"></span>**ERROR\_WINDOW\_NOT\_COMBOBOX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-486">1423 (0x58F)</span><span class="sxs-lookup"><span data-stu-id="e4551-486">1423 (0x58F)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-487">La ventana no es un cuadro combinado.</span><span class="sxs-lookup"><span data-stu-id="e4551-487">The window is not a combo box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-488"><span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERROR \_ de \_ edición de alto no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-488"><span id="ERROR_INVALID_EDIT_HEIGHT"></span><span id="error_invalid_edit_height"></span>**ERROR\_INVALID\_EDIT\_HEIGHT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-489">1424 (0x590)</span><span class="sxs-lookup"><span data-stu-id="e4551-489">1424 (0x590)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-490">El alto debe ser inferior a 256.</span><span class="sxs-lookup"><span data-stu-id="e4551-490">Height must be less than 256.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-491"><span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**\_ \_ no \_ se encontró el DC de error**</span><span class="sxs-lookup"><span data-stu-id="e4551-491"><span id="ERROR_DC_NOT_FOUND"></span><span id="error_dc_not_found"></span>**ERROR\_DC\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-492">1425 (0x591)</span><span class="sxs-lookup"><span data-stu-id="e4551-492">1425 (0x591)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-493">Identificador de contexto de dispositivo (DC) no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-493">Invalid device context (DC) handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-494"><span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERROR \_ de \_ filtro de enlace no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-494"><span id="ERROR_INVALID_HOOK_FILTER"></span><span id="error_invalid_hook_filter"></span>**ERROR\_INVALID\_HOOK\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-495">1426 (0x592)</span><span class="sxs-lookup"><span data-stu-id="e4551-495">1426 (0x592)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-496">Tipo de procedimiento de enlace no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-496">Invalid hook procedure type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-497"><span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERROR \_ de \_ filtro no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-497"><span id="ERROR_INVALID_FILTER_PROC"></span><span id="error_invalid_filter_proc"></span>**ERROR\_INVALID\_FILTER\_PROC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-498">1427 (0x593)</span><span class="sxs-lookup"><span data-stu-id="e4551-498">1427 (0x593)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-499">Procedimiento de enlace no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-499">Invalid hook procedure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-500"><span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**el \_ enlace de errores \_ necesita \_ HMOD**</span><span class="sxs-lookup"><span data-stu-id="e4551-500"><span id="ERROR_HOOK_NEEDS_HMOD"></span><span id="error_hook_needs_hmod"></span>**ERROR\_HOOK\_NEEDS\_HMOD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-501">1428 (0x594)</span><span class="sxs-lookup"><span data-stu-id="e4551-501">1428 (0x594)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-502">No se puede establecer un enlace no local sin un identificador de módulo.</span><span class="sxs-lookup"><span data-stu-id="e4551-502">Cannot set nonlocal hook without a module handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-503"><span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**ERROR \_ de \_ enlace solo global \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-503"><span id="ERROR_GLOBAL_ONLY_HOOK"></span><span id="error_global_only_hook"></span>**ERROR\_GLOBAL\_ONLY\_HOOK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-504">1429 (0x595)</span><span class="sxs-lookup"><span data-stu-id="e4551-504">1429 (0x595)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-505">Este procedimiento de enlace solo se puede establecer globalmente.</span><span class="sxs-lookup"><span data-stu-id="e4551-505">This hook procedure can only be set globally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-506"><span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**\_conjunto de \_ enlaces del diario de errores \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-506"><span id="ERROR_JOURNAL_HOOK_SET"></span><span id="error_journal_hook_set"></span>**ERROR\_JOURNAL\_HOOK\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-507">1430 (0x596)</span><span class="sxs-lookup"><span data-stu-id="e4551-507">1430 (0x596)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-508">El procedimiento de enlace del diario ya está instalado.</span><span class="sxs-lookup"><span data-stu-id="e4551-508">The journal hook procedure is already installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-509"><span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**ERROR de \_ enlace \_ no \_ instalado**</span><span class="sxs-lookup"><span data-stu-id="e4551-509"><span id="ERROR_HOOK_NOT_INSTALLED"></span><span id="error_hook_not_installed"></span>**ERROR\_HOOK\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-510">1431 (0x597)</span><span class="sxs-lookup"><span data-stu-id="e4551-510">1431 (0x597)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-511">El procedimiento de enlace no está instalado.</span><span class="sxs-lookup"><span data-stu-id="e4551-511">The hook procedure is not installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-512"><span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERROR \_ de \_ mensaje lb no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-512"><span id="ERROR_INVALID_LB_MESSAGE"></span><span id="error_invalid_lb_message"></span>**ERROR\_INVALID\_LB\_MESSAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-513">1432 (0x598)</span><span class="sxs-lookup"><span data-stu-id="e4551-513">1432 (0x598)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-514">Mensaje no válido para el cuadro de lista de selección única.</span><span class="sxs-lookup"><span data-stu-id="e4551-514">Invalid message for single-selection list box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-515"><span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERROR \_ SETCOUNT \_ en \_ \_ lb**</span><span class="sxs-lookup"><span data-stu-id="e4551-515"><span id="ERROR_SETCOUNT_ON_BAD_LB"></span><span id="error_setcount_on_bad_lb"></span>**ERROR\_SETCOUNT\_ON\_BAD\_LB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-516">1433 (0x599)</span><span class="sxs-lookup"><span data-stu-id="e4551-516">1433 (0x599)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-517">LB \_ SETCOUNT enviado a un cuadro de lista no diferido.</span><span class="sxs-lookup"><span data-stu-id="e4551-517">LB\_SETCOUNT sent to non-lazy list box.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-518"><span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERROR \_ lb \_ sin \_ TABSTOPS**</span><span class="sxs-lookup"><span data-stu-id="e4551-518"><span id="ERROR_LB_WITHOUT_TABSTOPS"></span><span id="error_lb_without_tabstops"></span>**ERROR\_LB\_WITHOUT\_TABSTOPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-519">1434 (0x59A)</span><span class="sxs-lookup"><span data-stu-id="e4551-519">1434 (0x59A)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-520">Este cuadro de lista no admite tabulaciones.</span><span class="sxs-lookup"><span data-stu-id="e4551-520">This list box does not support tab stops.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-521"><span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERROR al \_ destruir el \_ objeto \_ de \_ otro \_ subproceso**</span><span class="sxs-lookup"><span data-stu-id="e4551-521"><span id="ERROR_DESTROY_OBJECT_OF_OTHER_THREAD"></span><span id="error_destroy_object_of_other_thread"></span>**ERROR\_DESTROY\_OBJECT\_OF\_OTHER\_THREAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-522">1435 (0x59B)</span><span class="sxs-lookup"><span data-stu-id="e4551-522">1435 (0x59B)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-523">No se puede destruir el objeto creado por otro subproceso.</span><span class="sxs-lookup"><span data-stu-id="e4551-523">Cannot destroy object created by another thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-524"><span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**\_menú de \_ ventana \_ secundaria de error**</span><span class="sxs-lookup"><span data-stu-id="e4551-524"><span id="ERROR_CHILD_WINDOW_MENU"></span><span id="error_child_window_menu"></span>**ERROR\_CHILD\_WINDOW\_MENU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-525">1436 (0x59C)</span><span class="sxs-lookup"><span data-stu-id="e4551-525">1436 (0x59C)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-526">Las ventanas secundarias no pueden tener menús.</span><span class="sxs-lookup"><span data-stu-id="e4551-526">Child windows cannot have menus.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-527"><span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERROR: \_ no hay \_ menú del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-527"><span id="ERROR_NO_SYSTEM_MENU"></span><span id="error_no_system_menu"></span>**ERROR\_NO\_SYSTEM\_MENU**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-528">1437 (0x59D)</span><span class="sxs-lookup"><span data-stu-id="e4551-528">1437 (0x59D)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-529">La ventana no tiene un menú del sistema.</span><span class="sxs-lookup"><span data-stu-id="e4551-529">The window does not have a system menu.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-530"><span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERROR \_ de \_ estilo de MsgBox no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-530"><span id="ERROR_INVALID_MSGBOX_STYLE"></span><span id="error_invalid_msgbox_style"></span>**ERROR\_INVALID\_MSGBOX\_STYLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-531">1438 (0x59E)</span><span class="sxs-lookup"><span data-stu-id="e4551-531">1438 (0x59E)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-532">Estilo de cuadro de mensaje no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-532">Invalid message box style.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-533"><span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERROR \_ de \_ valor SPI no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-533"><span id="ERROR_INVALID_SPI_VALUE"></span><span id="error_invalid_spi_value"></span>**ERROR\_INVALID\_SPI\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-534">1439 (0x59F)</span><span class="sxs-lookup"><span data-stu-id="e4551-534">1439 (0x59F)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-535">Parámetro de todo el sistema (SPI) no válido \_ \* .</span><span class="sxs-lookup"><span data-stu-id="e4551-535">Invalid system-wide (SPI\_\*) parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-536"><span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**pantalla de ERROR \_ \_ ya \_ bloqueada**</span><span class="sxs-lookup"><span data-stu-id="e4551-536"><span id="ERROR_SCREEN_ALREADY_LOCKED"></span><span id="error_screen_already_locked"></span>**ERROR\_SCREEN\_ALREADY\_LOCKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-537">1440 (0x5A0)</span><span class="sxs-lookup"><span data-stu-id="e4551-537">1440 (0x5A0)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-538">La pantalla ya está bloqueada.</span><span class="sxs-lookup"><span data-stu-id="e4551-538">Screen already locked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-539"><span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**ERROR \_ hWnd \_ tener \_ diff \_ Parent**</span><span class="sxs-lookup"><span data-stu-id="e4551-539"><span id="ERROR_HWNDS_HAVE_DIFF_PARENT"></span><span id="error_hwnds_have_diff_parent"></span>**ERROR\_HWNDS\_HAVE\_DIFF\_PARENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-540">1441 (0x5A1)</span><span class="sxs-lookup"><span data-stu-id="e4551-540">1441 (0x5A1)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-541">Todos los identificadores de Windows en una estructura de posición de varias ventanas deben tener el mismo elemento primario.</span><span class="sxs-lookup"><span data-stu-id="e4551-541">All handles to windows in a multiple-window position structure must have the same parent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-542"><span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**ERROR en la \_ \_ \_ ventana secundaria**</span><span class="sxs-lookup"><span data-stu-id="e4551-542"><span id="ERROR_NOT_CHILD_WINDOW"></span><span id="error_not_child_window"></span>**ERROR\_NOT\_CHILD\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-543">1442 (0x5A2)</span><span class="sxs-lookup"><span data-stu-id="e4551-543">1442 (0x5A2)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-544">La ventana no es una ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="e4551-544">The window is not a child window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-545"><span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERROR \_ de \_ comando GW no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-545"><span id="ERROR_INVALID_GW_COMMAND"></span><span id="error_invalid_gw_command"></span>**ERROR\_INVALID\_GW\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-546">1443 (0x5A3)</span><span class="sxs-lookup"><span data-stu-id="e4551-546">1443 (0x5A3)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-547">Comando de GW no válido \_ \* .</span><span class="sxs-lookup"><span data-stu-id="e4551-547">Invalid GW\_\* command.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-548"><span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**ERROR \_ de \_ ID. de subproceso no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-548"><span id="ERROR_INVALID_THREAD_ID"></span><span id="error_invalid_thread_id"></span>**ERROR\_INVALID\_THREAD\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-549">1444 (0x5A4)</span><span class="sxs-lookup"><span data-stu-id="e4551-549">1444 (0x5A4)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-550">Identificador de subproceso no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-550">Invalid thread identifier.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-551"><span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**ERROR en la \_ \_ ventana no MDICHILD \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-551"><span id="ERROR_NON_MDICHILD_WINDOW"></span><span id="error_non_mdichild_window"></span>**ERROR\_NON\_MDICHILD\_WINDOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-552">1445 (0x5A5)</span><span class="sxs-lookup"><span data-stu-id="e4551-552">1445 (0x5A5)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-553">No se puede procesar un mensaje desde una ventana que no sea una ventana de interfaz de múltiples documentos (MDI).</span><span class="sxs-lookup"><span data-stu-id="e4551-553">Cannot process a message from a window that is not a multiple document interface (MDI) window.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-554"><span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**ERROR \_ emergente \_ ya \_ activo**</span><span class="sxs-lookup"><span data-stu-id="e4551-554"><span id="ERROR_POPUP_ALREADY_ACTIVE"></span><span id="error_popup_already_active"></span>**ERROR\_POPUP\_ALREADY\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-555">1446 (0x5A6)</span><span class="sxs-lookup"><span data-stu-id="e4551-555">1446 (0x5A6)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-556">El menú emergente ya está activo.</span><span class="sxs-lookup"><span data-stu-id="e4551-556">Popup menu already active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-557"><span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERROR: \_ no hay \_ barras de desplazamiento**</span><span class="sxs-lookup"><span data-stu-id="e4551-557"><span id="ERROR_NO_SCROLLBARS"></span><span id="error_no_scrollbars"></span>**ERROR\_NO\_SCROLLBARS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-558">1447 (0x5A7)</span><span class="sxs-lookup"><span data-stu-id="e4551-558">1447 (0x5A7)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-559">La ventana no tiene barras de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="e4551-559">The window does not have scroll bars.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-560"><span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERROR \_ de \_ intervalo de ScrollBar no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-560"><span id="ERROR_INVALID_SCROLLBAR_RANGE"></span><span id="error_invalid_scrollbar_range"></span>**ERROR\_INVALID\_SCROLLBAR\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-561">1448 (0x5A8)</span><span class="sxs-lookup"><span data-stu-id="e4551-561">1448 (0x5A8)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-562">El intervalo de la barra de desplazamiento no puede ser mayor que MAXLONG.</span><span class="sxs-lookup"><span data-stu-id="e4551-562">Scroll bar range cannot be greater than MAXLONG.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-563"><span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERROR \_ de \_ comando SHOWWIN no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-563"><span id="ERROR_INVALID_SHOWWIN_COMMAND"></span><span id="error_invalid_showwin_command"></span>**ERROR\_INVALID\_SHOWWIN\_COMMAND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-564">1449 (0x5A9)</span><span class="sxs-lookup"><span data-stu-id="e4551-564">1449 (0x5A9)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-565">No se puede mostrar o quitar la ventana de la manera especificada.</span><span class="sxs-lookup"><span data-stu-id="e4551-565">Cannot show or remove the window in the way specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-566"><span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERROR: \_ no hay \_ recursos del sistema \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-566"><span id="ERROR_NO_SYSTEM_RESOURCES"></span><span id="error_no_system_resources"></span>**ERROR\_NO\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-567">1450 (0x5AA)</span><span class="sxs-lookup"><span data-stu-id="e4551-567">1450 (0x5AA)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-568">No hay suficientes recursos del sistema para completar el servicio solicitado.</span><span class="sxs-lookup"><span data-stu-id="e4551-568">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-569"><span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ERROR de \_ \_ recursos del sistema no paginados \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-569"><span id="ERROR_NONPAGED_SYSTEM_RESOURCES"></span><span id="error_nonpaged_system_resources"></span>**ERROR\_NONPAGED\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-570">1451 (0x5AB)</span><span class="sxs-lookup"><span data-stu-id="e4551-570">1451 (0x5AB)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-571">No hay suficientes recursos del sistema para completar el servicio solicitado.</span><span class="sxs-lookup"><span data-stu-id="e4551-571">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-572"><span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ERRORES de \_ \_ recursos del sistema paginados \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-572"><span id="ERROR_PAGED_SYSTEM_RESOURCES"></span><span id="error_paged_system_resources"></span>**ERROR\_PAGED\_SYSTEM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-573">1452 (0x5AC)</span><span class="sxs-lookup"><span data-stu-id="e4551-573">1452 (0x5AC)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-574">No hay suficientes recursos del sistema para completar el servicio solicitado.</span><span class="sxs-lookup"><span data-stu-id="e4551-574">Insufficient system resources exist to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-575"><span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**cuota de espacio de trabajo de ERROR \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-575"><span id="ERROR_WORKING_SET_QUOTA"></span><span id="error_working_set_quota"></span>**ERROR\_WORKING\_SET\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-576">1453 (0x5AD)</span><span class="sxs-lookup"><span data-stu-id="e4551-576">1453 (0x5AD)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-577">Cuota insuficiente para completar el servicio solicitado.</span><span class="sxs-lookup"><span data-stu-id="e4551-577">Insufficient quota to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-578"><span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**cuota del archivo de \_ paginación de errores \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-578"><span id="ERROR_PAGEFILE_QUOTA"></span><span id="error_pagefile_quota"></span>**ERROR\_PAGEFILE\_QUOTA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-579">1454 (0x5AE)</span><span class="sxs-lookup"><span data-stu-id="e4551-579">1454 (0x5AE)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-580">Cuota insuficiente para completar el servicio solicitado.</span><span class="sxs-lookup"><span data-stu-id="e4551-580">Insufficient quota to complete the requested service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-581"><span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**\_límite de compromiso de error \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-581"><span id="ERROR_COMMITMENT_LIMIT"></span><span id="error_commitment_limit"></span>**ERROR\_COMMITMENT\_LIMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-582">1455 (0x5AF)</span><span class="sxs-lookup"><span data-stu-id="e4551-582">1455 (0x5AF)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-583">El archivo de paginación es demasiado pequeño para que se complete esta operación.</span><span class="sxs-lookup"><span data-stu-id="e4551-583">The paging file is too small for this operation to complete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-584"><span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**\_ \_ \_ no \_ se encontró el elemento de menú de error**</span><span class="sxs-lookup"><span data-stu-id="e4551-584"><span id="ERROR_MENU_ITEM_NOT_FOUND"></span><span id="error_menu_item_not_found"></span>**ERROR\_MENU\_ITEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-585">1456 (0x5B0)</span><span class="sxs-lookup"><span data-stu-id="e4551-585">1456 (0x5B0)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-586">No se encontró un elemento de menú.</span><span class="sxs-lookup"><span data-stu-id="e4551-586">A menu item was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-587"><span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERROR \_ de \_ identificador de teclado no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-587"><span id="ERROR_INVALID_KEYBOARD_HANDLE"></span><span id="error_invalid_keyboard_handle"></span>**ERROR\_INVALID\_KEYBOARD\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-588">1457 (0x5B1)</span><span class="sxs-lookup"><span data-stu-id="e4551-588">1457 (0x5B1)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-589">Controlador de distribución de teclado no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-589">Invalid keyboard layout handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-590"><span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**tipo de enlace de ERROR \_ \_ \_ no \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="e4551-590"><span id="ERROR_HOOK_TYPE_NOT_ALLOWED"></span><span id="error_hook_type_not_allowed"></span>**ERROR\_HOOK\_TYPE\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-591">1458 (0x5B2)</span><span class="sxs-lookup"><span data-stu-id="e4551-591">1458 (0x5B2)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-592">Tipo de enlace no permitido.</span><span class="sxs-lookup"><span data-stu-id="e4551-592">Hook type not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-593"><span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**el ERROR \_ requiere \_ WINDOWSTATION interactivos \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-593"><span id="ERROR_REQUIRES_INTERACTIVE_WINDOWSTATION"></span><span id="error_requires_interactive_windowstation"></span>**ERROR\_REQUIRES\_INTERACTIVE\_WINDOWSTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-594">1459 (0x5B3)</span><span class="sxs-lookup"><span data-stu-id="e4551-594">1459 (0x5B3)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-595">Esta operación requiere una estación de ventana interactiva.</span><span class="sxs-lookup"><span data-stu-id="e4551-595">This operation requires an interactive window station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-596"><span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**tiempo de espera de ERROR \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-596"><span id="ERROR_TIMEOUT"></span><span id="error_timeout"></span>**ERROR\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-597">1460 (0x5B4)</span><span class="sxs-lookup"><span data-stu-id="e4551-597">1460 (0x5B4)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-598">Esta operación devolvió porque expiró el período de tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="e4551-598">This operation returned because the timeout period expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-599"><span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERROR \_ de \_ identificador de monitor no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-599"><span id="ERROR_INVALID_MONITOR_HANDLE"></span><span id="error_invalid_monitor_handle"></span>**ERROR\_INVALID\_MONITOR\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-600">1461 (0x5B5)</span><span class="sxs-lookup"><span data-stu-id="e4551-600">1461 (0x5B5)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-601">Identificador de monitor no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-601">Invalid monitor handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-602"><span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**ERROR \_ de \_ tamaño incorrecto**</span><span class="sxs-lookup"><span data-stu-id="e4551-602"><span id="ERROR_INCORRECT_SIZE"></span><span id="error_incorrect_size"></span>**ERROR\_INCORRECT\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-603">1462 (0x5B6)</span><span class="sxs-lookup"><span data-stu-id="e4551-603">1462 (0x5B6)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-604">Argumento de tamaño incorrecto.</span><span class="sxs-lookup"><span data-stu-id="e4551-604">Incorrect size argument.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-605"><span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**\_clase SYMLINK de error \_ \_ deshabilitada**</span><span class="sxs-lookup"><span data-stu-id="e4551-605"><span id="ERROR_SYMLINK_CLASS_DISABLED"></span><span id="error_symlink_class_disabled"></span>**ERROR\_SYMLINK\_CLASS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-606">1463 (0x5B7)</span><span class="sxs-lookup"><span data-stu-id="e4551-606">1463 (0x5B7)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-607">No se puede seguir el vínculo simbólico porque su tipo está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="e4551-607">The symbolic link cannot be followed because its type is disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-608"><span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**ERROR \_ SYMLINK \_ no \_ admitido**</span><span class="sxs-lookup"><span data-stu-id="e4551-608"><span id="ERROR_SYMLINK_NOT_SUPPORTED"></span><span id="error_symlink_not_supported"></span>**ERROR\_SYMLINK\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-609">1464 (0x5B8)</span><span class="sxs-lookup"><span data-stu-id="e4551-609">1464 (0x5B8)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-610">Esta aplicación no admite la operación actual en vínculos simbólicos.</span><span class="sxs-lookup"><span data-stu-id="e4551-610">This application does not support the current operation on symbolic links.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-611"><span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**error de \_ análisis de XML de error \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-611"><span id="ERROR_XML_PARSE_ERROR"></span><span id="error_xml_parse_error"></span>**ERROR\_XML\_PARSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-612">1465 (0x5B9)</span><span class="sxs-lookup"><span data-stu-id="e4551-612">1465 (0x5B9)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-613">Windows no pudo analizar los datos XML solicitados.</span><span class="sxs-lookup"><span data-stu-id="e4551-613">Windows was unable to parse the requested XML data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-614"><span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**error \_ XMLDSIG de error \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-614"><span id="ERROR_XMLDSIG_ERROR"></span><span id="error_xmldsig_error"></span>**ERROR\_XMLDSIG\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-615">1466 (0x5BA)</span><span class="sxs-lookup"><span data-stu-id="e4551-615">1466 (0x5BA)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-616">Se encontró un error al procesar una firma digital XML.</span><span class="sxs-lookup"><span data-stu-id="e4551-616">An error was encountered while processing an XML digital signature.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-617"><span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**ERROR al \_ reiniciar la \_ aplicación**</span><span class="sxs-lookup"><span data-stu-id="e4551-617"><span id="ERROR_RESTART_APPLICATION"></span><span id="error_restart_application"></span>**ERROR\_RESTART\_APPLICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-618">1467 (0x5BB)</span><span class="sxs-lookup"><span data-stu-id="e4551-618">1467 (0x5BB)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-619">Esta aplicación debe reiniciarse.</span><span class="sxs-lookup"><span data-stu-id="e4551-619">This application must be restarted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-620"><span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**\_compartimiento incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-620"><span id="ERROR_WRONG_COMPARTMENT"></span><span id="error_wrong_compartment"></span>**ERROR\_WRONG\_COMPARTMENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-621">1468 (0x5BC)</span><span class="sxs-lookup"><span data-stu-id="e4551-621">1468 (0x5BC)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-622">El autor de la llamada realizó la solicitud de conexión en el compartimiento de enrutamiento equivocado.</span><span class="sxs-lookup"><span data-stu-id="e4551-622">The caller made the connection request in the wrong routing compartment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-623"><span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERROR de \_ AUTHIP \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-623"><span id="ERROR_AUTHIP_FAILURE"></span><span id="error_authip_failure"></span>**ERROR\_AUTHIP\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-624">1469 (0x5BD)</span><span class="sxs-lookup"><span data-stu-id="e4551-624">1469 (0x5BD)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-625">Error de AuthIP al intentar conectarse al host remoto.</span><span class="sxs-lookup"><span data-stu-id="e4551-625">There was an AuthIP failure when attempting to connect to the remote host.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-626"><span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERROR: \_ no hay \_ \_ recursos NVRAM**</span><span class="sxs-lookup"><span data-stu-id="e4551-626"><span id="ERROR_NO_NVRAM_RESOURCES"></span><span id="error_no_nvram_resources"></span>**ERROR\_NO\_NVRAM\_RESOURCES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-627">1470 (0x5BE)</span><span class="sxs-lookup"><span data-stu-id="e4551-627">1470 (0x5BE)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-628">No existen recursos NVRAM suficientes para completar el servicio solicitado.</span><span class="sxs-lookup"><span data-stu-id="e4551-628">Insufficient NVRAM resources exist to complete the requested service.</span></span> <span data-ttu-id="e4551-629">Es posible que se necesite un reinicio.</span><span class="sxs-lookup"><span data-stu-id="e4551-629">A reboot might be required.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-630"><span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**ERROR \_ de \_ proceso de GUI \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-630"><span id="ERROR_NOT_GUI_PROCESS"></span><span id="error_not_gui_process"></span>**ERROR\_NOT\_GUI\_PROCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-631">1471 (0x5BF)</span><span class="sxs-lookup"><span data-stu-id="e4551-631">1471 (0x5BF)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-632">No se puede finalizar la operación solicitada porque el proceso especificado no es un proceso de GUI.</span><span class="sxs-lookup"><span data-stu-id="e4551-632">Unable to finish the requested operation because the specified process is not a GUI process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-633"><span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**el \_ archivo EVENTLOG de error \_ \_ está dañado**</span><span class="sxs-lookup"><span data-stu-id="e4551-633"><span id="ERROR_EVENTLOG_FILE_CORRUPT"></span><span id="error_eventlog_file_corrupt"></span>**ERROR\_EVENTLOG\_FILE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-634">1500 (0x5DC)</span><span class="sxs-lookup"><span data-stu-id="e4551-634">1500 (0x5DC)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-635">El archivo de registro de eventos está dañado.</span><span class="sxs-lookup"><span data-stu-id="e4551-635">The event log file is corrupted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-636"><span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**ERROR \_ al \_ \_ iniciar EVENTLOG**</span><span class="sxs-lookup"><span data-stu-id="e4551-636"><span id="ERROR_EVENTLOG_CANT_START"></span><span id="error_eventlog_cant_start"></span>**ERROR\_EVENTLOG\_CANT\_START**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-637">1501 (0x5DD)</span><span class="sxs-lookup"><span data-stu-id="e4551-637">1501 (0x5DD)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-638">No se pudo abrir ningún archivo de registro de eventos, por lo que no se inició el servicio de registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="e4551-638">No event log file could be opened, so the event logging service did not start.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-639"><span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**archivo de registro de errores \_ \_ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="e4551-639"><span id="ERROR_LOG_FILE_FULL"></span><span id="error_log_file_full"></span>**ERROR\_LOG\_FILE\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-640">1502 (0x5DE)</span><span class="sxs-lookup"><span data-stu-id="e4551-640">1502 (0x5DE)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-641">El archivo de registro de eventos está lleno.</span><span class="sxs-lookup"><span data-stu-id="e4551-641">The event log file is full.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-642"><span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**el \_ archivo EVENTLOG de error \_ \_ cambió**</span><span class="sxs-lookup"><span data-stu-id="e4551-642"><span id="ERROR_EVENTLOG_FILE_CHANGED"></span><span id="error_eventlog_file_changed"></span>**ERROR\_EVENTLOG\_FILE\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-643">1503 (0x5DF)</span><span class="sxs-lookup"><span data-stu-id="e4551-643">1503 (0x5DF)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-644">El archivo de registro de eventos ha cambiado entre las operaciones de lectura.</span><span class="sxs-lookup"><span data-stu-id="e4551-644">The event log file has changed between read operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-645"><span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**ERROR \_ de \_ nombre de tarea no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-645"><span id="ERROR_INVALID_TASK_NAME"></span><span id="error_invalid_task_name"></span>**ERROR\_INVALID\_TASK\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-646">1550 (0x60E)</span><span class="sxs-lookup"><span data-stu-id="e4551-646">1550 (0x60E)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-647">El nombre de tarea especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-647">The specified task name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-648"><span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERROR \_ de \_ Índice de tarea no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-648"><span id="ERROR_INVALID_TASK_INDEX"></span><span id="error_invalid_task_index"></span>**ERROR\_INVALID\_TASK\_INDEX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-649">1551 (0x60F)</span><span class="sxs-lookup"><span data-stu-id="e4551-649">1551 (0x60F)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-650">El índice de tarea especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-650">The specified task index is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-651"><span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**el \_ subproceso \_ de error ya está \_ en la \_ tarea**</span><span class="sxs-lookup"><span data-stu-id="e4551-651"><span id="ERROR_THREAD_ALREADY_IN_TASK"></span><span id="error_thread_already_in_task"></span>**ERROR\_THREAD\_ALREADY\_IN\_TASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-652">1552 (0x610)</span><span class="sxs-lookup"><span data-stu-id="e4551-652">1552 (0x610)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-653">El subproceso especificado ya está uniendo una tarea.</span><span class="sxs-lookup"><span data-stu-id="e4551-653">The specified thread is already joining a task.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-654"><span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERROR al \_ instalar el \_ servicio \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-654"><span id="ERROR_INSTALL_SERVICE_FAILURE"></span><span id="error_install_service_failure"></span>**ERROR\_INSTALL\_SERVICE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-655">1601 (0x641)</span><span class="sxs-lookup"><span data-stu-id="e4551-655">1601 (0x641)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-656">No se pudo obtener acceso al servicio Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e4551-656">The Windows Installer Service could not be accessed.</span></span> <span data-ttu-id="e4551-657">Esto puede ocurrir si el Windows Installer no está correctamente instalado.</span><span class="sxs-lookup"><span data-stu-id="e4551-657">This can occur if the Windows Installer is not correctly installed.</span></span> <span data-ttu-id="e4551-658">Póngase en contacto con el personal de soporte técnico para obtener ayuda.</span><span class="sxs-lookup"><span data-stu-id="e4551-658">Contact your support personnel for assistance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-659"><span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERROR al \_ instalar \_ USEREXIT**</span><span class="sxs-lookup"><span data-stu-id="e4551-659"><span id="ERROR_INSTALL_USEREXIT"></span><span id="error_install_userexit"></span>**ERROR\_INSTALL\_USEREXIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-660">1602 (0x642)</span><span class="sxs-lookup"><span data-stu-id="e4551-660">1602 (0x642)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-661">El usuario canceló la instalación.</span><span class="sxs-lookup"><span data-stu-id="e4551-661">User cancelled installation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-662"><span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**ERROR de instalación de ERROR \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-662"><span id="ERROR_INSTALL_FAILURE"></span><span id="error_install_failure"></span>**ERROR\_INSTALL\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-663">1603 (0x643)</span><span class="sxs-lookup"><span data-stu-id="e4551-663">1603 (0x643)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-664">Error irrecuperable durante la instalación.</span><span class="sxs-lookup"><span data-stu-id="e4551-664">Fatal error during installation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-665"><span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERROR de \_ instalación de \_ suspensión**</span><span class="sxs-lookup"><span data-stu-id="e4551-665"><span id="ERROR_INSTALL_SUSPEND"></span><span id="error_install_suspend"></span>**ERROR\_INSTALL\_SUSPEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-666">1604 (0x644)</span><span class="sxs-lookup"><span data-stu-id="e4551-666">1604 (0x644)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-667">Instalación suspendida, incompleta.</span><span class="sxs-lookup"><span data-stu-id="e4551-667">Installation suspended, incomplete.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-668"><span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERROR \_ desconocido del \_ producto**</span><span class="sxs-lookup"><span data-stu-id="e4551-668"><span id="ERROR_UNKNOWN_PRODUCT"></span><span id="error_unknown_product"></span>**ERROR\_UNKNOWN\_PRODUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-669">1605 (0x645)</span><span class="sxs-lookup"><span data-stu-id="e4551-669">1605 (0x645)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-670">Esta acción solo es válida para los productos que están instalados actualmente.</span><span class="sxs-lookup"><span data-stu-id="e4551-670">This action is only valid for products that are currently installed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-671"><span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**ERROR \_ de \_ característica desconocida**</span><span class="sxs-lookup"><span data-stu-id="e4551-671"><span id="ERROR_UNKNOWN_FEATURE"></span><span id="error_unknown_feature"></span>**ERROR\_UNKNOWN\_FEATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-672">1606 (0x646)</span><span class="sxs-lookup"><span data-stu-id="e4551-672">1606 (0x646)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-673">IDENTIFICADOR de característica no registrado.</span><span class="sxs-lookup"><span data-stu-id="e4551-673">Feature ID not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-674"><span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**ERROR \_ de \_ componente desconocido**</span><span class="sxs-lookup"><span data-stu-id="e4551-674"><span id="ERROR_UNKNOWN_COMPONENT"></span><span id="error_unknown_component"></span>**ERROR\_UNKNOWN\_COMPONENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-675">1607 (0x647)</span><span class="sxs-lookup"><span data-stu-id="e4551-675">1607 (0x647)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-676">IDENTIFICADOR de componente no registrado.</span><span class="sxs-lookup"><span data-stu-id="e4551-676">Component ID not registered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-677"><span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERROR \_ desconocido \_ (propiedad)**</span><span class="sxs-lookup"><span data-stu-id="e4551-677"><span id="ERROR_UNKNOWN_PROPERTY"></span><span id="error_unknown_property"></span>**ERROR\_UNKNOWN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-678">1608 (0x648)</span><span class="sxs-lookup"><span data-stu-id="e4551-678">1608 (0x648)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-679">Propiedad desconocida.</span><span class="sxs-lookup"><span data-stu-id="e4551-679">Unknown property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-680"><span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERROR \_ de \_ Estado de identificador no válido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-680"><span id="ERROR_INVALID_HANDLE_STATE"></span><span id="error_invalid_handle_state"></span>**ERROR\_INVALID\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-681">1609 (0x649)</span><span class="sxs-lookup"><span data-stu-id="e4551-681">1609 (0x649)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-682">El identificador está en un estado no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-682">Handle is in an invalid state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-683"><span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERROR \_ de \_ Configuración incorrecta**</span><span class="sxs-lookup"><span data-stu-id="e4551-683"><span id="ERROR_BAD_CONFIGURATION"></span><span id="error_bad_configuration"></span>**ERROR\_BAD\_CONFIGURATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-684">1610 (0x64A)</span><span class="sxs-lookup"><span data-stu-id="e4551-684">1610 (0x64A)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-685">Los datos de configuración de este producto están dañados.</span><span class="sxs-lookup"><span data-stu-id="e4551-685">The configuration data for this product is corrupt.</span></span> <span data-ttu-id="e4551-686">Póngase en contacto con el personal de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="e4551-686">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-687"><span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**Índice de ERROR \_ \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="e4551-687"><span id="ERROR_INDEX_ABSENT"></span><span id="error_index_absent"></span>**ERROR\_INDEX\_ABSENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-688">1611 (0x64B)</span><span class="sxs-lookup"><span data-stu-id="e4551-688">1611 (0x64B)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-689">El calificador de componente no está presente.</span><span class="sxs-lookup"><span data-stu-id="e4551-689">Component qualifier not present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-690"><span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**origen de instalación de ERROR \_ \_ \_ ausente**</span><span class="sxs-lookup"><span data-stu-id="e4551-690"><span id="ERROR_INSTALL_SOURCE_ABSENT"></span><span id="error_install_source_absent"></span>**ERROR\_INSTALL\_SOURCE\_ABSENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-691">1612 (0x64C)</span><span class="sxs-lookup"><span data-stu-id="e4551-691">1612 (0x64C)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-692">El origen de instalación de este producto no está disponible.</span><span class="sxs-lookup"><span data-stu-id="e4551-692">The installation source for this product is not available.</span></span> <span data-ttu-id="e4551-693">Compruebe que el origen existe y que puede acceder a él.</span><span class="sxs-lookup"><span data-stu-id="e4551-693">Verify that the source exists and that you can access it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-694"><span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERROR al \_ instalar la \_ versión del paquete \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-694"><span id="ERROR_INSTALL_PACKAGE_VERSION"></span><span id="error_install_package_version"></span>**ERROR\_INSTALL\_PACKAGE\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-695">1613 (0x64D)</span><span class="sxs-lookup"><span data-stu-id="e4551-695">1613 (0x64D)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-696">El servicio Windows Installer no puede instalar este paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="e4551-696">This installation package cannot be installed by the Windows Installer service.</span></span> <span data-ttu-id="e4551-697">Debe instalar un Service Pack de Windows que contenga una versión más reciente del servicio Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e4551-697">You must install a Windows service pack that contains a newer version of the Windows Installer service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-698"><span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**producto de ERROR \_ \_ desinstalado**</span><span class="sxs-lookup"><span data-stu-id="e4551-698"><span id="ERROR_PRODUCT_UNINSTALLED"></span><span id="error_product_uninstalled"></span>**ERROR\_PRODUCT\_UNINSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-699">1614 (0x64E)</span><span class="sxs-lookup"><span data-stu-id="e4551-699">1614 (0x64E)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-700">El producto se desinstala.</span><span class="sxs-lookup"><span data-stu-id="e4551-700">Product is uninstalled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-701"><span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**ERROR \_ de \_ Sintaxis de consulta incorrecta \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-701"><span id="ERROR_BAD_QUERY_SYNTAX"></span><span id="error_bad_query_syntax"></span>**ERROR\_BAD\_QUERY\_SYNTAX**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-702">1615 (0x64F)</span><span class="sxs-lookup"><span data-stu-id="e4551-702">1615 (0x64F)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-703">Sintaxis de consulta SQL no válida o no admitida.</span><span class="sxs-lookup"><span data-stu-id="e4551-703">SQL query syntax invalid or unsupported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-704"><span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**ERROR \_ de \_ campo no válido**</span><span class="sxs-lookup"><span data-stu-id="e4551-704"><span id="ERROR_INVALID_FIELD"></span><span id="error_invalid_field"></span>**ERROR\_INVALID\_FIELD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-705">1616 (0x650)</span><span class="sxs-lookup"><span data-stu-id="e4551-705">1616 (0x650)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-706">El campo de registro no existe.</span><span class="sxs-lookup"><span data-stu-id="e4551-706">Record field does not exist.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-707"><span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**dispositivo de ERROR \_ \_ quitado**</span><span class="sxs-lookup"><span data-stu-id="e4551-707"><span id="ERROR_DEVICE_REMOVED"></span><span id="error_device_removed"></span>**ERROR\_DEVICE\_REMOVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-708">1617 (0x651)</span><span class="sxs-lookup"><span data-stu-id="e4551-708">1617 (0x651)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-709">Se ha quitado el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e4551-709">The device has been removed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-710"><span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**la \_ instalación de error \_ ya se \_ está ejecutando**</span><span class="sxs-lookup"><span data-stu-id="e4551-710"><span id="ERROR_INSTALL_ALREADY_RUNNING"></span><span id="error_install_already_running"></span>**ERROR\_INSTALL\_ALREADY\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-711">1618 (0x652)</span><span class="sxs-lookup"><span data-stu-id="e4551-711">1618 (0x652)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-712">Ya hay otra instalación en curso.</span><span class="sxs-lookup"><span data-stu-id="e4551-712">Another installation is already in progress.</span></span> <span data-ttu-id="e4551-713">Complete esa instalación antes de continuar con la instalación.</span><span class="sxs-lookup"><span data-stu-id="e4551-713">Complete that installation before proceeding with this install.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-714"><span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERROR \_ \_ al abrir el paquete de instalación \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-714"><span id="ERROR_INSTALL_PACKAGE_OPEN_FAILED"></span><span id="error_install_package_open_failed"></span>**ERROR\_INSTALL\_PACKAGE\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-715">1619 (0x653)</span><span class="sxs-lookup"><span data-stu-id="e4551-715">1619 (0x653)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-716">No se pudo abrir este paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="e4551-716">This installation package could not be opened.</span></span> <span data-ttu-id="e4551-717">Compruebe que el paquete existe y que puede acceder a él, o póngase en contacto con el proveedor de la aplicación para comprobar que se trata de un paquete de Windows Installer válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-717">Verify that the package exists and that you can access it, or contact the application vendor to verify that this is a valid Windows Installer package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-718"><span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERROR al \_ instalar el \_ paquete \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="e4551-718"><span id="ERROR_INSTALL_PACKAGE_INVALID"></span><span id="error_install_package_invalid"></span>**ERROR\_INSTALL\_PACKAGE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-719">1620 (0x654)</span><span class="sxs-lookup"><span data-stu-id="e4551-719">1620 (0x654)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-720">No se pudo abrir este paquete de instalación.</span><span class="sxs-lookup"><span data-stu-id="e4551-720">This installation package could not be opened.</span></span> <span data-ttu-id="e4551-721">Póngase en contacto con el proveedor de la aplicación para comprobar que se trata de un paquete de Windows Installer válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-721">Contact the application vendor to verify that this is a valid Windows Installer package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-722"><span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERROR de instalación de ERROR de \_ \_ UI \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-722"><span id="ERROR_INSTALL_UI_FAILURE"></span><span id="error_install_ui_failure"></span>**ERROR\_INSTALL\_UI\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-723">1621 (0x655)</span><span class="sxs-lookup"><span data-stu-id="e4551-723">1621 (0x655)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-724">Error al iniciar la interfaz de usuario del servicio de Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e4551-724">There was an error starting the Windows Installer service user interface.</span></span> <span data-ttu-id="e4551-725">Póngase en contacto con el personal de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="e4551-725">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-726"><span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**ERROR de \_ registro de instalación de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-726"><span id="ERROR_INSTALL_LOG_FAILURE"></span><span id="error_install_log_failure"></span>**ERROR\_INSTALL\_LOG\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-727">1622 (0x656)</span><span class="sxs-lookup"><span data-stu-id="e4551-727">1622 (0x656)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-728">Error al abrir el archivo de registro de instalación.</span><span class="sxs-lookup"><span data-stu-id="e4551-728">Error opening installation log file.</span></span> <span data-ttu-id="e4551-729">Compruebe que la ubicación del archivo de registro especificada existe y que puede escribir en ella.</span><span class="sxs-lookup"><span data-stu-id="e4551-729">Verify that the specified log file location exists and that you can write to it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-730"><span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**\_no se \_ admite el idioma de instalación de errores \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-730"><span id="ERROR_INSTALL_LANGUAGE_UNSUPPORTED"></span><span id="error_install_language_unsupported"></span>**ERROR\_INSTALL\_LANGUAGE\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-731">1623 (0x657)</span><span class="sxs-lookup"><span data-stu-id="e4551-731">1623 (0x657)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-732">El idioma de este paquete de instalación no es compatible con el sistema.</span><span class="sxs-lookup"><span data-stu-id="e4551-732">The language of this installation package is not supported by your system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-733"><span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**ERROR al \_ instalar la \_ transformación \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-733"><span id="ERROR_INSTALL_TRANSFORM_FAILURE"></span><span id="error_install_transform_failure"></span>**ERROR\_INSTALL\_TRANSFORM\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-734">1624 (0x658)</span><span class="sxs-lookup"><span data-stu-id="e4551-734">1624 (0x658)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-735">Error al aplicar transformaciones.</span><span class="sxs-lookup"><span data-stu-id="e4551-735">Error applying transforms.</span></span> <span data-ttu-id="e4551-736">Compruebe que las rutas de acceso de transformación especificadas son válidas.</span><span class="sxs-lookup"><span data-stu-id="e4551-736">Verify that the specified transform paths are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-737"><span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERROR de \_ instalación de \_ paquete \_ rechazado**</span><span class="sxs-lookup"><span data-stu-id="e4551-737"><span id="ERROR_INSTALL_PACKAGE_REJECTED"></span><span id="error_install_package_rejected"></span>**ERROR\_INSTALL\_PACKAGE\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-738">1625 (0x659)</span><span class="sxs-lookup"><span data-stu-id="e4551-738">1625 (0x659)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-739">Esta instalación está prohibida por la Directiva del sistema.</span><span class="sxs-lookup"><span data-stu-id="e4551-739">This installation is forbidden by system policy.</span></span> <span data-ttu-id="e4551-740">Póngase en contacto con el administrador del sistema.</span><span class="sxs-lookup"><span data-stu-id="e4551-740">Contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-741"><span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**función de ERROR \_ \_ no \_ llamada**</span><span class="sxs-lookup"><span data-stu-id="e4551-741"><span id="ERROR_FUNCTION_NOT_CALLED"></span><span id="error_function_not_called"></span>**ERROR\_FUNCTION\_NOT\_CALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-742">1626 (0x65A)</span><span class="sxs-lookup"><span data-stu-id="e4551-742">1626 (0x65A)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-743">No se pudo ejecutar la función.</span><span class="sxs-lookup"><span data-stu-id="e4551-743">Function could not be executed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-744"><span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**ERROR en la \_ función error \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-744"><span id="ERROR_FUNCTION_FAILED"></span><span id="error_function_failed"></span>**ERROR\_FUNCTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-745">1627 (0x65B)</span><span class="sxs-lookup"><span data-stu-id="e4551-745">1627 (0x65B)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-746">Error de la función durante la ejecución.</span><span class="sxs-lookup"><span data-stu-id="e4551-746">Function failed during execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-747"><span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**ERROR \_ de \_ tabla no válida**</span><span class="sxs-lookup"><span data-stu-id="e4551-747"><span id="ERROR_INVALID_TABLE"></span><span id="error_invalid_table"></span>**ERROR\_INVALID\_TABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-748">1628 (0x65C)</span><span class="sxs-lookup"><span data-stu-id="e4551-748">1628 (0x65C)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-749">Se especificó una tabla no válida o desconocida.</span><span class="sxs-lookup"><span data-stu-id="e4551-749">Invalid or unknown table specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-750"><span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**ERROR de \_ coincidencia de tipo de mensaje \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-750"><span id="ERROR_DATATYPE_MISMATCH"></span><span id="error_datatype_mismatch"></span>**ERROR\_DATATYPE\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-751">1629 (0x65D)</span><span class="sxs-lookup"><span data-stu-id="e4551-751">1629 (0x65D)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-752">Los datos proporcionados son de un tipo incorrecto.</span><span class="sxs-lookup"><span data-stu-id="e4551-752">Data supplied is of wrong type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-753"><span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**ERROR de \_ tipo no compatible \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-753"><span id="ERROR_UNSUPPORTED_TYPE"></span><span id="error_unsupported_type"></span>**ERROR\_UNSUPPORTED\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-754">1630 (0x65E)</span><span class="sxs-lookup"><span data-stu-id="e4551-754">1630 (0x65E)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-755">No se admiten los datos de este tipo.</span><span class="sxs-lookup"><span data-stu-id="e4551-755">Data of this type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-756"><span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**ERROR \_ al crear error \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-756"><span id="ERROR_CREATE_FAILED"></span><span id="error_create_failed"></span>**ERROR\_CREATE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-757">1631 (0x65F)</span><span class="sxs-lookup"><span data-stu-id="e4551-757">1631 (0x65F)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-758">No se pudo iniciar el servicio Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e4551-758">The Windows Installer service failed to start.</span></span> <span data-ttu-id="e4551-759">Póngase en contacto con el personal de soporte técnico.</span><span class="sxs-lookup"><span data-stu-id="e4551-759">Contact your support personnel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-760"><span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERROR al \_ instalar \_ temp no \_ interescribible**</span><span class="sxs-lookup"><span data-stu-id="e4551-760"><span id="ERROR_INSTALL_TEMP_UNWRITABLE"></span><span id="error_install_temp_unwritable"></span>**ERROR\_INSTALL\_TEMP\_UNWRITABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-761">1632 (0x660)</span><span class="sxs-lookup"><span data-stu-id="e4551-761">1632 (0x660)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-762">La carpeta Temp está en una unidad que está llena o es inaccesible.</span><span class="sxs-lookup"><span data-stu-id="e4551-762">The Temp folder is on a drive that is full or is inaccessible.</span></span> <span data-ttu-id="e4551-763">Libere espacio en la unidad o Compruebe que tiene permiso de escritura en la carpeta Temp.</span><span class="sxs-lookup"><span data-stu-id="e4551-763">Free up space on the drive or verify that you have write permission on the Temp folder.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-764"><span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERROR al \_ instalar la \_ plataforma \_ no compatible**</span><span class="sxs-lookup"><span data-stu-id="e4551-764"><span id="ERROR_INSTALL_PLATFORM_UNSUPPORTED"></span><span id="error_install_platform_unsupported"></span>**ERROR\_INSTALL\_PLATFORM\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-765">1633 (0x661)</span><span class="sxs-lookup"><span data-stu-id="e4551-765">1633 (0x661)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-766">Este paquete de instalación no es compatible con este tipo de procesador.</span><span class="sxs-lookup"><span data-stu-id="e4551-766">This installation package is not supported by this processor type.</span></span> <span data-ttu-id="e4551-767">Póngase en contacto con el fabricante del producto.</span><span class="sxs-lookup"><span data-stu-id="e4551-767">Contact your product vendor.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-768"><span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERROR al \_ instalar \_ NOTUSED**</span><span class="sxs-lookup"><span data-stu-id="e4551-768"><span id="ERROR_INSTALL_NOTUSED"></span><span id="error_install_notused"></span>**ERROR\_INSTALL\_NOTUSED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-769">1634 (0x662)</span><span class="sxs-lookup"><span data-stu-id="e4551-769">1634 (0x662)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-770">Componente no usado en este equipo.</span><span class="sxs-lookup"><span data-stu-id="e4551-770">Component not used on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-771"><span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**ERROR \_ \_ al abrir el paquete de revisión de \_ errores \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-771"><span id="ERROR_PATCH_PACKAGE_OPEN_FAILED"></span><span id="error_patch_package_open_failed"></span>**ERROR\_PATCH\_PACKAGE\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-772">1635 (0x663)</span><span class="sxs-lookup"><span data-stu-id="e4551-772">1635 (0x663)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-773">No se pudo abrir este paquete de actualización.</span><span class="sxs-lookup"><span data-stu-id="e4551-773">This update package could not be opened.</span></span> <span data-ttu-id="e4551-774">Compruebe que el paquete de actualización existe y que puede acceder a él, o póngase en contacto con el proveedor de la aplicación para comprobar que se trata de un paquete de actualización de Windows Installer válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-774">Verify that the update package exists and that you can access it, or contact the application vendor to verify that this is a valid Windows Installer update package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-775"><span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**paquete de revisión de ERROR \_ \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="e4551-775"><span id="ERROR_PATCH_PACKAGE_INVALID"></span><span id="error_patch_package_invalid"></span>**ERROR\_PATCH\_PACKAGE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-776">1636 (0x664)</span><span class="sxs-lookup"><span data-stu-id="e4551-776">1636 (0x664)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-777">No se pudo abrir este paquete de actualización.</span><span class="sxs-lookup"><span data-stu-id="e4551-777">This update package could not be opened.</span></span> <span data-ttu-id="e4551-778">Póngase en contacto con el proveedor de la aplicación para comprobar que se trata de un paquete de actualización de Windows Installer válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-778">Contact the application vendor to verify that this is a valid Windows Installer update package.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-779"><span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**paquete de revisión de ERROR \_ \_ \_ no compatible**</span><span class="sxs-lookup"><span data-stu-id="e4551-779"><span id="ERROR_PATCH_PACKAGE_UNSUPPORTED"></span><span id="error_patch_package_unsupported"></span>**ERROR\_PATCH\_PACKAGE\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-780">1637 (0x665)</span><span class="sxs-lookup"><span data-stu-id="e4551-780">1637 (0x665)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-781">El servicio Windows Installer no puede procesar este paquete de actualización.</span><span class="sxs-lookup"><span data-stu-id="e4551-781">This update package cannot be processed by the Windows Installer service.</span></span> <span data-ttu-id="e4551-782">Debe instalar un Service Pack de Windows que contenga una versión más reciente del servicio Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="e4551-782">You must install a Windows service pack that contains a newer version of the Windows Installer service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-783"><span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**\_versión del producto de error \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-783"><span id="ERROR_PRODUCT_VERSION"></span><span id="error_product_version"></span>**ERROR\_PRODUCT\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-784">1638 (0x666)</span><span class="sxs-lookup"><span data-stu-id="e4551-784">1638 (0x666)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-785">Ya está instalada otra versión de este producto.</span><span class="sxs-lookup"><span data-stu-id="e4551-785">Another version of this product is already installed.</span></span> <span data-ttu-id="e4551-786">La instalación de esta versión no puede continuar.</span><span class="sxs-lookup"><span data-stu-id="e4551-786">Installation of this version cannot continue.</span></span> <span data-ttu-id="e4551-787">Para configurar o quitar la versión existente de este producto, use agregar o quitar programas en el panel de control.</span><span class="sxs-lookup"><span data-stu-id="e4551-787">To configure or remove the existing version of this product, use Add/Remove Programs on the Control Panel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-788"><span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERROR \_ de \_ línea de comandos no válida \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-788"><span id="ERROR_INVALID_COMMAND_LINE"></span><span id="error_invalid_command_line"></span>**ERROR\_INVALID\_COMMAND\_LINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-789">1639 (0x667)</span><span class="sxs-lookup"><span data-stu-id="e4551-789">1639 (0x667)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-790">Argumento de línea de comandos no válido.</span><span class="sxs-lookup"><span data-stu-id="e4551-790">Invalid command line argument.</span></span> <span data-ttu-id="e4551-791">Consulte el SDK de Windows Installer para obtener ayuda detallada sobre la línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="e4551-791">Consult the Windows Installer SDK for detailed command line help.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-792"><span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERROR de \_ instalación \_ remota no \_ permitida**</span><span class="sxs-lookup"><span data-stu-id="e4551-792"><span id="ERROR_INSTALL_REMOTE_DISALLOWED"></span><span id="error_install_remote_disallowed"></span>**ERROR\_INSTALL\_REMOTE\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-793">1640 (0x668)</span><span class="sxs-lookup"><span data-stu-id="e4551-793">1640 (0x668)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-794">Solo los administradores tienen permiso para agregar, quitar o configurar el software de servidor durante una sesión remota de Terminal Services.</span><span class="sxs-lookup"><span data-stu-id="e4551-794">Only administrators have permission to add, remove, or configure server software during a Terminal services remote session.</span></span> <span data-ttu-id="e4551-795">Si desea instalar o configurar el software en el servidor, póngase en contacto con el administrador de red.</span><span class="sxs-lookup"><span data-stu-id="e4551-795">If you want to install or configure software on the server, contact your network administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-796"><span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**ERROR \_ de \_ reinicio \_ iniciado correctamente**</span><span class="sxs-lookup"><span data-stu-id="e4551-796"><span id="ERROR_SUCCESS_REBOOT_INITIATED"></span><span id="error_success_reboot_initiated"></span>**ERROR\_SUCCESS\_REBOOT\_INITIATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-797">1641 (0x669)</span><span class="sxs-lookup"><span data-stu-id="e4551-797">1641 (0x669)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-798">La operación solicitada se completó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e4551-798">The requested operation completed successfully.</span></span> <span data-ttu-id="e4551-799">El sistema se reiniciará para que los cambios surtan efecto.</span><span class="sxs-lookup"><span data-stu-id="e4551-799">The system will be restarted so the changes can take effect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-800"><span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**\_ \_ \_ no \_ se encontró el destino de revisión de error**</span><span class="sxs-lookup"><span data-stu-id="e4551-800"><span id="ERROR_PATCH_TARGET_NOT_FOUND"></span><span id="error_patch_target_not_found"></span>**ERROR\_PATCH\_TARGET\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-801">1642 (0x66A)</span><span class="sxs-lookup"><span data-stu-id="e4551-801">1642 (0x66A)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-802">El servicio Windows Installer no puede instalar la actualización porque es posible que falte el programa que se va a actualizar o que la actualización pueda actualizar una versión diferente del programa.</span><span class="sxs-lookup"><span data-stu-id="e4551-802">The upgrade cannot be installed by the Windows Installer service because the program to be upgraded may be missing, or the upgrade may update a different version of the program.</span></span> <span data-ttu-id="e4551-803">Compruebe que el programa que se va a actualizar existe en el equipo y que tiene la actualización correcta.</span><span class="sxs-lookup"><span data-stu-id="e4551-803">Verify that the program to be upgraded exists on your computer and that you have the correct upgrade.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-804"><span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**paquete de revisión de errores \_ \_ \_ rechazado**</span><span class="sxs-lookup"><span data-stu-id="e4551-804"><span id="ERROR_PATCH_PACKAGE_REJECTED"></span><span id="error_patch_package_rejected"></span>**ERROR\_PATCH\_PACKAGE\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-805">1643 (0x66B)</span><span class="sxs-lookup"><span data-stu-id="e4551-805">1643 (0x66B)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-806">La Directiva de restricción de software no permite el paquete de actualización.</span><span class="sxs-lookup"><span data-stu-id="e4551-806">The update package is not permitted by software restriction policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-807"><span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERROR \_ de \_ transformación de instalación \_ rechazada**</span><span class="sxs-lookup"><span data-stu-id="e4551-807"><span id="ERROR_INSTALL_TRANSFORM_REJECTED"></span><span id="error_install_transform_rejected"></span>**ERROR\_INSTALL\_TRANSFORM\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-808">1644 (0x66C)</span><span class="sxs-lookup"><span data-stu-id="e4551-808">1644 (0x66C)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-809">Una o más personalizaciones no están permitidas por la Directiva de restricción de software.</span><span class="sxs-lookup"><span data-stu-id="e4551-809">One or more customizations are not permitted by software restriction policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-810"><span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERROR al \_ instalar el \_ remoto \_ prohibido**</span><span class="sxs-lookup"><span data-stu-id="e4551-810"><span id="ERROR_INSTALL_REMOTE_PROHIBITED"></span><span id="error_install_remote_prohibited"></span>**ERROR\_INSTALL\_REMOTE\_PROHIBITED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-811">1645 (0x66D)</span><span class="sxs-lookup"><span data-stu-id="e4551-811">1645 (0x66D)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-812">El Windows Installer no permite la instalación desde un Conexión a Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="e4551-812">The Windows Installer does not permit installation from a Remote Desktop Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-813"><span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**\_no se \_ admite la eliminación de la revisión de errores \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-813"><span id="ERROR_PATCH_REMOVAL_UNSUPPORTED"></span><span id="error_patch_removal_unsupported"></span>**ERROR\_PATCH\_REMOVAL\_UNSUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-814">1646 (0x66E)</span><span class="sxs-lookup"><span data-stu-id="e4551-814">1646 (0x66E)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-815">No se admite la desinstalación del paquete de actualización.</span><span class="sxs-lookup"><span data-stu-id="e4551-815">Uninstallation of the update package is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-816"><span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**ERROR \_ de \_ revisión desconocida**</span><span class="sxs-lookup"><span data-stu-id="e4551-816"><span id="ERROR_UNKNOWN_PATCH"></span><span id="error_unknown_patch"></span>**ERROR\_UNKNOWN\_PATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-817">1647 (0x66F)</span><span class="sxs-lookup"><span data-stu-id="e4551-817">1647 (0x66F)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-818">La actualización no se aplica a este producto.</span><span class="sxs-lookup"><span data-stu-id="e4551-818">The update is not applied to this product.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-819"><span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**ERROR de \_ revisión \_ sin \_ secuencia**</span><span class="sxs-lookup"><span data-stu-id="e4551-819"><span id="ERROR_PATCH_NO_SEQUENCE"></span><span id="error_patch_no_sequence"></span>**ERROR\_PATCH\_NO\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-820">1648 (0x670)</span><span class="sxs-lookup"><span data-stu-id="e4551-820">1648 (0x670)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-821">No se encontró ninguna secuencia válida para el conjunto de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="e4551-821">No valid sequence could be found for the set of updates.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-822"><span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**no \_ se \_ permite la eliminación de la revisión de errores \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-822"><span id="ERROR_PATCH_REMOVAL_DISALLOWED"></span><span id="error_patch_removal_disallowed"></span>**ERROR\_PATCH\_REMOVAL\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-823">1649 (0x671)</span><span class="sxs-lookup"><span data-stu-id="e4551-823">1649 (0x671)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-824">No se ha permitido la eliminación de la actualización por la Directiva.</span><span class="sxs-lookup"><span data-stu-id="e4551-824">Update removal was disallowed by policy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-825"><span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERROR \_ de \_ revisión \_ XML no válida**</span><span class="sxs-lookup"><span data-stu-id="e4551-825"><span id="ERROR_INVALID_PATCH_XML"></span><span id="error_invalid_patch_xml"></span>**ERROR\_INVALID\_PATCH\_XML**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-826">1650 (0x672)</span><span class="sxs-lookup"><span data-stu-id="e4551-826">1650 (0x672)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-827">Los datos de actualización XML no son válidos.</span><span class="sxs-lookup"><span data-stu-id="e4551-827">The XML update data is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-828"><span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**producto de revisión de errores \_ \_ administrado \_ anunciada \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-828"><span id="ERROR_PATCH_MANAGED_ADVERTISED_PRODUCT"></span><span id="error_patch_managed_advertised_product"></span>**ERROR\_PATCH\_MANAGED\_ADVERTISED\_PRODUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-829">1651 (0x673)</span><span class="sxs-lookup"><span data-stu-id="e4551-829">1651 (0x673)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-830">Windows Installer no permite la actualización de productos anunciados administrados.</span><span class="sxs-lookup"><span data-stu-id="e4551-830">Windows Installer does not permit updating of managed advertised products.</span></span> <span data-ttu-id="e4551-831">Debe instalar al menos una característica del producto antes de aplicar la actualización.</span><span class="sxs-lookup"><span data-stu-id="e4551-831">At least one feature of the product must be installed before applying the update.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-832"><span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERROR al \_ instalar el \_ servicio \_ SafeBoot**</span><span class="sxs-lookup"><span data-stu-id="e4551-832"><span id="ERROR_INSTALL_SERVICE_SAFEBOOT"></span><span id="error_install_service_safeboot"></span>**ERROR\_INSTALL\_SERVICE\_SAFEBOOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-833">1652 (0x674)</span><span class="sxs-lookup"><span data-stu-id="e4551-833">1652 (0x674)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-834">No se puede obtener acceso al servicio Windows Installer en modo seguro.</span><span class="sxs-lookup"><span data-stu-id="e4551-834">The Windows Installer service is not accessible in Safe Mode.</span></span> <span data-ttu-id="e4551-835">Vuelva a intentarlo cuando el equipo no esté en modo seguro o use Restaurar sistema para devolver el equipo a un estado bueno anterior.</span><span class="sxs-lookup"><span data-stu-id="e4551-835">Please try again when your computer is not in Safe Mode or you can use System Restore to return your machine to a previous good state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-836"><span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**excepción de ERROR de ERROR \_ \_ rápido \_**</span><span class="sxs-lookup"><span data-stu-id="e4551-836"><span id="ERROR_FAIL_FAST_EXCEPTION"></span><span id="error_fail_fast_exception"></span>**ERROR\_FAIL\_FAST\_EXCEPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-837">1653 (0x675)</span><span class="sxs-lookup"><span data-stu-id="e4551-837">1653 (0x675)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-838">Se produjo una excepción de error rápido.</span><span class="sxs-lookup"><span data-stu-id="e4551-838">A fail fast exception occurred.</span></span> <span data-ttu-id="e4551-839">No se invocarán los controladores de excepciones y el proceso se terminará inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="e4551-839">Exception handlers will not be invoked and the process will be terminated immediately.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e4551-840"><span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**instalación de ERROR \_ \_ rechazada**</span><span class="sxs-lookup"><span data-stu-id="e4551-840"><span id="ERROR_INSTALL_REJECTED"></span><span id="error_install_rejected"></span>**ERROR\_INSTALL\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e4551-841">1654 (0x676)</span><span class="sxs-lookup"><span data-stu-id="e4551-841">1654 (0x676)</span></span>
</dt> <dt>



<span data-ttu-id="e4551-842">La aplicación que está intentando ejecutar no es compatible con esta versión de Windows.</span><span class="sxs-lookup"><span data-stu-id="e4551-842">The app that you are trying to run is not supported on this version of Windows.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e4551-843">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4551-843">Requirements</span></span>



| <span data-ttu-id="e4551-844">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4551-844">Requirement</span></span> | <span data-ttu-id="e4551-845">Value</span><span class="sxs-lookup"><span data-stu-id="e4551-845">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e4551-846">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4551-846">Minimum supported client</span></span><br/> | <span data-ttu-id="e4551-847">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e4551-847">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e4551-848">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e4551-848">Minimum supported server</span></span><br/> | <span data-ttu-id="e4551-849">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e4551-849">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e4551-850">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e4551-850">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4551-851"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4551-851"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4551-852">Vea también</span><span class="sxs-lookup"><span data-stu-id="e4551-852">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4551-853">Códigos de error del sistema</span><span class="sxs-lookup"><span data-stu-id="e4551-853">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




