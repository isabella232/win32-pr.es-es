---
description: Contiene definiciones de términos de seguridad que comienzan por la letra B.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 2e570727-7da0-4e17-bf5d-6fe0e6aef65b
title: B (Glosario de seguridad)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40aedaebddb86ddf9f32a9a3d86cf4cf4a613642
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688174"
---
# <a name="b-security-glossary"></a><span data-ttu-id="103f2-103">B (Glosario de seguridad)</span><span class="sxs-lookup"><span data-stu-id="103f2-103">B (Security Glossary)</span></span>

<span data-ttu-id="103f2-104">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [o](o-gly.md) [p](p-gly.md) Q [R](r-gly.md) [s](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span><span class="sxs-lookup"><span data-stu-id="103f2-104">[A](a-gly.md) B [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [I](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z</span></span>

<dl> <dt>

<span data-ttu-id="103f2-105"><span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**autoridad de copia de seguridad**</span><span class="sxs-lookup"><span data-stu-id="103f2-105"><span id="_security_backup_authority_gly"></span><span id="_SECURITY_BACKUP_AUTHORITY_GLY"></span>**backup authority**</span></span>
</dt> <dd>

<span data-ttu-id="103f2-106">Aplicación de confianza que se ejecuta en un equipo seguro y que proporciona almacenamiento secundario para las claves de sesión de sus clientes.</span><span class="sxs-lookup"><span data-stu-id="103f2-106">A trusted application running on a secure computer that provides secondary storage for the session keys of its clients.</span></span> <span data-ttu-id="103f2-107">La autoridad de copia de seguridad almacena las claves de sesión como blobs de clave que se cifran con la clave pública de la entidad de seguridad.</span><span class="sxs-lookup"><span data-stu-id="103f2-107">The backup authority stores session keys as key BLOBs that are encrypted with the backup authority's public key.</span></span>

</dd> <dt>

<span data-ttu-id="103f2-108"><span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**tipo de contenido base**</span><span class="sxs-lookup"><span data-stu-id="103f2-108"><span id="_security_base_content_type_gly"></span><span id="_SECURITY_BASE_CONTENT_TYPE_GLY"></span>**base content type**</span></span>
</dt> <dd>

<span data-ttu-id="103f2-109">Un tipo de datos contenido en un \# mensaje PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="103f2-109">A type of data contained in a PKCS \#7 message.</span></span> <span data-ttu-id="103f2-110">Los tipos de contenido base solo contienen datos, sin mejoras criptográficas como los valores hash o las firmas.</span><span class="sxs-lookup"><span data-stu-id="103f2-110">Base content types only contain data, no cryptographic enhancements such as hashes or signatures.</span></span> <span data-ttu-id="103f2-111">Actualmente, el único tipo de contenido base es el tipo de contenido de datos.</span><span class="sxs-lookup"><span data-stu-id="103f2-111">Currently, the only base content type is the Data content type.</span></span>

</dd> <dt>

<span data-ttu-id="103f2-112"><span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**funciones criptográficas base**</span><span class="sxs-lookup"><span data-stu-id="103f2-112"><span id="_security_base_cryptographic_functions_gly"></span><span id="_SECURITY_BASE_CRYPTOGRAPHIC_FUNCTIONS_GLY"></span>**base cryptographic functions**</span></span>
</dt> <dd>

<span data-ttu-id="103f2-113">Nivel más bajo de funciones de la arquitectura de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="103f2-113">The lowest level of functions in the CryptoAPI architecture.</span></span> <span data-ttu-id="103f2-114">Las usan las aplicaciones y otras funciones de CryptoAPI de alto nivel para proporcionar acceso a los algoritmos criptográficos proporcionados por CSP, la generación de claves segura y el almacenamiento seguro de secretos.</span><span class="sxs-lookup"><span data-stu-id="103f2-114">They are used by applications and other high-level CryptoAPI functions to provide access to CSP-provided cryptographic algorithms, secure key generation, and secure storage of secrets.</span></span>

<span data-ttu-id="103f2-115">Vea también [*proveedores de servicios de cifrado*](c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="103f2-115">See also [*cryptographic service providers*](c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="103f2-116"><span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**Reglas de codificación básicas**</span><span class="sxs-lookup"><span data-stu-id="103f2-116"><span id="_security_basic_encoding_rules_gly"></span><span id="_SECURITY_BASIC_ENCODING_RULES_GLY"></span>**Basic Encoding Rules**</span></span>
</dt> <dd>

<span data-ttu-id="103f2-117">BER Conjunto de reglas que se usan para codificar los datos definidos por ASN. 1 en un flujo de bits (ceros o unos) para la transmisión o el almacenamiento externo.</span><span class="sxs-lookup"><span data-stu-id="103f2-117">(BER) The set of rules used to encode ASN.1 defined data into a stream of bits (zeros or ones) for external storage or transmission.</span></span> <span data-ttu-id="103f2-118">Un único objeto ASN. 1 puede tener varias codificaciones BER equivalentes.</span><span class="sxs-lookup"><span data-stu-id="103f2-118">A single ASN.1 object may have several equivalent BER encodes.</span></span> <span data-ttu-id="103f2-119">BER se define en la recomendación de CCITt X. 209.</span><span class="sxs-lookup"><span data-stu-id="103f2-119">BER is defined in CCITT Recommendation X.209.</span></span> <span data-ttu-id="103f2-120">Éste es uno de los dos métodos de codificación que usa actualmente CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="103f2-120">This is one of the two encoding methods currently used by CryptoAPI.</span></span>

</dd> <dt>

<span data-ttu-id="103f2-121"><span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**BER**</span><span class="sxs-lookup"><span data-stu-id="103f2-121"><span id="_security_ber_gly"></span><span id="_SECURITY_BER_GLY"></span>**BER**</span></span>
</dt> <dd>

<span data-ttu-id="103f2-122">Vea *reglas de codificación básicas*.</span><span class="sxs-lookup"><span data-stu-id="103f2-122">See *Basic Encoding Rules*.</span></span>

</dd> <dt>

<span data-ttu-id="103f2-123"><span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**Big-Endian**</span><span class="sxs-lookup"><span data-stu-id="103f2-123"><span id="_security_big_endian_gly"></span><span id="_SECURITY_BIG_ENDIAN_GLY"></span>**big-endian**</span></span>
</dt> <dd>

<span data-ttu-id="103f2-124">Una memoria o un formato de datos en el que el byte más significativo se almacena en la dirección inferior o se llega primero.</span><span class="sxs-lookup"><span data-stu-id="103f2-124">A memory or data format in which the most significant byte is stored at the lower address or arrives first.</span></span>

<span data-ttu-id="103f2-125">Vea también [*Little-Endian*](l-gly.md).</span><span class="sxs-lookup"><span data-stu-id="103f2-125">See also [*little-endian*](l-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="103f2-126"><span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**BLOB**</span><span class="sxs-lookup"><span data-stu-id="103f2-126"><span id="_security_blob_gly"></span><span id="_SECURITY_BLOB_GLY"></span>**BLOB**</span></span>
</dt> <dd>

<span data-ttu-id="103f2-127">Secuencia genérica de bits que contiene una o más estructuras de encabezado de longitud fija más datos específicos del contexto.</span><span class="sxs-lookup"><span data-stu-id="103f2-127">A generic sequence of bits that contain one or more fixed-length header structures plus context specific data.</span></span>

<span data-ttu-id="103f2-128">Vea también [*blobs de claves*](k-gly.md), [*blobs de certificados*](c-gly.md), [*blobs de nombres de certificado*](c-gly.md)y [*blobs de atributos*](a-gly.md).</span><span class="sxs-lookup"><span data-stu-id="103f2-128">See also [*key BLOBs*](k-gly.md), [*certificate BLOBs*](c-gly.md), [*certificate name BLOBs*](c-gly.md), and [*attribute BLOBs*](a-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="103f2-129"><span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**cifrado de bloques**</span><span class="sxs-lookup"><span data-stu-id="103f2-129"><span id="_security_block_cipher_gly"></span><span id="_SECURITY_BLOCK_CIPHER_GLY"></span>**block cipher**</span></span>
</dt> <dd>

<span data-ttu-id="103f2-130">Algoritmo de cifrado que cifra los datos en unidades discretas (denominadas bloques), en lugar de como una secuencia continua de bits.</span><span class="sxs-lookup"><span data-stu-id="103f2-130">A cipher algorithm that encrypts data in discrete units (called blocks), rather than as a continuous stream of bits.</span></span> <span data-ttu-id="103f2-131">El tamaño de bloque más común es 64 bits.</span><span class="sxs-lookup"><span data-stu-id="103f2-131">The most common block size is 64 bits.</span></span> <span data-ttu-id="103f2-132">Por ejemplo, DES es un cifrado de bloques.</span><span class="sxs-lookup"><span data-stu-id="103f2-132">For example, DES is a block cipher.</span></span>

<span data-ttu-id="103f2-133">Vea también [*cifrado de secuencias*](s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="103f2-133">See also [*stream cipher*](s-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="103f2-134"><span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**clave de cifrado masivo**</span><span class="sxs-lookup"><span data-stu-id="103f2-134"><span id="_security_bulk_encryption_key_gly"></span><span id="_SECURITY_BULK_ENCRYPTION_KEY_GLY"></span>**bulk encryption key**</span></span>
</dt> <dd>

<span data-ttu-id="103f2-135">Una clave de sesión derivada de una clave maestra.</span><span class="sxs-lookup"><span data-stu-id="103f2-135">A session key derived from a master key.</span></span> <span data-ttu-id="103f2-136">Las claves de cifrado masivo se usan en el cifrado [*Schannel*](s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="103f2-136">Bulk encryption keys are used in [*Schannel*](s-gly.md) encryption.</span></span>

</dd> </dl>

 

 



