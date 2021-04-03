---
description: Describe los códigos de error 6000-8199 definidos en el archivo de encabezado WinError. h y está destinado a los desarrolladores.
ms.assetid: eaaf9f65-e8ff-4e54-90a9-04252cdd773a
title: Códigos de error del sistema (6000-8199) (WinError. h)
ms.topic: reference
ms.date: 07/18/2019
ms.openlocfilehash: 0660009411224673481e9b65bcb62d7b194ab71f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907354"
---
# <a name="system-error-codes-6000-8199"></a><span data-ttu-id="b7eb9-103">Códigos de error del sistema (6000-8199)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-103">System Error Codes (6000-8199)</span></span>

> [!NOTE]
> <span data-ttu-id="b7eb9-104">Esta información está destinada a los desarrolladores que depuran errores del sistema.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-104">This information is intended for developers debugging system errors.</span></span> <span data-ttu-id="b7eb9-105">En el caso de otros errores, como los problemas con Windows Update, hay una lista de recursos en la página [códigos de error](system-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="b7eb9-105">For other errors, such as issues with Windows Update, there is a list of resources on the [Error codes](system-error-codes.md) page.</span></span>

<span data-ttu-id="b7eb9-106">En la lista siguiente se describen los [códigos de error del sistema](system-error-codes.md) (errores 6000 a 8199).</span><span class="sxs-lookup"><span data-stu-id="b7eb9-106">The following list describes [system error codes](system-error-codes.md) (errors 6000 to 8199).</span></span> <span data-ttu-id="b7eb9-107">La función [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) devuelve los resultados cuando se produce un error en muchas funciones.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-107">They are returned by the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function when many functions fail.</span></span> <span data-ttu-id="b7eb9-108">Para recuperar el texto de la descripción del error en la aplicación, use la función [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) con **el \_ mensaje format \_ from \_ System** Flag.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-108">To retrieve the description text for the error in your application, use the [**FormatMessage**](/windows/desktop/api/WinBase/nf-winbase-formatmessage) function with the **FORMAT\_MESSAGE\_FROM\_SYSTEM** flag.</span></span>

<dl> <dt>

<span data-ttu-id="b7eb9-109"><span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**ERROR de \_ cifrado de errores \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-109"><span id="ERROR_ENCRYPTION_FAILED"></span><span id="error_encryption_failed"></span>**ERROR\_ENCRYPTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-110">6000 (0x1770)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-110">6000 (0x1770)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-111">No se pudo cifrar el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-111">The specified file could not be encrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-112"><span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**error en el \_ DEScifrado de errores \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-112"><span id="ERROR_DECRYPTION_FAILED"></span><span id="error_decryption_failed"></span>**ERROR\_DECRYPTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-113">6001 (0x1771)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-113">6001 (0x1771)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-114">No se pudo descifrar el archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-114">The specified file could not be decrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-115"><span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**archivo de ERROR \_ \_ cifrado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-115"><span id="ERROR_FILE_ENCRYPTED"></span><span id="error_file_encrypted"></span>**ERROR\_FILE\_ENCRYPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-116">6002 (0x1772)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-116">6002 (0x1772)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-117">El archivo especificado está cifrado y el usuario no tiene la capacidad de descifrarlo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-117">The specified file is encrypted and the user does not have the ability to decrypt it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-118"><span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERROR: \_ no hay \_ Directiva de recuperación \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-118"><span id="ERROR_NO_RECOVERY_POLICY"></span><span id="error_no_recovery_policy"></span>**ERROR\_NO\_RECOVERY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-119">6003 (0x1773)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-119">6003 (0x1773)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-120">No hay ninguna directiva de recuperación de cifrado válida configurada para este sistema.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-120">There is no valid encryption recovery policy configured for this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-121"><span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERROR \_ no \_ EFS**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-121"><span id="ERROR_NO_EFS"></span><span id="error_no_efs"></span>**ERROR\_NO\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-122">6004 (0x1774)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-122">6004 (0x1774)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-123">No se ha cargado el controlador de cifrado necesario para este sistema.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-123">The required encryption driver is not loaded for this system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-124"><span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERROR \_ de \_ EFS incorrecto**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-124"><span id="ERROR_WRONG_EFS"></span><span id="error_wrong_efs"></span>**ERROR\_WRONG\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-125">6005 (0x1775)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-125">6005 (0x1775)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-126">El archivo se cifró con un controlador de cifrado diferente del que está cargado actualmente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-126">The file was encrypted with a different encryption driver than is currently loaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-127"><span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERROR: \_ no hay \_ claves de usuario \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-127"><span id="ERROR_NO_USER_KEYS"></span><span id="error_no_user_keys"></span>**ERROR\_NO\_USER\_KEYS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-128">6006 (0x1776)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-128">6006 (0x1776)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-129">No hay claves de EFS definidas para el usuario.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-129">There are no EFS keys defined for the user.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-130"><span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**archivo de ERROR \_ \_ no \_ cifrado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-130"><span id="ERROR_FILE_NOT_ENCRYPTED"></span><span id="error_file_not_encrypted"></span>**ERROR\_FILE\_NOT\_ENCRYPTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-131">6007 (0x1777)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-131">6007 (0x1777)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-132">El archivo especificado no está cifrado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-132">The specified file is not encrypted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-133"><span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**no se pudo \_ \_ exportar el \_ formato**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-133"><span id="ERROR_NOT_EXPORT_FORMAT"></span><span id="error_not_export_format"></span>**ERROR\_NOT\_EXPORT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-134">6008 (0x1778)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-134">6008 (0x1778)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-135">El archivo especificado no está en el formato de exportación de EFS definido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-135">The specified file is not in the defined EFS export format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-136"><span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**archivo de ERROR de \_ \_ \_ solo lectura**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-136"><span id="ERROR_FILE_READ_ONLY"></span><span id="error_file_read_only"></span>**ERROR\_FILE\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-137">6009 (0x1779)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-137">6009 (0x1779)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-138">El archivo especificado es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-138">The specified file is read only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-139"><span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERROR en el \_ directorio \_ EFS no \_ permitido**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-139"><span id="ERROR_DIR_EFS_DISALLOWED"></span><span id="error_dir_efs_disallowed"></span>**ERROR\_DIR\_EFS\_DISALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-140">6010 (0x177A)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-140">6010 (0x177A)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-141">El directorio se ha deshabilitado para el cifrado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-141">The directory has been disabled for encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-142"><span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERROR \_ el \_ servidor EFS no es de \_ \_ confianza**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-142"><span id="ERROR_EFS_SERVER_NOT_TRUSTED"></span><span id="error_efs_server_not_trusted"></span>**ERROR\_EFS\_SERVER\_NOT\_TRUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-143">6011 (0x177B)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-143">6011 (0x177B)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-144">No se confía en el servidor para la operación de cifrado remoto.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-144">The server is not trusted for remote encryption operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-145"><span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERROR \_ de \_ Directiva de recuperación incorrecta \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-145"><span id="ERROR_BAD_RECOVERY_POLICY"></span><span id="error_bad_recovery_policy"></span>**ERROR\_BAD\_RECOVERY\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-146">6012 (0x177C)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-146">6012 (0x177C)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-147">La Directiva de recuperación configurada para este sistema contiene un certificado de recuperación no válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-147">Recovery policy configured for this system contains invalid recovery certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-148"><span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERROR \_ de \_ BLOB de EFS alg \_ \_ demasiado \_ grande**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-148"><span id="ERROR_EFS_ALG_BLOB_TOO_BIG"></span><span id="error_efs_alg_blob_too_big"></span>**ERROR\_EFS\_ALG\_BLOB\_TOO\_BIG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-149">6013 (0x177D)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-149">6013 (0x177D)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-150">El algoritmo de cifrado usado en el archivo de origen necesita un búfer de clave mayor que el del archivo de destino.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-150">The encryption algorithm used on the source file needs a bigger key buffer than the one on the destination file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-151"><span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**el \_ volumen de error \_ no es \_ compatible con \_ EFS**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-151"><span id="ERROR_VOLUME_NOT_SUPPORT_EFS"></span><span id="error_volume_not_support_efs"></span>**ERROR\_VOLUME\_NOT\_SUPPORT\_EFS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-152">6014 (0x177E)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-152">6014 (0x177E)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-153">La partición de disco no admite el cifrado de archivos.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-153">The disk partition does not support file encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-154"><span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERROR de \_ EFS \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-154"><span id="ERROR_EFS_DISABLED"></span><span id="error_efs_disabled"></span>**ERROR\_EFS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-155">6015 (0x177F)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-155">6015 (0x177F)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-156">Esta máquina está deshabilitada para el cifrado de archivos.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-156">This machine is disabled for file encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-157"><span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERROR: la \_ versión de EFS \_ no es \_ \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-157"><span id="ERROR_EFS_VERSION_NOT_SUPPORT"></span><span id="error_efs_version_not_support"></span>**ERROR\_EFS\_VERSION\_NOT\_SUPPORT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-158">6016 (0x1780)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-158">6016 (0x1780)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-159">Se requiere un sistema más reciente para descifrar este archivo cifrado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-159">A newer system is required to decrypt this encrypted file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-160"><span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERROR \_ de \_ cifrado de CS \_ respuesta de servidor no válida \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-160"><span id="ERROR_CS_ENCRYPTION_INVALID_SERVER_RESPONSE"></span><span id="error_cs_encryption_invalid_server_response"></span>**ERROR\_CS\_ENCRYPTION\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-161">6017 (0x1781)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-161">6017 (0x1781)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-162">El servidor remoto ha enviado una respuesta no válida para un archivo que se está abriendo con el cifrado del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-162">The remote server sent an invalid response for a file being opened with Client Side Encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-163"><span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERROR en el \_ \_ servidor de cifrado CS \_ no compatible \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-163"><span id="ERROR_CS_ENCRYPTION_UNSUPPORTED_SERVER"></span><span id="error_cs_encryption_unsupported_server"></span>**ERROR\_CS\_ENCRYPTION\_UNSUPPORTED\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-164">6018 (0x1782)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-164">6018 (0x1782)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-165">El servidor remoto no admite el cifrado del lado cliente, aunque notifica que es compatible.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-165">Client Side Encryption is not supported by the remote server even though it claims to support it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-166"><span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERROR \_ CS \_ cifrado \_ \_ archivo cifrado existente \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-166"><span id="ERROR_CS_ENCRYPTION_EXISTING_ENCRYPTED_FILE"></span><span id="error_cs_encryption_existing_encrypted_file"></span>**ERROR\_CS\_ENCRYPTION\_EXISTING\_ENCRYPTED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-167">6019 (0x1783)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-167">6019 (0x1783)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-168">El archivo está cifrado y debe abrirse en el modo de cifrado del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-168">File is encrypted and should be opened in Client Side Encryption mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-169"><span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERROR \_ CS \_ cifrado \_ nuevo \_ archivo cifrado \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-169"><span id="ERROR_CS_ENCRYPTION_NEW_ENCRYPTED_FILE"></span><span id="error_cs_encryption_new_encrypted_file"></span>**ERROR\_CS\_ENCRYPTION\_NEW\_ENCRYPTED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-170">6020 (0x1784)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-170">6020 (0x1784)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-171">Se está creando un nuevo archivo cifrado y debe proporcionarse un $EFS.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-171">A new encrypted file is being created and a $EFS needs to be provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-172"><span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERROR \_ de \_ archivo de cifrado CS \_ \_ no \_ CSE**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-172"><span id="ERROR_CS_ENCRYPTION_FILE_NOT_CSE"></span><span id="error_cs_encryption_file_not_cse"></span>**ERROR\_CS\_ENCRYPTION\_FILE\_NOT\_CSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-173">6021 (0x1785)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-173">6021 (0x1785)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-174">El cliente SMB solicitó un FSCTL de CSE en un archivo que no es de CSE.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-174">The SMB client requested a CSE FSCTL on a non-CSE file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-175"><span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**la \_ Directiva de cifrado de errores \_ \_ deniega la \_ operación**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-175"><span id="ERROR_ENCRYPTION_POLICY_DENIES_OPERATION"></span><span id="error_encryption_policy_denies_operation"></span>**ERROR\_ENCRYPTION\_POLICY\_DENIES\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-176">6022 (0x1786)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-176">6022 (0x1786)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-177">La Directiva bloqueó la operación solicitada.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-177">The requested operation was blocked by policy.</span></span> <span data-ttu-id="b7eb9-178">Para obtener más información, póngase en contacto con el administrador del sistema.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-178">For more information, contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-179"><span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERROR \_ no \_ \_ se encontraron servidores de explorador \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-179"><span id="ERROR_NO_BROWSER_SERVERS_FOUND"></span><span id="error_no_browser_servers_found"></span>**ERROR\_NO\_BROWSER\_SERVERS\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-180">6118 (0x17E6)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-180">6118 (0x17E6)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-181">La lista de servidores de este grupo de trabajo no está disponible actualmente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-181">The list of servers for this workgroup is not currently available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-182"><span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**el \_ servicio sched E \_ no es \_ \_ LOCALSYSTEM**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-182"><span id="SCHED_E_SERVICE_NOT_LOCALSYSTEM"></span><span id="sched_e_service_not_localsystem"></span>**SCHED\_E\_SERVICE\_NOT\_LOCALSYSTEM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-183">6200 (0x1838)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-183">6200 (0x1838)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-184">El servicio de Programador de tareas debe estar configurado para ejecutarse en la cuenta del sistema para funcionar correctamente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-184">The Task Scheduler service must be configured to run in the System account to function properly.</span></span> <span data-ttu-id="b7eb9-185">Las tareas individuales se pueden configurar para ejecutarse en otras cuentas.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-185">Individual tasks may be configured to run in other accounts.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-186"><span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**SECTOR de registro de errores \_ \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-186"><span id="ERROR_LOG_SECTOR_INVALID"></span><span id="error_log_sector_invalid"></span>**ERROR\_LOG\_SECTOR\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-187">6600 (0x19C8)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-187">6600 (0x19C8)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-188">El servicio de registro encontró un sector de registro no válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-188">Log service encountered an invalid log sector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-189"><span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**paridad del sector de registro de errores \_ \_ \_ \_ no válida**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-189"><span id="ERROR_LOG_SECTOR_PARITY_INVALID"></span><span id="error_log_sector_parity_invalid"></span>**ERROR\_LOG\_SECTOR\_PARITY\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-190">6601 (0x19C9)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-190">6601 (0x19C9)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-191">El servicio de registro encontró un sector de registro con paridad de bloque no válida.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-191">Log service encountered a log sector with invalid block parity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-192"><span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**SECTOR de registro de errores \_ \_ \_ reasignado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-192"><span id="ERROR_LOG_SECTOR_REMAPPED"></span><span id="error_log_sector_remapped"></span>**ERROR\_LOG\_SECTOR\_REMAPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-193">6602 (0x19CA)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-193">6602 (0x19CA)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-194">El servicio de registro encontró un sector de registro reasignado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-194">Log service encountered a remapped log sector.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-195"><span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**bloque de registro de errores \_ \_ \_ incompleto**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-195"><span id="ERROR_LOG_BLOCK_INCOMPLETE"></span><span id="error_log_block_incomplete"></span>**ERROR\_LOG\_BLOCK\_INCOMPLETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-196">6603 (0x19CB)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-196">6603 (0x19CB)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-197">El servicio de registro encontró un bloque de registro parcial o incompleto.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-197">Log service encountered a partial or incomplete log block.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-198"><span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**\_ \_ intervalo no válido de registro de errores \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-198"><span id="ERROR_LOG_INVALID_RANGE"></span><span id="error_log_invalid_range"></span>**ERROR\_LOG\_INVALID\_RANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-199">6604 (0x19CC)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-199">6604 (0x19CC)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-200">El servicio de registro detectó un intento de obtener acceso a datos fuera del intervalo de registros activo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-200">Log service encountered an attempt access data outside the active log range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-201"><span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**bloques de registro de errores \_ \_ \_ agotados**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-201"><span id="ERROR_LOG_BLOCKS_EXHAUSTED"></span><span id="error_log_blocks_exhausted"></span>**ERROR\_LOG\_BLOCKS\_EXHAUSTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-202">6605 (0x19CD)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-202">6605 (0x19CD)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-203">Los búferes de serialización de usuario del servicio de registro están agotados.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-203">Log service user marshalling buffers are exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-204"><span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**contexto de lectura de registro de errores \_ \_ \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-204"><span id="ERROR_LOG_READ_CONTEXT_INVALID"></span><span id="error_log_read_context_invalid"></span>**ERROR\_LOG\_READ\_CONTEXT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-205">6606 (0x19CE)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-205">6606 (0x19CE)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-206">El servicio de registro detectó un intento de leer desde un área de cálculo de referencias con un contexto de lectura no válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-206">Log service encountered an attempt read from a marshalling area with an invalid read context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-207"><span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**reinicio de registro de errores \_ \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-207"><span id="ERROR_LOG_RESTART_INVALID"></span><span id="error_log_restart_invalid"></span>**ERROR\_LOG\_RESTART\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-208">6607 (0x19CF)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-208">6607 (0x19CF)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-209">El servicio de registro encontró un área de reinicio de registro no válida.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-209">Log service encountered an invalid log restart area.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-210"><span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**\_versión de \_ bloque de registro de errores \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-210"><span id="ERROR_LOG_BLOCK_VERSION"></span><span id="error_log_block_version"></span>**ERROR\_LOG\_BLOCK\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-211">6608 (0x19D0)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-211">6608 (0x19D0)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-212">El servicio de registro encontró una versión de bloque de registro no válida.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-212">Log service encountered an invalid log block version.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-213"><span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**bloque de registro de errores \_ \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-213"><span id="ERROR_LOG_BLOCK_INVALID"></span><span id="error_log_block_invalid"></span>**ERROR\_LOG\_BLOCK\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-214">6609 (0x19D1)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-214">6609 (0x19D1)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-215">El servicio de registro encontró un bloque de registro no válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-215">Log service encountered an invalid log block.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-216"><span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**modo de lectura de registro de errores \_ \_ \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-216"><span id="ERROR_LOG_READ_MODE_INVALID"></span><span id="error_log_read_mode_invalid"></span>**ERROR\_LOG\_READ\_MODE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-217">6610 (0x19D2)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-217">6610 (0x19D2)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-218">El servicio de registro detectó un intento de leer el registro con un modo de lectura no válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-218">Log service encountered an attempt to read the log with an invalid read mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-219"><span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**\_ \_ no reiniciar el registro de errores \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-219"><span id="ERROR_LOG_NO_RESTART"></span><span id="error_log_no_restart"></span>**ERROR\_LOG\_NO\_RESTART**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-220">6611 (0x19D3)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-220">6611 (0x19D3)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-221">El servicio de registro encontró una secuencia de registro sin área de reinicio.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-221">Log service encountered a log stream with no restart area.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-222"><span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**metadatos de registro de errores \_ \_ \_ dañados**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-222"><span id="ERROR_LOG_METADATA_CORRUPT"></span><span id="error_log_metadata_corrupt"></span>**ERROR\_LOG\_METADATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-223">6612 (0x19D4)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-223">6612 (0x19D4)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-224">El servicio de registro encontró un archivo de metadatos dañado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-224">Log service encountered a corrupted metadata file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-225"><span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**metadatos de registro de errores \_ \_ \_ no válidos**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-225"><span id="ERROR_LOG_METADATA_INVALID"></span><span id="error_log_metadata_invalid"></span>**ERROR\_LOG\_METADATA\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-226">6613 (0x19D5)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-226">6613 (0x19D5)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-227">El servicio de registro encontró un archivo de metadatos que el sistema de archivos de registro no pudo crear.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-227">Log service encountered a metadata file that could not be created by the log file system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-228"><span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**metadatos de registro de errores \_ \_ \_ incoherentes**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-228"><span id="ERROR_LOG_METADATA_INCONSISTENT"></span><span id="error_log_metadata_inconsistent"></span>**ERROR\_LOG\_METADATA\_INCONSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-229">6614 (0x19D6)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-229">6614 (0x19D6)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-230">El servicio de registro encontró un archivo de metadatos con datos incoherentes.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-230">Log service encountered a metadata file with inconsistent data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-231"><span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**Reserva de registro de errores \_ \_ \_ no válida**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-231"><span id="ERROR_LOG_RESERVATION_INVALID"></span><span id="error_log_reservation_invalid"></span>**ERROR\_LOG\_RESERVATION\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-232">6615 (0x19D7)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-232">6615 (0x19D7)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-233">El servicio de registro detectó un intento de asignar o eliminar el espacio de reserva.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-233">Log service encountered an attempt to erroneous allocate or dispose reservation space.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-234"><span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**no se pudo eliminar el registro de errores \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-234"><span id="ERROR_LOG_CANT_DELETE"></span><span id="error_log_cant_delete"></span>**ERROR\_LOG\_CANT\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-235">6616 (0x19D8)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-235">6616 (0x19D8)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-236">El servicio de registro no puede eliminar el archivo de registro o el contenedor del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-236">Log service cannot delete log file or file system container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-237"><span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**límite de contenedor de registro de errores \_ \_ \_ \_ superado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-237"><span id="ERROR_LOG_CONTAINER_LIMIT_EXCEEDED"></span><span id="error_log_container_limit_exceeded"></span>**ERROR\_LOG\_CONTAINER\_LIMIT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-238">6617 (0x19D9)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-238">6617 (0x19D9)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-239">El servicio de registro ha alcanzado el número máximo de contenedores permitidos asignados a un archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-239">Log service has reached the maximum allowable containers allocated to a log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-240"><span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**\_ \_ Inicio del registro \_ de errores de \_ registro**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-240"><span id="ERROR_LOG_START_OF_LOG"></span><span id="error_log_start_of_log"></span>**ERROR\_LOG\_START\_OF\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-241">6618 (0x19DA)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-241">6618 (0x19DA)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-242">El servicio de registro ha intentado leer o escribir hacia atrás más allá del inicio del registro.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-242">Log service has attempted to read or write backward past the start of the log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-243"><span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**la \_ Directiva de registro de errores \_ \_ ya está \_ instalada**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-243"><span id="ERROR_LOG_POLICY_ALREADY_INSTALLED"></span><span id="error_log_policy_already_installed"></span>**ERROR\_LOG\_POLICY\_ALREADY\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-244">6619 (0x19DB)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-244">6619 (0x19DB)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-245">No se pudo instalar la Directiva de registro porque ya hay una directiva del mismo tipo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-245">Log policy could not be installed because a policy of the same type is already present.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-246"><span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**Directiva de registro de errores \_ \_ \_ no \_ instalada**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-246"><span id="ERROR_LOG_POLICY_NOT_INSTALLED"></span><span id="error_log_policy_not_installed"></span>**ERROR\_LOG\_POLICY\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-247">6620 (0x19DC)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-247">6620 (0x19DC)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-248">La Directiva de registro en cuestión no se instaló en el momento de la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-248">Log policy in question was not installed at the time of the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-249"><span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**Directiva de registro de errores \_ \_ \_ no válida**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-249"><span id="ERROR_LOG_POLICY_INVALID"></span><span id="error_log_policy_invalid"></span>**ERROR\_LOG\_POLICY\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-250">6621 (0x19DD)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-250">6621 (0x19DD)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-251">El conjunto de directivas instalado en el registro no es válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-251">The installed set of policies on the log is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-252"><span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**\_conflicto de \_ directivas de registro de errores \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-252"><span id="ERROR_LOG_POLICY_CONFLICT"></span><span id="error_log_policy_conflict"></span>**ERROR\_LOG\_POLICY\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-253">6622 (0x19DE)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-253">6622 (0x19DE)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-254">Una directiva del registro en cuestión impidió que se completara la operación.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-254">A policy on the log in question prevented the operation from completing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-255"><span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**\_cola de \_ archivo anclada al registro \_ de errores \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-255"><span id="ERROR_LOG_PINNED_ARCHIVE_TAIL"></span><span id="error_log_pinned_archive_tail"></span>**ERROR\_LOG\_PINNED\_ARCHIVE\_TAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-256">6623 (0x19DF)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-256">6623 (0x19DF)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-257">No se puede reclamar el espacio del registro porque el registro está anclado por la cola del archivo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-257">Log space cannot be reclaimed because the log is pinned by the archive tail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-258"><span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**entrada de registro de errores no \_ \_ \_ existente**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-258"><span id="ERROR_LOG_RECORD_NONEXISTENT"></span><span id="error_log_record_nonexistent"></span>**ERROR\_LOG\_RECORD\_NONEXISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-259">6624 (0x19E0)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-259">6624 (0x19E0)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-260">La entrada de registro no es un registro del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-260">Log record is not a record in the log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-261"><span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**\_registros de \_ errores \_ reservados \_ no válidos**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-261"><span id="ERROR_LOG_RECORDS_RESERVED_INVALID"></span><span id="error_log_records_reserved_invalid"></span>**ERROR\_LOG\_RECORDS\_RESERVED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-262">6625 (0x19E1)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-262">6625 (0x19E1)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-263">El número de entradas de registro reservadas o el ajuste del número de entradas de registro reservadas no es válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-263">Number of reserved log records or the adjustment of the number of reserved log records is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-264"><span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**espacio de registro de errores \_ \_ \_ reservado \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-264"><span id="ERROR_LOG_SPACE_RESERVED_INVALID"></span><span id="error_log_space_reserved_invalid"></span>**ERROR\_LOG\_SPACE\_RESERVED\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-265">6626 (0x19E2)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-265">6626 (0x19E2)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-266">El espacio de registro reservado o el ajuste del espacio de registro no es válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-266">Reserved log space or the adjustment of the log space is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-267"><span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**cola de registro de errores \_ \_ \_ no válida**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-267"><span id="ERROR_LOG_TAIL_INVALID"></span><span id="error_log_tail_invalid"></span>**ERROR\_LOG\_TAIL\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-268">6627 (0x19E3)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-268">6627 (0x19E3)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-269">Una cola de archivo nueva o existente o la base del registro activo no es válida.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-269">An new or existing archive tail or base of the active log is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-270"><span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**registro de errores \_ \_ completo**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-270"><span id="ERROR_LOG_FULL"></span><span id="error_log_full"></span>**ERROR\_LOG\_FULL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-271">6628 (0x19E4)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-271">6628 (0x19E4)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-272">Se agotó el espacio de registro.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-272">Log space is exhausted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-273"><span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**ERROR \_ no se pudo \_ \_ cambiar el tamaño del \_ registro**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-273"><span id="ERROR_COULD_NOT_RESIZE_LOG"></span><span id="error_could_not_resize_log"></span>**ERROR\_COULD\_NOT\_RESIZE\_LOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-274">6629 (0x19E5)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-274">6629 (0x19E5)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-275">No se pudo establecer el tamaño solicitado en el registro.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-275">The log could not be set to the requested size.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-276"><span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**registro de errores \_ \_ multiplexado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-276"><span id="ERROR_LOG_MULTIPLEXED"></span><span id="error_log_multiplexed"></span>**ERROR\_LOG\_MULTIPLEXED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-277">6630 (0x19E6)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-277">6630 (0x19E6)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-278">El registro se multiplexa, no se permiten escrituras directas en el registro físico.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-278">Log is multiplexed, no direct writes to the physical log is allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-279"><span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**registro de errores \_ \_ dedicado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-279"><span id="ERROR_LOG_DEDICATED"></span><span id="error_log_dedicated"></span>**ERROR\_LOG\_DEDICATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-280">6631 (0x19E7)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-280">6631 (0x19E7)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-281">No se pudo realizar la operación porque el registro es un registro dedicado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-281">The operation failed because the log is a dedicated log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-282"><span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**el \_ \_ archivo \_ de registro de errores no está \_ en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-282"><span id="ERROR_LOG_ARCHIVE_NOT_IN_PROGRESS"></span><span id="error_log_archive_not_in_progress"></span>**ERROR\_LOG\_ARCHIVE\_NOT\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-283">6632 (0x19E8)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-283">6632 (0x19E8)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-284">La operación requiere un contexto de archivo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-284">The operation requires an archive context.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-285"><span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**\_ \_ archivo de registro \_ de errores en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-285"><span id="ERROR_LOG_ARCHIVE_IN_PROGRESS"></span><span id="error_log_archive_in_progress"></span>**ERROR\_LOG\_ARCHIVE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-286">6633 (0x19E9)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-286">6633 (0x19E9)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-287">El archivo de registro está en curso.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-287">Log archival is in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-288"><span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**ERROR de \_ Registro \_ efímero**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-288"><span id="ERROR_LOG_EPHEMERAL"></span><span id="error_log_ephemeral"></span>**ERROR\_LOG\_EPHEMERAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-289">6634 (0x19EA)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-289">6634 (0x19EA)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-290">La operación requiere un registro no efímero, pero el registro es efímero.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-290">The operation requires a non-ephemeral log, but the log is ephemeral.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-291"><span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**el \_ registro de errores \_ no tiene \_ suficientes \_ contenedores**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-291"><span id="ERROR_LOG_NOT_ENOUGH_CONTAINERS"></span><span id="error_log_not_enough_containers"></span>**ERROR\_LOG\_NOT\_ENOUGH\_CONTAINERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-292">6635 (0x19EB)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-292">6635 (0x19EB)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-293">El registro debe tener al menos dos contenedores antes de que se puedan leer o escribir en él.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-293">The log must have at least two containers before it can be read from or written to.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-294"><span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**el \_ cliente de registro de errores \_ \_ ya está \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-294"><span id="ERROR_LOG_CLIENT_ALREADY_REGISTERED"></span><span id="error_log_client_already_registered"></span>**ERROR\_LOG\_CLIENT\_ALREADY\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-295">6636 (0x19EC)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-295">6636 (0x19EC)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-296">Ya hay un cliente de registro registrado en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-296">A log client has already registered on the stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-297"><span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**cliente de registro de errores \_ \_ \_ no \_ registrado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-297"><span id="ERROR_LOG_CLIENT_NOT_REGISTERED"></span><span id="error_log_client_not_registered"></span>**ERROR\_LOG\_CLIENT\_NOT\_REGISTERED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-298">6637 (0x19ED)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-298">6637 (0x19ED)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-299">No se ha registrado un cliente de registro en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-299">A log client has not been registered on the stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-300"><span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**\_ \_ \_ controlador completo de registro \_ de errores en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-300"><span id="ERROR_LOG_FULL_HANDLER_IN_PROGRESS"></span><span id="error_log_full_handler_in_progress"></span>**ERROR\_LOG\_FULL\_HANDLER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-301">6638 (0x19EE)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-301">6638 (0x19EE)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-302">Ya se ha realizado una solicitud para administrar la condición de registro completa.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-302">A request has already been made to handle the log full condition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-303"><span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**error \_ \_ al leer el contenedor del registro de \_ errores \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-303"><span id="ERROR_LOG_CONTAINER_READ_FAILED"></span><span id="error_log_container_read_failed"></span>**ERROR\_LOG\_CONTAINER\_READ\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-304">6639 (0x19EF)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-304">6639 (0x19EF)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-305">El servicio de registro encontró un error al intentar leer desde un contenedor de registros.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-305">Log service encountered an error when attempting to read from a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-306"><span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**error de escritura en el contenedor de registro de errores \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-306"><span id="ERROR_LOG_CONTAINER_WRITE_FAILED"></span><span id="error_log_container_write_failed"></span>**ERROR\_LOG\_CONTAINER\_WRITE\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-307">6640 (0x19F0)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-307">6640 (0x19F0)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-308">El servicio de registro encontró un error al intentar escribir en un contenedor de registro.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-308">Log service encountered an error when attempting to write to a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-309"><span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**error \_ \_ al abrir el contenedor del registro de \_ errores \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-309"><span id="ERROR_LOG_CONTAINER_OPEN_FAILED"></span><span id="error_log_container_open_failed"></span>**ERROR\_LOG\_CONTAINER\_OPEN\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-310">6641 (0x19F1)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-310">6641 (0x19F1)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-311">El servicio de registro encontró un error al intentar abrir un contenedor de registros.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-311">Log service encountered an error when attempting open a log container.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-312"><span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**Estado del contenedor de registro de errores \_ \_ \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-312"><span id="ERROR_LOG_CONTAINER_STATE_INVALID"></span><span id="error_log_container_state_invalid"></span>**ERROR\_LOG\_CONTAINER\_STATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-313">6642 (0x19F2)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-313">6642 (0x19F2)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-314">El servicio de registro encontró un estado de contenedor no válido al intentar una acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-314">Log service encountered an invalid container state when attempting a requested action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-315"><span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**Estado de registro de errores \_ \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-315"><span id="ERROR_LOG_STATE_INVALID"></span><span id="error_log_state_invalid"></span>**ERROR\_LOG\_STATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-316">6643 (0x19F3)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-316">6643 (0x19F3)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-317">El servicio de registro no está en el estado correcto para realizar una acción solicitada.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-317">Log service is not in the correct state to perform a requested action.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-318"><span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**registro de errores \_ \_ anclado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-318"><span id="ERROR_LOG_PINNED"></span><span id="error_log_pinned"></span>**ERROR\_LOG\_PINNED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-319">6644 (0x19F4)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-319">6644 (0x19F4)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-320">No se puede reclamar el espacio del registro porque el registro está anclado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-320">Log space cannot be reclaimed because the log is pinned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-321"><span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**error \_ de \_ vaciado de metadatos de registro de \_ errores \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-321"><span id="ERROR_LOG_METADATA_FLUSH_FAILED"></span><span id="error_log_metadata_flush_failed"></span>**ERROR\_LOG\_METADATA\_FLUSH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-322">6645 (0x19F5)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-322">6645 (0x19F5)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-323">Error de vaciado de metadatos de registro.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-323">Log metadata flush failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-324"><span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**\_ \_ seguridad incoherente del registro de errores \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-324"><span id="ERROR_LOG_INCONSISTENT_SECURITY"></span><span id="error_log_inconsistent_security"></span>**ERROR\_LOG\_INCONSISTENT\_SECURITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-325">6646 (0x19F6)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-325">6646 (0x19F6)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-326">La seguridad en el registro y sus contenedores es incoherente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-326">Security on the log and its containers is inconsistent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-327"><span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**error \_ de \_ vaciado anexado de registro de \_ errores \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-327"><span id="ERROR_LOG_APPENDED_FLUSH_FAILED"></span><span id="error_log_appended_flush_failed"></span>**ERROR\_LOG\_APPENDED\_FLUSH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-328">6647 (0x19F7)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-328">6647 (0x19F7)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-329">Se anexaron registros al registro o se realizaron cambios en la reserva, pero no se pudo vaciar el registro.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-329">Records were appended to the log or reservation changes were made, but the log could not be flushed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-330"><span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**\_ \_ reserva anclada del registro de errores \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-330"><span id="ERROR_LOG_PINNED_RESERVATION"></span><span id="error_log_pinned_reservation"></span>**ERROR\_LOG\_PINNED\_RESERVATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-331">6648 (0x19F8)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-331">6648 (0x19F8)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-332">El registro está anclado debido a la reserva que consume la mayor parte del espacio del registro.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-332">The log is pinned due to reservation consuming most of the log space.</span></span> <span data-ttu-id="b7eb9-333">Libere algunos registros reservados para dejar espacio disponible.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-333">Free some reserved records to make space available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-334"><span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERROR \_ de \_ transacción no válida**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-334"><span id="ERROR_INVALID_TRANSACTION"></span><span id="error_invalid_transaction"></span>**ERROR\_INVALID\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-335">6700 (0x1A2C)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-335">6700 (0x1A2C)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-336">El identificador de transacción asociado a esta operación no es válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-336">The transaction handle associated with this operation is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-337"><span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**ERROR de \_ transacción \_ no \_ activa**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-337"><span id="ERROR_TRANSACTION_NOT_ACTIVE"></span><span id="error_transaction_not_active"></span>**ERROR\_TRANSACTION\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-338">6701 (0x1A2D)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-338">6701 (0x1A2D)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-339">La operación solicitada se realizó en el contexto de una transacción que ya no está activa.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-339">The requested operation was made in the context of a transaction that is no longer active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-340"><span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**ERROR \_ de \_ solicitud de transacción \_ no \_ válida**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-340"><span id="ERROR_TRANSACTION_REQUEST_NOT_VALID"></span><span id="error_transaction_request_not_valid"></span>**ERROR\_TRANSACTION\_REQUEST\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-341">6702 (0x1A2E)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-341">6702 (0x1A2E)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-342">La operación solicitada no es válida en el objeto de transacción en su estado actual.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-342">The requested operation is not valid on the Transaction object in its current state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-343"><span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**\_no se \_ solicitó la transacción de error \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-343"><span id="ERROR_TRANSACTION_NOT_REQUESTED"></span><span id="error_transaction_not_requested"></span>**ERROR\_TRANSACTION\_NOT\_REQUESTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-344">6703 (0x1A2F)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-344">6703 (0x1A2F)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-345">El autor de la llamada ha llamado a una API de respuesta, pero no se espera la respuesta porque TM no ha emitido la solicitud correspondiente al llamador.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-345">The caller has called a response API, but the response is not expected because the TM did not issue the corresponding request to the caller.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-346"><span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**transacción de ERROR \_ \_ ya \_ anulada**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-346"><span id="ERROR_TRANSACTION_ALREADY_ABORTED"></span><span id="error_transaction_already_aborted"></span>**ERROR\_TRANSACTION\_ALREADY\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-347">6704 (0x1A30)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-347">6704 (0x1A30)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-348">Es demasiado tarde para realizar la operación solicitada, ya que la transacción ya se ha anulado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-348">It is too late to perform the requested operation, since the Transaction has already been aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-349"><span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**transacción de ERROR \_ \_ ya \_ confirmada**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-349"><span id="ERROR_TRANSACTION_ALREADY_COMMITTED"></span><span id="error_transaction_already_committed"></span>**ERROR\_TRANSACTION\_ALREADY\_COMMITTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-350">6705 (0x1A31)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-350">6705 (0x1A31)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-351">Es demasiado tarde para realizar la operación solicitada, puesto que ya se ha confirmado la transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-351">It is too late to perform the requested operation, since the Transaction has already been committed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-352"><span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**ERROR \_ de \_ inicialización de TM \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-352"><span id="ERROR_TM_INITIALIZATION_FAILED"></span><span id="error_tm_initialization_failed"></span>**ERROR\_TM\_INITIALIZATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-353">6706 (0x1A32)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-353">6706 (0x1A32)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-354">No se pudo inicializar correctamente el administrador de transacciones.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-354">The Transaction Manager was unable to be successfully initialized.</span></span> <span data-ttu-id="b7eb9-355">No se admiten las operaciones de transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-355">Transacted operations are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-356"><span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERROR \_ RESOURCEMANAGER \_ - \_ solo lectura**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-356"><span id="ERROR_RESOURCEMANAGER_READ_ONLY"></span><span id="error_resourcemanager_read_only"></span>**ERROR\_RESOURCEMANAGER\_READ\_ONLY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-357">6707 (0x1A33)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-357">6707 (0x1A33)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-358">El ResourceManager especificado no realizó cambios ni actualizaciones en el recurso en esta transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-358">The specified ResourceManager made no changes or updates to the resource under this transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-359"><span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**ERROR de \_ transacción \_ no \_ unida**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-359"><span id="ERROR_TRANSACTION_NOT_JOINED"></span><span id="error_transaction_not_joined"></span>**ERROR\_TRANSACTION\_NOT\_JOINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-360">6708 (0x1A34)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-360">6708 (0x1A34)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-361">Resource Manager intentó preparar una transacción que no se ha unido correctamente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-361">The resource manager has attempted to prepare a transaction that it has not successfully joined.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-362"><span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**existe una transacción de ERROR \_ \_ superior \_ existente**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-362"><span id="ERROR_TRANSACTION_SUPERIOR_EXISTS"></span><span id="error_transaction_superior_exists"></span>**ERROR\_TRANSACTION\_SUPERIOR\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-363">6709 (0x1A35)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-363">6709 (0x1A35)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-364">El objeto de transacción ya tiene una inscripción superior y el llamador intentó realizar una operación que habría creado un nuevo superior.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-364">The Transaction object already has a superior enlistment, and the caller attempted an operation that would have created a new superior.</span></span> <span data-ttu-id="b7eb9-365">Solo se permite una inscripción superior.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-365">Only a single superior enlistment is allow.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-366"><span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**el \_ Protocolo CRM de error \_ \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-366"><span id="ERROR_CRM_PROTOCOL_ALREADY_EXISTS"></span><span id="error_crm_protocol_already_exists"></span>**ERROR\_CRM\_PROTOCOL\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-367">6710 (0x1A36)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-367">6710 (0x1A36)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-368">El RM ha intentado registrar un protocolo que ya existe.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-368">The RM tried to register a protocol that already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-369"><span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**ERROR en la propagación de la \_ transacción \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-369"><span id="ERROR_TRANSACTION_PROPAGATION_FAILED"></span><span id="error_transaction_propagation_failed"></span>**ERROR\_TRANSACTION\_PROPAGATION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-370">6711 (0x1A37)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-370">6711 (0x1A37)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-371">Error al tratar de propagar la transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-371">The attempt to propagate the Transaction failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-372"><span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERROR \_ de \_ Protocolo CRM \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-372"><span id="ERROR_CRM_PROTOCOL_NOT_FOUND"></span><span id="error_crm_protocol_not_found"></span>**ERROR\_CRM\_PROTOCOL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-373">6712 (0x1A38)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-373">6712 (0x1A38)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-374">El protocolo de propagación solicitado no se registró como CRM.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-374">The requested propagation protocol was not registered as a CRM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-375"><span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**ERROR de \_ búfer de referencia de transacción \_ no válido \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-375"><span id="ERROR_TRANSACTION_INVALID_MARSHALL_BUFFER"></span><span id="error_transaction_invalid_marshall_buffer"></span>**ERROR\_TRANSACTION\_INVALID\_MARSHALL\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-376">6713 (0x1A39)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-376">6713 (0x1A39)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-377">El búfer pasado a PushTransaction o PullTransaction no tiene un formato válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-377">The buffer passed in to PushTransaction or PullTransaction is not in a valid format.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-378"><span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**ERROR \_ de \_ transacción actual \_ no \_ válida**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-378"><span id="ERROR_CURRENT_TRANSACTION_NOT_VALID"></span><span id="error_current_transaction_not_valid"></span>**ERROR\_CURRENT\_TRANSACTION\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-379">6714 (0x1A3A)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-379">6714 (0x1A3A)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-380">El contexto de transacción actual asociado al subproceso no es un identificador válido para un objeto de transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-380">The current transaction context associated with the thread is not a valid handle to a transaction object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-381"><span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**\_ \_ no \_ se encontró la transacción de error**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-381"><span id="ERROR_TRANSACTION_NOT_FOUND"></span><span id="error_transaction_not_found"></span>**ERROR\_TRANSACTION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-382">6715 (0x1A3B)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-382">6715 (0x1A3B)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-383">No se pudo abrir el objeto de transacción especificado porque no se encontró.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-383">The specified Transaction object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-384"><span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERROR \_ RESOURCEMANAGER \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-384"><span id="ERROR_RESOURCEMANAGER_NOT_FOUND"></span><span id="error_resourcemanager_not_found"></span>**ERROR\_RESOURCEMANAGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-385">6716 (0x1A3C)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-385">6716 (0x1A3C)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-386">No se pudo abrir el objeto ResourceManager especificado porque no se encontró.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-386">The specified ResourceManager object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-387"><span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**\_ \_ no se encontró la inscripción \_ de errores**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-387"><span id="ERROR_ENLISTMENT_NOT_FOUND"></span><span id="error_enlistment_not_found"></span>**ERROR\_ENLISTMENT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-388">6717 (0x1A3D)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-388">6717 (0x1A3D)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-389">No se pudo abrir el objeto de inscripción especificado porque no se encontró.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-389">The specified Enlistment object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-390"><span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERROR \_ TRANSACTIONMANAGER \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-390"><span id="ERROR_TRANSACTIONMANAGER_NOT_FOUND"></span><span id="error_transactionmanager_not_found"></span>**ERROR\_TRANSACTIONMANAGER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-391">6718 (0x1A3E)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-391">6718 (0x1A3E)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-392">No se pudo abrir el objeto TransactionManager especificado porque no se encontró.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-392">The specified TransactionManager object could not be opened, because it was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-393"><span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERROR \_ TRANSACTIONMANAGER \_ no está \_ en línea**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-393"><span id="ERROR_TRANSACTIONMANAGER_NOT_ONLINE"></span><span id="error_transactionmanager_not_online"></span>**ERROR\_TRANSACTIONMANAGER\_NOT\_ONLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-394">6719 (0x1A3F)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-394">6719 (0x1A3F)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-395">No se pudo crear o abrir el objeto especificado porque su TransactionManager asociado no está en línea.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-395">The object specified could not be created or opened, because its associated TransactionManager is not online.</span></span> <span data-ttu-id="b7eb9-396">El TransactionManager debe estar totalmente en línea mediante una llamada a RecoverTransactionManager para recuperar hasta el final de su archivo de registro antes de que se puedan abrir los objetos de la transacción o los espacios de nombres ResourceManager.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-396">The TransactionManager must be brought fully Online by calling RecoverTransactionManager to recover to the end of its LogFile before objects in its Transaction or ResourceManager namespaces can be opened.</span></span> <span data-ttu-id="b7eb9-397">Además, los errores en la escritura de registros en el archivo de registro pueden hacer que un TransactionManager quede sin conexión.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-397">In addition, errors in writing records to its LogFile can cause a TransactionManager to go offline.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-398"><span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERROR \_ TRANSACTIONMANAGER de la colisión de \_ nombres de recuperación \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-398"><span id="ERROR_TRANSACTIONMANAGER_RECOVERY_NAME_COLLISION"></span><span id="error_transactionmanager_recovery_name_collision"></span>**ERROR\_TRANSACTIONMANAGER\_RECOVERY\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-399">6720 (0x1A40)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-399">6720 (0x1A40)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-400">El TransactionManager especificado no pudo crear los objetos contenidos en su archivo de registro en el espacio de nombres ob.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-400">The specified TransactionManager was unable to create the objects contained in its logfile in the Ob namespace.</span></span> <span data-ttu-id="b7eb9-401">Por lo tanto, el TransactionManager no se pudo recuperar.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-401">Therefore, the TransactionManager was unable to recover.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-402"><span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**ERROR de \_ transacción \_ no \_ raíz**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-402"><span id="ERROR_TRANSACTION_NOT_ROOT"></span><span id="error_transaction_not_root"></span>**ERROR\_TRANSACTION\_NOT\_ROOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-403">6721 (0x1A41)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-403">6721 (0x1A41)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-404">No se pudo completar la llamada para crear una inscripción superior en este objeto de transacción porque el objeto de transacción especificado para la inscripción es una rama subordinada de la transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-404">The call to create a superior Enlistment on this Transaction object could not be completed, because the Transaction object specified for the enlistment is a subordinate branch of the Transaction.</span></span> <span data-ttu-id="b7eb9-405">Solo se puede dar de alta la raíz de la transacción en como un nivel superior.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-405">Only the root of the Transaction can be enlisted on as a superior.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-406"><span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**objeto de transacción de ERROR \_ \_ \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-406"><span id="ERROR_TRANSACTION_OBJECT_EXPIRED"></span><span id="error_transaction_object_expired"></span>**ERROR\_TRANSACTION\_OBJECT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-407">6722 (0x1A42)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-407">6722 (0x1A42)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-408">Dado que el administrador de transacciones asociado o el administrador de recursos se ha cerrado, el identificador ya no es válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-408">Because the associated transaction manager or resource manager has been closed, the handle is no longer valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-409"><span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**respuesta de transacción de ERROR \_ \_ \_ no \_ dada de alta**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-409"><span id="ERROR_TRANSACTION_RESPONSE_NOT_ENLISTED"></span><span id="error_transaction_response_not_enlisted"></span>**ERROR\_TRANSACTION\_RESPONSE\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-410">6723 (0x1A43)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-410">6723 (0x1A43)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-411">No se pudo realizar la operación especificada en esta inscripción superior porque la inscripción no se creó con la respuesta de finalización correspondiente en NotificationMask.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-411">The specified operation could not be performed on this Superior enlistment, because the enlistment was not created with the corresponding completion response in the NotificationMask.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-412"><span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**registro de transacción de ERROR \_ \_ \_ demasiado \_ largo**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-412"><span id="ERROR_TRANSACTION_RECORD_TOO_LONG"></span><span id="error_transaction_record_too_long"></span>**ERROR\_TRANSACTION\_RECORD\_TOO\_LONG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-413">6724 (0x1A44)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-413">6724 (0x1A44)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-414">No se pudo realizar la operación especificada porque el registro que se registraría era demasiado largo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-414">The specified operation could not be performed, because the record that would be logged was too long.</span></span> <span data-ttu-id="b7eb9-415">Esto puede deberse a dos condiciones: hay demasiadas inscritos en esta transacción o la combinación de RecoveryInformation que se está registrando en nombre de las inscritos es demasiado larga.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-415">This can occur because of two conditions: either there are too many Enlistments on this Transaction, or the combined RecoveryInformation being logged on behalf of those Enlistments is too long.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-416"><span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**ERROR \_ de \_ transacción implícita \_ no \_ compatible**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-416"><span id="ERROR_IMPLICIT_TRANSACTION_NOT_SUPPORTED"></span><span id="error_implicit_transaction_not_supported"></span>**ERROR\_IMPLICIT\_TRANSACTION\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-417">6725 (0x1A45)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-417">6725 (0x1A45)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-418">No se admiten las transacciones implícitas.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-418">Implicit transaction are not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-419"><span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**ERROR \_ de \_ integridad de transacción \_ infringida**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-419"><span id="ERROR_TRANSACTION_INTEGRITY_VIOLATED"></span><span id="error_transaction_integrity_violated"></span>**ERROR\_TRANSACTION\_INTEGRITY\_VIOLATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-420">6726 (0x1A46)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-420">6726 (0x1A46)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-421">El administrador de transacciones de kernel tenía que anular u olvidar la transacción porque bloqueó el progreso de avance.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-421">The kernel transaction manager had to abort or forget the transaction because it blocked forward progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-422"><span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERROR \_ de \_ desigualdad de identidad de TRANSACTIONMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-422"><span id="ERROR_TRANSACTIONMANAGER_IDENTITY_MISMATCH"></span><span id="error_transactionmanager_identity_mismatch"></span>**ERROR\_TRANSACTIONMANAGER\_IDENTITY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-423">6727 (0x1A47)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-423">6727 (0x1A47)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-424">La identidad TransactionManager suministrada no coincidía con la que se registró en el archivo de registro de TransactionManager.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-424">The TransactionManager identity that was supplied did not match the one recorded in the TransactionManager's log file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-425"><span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**\_ \_ no se puede \_ \_ inmovilizar el error RM \_ para la \_ instantánea**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-425"><span id="ERROR_RM_CANNOT_BE_FROZEN_FOR_SNAPSHOT"></span><span id="error_rm_cannot_be_frozen_for_snapshot"></span>**ERROR\_RM\_CANNOT\_BE\_FROZEN\_FOR\_SNAPSHOT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-426">6728 (0x1A48)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-426">6728 (0x1A48)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-427">Esta operación de instantánea no puede continuar porque un administrador de recursos transaccional no se puede inmovilizar en su estado actual.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-427">This snapshot operation cannot continue because a transactional resource manager cannot be frozen in its current state.</span></span> <span data-ttu-id="b7eb9-428">Inténtelo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-428">Please try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-429"><span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**la \_ transacción de error \_ debe \_ WRITETHROUGH**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-429"><span id="ERROR_TRANSACTION_MUST_WRITETHROUGH"></span><span id="error_transaction_must_writethrough"></span>**ERROR\_TRANSACTION\_MUST\_WRITETHROUGH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-430">6729 (0x1A49)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-430">6729 (0x1A49)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-431">No se puede dar de alta la transacción en con el EnlistmentMask especificado, porque la transacción ya ha completado la fase de prepreparación.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-431">The transaction cannot be enlisted on with the specified EnlistmentMask, because the transaction has already completed the PrePrepare phase.</span></span> <span data-ttu-id="b7eb9-432">Para garantizar la exactitud, ResourceManager debe cambiar a un modo de escritura a través y dejar de almacenar en caché los datos en esta transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-432">In order to ensure correctness, the ResourceManager must switch to a write- through mode and cease caching data within this transaction.</span></span> <span data-ttu-id="b7eb9-433">La inscripción solo en fases posteriores de la transacción puede realizarse correctamente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-433">Enlisting for only subsequent transaction phases may still succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-434"><span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**ERROR de \_ transacción \_ no \_ superior**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-434"><span id="ERROR_TRANSACTION_NO_SUPERIOR"></span><span id="error_transaction_no_superior"></span>**ERROR\_TRANSACTION\_NO\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-435">6730 (0x1A4A)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-435">6730 (0x1A4A)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-436">La transacción no tiene una inscripción superior.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-436">The transaction does not have a superior enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-437"><span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**daños en la heurística de errores \_ \_ \_ posibles**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-437"><span id="ERROR_HEURISTIC_DAMAGE_POSSIBLE"></span><span id="error_heuristic_damage_possible"></span>**ERROR\_HEURISTIC\_DAMAGE\_POSSIBLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-438">6731 (0x1A4B)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-438">6731 (0x1A4B)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-439">Se completó el intento de confirmar la transacción, pero es posible que alguna parte del árbol de transacciones no se confirmara correctamente debido a la heurística.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-439">The attempt to commit the Transaction completed, but it is possible that some portion of the transaction tree did not commit successfully due to heuristics.</span></span> <span data-ttu-id="b7eb9-440">Por lo tanto, es posible que algunos datos modificados en la transacción no se hayan confirmado, lo que provoca una incoherencia transaccional.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-440">Therefore it is possible that some data modified in the transaction may not have committed, resulting in transactional inconsistency.</span></span> <span data-ttu-id="b7eb9-441">Si es posible, Compruebe la coherencia de los datos asociados.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-441">If possible, check the consistency of the associated data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-442"><span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**\_conflicto transaccional de errores \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-442"><span id="ERROR_TRANSACTIONAL_CONFLICT"></span><span id="error_transactional_conflict"></span>**ERROR\_TRANSACTIONAL\_CONFLICT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-443">6800 (0x1A90)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-443">6800 (0x1A90)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-444">La función intentó utilizar un nombre que está reservado para su uso por otra transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-444">The function attempted to use a name that is reserved for use by another transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-445"><span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERROR \_ RM \_ no \_ activo**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-445"><span id="ERROR_RM_NOT_ACTIVE"></span><span id="error_rm_not_active"></span>**ERROR\_RM\_NOT\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-446">6801 (0x1A91)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-446">6801 (0x1A91)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-447">La compatibilidad con transacciones en el administrador de recursos especificado no se inició o se apagó debido a un error.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-447">Transaction support within the specified resource manager is not started or was shut down due to an error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-448"><span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERROR \_ de \_ metadatos de RM \_ dañados**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-448"><span id="ERROR_RM_METADATA_CORRUPT"></span><span id="error_rm_metadata_corrupt"></span>**ERROR\_RM\_METADATA\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-449">6802 (0x1A92)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-449">6802 (0x1A92)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-450">Los metadatos de RM están dañados.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-450">The metadata of the RM has been corrupted.</span></span> <span data-ttu-id="b7eb9-451">El RM no funcionará.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-451">The RM will not function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-452"><span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**directorio de errores \_ \_ no \_ RM**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-452"><span id="ERROR_DIRECTORY_NOT_RM"></span><span id="error_directory_not_rm"></span>**ERROR\_DIRECTORY\_NOT\_RM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-453">6803 (0x1A93)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-453">6803 (0x1A93)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-454">El directorio especificado no contiene un administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-454">The specified directory does not contain a resource manager.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-455"><span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**transacciones de ERROR \_ \_ remotas no admitidas \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-455"><span id="ERROR_TRANSACTIONS_UNSUPPORTED_REMOTE"></span><span id="error_transactions_unsupported_remote"></span>**ERROR\_TRANSACTIONS\_UNSUPPORTED\_REMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-456">6805 (0x1A95)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-456">6805 (0x1A95)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-457">El recurso compartido o el servidor remoto no admiten operaciones de archivo de transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-457">The remote server or share does not support transacted file operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-458"><span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**tamaño de registro de errores de \_ \_ \_ tamaño no válido \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-458"><span id="ERROR_LOG_RESIZE_INVALID_SIZE"></span><span id="error_log_resize_invalid_size"></span>**ERROR\_LOG\_RESIZE\_INVALID\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-459">6806 (0x1A96)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-459">6806 (0x1A96)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-460">El tamaño de registro solicitado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-460">The requested log size is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-461"><span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**el objeto de ERROR ya \_ \_ no \_ \_ existe**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-461"><span id="ERROR_OBJECT_NO_LONGER_EXISTS"></span><span id="error_object_no_longer_exists"></span>**ERROR\_OBJECT\_NO\_LONGER\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-462">6807 (0x1A97)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-462">6807 (0x1A97)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-463">La reversión de un punto de retorno de la transacción ha eliminado el objeto (archivo, secuencia, vínculo) correspondiente al identificador.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-463">The object (file, stream, link) corresponding to the handle has been deleted by a Transaction Savepoint Rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-464"><span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**\_ \_ \_ no \_ se encontró la MINIVERSIÓN del flujo de error**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-464"><span id="ERROR_STREAM_MINIVERSION_NOT_FOUND"></span><span id="error_stream_miniversion_not_found"></span>**ERROR\_STREAM\_MINIVERSION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-465">6808 (0x1A98)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-465">6808 (0x1A98)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-466">No se encontró la miniversión de archivo especificada para este archivo de transacción abierto.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-466">The specified file miniversion was not found for this transacted file open.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-467"><span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**la \_ miniversión del flujo de error \_ \_ no \_ es válida**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-467"><span id="ERROR_STREAM_MINIVERSION_NOT_VALID"></span><span id="error_stream_miniversion_not_valid"></span>**ERROR\_STREAM\_MINIVERSION\_NOT\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-468">6809 (0x1A99)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-468">6809 (0x1A99)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-469">Se encontró la miniversión de archivo especificada, pero se invalidó.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-469">The specified file miniversion was found but has been invalidated.</span></span> <span data-ttu-id="b7eb9-470">La causa más probable es la reversión de un punto de retorno de transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-470">Most likely cause is a transaction savepoint rollback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-471"><span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERROR \_ \_ de MINIVERSIÓN inaccesible \_ desde \_ la \_ transacción especificada**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-471"><span id="ERROR_MINIVERSION_INACCESSIBLE_FROM_SPECIFIED_TRANSACTION"></span><span id="error_miniversion_inaccessible_from_specified_transaction"></span>**ERROR\_MINIVERSION\_INACCESSIBLE\_FROM\_SPECIFIED\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-472">6810 (0x1A9A)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-472">6810 (0x1A9A)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-473">Una miniversión solo se puede abrir en el contexto de la transacción que la creó.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-473">A miniversion may only be opened in the context of the transaction that created it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-474"><span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERROR no se pudo \_ \_ abrir la \_ miniversión con el \_ \_ intento de modificación \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-474"><span id="ERROR_CANT_OPEN_MINIVERSION_WITH_MODIFY_INTENT"></span><span id="error_cant_open_miniversion_with_modify_intent"></span>**ERROR\_CANT\_OPEN\_MINIVERSION\_WITH\_MODIFY\_INTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-475">6811 (0x1A9B)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-475">6811 (0x1A9B)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-476">No es posible abrir una miniversión con el acceso de modificación.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-476">It is not possible to open a miniversion with modify access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-477"><span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ERROR no se pudo \_ \_ crear \_ más \_ secuencia \_ MINIVERSIONS**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-477"><span id="ERROR_CANT_CREATE_MORE_STREAM_MINIVERSIONS"></span><span id="error_cant_create_more_stream_miniversions"></span>**ERROR\_CANT\_CREATE\_MORE\_STREAM\_MINIVERSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-478">6812 (0x1A9C)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-478">6812 (0x1A9C)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-479">No es posible crear más miniversions para esta secuencia.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-479">It is not possible to create any more miniversions for this stream.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-480"><span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERROR \_ de \_ \_ coincidencia de versión de archivo remoto \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-480"><span id="ERROR_REMOTE_FILE_VERSION_MISMATCH"></span><span id="error_remote_file_version_mismatch"></span>**ERROR\_REMOTE\_FILE\_VERSION\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-481">6814 (0x1A9E)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-481">6814 (0x1A9E)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-482">El servidor remoto ha enviado un número de versión o FID no coincidente para un archivo abierto con transacciones.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-482">The remote server sent mismatching version number or Fid for a file opened with transactions.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-483"><span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**el identificador de ERROR ya \_ \_ no \_ \_ es válido**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-483"><span id="ERROR_HANDLE_NO_LONGER_VALID"></span><span id="error_handle_no_longer_valid"></span>**ERROR\_HANDLE\_NO\_LONGER\_VALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-484">6815 (0x1A9F)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-484">6815 (0x1A9F)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-485">Una transacción ha invalidado el identificador.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-485">The handle has been invalidated by a transaction.</span></span> <span data-ttu-id="b7eb9-486">La causa más probable es la presencia de la asignación de memoria en un archivo o un controlador abierto cuando la transacción finaliza o se revierte al punto de retorno.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-486">The most likely cause is the presence of memory mapping on a file or an open handle when the transaction ended or rolled back to savepoint.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-487"><span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERROR: \_ no hay \_ \_ metadatos de TxF**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-487"><span id="ERROR_NO_TXF_METADATA"></span><span id="error_no_txf_metadata"></span>**ERROR\_NO\_TXF\_METADATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-488">6816 (0x1AA0)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-488">6816 (0x1AA0)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-489">No hay metadatos de transacción en el archivo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-489">There is no transaction metadata on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-490"><span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**daños en el registro de errores \_ \_ \_ detectados**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-490"><span id="ERROR_LOG_CORRUPTION_DETECTED"></span><span id="error_log_corruption_detected"></span>**ERROR\_LOG\_CORRUPTION\_DETECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-491">6817 (0x1AA1)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-491">6817 (0x1AA1)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-492">Los datos de registro están dañados.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-492">The log data is corrupt.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-493"><span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**ERROR no se pudo \_ \_ recuperar \_ con el \_ identificador \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-493"><span id="ERROR_CANT_RECOVER_WITH_HANDLE_OPEN"></span><span id="error_cant_recover_with_handle_open"></span>**ERROR\_CANT\_RECOVER\_WITH\_HANDLE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-494">6818 (0x1AA2)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-494">6818 (0x1AA2)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-495">No se puede recuperar el archivo porque todavía hay un controlador abierto en él.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-495">The file can't be recovered because there is a handle still open on it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-496"><span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERROR de \_ RM \_ desconectado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-496"><span id="ERROR_RM_DISCONNECTED"></span><span id="error_rm_disconnected"></span>**ERROR\_RM\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-497">6819 (0x1AA3)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-497">6819 (0x1AA3)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-498">El resultado de la transacción no está disponible porque el administrador de recursos responsable se ha desconectado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-498">The transaction outcome is unavailable because the resource manager responsible for it has disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-499"><span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**INSCRIPCIÓN de ERROR \_ \_ no \_ superior**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-499"><span id="ERROR_ENLISTMENT_NOT_SUPERIOR"></span><span id="error_enlistment_not_superior"></span>**ERROR\_ENLISTMENT\_NOT\_SUPERIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-500">6820 (0x1AA4)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-500">6820 (0x1AA4)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-501">Se rechazó la solicitud porque la inscripción en cuestión no es una inscripción superior.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-501">The request was rejected because the enlistment in question is not a superior enlistment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-502"><span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**recuperación de errores \_ \_ no \_ necesaria**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-502"><span id="ERROR_RECOVERY_NOT_NEEDED"></span><span id="error_recovery_not_needed"></span>**ERROR\_RECOVERY\_NOT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-503">6821 (0x1AA5)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-503">6821 (0x1AA5)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-504">El administrador de recursos transaccional ya es coherente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-504">The transactional resource manager is already consistent.</span></span> <span data-ttu-id="b7eb9-505">No es necesaria la recuperación.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-505">Recovery is not needed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-506"><span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**ERROR \_ RM \_ ya \_ iniciado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-506"><span id="ERROR_RM_ALREADY_STARTED"></span><span id="error_rm_already_started"></span>**ERROR\_RM\_ALREADY\_STARTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-507">6822 (0x1AA6)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-507">6822 (0x1AA6)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-508">El administrador de recursos de transacciones ya se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-508">The transactional resource manager has already been started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-509"><span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**la \_ identidad del archivo de error \_ no es \_ \_ persistente**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-509"><span id="ERROR_FILE_IDENTITY_NOT_PERSISTENT"></span><span id="error_file_identity_not_persistent"></span>**ERROR\_FILE\_IDENTITY\_NOT\_PERSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-510">6823 (0x1AA7)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-510">6823 (0x1AA7)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-511">No se puede abrir el archivo de transacciones, porque su identidad depende del resultado de una transacción no resuelta.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-511">The file cannot be opened transactionally, because its identity depends on the outcome of an unresolved transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-512"><span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ERROR no se pudo \_ \_ interrumpir la \_ \_ dependencia transaccional**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-512"><span id="ERROR_CANT_BREAK_TRANSACTIONAL_DEPENDENCY"></span><span id="error_cant_break_transactional_dependency"></span>**ERROR\_CANT\_BREAK\_TRANSACTIONAL\_DEPENDENCY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-513">6824 (0x1AA8)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-513">6824 (0x1AA8)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-514">No se puede realizar la operación porque otra transacción depende del hecho de que esta propiedad no cambie.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-514">The operation cannot be performed because another transaction is depending on the fact that this property will not change.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-515"><span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**no se pudo obtener el \_ \_ \_ límite de RM cruzado \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-515"><span id="ERROR_CANT_CROSS_RM_BOUNDARY"></span><span id="error_cant_cross_rm_boundary"></span>**ERROR\_CANT\_CROSS\_RM\_BOUNDARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-516">6825 (0x1AA9)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-516">6825 (0x1AA9)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-517">La operación implicaría un solo archivo con dos administradores de recursos transaccionales y, por lo tanto, no se permite.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-517">The operation would involve a single file with two transactional resource managers and is therefore not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-518"><span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERROR \_ dir de TxF \_ \_ no \_ vacío**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-518"><span id="ERROR_TXF_DIR_NOT_EMPTY"></span><span id="error_txf_dir_not_empty"></span>**ERROR\_TXF\_DIR\_NOT\_EMPTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-519">6826 (0x1AAA)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-519">6826 (0x1AAA)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-520">El directorio $Txf debe estar vacío para que esta operación se realice correctamente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-520">The $Txf directory must be empty for this operation to succeed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-521"><span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**\_ \_ existen transacciones de ERROR de errores \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-521"><span id="ERROR_INDOUBT_TRANSACTIONS_EXIST"></span><span id="error_indoubt_transactions_exist"></span>**ERROR\_INDOUBT\_TRANSACTIONS\_EXIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-522">6827 (0x1AAB)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-522">6827 (0x1AAB)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-523">La operación dejaría un administrador de recursos transaccional en un estado incoherente y, por lo tanto, no se permite.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-523">The operation would leave a transactional resource manager in an inconsistent state and is therefore not allowed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-524"><span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERROR \_ TM \_ volatile**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-524"><span id="ERROR_TM_VOLATILE"></span><span id="error_tm_volatile"></span>**ERROR\_TM\_VOLATILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-525">6828 (0x1AAC)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-525">6828 (0x1AAC)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-526">No se pudo completar la operación porque el administrador de transacciones no tiene un registro.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-526">The operation could not be completed because the transaction manager does not have a log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-527"><span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**ERROR \_ del temporizador de reversión \_ \_ expirado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-527"><span id="ERROR_ROLLBACK_TIMER_EXPIRED"></span><span id="error_rollback_timer_expired"></span>**ERROR\_ROLLBACK\_TIMER\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-528">6829 (0x1AAD)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-528">6829 (0x1AAD)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-529">No se pudo programar una reversión porque ya se ejecutó una reversión programada anteriormente o se puso en cola para su ejecución.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-529">A rollback could not be scheduled because a previously scheduled rollback has already executed or been queued for execution.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-530"><span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**atributo de TxF de ERROR \_ \_ \_ dañado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-530"><span id="ERROR_TXF_ATTRIBUTE_CORRUPT"></span><span id="error_txf_attribute_corrupt"></span>**ERROR\_TXF\_ATTRIBUTE\_CORRUPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-531">6830 (0x1AAE)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-531">6830 (0x1AAE)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-532">El atributo de metadatos transaccional del archivo o directorio está dañado y es ilegible.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-532">The transactional metadata attribute on the file or directory is corrupt and unreadable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-533"><span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERROR \_ \_ de EFS no \_ permitido en la \_ \_ transacción**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-533"><span id="ERROR_EFS_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_efs_not_allowed_in_transaction"></span>**ERROR\_EFS\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-534">6831 (0x1AAF)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-534">6831 (0x1AAF)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-535">No se pudo completar la operación de cifrado porque una transacción está activa.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-535">The encryption operation could not be completed because a transaction is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-536"><span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERROR de \_ apertura transaccional \_ \_ no \_ permitida**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-536"><span id="ERROR_TRANSACTIONAL_OPEN_NOT_ALLOWED"></span><span id="error_transactional_open_not_allowed"></span>**ERROR\_TRANSACTIONAL\_OPEN\_NOT\_ALLOWED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-537">6832 (0x1AB0)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-537">6832 (0x1AB0)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-538">No se permite abrir este objeto en una transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-538">This object is not allowed to be opened in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-539"><span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**error de \_ crecimiento del registro de errores \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-539"><span id="ERROR_LOG_GROWTH_FAILED"></span><span id="error_log_growth_failed"></span>**ERROR\_LOG\_GROWTH\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-540">6833 (0x1AB1)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-540">6833 (0x1AB1)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-541">Error al tratar de crear espacio en el registro del administrador de recursos transaccionales.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-541">An attempt to create space in the transactional resource manager's log failed.</span></span> <span data-ttu-id="b7eb9-542">El estado de error se ha registrado en el registro de eventos.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-542">The failure status has been recorded in the event log.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-543"><span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERROR de \_ asignación de transacción \_ \_ remota no admitida \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-543"><span id="ERROR_TRANSACTED_MAPPING_UNSUPPORTED_REMOTE"></span><span id="error_transacted_mapping_unsupported_remote"></span>**ERROR\_TRANSACTED\_MAPPING\_UNSUPPORTED\_REMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-544">6834 (0x1AB2)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-544">6834 (0x1AB2)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-545">No se admite la asignación de memoria (creación de una sección asignada) a un archivo remoto en una transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-545">Memory mapping (creating a mapped section) a remote file under a transaction is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-546"><span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**los \_ metadatos de TxF de error \_ \_ ya están \_ presentes**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-546"><span id="ERROR_TXF_METADATA_ALREADY_PRESENT"></span><span id="error_txf_metadata_already_present"></span>**ERROR\_TXF\_METADATA\_ALREADY\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-547">6835 (0x1AB3)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-547">6835 (0x1AB3)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-548">Los metadatos de transacción ya están presentes en este archivo y no se pueden reemplazar.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-548">Transaction metadata is already present on this file and cannot be superseded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-549"><span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**ERROR \_ de \_ devoluciones de llamada de ámbito de transacción \_ \_ no \_ establecida**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-549"><span id="ERROR_TRANSACTION_SCOPE_CALLBACKS_NOT_SET"></span><span id="error_transaction_scope_callbacks_not_set"></span>**ERROR\_TRANSACTION\_SCOPE\_CALLBACKS\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-550">6836 (0x1AB4)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-550">6836 (0x1AB4)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-551">No se pudo especificar un ámbito de transacción porque el controlador de ámbito no se ha inicializado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-551">A transaction scope could not be entered because the scope handler has not been initialized.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-552"><span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**promoción de la transacción de ERROR \_ \_ necesaria \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-552"><span id="ERROR_TRANSACTION_REQUIRED_PROMOTION"></span><span id="error_transaction_required_promotion"></span>**ERROR\_TRANSACTION\_REQUIRED\_PROMOTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-553">6837 (0x1AB5)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-553">6837 (0x1AB5)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-554">La promoción era necesaria para permitir que el administrador de recursos se inscriba, pero la transacción se configuró para no permitirla.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-554">Promotion was required in order to allow the resource manager to enlist, but the transaction was set to disallow it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-555"><span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERROR: \_ no se puede \_ ejecutar el \_ archivo en la \_ \_ transacción**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-555"><span id="ERROR_CANNOT_EXECUTE_FILE_IN_TRANSACTION"></span><span id="error_cannot_execute_file_in_transaction"></span>**ERROR\_CANNOT\_EXECUTE\_FILE\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-556">6838 (0x1AB6)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-556">6838 (0x1AB6)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-557">Este archivo está abierto para su modificación en una transacción no resuelta y solo se puede abrir para ejecutarlo un lector de transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-557">This file is open for modification in an unresolved transaction and may be opened for execute only by a transacted reader.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-558"><span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**transacciones de ERROR \_ \_ no \_ inmovilizadas**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-558"><span id="ERROR_TRANSACTIONS_NOT_FROZEN"></span><span id="error_transactions_not_frozen"></span>**ERROR\_TRANSACTIONS\_NOT\_FROZEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-559">6839 (0x1AB7)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-559">6839 (0x1AB7)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-560">Se omitió la solicitud para reanudar las transacciones inmovilizadas porque las transacciones no se han inmovilizado previamente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-560">The request to thaw frozen transactions was ignored because transactions had not previously been frozen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-561"><span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**ERROR \_ \_ en la inmovilización \_ de transacciones en \_ curso**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-561"><span id="ERROR_TRANSACTION_FREEZE_IN_PROGRESS"></span><span id="error_transaction_freeze_in_progress"></span>**ERROR\_TRANSACTION\_FREEZE\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-562">6840 (0x1AB8)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-562">6840 (0x1AB8)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-563">No se pueden inmovilizar las transacciones porque ya hay una inmovilización en curso.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-563">Transactions cannot be frozen because a freeze is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-564"><span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERROR \_ : \_ volumen de instantánea \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-564"><span id="ERROR_NOT_SNAPSHOT_VOLUME"></span><span id="error_not_snapshot_volume"></span>**ERROR\_NOT\_SNAPSHOT\_VOLUME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-565">6841 (0x1AB9)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-565">6841 (0x1AB9)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-566">El volumen de destino no es un volumen de instantánea.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-566">The target volume is not a snapshot volume.</span></span> <span data-ttu-id="b7eb9-567">Esta operación solo es válida en un volumen montado como una instantánea.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-567">This operation is only valid on a volume mounted as a snapshot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-568"><span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERROR: \_ no hay ningún \_ punto \_ de retorno con \_ \_ archivos abiertos**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-568"><span id="ERROR_NO_SAVEPOINT_WITH_OPEN_FILES"></span><span id="error_no_savepoint_with_open_files"></span>**ERROR\_NO\_SAVEPOINT\_WITH\_OPEN\_FILES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-569">6842 (0x1ABA)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-569">6842 (0x1ABA)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-570">No se pudo realizar la operación de punto de retorno porque los archivos están abiertos en la transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-570">The savepoint operation failed because files are open on the transaction.</span></span> <span data-ttu-id="b7eb9-571">Esto no se permite.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-571">This is not permitted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-572"><span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**reparación de errores de \_ datos \_ perdidos \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-572"><span id="ERROR_DATA_LOST_REPAIR"></span><span id="error_data_lost_repair"></span>**ERROR\_DATA\_LOST\_REPAIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-573">6843 (0x1ABB)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-573">6843 (0x1ABB)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-574">Windows ha detectado daños en un archivo y ese archivo se ha reparado desde entonces.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-574">Windows has discovered corruption in a file, and that file has since been repaired.</span></span> <span data-ttu-id="b7eb9-575">Es posible que se haya producido una pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-575">Data loss may have occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-576"><span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERROR \_ disperso \_ no \_ permitido \_ en la \_ transacción**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-576"><span id="ERROR_SPARSE_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_sparse_not_allowed_in_transaction"></span>**ERROR\_SPARSE\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-577">6844 (0x1ABC)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-577">6844 (0x1ABC)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-578">No se pudo completar la operación dispersa porque hay una transacción activa en el archivo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-578">The sparse operation could not be completed because a transaction is active on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-579"><span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**ERROR \_ de \_ incoherencia de identidad de TM \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-579"><span id="ERROR_TM_IDENTITY_MISMATCH"></span><span id="error_tm_identity_mismatch"></span>**ERROR\_TM\_IDENTITY\_MISMATCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-580">6845 (0x1ABD)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-580">6845 (0x1ABD)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-581">Error en la llamada para crear un objeto TransactionManager porque la identidad de TM almacenada en el archivo de registro no coincide con la identidad de TM que se pasó como argumento.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-581">The call to create a TransactionManager object failed because the Tm Identity stored in the logfile does not match the Tm Identity that was passed in as an argument.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-582"><span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**ERROR de la \_ \_ sección flotante**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-582"><span id="ERROR_FLOATED_SECTION"></span><span id="error_floated_section"></span>**ERROR\_FLOATED\_SECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-583">6846 (0x1ABE)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-583">6846 (0x1ABE)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-584">Se intentó una operación de e/s en un objeto de sección que se ha flotado como resultado de la finalización de una transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-584">I/O was attempted on a section object that has been floated as a result of a transaction ending.</span></span> <span data-ttu-id="b7eb9-585">No hay datos válidos.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-585">There is no valid data.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-586"><span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**el ERROR \_ no puede \_ aceptar el \_ trabajo de transacción \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-586"><span id="ERROR_CANNOT_ACCEPT_TRANSACTED_WORK"></span><span id="error_cannot_accept_transacted_work"></span>**ERROR\_CANNOT\_ACCEPT\_TRANSACTED\_WORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-587">6847 (0x1ABF)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-587">6847 (0x1ABF)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-588">El administrador de recursos de transacciones no puede aceptar actualmente el trabajo de transacción debido a una condición transitoria como recursos insuficientes.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-588">The transactional resource manager cannot currently accept transacted work due to a transient condition such as low resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-589"><span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERROR \_ no se pueden \_ anular \_ las transacciones**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-589"><span id="ERROR_CANNOT_ABORT_TRANSACTIONS"></span><span id="error_cannot_abort_transactions"></span>**ERROR\_CANNOT\_ABORT\_TRANSACTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-590">6848 (0x1AC0)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-590">6848 (0x1AC0)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-591">El administrador de recursos transaccional tenía demasiados contabilizan pendientes que no se pudieron anular.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-591">The transactional resource manager had too many tranactions outstanding that could not be aborted.</span></span> <span data-ttu-id="b7eb9-592">Se ha cerrado el administrador de recursos transaccionales.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-592">The transactional resource manger has been shut down.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-593"><span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERROR \_ de \_ clústeres erróneos**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-593"><span id="ERROR_BAD_CLUSTERS"></span><span id="error_bad_clusters"></span>**ERROR\_BAD\_CLUSTERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-594">6849 (0x1AC1)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-594">6849 (0x1AC1)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-595">No se pudo completar la operación debido a clústeres defectuosos en el disco.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-595">The operation could not be completed due to bad clusters on disk.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-596"><span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**\_no se \_ permite la compresión de error en la \_ \_ \_ transacción**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-596"><span id="ERROR_COMPRESSION_NOT_ALLOWED_IN_TRANSACTION"></span><span id="error_compression_not_allowed_in_transaction"></span>**ERROR\_COMPRESSION\_NOT\_ALLOWED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-597">6850 (0x1AC2)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-597">6850 (0x1AC2)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-598">No se pudo completar la operación de compresión porque hay una transacción activa en el archivo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-598">The compression operation could not be completed because a transaction is active on the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-599"><span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**ERROR de \_ volumen \_ modificado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-599"><span id="ERROR_VOLUME_DIRTY"></span><span id="error_volume_dirty"></span>**ERROR\_VOLUME\_DIRTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-600">6851 (0x1AC3)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-600">6851 (0x1AC3)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-601">No se pudo completar la operación porque el volumen está sucio.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-601">The operation could not be completed because the volume is dirty.</span></span> <span data-ttu-id="b7eb9-602">Ejecute CHKDSK e inténtelo de nuevo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-602">Please run chkdsk and try again.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-603"><span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERROR: \_ no hay \_ \_ seguimiento \_ de vínculos en la \_ transacción**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-603"><span id="ERROR_NO_LINK_TRACKING_IN_TRANSACTION"></span><span id="error_no_link_tracking_in_transaction"></span>**ERROR\_NO\_LINK\_TRACKING\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-604">6852 (0x1AC4)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-604">6852 (0x1AC4)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-605">No se pudo completar la operación de seguimiento de vínculos porque una transacción está activa.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-605">The link tracking operation could not be completed because a transaction is active.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-606"><span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**\_no se \_ admite la operación de error en la \_ \_ \_ transacción**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-606"><span id="ERROR_OPERATION_NOT_SUPPORTED_IN_TRANSACTION"></span><span id="error_operation_not_supported_in_transaction"></span>**ERROR\_OPERATION\_NOT\_SUPPORTED\_IN\_TRANSACTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-607">6853 (0x1AC5)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-607">6853 (0x1AC5)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-608">Esta operación no se puede realizar en una transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-608">This operation cannot be performed in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-609"><span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**identificador de ERROR \_ expirado \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-609"><span id="ERROR_EXPIRED_HANDLE"></span><span id="error_expired_handle"></span>**ERROR\_EXPIRED\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-610">6854 (0x1AC6)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-610">6854 (0x1AC6)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-611">El identificador ya no está asociado correctamente a su transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-611">The handle is no longer properly associated with its transaction.</span></span> <span data-ttu-id="b7eb9-612">Es posible que se haya abierto en un administrador de recursos transaccional que se forzó posteriormente para reiniciarse.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-612">It may have been opened in a transactional resource manager that was subsequently forced to restart.</span></span> <span data-ttu-id="b7eb9-613">Cierre el identificador y abra uno nuevo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-613">Please close the handle and open a new one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-614"><span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**no se ha dado de \_ alta la transacción de error \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-614"><span id="ERROR_TRANSACTION_NOT_ENLISTED"></span><span id="error_transaction_not_enlisted"></span>**ERROR\_TRANSACTION\_NOT\_ENLISTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-615">6855 (0x1AC7)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-615">6855 (0x1AC7)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-616">No se pudo realizar la operación especificada porque el administrador de recursos no está dado de alta en la transacción.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-616">The specified operation could not be performed because the resource manager is not enlisted in the transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-617"><span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERROR \_ CTX en \_ el nombre de la estación de \_ nombres \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-617"><span id="ERROR_CTX_WINSTATION_NAME_INVALID"></span><span id="error_ctx_winstation_name_invalid"></span>**ERROR\_CTX\_WINSTATION\_NAME\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-618">7001 (0x1B59)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-618">7001 (0x1B59)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-619">El nombre de sesión especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-619">The specified session name is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-620"><span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERROR \_ CTX \_ no válido \_ PD**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-620"><span id="ERROR_CTX_INVALID_PD"></span><span id="error_ctx_invalid_pd"></span>**ERROR\_CTX\_INVALID\_PD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-621">7002 (0x1B5A)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-621">7002 (0x1B5A)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-622">El controlador de protocolo especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-622">The specified protocol driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-623"><span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERROR \_ CTX \_ PD \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-623"><span id="ERROR_CTX_PD_NOT_FOUND"></span><span id="error_ctx_pd_not_found"></span>**ERROR\_CTX\_PD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-624">7003 (0x1B5B)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-624">7003 (0x1B5B)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-625">No se encontró el controlador de protocolo especificado en la ruta de acceso del sistema.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-625">The specified protocol driver was not found in the system path.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-626"><span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERROR \_ CTX \_ WD \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-626"><span id="ERROR_CTX_WD_NOT_FOUND"></span><span id="error_ctx_wd_not_found"></span>**ERROR\_CTX\_WD\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-627">7004 (0x1B5C)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-627">7004 (0x1B5C)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-628">No se encontró el controlador de conexión de terminal especificado en la ruta de acceso del sistema.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-628">The specified terminal connection driver was not found in the system path.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-629"><span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERROR \_ CTX \_ no se puede \_ crear la entrada del registro de \_ eventos \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-629"><span id="ERROR_CTX_CANNOT_MAKE_EVENTLOG_ENTRY"></span><span id="error_ctx_cannot_make_eventlog_entry"></span>**ERROR\_CTX\_CANNOT\_MAKE\_EVENTLOG\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-630">7005 (0x1B5D)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-630">7005 (0x1B5D)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-631">No se pudo crear una clave del registro para el registro de eventos para esta sesión.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-631">A registry key for event logging could not be created for this session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-632"><span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERROR \_ CTX \_ \_ colisión de nombre de servicio \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-632"><span id="ERROR_CTX_SERVICE_NAME_COLLISION"></span><span id="error_ctx_service_name_collision"></span>**ERROR\_CTX\_SERVICE\_NAME\_COLLISION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-633">7006 (0x1B5E)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-633">7006 (0x1B5E)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-634">Ya existe un servicio con el mismo nombre en el sistema.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-634">A service with the same name already exists on the system.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-635"><span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERROR \_ CTX \_ cierre \_ pendiente**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-635"><span id="ERROR_CTX_CLOSE_PENDING"></span><span id="error_ctx_close_pending"></span>**ERROR\_CTX\_CLOSE\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-636">7007 (0x1B5F)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-636">7007 (0x1B5F)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-637">Hay una operación de cierre pendiente en la sesión.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-637">A close operation is pending on the session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-638"><span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERROR \_ CTX \_ no \_ OUTBUF**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-638"><span id="ERROR_CTX_NO_OUTBUF"></span><span id="error_ctx_no_outbuf"></span>**ERROR\_CTX\_NO\_OUTBUF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-639">7008 (0x1B60)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-639">7008 (0x1B60)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-640">No hay ningún búfer de salida disponible.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-640">There are no free output buffers available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-641"><span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERROR \_ CTX \_ modem \_ INF \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-641"><span id="ERROR_CTX_MODEM_INF_NOT_FOUND"></span><span id="error_ctx_modem_inf_not_found"></span>**ERROR\_CTX\_MODEM\_INF\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-642">7009 (0x1B61)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-642">7009 (0x1B61)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-643">El módem. No se encontró el archivo INF.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-643">The MODEM.INF file was not found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-644"><span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERROR \_ CTX \_ MODEMNAME no válido \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-644"><span id="ERROR_CTX_INVALID_MODEMNAME"></span><span id="error_ctx_invalid_modemname"></span>**ERROR\_CTX\_INVALID\_MODEMNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-645">7010 (0x1B62)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-645">7010 (0x1B62)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-646">No se encontró el nombre del módem en MODEM. INF.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-646">The modem name was not found in MODEM.INF.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-647"><span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**error \_ de \_ respuesta de módem CTX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-647"><span id="ERROR_CTX_MODEM_RESPONSE_ERROR"></span><span id="error_ctx_modem_response_error"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-648">7011 (0x1B63)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-648">7011 (0x1B63)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-649">El módem no aceptó el comando que se le ha enviado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-649">The modem did not accept the command sent to it.</span></span> <span data-ttu-id="b7eb9-650">Compruebe que el nombre del módem configurado coincide con el módem conectado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-650">Verify that the configured modem name matches the attached modem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-651"><span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERROR \_ CTX \_ \_ tiempo de espera de respuesta del módem \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-651"><span id="ERROR_CTX_MODEM_RESPONSE_TIMEOUT"></span><span id="error_ctx_modem_response_timeout"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-652">7012 (0x1B64)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-652">7012 (0x1B64)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-653">El módem no respondió al comando que se le ha enviado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-653">The modem did not respond to the command sent to it.</span></span> <span data-ttu-id="b7eb9-654">Compruebe que el módem está correctamente cableado y encendido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-654">Verify that the modem is properly cabled and powered on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-655"><span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERROR \_ CTX \_ respuesta de módem \_ \_ no \_ portadora**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-655"><span id="ERROR_CTX_MODEM_RESPONSE_NO_CARRIER"></span><span id="error_ctx_modem_response_no_carrier"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_NO\_CARRIER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-656">7013 (0x1B65)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-656">7013 (0x1B65)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-657">No se pudo detectar el operador o se quitó el operador debido a la desconexión.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-657">Carrier detect has failed or carrier has been dropped due to disconnect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-658"><span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERROR \_ CTX \_ respuesta de módem \_ \_ sin \_ ditono**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-658"><span id="ERROR_CTX_MODEM_RESPONSE_NO_DIALTONE"></span><span id="error_ctx_modem_response_no_dialtone"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_NO\_DIALTONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-659">7014 (0x1B66)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-659">7014 (0x1B66)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-660">No se detectó el tono de marcado en el tiempo requerido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-660">Dial tone not detected within the required time.</span></span> <span data-ttu-id="b7eb9-661">Compruebe que el cable telefónico está conectado correctamente y funciona.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-661">Verify that the phone cable is properly attached and functional.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-662"><span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERROR \_ de \_ respuesta de módem CTX \_ \_ ocupada**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-662"><span id="ERROR_CTX_MODEM_RESPONSE_BUSY"></span><span id="error_ctx_modem_response_busy"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-663">7015 (0x1B67)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-663">7015 (0x1B67)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-664">Señal de ocupado detectada en el sitio remoto en la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-664">Busy signal detected at remote site on callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-665"><span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERROR \_ CTX \_ \_ voz de respuesta de módem \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-665"><span id="ERROR_CTX_MODEM_RESPONSE_VOICE"></span><span id="error_ctx_modem_response_voice"></span>**ERROR\_CTX\_MODEM\_RESPONSE\_VOICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-666">7016 (0x1B68)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-666">7016 (0x1B68)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-667">Voz detectada en el sitio remoto en la devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-667">Voice detected at remote site on callback.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-668"><span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**error \_ CTX \_ TD \_ error**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-668"><span id="ERROR_CTX_TD_ERROR"></span><span id="error_ctx_td_error"></span>**ERROR\_CTX\_TD\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-669">7017 (0x1B69)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-669">7017 (0x1B69)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-670">Error del controlador de transporte.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-670">Transport driver error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-671"><span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERROR \_ CTX-en \_ \_ no \_ encontrado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-671"><span id="ERROR_CTX_WINSTATION_NOT_FOUND"></span><span id="error_ctx_winstation_not_found"></span>**ERROR\_CTX\_WINSTATION\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-672">7022 (0x1B6E)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-672">7022 (0x1B6E)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-673">No se encuentra la sesión especificada.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-673">The specified session cannot be found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-674"><span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**el ERROR CTX en la estación de mensaje \_ \_ \_ ya \_ existe**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-674"><span id="ERROR_CTX_WINSTATION_ALREADY_EXISTS"></span><span id="error_ctx_winstation_already_exists"></span>**ERROR\_CTX\_WINSTATION\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-675">7023 (0x1B6F)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-675">7023 (0x1B6F)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-676">El nombre de sesión especificado ya está en uso.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-676">The specified session name is already in use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-677"><span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERROR de \_ CTX en \_ \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-677"><span id="ERROR_CTX_WINSTATION_BUSY"></span><span id="error_ctx_winstation_busy"></span>**ERROR\_CTX\_WINSTATION\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-678">7024 (0x1B70)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-678">7024 (0x1B70)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-679">No se puede completar la tarea que está intentando realizar porque Servicios de Escritorio remoto está ocupado actualmente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-679">The task you are trying to do can't be completed because Remote Desktop Services is currently busy.</span></span> <span data-ttu-id="b7eb9-680">Inténtalo de nuevo al cabo de un rato.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-680">Please try again in a few minutes.</span></span> <span data-ttu-id="b7eb9-681">Otros usuarios todavía deben poder iniciar sesión.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-681">Other users should still be able to log on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-682"><span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERROR \_ CTX \_ \_ modo de vídeo incorrecto \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-682"><span id="ERROR_CTX_BAD_VIDEO_MODE"></span><span id="error_ctx_bad_video_mode"></span>**ERROR\_CTX\_BAD\_VIDEO\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-683">7025 (0x1B71)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-683">7025 (0x1B71)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-684">Se ha intentado conectar a una sesión cuyo modo de vídeo no es compatible con el cliente actual.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-684">An attempt has been made to connect to a session whose video mode is not supported by the current client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-685"><span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERROR \_ CTX \_ Graphics \_ no válida**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-685"><span id="ERROR_CTX_GRAPHICS_INVALID"></span><span id="error_ctx_graphics_invalid"></span>**ERROR\_CTX\_GRAPHICS\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-686">7035 (0x1B7B)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-686">7035 (0x1B7B)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-687">La aplicación intentó habilitar el modo de gráficos de DOS.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-687">The application attempted to enable DOS graphics mode.</span></span> <span data-ttu-id="b7eb9-688">No se admite el modo de gráficos de DOS.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-688">DOS graphics mode is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-689"><span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERROR \_ CTX \_ Inicio de sesión \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-689"><span id="ERROR_CTX_LOGON_DISABLED"></span><span id="error_ctx_logon_disabled"></span>**ERROR\_CTX\_LOGON\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-690">7037 (0x1B7D)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-690">7037 (0x1B7D)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-691">Se ha deshabilitado el privilegio de inicio de sesión interactivo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-691">Your interactive logon privilege has been disabled.</span></span> <span data-ttu-id="b7eb9-692">Póngase en contacto con el administrador.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-692">Please contact your administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-693"><span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERROR \_ CTX \_ no \_ Console**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-693"><span id="ERROR_CTX_NOT_CONSOLE"></span><span id="error_ctx_not_console"></span>**ERROR\_CTX\_NOT\_CONSOLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-694">7038 (0x1B7E)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-694">7038 (0x1B7E)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-695">La operación solicitada solo se puede realizar en la consola del sistema.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-695">The requested operation can be performed only on the system console.</span></span> <span data-ttu-id="b7eb9-696">Esto suele ser el resultado de un controlador o DLL del sistema que requiere acceso directo a la consola.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-696">This is most often the result of a driver or system DLL requiring direct console access.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-697"><span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERROR \_ de \_ tiempo de espera de consulta de cliente CTX \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-697"><span id="ERROR_CTX_CLIENT_QUERY_TIMEOUT"></span><span id="error_ctx_client_query_timeout"></span>**ERROR\_CTX\_CLIENT\_QUERY\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-698">7040 (0x1B80)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-698">7040 (0x1B80)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-699">El cliente no pudo responder al mensaje de conexión de servidor.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-699">The client failed to respond to the server connect message.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-700"><span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**ERROR \_ CTX \_ \_ desconexión de consola**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-700"><span id="ERROR_CTX_CONSOLE_DISCONNECT"></span><span id="error_ctx_console_disconnect"></span>**ERROR\_CTX\_CONSOLE\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-701">7041 (0x1B81)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-701">7041 (0x1B81)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-702">No se admite la desconexión de la sesión de consola.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-702">Disconnecting the console session is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-703"><span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERROR \_ CTX \_ Console \_ Connect**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-703"><span id="ERROR_CTX_CONSOLE_CONNECT"></span><span id="error_ctx_console_connect"></span>**ERROR\_CTX\_CONSOLE\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-704">7042 (0x1B82)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-704">7042 (0x1B82)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-705">No se puede volver a conectar una sesión desconectada a la consola.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-705">Reconnecting a disconnected session to the console is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-706"><span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERROR \_ CTX \_ sombra \_ denegada**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-706"><span id="ERROR_CTX_SHADOW_DENIED"></span><span id="error_ctx_shadow_denied"></span>**ERROR\_CTX\_SHADOW\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-707">7044 (0x1B84)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-707">7044 (0x1B84)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-708">Se denegó la solicitud para controlar otra sesión de forma remota.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-708">The request to control another session remotely was denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-709"><span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERROR \_ CTX en el \_ \_ acceso \_ denegado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-709"><span id="ERROR_CTX_WINSTATION_ACCESS_DENIED"></span><span id="error_ctx_winstation_access_denied"></span>**ERROR\_CTX\_WINSTATION\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-710">7045 (0x1B85)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-710">7045 (0x1B85)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-711">Se denegó el acceso a la sesión solicitado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-711">The requested session access is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-712"><span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERROR \_ CTX \_ no válido \_ WD**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-712"><span id="ERROR_CTX_INVALID_WD"></span><span id="error_ctx_invalid_wd"></span>**ERROR\_CTX\_INVALID\_WD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-713">7049 (0x1B89)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-713">7049 (0x1B89)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-714">El controlador de conexión de terminal especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-714">The specified terminal connection driver is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-715"><span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERROR \_ CTX \_ Shadow \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-715"><span id="ERROR_CTX_SHADOW_INVALID"></span><span id="error_ctx_shadow_invalid"></span>**ERROR\_CTX\_SHADOW\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-716">7050 (0x1B8A)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-716">7050 (0x1B8A)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-717">La sesión solicitada no se puede controlar de forma remota.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-717">The requested session cannot be controlled remotely.</span></span> <span data-ttu-id="b7eb9-718">Esto puede deberse a que la sesión está desconectada o no tiene un usuario que ha iniciado sesión actualmente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-718">This may be because the session is disconnected or does not currently have a user logged on.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-719"><span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERROR de la \_ \_ sombra CTX \_ deshabilitada**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-719"><span id="ERROR_CTX_SHADOW_DISABLED"></span><span id="error_ctx_shadow_disabled"></span>**ERROR\_CTX\_SHADOW\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-720">7051 (0x1B8B)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-720">7051 (0x1B8B)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-721">La sesión solicitada no está configurada para permitir el control remoto.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-721">The requested session is not configured to allow remote control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-722"><span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERROR \_ \_ \_ de licencia de cliente CTX \_ en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-722"><span id="ERROR_CTX_CLIENT_LICENSE_IN_USE"></span><span id="error_ctx_client_license_in_use"></span>**ERROR\_CTX\_CLIENT\_LICENSE\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-723">7052 (0x1B8C)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-723">7052 (0x1B8C)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-724">Se ha rechazado la solicitud de conexión a este Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-724">Your request to connect to this Terminal Server has been rejected.</span></span> <span data-ttu-id="b7eb9-725">Otro usuario está usando actualmente su Terminal Server número de licencia de cliente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-725">Your Terminal Server client license number is currently being used by another user.</span></span> <span data-ttu-id="b7eb9-726">Llame al administrador del sistema para obtener un número de licencia único.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-726">Please call your system administrator to obtain a unique license number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-727"><span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERROR de la \_ \_ licencia de cliente CTX \_ \_ no \_ establecida**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-727"><span id="ERROR_CTX_CLIENT_LICENSE_NOT_SET"></span><span id="error_ctx_client_license_not_set"></span>**ERROR\_CTX\_CLIENT\_LICENSE\_NOT\_SET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-728">7053 (0x1B8D)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-728">7053 (0x1B8D)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-729">Se ha rechazado la solicitud de conexión a este Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-729">Your request to connect to this Terminal Server has been rejected.</span></span> <span data-ttu-id="b7eb9-730">No se ha especificado el número de licencia de cliente de Terminal Server para esta copia del cliente de Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-730">Your Terminal Server client license number has not been entered for this copy of the Terminal Server client.</span></span> <span data-ttu-id="b7eb9-731">Póngase en contacto con el administrador del sistema.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-731">Please contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-732"><span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**ERROR \_ de \_ licencia de CTX \_ no \_ disponible**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-732"><span id="ERROR_CTX_LICENSE_NOT_AVAILABLE"></span><span id="error_ctx_license_not_available"></span>**ERROR\_CTX\_LICENSE\_NOT\_AVAILABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-733">7054 (0x1B8E)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-733">7054 (0x1B8E)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-734">El número de conexiones a este equipo es limitado y ahora todas las conexiones están en uso.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-734">The number of connections to this computer is limited and all connections are in use right now.</span></span> <span data-ttu-id="b7eb9-735">Intente conectarse más tarde o póngase en contacto con el administrador del sistema.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-735">Try connecting later or contact your system administrator.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-736"><span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERROR \_ de \_ cliente de licencia CTX \_ \_ no válido**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-736"><span id="ERROR_CTX_LICENSE_CLIENT_INVALID"></span><span id="error_ctx_license_client_invalid"></span>**ERROR\_CTX\_LICENSE\_CLIENT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-737">7055 (0x1B8F)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-737">7055 (0x1B8F)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-738">El cliente que está usando no tiene licencia para usar este sistema.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-738">The client you are using is not licensed to use this system.</span></span> <span data-ttu-id="b7eb9-739">Se denegó la solicitud de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-739">Your logon request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-740"><span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERROR \_ CTX \_ expiró la licencia \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-740"><span id="ERROR_CTX_LICENSE_EXPIRED"></span><span id="error_ctx_license_expired"></span>**ERROR\_CTX\_LICENSE\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-741">7056 (0x1B90)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-741">7056 (0x1B90)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-742">La licencia del sistema ha expirado.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-742">The system license has expired.</span></span> <span data-ttu-id="b7eb9-743">Se denegó la solicitud de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-743">Your logon request is denied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-744"><span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERROR de la \_ sombra de CTX \_ no en \_ \_ ejecución**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-744"><span id="ERROR_CTX_SHADOW_NOT_RUNNING"></span><span id="error_ctx_shadow_not_running"></span>**ERROR\_CTX\_SHADOW\_NOT\_RUNNING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-745">7057 (0x1B91)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-745">7057 (0x1B91)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-746">No se pudo terminar el control remoto porque la sesión especificada no se está controlando de forma remota.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-746">Remote control could not be terminated because the specified session is not currently being remotely controlled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-747"><span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**ERROR \_ \_ de la sombra \_ de CTX terminada \_ por el \_ modo \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-747"><span id="ERROR_CTX_SHADOW_ENDED_BY_MODE_CHANGE"></span><span id="error_ctx_shadow_ended_by_mode_change"></span>**ERROR\_CTX\_SHADOW\_ENDED\_BY\_MODE\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-748">7058 (0x1B92)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-748">7058 (0x1B92)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-749">El control remoto de la consola ha finalizado porque se ha cambiado el modo de presentación.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-749">The remote control of the console was terminated because the display mode was changed.</span></span> <span data-ttu-id="b7eb9-750">No se admite el cambio del modo de presentación en una sesión de control remoto.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-750">Changing the display mode in a remote control session is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-751"><span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**recuento de \_ activaciones de errores \_ \_ superado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-751"><span id="ERROR_ACTIVATION_COUNT_EXCEEDED"></span><span id="error_activation_count_exceeded"></span>**ERROR\_ACTIVATION\_COUNT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-752">7059 (0x1B93)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-752">7059 (0x1B93)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-753">La activación ya se ha restablecido el número máximo de veces para esta instalación.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-753">Activation has already been reset the maximum number of times for this installation.</span></span> <span data-ttu-id="b7eb9-754">El temporizador de activación no se borrará.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-754">Your activation timer will not be cleared.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-755"><span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERROR \_ CTX \_ WINSTATIONS \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-755"><span id="ERROR_CTX_WINSTATIONS_DISABLED"></span><span id="error_ctx_winstations_disabled"></span>**ERROR\_CTX\_WINSTATIONS\_DISABLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-756">7060 (0x1B94)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-756">7060 (0x1B94)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-757">Los inicios de sesión remotos están deshabilitados actualmente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-757">Remote logins are currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-758"><span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERROR \_ de \_ nivel de cifrado CTX \_ \_ requerido**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-758"><span id="ERROR_CTX_ENCRYPTION_LEVEL_REQUIRED"></span><span id="error_ctx_encryption_level_required"></span>**ERROR\_CTX\_ENCRYPTION\_LEVEL\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-759">7061 (0x1B95)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-759">7061 (0x1B95)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-760">No tiene el nivel de cifrado adecuado para obtener acceso a esta sesión.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-760">You do not have the proper encryption level to access this Session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-761"><span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERROR \_ \_ de sesión CTX \_ en \_ uso**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-761"><span id="ERROR_CTX_SESSION_IN_USE"></span><span id="error_ctx_session_in_use"></span>**ERROR\_CTX\_SESSION\_IN\_USE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-762">7062 (0x1B96)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-762">7062 (0x1B96)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-763">El usuario% s \\ \\ % s ha iniciado sesión en este equipo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-763">The user %s\\\\%s is currently logged on to this computer.</span></span> <span data-ttu-id="b7eb9-764">Solo el usuario actual o un administrador pueden iniciar sesión en este equipo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-764">Only the current user or an administrator can log on to this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-765"><span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERROR \_ CTX \_ no \_ forzar \_ cierre de sesión**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-765"><span id="ERROR_CTX_NO_FORCE_LOGOFF"></span><span id="error_ctx_no_force_logoff"></span>**ERROR\_CTX\_NO\_FORCE\_LOGOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-766">7063 (0x1B97)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-766">7063 (0x1B97)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-767">El usuario% s \\ \\ % s ya ha iniciado sesión en la consola de este equipo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-767">The user %s\\\\%s is already logged on to the console of this computer.</span></span> <span data-ttu-id="b7eb9-768">No tiene permiso para iniciar sesión en este momento.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-768">You do not have permission to log in at this time.</span></span> <span data-ttu-id="b7eb9-769">Para resolver este problema, póngase en contacto con% s \\ \\ % s y pídale que cierre la sesión.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-769">To resolve this issue, contact %s\\\\%s and have them log off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-770"><span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERROR \_ de \_ restricción de cuenta de CTX \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-770"><span id="ERROR_CTX_ACCOUNT_RESTRICTION"></span><span id="error_ctx_account_restriction"></span>**ERROR\_CTX\_ACCOUNT\_RESTRICTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-771">7064 (0x1B98)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-771">7064 (0x1B98)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-772">No se puede iniciar la sesión debido a una restricción de cuenta.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-772">Unable to log you on because of an account restriction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-773"><span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**error \_ de \_ Protocolo RDP \_ error**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-773"><span id="ERROR_RDP_PROTOCOL_ERROR"></span><span id="error_rdp_protocol_error"></span>**ERROR\_RDP\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-774">7065 (0x1B99)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-774">7065 (0x1B99)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-775">El componente de protocolo RDP %2 detectó un error en el flujo de protocolo y ha desconectado el cliente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-775">The RDP protocol component %2 detected an error in the protocol stream and has disconnected the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-776"><span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERROR \_ CTX \_ CDM \_ Connect**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-776"><span id="ERROR_CTX_CDM_CONNECT"></span><span id="error_ctx_cdm_connect"></span>**ERROR\_CTX\_CDM\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-777">7066 (0x1B9A)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-777">7066 (0x1B9A)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-778">El servicio de asignación de unidad de cliente se ha conectado en la conexión de terminal.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-778">The Client Drive Mapping Service Has Connected on Terminal Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-779"><span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERROR \_ CTX \_ CDM \_ Disconnect**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-779"><span id="ERROR_CTX_CDM_DISCONNECT"></span><span id="error_ctx_cdm_disconnect"></span>**ERROR\_CTX\_CDM\_DISCONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-780">7067 (0x1B9B)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-780">7067 (0x1B9B)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-781">El servicio de asignación de unidad de cliente se ha desconectado en la conexión de terminal.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-781">The Client Drive Mapping Service Has Disconnected on Terminal Connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-782"><span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**error \_ CTX error de \_ nivel de seguridad \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-782"><span id="ERROR_CTX_SECURITY_LAYER_ERROR"></span><span id="error_ctx_security_layer_error"></span>**ERROR\_CTX\_SECURITY\_LAYER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-783">7068 (0x1B9C)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-783">7068 (0x1B9C)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-784">El nivel de seguridad de Terminal Server ha detectado un error en el flujo de protocolo y ha desconectado el cliente.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-784">The Terminal Server security layer detected an error in the protocol stream and has disconnected the client.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-785"><span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ERROR \_ de \_ sesiones incompatibles de TS \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-785"><span id="ERROR_TS_INCOMPATIBLE_SESSIONS"></span><span id="error_ts_incompatible_sessions"></span>**ERROR\_TS\_INCOMPATIBLE\_SESSIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-786">7069 (0x1B9D)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-786">7069 (0x1B9D)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-787">La sesión de destino no es compatible con la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-787">The target session is incompatible with the current session.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-788"><span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**error \_ de \_ subsistema de vídeo de TS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-788"><span id="ERROR_TS_VIDEO_SUBSYSTEM_ERROR"></span><span id="error_ts_video_subsystem_error"></span>**ERROR\_TS\_VIDEO\_SUBSYSTEM\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-789">7070 (0x1B9E)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-789">7070 (0x1B9E)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-790">Windows no se puede conectar a la sesión porque se produjo un problema en el subsistema de vídeo de Windows.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-790">Windows can't connect to your session because a problem occurred in the Windows video subsystem.</span></span> <span data-ttu-id="b7eb9-791">Intente conectarse de nuevo más tarde o póngase en contacto con el administrador del servidor para obtener ayuda.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-791">Try connecting again later, or contact the server administrator for assistance.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-792"><span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**\_secuencia de \_ API no válida de FRS Err \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-792"><span id="FRS_ERR_INVALID_API_SEQUENCE"></span><span id="frs_err_invalid_api_sequence"></span>**FRS\_ERR\_INVALID\_API\_SEQUENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-793">8001 (0x1F41)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-793">8001 (0x1F41)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-794">Se llamó incorrectamente a la API del servicio de replicación de archivos.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-794">The file replication service API was called incorrectly.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-795"><span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**servicio de inicio de FRS \_ Err \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-795"><span id="FRS_ERR_STARTING_SERVICE"></span><span id="frs_err_starting_service"></span>**FRS\_ERR\_STARTING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-796">8002 (0x1F42)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-796">8002 (0x1F42)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-797">No se puede iniciar el servicio de replicación de archivos.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-797">The file replication service cannot be started.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-798"><span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**error de FRS al \_ \_ detener el \_ servicio**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-798"><span id="FRS_ERR_STOPPING_SERVICE"></span><span id="frs_err_stopping_service"></span>**FRS\_ERR\_STOPPING\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-799">8003 (0x1F43)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-799">8003 (0x1F43)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-800">No se puede detener el servicio de replicación de archivos.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-800">The file replication service cannot be stopped.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-801"><span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**\_ \_ API interna de error de FRS \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-801"><span id="FRS_ERR_INTERNAL_API"></span><span id="frs_err_internal_api"></span>**FRS\_ERR\_INTERNAL\_API**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-802">8004 (0x1F44)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-802">8004 (0x1F44)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-803">La API del servicio de replicación de archivos finalizó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-803">The file replication service API terminated the request.</span></span> <span data-ttu-id="b7eb9-804">Es posible que el registro de eventos tenga más información.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-804">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-805"><span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**error de FRS \_ \_ interno**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-805"><span id="FRS_ERR_INTERNAL"></span><span id="frs_err_internal"></span>**FRS\_ERR\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-806">8005 (0x1F45)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-806">8005 (0x1F45)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-807">El servicio de replicación de archivos finalizó la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-807">The file replication service terminated the request.</span></span> <span data-ttu-id="b7eb9-808">Es posible que el registro de eventos tenga más información.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-808">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-809"><span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**servicio de error de FRS \_ \_ \_ COMM**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-809"><span id="FRS_ERR_SERVICE_COMM"></span><span id="frs_err_service_comm"></span>**FRS\_ERR\_SERVICE\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-810">8006 (0x1F46)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-810">8006 (0x1F46)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-811">No se puede establecer contacto con el servicio de replicación de archivos.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-811">The file replication service cannot be contacted.</span></span> <span data-ttu-id="b7eb9-812">Es posible que el registro de eventos tenga más información.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-812">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-813"><span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS \_ Err \_ insuficiente \_ priv**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-813"><span id="FRS_ERR_INSUFFICIENT_PRIV"></span><span id="frs_err_insufficient_priv"></span>**FRS\_ERR\_INSUFFICIENT\_PRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-814">8007 (0x1F47)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-814">8007 (0x1F47)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-815">El servicio de replicación de archivos no puede satisfacer la solicitud porque el usuario no tiene privilegios suficientes.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-815">The file replication service cannot satisfy the request because the user has insufficient privileges.</span></span> <span data-ttu-id="b7eb9-816">Es posible que el registro de eventos tenga más información.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-816">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-817"><span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**autenticación de FRS \_ Err \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-817"><span id="FRS_ERR_AUTHENTICATION"></span><span id="frs_err_authentication"></span>**FRS\_ERR\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-818">8008 (0x1F48)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-818">8008 (0x1F48)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-819">El servicio de replicación de archivos no puede satisfacer la solicitud porque la RPC autenticada no está disponible.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-819">The file replication service cannot satisfy the request because authenticated RPC is not available.</span></span> <span data-ttu-id="b7eb9-820">Es posible que el registro de eventos tenga más información.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-820">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-821"><span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS \_ Err \_ Parent \_ insuficiente \_ priv**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-821"><span id="FRS_ERR_PARENT_INSUFFICIENT_PRIV"></span><span id="frs_err_parent_insufficient_priv"></span>**FRS\_ERR\_PARENT\_INSUFFICIENT\_PRIV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-822">8009 (0x1F49)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-822">8009 (0x1F49)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-823">El servicio de replicación de archivos no puede satisfacer la solicitud porque el usuario no tiene privilegios suficientes en el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-823">The file replication service cannot satisfy the request because the user has insufficient privileges on the domain controller.</span></span> <span data-ttu-id="b7eb9-824">Es posible que el registro de eventos tenga más información.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-824">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-825"><span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**\_ \_ autenticación principal FRS \_ Err**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-825"><span id="FRS_ERR_PARENT_AUTHENTICATION"></span><span id="frs_err_parent_authentication"></span>**FRS\_ERR\_PARENT\_AUTHENTICATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-826">8010 (0x1F4A)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-826">8010 (0x1F4A)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-827">El servicio de replicación de archivos no puede satisfacer la solicitud porque la RPC autenticada no está disponible en el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-827">The file replication service cannot satisfy the request because authenticated RPC is not available on the domain controller.</span></span> <span data-ttu-id="b7eb9-828">Es posible que el registro de eventos tenga más información.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-828">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-829"><span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS \_ Err \_ secundario \_ a \_ elemento primario \_ COMM**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-829"><span id="FRS_ERR_CHILD_TO_PARENT_COMM"></span><span id="frs_err_child_to_parent_comm"></span>**FRS\_ERR\_CHILD\_TO\_PARENT\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-830">8011 (0x1F4B)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-830">8011 (0x1F4B)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-831">El servicio de replicación de archivos no se puede comunicar con el servicio de replicación de archivos en el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-831">The file replication service cannot communicate with the file replication service on the domain controller.</span></span> <span data-ttu-id="b7eb9-832">Es posible que el registro de eventos tenga más información.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-832">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-833"><span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**\_COMM ERR \_ Parent \_ to \_ Child \_ COMM**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-833"><span id="FRS_ERR_PARENT_TO_CHILD_COMM"></span><span id="frs_err_parent_to_child_comm"></span>**FRS\_ERR\_PARENT\_TO\_CHILD\_COMM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-834">8012 (0x1F4C)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-834">8012 (0x1F4C)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-835">El servicio de replicación de archivos del controlador de dominio no se puede comunicar con el servicio de replicación de archivos de este equipo.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-835">The file replication service on the domain controller cannot communicate with the file replication service on this computer.</span></span> <span data-ttu-id="b7eb9-836">Es posible que el registro de eventos tenga más información.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-836">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-837"><span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS \_ Err Err \_ SYSVOL \_ rellenar**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-837"><span id="FRS_ERR_SYSVOL_POPULATE"></span><span id="frs_err_sysvol_populate"></span>**FRS\_ERR\_SYSVOL\_POPULATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-838">8013 (0x1F4D)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-838">8013 (0x1F4D)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-839">El servicio de replicación de archivos no puede rellenar el volumen del sistema debido a un error interno.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-839">The file replication service cannot populate the system volume because of an internal error.</span></span> <span data-ttu-id="b7eb9-840">Es posible que el registro de eventos tenga más información.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-840">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-841"><span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**FRS \_ Err error de \_ llenado de SYSVOL \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-841"><span id="FRS_ERR_SYSVOL_POPULATE_TIMEOUT"></span><span id="frs_err_sysvol_populate_timeout"></span>**FRS\_ERR\_SYSVOL\_POPULATE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-842">8014 (0x1F4E)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-842">8014 (0x1F4E)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-843">El servicio de replicación de archivos no puede rellenar el volumen del sistema debido a un tiempo de espera interno.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-843">The file replication service cannot populate the system volume because of an internal timeout.</span></span> <span data-ttu-id="b7eb9-844">Es posible que el registro de eventos tenga más información.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-844">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-845"><span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS \_ Err error de \_ SYSVOL \_ está \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-845"><span id="FRS_ERR_SYSVOL_IS_BUSY"></span><span id="frs_err_sysvol_is_busy"></span>**FRS\_ERR\_SYSVOL\_IS\_BUSY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-846">8015 (0x1F4F)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-846">8015 (0x1F4F)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-847">El servicio de replicación de archivos no puede procesar la solicitud.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-847">The file replication service cannot process the request.</span></span> <span data-ttu-id="b7eb9-848">El volumen del sistema está ocupado con una solicitud anterior.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-848">The system volume is busy with a previous request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-849"><span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS \_ Err error de la \_ \_ degradación**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-849"><span id="FRS_ERR_SYSVOL_DEMOTE"></span><span id="frs_err_sysvol_demote"></span>**FRS\_ERR\_SYSVOL\_DEMOTE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-850">8016 (0x1F50)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-850">8016 (0x1F50)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-851">El servicio de replicación de archivos no puede detener la replicación del volumen del sistema debido a un error interno.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-851">The file replication service cannot stop replicating the system volume because of an internal error.</span></span> <span data-ttu-id="b7eb9-852">Es posible que el registro de eventos tenga más información.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-852">The event log may have more information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b7eb9-853"><span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**\_parámetro de \_ servicio no válido de FRS Err \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b7eb9-853"><span id="FRS_ERR_INVALID_SERVICE_PARAMETER"></span><span id="frs_err_invalid_service_parameter"></span>**FRS\_ERR\_INVALID\_SERVICE\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7eb9-854">8017 (0x1F51)</span><span class="sxs-lookup"><span data-stu-id="b7eb9-854">8017 (0x1F51)</span></span>
</dt> <dt>



<span data-ttu-id="b7eb9-855">El servicio de replicación de archivos ha detectado un parámetro no válido.</span><span class="sxs-lookup"><span data-stu-id="b7eb9-855">The file replication service detected an invalid parameter.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7eb9-856">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7eb9-856">Requirements</span></span>



| <span data-ttu-id="b7eb9-857">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7eb9-857">Requirement</span></span> | <span data-ttu-id="b7eb9-858">Value</span><span class="sxs-lookup"><span data-stu-id="b7eb9-858">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7eb9-859">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7eb9-859">Minimum supported client</span></span><br/> | <span data-ttu-id="b7eb9-860">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b7eb9-860">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b7eb9-861">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7eb9-861">Minimum supported server</span></span><br/> | <span data-ttu-id="b7eb9-862">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b7eb9-862">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7eb9-863">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b7eb9-863">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7eb9-864"><dt>WinError. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7eb9-864"><dt>WinError.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7eb9-865">Vea también</span><span class="sxs-lookup"><span data-stu-id="b7eb9-865">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7eb9-866">Códigos de error del sistema</span><span class="sxs-lookup"><span data-stu-id="b7eb9-866">System Error Codes</span></span>](system-error-codes.md)
</dt> </dl>

 

 




