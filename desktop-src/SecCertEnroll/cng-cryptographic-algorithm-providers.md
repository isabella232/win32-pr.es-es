---
description: 'A diferencia de Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separa los proveedores de servicios criptográficos de los proveedores de almacenamiento de claves.'
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: Proveedores de algoritmos criptográficos CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bc64926236157e581ce6406d95681bd8d4add14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648526"
---
# <a name="cng-cryptographic-algorithm-providers"></a><span data-ttu-id="2c3b5-103">Proveedores de algoritmos criptográficos CNG</span><span class="sxs-lookup"><span data-stu-id="2c3b5-103">CNG Cryptographic Algorithm Providers</span></span>

<span data-ttu-id="2c3b5-104">A diferencia de Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separa los proveedores de servicios criptográficos de los proveedores de almacenamiento de claves.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-104">Unlike Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separates cryptographic providers from key storage providers.</span></span> <span data-ttu-id="2c3b5-105">Las operaciones básicas de los algoritmos criptográficos como la firma y el hash se denominan operaciones primitivas o simplemente primitivas.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-105">Basic cryptographic algorithm operations such as hashing and signing are called primitive operations or simply primitives.</span></span> <span data-ttu-id="2c3b5-106">CNG incluye un proveedor que implementa los algoritmos siguientes.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-106">CNG includes a provider that implements the following algorithms.</span></span>

-   [<span data-ttu-id="2c3b5-107">Algoritmos simétricos</span><span class="sxs-lookup"><span data-stu-id="2c3b5-107">Symmetric Algorithms</span></span>](#symmetric-algorithms)
-   [<span data-ttu-id="2c3b5-108">Algoritmos asimétricos</span><span class="sxs-lookup"><span data-stu-id="2c3b5-108">Asymmetric Algorithms</span></span>](#asymmetric-algorithms)
-   [<span data-ttu-id="2c3b5-109">Algoritmos de hash</span><span class="sxs-lookup"><span data-stu-id="2c3b5-109">Hashing Algorithms</span></span>](#hashing-algorithms)
-   [<span data-ttu-id="2c3b5-110">Algoritmos de intercambio de claves</span><span class="sxs-lookup"><span data-stu-id="2c3b5-110">Key Exchange Algorithms</span></span>](#key-exchange-algorithms)
-   [<span data-ttu-id="2c3b5-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c3b5-111">Related topics</span></span>](#related-topics)

## <a name="symmetric-algorithms"></a><span data-ttu-id="2c3b5-112">Algoritmos simétricos</span><span class="sxs-lookup"><span data-stu-id="2c3b5-112">Symmetric Algorithms</span></span>



| <span data-ttu-id="2c3b5-113">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c3b5-113">Name</span></span>                                   | <span data-ttu-id="2c3b5-114">Modos admitidos</span><span class="sxs-lookup"><span data-stu-id="2c3b5-114">Supported modes</span></span>                                                                                                                                                                                                 | <span data-ttu-id="2c3b5-115">Tamaño de clave en bits (predeterminado/mín./máx.)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-115">Key size in bits (Default/Min/Max)</span></span> |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| <span data-ttu-id="2c3b5-116">Estándar de cifrado avanzado (AES)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-116">Advanced Encryption Standard (AES)</span></span>     | <span data-ttu-id="2c3b5-117">ECB, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, encapsulado de claves AES, XTS</span><span class="sxs-lookup"><span data-stu-id="2c3b5-117">ECB, CBC, CFB8, CFB128, GCM, CCM, GMAC, CMAC, AES Key Wrap, XTS</span></span><br/> <span data-ttu-id="2c3b5-118">**Windows 8:** Comienza la compatibilidad con los modos CFB128 y CMAC.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-118">**Windows 8:** Support for the CFB128 and CMAC modes begins.</span></span><br/> <span data-ttu-id="2c3b5-119">**Windows 10:** Se inicia la compatibilidad con el modo XTS-AES.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-119">**Windows 10:** Support for XTS-AES mode begins.</span></span><br/> | <span data-ttu-id="2c3b5-120">128/192/256</span><span class="sxs-lookup"><span data-stu-id="2c3b5-120">128/192/256</span></span>                        |
| <span data-ttu-id="2c3b5-121">Estándar de cifrado de datos (DES)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-121">Data Encryption Standard (DES)</span></span>         | <span data-ttu-id="2c3b5-122">ECB, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="2c3b5-122">ECB, CBC, CFB8, CFB64</span></span><br/> <span data-ttu-id="2c3b5-123">**Windows 8:** Se inicia la compatibilidad con el modo CFB64.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-123">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                   | <span data-ttu-id="2c3b5-124">56/56/56</span><span class="sxs-lookup"><span data-stu-id="2c3b5-124">56/56/56</span></span>                           |
| <span data-ttu-id="2c3b5-125">Estándar de cifrado de datos XORed (DESX)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-125">Data Encryption Standard XORed(DESX)</span></span>   | <span data-ttu-id="2c3b5-126">ECB, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="2c3b5-126">ECB, CBC, CFB8, CFB64</span></span> <br/> <span data-ttu-id="2c3b5-127">**Windows 8:** Se inicia la compatibilidad con el modo CFB64.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-127">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                  | <span data-ttu-id="2c3b5-128">192/192/192</span><span class="sxs-lookup"><span data-stu-id="2c3b5-128">192/192/192</span></span>                        |
| <span data-ttu-id="2c3b5-129">Estándar de cifrado de datos triple (3DES)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-129">Triple Data Encryption Standard (3DES)</span></span> | <span data-ttu-id="2c3b5-130">ECB, CBC, CFB8, CFB64</span><span class="sxs-lookup"><span data-stu-id="2c3b5-130">ECB, CBC, CFB8, CFB64</span></span> <br/> <span data-ttu-id="2c3b5-131">**Windows 8:** Se inicia la compatibilidad con el modo CFB64.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-131">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                                                  | <span data-ttu-id="2c3b5-132">112/168</span><span class="sxs-lookup"><span data-stu-id="2c3b5-132">112/168</span></span>                            |
| <span data-ttu-id="2c3b5-133">RSA Data Security 2 (RC2)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-133">RSA Data Security 2 (RC2)</span></span>              | <span data-ttu-id="2c3b5-134">Se admiten los modos ECB, CBC, CFB8 y CFB64.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-134">ECB, CBC, CFB8, CFB64 modes are supported.</span></span><br/> <span data-ttu-id="2c3b5-135">**Windows 8:** Se inicia la compatibilidad con el modo CFB64.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-135">**Windows 8:** Support for the CFB64 mode begins.</span></span><br/>                                                                                              | <span data-ttu-id="2c3b5-136">de 16 a 128 en incrementos de 8 bits</span><span class="sxs-lookup"><span data-stu-id="2c3b5-136">16 to 128 in 8 bit increments</span></span>      |
| <span data-ttu-id="2c3b5-137">RSA Data Security 4 (RC4)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-137">RSA Data Security 4 (RC4)</span></span>              |                                                                                                                                                                                                                 | <span data-ttu-id="2c3b5-138">de 8 a 512, en incrementos de 8 bits</span><span class="sxs-lookup"><span data-stu-id="2c3b5-138">8 to 512, in 8-bit increments</span></span>      |



 

## <a name="asymmetric-algorithms"></a><span data-ttu-id="2c3b5-139">Algoritmos asimétricos</span><span class="sxs-lookup"><span data-stu-id="2c3b5-139">Asymmetric Algorithms</span></span>



| <span data-ttu-id="2c3b5-140">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c3b5-140">Name</span></span>                              | <span data-ttu-id="2c3b5-141">Notas</span><span class="sxs-lookup"><span data-stu-id="2c3b5-141">Notes</span></span>                                                                                                                                                                             | <span data-ttu-id="2c3b5-142">Tamaño de clave en bits (predeterminado/mín./máx.)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-142">Key size in bits (Default/Min/Max)</span></span>                                                                            |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c3b5-143">Algoritmo de firma digital (DSA)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-143">Digital Signature Algorithm (DSA)</span></span> | <span data-ttu-id="2c3b5-144">La implementación se ajusta a FIPS 186-3 para tamaños de clave entre los bits 1024 y 3072.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-144">Implementation conforms to FIPS 186-3 for key sizes between 1024 and 3072 bits.</span></span> <br/> <span data-ttu-id="2c3b5-145">La implementación se ajusta a FIPS 186-2 para tamaños de clave de 512 a 1024 bits.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-145">Implementation conforms to FIPS 186-2 for key sizes from 512 to 1024 bits.</span></span><br/> | <span data-ttu-id="2c3b5-146">de 512 a 3072, en incrementos de 64 bits</span><span class="sxs-lookup"><span data-stu-id="2c3b5-146">512 to 3072, in 64-bit increments</span></span><br/> <span data-ttu-id="2c3b5-147">**Windows 8:** Se inicia la compatibilidad con la clave de 3072 bits.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-147">**Windows 8:** Support for the a 3072 bit key begins.</span></span><br/> |
| <span data-ttu-id="2c3b5-148">RSA</span><span class="sxs-lookup"><span data-stu-id="2c3b5-148">RSA</span></span>                               | <span data-ttu-id="2c3b5-149">Incluye algoritmos RSA que usan codificación y relleno de cifrado asimétrico (OAEP) óptimos de cifrado asimétrico (OAEP) o relleno de texto sin formato del esquema de firma probabilística (PSS).</span><span class="sxs-lookup"><span data-stu-id="2c3b5-149">Includes RSA algorithms that use PKCS1, Optimal Asymmetric Encryption Padding (OAEP) encoding or padding, or Probabilistic Signature Scheme (PSS) plaintext padding</span></span>               | <span data-ttu-id="2c3b5-150">de 512 a 16384, en incrementos de 64 bits</span><span class="sxs-lookup"><span data-stu-id="2c3b5-150">512 to 16384, in 64-bit increments</span></span>                                                                            |



 

## <a name="hashing-algorithms"></a><span data-ttu-id="2c3b5-151">Algoritmos de hash</span><span class="sxs-lookup"><span data-stu-id="2c3b5-151">Hashing Algorithms</span></span>



| <span data-ttu-id="2c3b5-152">Nombre</span><span class="sxs-lookup"><span data-stu-id="2c3b5-152">Name</span></span>                               | <span data-ttu-id="2c3b5-153">Notas</span><span class="sxs-lookup"><span data-stu-id="2c3b5-153">Notes</span></span>               | <span data-ttu-id="2c3b5-154">Tamaño de clave en bits (predeterminado/mín./máx.)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-154">Key size in bits (Default/Min/Max)</span></span> |
|------------------------------------|---------------------|------------------------------------|
| <span data-ttu-id="2c3b5-155">Algoritmo hash seguro 1 (SHA1)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-155">Secure Hash Algorithm 1 (SHA1)</span></span>     | <span data-ttu-id="2c3b5-156">Incluye HmacSha1</span><span class="sxs-lookup"><span data-stu-id="2c3b5-156">Includes HmacSha1</span></span>   | <span data-ttu-id="2c3b5-157">160/160/160</span><span class="sxs-lookup"><span data-stu-id="2c3b5-157">160/160/160</span></span>                        |
| <span data-ttu-id="2c3b5-158">Algoritmo hash seguro 256 (SHA256)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-158">Secure Hash Algorithm 256 (SHA256)</span></span> | <span data-ttu-id="2c3b5-159">Incluye HmacSha256</span><span class="sxs-lookup"><span data-stu-id="2c3b5-159">Includes HmacSha256</span></span> | <span data-ttu-id="2c3b5-160">256/256/256</span><span class="sxs-lookup"><span data-stu-id="2c3b5-160">256/256/256</span></span>                        |
| <span data-ttu-id="2c3b5-161">Algoritmo hash seguro 384 (SHA384)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-161">Secure Hash Algorithm 384 (SHA384)</span></span> | <span data-ttu-id="2c3b5-162">Incluye HmacSha384</span><span class="sxs-lookup"><span data-stu-id="2c3b5-162">Includes HmacSha384</span></span> | <span data-ttu-id="2c3b5-163">384/384/384</span><span class="sxs-lookup"><span data-stu-id="2c3b5-163">384/384/384</span></span>                        |
| <span data-ttu-id="2c3b5-164">Algoritmo hash seguro 512 (SHA512)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-164">Secure Hash Algorithm 512 (SHA512)</span></span> | <span data-ttu-id="2c3b5-165">Incluye HmacSha512</span><span class="sxs-lookup"><span data-stu-id="2c3b5-165">Includes HmacSha512</span></span> | <span data-ttu-id="2c3b5-166">512/512/512</span><span class="sxs-lookup"><span data-stu-id="2c3b5-166">512/512/512</span></span>                        |
| <span data-ttu-id="2c3b5-167">Síntesis del mensaje 2 (MD2)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-167">Message Digest 2 (MD2)</span></span>             | <span data-ttu-id="2c3b5-168">Incluye HmacMd2</span><span class="sxs-lookup"><span data-stu-id="2c3b5-168">Includes HmacMd2</span></span>    | <span data-ttu-id="2c3b5-169">128/128/128</span><span class="sxs-lookup"><span data-stu-id="2c3b5-169">128/128/128</span></span>                        |
| <span data-ttu-id="2c3b5-170">Síntesis del mensaje 4 (MD4)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-170">Message Digest 4 (MD4)</span></span>             | <span data-ttu-id="2c3b5-171">Incluye HmacMd4</span><span class="sxs-lookup"><span data-stu-id="2c3b5-171">Includes HmacMd4</span></span>    | <span data-ttu-id="2c3b5-172">128/128/128</span><span class="sxs-lookup"><span data-stu-id="2c3b5-172">128/128/128</span></span>                        |
| <span data-ttu-id="2c3b5-173">Síntesis del mensaje 5 (MD5)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-173">Message Digest 5 (MD5)</span></span>             | <span data-ttu-id="2c3b5-174">Incluye HmacMd5</span><span class="sxs-lookup"><span data-stu-id="2c3b5-174">Includes HmacMd5</span></span>    | <span data-ttu-id="2c3b5-175">128/128/128</span><span class="sxs-lookup"><span data-stu-id="2c3b5-175">128/128/128</span></span>                        |



 

## <a name="key-exchange-algorithms"></a><span data-ttu-id="2c3b5-176">Algoritmos de intercambio de claves</span><span class="sxs-lookup"><span data-stu-id="2c3b5-176">Key Exchange Algorithms</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2c3b5-177">Nombre del algoritmo</span><span class="sxs-lookup"><span data-stu-id="2c3b5-177">Algorithm name</span></span></th>
<th><span data-ttu-id="2c3b5-178">Notas</span><span class="sxs-lookup"><span data-stu-id="2c3b5-178">Notes</span></span></th>
<th><span data-ttu-id="2c3b5-179">Tamaño de clave en bits (predeterminado/mín./máx.)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-179">Key size in bits (Default/Min/Max)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2c3b5-180">Algoritmo de intercambio de claves Diffie-Hellman</span><span class="sxs-lookup"><span data-stu-id="2c3b5-180">Diffie-Hellman Key Exchange Algorithm</span></span></td>

<td><span data-ttu-id="2c3b5-181">de 512 a 4096, en incrementos de 64 bits</span><span class="sxs-lookup"><span data-stu-id="2c3b5-181">512 to 4096, in 64-bit increments</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2c3b5-182">Diffie-Hellman de curva elíptica (ECDH)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-182">Elliptic Curve Diffie-Hellman (ECDH)</span></span></td>
<td><span data-ttu-id="2c3b5-183">Incluye curvas que usan claves públicas 256, 384 y 521 bits como se especifica en SP800-56A.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-183">Includes curves that use 256, 384 and 521 bit public keys as specified in SP800-56A.</span></span></td>
<td><span data-ttu-id="2c3b5-184">256/384/521</span><span class="sxs-lookup"><span data-stu-id="2c3b5-184">256/384/521</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2c3b5-185">Algoritmo de firma digital de curva elíptica (ECDSA)</span><span class="sxs-lookup"><span data-stu-id="2c3b5-185">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span></td>
<td><span data-ttu-id="2c3b5-186">Incluye curvas que usan claves públicas de 256, 384 y 521, tal y como se especifica en FIPS 186-3.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-186">Includes curves that use 256, 384 and 521 bit public keys as specified in FIPS 186-3.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="2c3b5-187">Para mostrar todas las curvas elípticas con nombre, use <strong>certutil displayEccCurve</strong>.</span><span class="sxs-lookup"><span data-stu-id="2c3b5-187">To display all named elliptic curves, use <strong>certutil  displayEccCurve</strong>.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="2c3b5-188">256/384/521</span><span class="sxs-lookup"><span data-stu-id="2c3b5-188">256/384/521</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="2c3b5-189">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2c3b5-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c3b5-190">**Identificadores de algoritmo CNG**</span><span class="sxs-lookup"><span data-stu-id="2c3b5-190">**CNG Algorithm Identifiers**</span></span>](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[<span data-ttu-id="2c3b5-191">Funciones primitivas criptográficas de CNG</span><span class="sxs-lookup"><span data-stu-id="2c3b5-191">CNG Cryptographic Primitive Functions</span></span>](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[<span data-ttu-id="2c3b5-192">Descripción de los proveedores de servicios criptográficos</span><span class="sxs-lookup"><span data-stu-id="2c3b5-192">Understanding Cryptographic Providers</span></span>](understanding-cryptographic-providers.md)
</dt> </dl>

 

