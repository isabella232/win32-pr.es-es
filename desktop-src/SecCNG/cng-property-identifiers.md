---
description: Se usa con las funciones BCryptGetProperty y BCryptSetProperty para identificar una propiedad.
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: Identificadores de propiedad primitiva de criptografía (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f4996a216fbc4fbf63216f99b5f630c4769e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907651"
---
# <a name="cryptography-primitive-property-identifiers"></a><span data-ttu-id="2389d-103">Identificadores de propiedad primitiva de criptografía</span><span class="sxs-lookup"><span data-stu-id="2389d-103">Cryptography Primitive Property Identifiers</span></span>

<span data-ttu-id="2389d-104">Los valores siguientes se usan con las funciones [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) y [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) para identificar una propiedad.</span><span class="sxs-lookup"><span data-stu-id="2389d-104">The following values are used with the [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) and [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) functions to identify a property.</span></span>

<dl> <dt>

<span data-ttu-id="2389d-105"><span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**\_nombre del algoritmo BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-105"><span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**BCRYPT\_ALGORITHM\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-106">L "AlgorithmName"</span><span class="sxs-lookup"><span data-stu-id="2389d-106">L"AlgorithmName"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-107">Una cadena Unicode terminada en null que contiene el nombre del algoritmo.</span><span class="sxs-lookup"><span data-stu-id="2389d-107">A null-terminated Unicode string that contains the name of the algorithm.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-108"><span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**\_longitud de \_ etiqueta de autenticación de BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-108"><span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**BCRYPT\_AUTH\_TAG\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-109">L "AuthTagLength"</span><span class="sxs-lookup"><span data-stu-id="2389d-109">L"AuthTagLength"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-110">Longitudes de las etiquetas de autenticación admitidas por el algoritmo.</span><span class="sxs-lookup"><span data-stu-id="2389d-110">The authentication tag lengths that are supported by the algorithm.</span></span> <span data-ttu-id="2389d-111">Esta propiedad es una estructura de [**struct de longitud de \_ etiquetas de autenticación \_ \_ \_ BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) .</span><span class="sxs-lookup"><span data-stu-id="2389d-111">This property is a [**BCRYPT\_AUTH\_TAG\_LENGTHS\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) structure.</span></span> <span data-ttu-id="2389d-112">Esta propiedad solo se aplica a los algoritmos.</span><span class="sxs-lookup"><span data-stu-id="2389d-112">This property only applies to algorithms.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-113"><span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**\_longitud del bloque BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-113"><span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**BCRYPT\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-114">L "BlockLength"</span><span class="sxs-lookup"><span data-stu-id="2389d-114">L"BlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-115">Tamaño, en bytes, de un bloque de cifrado para el algoritmo.</span><span class="sxs-lookup"><span data-stu-id="2389d-115">The size, in bytes, of a cipher block for the algorithm.</span></span> <span data-ttu-id="2389d-116">Esta propiedad solo se aplica a los algoritmos de cifrado de bloques.</span><span class="sxs-lookup"><span data-stu-id="2389d-116">This property only applies to block cipher algorithms.</span></span> <span data-ttu-id="2389d-117">Este tipo de datos es un **valor DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2389d-117">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-118"><span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**\_lista de \_ tamaños de bloque BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-118"><span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**BCRYPT\_BLOCK\_SIZE\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-119">L "BlockSizeList"</span><span class="sxs-lookup"><span data-stu-id="2389d-119">L"BlockSizeList"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-120">Una lista de las longitudes de bloque que admite un algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="2389d-120">A list of the block lengths supported by an encryption algorithm.</span></span> <span data-ttu-id="2389d-121">Este tipo de datos es una matriz de **DWords**.</span><span class="sxs-lookup"><span data-stu-id="2389d-121">This data type is an array of **DWORDs**.</span></span> <span data-ttu-id="2389d-122">El número de elementos de la matriz se puede determinar dividiendo el número de bytes recuperados por el tamaño de un único **DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2389d-122">The number of elements in the array can be determined by dividing the number of bytes retrieved by the size of a single **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-123"><span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**\_modo de encadenamiento BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-123"><span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**BCRYPT\_CHAINING\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-124">L "ChainingMode"</span><span class="sxs-lookup"><span data-stu-id="2389d-124">L"ChainingMode"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-125">Puntero a una cadena Unicode terminada en null que representa el modo de encadenamiento del algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="2389d-125">A pointer to a null-terminated Unicode string that represents the chaining mode of the encryption algorithm.</span></span> <span data-ttu-id="2389d-126">Esta propiedad se puede establecer en un identificador de algoritmo o en un identificador de clave para uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2389d-126">This property can be set on an algorithm handle or a key handle to one of the following values.</span></span>



| <span data-ttu-id="2389d-127">Identificador</span><span class="sxs-lookup"><span data-stu-id="2389d-127">Identifier</span></span>                   | <span data-ttu-id="2389d-128">Value</span><span class="sxs-lookup"><span data-stu-id="2389d-128">Value</span></span>                         | <span data-ttu-id="2389d-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="2389d-129">Description</span></span>                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2389d-130">**\_modo de cadena BCRYPT \_ \_ CBC**</span><span class="sxs-lookup"><span data-stu-id="2389d-130">**BCRYPT\_CHAIN\_MODE\_CBC**</span></span> | <span data-ttu-id="2389d-131">L "ChainingModeCBC"</span><span class="sxs-lookup"><span data-stu-id="2389d-131">L"ChainingModeCBC"</span></span><br/> | <span data-ttu-id="2389d-132">Establece el modo de encadenamiento del algoritmo en el [*encadenamiento de bloques de cifrado*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="2389d-132">Sets the algorithm's chaining mode to [*cipher block chaining*](/windows/desktop/SecGloss/c-gly).</span></span><br/>            |
| <span data-ttu-id="2389d-133">**\_CCM del \_ modo de cadena BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-133">**BCRYPT\_CHAIN\_MODE\_CCM**</span></span> | <span data-ttu-id="2389d-134">L "ChainingModeCCM"</span><span class="sxs-lookup"><span data-stu-id="2389d-134">L"ChainingModeCCM"</span></span><br/> | <span data-ttu-id="2389d-135">Establece el modo de encadenamiento del algoritmo en el modo CBC-MAC (CCM). **Windows Vista:** Este valor se admite a partir de Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="2389d-135">Sets the algorithm's chaining mode to counter with CBC-MAC mode (CCM).**Windows Vista:** This value is supported beginning with Windows Vista with SP1.</span></span><br/> <br/> |
| <span data-ttu-id="2389d-136">**\_modo de cadena BCRYPT \_ \_ CFB**</span><span class="sxs-lookup"><span data-stu-id="2389d-136">**BCRYPT\_CHAIN\_MODE\_CFB**</span></span> | <span data-ttu-id="2389d-137">L "ChainingModeCFB"</span><span class="sxs-lookup"><span data-stu-id="2389d-137">L"ChainingModeCFB"</span></span><br/> | <span data-ttu-id="2389d-138">Establece el modo de encadenamiento del algoritmo en los [*comentarios de cifrado*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="2389d-138">Sets the algorithm's chaining mode to [*cipher feedback*](/windows/desktop/SecGloss/c-gly).</span></span><br/>                              |
| <span data-ttu-id="2389d-139">**\_ECB del \_ modo de cadena BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-139">**BCRYPT\_CHAIN\_MODE\_ECB**</span></span> | <span data-ttu-id="2389d-140">L "ChainingModeECB"</span><span class="sxs-lookup"><span data-stu-id="2389d-140">L"ChainingModeECB"</span></span><br/> | <span data-ttu-id="2389d-141">Establece el modo de encadenamiento del algoritmo en [*Electronic Codebook*](/windows/desktop/SecGloss/e-gly).</span><span class="sxs-lookup"><span data-stu-id="2389d-141">Sets the algorithm's chaining mode to [*electronic codebook*](/windows/desktop/SecGloss/e-gly).</span></span><br/>                  |
| <span data-ttu-id="2389d-142">**\_modo de cadena BCRYPT \_ \_ GCM**</span><span class="sxs-lookup"><span data-stu-id="2389d-142">**BCRYPT\_CHAIN\_MODE\_GCM**</span></span> | <span data-ttu-id="2389d-143">L "ChainingModeGCM"</span><span class="sxs-lookup"><span data-stu-id="2389d-143">L"ChainingModeGCM"</span></span><br/> | <span data-ttu-id="2389d-144">Establece el modo de encadenamiento del algoritmo en el modo de Galois/contador (GCM). **Windows Vista:** Este valor se admite a partir de Windows Vista con SP1.</span><span class="sxs-lookup"><span data-stu-id="2389d-144">Sets the algorithm's chaining mode to Galois/counter mode (GCM).**Windows Vista:** This value is supported beginning with Windows Vista with SP1.</span></span><br/> <br/>       |
| <span data-ttu-id="2389d-145">**\_modo de cadena BCRYPT \_ \_ na**</span><span class="sxs-lookup"><span data-stu-id="2389d-145">**BCRYPT\_CHAIN\_MODE\_NA**</span></span>  | <span data-ttu-id="2389d-146">L "ChainingModeN/A"</span><span class="sxs-lookup"><span data-stu-id="2389d-146">L"ChainingModeN/A"</span></span><br/> | <span data-ttu-id="2389d-147">El algoritmo no admite el encadenamiento.</span><span class="sxs-lookup"><span data-stu-id="2389d-147">The algorithm does not support chaining.</span></span><br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-148"><span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**\_parámetros DH de BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-148"><span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**BCRYPT\_DH\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-149">L "DHParameters"</span><span class="sxs-lookup"><span data-stu-id="2389d-149">L"DHParameters"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-150">Especifica los parámetros que se van a usar con una clave de Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="2389d-150">Specifies parameters to use with a Diffie-Hellman key.</span></span> <span data-ttu-id="2389d-151">Este tipo de datos es un puntero a una estructura de [**\_ encabezado de \_ parámetro \_ de BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="2389d-151">This data type is a pointer to a [**BCRYPT\_DH\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) structure.</span></span> <span data-ttu-id="2389d-152">Esta propiedad solo se puede establecer y debe establecerse para la clave antes de que se complete la clave.</span><span class="sxs-lookup"><span data-stu-id="2389d-152">This property can only be set and must be set for the key before the key is completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-153"><span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**\_parámetros DSA de BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-153"><span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**BCRYPT\_DSA\_PARAMETERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-154">L "DSAParameters"</span><span class="sxs-lookup"><span data-stu-id="2389d-154">L"DSAParameters"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-155">Especifica los parámetros que se van a usar con una clave DSA.</span><span class="sxs-lookup"><span data-stu-id="2389d-155">Specifies parameters to use with a DSA key.</span></span> <span data-ttu-id="2389d-156">Esta propiedad es un [**\_ encabezado de \_ parámetro \_ DSA de bcrypt**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) o una estructura de [**encabezado del \_ parámetro DSA de bcrypt \_ \_ \_ V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) .</span><span class="sxs-lookup"><span data-stu-id="2389d-156">This property is a [**BCRYPT\_DSA\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) or a [**BCRYPT\_DSA\_PARAMETER\_HEADER\_V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) structure.</span></span> <span data-ttu-id="2389d-157">Esta propiedad solo se puede establecer y debe establecerse para la clave antes de que se complete la clave.</span><span class="sxs-lookup"><span data-stu-id="2389d-157">This property can only be set and must be set for the key before the key is completed.</span></span>

<span data-ttu-id="2389d-158">**Windows 8:** A partir de Windows 8, esta propiedad puede ser una estructura de [**\_ encabezado del parámetro DSA de BCRYPT \_ \_ \_ V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) .</span><span class="sxs-lookup"><span data-stu-id="2389d-158">**Windows 8:** Beginning with Windows 8, this property can be a [**BCRYPT\_DSA\_PARAMETER\_HEADER\_V2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) structure.</span></span> <span data-ttu-id="2389d-159">Use esta estructura si el tamaño de clave supera los 1024 bits y es menor o igual que 3072 bits.</span><span class="sxs-lookup"><span data-stu-id="2389d-159">Use this structure if the key size exceeds 1024 bits and is less than or equal to 3072 bits.</span></span> <span data-ttu-id="2389d-160">Si el tamaño de la clave es mayor o igual que 512 pero menor o igual que 1024 bits, use la estructura de [**\_ \_ \_ encabezado del parámetro DSA de BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) .</span><span class="sxs-lookup"><span data-stu-id="2389d-160">If the key size is greater than or equal to 512 but less than or equal to 1024 bits, use the [**BCRYPT\_DSA\_PARAMETER\_HEADER**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) structure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-161"><span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**\_longitud de \_ clave \_ efectiva BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="2389d-161"><span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**BCRYPT\_EFFECTIVE\_KEY\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-162">L "EffectiveKeyLength"</span><span class="sxs-lookup"><span data-stu-id="2389d-162">L"EffectiveKeyLength"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-163">Tamaño, en bits, de la longitud efectiva de una clave RC2.</span><span class="sxs-lookup"><span data-stu-id="2389d-163">The size, in bits, of the effective length of an RC2 key.</span></span> <span data-ttu-id="2389d-164">Este tipo de datos es un **valor DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2389d-164">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-165"><span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**\_longitud del \_ bloque \_ hash de BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="2389d-165"><span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**BCRYPT\_HASH\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-166">L "HashBlockLength"</span><span class="sxs-lookup"><span data-stu-id="2389d-166">L"HashBlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-167">Tamaño, en bytes, del bloque de un valor hash.</span><span class="sxs-lookup"><span data-stu-id="2389d-167">The size, in bytes, of the block for a hash.</span></span> <span data-ttu-id="2389d-168">Esta propiedad solo se aplica a los algoritmos hash.</span><span class="sxs-lookup"><span data-stu-id="2389d-168">This property only applies to hash algorithms.</span></span> <span data-ttu-id="2389d-169">Este tipo de datos es un **valor DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2389d-169">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-170"><span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**\_longitud del hash de BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-170"><span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**BCRYPT\_HASH\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-171">L "HashDigestLength"</span><span class="sxs-lookup"><span data-stu-id="2389d-171">L"HashDigestLength"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-172">Tamaño, en bytes, del valor hash de un proveedor hash.</span><span class="sxs-lookup"><span data-stu-id="2389d-172">The size, in bytes, of the hash value of a hash provider.</span></span> <span data-ttu-id="2389d-173">Este tipo de datos es un **valor DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2389d-173">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-174"><span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**\_lista de \_ OID \_ hash de BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="2389d-174"><span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**BCRYPT\_HASH\_OID\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-175">L "HashOIDList"</span><span class="sxs-lookup"><span data-stu-id="2389d-175">L"HashOIDList"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-176">Lista de [*identificadores de objeto*](/windows/desktop/SecGloss/o-gly) hash (OID) con codificación [*der*](/windows/desktop/SecGloss/d-gly).</span><span class="sxs-lookup"><span data-stu-id="2389d-176">The list of [*DER*](/windows/desktop/SecGloss/d-gly)-encoded hashing [*object identifiers*](/windows/desktop/SecGloss/o-gly) (OIDs).</span></span> <span data-ttu-id="2389d-177">Esta propiedad es una estructura de [**\_ \_ lista de OID de BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) .</span><span class="sxs-lookup"><span data-stu-id="2389d-177">This property is a [**BCRYPT\_OID\_LIST**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) structure.</span></span> <span data-ttu-id="2389d-178">Esta propiedad solo se puede leer.</span><span class="sxs-lookup"><span data-stu-id="2389d-178">This property can only be read.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-179"><span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**\_Vector de inicialización de BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-179"><span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**BCRYPT\_INITIALIZATION\_VECTOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-180">L "IV"</span><span class="sxs-lookup"><span data-stu-id="2389d-180">L"IV"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-181">Contiene el [*Vector de inicialización*](/windows/desktop/SecGloss/i-gly) (IV) para una clave.</span><span class="sxs-lookup"><span data-stu-id="2389d-181">Contains the [*initialization vector*](/windows/desktop/SecGloss/i-gly) (IV) for a key.</span></span> <span data-ttu-id="2389d-182">Esta propiedad solo se aplica a las claves.</span><span class="sxs-lookup"><span data-stu-id="2389d-182">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-183"><span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**longitud de la \_ clave BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-183"><span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**BCRYPT\_KEY\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-184">L "KeyLength"</span><span class="sxs-lookup"><span data-stu-id="2389d-184">L"KeyLength"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-185">Tamaño, en bits, del valor de clave de un proveedor de claves simétricas.</span><span class="sxs-lookup"><span data-stu-id="2389d-185">The size, in bits, of the key value of a symmetric key provider.</span></span> <span data-ttu-id="2389d-186">Este tipo de datos es un **valor DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2389d-186">This data type is a **DWORD**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-187"><span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**\_longitudes de clave de BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-187"><span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**BCRYPT\_KEY\_LENGTHS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-188">L "KeyLengths"</span><span class="sxs-lookup"><span data-stu-id="2389d-188">L"KeyLengths"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-189">Longitudes de clave admitidas por el algoritmo.</span><span class="sxs-lookup"><span data-stu-id="2389d-189">The key lengths that are supported by the algorithm.</span></span> <span data-ttu-id="2389d-190">Esta propiedad es una estructura de [**\_ \_ \_ struct de longitudes de clave BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) .</span><span class="sxs-lookup"><span data-stu-id="2389d-190">This property is a [**BCRYPT\_KEY\_LENGTHS\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) structure.</span></span> <span data-ttu-id="2389d-191">Esta propiedad solo se aplica a los algoritmos.</span><span class="sxs-lookup"><span data-stu-id="2389d-191">This property only applies to algorithms.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-192"><span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**\_longitud del \_ objeto de clave BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-192"><span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**BCRYPT\_KEY\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-193">L "KeyObjectLength"</span><span class="sxs-lookup"><span data-stu-id="2389d-193">L"KeyObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-194">No se usa esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="2389d-194">This property is not used.</span></span> <span data-ttu-id="2389d-195">La propiedad de **\_ \_ longitud del objeto BCRYPT** se usa para obtener esta información.</span><span class="sxs-lookup"><span data-stu-id="2389d-195">The **BCRYPT\_OBJECT\_LENGTH** property is used to obtain this information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-196"><span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**\_nivel de clave BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-196"><span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**BCRYPT\_KEY\_STRENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-197">L "KeyStrength"</span><span class="sxs-lookup"><span data-stu-id="2389d-197">L"KeyStrength"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-198">Número de bits de la clave.</span><span class="sxs-lookup"><span data-stu-id="2389d-198">The number of bits in the key.</span></span> <span data-ttu-id="2389d-199">Este tipo de datos es un **valor DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2389d-199">This data type is a **DWORD**.</span></span> <span data-ttu-id="2389d-200">Esta propiedad solo se aplica a las claves.</span><span class="sxs-lookup"><span data-stu-id="2389d-200">This property only applies to keys.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-201"><span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**\_longitud del \_ bloque de mensajes BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-201"><span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**BCRYPT\_MESSAGE\_BLOCK\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-202">L "MessageBlockLength"</span><span class="sxs-lookup"><span data-stu-id="2389d-202">L"MessageBlockLength"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-203">Se puede establecer en cualquier identificador de clave que tenga establecido el modo de encadenamiento CFB.</span><span class="sxs-lookup"><span data-stu-id="2389d-203">This can be set on any key handle that has the CFB chaining mode set.</span></span> <span data-ttu-id="2389d-204">De forma predeterminada, esta propiedad se establece en 1 para CFB de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="2389d-204">By default, this property is set to 1 for 8-bit CFB.</span></span> <span data-ttu-id="2389d-205">Si se establece en el tamaño de bloque en bytes, se usará CFB de bloque completo.</span><span class="sxs-lookup"><span data-stu-id="2389d-205">Setting it to the block size in bytes causes full-block CFB to be used.</span></span> <span data-ttu-id="2389d-206">En el caso de las claves XTS, se usa para establecer el tamaño, en bytes, de la unidad de datos XTS (normalmente 512 o 4096).</span><span class="sxs-lookup"><span data-stu-id="2389d-206">For XTS keys it is used to set the size, in bytes, of the XTS Data Unit (commonly 512 or 4096).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-207"><span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**\_longitud de varios \_ objetos \_ BCRYPT**</span><span class="sxs-lookup"><span data-stu-id="2389d-207"><span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**BCRYPT\_MULTI\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-208">L "MultiObjectLength"</span><span class="sxs-lookup"><span data-stu-id="2389d-208">L"MultiObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-209">Esta propiedad devuelve una [**\_ estructura de \_ \_ longitud \_ de varios objetos BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), que contiene la información necesaria para calcular el tamaño de un búfer de objetos.</span><span class="sxs-lookup"><span data-stu-id="2389d-209">This property returns a [**BCRYPT\_MULTI\_OBJECT\_LENGTH\_STRUCT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct), which contains information necessary to calculate the size of an object buffer.</span></span> <span data-ttu-id="2389d-210">Esta propiedad solo se admite en las versiones de sistema operativo que admiten la función [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) .</span><span class="sxs-lookup"><span data-stu-id="2389d-210">This property is only supported on operating system versions that support the [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) function.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-211"><span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**\_longitud del objeto BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-211"><span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**BCRYPT\_OBJECT\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-212">L "ObjectLength"</span><span class="sxs-lookup"><span data-stu-id="2389d-212">L"ObjectLength"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-213">Tamaño, en bytes, del subobjeto de un proveedor.</span><span class="sxs-lookup"><span data-stu-id="2389d-213">The size, in bytes, of the subobject of a provider.</span></span> <span data-ttu-id="2389d-214">Este tipo de datos es un **valor DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2389d-214">This data type is a **DWORD**.</span></span> <span data-ttu-id="2389d-215">Actualmente, los proveedores de algoritmos hash y algoritmos de cifrado simétrico utilizan búferes asignados por el autor de la llamada para almacenar sus subobjetos.</span><span class="sxs-lookup"><span data-stu-id="2389d-215">Currently, the hash and symmetric cipher algorithm providers use caller-allocated buffers to store their subobjects.</span></span> <span data-ttu-id="2389d-216">Por ejemplo, el proveedor hash requiere que asigne memoria para el objeto hash obtenido con la función [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) .</span><span class="sxs-lookup"><span data-stu-id="2389d-216">For example, the hash provider requires you to allocate memory for the hash object obtained with the [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) function.</span></span> <span data-ttu-id="2389d-217">Esta propiedad proporciona el tamaño de búfer para el objeto de un proveedor, de modo que pueda asignar memoria para el objeto creado por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="2389d-217">This property provides the buffer size for a provider's object so you can allocate memory for the object created by the provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-218"><span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**\_esquemas de relleno de BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-218"><span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**BCRYPT\_PADDING\_SCHEMES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-219">L "PaddingSchemes"</span><span class="sxs-lookup"><span data-stu-id="2389d-219">L"PaddingSchemes"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-220">Representa el esquema de relleno del proveedor de algoritmos RSA.</span><span class="sxs-lookup"><span data-stu-id="2389d-220">Represents the padding scheme of the RSA algorithm provider.</span></span> <span data-ttu-id="2389d-221">Este tipo de datos es un **valor DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2389d-221">This data type is a **DWORD**.</span></span> <span data-ttu-id="2389d-222">Puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="2389d-222">This can be one of the following values.</span></span>



| <span data-ttu-id="2389d-223">Identificador</span><span class="sxs-lookup"><span data-stu-id="2389d-223">Identifier</span></span>                             | <span data-ttu-id="2389d-224">Value</span><span class="sxs-lookup"><span data-stu-id="2389d-224">Value</span></span>      | <span data-ttu-id="2389d-225">Descripción</span><span class="sxs-lookup"><span data-stu-id="2389d-225">Description</span></span>                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| <span data-ttu-id="2389d-226">**el \_ \_ enrutador de controlador compatible con BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-226">**BCRYPT\_SUPPORTED\_PAD\_ROUTER**</span></span>     | <span data-ttu-id="2389d-227">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2389d-227">0x00000001</span></span> | <span data-ttu-id="2389d-228">El proveedor admite el relleno agregado por el enrutador.</span><span class="sxs-lookup"><span data-stu-id="2389d-228">The provider supports padding added by the router.</span></span>         |
| <span data-ttu-id="2389d-229">**El \_ controlador compatible con BCRYPT \_ \_ PKCS1 \_ enc**</span><span class="sxs-lookup"><span data-stu-id="2389d-229">**BCRYPT\_SUPPORTED\_PAD\_PKCS1\_ENC**</span></span> | <span data-ttu-id="2389d-230">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2389d-230">0x00000002</span></span> | <span data-ttu-id="2389d-231">El proveedor admite el esquema de relleno de cifrado PKCS1.</span><span class="sxs-lookup"><span data-stu-id="2389d-231">The provider supports the PKCS1 encryption padding scheme.</span></span> |
| <span data-ttu-id="2389d-232">**BCRYPT \_ compatible con la \_ almohadilla \_ PKCS1 \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-232">**BCRYPT\_SUPPORTED\_PAD\_PKCS1\_SIG**</span></span> | <span data-ttu-id="2389d-233">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2389d-233">0x00000004</span></span> | <span data-ttu-id="2389d-234">El proveedor admite el esquema de relleno de firmas PKCS1.</span><span class="sxs-lookup"><span data-stu-id="2389d-234">The provider supports the PKCS1 signature padding scheme.</span></span>  |
| <span data-ttu-id="2389d-235">**se \_ admitía el \_ panel \_ OAEP**</span><span class="sxs-lookup"><span data-stu-id="2389d-235">**BCRYPT\_SUPPORTED\_PAD\_OAEP**</span></span>       | <span data-ttu-id="2389d-236">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2389d-236">0x00000008</span></span> | <span data-ttu-id="2389d-237">El proveedor admite el esquema de relleno OAEP.</span><span class="sxs-lookup"><span data-stu-id="2389d-237">The provider supports the OAEP padding scheme.</span></span>             |
| <span data-ttu-id="2389d-238">**\_controlador compatible con BCRYPT \_ \_ PSS**</span><span class="sxs-lookup"><span data-stu-id="2389d-238">**BCRYPT\_SUPPORTED\_PAD\_PSS**</span></span>        | <span data-ttu-id="2389d-239">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2389d-239">0x00000010</span></span> | <span data-ttu-id="2389d-240">El proveedor admite el esquema de relleno de PSS.</span><span class="sxs-lookup"><span data-stu-id="2389d-240">The provider supports the PSS padding scheme.</span></span>              |



 


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-241"><span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**\_identificador del proveedor de BCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-241"><span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**BCRYPT\_PROVIDER\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-242">L "ProviderHandle"</span><span class="sxs-lookup"><span data-stu-id="2389d-242">L"ProviderHandle"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-243">Identificador del proveedor de CNG que creó el objeto pasado en el parámetro *hObject* .</span><span class="sxs-lookup"><span data-stu-id="2389d-243">The handle of the CNG provider that created the object passed in the *hObject* parameter.</span></span> <span data-ttu-id="2389d-244">Este tipo de datos es **un \_ \_ identificador ALG de BCRYPT**.</span><span class="sxs-lookup"><span data-stu-id="2389d-244">This data type is a **BCRYPT\_ALG\_HANDLE**.</span></span> <span data-ttu-id="2389d-245">Esta propiedad solo se puede recuperar; no se puede establecer.</span><span class="sxs-lookup"><span data-stu-id="2389d-245">This property can only be retrieved; it cannot be set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="2389d-246"><span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**longitud de la firma de BCRYPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2389d-246"><span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**BCRYPT\_SIGNATURE\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2389d-247">L "SignatureLength"</span><span class="sxs-lookup"><span data-stu-id="2389d-247">L"SignatureLength"</span></span>
</dt> <dt>



<span data-ttu-id="2389d-248">Tamaño, en bytes, de la longitud de una firma para una clave.</span><span class="sxs-lookup"><span data-stu-id="2389d-248">The size, in bytes, of the length of a signature for a key.</span></span> <span data-ttu-id="2389d-249">Este tipo de datos es un **valor DWORD**.</span><span class="sxs-lookup"><span data-stu-id="2389d-249">This data type is a **DWORD**.</span></span> <span data-ttu-id="2389d-250">Esta propiedad solo se aplica a las claves.</span><span class="sxs-lookup"><span data-stu-id="2389d-250">This property only applies to keys.</span></span> <span data-ttu-id="2389d-251">Esta propiedad solo se puede recuperar; no se puede establecer.</span><span class="sxs-lookup"><span data-stu-id="2389d-251">This property can only be retrieved; it cannot be set.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2389d-252">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2389d-252">Requirements</span></span>



| <span data-ttu-id="2389d-253">Requisito</span><span class="sxs-lookup"><span data-stu-id="2389d-253">Requirement</span></span> | <span data-ttu-id="2389d-254">Value</span><span class="sxs-lookup"><span data-stu-id="2389d-254">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2389d-255">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2389d-255">Minimum supported client</span></span><br/> | <span data-ttu-id="2389d-256">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2389d-256">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2389d-257">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2389d-257">Minimum supported server</span></span><br/> | <span data-ttu-id="2389d-258">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2389d-258">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2389d-259">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2389d-259">Header</span></span><br/>                   | <dl> <span data-ttu-id="2389d-260"><dt>Bcrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="2389d-260"><dt>Bcrypt.h</dt></span></span> </dl> |



 

