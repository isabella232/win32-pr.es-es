---
description: La API de protección de datos de CNG usa las siguientes constantes.
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: Constantes DPAPI de CNG (NCryptprotect. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece376a0b7282f26ef933b249a1356b2d012d438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496972"
---
# <a name="cng-dpapi-constants"></a><span data-ttu-id="d6c71-103">Constantes DPAPI de CNG</span><span class="sxs-lookup"><span data-stu-id="d6c71-103">CNG DPAPI Constants</span></span>

<span data-ttu-id="d6c71-104">La API de protección de datos de CNG usa las siguientes constantes.</span><span class="sxs-lookup"><span data-stu-id="d6c71-104">The following constants are used by the CNG Data Protection API.</span></span>

<dl> <dt>

<span data-ttu-id="d6c71-105"><span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**\_ \_ delimitador \_ de descripción de NCRYPT y**</span><span class="sxs-lookup"><span data-stu-id="d6c71-105"><span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**NCRYPT\_DESCR\_DELIMITER\_AND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6c71-106">L "Y"</span><span class="sxs-lookup"><span data-stu-id="d6c71-106">L" AND "</span></span>
</dt> <dt>



<span data-ttu-id="d6c71-107">Se puede usar para probar una cadena de descriptor de protección para un delimitador y.</span><span class="sxs-lookup"><span data-stu-id="d6c71-107">Can be used to test a protection descriptor string for an AND delimiter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c71-108"><span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**valor de descripción de NCRYPT \_ \_ igual**</span><span class="sxs-lookup"><span data-stu-id="d6c71-108"><span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**NCRYPT\_DESCR\_EQUAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6c71-109">L "="</span><span class="sxs-lookup"><span data-stu-id="d6c71-109">L"="</span></span>
</dt> <dt>



<span data-ttu-id="d6c71-110">Se puede usar para probar una cadena de descriptor de protección para un signo igual.</span><span class="sxs-lookup"><span data-stu-id="d6c71-110">Can be used to test a protection descriptor string for an equals sign.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c71-111"><span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**\_ \_ delimitador \_ de descripción de NCRYPT o**</span><span class="sxs-lookup"><span data-stu-id="d6c71-111"><span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**NCRYPT\_DESCR\_DELIMITER\_OR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6c71-112">L "O"</span><span class="sxs-lookup"><span data-stu-id="d6c71-112">L" OR "</span></span>
</dt> <dt>



<span data-ttu-id="d6c71-113">Se puede usar para probar una cadena de descriptor de protección para un delimitador o.</span><span class="sxs-lookup"><span data-stu-id="d6c71-113">Can be used to test a protection descriptor string for an OR delimiter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c71-114"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**\_algoritmo de protección de claves NCRYPT \_ \_ \_ local**</span><span class="sxs-lookup"><span data-stu-id="d6c71-114"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_LOCAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6c71-115">"LOCAL"</span><span class="sxs-lookup"><span data-stu-id="d6c71-115">"LOCAL"</span></span>
</dt> <dt>



<span data-ttu-id="d6c71-116">El descriptor de protección LOCAL protege el contenido en la sesión de inicio de sesión, el usuario actual o el equipo local, tal y como se identifica en las siguientes constantes:</span><span class="sxs-lookup"><span data-stu-id="d6c71-116">The LOCAL protection descriptor protects content to the logon session, the current user, or the local machine as identified by the following constants:</span></span>

-   <span data-ttu-id="d6c71-117">**\_configuración de \_ Inicio \_ de \_ sesión local de la protección de claves NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="d6c71-117">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_LOGON**</span></span>
-   <span data-ttu-id="d6c71-118">**\_ \_ usuario local de protección de claves NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6c71-118">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_USER**</span></span>
-   <span data-ttu-id="d6c71-119">**\_ \_ máquina local de protección de claves NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6c71-119">**NCRYPT\_KEY\_PROTECTION\_LOCAL\_MACHINE**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c71-120"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**algoritmo de protección de claves de NCRYPT \_ \_ \_ \_ SDDL**</span><span class="sxs-lookup"><span data-stu-id="d6c71-120"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SDDL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6c71-121">SDDL</span><span class="sxs-lookup"><span data-stu-id="d6c71-121">"SDDL"</span></span>
</dt> <dt>



<span data-ttu-id="d6c71-122">Protege el contenido en una cadena SDDL (lenguaje de definición de descriptores de seguridad) que contiene información del descriptor de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d6c71-122">Protects content to an SDDL (Security Descriptor Definition Language) string that contains security descriptor information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c71-123"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**\_SID del \_ algoritmo de protección de claves NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6c71-123"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6c71-124">Junction</span><span class="sxs-lookup"><span data-stu-id="d6c71-124">"SID"</span></span>
</dt> <dt>



<span data-ttu-id="d6c71-125">El descriptor de protección de SID contiene un grupo o una identidad de entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="d6c71-125">The SID protection descriptor contains a group or principal identity.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c71-126"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**\_claves de \_ algoritmo de protección de claves NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6c71-126"><span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_WEBCREDENTIALS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6c71-127">"CREDENCIALes"</span><span class="sxs-lookup"><span data-stu-id="d6c71-127">"WEBCREDENTIALS"</span></span>
</dt> <dt>



<span data-ttu-id="d6c71-128">Protege a las credenciales de la cuenta Web de un usuario.</span><span class="sxs-lookup"><span data-stu-id="d6c71-128">Protects to a user's web account credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c71-129"><span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**\_configuración de \_ Inicio \_ de \_ sesión local de la protección de claves NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="d6c71-129"><span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_LOGON**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6c71-130">expire</span><span class="sxs-lookup"><span data-stu-id="d6c71-130">"logon"</span></span>
</dt> <dt>



<span data-ttu-id="d6c71-131">Protege el contenido de la sesión de inicio de sesión actual.</span><span class="sxs-lookup"><span data-stu-id="d6c71-131">Protects content to the current logon session.</span></span> <span data-ttu-id="d6c71-132">Los usuarios no podrán descifrar el contenido protegido después de cerrar la sesión o reiniciar.</span><span class="sxs-lookup"><span data-stu-id="d6c71-132">Users will not be able to decrypt the protected content after logoff or reboot.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c71-133"><span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**\_ \_ máquina local de protección de claves NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6c71-133"><span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_MACHINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6c71-134">sistema</span><span class="sxs-lookup"><span data-stu-id="d6c71-134">"machine"</span></span>
</dt> <dt>



<span data-ttu-id="d6c71-135">Protege el contenido en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="d6c71-135">Protects content to the local computer.</span></span> <span data-ttu-id="d6c71-136">Todos los usuarios del equipo local pueden descifrar el contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="d6c71-136">All users on the local computer can decrypt the protected content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c71-137"><span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**\_ \_ usuario local de protección de claves NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6c71-137"><span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**NCRYPT\_KEY\_PROTECTION\_LOCAL\_USER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6c71-138">usuario</span><span class="sxs-lookup"><span data-stu-id="d6c71-138">"user"</span></span>
</dt> <dt>



<span data-ttu-id="d6c71-139">Protege el contenido de la sesión de usuario actual.</span><span class="sxs-lookup"><span data-stu-id="d6c71-139">Protects content to the current user session.</span></span> <span data-ttu-id="d6c71-140">Solo este usuario en el equipo local podrá descifrar el contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="d6c71-140">Only this user on the local computer will be able to decrypt the protected content.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c71-141"><span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**\_proveedor de \_ protección de claves de MS \_**</span><span class="sxs-lookup"><span data-stu-id="d6c71-141"><span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**MS\_KEY\_PROTECTION\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6c71-142">"Proveedor de protección de claves de Microsoft"</span><span class="sxs-lookup"><span data-stu-id="d6c71-142">"Microsoft Key Protection Provider"</span></span>
</dt> <dt>



<span data-ttu-id="d6c71-143">Representa el proveedor de protección de claves de Microsoft, que admite formatos representados por las constantes siguientes:</span><span class="sxs-lookup"><span data-stu-id="d6c71-143">Represents the Microsoft key protection provider which supports formats represented by the following constants:</span></span>

-   <span data-ttu-id="d6c71-144">**\_SID del \_ algoritmo de protección de claves NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6c71-144">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SID**</span></span>
-   <span data-ttu-id="d6c71-145">**\_algoritmo de protección de claves NCRYPT \_ \_ \_ local**</span><span class="sxs-lookup"><span data-stu-id="d6c71-145">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_LOCAL**</span></span>
-   <span data-ttu-id="d6c71-146">**algoritmo de protección de claves de NCRYPT \_ \_ \_ \_ SDDL**</span><span class="sxs-lookup"><span data-stu-id="d6c71-146">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_SDDL**</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="d6c71-147"><span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**\_proveedor de \_ protección de claves de cliente de Windows \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6c71-147"><span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**WINDOWS\_CLIENT\_KEY\_PROTECTION\_PROVIDER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d6c71-148">"Proveedor de protección de claves de cliente de Windows"</span><span class="sxs-lookup"><span data-stu-id="d6c71-148">"Windows Client Key Protection Provider"</span></span>
</dt> <dt>



<span data-ttu-id="d6c71-149">Representa el proveedor de protección de claves de Microsoft que solo está disponible en el cliente y que admite formatos representados por las constantes siguientes:</span><span class="sxs-lookup"><span data-stu-id="d6c71-149">Represents the Microsoft key protection provider that is available only on the client and which supports formats represented by the following constants:</span></span>

-   <span data-ttu-id="d6c71-150">**\_claves de \_ algoritmo de protección de claves NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d6c71-150">**NCRYPT\_KEY\_PROTECTION\_ALGORITHM\_WEBCREDENTIALS**</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d6c71-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6c71-151">Requirements</span></span>



| <span data-ttu-id="d6c71-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6c71-152">Requirement</span></span> | <span data-ttu-id="d6c71-153">Value</span><span class="sxs-lookup"><span data-stu-id="d6c71-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6c71-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6c71-154">Minimum supported client</span></span><br/> | <span data-ttu-id="d6c71-155">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6c71-155">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d6c71-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d6c71-156">Minimum supported server</span></span><br/> | <span data-ttu-id="d6c71-157">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="d6c71-157">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d6c71-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d6c71-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6c71-159"><dt>NCryptprotect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6c71-159"><dt>NCryptprotect.h</dt></span></span> </dl> |



 

 




