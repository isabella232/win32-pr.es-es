---
description: Contiene definiciones de términos de seguridad que comienzan por la letra P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a
title: P (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd5b580295c35bc021ade53d3cb922ce8fe13d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911249"
---
# <a name="p-security-glossary"></a><span data-ttu-id="f7174-103">P (Glosario de seguridad)</span><span class="sxs-lookup"><span data-stu-id="f7174-103">P (Security Glossary)</span></span>

<span data-ttu-id="f7174-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [o](o-gly.md) p Q [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="f7174-104">[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) P Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="f7174-105"><span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**acolcha**</span><span class="sxs-lookup"><span data-stu-id="f7174-105"><span id="_security_padding_gly"></span><span id="_SECURITY_PADDING_GLY"></span>**padding**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-106">Cadena que se suele agregar cuando el último bloque de texto simple es corto.</span><span class="sxs-lookup"><span data-stu-id="f7174-106">A string, typically added when the last plaintext block is short.</span></span> <span data-ttu-id="f7174-107">Por ejemplo, si la longitud del bloque es de 64 bits y el último bloque contiene solo 40 bits, se deben agregar 24 bits de relleno al último bloque.</span><span class="sxs-lookup"><span data-stu-id="f7174-107">For example, if the block length is 64 bits and the last block contains only 40 bits, then 24 bits of padding must be added to the last block.</span></span> <span data-ttu-id="f7174-108">La cadena de relleno puede contener ceros, alternar ceros y otros, o algún otro patrón.</span><span class="sxs-lookup"><span data-stu-id="f7174-108">The padding string may contain zeros, alternating zeros and ones, or some other pattern.</span></span> <span data-ttu-id="f7174-109">Las aplicaciones que usan [*CryptoAPI*](c-gly.md) no necesitan agregar relleno a su texto no cifrado antes de que se cifren, ni tampoco deben quitarlo después del descifrado.</span><span class="sxs-lookup"><span data-stu-id="f7174-109">Applications that use [*CryptoAPI*](c-gly.md) need not add padding to their plaintext before it is encrypted, nor do they have to remove it after decrypting.</span></span> <span data-ttu-id="f7174-110">Esto se controla automáticamente.</span><span class="sxs-lookup"><span data-stu-id="f7174-110">This is all handled automatically.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-111"><span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**filtro de contraseñas**</span><span class="sxs-lookup"><span data-stu-id="f7174-111"><span id="_security_password_filter_gly"></span><span id="_SECURITY_PASSWORD_FILTER_GLY"></span>**password filter**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-112">Un archivo DLL que proporciona la aplicación de la Directiva de contraseñas y la notificación de cambios.</span><span class="sxs-lookup"><span data-stu-id="f7174-112">A DLL that provides password policy enforcement and change notification.</span></span> <span data-ttu-id="f7174-113">La [*autoridad de seguridad local*](l-gly.md)llama a las funciones implementadas por los filtros de contraseña.</span><span class="sxs-lookup"><span data-stu-id="f7174-113">The functions implemented by password filters are called by the [*Local Security Authority*](l-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7174-114"><span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**almacenamiento persistente**</span><span class="sxs-lookup"><span data-stu-id="f7174-114"><span id="_security_persistent_storage_gly"></span><span id="_SECURITY_PERSISTENT_STORAGE_GLY"></span>**persistent storage**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-115">Cualquier medio de almacenamiento que permanezca intacto cuando se desconecte la alimentación.</span><span class="sxs-lookup"><span data-stu-id="f7174-115">Any storage medium that remains intact when the power to it is disconnected.</span></span> <span data-ttu-id="f7174-116">Muchas bases de datos del [*almacén de certificados*](c-gly.md) son formas de almacenamiento persistente.</span><span class="sxs-lookup"><span data-stu-id="f7174-116">Many [*certificate store*](c-gly.md) databases are forms of persistent storage.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-117"><span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS**</span><span class="sxs-lookup"><span data-stu-id="f7174-117"><span id="_security_pkcs_gly"></span><span id="_SECURITY_PKCS_GLY"></span>**PKCS**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-118">Consulte *estándares de criptografía de clave pública*.</span><span class="sxs-lookup"><span data-stu-id="f7174-118">See *Public Key Cryptography Standards*.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-119"><span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \# 1**</span><span class="sxs-lookup"><span data-stu-id="f7174-119"><span id="_security_pkcs_1_standard_gly"></span><span id="_SECURITY_PKCS_1_STANDARD_GLY"></span>**PKCS \#1**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-120">Los estándares recomendados para la implementación de la criptografía de clave pública basada en el algoritmo de RSA, tal como se define en [RFC 3447](https://tools.ietf.org/html/rfc3447).</span><span class="sxs-lookup"><span data-stu-id="f7174-120">The recommended standards for the implementation of public-key cryptography based on the RSA algorithm as defined in [RFC 3447](https://tools.ietf.org/html/rfc3447).</span></span>

</dd> <dt>

<span data-ttu-id="f7174-121"><span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \# 12**</span><span class="sxs-lookup"><span data-stu-id="f7174-121"><span id="_security_pkcs_12_standard_gly"></span><span id="_SECURITY_PKCS_12_STANDARD_GLY"></span>**PKCS \#12**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-122">Estándar de sintaxis de intercambio de información personal, desarrollado y mantenido por RSA Data Security, Inc. Este estándar de sintaxis especifica un formato portátil para almacenar o transportar claves privadas, certificados y secretos distintos de un usuario.</span><span class="sxs-lookup"><span data-stu-id="f7174-122">The Personal Information Exchange Syntax Standard, developed and maintained by RSA Data Security, Inc. This syntax standard specifies a portable format for storing or transporting a user's private keys, certificates, and miscellaneous secrets.</span></span>

<span data-ttu-id="f7174-123">Vea también estándares de *criptografía de clave pública* y [*certificado*](c-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f7174-123">See also [*certificate*](c-gly.md) and *Public Key Cryptography Standards*.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-124"><span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**\#Datos firmados PKCS 7**</span><span class="sxs-lookup"><span data-stu-id="f7174-124"><span id="_security_pkcs_7_signed_data_gly"></span><span id="_SECURITY_PKCS_7_SIGNED_DATA_GLY"></span>**PKCS \#7 Signed Data**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-125">Un objeto de datos que se firma con el estándar de criptografía de clave pública \# 7 (PKCS \# 7) y que encapsula la información utilizada para firmar un archivo.</span><span class="sxs-lookup"><span data-stu-id="f7174-125">A data object that is signed with the Public Key Cryptography Standard \#7 (PKCS \#7) and that encapsulates the information used to sign a file.</span></span> <span data-ttu-id="f7174-126">Normalmente, incluye el certificado del firmante y el [*certificado raíz*](r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f7174-126">Typically, it includes the signer's certificate and the [*root certificate*](r-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7174-127"><span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \# 7**</span><span class="sxs-lookup"><span data-stu-id="f7174-127"><span id="_security_pkcs_7_standard_gly"></span><span id="_SECURITY_PKCS_7_STANDARD_GLY"></span>**PKCS \#7**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-128">Estándar de sintaxis de mensajes criptográficos.</span><span class="sxs-lookup"><span data-stu-id="f7174-128">The Cryptographic Message Syntax Standard.</span></span> <span data-ttu-id="f7174-129">Una sintaxis general para los datos a los que se puede aplicar la criptografía, como cifrado y firmas digitales.</span><span class="sxs-lookup"><span data-stu-id="f7174-129">A general syntax for data to which cryptography may be applied, such as digital signatures and encryption.</span></span> <span data-ttu-id="f7174-130">También proporciona una sintaxis para la diseminación de certificados o listas de revocación de certificados y otros atributos de mensajes, como las marcas de tiempo, al mensaje.</span><span class="sxs-lookup"><span data-stu-id="f7174-130">It also provides a syntax for disseminating certificates or certificate revocation lists and other message attributes, such as time stamps, to the message.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-131"><span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**CODIFICACIÓN de ASN de PKCS \_ 7 \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f7174-131"><span id="_security_pkcs_7_asn_encoding_gly"></span><span id="_SECURITY_PKCS_7_ASN_ENCODING_GLY"></span>**PKCS\_7\_ASN\_ENCODING**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-132">[*Tipo de codificación de mensajes*](m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f7174-132">A [*message encoding type*](m-gly.md).</span></span> <span data-ttu-id="f7174-133">Los tipos de codificación de mensajes se almacenan en la palabra de orden superior de un **DWORD** (el valor es: 0x00010000).</span><span class="sxs-lookup"><span data-stu-id="f7174-133">Message encoding types are stored in the high-order word of a **DWORD** (value is: 0x00010000).</span></span>

</dd> <dt>

<span data-ttu-id="f7174-134"><span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**texto**</span><span class="sxs-lookup"><span data-stu-id="f7174-134"><span id="_security_plaintext_gly"></span><span id="_SECURITY_PLAINTEXT_GLY"></span>**plaintext**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-135">Un mensaje no cifrado.</span><span class="sxs-lookup"><span data-stu-id="f7174-135">A message that is not encrypted.</span></span> <span data-ttu-id="f7174-136">Los mensajes de texto simple se conocen a veces como mensajes texto sin cifrar.</span><span class="sxs-lookup"><span data-stu-id="f7174-136">Plaintext messages are sometimes referred to as cleartext messages.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-137"><span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Imagen ejecutable portable (PE)**</span><span class="sxs-lookup"><span data-stu-id="f7174-137"><span id="_security_portable_executable_pe_image_gly"></span><span id="_SECURITY_PORTABLE_EXECUTABLE_PE_IMAGE_GLY"></span>**Portable Executable (PE) Image**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-138">Formato de archivo ejecutable de Windows estándar.</span><span class="sxs-lookup"><span data-stu-id="f7174-138">The standard Windows executable format.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-139"><span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**FICHERO**</span><span class="sxs-lookup"><span data-stu-id="f7174-139"><span id="_security_prf_gly"></span><span id="_SECURITY_PRF_GLY"></span>**PRF**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-140">Vea *función pseudoaleatorios*.</span><span class="sxs-lookup"><span data-stu-id="f7174-140">See *Pseudo-Random Function*.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-141"><span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**credenciales principales**</span><span class="sxs-lookup"><span data-stu-id="f7174-141"><span id="_security_primary_credentials_gly"></span><span id="_SECURITY_PRIMARY_CREDENTIALS_GLY"></span>**primary credentials**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-142">El \_ paquete de autenticación MsV1 0 define un valor de cadena de clave de credencial principal: la cadena de credenciales principal contiene las credenciales proporcionadas en la hora de inicio de sesión inicial.</span><span class="sxs-lookup"><span data-stu-id="f7174-142">The MsV1\_0 authentication package defines a primary credential key string value: The primary credentials string holds the credentials provided at initial logon time.</span></span> <span data-ttu-id="f7174-143">Incluye el nombre de usuario y las formas con distinción de mayúsculas y minúsculas y sin distinción de mayúsculas y minúsculas de la contraseña del usuario.</span><span class="sxs-lookup"><span data-stu-id="f7174-143">It includes the user name and both case-sensitive and case-insensitive forms of the user's password.</span></span>

<span data-ttu-id="f7174-144">Vea también [*credenciales adicionales*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f7174-144">See also [*supplemental credentials*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7174-145"><span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**proveedor de servicios principal**</span><span class="sxs-lookup"><span data-stu-id="f7174-145"><span id="_security_primary_service_provider_gly"></span><span id="_SECURITY_PRIMARY_SERVICE_PROVIDER_GLY"></span>**primary service provider**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-146">Proveedor de servicios que proporciona las interfaces de control a la tarjeta.</span><span class="sxs-lookup"><span data-stu-id="f7174-146">The service provider that supplies the control interfaces to the card.</span></span> <span data-ttu-id="f7174-147">Cada tarjeta inteligente puede registrar su proveedor de servicios principal en la base de datos de tarjetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="f7174-147">Each smart card can register its primary service provider in the smart card database.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-148"><span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**token principal**</span><span class="sxs-lookup"><span data-stu-id="f7174-148"><span id="_security_primary_token_gly"></span><span id="_SECURITY_PRIMARY_TOKEN_GLY"></span>**primary token**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-149">Un token de acceso que normalmente solo crea el kernel de Windows.</span><span class="sxs-lookup"><span data-stu-id="f7174-149">An access token that is typically created only by the Windows kernel.</span></span> <span data-ttu-id="f7174-150">Se puede asignar a un proceso para representar la información de seguridad predeterminada para ese proceso.</span><span class="sxs-lookup"><span data-stu-id="f7174-150">It may be assigned to a process to represent the default security information for that process.</span></span>

<span data-ttu-id="f7174-151">Vea también token de [*acceso*](a-gly.md) y [*token de suplantación*](i-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f7174-151">See also [*access token*](a-gly.md) and [*impersonation token*](i-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7174-152"><span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**entidad**</span><span class="sxs-lookup"><span data-stu-id="f7174-152"><span id="_security_principal_gly"></span><span id="_SECURITY_PRINCIPAL_GLY"></span>**principal**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-153">Consulte [*entidad de seguridad*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f7174-153">See [*security principal*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7174-154"><span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**Service**</span><span class="sxs-lookup"><span data-stu-id="f7174-154"><span id="_security_privacy_gly"></span><span id="_SECURITY_PRIVACY_GLY"></span>**privacy**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-155">Condición de estar aislada de la vista o el secreto.</span><span class="sxs-lookup"><span data-stu-id="f7174-155">The condition of being isolated from view or secret.</span></span> <span data-ttu-id="f7174-156">Con respecto a los mensajes, los mensajes privados son mensajes cifrados cuyo texto está oculto en la vista.</span><span class="sxs-lookup"><span data-stu-id="f7174-156">With respect to messages, private messages are encrypted messages whose text is hidden from view.</span></span> <span data-ttu-id="f7174-157">Con respecto a las claves, una clave privada es una clave secreta oculta de otras.</span><span class="sxs-lookup"><span data-stu-id="f7174-157">With respect to keys, a private key is a secret key concealed from others.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-158"><span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**clave privada**</span><span class="sxs-lookup"><span data-stu-id="f7174-158"><span id="_security_private_key_gly"></span><span id="_SECURITY_PRIVATE_KEY_GLY"></span>**private key**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-159">La mitad secreta de un par de claves usado en un algoritmo de clave pública.</span><span class="sxs-lookup"><span data-stu-id="f7174-159">The secret half of a key pair used in a public key algorithm.</span></span> <span data-ttu-id="f7174-160">Las claves privadas se utilizan normalmente para cifrar una clave de sesión simétrica, firmar digitalmente un mensaje o descifrar un mensaje cifrado con la clave pública correspondiente.</span><span class="sxs-lookup"><span data-stu-id="f7174-160">Private keys are typically used to encrypt a symmetric session key, digitally sign a message, or decrypt a message that has been encrypted with the corresponding public key.</span></span>

<span data-ttu-id="f7174-161">Vea también *clave pública*.</span><span class="sxs-lookup"><span data-stu-id="f7174-161">See also *public key*.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-162"><span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**BLOB de clave privada**</span><span class="sxs-lookup"><span data-stu-id="f7174-162"><span id="_security_private_key_blob_gly"></span><span id="_SECURITY_PRIVATE_KEY_BLOB_GLY"></span>**private key BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-163">Un BLOB de clave que contiene un par de claves pública y privada completo.</span><span class="sxs-lookup"><span data-stu-id="f7174-163">A key BLOB that contains a complete public/private key pair.</span></span> <span data-ttu-id="f7174-164">Los programas administrativos usan blobs de clave privada para transportar pares de claves.</span><span class="sxs-lookup"><span data-stu-id="f7174-164">Private key BLOBs are used by administrative programs to transport key pairs.</span></span> <span data-ttu-id="f7174-165">Como la parte de la clave privada del par de claves es extremadamente confidencial, estos blobs se suelen mantener cifrados con un cifrado simétrico.</span><span class="sxs-lookup"><span data-stu-id="f7174-165">As the private key portion of the key pair is extremely confidential, these BLOBs are typically kept encrypted with a symmetric cipher.</span></span> <span data-ttu-id="f7174-166">Estos blobs de clave también pueden usarse en aplicaciones avanzadas en las que los pares de claves se almacenan dentro de la aplicación, en lugar de depender del mecanismo de almacenamiento del CSP.</span><span class="sxs-lookup"><span data-stu-id="f7174-166">These key BLOBs can also be used by advanced applications where the key pairs are stored within the application, rather than relying on the CSP's storage mechanism.</span></span> <span data-ttu-id="f7174-167">Un BLOB de clave se crea mediante una llamada a la función **CryptExportKey** .</span><span class="sxs-lookup"><span data-stu-id="f7174-167">A key BLOB is created by calling the **CryptExportKey** function.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-168"><span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**privilegia**</span><span class="sxs-lookup"><span data-stu-id="f7174-168"><span id="_security_privilege_gly"></span><span id="_SECURITY_PRIVILEGE_GLY"></span>**privilege**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-169">El derecho de un usuario para realizar varias operaciones relacionadas con el sistema, como apagar el sistema, cargar los controles de dispositivos o cambiar la hora del sistema.</span><span class="sxs-lookup"><span data-stu-id="f7174-169">The right of a user to perform various system-related operations, such as shutting down the system, loading device drivers, or changing the system time.</span></span> <span data-ttu-id="f7174-170">El token de acceso de un usuario contiene una lista de los privilegios que mantiene el usuario o los grupos del usuario.</span><span class="sxs-lookup"><span data-stu-id="f7174-170">A user's access token contains a list of the privileges held by either the user or the user's groups.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-171"><span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**Procese**</span><span class="sxs-lookup"><span data-stu-id="f7174-171"><span id="_security_process_gly"></span><span id="_SECURITY_PROCESS_GLY"></span>**process**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-172">El contexto de seguridad bajo el que se ejecuta una aplicación.</span><span class="sxs-lookup"><span data-stu-id="f7174-172">The security context under which an application runs.</span></span> <span data-ttu-id="f7174-173">Normalmente, el contexto de seguridad está asociado a un usuario, por lo que todas las aplicaciones que se ejecutan bajo un proceso determinado toman los permisos y privilegios del usuario propietario.</span><span class="sxs-lookup"><span data-stu-id="f7174-173">Typically, the security context is associated with a user, so all applications running under a given process take on the permissions and privileges of the owning user.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-174"><span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**DSS de PROV \_**</span><span class="sxs-lookup"><span data-stu-id="f7174-174"><span id="_security_prov_dss_gly"></span><span id="_SECURITY_PROV_DSS_GLY"></span>**PROV\_DSS**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-175">Consulte *el \_ tipo de proveedor de DSS de Prov*.</span><span class="sxs-lookup"><span data-stu-id="f7174-175">See *PROV\_DSS provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-176"><span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**Tipo de proveedor de DSS de PROV \_**</span><span class="sxs-lookup"><span data-stu-id="f7174-176"><span id="_security_prov_dss_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_PROVIDER_TYPE_GLY"></span>**PROV\_DSS Provider Type**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-177">Tipo de proveedor predefinido que solo admite firmas y hashes digitales.</span><span class="sxs-lookup"><span data-stu-id="f7174-177">Predefined provider type that only supports digital signatures and hashes.</span></span> <span data-ttu-id="f7174-178">Especifica el algoritmo de firma de DSA y los algoritmos hash MD5 y SHA-1.</span><span class="sxs-lookup"><span data-stu-id="f7174-178">It specifies the DSA signature algorithm, and the MD5 and SHA-1 hashing algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-179"><span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**de PROV \_ DSS \_ DH**</span><span class="sxs-lookup"><span data-stu-id="f7174-179"><span id="_security_prov_dss_dh_gly"></span><span id="_SECURITY_PROV_DSS_DH_GLY"></span>**PROV\_DSS\_DH**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-180">Consulte *\_ tipo de \_ proveedor de la DSS DSS de Prov*.</span><span class="sxs-lookup"><span data-stu-id="f7174-180">See *PROV\_DSS\_DH provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-181"><span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**\_Tipo de proveedor de DSS DSS \_ DH**</span><span class="sxs-lookup"><span data-stu-id="f7174-181"><span id="_security_prov_dss_dh_provider_type_gly"></span><span id="_SECURITY_PROV_DSS_DH_PROVIDER_TYPE_GLY"></span>**PROV\_DSS\_DH provider type**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-182">Tipo de proveedor predefinido que proporciona intercambio de claves, firma digital y algoritmos hash.</span><span class="sxs-lookup"><span data-stu-id="f7174-182">Predefined provider type that provides key exchange, digital signature, and hashing algorithms.</span></span> <span data-ttu-id="f7174-183">Es similar al tipo de proveedor de DSS de PROV \_ .</span><span class="sxs-lookup"><span data-stu-id="f7174-183">It is similar to the PROV\_DSS provider type.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-184"><span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**Fortezza de PROV \_**</span><span class="sxs-lookup"><span data-stu-id="f7174-184"><span id="_security_prov_fortezza_gly"></span><span id="_SECURITY_PROV_FORTEZZA_GLY"></span>**PROV\_FORTEZZA**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-185">Vea *\_ tipo de proveedor de Fortezza de Prov*.</span><span class="sxs-lookup"><span data-stu-id="f7174-185">See *PROV\_FORTEZZA provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-186"><span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**Tipo de proveedor de Fortezza de PROV \_**</span><span class="sxs-lookup"><span data-stu-id="f7174-186"><span id="_security_prov_fortezza_provider_type_gly"></span><span id="_SECURITY_PROV_FORTEZZA_PROVIDER_TYPE_GLY"></span>**PROV\_FORTEZZA provider type**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-187">Tipo de proveedor predefinido que proporciona intercambio de claves, firma digital, cifrado y algoritmos hash.</span><span class="sxs-lookup"><span data-stu-id="f7174-187">Predefined provider type that provides key exchange, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="f7174-188">Los protocolos criptográficos y los algoritmos especificados por este tipo de proveedor pertenecen al National Institute of Standards and Technology (NIST).</span><span class="sxs-lookup"><span data-stu-id="f7174-188">The cryptographic protocols and algorithms specified by this provider type are owned by the National Institute of Standards and Technology (NIST).</span></span>

</dd> <dt>

<span data-ttu-id="f7174-189"><span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**\_Microsoft \_ Exchange**</span><span class="sxs-lookup"><span data-stu-id="f7174-189"><span id="_security_prov_ms_exchange_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_GLY"></span>**PROV\_MS\_EXCHANGE**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-190">Consulte *\_ tipo de \_ proveedor de Microsoft Exchange*.</span><span class="sxs-lookup"><span data-stu-id="f7174-190">See *PROV\_MS\_EXCHANGE provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-191"><span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**\_Tipo de \_ proveedor de Microsoft Exchange**</span><span class="sxs-lookup"><span data-stu-id="f7174-191"><span id="_security_prov_ms_exchange_provider_type_gly"></span><span id="_SECURITY_PROV_MS_EXCHANGE_PROVIDER_TYPE_GLY"></span>**PROV\_MS\_EXCHANGE provider type**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-192">Tipo de proveedor predefinido diseñado para las necesidades de Microsoft Exchange, así como otras aplicaciones compatibles con Microsoft Mail.</span><span class="sxs-lookup"><span data-stu-id="f7174-192">Predefined provider type designed for the needs of Microsoft Exchange, as well as other applications that are compatible with Microsoft Mail.</span></span> <span data-ttu-id="f7174-193">Proporciona intercambio de claves, firma digital, cifrado y algoritmos hash.</span><span class="sxs-lookup"><span data-stu-id="f7174-193">It provides key exchange, digital signature, encryption, and hashing algorithms.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-194"><span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**aprovisionamiento \_ completo de RSA \_**</span><span class="sxs-lookup"><span data-stu-id="f7174-194"><span id="_security_prov_rsa_full_gly"></span><span id="_SECURITY_PROV_RSA_FULL_GLY"></span>**PROV\_RSA\_FULL**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-195">Consulte *el \_ \_ tipo de proveedor completo RSA*.</span><span class="sxs-lookup"><span data-stu-id="f7174-195">See *PROV\_RSA\_FULL provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-196"><span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**\_Tipo de \_ proveedor completo RSA de Prov**</span><span class="sxs-lookup"><span data-stu-id="f7174-196"><span id="_security_prov_rsa_full_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_FULL_PROVIDER_TYPE_GLY"></span>**PROV\_RSA\_FULL provider type**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-197">Tipo de proveedor predefinido definido por Microsoft y RSA Data Security, Inc. Este tipo de proveedor de uso general proporciona intercambio de claves, firma digital, cifrado y algoritmos hash.</span><span class="sxs-lookup"><span data-stu-id="f7174-197">Predefined provider type defined by Microsoft and RSA Data Security, Inc. This general purpose provider type provides key exchange, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="f7174-198">El intercambio de claves, la firma digital y los algoritmos de cifrado se basan en la criptografía de clave pública RSA.</span><span class="sxs-lookup"><span data-stu-id="f7174-198">The key exchange, digital signature, and encryption algorithms are based on RSA public key cryptography.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-199"><span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**\_firma RSA \_ SIG**</span><span class="sxs-lookup"><span data-stu-id="f7174-199"><span id="_security_prov_rsa_sig_gly"></span><span id="_SECURITY_PROV_RSA_SIG_GLY"></span>**PROV\_RSA\_SIG**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-200">Consulte *\_ tipo de \_ proveedor de RSA SIG de Prov*.</span><span class="sxs-lookup"><span data-stu-id="f7174-200">See *PROV\_RSA\_SIG provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-201"><span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**\_Tipo de proveedor de RSA SIG de Prov \_**</span><span class="sxs-lookup"><span data-stu-id="f7174-201"><span id="_security_prov_rsa_sig_provider_type_gly"></span><span id="_SECURITY_PROV_RSA_SIG_PROVIDER_TYPE_GLY"></span>**PROV\_RSA\_SIG provider type**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-202">Tipo de proveedor predefinido definido por Microsoft y RSA Data Security.</span><span class="sxs-lookup"><span data-stu-id="f7174-202">Predefined provider type defined by Microsoft and RSA Data Security.</span></span> <span data-ttu-id="f7174-203">Este tipo de proveedor es un subconjunto de aprovisionamiento de \_ RSA \_ completo que proporciona solo algoritmos de firma digital y hash.</span><span class="sxs-lookup"><span data-stu-id="f7174-203">This provider type is a subset of PROV\_RSA\_FULL that provides only digital signature and hashing algorithms.</span></span> <span data-ttu-id="f7174-204">El algoritmo de firma digital es un algoritmo de clave pública RSA.</span><span class="sxs-lookup"><span data-stu-id="f7174-204">The digital signature algorithm is an RSA public key algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-205"><span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**SSL de PROV \_**</span><span class="sxs-lookup"><span data-stu-id="f7174-205"><span id="_security_prov_ssl_gly"></span><span id="_SECURITY_PROV_SSL_GLY"></span>**PROV\_SSL**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-206">Vea *\_ tipo de proveedor de SSL de Prov*.</span><span class="sxs-lookup"><span data-stu-id="f7174-206">See *PROV\_SSL provider type*.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-207"><span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**Tipo de proveedor de SSL de PROV \_**</span><span class="sxs-lookup"><span data-stu-id="f7174-207"><span id="_security_prov_ssl_provider_type_gly"></span><span id="_SECURITY_PROV_SSL_PROVIDER_TYPE_GLY"></span>**PROV\_SSL provider type**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-208">Tipo de proveedor predefinido que admite el protocolo Capa de sockets seguros (SSL).</span><span class="sxs-lookup"><span data-stu-id="f7174-208">Predefined provider type that supports the Secure Sockets Layer (SSL) protocol.</span></span> <span data-ttu-id="f7174-209">Este tipo proporciona cifrado de claves, firma digital, cifrado y algoritmos hash.</span><span class="sxs-lookup"><span data-stu-id="f7174-209">This type provides key encryption, digital signature, encryption, and hashing algorithms.</span></span> <span data-ttu-id="f7174-210">Una especificación que explica SSL está disponible en Netscape Communications Corp.</span><span class="sxs-lookup"><span data-stu-id="f7174-210">A specification explaining SSL is available from Netscape Communications Corp.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-211"><span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**presta**</span><span class="sxs-lookup"><span data-stu-id="f7174-211"><span id="_security_provider_gly"></span><span id="_SECURITY_PROVIDER_GLY"></span>**provider**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-212">Vea [*proveedor de servicios de cifrado*](c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f7174-212">See [*Cryptographic Service Provider*](c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7174-213"><span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**nombre del proveedor**</span><span class="sxs-lookup"><span data-stu-id="f7174-213"><span id="_security_provider_name_gly"></span><span id="_SECURITY_PROVIDER_NAME_GLY"></span>**provider name**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-214">Nombre usado para identificar un CSP.</span><span class="sxs-lookup"><span data-stu-id="f7174-214">A name used to identify a CSP.</span></span> <span data-ttu-id="f7174-215">Por ejemplo, la versión 1,0 del proveedor de servicios criptográficos básicos de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f7174-215">For example, the Microsoft Base Cryptographic Provider version 1.0.</span></span> <span data-ttu-id="f7174-216">Normalmente, el nombre del proveedor se usa al llamar a la función **CryptAcquireContext** para conectarse a un CSP.</span><span class="sxs-lookup"><span data-stu-id="f7174-216">The provider name is typically used when calling the **CryptAcquireContext** function to connect to a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-217"><span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**tipo de proveedor**</span><span class="sxs-lookup"><span data-stu-id="f7174-217"><span id="_security_provider_type_gly"></span><span id="_SECURITY_PROVIDER_TYPE_GLY"></span>**provider type**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-218">Término usado para identificar un tipo de proveedor de servicios criptográficos (CSP).</span><span class="sxs-lookup"><span data-stu-id="f7174-218">A term used to identify a type of cryptographic service provider (CSP).</span></span> <span data-ttu-id="f7174-219">Los CSP se agrupan en diferentes tipos de proveedor que representan una familia específica de protocolos y formatos de datos estándar.</span><span class="sxs-lookup"><span data-stu-id="f7174-219">CSPs are grouped into different provider types that represent a specific families of standard data formats and protocols.</span></span> <span data-ttu-id="f7174-220">A diferencia del nombre de proveedor único de un CSP, los tipos de proveedor no son únicos para un CSP determinado.</span><span class="sxs-lookup"><span data-stu-id="f7174-220">In contrast to a CSP's unique provider name, provider types are not unique for a given CSP.</span></span> <span data-ttu-id="f7174-221">Normalmente, el tipo de proveedor se usa al llamar a la función **CryptAcquireContext** para conectarse a un CSP.</span><span class="sxs-lookup"><span data-stu-id="f7174-221">The provider type is typically used when calling the **CryptAcquireContext** function to connect to a CSP.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-222"><span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**función pseudoaleatorios**</span><span class="sxs-lookup"><span data-stu-id="f7174-222"><span id="_security_pseudo_random_function_gly"></span><span id="_SECURITY_PSEUDO_RANDOM_FUNCTION_GLY"></span>**pseudo-random function**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-223">FICHERO Una función que toma una clave, una etiqueta y una inicialización como entrada y, a continuación, genera una salida de longitud arbitraria.</span><span class="sxs-lookup"><span data-stu-id="f7174-223">(PRF) A function that takes a key, label, and seed as input, then produces an output of arbitrary length.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-224"><span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**par de claves pública y privada**</span><span class="sxs-lookup"><span data-stu-id="f7174-224"><span id="_security_public_private_key_pair_gly"></span><span id="_SECURITY_PUBLIC_PRIVATE_KEY_PAIR_GLY"></span>**public/private key pair**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-225">Un conjunto de claves criptográficas utilizado para la criptografía de clave pública.</span><span class="sxs-lookup"><span data-stu-id="f7174-225">A set of cryptographic keys used for public key cryptography.</span></span> <span data-ttu-id="f7174-226">Para cada usuario, un CSP normalmente mantiene dos pares de claves pública y privada: un par de claves de intercambio y un par de claves de firma digital.</span><span class="sxs-lookup"><span data-stu-id="f7174-226">For each user, a CSP usually maintains two public/private key pairs: an exchange key pair and a digital signature key pair.</span></span> <span data-ttu-id="f7174-227">Ambos pares de claves se mantienen de una sesión a otra.</span><span class="sxs-lookup"><span data-stu-id="f7174-227">Both key pairs are maintained from session to session.</span></span>

<span data-ttu-id="f7174-228">Consulte par de claves de [*Exchange*](e-gly.md) y par de [*claves de firma*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f7174-228">See [*exchange key pair*](e-gly.md) and [*signature key pair*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="f7174-229"><span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**clave pública**</span><span class="sxs-lookup"><span data-stu-id="f7174-229"><span id="_security_public_key_gly"></span><span id="_SECURITY_PUBLIC_KEY_GLY"></span>**public key**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-230">Una clave criptográfica utilizada normalmente al descifrar una clave de sesión o una firma digital.</span><span class="sxs-lookup"><span data-stu-id="f7174-230">A cryptographic key typically used when decrypting a session key or a digital signature.</span></span> <span data-ttu-id="f7174-231">La clave pública también se puede utilizar para cifrar un mensaje, garantizando que solo la persona con la clave privada correspondiente puede descifrar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="f7174-231">The public key can also be used to encrypt a message, guaranteeing that only the person with the corresponding private key can decrypt the message.</span></span>

<span data-ttu-id="f7174-232">Vea también *clave privada*.</span><span class="sxs-lookup"><span data-stu-id="f7174-232">See also *private key*.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-233"><span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**algoritmo de clave pública**</span><span class="sxs-lookup"><span data-stu-id="f7174-233"><span id="_security_public_key_algorithm_gly"></span><span id="_SECURITY_PUBLIC_KEY_ALGORITHM_GLY"></span>**public key algorithm**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-234">Cifrado asimétrico que usa dos claves, una para el cifrado, la clave pública y la otra para el descifrado, la clave privada.</span><span class="sxs-lookup"><span data-stu-id="f7174-234">An asymmetric cipher that uses two keys, one for encryption, the public key, and the other for decryption, the private key.</span></span> <span data-ttu-id="f7174-235">Como se trata de los nombres de clave, la clave pública que se usa para codificar texto no cifrado puede ponerse a disposición de cualquier usuario.</span><span class="sxs-lookup"><span data-stu-id="f7174-235">As implied by the key names, the public key used to encode plaintext can be made available to anyone.</span></span> <span data-ttu-id="f7174-236">Sin embargo, la clave privada debe permanecer secreta.</span><span class="sxs-lookup"><span data-stu-id="f7174-236">However, the private key must remain secret.</span></span> <span data-ttu-id="f7174-237">Solo la clave privada puede descifrar el texto cifrado.</span><span class="sxs-lookup"><span data-stu-id="f7174-237">Only the private key can decrypt the ciphertext.</span></span> <span data-ttu-id="f7174-238">El algoritmo de clave pública que se usa en este proceso es lento (en el orden de 1.000 veces más lento que los algoritmos simétricos) y normalmente se usa para cifrar las claves de sesión o firmar digitalmente un mensaje.</span><span class="sxs-lookup"><span data-stu-id="f7174-238">The public key algorithm used in this process is slow (on the order of 1,000 times slower than symmetric algorithms), and is typically used to encrypt session keys or digitally sign a message.</span></span>

<span data-ttu-id="f7174-239">Vea también *clave pública* y *clave privada*.</span><span class="sxs-lookup"><span data-stu-id="f7174-239">See also *public key* and *private key*.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-240"><span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**BLOB de clave pública**</span><span class="sxs-lookup"><span data-stu-id="f7174-240"><span id="_security_public_key_blob_gly"></span><span id="_SECURITY_PUBLIC_KEY_BLOB_GLY"></span>**public key BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-241">Un BLOB que se usa para almacenar la parte de la clave pública de un par de claves pública y privada.</span><span class="sxs-lookup"><span data-stu-id="f7174-241">A BLOB used to store the public key portion of a public/private key pair.</span></span> <span data-ttu-id="f7174-242">Los blobs de clave pública no se cifran, ya que la clave pública incluida en no es secreta.</span><span class="sxs-lookup"><span data-stu-id="f7174-242">Public key BLOBs are not encrypted as the public key contained within is not secret.</span></span> <span data-ttu-id="f7174-243">Un BLOB de clave pública se crea mediante una llamada a la función **CryptExportKey** .</span><span class="sxs-lookup"><span data-stu-id="f7174-243">A public key BLOB is created by calling the **CryptExportKey** function.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-244"><span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Estándares de criptografía de clave pública**</span><span class="sxs-lookup"><span data-stu-id="f7174-244"><span id="_security_public_key_cryptography_standards_gly"></span><span id="_SECURITY_PUBLIC_KEY_CRYPTOGRAPHY_STANDARDS_GLY"></span>**Public Key Cryptography Standards**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-245">PKCS Un conjunto de estándares de sintaxis para la criptografía de clave pública que abarca las funciones de seguridad, incluidos los métodos para firmar datos, el intercambio de claves, la solicitud de certificados, el cifrado y descifrado de claves públicas y otras funciones de seguridad.</span><span class="sxs-lookup"><span data-stu-id="f7174-245">(PKCS) A set of syntax standards for public key cryptography covering security functions, including methods for signing data, exchanging keys, requesting certificates, public key encryption and decryption, and other security functions.</span></span>

</dd> <dt>

<span data-ttu-id="f7174-246"><span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**cifrado de clave pública**</span><span class="sxs-lookup"><span data-stu-id="f7174-246"><span id="_security_public_key_encryption_gly"></span><span id="_SECURITY_PUBLIC_KEY_ENCRYPTION_GLY"></span>**public key encryption**</span></span>
</dt> <dd>

<span data-ttu-id="f7174-247">Cifrado que utiliza un par de claves, una clave para cifrar los datos y la otra clave para descifrar los datos.</span><span class="sxs-lookup"><span data-stu-id="f7174-247">Encryption that uses a pair of keys, one key to encrypt data and the other key to decrypt data.</span></span> <span data-ttu-id="f7174-248">Por el contrario, los algoritmos de cifrado simétricos usan la misma clave para cifrado y descifrado.</span><span class="sxs-lookup"><span data-stu-id="f7174-248">In contrast, symmetric encryption algorithms that use the same key for both encryption and decryption.</span></span> <span data-ttu-id="f7174-249">En la práctica, la criptografía de clave pública se usa normalmente para proteger la clave de sesión utilizada por un algoritmo de cifrado simétrico.</span><span class="sxs-lookup"><span data-stu-id="f7174-249">In practice, public key cryptography is typically used to protect the session key used by a symmetric encryption algorithm.</span></span> <span data-ttu-id="f7174-250">En este caso, la clave pública se utiliza para cifrar la clave de sesión, que, a su vez, fue utilizada para cifrar algunos datos, y la clave privada se utiliza para el descifrado.</span><span class="sxs-lookup"><span data-stu-id="f7174-250">In this case, the public key is used to encrypt the session key, which in turn was used to encrypt some data, and the private key is used for decryption.</span></span> <span data-ttu-id="f7174-251">Además de para proteger las claves de sesión, la criptografía de clave pública también se puede utilizar para firmar digitalmente un mensaje (mediante la clave privada) y validar la firma (mediante la clave pública).</span><span class="sxs-lookup"><span data-stu-id="f7174-251">In addition to protecting session keys, public key cryptography may also be used to digitally sign a message (using the private key) and validate the signature (using the public key).</span></span>

<span data-ttu-id="f7174-252">Vea también *algoritmo de clave pública*.</span><span class="sxs-lookup"><span data-stu-id="f7174-252">See also *public key algorithm*.</span></span>

</dd> </dl>

 

 



