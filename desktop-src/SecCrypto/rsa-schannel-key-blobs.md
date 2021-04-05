---
description: Los blobs se utilizan con el proveedor de RSA/Schannel para exportar claves del proveedor de servicios criptográficos (CSP) e importarlas en él.
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: Blobs de clave RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cea26a98e9c2925442166eb28245ebc471b1749e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908081"
---
# <a name="rsaschannel-key-blobs"></a><span data-ttu-id="2db0f-103">Blobs de clave RSA/Schannel</span><span class="sxs-lookup"><span data-stu-id="2db0f-103">RSA/Schannel Key BLOBs</span></span>

<span data-ttu-id="2db0f-104">Los [*blobs*](../secgloss/b-gly.md) se utilizan con el proveedor de Schannel de [*RSA*](../secgloss/r-gly.md) / [](../secgloss/s-gly.md) para exportar claves desde el proveedor de [*servicios de cifrado*](../secgloss/c-gly.md) (CSP) e importarlas en él.</span><span class="sxs-lookup"><span data-stu-id="2db0f-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="2db0f-105">Blobs de clave pública</span><span class="sxs-lookup"><span data-stu-id="2db0f-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="2db0f-106">Blobs de clave privada</span><span class="sxs-lookup"><span data-stu-id="2db0f-106">Private Key BLOBs</span></span>](#private-key-blobs)
-   [<span data-ttu-id="2db0f-107">Blobs de clave simple</span><span class="sxs-lookup"><span data-stu-id="2db0f-107">Simple Key BLOBs</span></span>](#simple-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="2db0f-108">Blobs de clave pública</span><span class="sxs-lookup"><span data-stu-id="2db0f-108">Public Key BLOBs</span></span>

<span data-ttu-id="2db0f-109">Los [*blobs de clave pública*](../secgloss/p-gly.md), tipo **PUBLICKEYBLOB**, se usan para almacenar [*claves públicas*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2db0f-109">[*Public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to store [*public keys*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="2db0f-110">Estas claves se exportan e importan como una secuencia de bytes con el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="2db0f-110">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

<span data-ttu-id="2db0f-111">En la tabla siguiente se describe cada componente de clave pública.</span><span class="sxs-lookup"><span data-stu-id="2db0f-111">The following table describes each public key component.</span></span> <span data-ttu-id="2db0f-112">Todos los valores están en formato [*Little-Endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="2db0f-112">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="2db0f-113">Campo</span><span class="sxs-lookup"><span data-stu-id="2db0f-113">Field</span></span>          | <span data-ttu-id="2db0f-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2db0f-114">Description</span></span>                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2db0f-115">modulus</span><span class="sxs-lookup"><span data-stu-id="2db0f-115">modulus</span></span>        | <span data-ttu-id="2db0f-116">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="2db0f-116">A **BYTE** sequence.</span></span> <span data-ttu-id="2db0f-117">Los datos del módulo de clave pública se encuentran directamente después de la estructura **RSAPUBKEY** .</span><span class="sxs-lookup"><span data-stu-id="2db0f-117">The public key modulus data is located directly after the **RSAPUBKEY** structure.</span></span> <span data-ttu-id="2db0f-118">La longitud de estos datos varía en función de la longitud de la clave pública.</span><span class="sxs-lookup"><span data-stu-id="2db0f-118">The length of this data varies, depending on the length of the public key.</span></span> <span data-ttu-id="2db0f-119">El número de bytes se puede determinar dividiendo el valor del miembro **bitlen** de **RSAPUBKEY** por ocho.</span><span class="sxs-lookup"><span data-stu-id="2db0f-119">The number of bytes can be determined by dividing the value of the **bitlen** member of **RSAPUBKEY** by eight.</span></span> |
| <span data-ttu-id="2db0f-120">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="2db0f-120">publickeystruc</span></span> | <span data-ttu-id="2db0f-121">Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="2db0f-121">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                              |
| <span data-ttu-id="2db0f-122">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="2db0f-122">rsapubkey</span></span>      | <span data-ttu-id="2db0f-123">Estructura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="2db0f-123">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="2db0f-124">El miembro **mágico** debe establecerse en 0x31415352.</span><span class="sxs-lookup"><span data-stu-id="2db0f-124">The **magic** member must be set to 0x31415352.</span></span> <span data-ttu-id="2db0f-125">Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de rsa1.</span><span class="sxs-lookup"><span data-stu-id="2db0f-125">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA1.</span></span>                                                                                      |



 

> [!Note]  
> <span data-ttu-id="2db0f-126">No se cifran los blobs de clave pública.</span><span class="sxs-lookup"><span data-stu-id="2db0f-126">Public key BLOBs are not encrypted.</span></span> <span data-ttu-id="2db0f-127">Contienen claves públicas en formato de [*texto simple*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="2db0f-127">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="2db0f-128">Blobs de clave privada</span><span class="sxs-lookup"><span data-stu-id="2db0f-128">Private Key BLOBs</span></span>

<span data-ttu-id="2db0f-129">Los [*blobs de clave privada*](../secgloss/p-gly.md), tipo **PRIVATEKEYBLOB**, se usan para almacenar [*pares de claves pública y privada*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2db0f-129">[*Private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store [*public/private key pairs*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="2db0f-130">Estas claves se exportan e importan como una secuencia de bytes con el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="2db0f-130">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
BYTE            prime1[rsapubkey.bitlen/16];
BYTE            prime2[rsapubkey.bitlen/16];
BYTE            exponent1[rsapubkey.bitlen/16];
BYTE            exponent2[rsapubkey.bitlen/16];
BYTE            coefficient[rsapubkey.bitlen/16];
BYTE            privateExponent[rsapubkey.bitlen/8];
```

<span data-ttu-id="2db0f-131">Si el [*BLOB de clave*](../secgloss/k-gly.md) está cifrado, se cifra todo excepto la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB.</span><span class="sxs-lookup"><span data-stu-id="2db0f-131">If the [*key BLOB*](../secgloss/k-gly.md) is encrypted, then everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="2db0f-132">Los parámetros de algoritmo de cifrado y clave de cifrado no se almacenan junto con el BLOB de clave privada.</span><span class="sxs-lookup"><span data-stu-id="2db0f-132">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="2db0f-133">Es responsabilidad de la aplicación administrar esta información.</span><span class="sxs-lookup"><span data-stu-id="2db0f-133">It is the responsibility of the application to manage this information.</span></span>

 

<span data-ttu-id="2db0f-134">En la tabla siguiente se describe cada componente de BLOB de clave privada.</span><span class="sxs-lookup"><span data-stu-id="2db0f-134">The following table describes each private key BLOB component.</span></span>

> [!Note]  
> <span data-ttu-id="2db0f-135">Estos campos se corresponden con los campos que se describen en la sección 7,2 de [*estándares de criptografía de clave pública*](../secgloss/p-gly.md) (PKCS) \# 1 con pequeñas diferencias.</span><span class="sxs-lookup"><span data-stu-id="2db0f-135">These fields correspond to the fields described in section 7.2 of [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1 with minor differences.</span></span>

 



| <span data-ttu-id="2db0f-136">Campo</span><span class="sxs-lookup"><span data-stu-id="2db0f-136">Field</span></span>           | <span data-ttu-id="2db0f-137">Descripción</span><span class="sxs-lookup"><span data-stu-id="2db0f-137">Description</span></span>                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2db0f-138">exponent1</span><span class="sxs-lookup"><span data-stu-id="2db0f-138">exponent1</span></span>       | <span data-ttu-id="2db0f-139">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="2db0f-139">A **BYTE** sequence.</span></span> <span data-ttu-id="2db0f-140">Primer exponente.</span><span class="sxs-lookup"><span data-stu-id="2db0f-140">The first exponent.</span></span> <span data-ttu-id="2db0f-141">Este tiene un valor numérico de d mod (p – 1).</span><span class="sxs-lookup"><span data-stu-id="2db0f-141">This has a numeric value of d mod (p – 1).</span></span>                                                                                                                           |
| <span data-ttu-id="2db0f-142">exponent2</span><span class="sxs-lookup"><span data-stu-id="2db0f-142">exponent2</span></span>       | <span data-ttu-id="2db0f-143">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="2db0f-143">A **BYTE** sequence.</span></span> <span data-ttu-id="2db0f-144">Segundo exponente.</span><span class="sxs-lookup"><span data-stu-id="2db0f-144">The second exponent.</span></span> <span data-ttu-id="2db0f-145">Este tiene un valor numérico de d mod (q – 1).</span><span class="sxs-lookup"><span data-stu-id="2db0f-145">This has a numeric value of d mod (q – 1).</span></span>                                                                                                                          |
| <span data-ttu-id="2db0f-146">coeficiente</span><span class="sxs-lookup"><span data-stu-id="2db0f-146">coefficient</span></span>     | <span data-ttu-id="2db0f-147">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="2db0f-147">A **BYTE** sequence.</span></span> <span data-ttu-id="2db0f-148">Coeficiente.</span><span class="sxs-lookup"><span data-stu-id="2db0f-148">Coefficient.</span></span> <span data-ttu-id="2db0f-149">Esto tiene un valor numérico de (inverso de q) mod p.</span><span class="sxs-lookup"><span data-stu-id="2db0f-149">This has a numeric value of (inverse of q) mod p.</span></span>                                                                                                                           |
| <span data-ttu-id="2db0f-150">Modulus</span><span class="sxs-lookup"><span data-stu-id="2db0f-150">Modulus</span></span>         | <span data-ttu-id="2db0f-151">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="2db0f-151">A **BYTE** sequence.</span></span> <span data-ttu-id="2db0f-152">El módulo.</span><span class="sxs-lookup"><span data-stu-id="2db0f-152">The modulus.</span></span> <span data-ttu-id="2db0f-153">Tiene una cadena que contiene *Prime1* \* *Prime2*.</span><span class="sxs-lookup"><span data-stu-id="2db0f-153">This has a string that contains *Prime1* \* *Prime2*.</span></span> <span data-ttu-id="2db0f-154">A menudo se conoce como n.</span><span class="sxs-lookup"><span data-stu-id="2db0f-154">It is often known as n.</span></span>                                                                                               |
| <span data-ttu-id="2db0f-155">prime1</span><span class="sxs-lookup"><span data-stu-id="2db0f-155">prime1</span></span>          | <span data-ttu-id="2db0f-156">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="2db0f-156">A **BYTE** sequence.</span></span> <span data-ttu-id="2db0f-157">Número primo 1, que a menudo se conoce como p.</span><span class="sxs-lookup"><span data-stu-id="2db0f-157">Prime number 1, often known as p.</span></span>                                                                                                                                                        |
| <span data-ttu-id="2db0f-158">prime2</span><span class="sxs-lookup"><span data-stu-id="2db0f-158">prime2</span></span>          | <span data-ttu-id="2db0f-159">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="2db0f-159">A **BYTE** sequence.</span></span> <span data-ttu-id="2db0f-160">Número primo 2, que a menudo se conoce como q.</span><span class="sxs-lookup"><span data-stu-id="2db0f-160">Prime number 2, often known as q.</span></span>                                                                                                                                                        |
| <span data-ttu-id="2db0f-161">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="2db0f-161">publickeystruc</span></span>  | <span data-ttu-id="2db0f-162">Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="2db0f-162">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                         |
| <span data-ttu-id="2db0f-163">privateExponent</span><span class="sxs-lookup"><span data-stu-id="2db0f-163">privateExponent</span></span> | <span data-ttu-id="2db0f-164">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="2db0f-164">A **BYTE** sequence.</span></span> <span data-ttu-id="2db0f-165">Exponente privado, que a menudo se conoce como d.</span><span class="sxs-lookup"><span data-stu-id="2db0f-165">The private exponent, often known as d.</span></span>                                                                                                                                                  |
| <span data-ttu-id="2db0f-166">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="2db0f-166">rsapubkey</span></span>       | <span data-ttu-id="2db0f-167">Estructura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="2db0f-167">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="2db0f-168">El miembro **mágico** debe establecerse en 0x32415352.</span><span class="sxs-lookup"><span data-stu-id="2db0f-168">The **magic** member must be set to 0x32415352.</span></span> <span data-ttu-id="2db0f-169">Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de RSA2.</span><span class="sxs-lookup"><span data-stu-id="2db0f-169">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA2.</span></span> |



 

> [!Note]  
> <span data-ttu-id="2db0f-170">No se cifran los blobs de clave privada.</span><span class="sxs-lookup"><span data-stu-id="2db0f-170">Private key BLOBs are not encrypted.</span></span> <span data-ttu-id="2db0f-171">Contienen claves privadas en formato de texto simple.</span><span class="sxs-lookup"><span data-stu-id="2db0f-171">They contain private keys in plaintext form.</span></span>

 

<span data-ttu-id="2db0f-172">Al llamar a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), el desarrollador puede elegir si desea cifrar la clave.</span><span class="sxs-lookup"><span data-stu-id="2db0f-172">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="2db0f-173">El **PRIVATEKEYBLOB** se cifra si el parámetro *hExpKey* contiene un identificador válido para una clave de sesión.</span><span class="sxs-lookup"><span data-stu-id="2db0f-173">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="2db0f-174">Todo excepto la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB está cifrado.</span><span class="sxs-lookup"><span data-stu-id="2db0f-174">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="2db0f-175">Los parámetros de algoritmo de cifrado y clave de cifrado no se almacenan junto con el BLOB de clave privada.</span><span class="sxs-lookup"><span data-stu-id="2db0f-175">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="2db0f-176">La aplicación debe administrar y almacenar esta información.</span><span class="sxs-lookup"><span data-stu-id="2db0f-176">The application must manage and store this information.</span></span> <span data-ttu-id="2db0f-177">Si se pasa cero para *hExpKey*, la clave privada se exportará sin cifrado.</span><span class="sxs-lookup"><span data-stu-id="2db0f-177">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="2db0f-178">Es peligroso exportar las claves privadas sin cifrado, ya que son vulnerables a la interceptación y el uso por parte de entidades no autorizadas.</span><span class="sxs-lookup"><span data-stu-id="2db0f-178">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

## <a name="simple-key-blobs"></a><span data-ttu-id="2db0f-179">Blobs de clave simple</span><span class="sxs-lookup"><span data-stu-id="2db0f-179">Simple Key BLOBs</span></span>

<span data-ttu-id="2db0f-180">Los [*blobs de clave simple*](../secgloss/s-gly.md), Type **SIMPLEBLOB**, se usan para almacenar y transportar claves de sesión.</span><span class="sxs-lookup"><span data-stu-id="2db0f-180">[*Simple key BLOBs*](../secgloss/s-gly.md), type **SIMPLEBLOB**, are used to store and transport session keys.</span></span> <span data-ttu-id="2db0f-181">Siempre se cifran con una [*clave pública de intercambio de claves*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2db0f-181">These are always encrypted with a [*key exchange public key*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="2db0f-182">Estas claves se exportan e importan como una secuencia de bytes con el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="2db0f-182">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

<span data-ttu-id="2db0f-183">En la tabla siguiente se describe cada componente de BLOB simple.</span><span class="sxs-lookup"><span data-stu-id="2db0f-183">The following table describes each simple BLOB component.</span></span>



| <span data-ttu-id="2db0f-184">Campo</span><span class="sxs-lookup"><span data-stu-id="2db0f-184">Field</span></span>          | <span data-ttu-id="2db0f-185">Descripción</span><span class="sxs-lookup"><span data-stu-id="2db0f-185">Description</span></span>                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2db0f-186">algid</span><span class="sxs-lookup"><span data-stu-id="2db0f-186">algid</span></span>          | <span data-ttu-id="2db0f-187">Una estructura de [**\_ identificador de alg**](alg-id.md) .</span><span class="sxs-lookup"><span data-stu-id="2db0f-187">An [**ALG\_ID**](alg-id.md) structure.</span></span> <span data-ttu-id="2db0f-188">Normalmente, esto especifica el \_ algoritmo CALG RSA \_ KEYX, que indica que los datos de la clave de sesión se cifraron con una clave pública de intercambio de claves, mediante el [*algoritmo de clave pública RSA*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2db0f-188">This typically specifies the CALG\_RSA\_KEYX algorithm, which indicates that the session key data was encrypted with a key exchange public key, using the [*RSA Public Key algorithm*](../secgloss/r-gly.md).</span></span> |
| <span data-ttu-id="2db0f-189">EncryptedKey</span><span class="sxs-lookup"><span data-stu-id="2db0f-189">encryptedkey</span></span>   | <span data-ttu-id="2db0f-190">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="2db0f-190">A **BYTE** sequence.</span></span> <span data-ttu-id="2db0f-191">Los datos de la clave de sesión cifrada tienen el formato de un \# bloque de cifrado PKCS 1, tipo 2.</span><span class="sxs-lookup"><span data-stu-id="2db0f-191">The encrypted session key data is in the form of a PKCS \#1, type 2 encryption block.</span></span> <span data-ttu-id="2db0f-192">Para obtener información sobre este formato de datos, consulte los estándares de criptografía de clave pública (PKCS) publicados por RSA Data Security, Inc.</span><span class="sxs-lookup"><span data-stu-id="2db0f-192">For information about this data format, see the Public Key Cryptography Standards (PKCS), published by RSA Data Security, Inc.</span></span>                                                                                     |
| <span data-ttu-id="2db0f-193">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="2db0f-193">publickeystruc</span></span> | <span data-ttu-id="2db0f-194">Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="2db0f-194">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                         |



 

<span data-ttu-id="2db0f-195">Estos datos tienen siempre el mismo tamaño que el módulo de la clave pública.</span><span class="sxs-lookup"><span data-stu-id="2db0f-195">This data is always the same size as the modulus of the public key.</span></span> <span data-ttu-id="2db0f-196">Por ejemplo, las claves públicas generadas por el proveedor de servicios criptográficos de base de Microsoft son siempre de 512 bits (64 bytes) de longitud, por lo que los datos de clave de sesión cifrada también tienen siempre 64 bytes.</span><span class="sxs-lookup"><span data-stu-id="2db0f-196">For example, public keys generated by the Microsoft Base Cryptographic Provider are always 512 bits (64 bytes) in length, so the encrypted session key data is also always 64 bytes.</span></span>

 

 
