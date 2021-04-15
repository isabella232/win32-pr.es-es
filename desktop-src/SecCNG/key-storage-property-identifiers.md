---
description: Se usa para identificar una propiedad de almacenamiento de claves.
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: Identificadores de propiedad de almacenamiento de claves (ncrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 813a15ba106989cb558eba181bc893d75c6d1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669911"
---
# <a name="key-storage-property-identifiers"></a><span data-ttu-id="70004-103">Identificadores de propiedad de almacenamiento de claves</span><span class="sxs-lookup"><span data-stu-id="70004-103">Key Storage Property Identifiers</span></span>

<span data-ttu-id="70004-104">Los valores siguientes se usan para identificar una propiedad de almacenamiento de claves.</span><span class="sxs-lookup"><span data-stu-id="70004-104">The following values are used to identify a key storage property.</span></span>

<dl> <dt>

<span data-ttu-id="70004-105"><span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**\_propiedad de \_ grupo de algoritmo NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-105"><span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**NCRYPT\_ALGORITHM\_GROUP\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-106">L "grupo de algoritmos"</span><span class="sxs-lookup"><span data-stu-id="70004-106">L"Algorithm Group"</span></span>
</dt> <dt>



<span data-ttu-id="70004-107">Una cadena Unicode terminada en null que contiene el nombre del grupo de algoritmos del objeto.</span><span class="sxs-lookup"><span data-stu-id="70004-107">A null-terminated Unicode string that contains the name of the object's algorithm group.</span></span> <span data-ttu-id="70004-108">Esta propiedad solo se aplica a las claves.</span><span class="sxs-lookup"><span data-stu-id="70004-108">This property only applies to keys.</span></span> <span data-ttu-id="70004-109">El proveedor de almacenamiento de claves de Microsoft devuelve los siguientes identificadores.</span><span class="sxs-lookup"><span data-stu-id="70004-109">The following identifiers are returned by the Microsoft key storage provider.</span></span>



| <span data-ttu-id="70004-110">Identificador</span><span class="sxs-lookup"><span data-stu-id="70004-110">Identifier</span></span>                                     | <span data-ttu-id="70004-111">Value</span><span class="sxs-lookup"><span data-stu-id="70004-111">Value</span></span>              | <span data-ttu-id="70004-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="70004-112">Description</span></span>                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| <span data-ttu-id="70004-113">**\_grupo de \_ algoritmos RSA de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-113">**NCRYPT\_RSA\_ALGORITHM\_GROUP**</span></span><br/>   | <span data-ttu-id="70004-114">RSA</span><span class="sxs-lookup"><span data-stu-id="70004-114">"RSA"</span></span><br/>   | <span data-ttu-id="70004-115">El grupo de algoritmos RSA.</span><span class="sxs-lookup"><span data-stu-id="70004-115">The RSA algorithm group.</span></span><br/>                           |
| <span data-ttu-id="70004-116">**\_grupo de \_ algoritmos DH NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-116">**NCRYPT\_DH\_ALGORITHM\_GROUP**</span></span><br/>    | <span data-ttu-id="70004-117">DH</span><span class="sxs-lookup"><span data-stu-id="70004-117">"DH"</span></span><br/>    | <span data-ttu-id="70004-118">El grupo de algoritmos Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="70004-118">The Diffie-Hellman algorithm group.</span></span><br/>                |
| <span data-ttu-id="70004-119">**\_grupo de \_ algoritmo \_ DSA de NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="70004-119">**NCRYPT\_DSA\_ALGORITHM\_GROUP**</span></span><br/>   | <span data-ttu-id="70004-120">ALGORITMO</span><span class="sxs-lookup"><span data-stu-id="70004-120">"DSA"</span></span><br/>   | <span data-ttu-id="70004-121">El grupo de algoritmos DSA.</span><span class="sxs-lookup"><span data-stu-id="70004-121">The DSA algorithm group.</span></span><br/>                           |
| <span data-ttu-id="70004-122">**\_grupo de \_ algoritmos ECDSA de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-122">**NCRYPT\_ECDSA\_ALGORITHM\_GROUP**</span></span><br/> | <span data-ttu-id="70004-123">ECDSA</span><span class="sxs-lookup"><span data-stu-id="70004-123">"ECDSA"</span></span><br/> | <span data-ttu-id="70004-124">El grupo de algoritmo DSA de curva elíptica.</span><span class="sxs-lookup"><span data-stu-id="70004-124">The elliptic curve DSA algorithm group.</span></span><br/>            |
| <span data-ttu-id="70004-125">**\_grupo de \_ algoritmos ECDH NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-125">**NCRYPT\_ECDH\_ALGORITHM\_GROUP**</span></span><br/>  | <span data-ttu-id="70004-126">ECDH</span><span class="sxs-lookup"><span data-stu-id="70004-126">"ECDH"</span></span><br/>  | <span data-ttu-id="70004-127">Curva elíptica Diffie-Hellman grupo de algoritmos.</span><span class="sxs-lookup"><span data-stu-id="70004-127">The elliptic curve Diffie-Hellman algorithm group.</span></span><br/> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-128"><span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**\_propiedad del algoritmo NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-128"><span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**NCRYPT\_ALGORITHM\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-129">L "nombre del algoritmo"</span><span class="sxs-lookup"><span data-stu-id="70004-129">L"Algorithm Name"</span></span>
</dt> <dt>



<span data-ttu-id="70004-130">Una cadena Unicode terminada en null que contiene el nombre del algoritmo del objeto.</span><span class="sxs-lookup"><span data-stu-id="70004-130">A null-terminated Unicode string that contains the name of the object's algorithm.</span></span> <span data-ttu-id="70004-131">Puede ser uno de los [**identificadores de algoritmo CNG**](cng-algorithm-identifiers.md) predefinidos u otro identificador de algoritmo registrado.</span><span class="sxs-lookup"><span data-stu-id="70004-131">This can be one of the predefined [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) or another registered algorithm identifier.</span></span> <span data-ttu-id="70004-132">Esta propiedad solo se aplica a las claves.</span><span class="sxs-lookup"><span data-stu-id="70004-132">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-133"><span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**\_ \_ clave ECDH asociada de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-133"><span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**NCRYPT\_ASSOCIATED\_ECDH\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-134">L "SmartCardAssociatedECDHKey"</span><span class="sxs-lookup"><span data-stu-id="70004-134">L"SmartCardAssociatedECDHKey"</span></span>
</dt> <dt>



<span data-ttu-id="70004-135">Valor **LPWStr** que indica el nombre del contenedor de la clave de curva elíptica Diffie-Hellman (ECDH) que se va a usar durante el inicio de sesión para un identificador determinado de una clave de algoritmo de firma digital de curva elíptica (ECDSA).</span><span class="sxs-lookup"><span data-stu-id="70004-135">An **LPWSTR** value that indicates the container name of the Elliptic Curve Diffie-Hellman (ECDH) key to use during logon for a given handle to an Elliptic Curve Digital Signature Algorithm (ECDSA) key.</span></span> <span data-ttu-id="70004-136">Si no hay ninguna clave ECDH en la tarjeta, el [*proveedor de almacenamiento de claves*](/windows/desktop/SecGloss/k-gly) (KSP) devuelve **NTE \_ no \_ encontrado**.</span><span class="sxs-lookup"><span data-stu-id="70004-136">If there are no ECDH keys on the card, the [*key storage provider*](/windows/desktop/SecGloss/k-gly) (KSP) returns **NTE\_NOT\_FOUND**.</span></span> <span data-ttu-id="70004-137">Esta propiedad se aplica a las claves ECDSA para el inicio de sesión con tarjetas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="70004-137">This property applies to ECDSA keys for logon with smart cards.</span></span> <span data-ttu-id="70004-138">La propiedad es compatible con el proveedor de almacenamiento de claves de tarjeta inteligente de Microsoft y no con el proveedor de almacenamiento de claves de software de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="70004-138">The property is supported by the Microsoft Smart Card key storage provider and not by the Microsoft Software key storage provider.</span></span>

<span data-ttu-id="70004-139">**Windows Server 2008 y Windows Vista:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="70004-139">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-140"><span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**\_ \_ propiedad longitud de bloque NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-140"><span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**NCRYPT\_BLOCK\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-141">L "longitud de bloque"</span><span class="sxs-lookup"><span data-stu-id="70004-141">L"Block Length"</span></span>
</dt> <dt>



<span data-ttu-id="70004-142">**DWORD** que contiene la longitud, en bytes, del bloque de cifrado.</span><span class="sxs-lookup"><span data-stu-id="70004-142">A **DWORD** that contains the length, in bytes, of the encryption block.</span></span> <span data-ttu-id="70004-143">Esta propiedad solo se aplica a las claves que admiten el cifrado.</span><span class="sxs-lookup"><span data-stu-id="70004-143">This property only applies to keys that support encryption.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-144"><span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**\_propiedad de certificado NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-144"><span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**NCRYPT\_CERTIFICATE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-145">L "SmartCardKeyCertificate"</span><span class="sxs-lookup"><span data-stu-id="70004-145">L"SmartCardKeyCertificate"</span></span>
</dt> <dt>



<span data-ttu-id="70004-146">Un [*BLOB*](/windows/desktop/SecGloss/b-gly) que contiene un certificado X. 509 que está asociado a la clave.</span><span class="sxs-lookup"><span data-stu-id="70004-146">A [*BLOB*](/windows/desktop/SecGloss/b-gly) that contains an X.509 certificate that is associated with the key.</span></span>

<span data-ttu-id="70004-147">**Windows server 2008 R2, Windows 7, Windows server 2008 y Windows Vista:** Un [*BLOB*](/windows/desktop/SecGloss/b-gly) que contiene el [*certificado*](/windows/desktop/SecGloss/c-gly)de clave de [*tarjeta inteligente*](/windows/desktop/SecGloss/s-gly) .</span><span class="sxs-lookup"><span data-stu-id="70004-147">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** A [*BLOB*](/windows/desktop/SecGloss/b-gly) that contains the [*smart card*](/windows/desktop/SecGloss/s-gly) key [*certificate*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="70004-148">Esta propiedad no es compatible con el proveedor de almacenamiento de claves de software de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="70004-148">This property is not supported by the Microsoft Software Key Storage Provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-149"><span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**\_propiedad de \_ parámetros \_ DH de NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="70004-149"><span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**NCRYPT\_DH\_PARAMETERS\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-150">L "DHParameters"</span><span class="sxs-lookup"><span data-stu-id="70004-150">L"DHParameters"</span></span>
</dt> <dt>



<span data-ttu-id="70004-151">Especifica los parámetros que se van a usar con una clave de Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="70004-151">Specifies parameters to use with a Diffie-Hellman key.</span></span> <span data-ttu-id="70004-152">Este tipo de datos es un puntero a una estructura de [**\_ encabezado de \_ parámetro \_ de BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="70004-152">This data type is a pointer to a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span> <span data-ttu-id="70004-153">Esta propiedad solo se puede establecer y debe establecerse para la clave antes de que se complete la clave.</span><span class="sxs-lookup"><span data-stu-id="70004-153">This property can only be set and must be set for the key before the key is completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-154"><span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**\_propiedad de \_ Directiva de exportación de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-154"><span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**NCRYPT\_EXPORT\_POLICY\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-155">L "exportar Directiva"</span><span class="sxs-lookup"><span data-stu-id="70004-155">L"Export Policy"</span></span>
</dt> <dt>



<span data-ttu-id="70004-156">**DWORD** que contiene un conjunto de marcas que especifican la Directiva de exportación para una clave conservada.</span><span class="sxs-lookup"><span data-stu-id="70004-156">A **DWORD** that contains a set of flags that specify the export policy for a persisted key.</span></span> <span data-ttu-id="70004-157">Esta propiedad solo se aplica a las claves.</span><span class="sxs-lookup"><span data-stu-id="70004-157">This property only applies to keys.</span></span> <span data-ttu-id="70004-158">Puede contener cero o una combinación de uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="70004-158">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="70004-159">Identificador</span><span class="sxs-lookup"><span data-stu-id="70004-159">Identifier</span></span>                                    | <span data-ttu-id="70004-160">Value</span><span class="sxs-lookup"><span data-stu-id="70004-160">Value</span></span>      | <span data-ttu-id="70004-161">Descripción</span><span class="sxs-lookup"><span data-stu-id="70004-161">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70004-162">**\_marca permitir \_ exportación de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-162">**NCRYPT\_ALLOW\_EXPORT\_FLAG**</span></span>               | <span data-ttu-id="70004-163">0x00000001</span><span class="sxs-lookup"><span data-stu-id="70004-163">0x00000001</span></span> | <span data-ttu-id="70004-164">Se puede exportar la clave privada.</span><span class="sxs-lookup"><span data-stu-id="70004-164">The private key can be exported.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="70004-165">**NCRYPT \_ permitir \_ la \_ marca de exportación de texto sin formato \_**</span><span class="sxs-lookup"><span data-stu-id="70004-165">**NCRYPT\_ALLOW\_PLAINTEXT\_EXPORT\_FLAG**</span></span>    | <span data-ttu-id="70004-166">0x00000002</span><span class="sxs-lookup"><span data-stu-id="70004-166">0x00000002</span></span> | <span data-ttu-id="70004-167">La clave privada se puede exportar en formato de texto simple.</span><span class="sxs-lookup"><span data-stu-id="70004-167">The private key can be exported in plaintext form.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="70004-168">**\_marca permitir \_ archivado \_ de NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="70004-168">**NCRYPT\_ALLOW\_ARCHIVING\_FLAG**</span></span>            | <span data-ttu-id="70004-169">0x00000004</span><span class="sxs-lookup"><span data-stu-id="70004-169">0x00000004</span></span> | <span data-ttu-id="70004-170">La clave privada se puede exportar una vez para fines de archivado.</span><span class="sxs-lookup"><span data-stu-id="70004-170">The private key can be exported once for archiving purposes.</span></span> <span data-ttu-id="70004-171">Esta marca solo se aplica al identificador de clave original en el que se establece.</span><span class="sxs-lookup"><span data-stu-id="70004-171">This flag only applies to the original key handle on which it is set.</span></span> <span data-ttu-id="70004-172">Esta directiva solo se puede aplicar al identificador de clave original.</span><span class="sxs-lookup"><span data-stu-id="70004-172">This policy can only be applied to the original key handle.</span></span> <span data-ttu-id="70004-173">Una vez que se ha cerrado el identificador de clave, ya no se puede exportar la clave para fines de archivado.</span><span class="sxs-lookup"><span data-stu-id="70004-173">After the key handle has been closed, the key can no longer be exported for archiving purposes.</span></span>                   |
| <span data-ttu-id="70004-174">**NCRYPT \_ permitir \_ el \_ marcado de archivo sin formato \_**</span><span class="sxs-lookup"><span data-stu-id="70004-174">**NCRYPT\_ALLOW\_PLAINTEXT\_ARCHIVING\_FLAG**</span></span> | <span data-ttu-id="70004-175">0x00000008</span><span class="sxs-lookup"><span data-stu-id="70004-175">0x00000008</span></span> | <span data-ttu-id="70004-176">La clave privada se puede exportar una vez en formato de texto no cifrado.</span><span class="sxs-lookup"><span data-stu-id="70004-176">The private key can be exported once in plaintext form for archiving purposes.</span></span> <span data-ttu-id="70004-177">Esta marca solo se aplica al identificador de clave original en el que se establece.</span><span class="sxs-lookup"><span data-stu-id="70004-177">This flag only applies to the original key handle on which it is set.</span></span> <span data-ttu-id="70004-178">Esta directiva solo se puede aplicar al identificador de clave original.</span><span class="sxs-lookup"><span data-stu-id="70004-178">This policy can only be applied to the original key handle.</span></span> <span data-ttu-id="70004-179">Una vez que se ha cerrado el identificador de clave, ya no se puede exportar la clave para fines de archivado.</span><span class="sxs-lookup"><span data-stu-id="70004-179">After the key handle has been closed, the key can no longer be exported for archiving purposes.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-180"><span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**\_propiedad del \_ tipo impl impl \_**</span><span class="sxs-lookup"><span data-stu-id="70004-180"><span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**NCRYPT\_IMPL\_TYPE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-181">L "tipo impl"</span><span class="sxs-lookup"><span data-stu-id="70004-181">L"Impl Type"</span></span>
</dt> <dt>



<span data-ttu-id="70004-182">**DWORD** que contiene un conjunto de marcadores que definen los detalles de implementación del proveedor.</span><span class="sxs-lookup"><span data-stu-id="70004-182">A **DWORD** that contains a set of flags that define implementation details of the provider.</span></span> <span data-ttu-id="70004-183">Esta propiedad solo se aplica a los proveedores de almacenamiento de claves.</span><span class="sxs-lookup"><span data-stu-id="70004-183">This property only applies to key storage providers.</span></span> <span data-ttu-id="70004-184">Puede contener cero o una combinación de uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="70004-184">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="70004-185">Identificador</span><span class="sxs-lookup"><span data-stu-id="70004-185">Identifier</span></span>                            | <span data-ttu-id="70004-186">Value</span><span class="sxs-lookup"><span data-stu-id="70004-186">Value</span></span>      | <span data-ttu-id="70004-187">Descripción</span><span class="sxs-lookup"><span data-stu-id="70004-187">Description</span></span>                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| <span data-ttu-id="70004-188">**\_marca de \_ hardware NCRYPT impl \_**</span><span class="sxs-lookup"><span data-stu-id="70004-188">**NCRYPT\_IMPL\_HARDWARE\_FLAG**</span></span>      | <span data-ttu-id="70004-189">0x00000001</span><span class="sxs-lookup"><span data-stu-id="70004-189">0x00000001</span></span> | <span data-ttu-id="70004-190">El proveedor está basado en hardware.</span><span class="sxs-lookup"><span data-stu-id="70004-190">The provider is hardware based.</span></span>                           |
| <span data-ttu-id="70004-191">**\_marca de \_ software NCRYPT impl \_**</span><span class="sxs-lookup"><span data-stu-id="70004-191">**NCRYPT\_IMPL\_SOFTWARE\_FLAG**</span></span>      | <span data-ttu-id="70004-192">0x00000002</span><span class="sxs-lookup"><span data-stu-id="70004-192">0x00000002</span></span> | <span data-ttu-id="70004-193">El proveedor está basado en software.</span><span class="sxs-lookup"><span data-stu-id="70004-193">The provider is software based.</span></span>                           |
| <span data-ttu-id="70004-194">**\_ \_ marca extraíble de NCRYPT impl \_**</span><span class="sxs-lookup"><span data-stu-id="70004-194">**NCRYPT\_IMPL\_REMOVABLE\_FLAG**</span></span>     | <span data-ttu-id="70004-195">0x00000008</span><span class="sxs-lookup"><span data-stu-id="70004-195">0x00000008</span></span> | <span data-ttu-id="70004-196">El proveedor es extraíble.</span><span class="sxs-lookup"><span data-stu-id="70004-196">The provider is removable.</span></span>                                |
| <span data-ttu-id="70004-197">**\_ \_ \_ marca RNG de hardware \_ de NCRYPT impl**</span><span class="sxs-lookup"><span data-stu-id="70004-197">**NCRYPT\_IMPL\_HARDWARE\_RNG\_FLAG**</span></span> | <span data-ttu-id="70004-198">0x00000010</span><span class="sxs-lookup"><span data-stu-id="70004-198">0x00000010</span></span> | <span data-ttu-id="70004-199">El proveedor es un generador de números aleatorios basado en hardware.</span><span class="sxs-lookup"><span data-stu-id="70004-199">The provider is a hardware based random number generator.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-200"><span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**\_ \_ propiedad tipo de clave NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-200"><span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**NCRYPT\_KEY\_TYPE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-201">L "tipo de clave"</span><span class="sxs-lookup"><span data-stu-id="70004-201">L"Key Type"</span></span>
</dt> <dt>



<span data-ttu-id="70004-202">**DWORD** que contiene un conjunto de marcas que definen el tipo de clave.</span><span class="sxs-lookup"><span data-stu-id="70004-202">A **DWORD** that contains a set of flags that define the key type.</span></span> <span data-ttu-id="70004-203">Esta propiedad solo se aplica a las claves.</span><span class="sxs-lookup"><span data-stu-id="70004-203">This property only applies to keys.</span></span> <span data-ttu-id="70004-204">Puede contener cero o el valor siguiente.</span><span class="sxs-lookup"><span data-stu-id="70004-204">This can contain zero or the following value.</span></span>



| <span data-ttu-id="70004-205">Identificador</span><span class="sxs-lookup"><span data-stu-id="70004-205">Identifier</span></span>                     | <span data-ttu-id="70004-206">Value</span><span class="sxs-lookup"><span data-stu-id="70004-206">Value</span></span>      | <span data-ttu-id="70004-207">Descripción</span><span class="sxs-lookup"><span data-stu-id="70004-207">Description</span></span>                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70004-208">**\_marca de \_ clave de equipo NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-208">**NCRYPT\_MACHINE\_KEY\_FLAG**</span></span> | <span data-ttu-id="70004-209">0x00000001</span><span class="sxs-lookup"><span data-stu-id="70004-209">0x00000001</span></span> | <span data-ttu-id="70004-210">La clave se aplica al equipo local.</span><span class="sxs-lookup"><span data-stu-id="70004-210">The key applies to the local computer.</span></span> <span data-ttu-id="70004-211">Si este marcador no está presente, la clave se aplica al usuario actual.</span><span class="sxs-lookup"><span data-stu-id="70004-211">If this flag is not present, the key applies to the current user.</span></span> |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-212"><span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**\_ \_ propiedad uso de clave NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-212"><span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**NCRYPT\_KEY\_USAGE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-213">L "uso de la clave"</span><span class="sxs-lookup"><span data-stu-id="70004-213">L"Key Usage"</span></span>
</dt> <dt>



<span data-ttu-id="70004-214">**DWORD** que contiene un conjunto de marcas que definen los detalles de uso de una clave.</span><span class="sxs-lookup"><span data-stu-id="70004-214">A **DWORD** that contains a set of flags that define the usage details for a key.</span></span> <span data-ttu-id="70004-215">Esta propiedad solo se aplica a las claves.</span><span class="sxs-lookup"><span data-stu-id="70004-215">This property only applies to keys.</span></span> <span data-ttu-id="70004-216">Puede contener cero o una combinación de uno o varios de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="70004-216">This can contain zero or a combination of one or more of the following values.</span></span>



| <span data-ttu-id="70004-217">Identificador</span><span class="sxs-lookup"><span data-stu-id="70004-217">Identifier</span></span>                              | <span data-ttu-id="70004-218">Value</span><span class="sxs-lookup"><span data-stu-id="70004-218">Value</span></span>      | <span data-ttu-id="70004-219">Descripción</span><span class="sxs-lookup"><span data-stu-id="70004-219">Description</span></span>                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| <span data-ttu-id="70004-220">**NCRYPT \_ permitir \_ marca de descifrado \_**</span><span class="sxs-lookup"><span data-stu-id="70004-220">**NCRYPT\_ALLOW\_DECRYPT\_FLAG**</span></span>        | <span data-ttu-id="70004-221">0x00000001</span><span class="sxs-lookup"><span data-stu-id="70004-221">0x00000001</span></span> | <span data-ttu-id="70004-222">La clave se puede utilizar para el descifrado.</span><span class="sxs-lookup"><span data-stu-id="70004-222">The key can be used for decryption.</span></span>                  |
| <span data-ttu-id="70004-223">**NCRYPT \_ permitir \_ la \_ marca de firma**</span><span class="sxs-lookup"><span data-stu-id="70004-223">**NCRYPT\_ALLOW\_SIGNING\_FLAG**</span></span>        | <span data-ttu-id="70004-224">0x00000002</span><span class="sxs-lookup"><span data-stu-id="70004-224">0x00000002</span></span> | <span data-ttu-id="70004-225">La clave se puede utilizar para firmar.</span><span class="sxs-lookup"><span data-stu-id="70004-225">The key can be used for signing.</span></span>                     |
| <span data-ttu-id="70004-226">**\_marca de \_ acuerdo de clave de permitir NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="70004-226">**NCRYPT\_ALLOW\_KEY\_AGREEMENT\_FLAG**</span></span> | <span data-ttu-id="70004-227">0x00000004</span><span class="sxs-lookup"><span data-stu-id="70004-227">0x00000004</span></span> | <span data-ttu-id="70004-228">La clave se puede usar para el cifrado del acuerdo secreto.</span><span class="sxs-lookup"><span data-stu-id="70004-228">The key can be used for secret agreement encryption.</span></span> |
| <span data-ttu-id="70004-229">**NCRYPT \_ permite \_ todos los \_ usos**</span><span class="sxs-lookup"><span data-stu-id="70004-229">**NCRYPT\_ALLOW\_ALL\_USAGES**</span></span>          | <span data-ttu-id="70004-230">0x00FFFFFF</span><span class="sxs-lookup"><span data-stu-id="70004-230">0x00ffffff</span></span> | <span data-ttu-id="70004-231">La clave se puede utilizar para cualquier propósito.</span><span class="sxs-lookup"><span data-stu-id="70004-231">The key can be used for any purpose.</span></span>                 |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-232"><span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**\_propiedad última \_ modificación de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-232"><span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**NCRYPT\_LAST\_MODIFIED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-233">L "modificado"</span><span class="sxs-lookup"><span data-stu-id="70004-233">L"Modified"</span></span>
</dt> <dt>



<span data-ttu-id="70004-234">Indica cuándo se modificó por última vez la clave.</span><span class="sxs-lookup"><span data-stu-id="70004-234">Indicates when the key was last modified.</span></span> <span data-ttu-id="70004-235">Este tipo de datos es un puntero a una estructura de [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) .</span><span class="sxs-lookup"><span data-stu-id="70004-235">This data type is a pointer to a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure.</span></span> <span data-ttu-id="70004-236">Esta propiedad solo se aplica a las claves persistentes.</span><span class="sxs-lookup"><span data-stu-id="70004-236">This property only applies to persisted keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-237"><span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**\_propiedad longitud de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-237"><span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**NCRYPT\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-238">L "longitud"</span><span class="sxs-lookup"><span data-stu-id="70004-238">L"Length"</span></span>
</dt> <dt>



<span data-ttu-id="70004-239">**DWORD** que contiene la longitud, en bits, de la clave.</span><span class="sxs-lookup"><span data-stu-id="70004-239">A **DWORD** that contains the length, in bits, of the key.</span></span> <span data-ttu-id="70004-240">Esta propiedad solo se aplica a las claves.</span><span class="sxs-lookup"><span data-stu-id="70004-240">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-241"><span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**\_propiedad de longitudes NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-241"><span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**NCRYPT\_LENGTHS\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-242">L "longitudes"</span><span class="sxs-lookup"><span data-stu-id="70004-242">L"Lengths"</span></span>
</dt> <dt>



<span data-ttu-id="70004-243">Indica los tamaños de clave admitidos por la clave.</span><span class="sxs-lookup"><span data-stu-id="70004-243">Indicates the key sizes that are supported by the key.</span></span> <span data-ttu-id="70004-244">Este tipo de datos es un puntero a una estructura de [**\_ \_ longitudes admitidas de NCRYPT**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) que contiene esta información.</span><span class="sxs-lookup"><span data-stu-id="70004-244">This data type is a pointer to an [**NCRYPT\_SUPPORTED\_LENGTHS**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) structure that contains this information.</span></span> <span data-ttu-id="70004-245">Esta propiedad solo se aplica a las claves.</span><span class="sxs-lookup"><span data-stu-id="70004-245">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-246"><span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**\_ \_ \_ propiedad longitud máxima del nombre NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-246"><span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**NCRYPT\_MAX\_NAME\_LENGTH\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-247">L "longitud máxima del nombre"</span><span class="sxs-lookup"><span data-stu-id="70004-247">L"Max Name Length"</span></span>
</dt> <dt>



<span data-ttu-id="70004-248">**DWORD** que contiene la longitud máxima, en caracteres, del nombre de una clave persistente.</span><span class="sxs-lookup"><span data-stu-id="70004-248">A **DWORD** that contains the maximum length, in characters, of the name of a persistent key.</span></span> <span data-ttu-id="70004-249">Esta propiedad solo se aplica a un proveedor.</span><span class="sxs-lookup"><span data-stu-id="70004-249">This property only applies to a provider.</span></span>

<span data-ttu-id="70004-250">Esta propiedad está pensada principalmente para ser utilizada por proveedores de almacenamiento de claves que almacenan sus claves en un dispositivo con una cantidad limitada de memoria disponible, como una tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="70004-250">This property is primarily intended to be used by key storage providers that store their keys on a device that has a limited amount of available memory, such as a smart card.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-251"><span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**\_propiedad de nombre NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-251"><span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**NCRYPT\_NAME\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-252">L "nombre"</span><span class="sxs-lookup"><span data-stu-id="70004-252">L"Name"</span></span>
</dt> <dt>



<span data-ttu-id="70004-253">Puntero a una cadena Unicode terminada en null que contiene el nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="70004-253">A pointer to a null-terminated Unicode string that contains the name of the object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-254"><span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**\_ \_ propiedad del símbolo del PIN de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-254"><span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**NCRYPT\_PIN\_PROMPT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-255">L "SmartCardPinPrompt"</span><span class="sxs-lookup"><span data-stu-id="70004-255">L"SmartCardPinPrompt"</span></span>
</dt> <dt>



<span data-ttu-id="70004-256">Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="70004-256">This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-257"><span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**\_propiedad PIN de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-257"><span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**NCRYPT\_PIN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-258">L "SmartCardPin"</span><span class="sxs-lookup"><span data-stu-id="70004-258">L"SmartCardPin"</span></span>
</dt> <dt>



<span data-ttu-id="70004-259">Puntero a una cadena Unicode terminada en null que contiene el código PIN.</span><span class="sxs-lookup"><span data-stu-id="70004-259">A pointer to a null-terminated Unicode string that contains the PIN.</span></span> <span data-ttu-id="70004-260">El PIN se usa para una clave de tarjeta inteligente o la contraseña de una clave protegida por contraseña almacenada en un KSP basado en software.</span><span class="sxs-lookup"><span data-stu-id="70004-260">The PIN is used for a smart card key or the password for a password-protected key stored in a software-based KSP.</span></span> <span data-ttu-id="70004-261">Esta propiedad solo se puede establecer.</span><span class="sxs-lookup"><span data-stu-id="70004-261">This property can only be set.</span></span> <span data-ttu-id="70004-262">Microsoft KSP almacenará en caché este valor para que el usuario solo se le solicite una vez por cada proceso.</span><span class="sxs-lookup"><span data-stu-id="70004-262">Microsoft KSPs will cache this value so that the user is only prompted once per process.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-263"><span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**\_propiedad de \_ identificador del proveedor NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-263"><span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**NCRYPT\_PROVIDER\_HANDLE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-264">L "identificador de proveedor"</span><span class="sxs-lookup"><span data-stu-id="70004-264">L"Provider Handle"</span></span>
</dt> <dt>



<span data-ttu-id="70004-265">**\_ \_ Identificador Prov de NCRYPT** que contiene el identificador del proveedor de almacenamiento de claves CNG.</span><span class="sxs-lookup"><span data-stu-id="70004-265">An **NCRYPT\_PROV\_HANDLE** that contains the handle of the CNG key storage provider.</span></span> <span data-ttu-id="70004-266">Cuando haya terminado de usar el identificador, debe llamar a [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) para liberarlo.</span><span class="sxs-lookup"><span data-stu-id="70004-266">When you are finished using the handle, you must call [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) to release it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-267"><span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**\_propiedad del lector NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-267"><span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**NCRYPT\_READER\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-268">L "SmartCardReader"</span><span class="sxs-lookup"><span data-stu-id="70004-268">L"SmartCardReader"</span></span>
</dt> <dt>



<span data-ttu-id="70004-269">Puntero a una cadena Unicode terminada en null que contiene el nombre del lector de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="70004-269">A pointer to a null-terminated Unicode string that contains the name of the smart card reader.</span></span> <span data-ttu-id="70004-270">Esta propiedad solo se puede establecer.</span><span class="sxs-lookup"><span data-stu-id="70004-270">This property can only be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-271"><span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**\_ \_ propiedad CERTSTORE raíz \_ NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="70004-271"><span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**NCRYPT\_ROOT\_CERTSTORE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-272">L "SmartcardRootCertStore"</span><span class="sxs-lookup"><span data-stu-id="70004-272">L"SmartcardRootCertStore"</span></span>
</dt> <dt>



<span data-ttu-id="70004-273">**HCERTSTORE** que representa el almacén de certificados raíz de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="70004-273">An **HCERTSTORE** that represents the smart card root certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-274"><span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCRYPT \_ identificador de \_ PIN \_ PPAC**</span><span class="sxs-lookup"><span data-stu-id="70004-274"><span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span> **NCRYPT\_SCARD\_PIN\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-275">L "SmartCardPinId"</span><span class="sxs-lookup"><span data-stu-id="70004-275">L"SmartCardPinId"</span></span>
</dt> <dt>



<span data-ttu-id="70004-276">Un puntero al valor **de \_ identificador de PIN** asociado a una [*clave criptográfica*](/windows/desktop/SecGloss/c-gly) determinada en una [*tarjeta inteligente*](/windows/desktop/SecGloss/s-gly).</span><span class="sxs-lookup"><span data-stu-id="70004-276">A pointer to the **PIN\_ID** value associated with a given [*cryptographic key*](/windows/desktop/SecGloss/c-gly) on a [*smart card*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="70004-277">Se trata de una propiedad de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="70004-277">This is a read-only property.</span></span> <span data-ttu-id="70004-278">El tipo de datos del **\_ identificador de PIN** se define en Cardmod. h.</span><span class="sxs-lookup"><span data-stu-id="70004-278">The **PIN\_ID** data type is defined in Cardmod.h.</span></span>

<span data-ttu-id="70004-279">**Windows Server 2008 y Windows Vista:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="70004-279">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-280"><span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**\_ \_ información del PIN PPAC (NCRYPT) \_**</span><span class="sxs-lookup"><span data-stu-id="70004-280"><span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**NCRYPT\_SCARD\_PIN\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-281">L "SmartCardPinInfo"</span><span class="sxs-lookup"><span data-stu-id="70004-281">L"SmartCardPinInfo"</span></span>
</dt> <dt>



<span data-ttu-id="70004-282">Un puntero a la estructura de [**\_ información**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) del PIN asociado a una clave criptográfica determinada en la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="70004-282">A pointer to [**PIN\_INFO**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) structure of the PIN associated with a given cryptographic key on the smart card.</span></span> <span data-ttu-id="70004-283">El autor de la llamada proporciona el identificador de clave.</span><span class="sxs-lookup"><span data-stu-id="70004-283">The caller provides the key handle.</span></span> <span data-ttu-id="70004-284">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="70004-284">This property is a read-only property.</span></span> <span data-ttu-id="70004-285">La estructura de **\_ información del PIN** se define en Cardmod. h.</span><span class="sxs-lookup"><span data-stu-id="70004-285">The **PIN\_INFO** structure is defined in Cardmod.h.</span></span>

<span data-ttu-id="70004-286">**Windows Server 2008 y Windows Vista:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="70004-286">**Windows Server 2008 and Windows Vista:** This value is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-287"><span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**\_propiedad de \_ PIN \_ seguro de NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="70004-287"><span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**NCRYPT\_SECURE\_PIN\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-288">L "SmartCardSecurePin"</span><span class="sxs-lookup"><span data-stu-id="70004-288">L"SmartCardSecurePin"</span></span>
</dt> <dt>



<span data-ttu-id="70004-289">Puntero a una cadena Unicode terminada en null que contiene el PIN de la sesión de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="70004-289">A pointer to a null-terminated Unicode string that contains the smart card session PIN.</span></span> <span data-ttu-id="70004-290">Esta propiedad solo se puede establecer.</span><span class="sxs-lookup"><span data-stu-id="70004-290">This property can only be set.</span></span>

<span data-ttu-id="70004-291">**Windows Vista:** Esta propiedad no se admite.</span><span class="sxs-lookup"><span data-stu-id="70004-291">**Windows Vista:** This property is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-292"><span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**\_propiedad de \_ Descripción de seguridad NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-292"><span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**NCRYPT\_SECURITY\_DESCR\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-293">L "Descripción de seguridad"</span><span class="sxs-lookup"><span data-stu-id="70004-293">L"Security Descr"</span></span>
</dt> <dt>



<span data-ttu-id="70004-294">Puntero a una estructura [**de \_ descriptores de seguridad**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) que contiene información de control de acceso para la clave.</span><span class="sxs-lookup"><span data-stu-id="70004-294">A pointer to a [**SECURITY\_DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) structure that contains access control information for the key.</span></span> <span data-ttu-id="70004-295">Esta propiedad solo se aplica a las claves persistentes.</span><span class="sxs-lookup"><span data-stu-id="70004-295">This property only applies to persistent keys.</span></span> <span data-ttu-id="70004-296">El parámetro *dwFlags* de la función [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) o [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) identifica la parte del descriptor de seguridad que se va a obtener o establecer.</span><span class="sxs-lookup"><span data-stu-id="70004-296">The *dwFlags* parameter of the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) or [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) function identifies the part of the security descriptor to get or set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-297"><span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**\_propiedad de \_ compatibilidad del Descr de seguridad NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="70004-297"><span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**NCRYPT\_SECURITY\_DESCR\_SUPPORT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-298">L "compatibilidad con el Descr de seguridad"</span><span class="sxs-lookup"><span data-stu-id="70004-298">L"Security Descr Support"</span></span>
</dt> <dt>



<span data-ttu-id="70004-299">Indica si el proveedor admite descriptores de seguridad para las claves.</span><span class="sxs-lookup"><span data-stu-id="70004-299">Indicates whether the provider supports security descriptors for keys.</span></span> <span data-ttu-id="70004-300">Esta propiedad es un **valor DWORD** que contiene 1 si el proveedor admite descriptores de seguridad para las claves.</span><span class="sxs-lookup"><span data-stu-id="70004-300">This property is a **DWORD** that contains 1 if the provider supports security descriptors for keys.</span></span> <span data-ttu-id="70004-301">Si esta propiedad contiene cualquier otro valor, o si la función [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) devuelve **NTE \_ not \_** Supported, el proveedor no admite descriptores de seguridad para las claves.</span><span class="sxs-lookup"><span data-stu-id="70004-301">If this property contains any other value, or if the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function returns **NTE\_NOT\_SUPPORTED**, then the provider does not support security descriptors for keys.</span></span> <span data-ttu-id="70004-302">Esta propiedad solo se aplica a los proveedores.</span><span class="sxs-lookup"><span data-stu-id="70004-302">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-303"><span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**\_propiedad GUID de tarjeta inteligente NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="70004-303"><span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**NCRYPT\_SMARTCARD\_GUID\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-304">L "SmartCardGuid"</span><span class="sxs-lookup"><span data-stu-id="70004-304">L"SmartCardGuid"</span></span>
</dt> <dt>



<span data-ttu-id="70004-305">Un BLOB que contiene el identificador de la tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="70004-305">A BLOB that contains the identifier of the smart card.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-306"><span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**propiedad de directiva de interfaz de \_ usuario NCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="70004-306"><span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**NCRYPT\_UI\_POLICY\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-307">L "Directiva de la interfaz de usuario"</span><span class="sxs-lookup"><span data-stu-id="70004-307">L"UI Policy"</span></span>
</dt> <dt>



<span data-ttu-id="70004-308">Si se usa con la función [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) o [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) , se trata de un puntero a una estructura de [**Directiva de \_ \_ interfaz**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) de usuario de NCRYPT que contiene la Directiva de interfaz de usuario de clave segura para la clave.</span><span class="sxs-lookup"><span data-stu-id="70004-308">If used with the [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) or [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function, this is a pointer to an [**NCRYPT\_UI\_POLICY**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) structure that contains the strong key user interface policy for the key.</span></span> <span data-ttu-id="70004-309">Esta propiedad solo se aplica a las claves persistentes.</span><span class="sxs-lookup"><span data-stu-id="70004-309">This property only applies to persistent keys.</span></span> <span data-ttu-id="70004-310">Esta propiedad solo se puede establecer cuando se genera la clave.</span><span class="sxs-lookup"><span data-stu-id="70004-310">This property can only be set when the key is being generated.</span></span> <span data-ttu-id="70004-311">Una vez que se ha llamado a la función [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) para esta clave, esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="70004-311">Once the [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) function has been called for this key, this property becomes read-only.</span></span>

<span data-ttu-id="70004-312">Un proveedor de almacenamiento de claves puede recibir este parámetro a través de una función de devolución de llamada [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) .</span><span class="sxs-lookup"><span data-stu-id="70004-312">A key storage provider can receive this parameter through an [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) callback function.</span></span> <span data-ttu-id="70004-313">El valor del parámetro es una \_ estructura de BLOB de directiva de interfaz de usuario NCRYPT \_ \_ que contiene la misma información.</span><span class="sxs-lookup"><span data-stu-id="70004-313">The parameter value is an NCRYPT\_UI\_POLICY\_BLOB structure that contains the same information.</span></span> <span data-ttu-id="70004-314">Del mismo modo, cuando una aplicación realiza una solicitud a través de NCryptSetPropertyFn al proveedor para devolver esta propiedad, se espera que el proveedor devuelva una \_ estructura de BLOB de directiva de interfaz de usuario NCRYPT \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="70004-314">Similarly, when an application makes a request through NCryptSetPropertyFn to the provider to return this property, the provider is expected to return an NCRYPT\_UI\_POLICY\_BLOB structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-315"><span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**\_ \_ propiedad nombre único de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-315"><span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**NCRYPT\_UNIQUE\_NAME\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-316">L "nombre único"</span><span class="sxs-lookup"><span data-stu-id="70004-316">L"Unique Name"</span></span>
</dt> <dt>



<span data-ttu-id="70004-317">Puntero a una cadena Unicode terminada en null que contiene el nombre único del objeto.</span><span class="sxs-lookup"><span data-stu-id="70004-317">A pointer to a null-terminated Unicode string that contains the unique name of the object.</span></span> <span data-ttu-id="70004-318">Se trata de un nombre alternativo que se puede usar al obtener acceso a la clave.</span><span class="sxs-lookup"><span data-stu-id="70004-318">This is an alternate name that can be used when accessing the key.</span></span> <span data-ttu-id="70004-319">Esta propiedad se usa cuando se considera que el nombre de clave que se pasó originalmente a [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) no es suficiente para identificar de forma confiable la clave persistente.</span><span class="sxs-lookup"><span data-stu-id="70004-319">This property is used when it is thought that the key name originally passed to [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) is not unique enough to reliably identify the persisted key.</span></span> <span data-ttu-id="70004-320">El proveedor de almacenamiento de claves de Microsoft devolverá el nombre de archivo de la clave como esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="70004-320">The Microsoft key storage provider will return the file name of the key as this property.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-321"><span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**\_propiedad de \_ contexto \_ use NCRYPT**</span><span class="sxs-lookup"><span data-stu-id="70004-321"><span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT\_USE\_CONTEXT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-322">L "usar contexto"</span><span class="sxs-lookup"><span data-stu-id="70004-322">L"Use Context"</span></span>
</dt> <dt>



<span data-ttu-id="70004-323">Puntero a una cadena Unicode terminada en null que describe el contexto de la operación.</span><span class="sxs-lookup"><span data-stu-id="70004-323">A pointer to a null-terminated Unicode string that describes the context of the operation.</span></span> <span data-ttu-id="70004-324">Esta propiedad no es persistente y se puede establecer en un proveedor o una clave.</span><span class="sxs-lookup"><span data-stu-id="70004-324">This property is not persistent and can be set on either a provider or a key.</span></span> <span data-ttu-id="70004-325">Una clave no tiene acceso a la propiedad **de \_ \_ \_ propiedad de contexto usar** el valor de NCRYPT del proveedor porque la propiedad solo es específica del identificador para el que se establece.</span><span class="sxs-lookup"><span data-stu-id="70004-325">A key does not have access to the **NCRYPT\_USE\_CONTEXT\_PROPERTY** property of the provider because the property is specific only to the handle it is set for.</span></span>

<span data-ttu-id="70004-326">Un ejemplo en el que esta propiedad se utilizaría en el contexto de un proveedor es un proveedor de almacenamiento de claves que necesita preguntar al usuario durante una llamada a [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (por ejemplo, "insertar la tarjeta inteligente en el lector").</span><span class="sxs-lookup"><span data-stu-id="70004-326">An example where this property would be used in the context of a provider is a key storage provider that needs to prompt the user during a call to [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (for example, "Insert your smart card in the reader.").</span></span> <span data-ttu-id="70004-327">Dado que el identificador de clave no está disponible hasta que **NCryptOpenKey** devuelve, la aplicación debe establecer esta propiedad en el identificador del proveedor antes de llamar a **NCryptOpenKey**.</span><span class="sxs-lookup"><span data-stu-id="70004-327">Because the key handle is not available until after **NCryptOpenKey** returns, the application should set this property on the provider handle prior to calling **NCryptOpenKey**.</span></span>

<span data-ttu-id="70004-328">Un ejemplo en el que esta propiedad se usaría en el contexto de un identificador de clave es un proveedor de almacenamiento de claves que necesita preguntar al usuario durante una operación con la clave (por ejemplo, "esta aplicación necesita usar esta clave para firmar un documento").</span><span class="sxs-lookup"><span data-stu-id="70004-328">An example where this property would be used in the context of a key handle is a key storage provider that needs to prompt the user during an operation using the key (for example, "This application needs to use this key to sign a document.").</span></span> <span data-ttu-id="70004-329">Después, el proveedor puede retransmitir esta información de contexto al usuario en cualquier interfaz de usuario que se muestra durante la operación.</span><span class="sxs-lookup"><span data-stu-id="70004-329">The provider could then relay this context information to the user in any user interface shown during the operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-330"><span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**\_propiedad de recuento de uso de NCRYPT \_ \_ habilitado \_**</span><span class="sxs-lookup"><span data-stu-id="70004-330"><span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**NCRYPT\_USE\_COUNT\_ENABLED\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-331">L "recuento de uso habilitado"</span><span class="sxs-lookup"><span data-stu-id="70004-331">L"Enabled Use Count"</span></span>
</dt> <dt>



<span data-ttu-id="70004-332">Indica si el proveedor admite el recuento de uso de claves.</span><span class="sxs-lookup"><span data-stu-id="70004-332">Indicates whether the provider supports usage counting for keys.</span></span> <span data-ttu-id="70004-333">Esta propiedad es un **valor DWORD** que contiene 1 si el proveedor admite el recuento de uso de claves.</span><span class="sxs-lookup"><span data-stu-id="70004-333">This property is a **DWORD** that contains 1 if the provider supports usage counting for keys.</span></span> <span data-ttu-id="70004-334">Si esta propiedad contiene cualquier otro valor, o si la función [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) devuelve **NTE \_ not \_** Supported, el proveedor no admite el recuento de uso de las claves.</span><span class="sxs-lookup"><span data-stu-id="70004-334">If this property contains any other value, or if the [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) function returns **NTE\_NOT\_SUPPORTED**, then the provider does not support usage counting for keys.</span></span> <span data-ttu-id="70004-335">Esta propiedad solo se aplica a los proveedores.</span><span class="sxs-lookup"><span data-stu-id="70004-335">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-336"><span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**\_propiedad de \_ recuento de uso de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-336"><span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**NCRYPT\_USE\_COUNT\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-337">L "recuento de uso"</span><span class="sxs-lookup"><span data-stu-id="70004-337">L"Use Count"</span></span>
</dt> <dt>



<span data-ttu-id="70004-338">Una variable de [**\_ entero ULARGE**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) que contiene el número de operaciones que ha realizado la [*clave privada*](/windows/desktop/SecGloss/p-gly) especificada.</span><span class="sxs-lookup"><span data-stu-id="70004-338">A [**ULARGE\_INTEGER**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) variable that contains the number of operations that the specified [*private key*](/windows/desktop/SecGloss/p-gly) has performed.</span></span> <span data-ttu-id="70004-339">Esta propiedad es opcional y es posible que no sea compatible con todos los proveedores.</span><span class="sxs-lookup"><span data-stu-id="70004-339">This property is optional and may not be supported by all providers.</span></span> <span data-ttu-id="70004-340">Los proveedores que admiten esta propiedad en las claves deben admitir también la propiedad de **\_ propiedad de recuento de uso de NCRYPT \_ \_ habilitada \_** en el identificador del proveedor.</span><span class="sxs-lookup"><span data-stu-id="70004-340">Providers that support this property on keys should also support the **NCRYPT\_USE\_COUNT\_ENABLED\_PROPERTY** property on the provider handle.</span></span> <span data-ttu-id="70004-341">El proveedor de almacenamiento de claves de Microsoft no admite esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="70004-341">The Microsoft key storage provider does not support this property.</span></span> <span data-ttu-id="70004-342">Esta propiedad solo se aplica a las claves persistentes.</span><span class="sxs-lookup"><span data-stu-id="70004-342">This property only applies to persistent keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-343"><span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**\_ \_ propiedad CERTSTORE de usuario de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-343"><span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**NCRYPT\_USER\_CERTSTORE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-344">L "SmartCardUserCertStore"</span><span class="sxs-lookup"><span data-stu-id="70004-344">L"SmartCardUserCertStore"</span></span>
</dt> <dt>



<span data-ttu-id="70004-345">Un **HCERTSTORE** que representa el almacén de certificados de usuario de tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="70004-345">An **HCERTSTORE** that represents the smart card user certificate store.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-346"><span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**\_propiedad versión de NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-346"><span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**NCRYPT\_VERSION\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-347">L "versión"</span><span class="sxs-lookup"><span data-stu-id="70004-347">L"Version"</span></span>
</dt> <dt>



<span data-ttu-id="70004-348">**DWORD** que contiene la versión de software del proveedor.</span><span class="sxs-lookup"><span data-stu-id="70004-348">A **DWORD** that contains the software version of the provider.</span></span> <span data-ttu-id="70004-349">La palabra alta contiene la versión principal y la palabra baja contiene la versión secundaria.</span><span class="sxs-lookup"><span data-stu-id="70004-349">The high word contains the major version and the low word contains the minor version.</span></span> <span data-ttu-id="70004-350">Por ejemplo, 0x00030033 = 3,51.</span><span class="sxs-lookup"><span data-stu-id="70004-350">For example, 0x00030033 = 3.51.</span></span> <span data-ttu-id="70004-351">Esta propiedad solo se aplica a los proveedores.</span><span class="sxs-lookup"><span data-stu-id="70004-351">This property only applies to providers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="70004-352"><span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**\_propiedad de \_ identificador de ventana NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="70004-352"><span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**NCRYPT\_WINDOW\_HANDLE\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="70004-353">L "identificador de HWND"</span><span class="sxs-lookup"><span data-stu-id="70004-353">L"HWND Handle"</span></span>
</dt> <dt>



<span data-ttu-id="70004-354">Puntero al identificador de ventana (**hWnd**) que se va a usar como elemento primario de cualquier interfaz de usuario que se muestre.</span><span class="sxs-lookup"><span data-stu-id="70004-354">A pointer to the window handle (**HWND**) to be used as the parent of any user interface that is displayed.</span></span>

<span data-ttu-id="70004-355">Dado que el comportamiento no deseado puede producirse cuando se muestra una interfaz de usuario mediante un identificador de ventana **nulo** para el elemento primario, se recomienda encarecidamente que un proveedor de almacenamiento de claves no muestre una interfaz de usuario a menos que se establezca esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="70004-355">Because undesirable behavior can happen when a user interface is shown by using a **NULL** window handle for the parent, we strongly recommend that a key storage provider not display a user interface unless this property is set.</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="70004-356">Los valores siguientes se usan para definir los límites de los datos de propiedad.</span><span class="sxs-lookup"><span data-stu-id="70004-356">The following values are used to define limits of property data.</span></span>



| <span data-ttu-id="70004-357">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="70004-357">Constant/value</span></span>                                                                                                                                                                                                                                                 | <span data-ttu-id="70004-358">Descripción</span><span class="sxs-lookup"><span data-stu-id="70004-358">Description</span></span>                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <span data-ttu-id="70004-359"><dt>**NCRYPT \_ Longitud máxima de \_ \_ datos de propiedad**</dt> <dt>0x100000</dt></span><span class="sxs-lookup"><span data-stu-id="70004-359"><dt>**NCRYPT\_MAX\_PROPERTY\_DATA**</dt> <dt>0x100000</dt></span></span> </dl> | <span data-ttu-id="70004-360">Especifica el tamaño máximo de un valor de propiedad, en bytes.</span><span class="sxs-lookup"><span data-stu-id="70004-360">Specifies the maximum size of a property value, in bytes.</span></span><br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <span data-ttu-id="70004-361"><dt>**NCRYPT \_ \_ \_ Nombre de propiedad Max**</dt> <dt>64</dt></span><span class="sxs-lookup"><span data-stu-id="70004-361"><dt>**NCRYPT\_MAX\_PROPERTY\_NAME**</dt> <dt>64</dt></span></span> </dl>       | <span data-ttu-id="70004-362">Especifica el tamaño máximo de un nombre de propiedad, en caracteres.</span><span class="sxs-lookup"><span data-stu-id="70004-362">Specifies the maximum size of a property name, in characters.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="70004-363">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70004-363">Requirements</span></span>



| <span data-ttu-id="70004-364">Requisito</span><span class="sxs-lookup"><span data-stu-id="70004-364">Requirement</span></span> | <span data-ttu-id="70004-365">Value</span><span class="sxs-lookup"><span data-stu-id="70004-365">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="70004-366">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70004-366">Minimum supported client</span></span><br/> | <span data-ttu-id="70004-367">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="70004-367">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="70004-368">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70004-368">Minimum supported server</span></span><br/> | <span data-ttu-id="70004-369">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="70004-369">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="70004-370">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70004-370">Header</span></span><br/>                   | <dl> <span data-ttu-id="70004-371"><dt>Ncrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="70004-371"><dt>Ncrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70004-372">Vea también</span><span class="sxs-lookup"><span data-stu-id="70004-372">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70004-373">**NCryptGetProperty**</span><span class="sxs-lookup"><span data-stu-id="70004-373">**NCryptGetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[<span data-ttu-id="70004-374">**NCryptSetProperty**</span><span class="sxs-lookup"><span data-stu-id="70004-374">**NCryptSetProperty**</span></span>](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 

