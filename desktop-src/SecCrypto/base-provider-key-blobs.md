---
description: El proveedor base y el proveedor extendido utilizan los mismos blobs de clave.
ms.assetid: b4592036-0fa3-4b7e-beed-78cf1d2f39a9
title: Blobs de clave de proveedor base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c763f97fe6e7868246e0bce30ee2a741e8bd212f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666534"
---
# <a name="base-provider-key-blobs"></a><span data-ttu-id="825aa-103">Blobs de clave de proveedor base</span><span class="sxs-lookup"><span data-stu-id="825aa-103">Base Provider Key BLOBs</span></span>

<span data-ttu-id="825aa-104">El proveedor base y el proveedor extendido utilizan los mismos [*blobs de clave*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="825aa-104">The Base Provider and Extended Provider use the same [*key BLOBs*](../secgloss/k-gly.md).</span></span>

-   [<span data-ttu-id="825aa-105">Blobs de clave pública</span><span class="sxs-lookup"><span data-stu-id="825aa-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="825aa-106">Blobs de clave privada</span><span class="sxs-lookup"><span data-stu-id="825aa-106">Private Key BLOBs</span></span>](#private-key-blobs)
-   [<span data-ttu-id="825aa-107">Blobs de clave simple</span><span class="sxs-lookup"><span data-stu-id="825aa-107">Simple Key BLOBs</span></span>](#simple-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="825aa-108">Blobs de clave pública</span><span class="sxs-lookup"><span data-stu-id="825aa-108">Public Key BLOBs</span></span>

<span data-ttu-id="825aa-109">Los [*blobs de clave pública*](../secgloss/p-gly.md), tipo **PUBLICKEYBLOB**, se usan para almacenar [*claves públicas*](../secgloss/p-gly.md) fuera de un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="825aa-109">[*Public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to store [*public keys*](../secgloss/p-gly.md) outside a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span> <span data-ttu-id="825aa-110">Los blobs de clave pública del proveedor base tienen el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="825aa-110">Base provider public key BLOBs have the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

<span data-ttu-id="825aa-111">En la tabla siguiente se describe cada componente de clave pública.</span><span class="sxs-lookup"><span data-stu-id="825aa-111">The following table describes each public key component.</span></span> <span data-ttu-id="825aa-112">Todos los valores están en formato [*Little-Endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="825aa-112">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="825aa-113">Campo</span><span class="sxs-lookup"><span data-stu-id="825aa-113">Field</span></span>          | <span data-ttu-id="825aa-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="825aa-114">Description</span></span>                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="825aa-115">modulus</span><span class="sxs-lookup"><span data-stu-id="825aa-115">modulus</span></span>        | <span data-ttu-id="825aa-116">Los datos del módulo de clave pública se encuentran directamente después de la estructura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="825aa-116">The public key modulus data is located directly after the [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="825aa-117">El tamaño de estos datos variará en función del tamaño de la clave pública.</span><span class="sxs-lookup"><span data-stu-id="825aa-117">The size of this data will vary, depending on the size of the public key.</span></span> <span data-ttu-id="825aa-118">El número de bytes se puede determinar dividiendo el valor del campo **bitlen de RSAPUBKEY** por ocho.</span><span class="sxs-lookup"><span data-stu-id="825aa-118">The number of bytes can be determined by dividing the value of the **RSAPUBKEY bitlen** field by eight.</span></span> |
| <span data-ttu-id="825aa-119">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="825aa-119">publickeystruc</span></span> | <span data-ttu-id="825aa-120">Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="825aa-120">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="825aa-121">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="825aa-121">rsapubkey</span></span>      | <span data-ttu-id="825aa-122">Estructura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="825aa-122">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="825aa-123">El miembro **mágico** debe establecerse en 0x31415352.</span><span class="sxs-lookup"><span data-stu-id="825aa-123">The **magic** member must be set to 0x31415352.</span></span> <span data-ttu-id="825aa-124">Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de rsa1.</span><span class="sxs-lookup"><span data-stu-id="825aa-124">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA1.</span></span>                                                                         |



 

> [!Note]  
> <span data-ttu-id="825aa-125">No se cifran los blobs de clave pública.</span><span class="sxs-lookup"><span data-stu-id="825aa-125">Public key BLOBs are not encrypted.</span></span> <span data-ttu-id="825aa-126">Contienen claves públicas en formato de [*texto simple*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="825aa-126">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="825aa-127">Blobs de clave privada</span><span class="sxs-lookup"><span data-stu-id="825aa-127">Private Key BLOBs</span></span>

<span data-ttu-id="825aa-128">Los [*blobs de clave privada*](../secgloss/p-gly.md), tipo **PRIVATEKEYBLOB**, se usan para almacenar [*claves privadas*](../secgloss/p-gly.md) fuera de un CSP.</span><span class="sxs-lookup"><span data-stu-id="825aa-128">[*Private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store [*private keys*](../secgloss/p-gly.md) outside a CSP.</span></span> <span data-ttu-id="825aa-129">Los blobs de clave privada del proveedor base tienen el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="825aa-129">Base provider private key BLOBs have the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
BYTE prime1[rsapubkey.bitlen/16];
BYTE prime2[rsapubkey.bitlen/16];
BYTE exponent1[rsapubkey.bitlen/16];
BYTE exponent2[rsapubkey.bitlen/16];
BYTE coefficient[rsapubkey.bitlen/16];
BYTE privateExponent[rsapubkey.bitlen/8];
```

<span data-ttu-id="825aa-130">En la tabla siguiente se describe el componente BLOB de clave privada.</span><span class="sxs-lookup"><span data-stu-id="825aa-130">The following table describes the private key BLOB component.</span></span>

> [!Note]  
> <span data-ttu-id="825aa-131">Estos campos se corresponden con los campos que se describen en la sección 7,2 de [*estándares de criptografía de clave pública*](../secgloss/p-gly.md) (PKCS) \# 1 con pequeñas diferencias.</span><span class="sxs-lookup"><span data-stu-id="825aa-131">These fields correspond to the fields described in section 7.2 of [*Public Key Cryptography Standards*](../secgloss/p-gly.md) (PKCS) \#1 with minor differences.</span></span>

 



| <span data-ttu-id="825aa-132">Campo</span><span class="sxs-lookup"><span data-stu-id="825aa-132">Field</span></span>           | <span data-ttu-id="825aa-133">Descripción</span><span class="sxs-lookup"><span data-stu-id="825aa-133">Description</span></span>                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="825aa-134">coeficiente</span><span class="sxs-lookup"><span data-stu-id="825aa-134">coefficient</span></span>     | <span data-ttu-id="825aa-135">Coeficiente.</span><span class="sxs-lookup"><span data-stu-id="825aa-135">Coefficient.</span></span> <span data-ttu-id="825aa-136">Esto tiene un valor numérico de (inverso de q) mod p.</span><span class="sxs-lookup"><span data-stu-id="825aa-136">This has a numeric value of (inverse of q) mod p.</span></span>                                                                                                                                                |
| <span data-ttu-id="825aa-137">exponent1</span><span class="sxs-lookup"><span data-stu-id="825aa-137">exponent1</span></span>       | <span data-ttu-id="825aa-138">Exponente 1.</span><span class="sxs-lookup"><span data-stu-id="825aa-138">Exponent 1.</span></span> <span data-ttu-id="825aa-139">Este tiene un valor numérico de d mod (p – 1).</span><span class="sxs-lookup"><span data-stu-id="825aa-139">This has a numeric value of d mod (p – 1).</span></span>                                                                                                                                                        |
| <span data-ttu-id="825aa-140">exponent2</span><span class="sxs-lookup"><span data-stu-id="825aa-140">exponent2</span></span>       | <span data-ttu-id="825aa-141">Exponente 2.</span><span class="sxs-lookup"><span data-stu-id="825aa-141">Exponent 2.</span></span> <span data-ttu-id="825aa-142">Este tiene un valor numérico de d mod (q – 1).</span><span class="sxs-lookup"><span data-stu-id="825aa-142">This has a numeric value of d mod (q – 1).</span></span>                                                                                                                                                        |
| <span data-ttu-id="825aa-143">Modulus</span><span class="sxs-lookup"><span data-stu-id="825aa-143">Modulus</span></span>         | <span data-ttu-id="825aa-144">El módulo.</span><span class="sxs-lookup"><span data-stu-id="825aa-144">The modulus.</span></span> <span data-ttu-id="825aa-145">Esto tiene un valor de *Prime1*×*Prime2* y a menudo se conoce como n.</span><span class="sxs-lookup"><span data-stu-id="825aa-145">This has a value of *Prime1*×*Prime2* and is often known as n.</span></span>                                                                                                                                   |
| <span data-ttu-id="825aa-146">prime1</span><span class="sxs-lookup"><span data-stu-id="825aa-146">prime1</span></span>          | <span data-ttu-id="825aa-147">Número primo 1, que a menudo se conoce como p.</span><span class="sxs-lookup"><span data-stu-id="825aa-147">Prime number 1, often known as p.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="825aa-148">prime2</span><span class="sxs-lookup"><span data-stu-id="825aa-148">prime2</span></span>          | <span data-ttu-id="825aa-149">Número primo 2, que a menudo se conoce como q.</span><span class="sxs-lookup"><span data-stu-id="825aa-149">Prime number 2, often known as q.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="825aa-150">privateExponent</span><span class="sxs-lookup"><span data-stu-id="825aa-150">privateExponent</span></span> | <span data-ttu-id="825aa-151">Exponente privado, que a menudo se conoce como d.</span><span class="sxs-lookup"><span data-stu-id="825aa-151">Private exponent, often known as d.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="825aa-152">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="825aa-152">publickeystruc</span></span>  | <span data-ttu-id="825aa-153">Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="825aa-153">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                         |
| <span data-ttu-id="825aa-154">rsapubkey</span><span class="sxs-lookup"><span data-stu-id="825aa-154">rsapubkey</span></span>       | <span data-ttu-id="825aa-155">Estructura [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) .</span><span class="sxs-lookup"><span data-stu-id="825aa-155">A [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) structure.</span></span> <span data-ttu-id="825aa-156">El miembro **mágico** debe establecerse en 0x32415352.</span><span class="sxs-lookup"><span data-stu-id="825aa-156">The **magic** member must be set to 0x32415352.</span></span> <span data-ttu-id="825aa-157">Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de RSA2.</span><span class="sxs-lookup"><span data-stu-id="825aa-157">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of RSA2.</span></span> |



 

> [!Note]  
> <span data-ttu-id="825aa-158">No se cifran los blobs de clave privada.</span><span class="sxs-lookup"><span data-stu-id="825aa-158">Private key BLOBs are not encrypted.</span></span> <span data-ttu-id="825aa-159">Contienen claves privadas en formato de texto simple.</span><span class="sxs-lookup"><span data-stu-id="825aa-159">They contain private keys in plaintext form.</span></span>

 

<span data-ttu-id="825aa-160">Al llamar a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), el desarrollador puede elegir si desea cifrar la clave.</span><span class="sxs-lookup"><span data-stu-id="825aa-160">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="825aa-161">El **PRIVATEKEYBLOB** se cifra si el parámetro *hExpKey* contiene un identificador válido para una clave de sesión.</span><span class="sxs-lookup"><span data-stu-id="825aa-161">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="825aa-162">Todo excepto la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB está cifrado.</span><span class="sxs-lookup"><span data-stu-id="825aa-162">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="825aa-163">Los parámetros de algoritmo de cifrado y clave de cifrado no se almacenan junto con el BLOB de clave privada.</span><span class="sxs-lookup"><span data-stu-id="825aa-163">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="825aa-164">La aplicación debe administrar y almacenar esta información.</span><span class="sxs-lookup"><span data-stu-id="825aa-164">The application must manage and store this information.</span></span> <span data-ttu-id="825aa-165">Si se pasa cero para *hExpKey*, la clave privada se exportará sin cifrado.</span><span class="sxs-lookup"><span data-stu-id="825aa-165">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="825aa-166">Es peligroso exportar las claves privadas sin cifrado, ya que son vulnerables a la interceptación y el uso por parte de entidades no autorizadas.</span><span class="sxs-lookup"><span data-stu-id="825aa-166">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

## <a name="simple-key-blobs"></a><span data-ttu-id="825aa-167">Blobs de clave simple</span><span class="sxs-lookup"><span data-stu-id="825aa-167">Simple Key BLOBs</span></span>

<span data-ttu-id="825aa-168">Los [*blobs de clave simple*](../secgloss/s-gly.md), Type **SIMPLEBLOB**, se usan para almacenar y transportar claves de sesión fuera de un CSP.</span><span class="sxs-lookup"><span data-stu-id="825aa-168">[*Simple key BLOBs*](../secgloss/s-gly.md), type **SIMPLEBLOB**, are used to store and transport session keys outside a CSP.</span></span> <span data-ttu-id="825aa-169">Los blobs de clave simple del proveedor base siempre se cifran con una [*clave pública de intercambio de claves*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="825aa-169">Base provider simple key BLOBs are always encrypted with a [*key exchange public key*](../secgloss/k-gly.md).</span></span> <span data-ttu-id="825aa-170">El miembro **pbData** de **SIMPLEBLOB** es una secuencia de bytes con el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="825aa-170">The **pbData** member of the **SIMPLEBLOB** is a sequence of bytes in the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

<span data-ttu-id="825aa-171">En la tabla siguiente se describe cada componente del miembro **pbData** de **SIMPLEBLOB**.</span><span class="sxs-lookup"><span data-stu-id="825aa-171">The following table describes each component of the **pbData** member of the **SIMPLEBLOB**.</span></span>



| <span data-ttu-id="825aa-172">Campo</span><span class="sxs-lookup"><span data-stu-id="825aa-172">Field</span></span>          | <span data-ttu-id="825aa-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="825aa-173">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="825aa-174">algid</span><span class="sxs-lookup"><span data-stu-id="825aa-174">algid</span></span>          | <span data-ttu-id="825aa-175">Una estructura de [**\_ identificador de alg**](alg-id.md) que especifica el algoritmo de cifrado que se usa para cifrar los datos de la clave de sesión.</span><span class="sxs-lookup"><span data-stu-id="825aa-175">An [**ALG\_ID**](alg-id.md) structure that specifies the encryption algorithm used to encrypt the session key data.</span></span> <span data-ttu-id="825aa-176">Normalmente, tiene un valor de CALG \_ RSA \_ KEYX, que indica que los datos de la clave de sesión se cifraron con una clave pública de intercambio de claves mediante el [*algoritmo de clave pública RSA*](../secgloss/r-gly.md).</span><span class="sxs-lookup"><span data-stu-id="825aa-176">This typically has a value of CALG\_RSA\_KEYX, which indicates that the session key data was encrypted with a key exchange public key using the [*RSA Public Key algorithm*](../secgloss/r-gly.md).</span></span>                                                                                                                           |
| <span data-ttu-id="825aa-177">EncryptedKey</span><span class="sxs-lookup"><span data-stu-id="825aa-177">encryptedkey</span></span>   | <span data-ttu-id="825aa-178">Secuencia de **bytes** que representa los datos de clave de sesión cifrada con el formato de un \# bloque de cifrado PKCS 1, tipo 2.</span><span class="sxs-lookup"><span data-stu-id="825aa-178">A **BYTE** sequence that represents the encrypted session key data in the form of a PKCS \#1, type 2 encryption block.</span></span> <span data-ttu-id="825aa-179">Para obtener información acerca de este formato de datos, consulte los estándares de criptografía de clave pública (PKCS) \# 1, publicados por RSA Data Security, Inc. Estos datos tienen siempre el mismo tamaño que el módulo de la clave pública.</span><span class="sxs-lookup"><span data-stu-id="825aa-179">For information about this data format, see the Public Key Cryptography Standards (PKCS) \#1, published by RSA Data Security, Inc. This data is always the same size as the modulus of the public key.</span></span> <span data-ttu-id="825aa-180">Por ejemplo, las claves públicas generadas por el proveedor base de RSA de Microsoft pueden tener una longitud de 512 bits (64 bytes), por lo que los datos de la clave de sesión cifrada también tienen siempre 512 bits (64 bytes).</span><span class="sxs-lookup"><span data-stu-id="825aa-180">For example, public keys generated by the Microsoft RSA Base Provider can be 512 bits (64 bytes) in length, so the encrypted session key data is also always 512 bits (64 bytes).</span></span><br/> |
| <span data-ttu-id="825aa-181">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="825aa-181">publickeystruc</span></span> | <span data-ttu-id="825aa-182">Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="825aa-182">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

 

 
