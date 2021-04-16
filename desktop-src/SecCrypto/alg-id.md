---
description: Especifica un identificador de algoritmo.
ms.assetid: 557436b4-f7f1-4708-acc7-c6b47e6322ad
title: ALG_ID (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ab1eb6dc262faae76d38f2b96c9e6191a313390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669899"
---
# <a name="alg_id"></a><span data-ttu-id="fe6a6-103">ALG_ID</span><span class="sxs-lookup"><span data-stu-id="fe6a6-103">ALG_ID</span></span>

<span data-ttu-id="fe6a6-104">El tipo de datos **ALG_ID** especifica un identificador de algoritmo.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-104">The **ALG_ID** data type specifies an algorithm identifier.</span></span> <span data-ttu-id="fe6a6-105">Los parámetros de este tipo de datos se pasan a la mayoría de las funciones de CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-105">Parameters of this data type are passed to most of the functions in CryptoAPI.</span></span>


```C++
typedef unsigned int ALG_ID;
```



<span data-ttu-id="fe6a6-106">En la tabla siguiente se enumeran los identificadores de algoritmo que están definidos actualmente.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-106">The following table lists the algorithm identifiers that are currently defined.</span></span> <span data-ttu-id="fe6a6-107">Los autores de [*proveedores de servicios criptográficos*](../secgloss/c-gly.md) (CSP) personalizados pueden definir nuevos valores.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-107">Authors of custom [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs) can define new values.</span></span> <span data-ttu-id="fe6a6-108">Además, la **ALG_ID** que usan los CSP personalizados para las especificaciones clave **AT_KEYEXCHANGE** y **AT_SIGNATURE** dependen del proveedor.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-108">Also, the **ALG_ID** used by custom CSPs for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are provider dependent.</span></span> <span data-ttu-id="fe6a6-109">Las asignaciones actuales siguen a la tabla.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-109">Current mappings follow the table.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fe6a6-110">Identificador</span><span class="sxs-lookup"><span data-stu-id="fe6a6-110">Identifier</span></span></th>
<th><span data-ttu-id="fe6a6-111">Value</span><span class="sxs-lookup"><span data-stu-id="fe6a6-111">Value</span></span></th>
<th><span data-ttu-id="fe6a6-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="fe6a6-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fe6a6-113">CALG_3DES</span><span class="sxs-lookup"><span data-stu-id="fe6a6-113">CALG_3DES</span></span></td>
<td><span data-ttu-id="fe6a6-114">0x00006603</span><span class="sxs-lookup"><span data-stu-id="fe6a6-114">0x00006603</span></span></td>
<td><span data-ttu-id="fe6a6-115">Algoritmo de cifrado <a href="/windows/desktop/SecGloss/t-gly"><em>triple des</em></a> .</span><span class="sxs-lookup"><span data-stu-id="fe6a6-115"><a href="/windows/desktop/SecGloss/t-gly"><em>Triple DES</em></a> encryption algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-116">CALG_3DES_112</span><span class="sxs-lookup"><span data-stu-id="fe6a6-116">CALG_3DES_112</span></span></td>
<td><span data-ttu-id="fe6a6-117">0x00006609</span><span class="sxs-lookup"><span data-stu-id="fe6a6-117">0x00006609</span></span></td>
<td><span data-ttu-id="fe6a6-118">Cifrado <a href="/windows/desktop/SecGloss/t-gly"><em>triple des</em></a> de dos claves con una longitud de clave efectiva igual a 112 bits.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-118">Two-key <a href="/windows/desktop/SecGloss/t-gly"><em>triple DES</em></a> encryption with effective key length equal to 112 bits.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-119">CALG_AES</span><span class="sxs-lookup"><span data-stu-id="fe6a6-119">CALG_AES</span></span></td>
<td><span data-ttu-id="fe6a6-120">0x00006611</span><span class="sxs-lookup"><span data-stu-id="fe6a6-120">0x00006611</span></span></td>
<td><span data-ttu-id="fe6a6-121">Estándar de cifrado avanzado (AES).</span><span class="sxs-lookup"><span data-stu-id="fe6a6-121">Advanced Encryption Standard (AES).</span></span> <span data-ttu-id="fe6a6-122">Este algoritmo es compatible con el <a href="microsoft-aes-cryptographic-provider.md">proveedor de servicios criptográficos AES de Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-122">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-123">CALG_AES_128</span><span class="sxs-lookup"><span data-stu-id="fe6a6-123">CALG_AES_128</span></span></td>
<td><span data-ttu-id="fe6a6-124">0x0000660e</span><span class="sxs-lookup"><span data-stu-id="fe6a6-124">0x0000660e</span></span></td>
<td><span data-ttu-id="fe6a6-125">AES de 128 bits.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-125">128 bit AES.</span></span> <span data-ttu-id="fe6a6-126">Este algoritmo es compatible con el <a href="microsoft-aes-cryptographic-provider.md">proveedor de servicios criptográficos AES de Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-126">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-127">CALG_AES_192</span><span class="sxs-lookup"><span data-stu-id="fe6a6-127">CALG_AES_192</span></span></td>
<td><span data-ttu-id="fe6a6-128">0x0000660f</span><span class="sxs-lookup"><span data-stu-id="fe6a6-128">0x0000660f</span></span></td>
<td><span data-ttu-id="fe6a6-129">AES de 192 bits.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-129">192 bit AES.</span></span> <span data-ttu-id="fe6a6-130">Este algoritmo es compatible con el <a href="microsoft-aes-cryptographic-provider.md">proveedor de servicios criptográficos AES de Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-130">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-131">CALG_AES_256</span><span class="sxs-lookup"><span data-stu-id="fe6a6-131">CALG_AES_256</span></span></td>
<td><span data-ttu-id="fe6a6-132">0x00006610</span><span class="sxs-lookup"><span data-stu-id="fe6a6-132">0x00006610</span></span></td>
<td><span data-ttu-id="fe6a6-133">AES de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-133">256 bit AES.</span></span> <span data-ttu-id="fe6a6-134">Este algoritmo es compatible con el <a href="microsoft-aes-cryptographic-provider.md">proveedor de servicios criptográficos AES de Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-134">This algorithm is supported by the <a href="microsoft-aes-cryptographic-provider.md">Microsoft AES Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-135">CALG_AGREEDKEY_ANY</span><span class="sxs-lookup"><span data-stu-id="fe6a6-135">CALG_AGREEDKEY_ANY</span></span></td>
<td><span data-ttu-id="fe6a6-136">0x0000aa03</span><span class="sxs-lookup"><span data-stu-id="fe6a6-136">0x0000aa03</span></span></td>
<td><span data-ttu-id="fe6a6-137">Identificador de algoritmo temporal para los identificadores de Diffie-Hellman: claves acordadas.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-137">Temporary algorithm identifier for handles of Diffie-Hellman–agreed keys.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-138">CALG_CYLINK_MEK</span><span class="sxs-lookup"><span data-stu-id="fe6a6-138">CALG_CYLINK_MEK</span></span></td>
<td><span data-ttu-id="fe6a6-139">0x0000660c</span><span class="sxs-lookup"><span data-stu-id="fe6a6-139">0x0000660c</span></span></td>
<td><span data-ttu-id="fe6a6-140">Un algoritmo para crear una clave DES de 40 bits con bits de paridad y bits de clave con ceros para que la longitud de la clave sea 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-140">An algorithm to create a 40-bit DES key that has parity bits and zeroed key bits to make its key length 64 bits.</span></span> <span data-ttu-id="fe6a6-141">Este algoritmo es compatible con el <a href=""></a> <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-141">This algorithm is supported by the <a href=""></a><a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-142">CALG_DES</span><span class="sxs-lookup"><span data-stu-id="fe6a6-142">CALG_DES</span></span></td>
<td><span data-ttu-id="fe6a6-143">0x00006601</span><span class="sxs-lookup"><span data-stu-id="fe6a6-143">0x00006601</span></span></td>
<td><span data-ttu-id="fe6a6-144">Algoritmo de cifrado DES.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-144">DES encryption algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-145">CALG_DESX</span><span class="sxs-lookup"><span data-stu-id="fe6a6-145">CALG_DESX</span></span></td>
<td><span data-ttu-id="fe6a6-146">0x00006604</span><span class="sxs-lookup"><span data-stu-id="fe6a6-146">0x00006604</span></span></td>
<td><span data-ttu-id="fe6a6-147">Algoritmo de cifrado DESX.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-147">DESX encryption algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-148">CALG_DH_EPHEM</span><span class="sxs-lookup"><span data-stu-id="fe6a6-148">CALG_DH_EPHEM</span></span></td>
<td><span data-ttu-id="fe6a6-149">0x0000aa02</span><span class="sxs-lookup"><span data-stu-id="fe6a6-149">0x0000aa02</span></span></td>
<td><span data-ttu-id="fe6a6-150">Algoritmo de intercambio de claves efímeras Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-150">Diffie-Hellman ephemeral key exchange algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-151">CALG_DH_SF</span><span class="sxs-lookup"><span data-stu-id="fe6a6-151">CALG_DH_SF</span></span></td>
<td><span data-ttu-id="fe6a6-152">0x0000aa01</span><span class="sxs-lookup"><span data-stu-id="fe6a6-152">0x0000aa01</span></span></td>
<td><span data-ttu-id="fe6a6-153">Diffie-Hellman el algoritmo de intercambio de claves de almacenamiento y reenvío.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-153">Diffie-Hellman store and forward key exchange algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-154">CALG_DSS_SIGN</span><span class="sxs-lookup"><span data-stu-id="fe6a6-154">CALG_DSS_SIGN</span></span></td>
<td><span data-ttu-id="fe6a6-155">0x00002200</span><span class="sxs-lookup"><span data-stu-id="fe6a6-155">0x00002200</span></span></td>
<td><span data-ttu-id="fe6a6-156">Algoritmo de firma de <a href="/windows/desktop/SecGloss/p-gly"><em>clave pública</em></a> DSA.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-156">DSA <a href="/windows/desktop/SecGloss/p-gly"><em>public key</em></a> signature algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-157">CALG_ECDH</span><span class="sxs-lookup"><span data-stu-id="fe6a6-157">CALG_ECDH</span></span></td>
<td><span data-ttu-id="fe6a6-158">0x0000aa05</span><span class="sxs-lookup"><span data-stu-id="fe6a6-158">0x0000aa05</span></span></td>
<td><span data-ttu-id="fe6a6-159">Algoritmo de intercambio de claves de curva elíptica Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-159">Elliptic curve Diffie-Hellman key exchange algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fe6a6-160">Este algoritmo solo se admite a través de <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-160">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe6a6-161"><strong>Windows Server 2003 y Windows XP:</strong> Este algoritmo no es compatible.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-161"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-162">CALG_ECDH_EPHEM</span><span class="sxs-lookup"><span data-stu-id="fe6a6-162">CALG_ECDH_EPHEM</span></span></td>
<td><span data-ttu-id="fe6a6-163">0x0000ae06</span><span class="sxs-lookup"><span data-stu-id="fe6a6-163">0x0000ae06</span></span></td>
<td><span data-ttu-id="fe6a6-164">Curva elíptica efímera Diffie-Hellman algoritmo de intercambio de claves.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-164">Ephemeral elliptic curve Diffie-Hellman key exchange algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fe6a6-165">Este algoritmo solo se admite a través de <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-165">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe6a6-166"><strong>Windows Server 2003 y Windows XP:</strong> Este algoritmo no es compatible.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-166"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-167">CALG_ECDSA</span><span class="sxs-lookup"><span data-stu-id="fe6a6-167">CALG_ECDSA</span></span></td>
<td><span data-ttu-id="fe6a6-168">0x00002203</span><span class="sxs-lookup"><span data-stu-id="fe6a6-168">0x00002203</span></span></td>
<td><span data-ttu-id="fe6a6-169">Algoritmo de firma digital de curva elíptica.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-169">Elliptic curve digital signature algorithm.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="fe6a6-170">Este algoritmo solo se admite a través de <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-170">This algorithm is supported only through <a href="/windows/desktop/SecCNG/cng-portal">Cryptography API: Next Generation</a>.</span></span>
</blockquote>
<br/> <span data-ttu-id="fe6a6-171"><strong>Windows Server 2003 y Windows XP:</strong> Este algoritmo no es compatible.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-171"><strong>Windows Server 2003 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-172">CALG_ECMQV</span><span class="sxs-lookup"><span data-stu-id="fe6a6-172">CALG_ECMQV</span></span></td>
<td><span data-ttu-id="fe6a6-173">0x0000a001</span><span class="sxs-lookup"><span data-stu-id="fe6a6-173">0x0000a001</span></span></td>
<td><span data-ttu-id="fe6a6-174">Algoritmo de intercambio de claves de curva elíptica Menezes, qu y Vanstone (MQV).</span><span class="sxs-lookup"><span data-stu-id="fe6a6-174">Elliptic curve Menezes, Qu, and Vanstone (MQV) key exchange algorithm.</span></span> <span data-ttu-id="fe6a6-175">Este algoritmo no es compatible.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-175">This algorithm is not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-176">CALG_HASH_REPLACE_OWF</span><span class="sxs-lookup"><span data-stu-id="fe6a6-176">CALG_HASH_REPLACE_OWF</span></span></td>
<td><span data-ttu-id="fe6a6-177">0x0000800b</span><span class="sxs-lookup"><span data-stu-id="fe6a6-177">0x0000800b</span></span></td>
<td><span data-ttu-id="fe6a6-178">Algoritmo hash de función unidireccional.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-178">One way function hashing algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-179">CALG_HUGHES_MD5</span><span class="sxs-lookup"><span data-stu-id="fe6a6-179">CALG_HUGHES_MD5</span></span></td>
<td><span data-ttu-id="fe6a6-180">0x0000a003</span><span class="sxs-lookup"><span data-stu-id="fe6a6-180">0x0000a003</span></span></td>
<td><span data-ttu-id="fe6a6-181">Algoritmo hash de Hughes MD5.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-181">Hughes MD5 hashing algorithm.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-182">CALG_HMAC</span><span class="sxs-lookup"><span data-stu-id="fe6a6-182">CALG_HMAC</span></span></td>
<td><span data-ttu-id="fe6a6-183">0x00008009</span><span class="sxs-lookup"><span data-stu-id="fe6a6-183">0x00008009</span></span></td>
<td><span data-ttu-id="fe6a6-184">Algoritmo hash con clave HMAC.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-184">HMAC keyed hash algorithm.</span></span> <span data-ttu-id="fe6a6-185">Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-185">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-186">CALG_KEA_KEYX</span><span class="sxs-lookup"><span data-stu-id="fe6a6-186">CALG_KEA_KEYX</span></span></td>
<td><span data-ttu-id="fe6a6-187">0x0000aa04</span><span class="sxs-lookup"><span data-stu-id="fe6a6-187">0x0000aa04</span></span></td>
<td><span data-ttu-id="fe6a6-188">Algoritmo de intercambio de claves de KEA (FORTEZZA).</span><span class="sxs-lookup"><span data-stu-id="fe6a6-188">KEA key exchange algorithm (FORTEZZA).</span></span> <span data-ttu-id="fe6a6-189">Este algoritmo no es compatible.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-189">This algorithm is not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-190">CALG_MAC</span><span class="sxs-lookup"><span data-stu-id="fe6a6-190">CALG_MAC</span></span></td>
<td><span data-ttu-id="fe6a6-191">0x00008005</span><span class="sxs-lookup"><span data-stu-id="fe6a6-191">0x00008005</span></span></td>
<td><span data-ttu-id="fe6a6-192">Algoritmo hash con clave de <a href="/windows/desktop/SecGloss/m-gly"><em>Mac</em></a> .</span><span class="sxs-lookup"><span data-stu-id="fe6a6-192"><a href="/windows/desktop/SecGloss/m-gly"><em>MAC</em></a> keyed hash algorithm.</span></span> <span data-ttu-id="fe6a6-193">Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-193">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-194">CALG_MD2</span><span class="sxs-lookup"><span data-stu-id="fe6a6-194">CALG_MD2</span></span></td>
<td><span data-ttu-id="fe6a6-195">0x00008001</span><span class="sxs-lookup"><span data-stu-id="fe6a6-195">0x00008001</span></span></td>
<td><span data-ttu-id="fe6a6-196">Algoritmo de hash MD2.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-196">MD2 hashing algorithm.</span></span> <span data-ttu-id="fe6a6-197">Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-197">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-198">CALG_MD4</span><span class="sxs-lookup"><span data-stu-id="fe6a6-198">CALG_MD4</span></span></td>
<td><span data-ttu-id="fe6a6-199">0x00008002</span><span class="sxs-lookup"><span data-stu-id="fe6a6-199">0x00008002</span></span></td>
<td><span data-ttu-id="fe6a6-200">Algoritmo de hash MD4.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-200">MD4 hashing algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-201">CALG_MD5</span><span class="sxs-lookup"><span data-stu-id="fe6a6-201">CALG_MD5</span></span></td>
<td><span data-ttu-id="fe6a6-202">0x00008003</span><span class="sxs-lookup"><span data-stu-id="fe6a6-202">0x00008003</span></span></td>
<td><span data-ttu-id="fe6a6-203">Algoritmo de hash MD5.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-203">MD5 hashing algorithm.</span></span> <span data-ttu-id="fe6a6-204">Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-204">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-205">CALG_NO_SIGN</span><span class="sxs-lookup"><span data-stu-id="fe6a6-205">CALG_NO_SIGN</span></span></td>
<td><span data-ttu-id="fe6a6-206">0x00002000</span><span class="sxs-lookup"><span data-stu-id="fe6a6-206">0x00002000</span></span></td>
<td><span data-ttu-id="fe6a6-207">No hay ningún algoritmo de firma.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-207">No signature algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-208">CALG_OID_INFO_CNG_ONLY</span><span class="sxs-lookup"><span data-stu-id="fe6a6-208">CALG_OID_INFO_CNG_ONLY</span></span></td>
<td><span data-ttu-id="fe6a6-209">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="fe6a6-209">0xffffffff</span></span></td>
<td><span data-ttu-id="fe6a6-210">El algoritmo solo se implementa en CNG.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-210">The algorithm is only implemented in CNG.</span></span> <span data-ttu-id="fe6a6-211">La macro, IS_SPECIAL_OID_INFO_ALGID, se puede usar para determinar si un algoritmo de criptografía solo se admite mediante las funciones de CNG.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-211">The macro, IS_SPECIAL_OID_INFO_ALGID, can be used to determine whether a cryptography algorithm is only supported by using the CNG functions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-212">CALG_OID_INFO_PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe6a6-212">CALG_OID_INFO_PARAMETERS</span></span></td>
<td><span data-ttu-id="fe6a6-213">0xfffffffe</span><span class="sxs-lookup"><span data-stu-id="fe6a6-213">0xfffffffe</span></span></td>
<td><span data-ttu-id="fe6a6-214">El algoritmo se define en los parámetros codificados.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-214">The algorithm is defined in the encoded parameters.</span></span> <span data-ttu-id="fe6a6-215">El algoritmo solo se admite mediante CNG.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-215">The algorithm is only supported by using CNG.</span></span> <span data-ttu-id="fe6a6-216">La macro, IS_SPECIAL_OID_INFO_ALGID, se puede usar para determinar si un algoritmo de criptografía solo se admite mediante las funciones de CNG.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-216">The macro, IS_SPECIAL_OID_INFO_ALGID, can be used to determine whether a cryptography algorithm is only supported by using the CNG functions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-217">CALG_PCT1_MASTER</span><span class="sxs-lookup"><span data-stu-id="fe6a6-217">CALG_PCT1_MASTER</span></span></td>
<td><span data-ttu-id="fe6a6-218">0x00004c04</span><span class="sxs-lookup"><span data-stu-id="fe6a6-218">0x00004c04</span></span></td>
<td><span data-ttu-id="fe6a6-219">Lo usa el sistema de operaciones de Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-219">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="fe6a6-220">Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</span><span class="sxs-lookup"><span data-stu-id="fe6a6-220">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-221">CALG_RC2</span><span class="sxs-lookup"><span data-stu-id="fe6a6-221">CALG_RC2</span></span></td>
<td><span data-ttu-id="fe6a6-222">0x00006602</span><span class="sxs-lookup"><span data-stu-id="fe6a6-222">0x00006602</span></span></td>
<td><span data-ttu-id="fe6a6-223">Algoritmo de cifrado de bloques RC2.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-223">RC2 block encryption algorithm.</span></span> <span data-ttu-id="fe6a6-224">Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-224">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-225">CALG_RC4</span><span class="sxs-lookup"><span data-stu-id="fe6a6-225">CALG_RC4</span></span></td>
<td><span data-ttu-id="fe6a6-226">0x00006801</span><span class="sxs-lookup"><span data-stu-id="fe6a6-226">0x00006801</span></span></td>
<td><span data-ttu-id="fe6a6-227">Algoritmo de cifrado de flujo RC4.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-227">RC4 stream encryption algorithm.</span></span> <span data-ttu-id="fe6a6-228">Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-228">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-229">CALG_RC5</span><span class="sxs-lookup"><span data-stu-id="fe6a6-229">CALG_RC5</span></span></td>
<td><span data-ttu-id="fe6a6-230">0x0000660d</span><span class="sxs-lookup"><span data-stu-id="fe6a6-230">0x0000660d</span></span></td>
<td><span data-ttu-id="fe6a6-231">Algoritmo de cifrado de bloque RC5.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-231">RC5 block encryption algorithm.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-232">CALG_RSA_KEYX</span><span class="sxs-lookup"><span data-stu-id="fe6a6-232">CALG_RSA_KEYX</span></span></td>
<td><span data-ttu-id="fe6a6-233">0x0000a400</span><span class="sxs-lookup"><span data-stu-id="fe6a6-233">0x0000a400</span></span></td>
<td><span data-ttu-id="fe6a6-234">Algoritmo de intercambio de claves públicas RSA.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-234">RSA public key exchange algorithm.</span></span> <span data-ttu-id="fe6a6-235">Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-235">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-236">CALG_RSA_SIGN</span><span class="sxs-lookup"><span data-stu-id="fe6a6-236">CALG_RSA_SIGN</span></span></td>
<td><span data-ttu-id="fe6a6-237">0x00002400</span><span class="sxs-lookup"><span data-stu-id="fe6a6-237">0x00002400</span></span></td>
<td><span data-ttu-id="fe6a6-238">Algoritmo de firma de clave pública RSA.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-238">RSA public key signature algorithm.</span></span> <span data-ttu-id="fe6a6-239">Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-239">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-240">CALG_SCHANNEL_ENC_KEY</span><span class="sxs-lookup"><span data-stu-id="fe6a6-240">CALG_SCHANNEL_ENC_KEY</span></span></td>
<td><span data-ttu-id="fe6a6-241">0x00004c07</span><span class="sxs-lookup"><span data-stu-id="fe6a6-241">0x00004c07</span></span></td>
<td><span data-ttu-id="fe6a6-242">Lo usa el sistema de operaciones de Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-242">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="fe6a6-243">Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</span><span class="sxs-lookup"><span data-stu-id="fe6a6-243">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-244">CALG_SCHANNEL_MAC_KEY</span><span class="sxs-lookup"><span data-stu-id="fe6a6-244">CALG_SCHANNEL_MAC_KEY</span></span></td>
<td><span data-ttu-id="fe6a6-245">0x00004c03</span><span class="sxs-lookup"><span data-stu-id="fe6a6-245">0x00004c03</span></span></td>
<td><span data-ttu-id="fe6a6-246">Lo usa el sistema de operaciones de Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-246">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="fe6a6-247">Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</span><span class="sxs-lookup"><span data-stu-id="fe6a6-247">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-248">CALG_SCHANNEL_MASTER_HASH</span><span class="sxs-lookup"><span data-stu-id="fe6a6-248">CALG_SCHANNEL_MASTER_HASH</span></span></td>
<td><span data-ttu-id="fe6a6-249">0x00004c02</span><span class="sxs-lookup"><span data-stu-id="fe6a6-249">0x00004c02</span></span></td>
<td><span data-ttu-id="fe6a6-250">Lo usa el sistema de operaciones de Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-250">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="fe6a6-251">Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</span><span class="sxs-lookup"><span data-stu-id="fe6a6-251">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-252">CALG_SEAL</span><span class="sxs-lookup"><span data-stu-id="fe6a6-252">CALG_SEAL</span></span></td>
<td><span data-ttu-id="fe6a6-253">0x00006802</span><span class="sxs-lookup"><span data-stu-id="fe6a6-253">0x00006802</span></span></td>
<td><span data-ttu-id="fe6a6-254">El algoritmo de cifrado de sellado.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-254">SEAL encryption algorithm.</span></span> <span data-ttu-id="fe6a6-255">Este algoritmo no es compatible.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-255">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-256">CALG_SHA</span><span class="sxs-lookup"><span data-stu-id="fe6a6-256">CALG_SHA</span></span></td>
<td><span data-ttu-id="fe6a6-257">0x00008004</span><span class="sxs-lookup"><span data-stu-id="fe6a6-257">0x00008004</span></span></td>
<td><span data-ttu-id="fe6a6-258">Algoritmo de hash SHA.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-258">SHA hashing algorithm.</span></span> <span data-ttu-id="fe6a6-259">Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-259">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-260">CALG_SHA1</span><span class="sxs-lookup"><span data-stu-id="fe6a6-260">CALG_SHA1</span></span></td>
<td><span data-ttu-id="fe6a6-261">0x00008004</span><span class="sxs-lookup"><span data-stu-id="fe6a6-261">0x00008004</span></span></td>
<td><span data-ttu-id="fe6a6-262">Igual que <strong>CALG_SHA</strong>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-262">Same as <strong>CALG_SHA</strong>.</span></span> <span data-ttu-id="fe6a6-263">Este algoritmo es compatible con el <a href="microsoft-base-cryptographic-provider.md">proveedor de servicios criptográficos de base de Microsoft</a>.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-263">This algorithm is supported by the <a href="microsoft-base-cryptographic-provider.md">Microsoft Base Cryptographic Provider</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-264">CALG_SHA_256</span><span class="sxs-lookup"><span data-stu-id="fe6a6-264">CALG_SHA_256</span></span></td>
<td><span data-ttu-id="fe6a6-265">0x0000800c</span><span class="sxs-lookup"><span data-stu-id="fe6a6-265">0x0000800c</span></span></td>
<td><span data-ttu-id="fe6a6-266">algoritmo hash SHA 256 bits.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-266">256 bit SHA hashing algorithm.</span></span> <span data-ttu-id="fe6a6-267">Este algoritmo es compatible con el proveedor de servicios criptográficos RSA y AES mejorado de Microsoft. <strong>Windows XP con SP3:</strong> Este algoritmo es compatible con el proveedor de servicios criptográficos (Prototype) de AES y RSA mejorado de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-267">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider..<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="fe6a6-268"><strong>Windows XP con SP2, Windows XP con SP1 y Windows XP:</strong> Este algoritmo no es compatible.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-268"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-269">CALG_SHA_384</span><span class="sxs-lookup"><span data-stu-id="fe6a6-269">CALG_SHA_384</span></span></td>
<td><span data-ttu-id="fe6a6-270">0x0000800d</span><span class="sxs-lookup"><span data-stu-id="fe6a6-270">0x0000800d</span></span></td>
<td><span data-ttu-id="fe6a6-271">algoritmo hash SHA 384 bits.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-271">384 bit SHA hashing algorithm.</span></span> <span data-ttu-id="fe6a6-272">Este algoritmo es compatible con el proveedor de servicios criptográficos RSA y AES mejorado de Microsoft. <strong>Windows XP con SP3:</strong> Este algoritmo es compatible con el proveedor de servicios criptográficos (Prototype) de AES y RSA mejorado de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-272">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider.<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="fe6a6-273"><strong>Windows XP con SP2, Windows XP con SP1 y Windows XP:</strong> Este algoritmo no es compatible.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-273"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-274">CALG_SHA_512</span><span class="sxs-lookup"><span data-stu-id="fe6a6-274">CALG_SHA_512</span></span></td>
<td><span data-ttu-id="fe6a6-275">0x0000800e</span><span class="sxs-lookup"><span data-stu-id="fe6a6-275">0x0000800e</span></span></td>
<td><span data-ttu-id="fe6a6-276">algoritmo hash SHA 512 bits.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-276">512 bit SHA hashing algorithm.</span></span> <span data-ttu-id="fe6a6-277">Este algoritmo es compatible con el proveedor de servicios criptográficos RSA y AES mejorado de Microsoft. <strong>Windows XP con SP3:</strong> Este algoritmo es compatible con el proveedor de servicios criptográficos (Prototype) de AES y RSA mejorado de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-277">This algorithm is supported by Microsoft Enhanced RSA and AES Cryptographic Provider.<strong>Windows XP with SP3:</strong> This algorithm is supported by the Microsoft Enhanced RSA and AES Cryptographic Provider (Prototype).</span></span><br/> <span data-ttu-id="fe6a6-278"><strong>Windows XP con SP2, Windows XP con SP1 y Windows XP:</strong> Este algoritmo no es compatible.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-278"><strong>Windows XP with SP2, Windows XP with SP1 and Windows XP:</strong> This algorithm is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-279">CALG_SKIPJACK</span><span class="sxs-lookup"><span data-stu-id="fe6a6-279">CALG_SKIPJACK</span></span></td>
<td><span data-ttu-id="fe6a6-280">0x0000660a</span><span class="sxs-lookup"><span data-stu-id="fe6a6-280">0x0000660a</span></span></td>
<td><span data-ttu-id="fe6a6-281">Algoritmo de cifrado de bloque Skipjack (FORTEZZA).</span><span class="sxs-lookup"><span data-stu-id="fe6a6-281">Skipjack block encryption algorithm (FORTEZZA).</span></span> <span data-ttu-id="fe6a6-282">Este algoritmo no es compatible.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-282">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-283">CALG_SSL2_MASTER</span><span class="sxs-lookup"><span data-stu-id="fe6a6-283">CALG_SSL2_MASTER</span></span></td>
<td><span data-ttu-id="fe6a6-284">0x00004c05</span><span class="sxs-lookup"><span data-stu-id="fe6a6-284">0x00004c05</span></span></td>
<td><span data-ttu-id="fe6a6-285">Lo usa el sistema de operaciones de Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-285">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="fe6a6-286">Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</span><span class="sxs-lookup"><span data-stu-id="fe6a6-286">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-287">CALG_SSL3_MASTER</span><span class="sxs-lookup"><span data-stu-id="fe6a6-287">CALG_SSL3_MASTER</span></span></td>
<td><span data-ttu-id="fe6a6-288">0x00004c01</span><span class="sxs-lookup"><span data-stu-id="fe6a6-288">0x00004c01</span></span></td>
<td><span data-ttu-id="fe6a6-289">Lo usa el sistema de operaciones de Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-289">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="fe6a6-290">Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</span><span class="sxs-lookup"><span data-stu-id="fe6a6-290">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-291">CALG_SSL3_SHAMD5</span><span class="sxs-lookup"><span data-stu-id="fe6a6-291">CALG_SSL3_SHAMD5</span></span></td>
<td><span data-ttu-id="fe6a6-292">0x00008008</span><span class="sxs-lookup"><span data-stu-id="fe6a6-292">0x00008008</span></span></td>
<td><span data-ttu-id="fe6a6-293">Lo usa el sistema de operaciones de Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-293">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="fe6a6-294">Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</span><span class="sxs-lookup"><span data-stu-id="fe6a6-294">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-295">CALG_TEK</span><span class="sxs-lookup"><span data-stu-id="fe6a6-295">CALG_TEK</span></span></td>
<td><span data-ttu-id="fe6a6-296">0x0000660b</span><span class="sxs-lookup"><span data-stu-id="fe6a6-296">0x0000660b</span></span></td>
<td><span data-ttu-id="fe6a6-297">TEK (FORTEZZA).</span><span class="sxs-lookup"><span data-stu-id="fe6a6-297">TEK (FORTEZZA).</span></span> <span data-ttu-id="fe6a6-298">Este algoritmo no es compatible.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-298">This algorithm is not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fe6a6-299">CALG_TLS1_MASTER</span><span class="sxs-lookup"><span data-stu-id="fe6a6-299">CALG_TLS1_MASTER</span></span></td>
<td><span data-ttu-id="fe6a6-300">0x00004c06</span><span class="sxs-lookup"><span data-stu-id="fe6a6-300">0x00004c06</span></span></td>
<td><span data-ttu-id="fe6a6-301">Lo usa el sistema de operaciones de Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-301">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="fe6a6-302">Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</span><span class="sxs-lookup"><span data-stu-id="fe6a6-302">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fe6a6-303">CALG_TLS1PRF</span><span class="sxs-lookup"><span data-stu-id="fe6a6-303">CALG_TLS1PRF</span></span></td>
<td><span data-ttu-id="fe6a6-304">0x0000800a</span><span class="sxs-lookup"><span data-stu-id="fe6a6-304">0x0000800a</span></span></td>
<td><span data-ttu-id="fe6a6-305">Lo usa el sistema de operaciones de Schannel.dll.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-305">Used by the Schannel.dll operations system.</span></span> <span data-ttu-id="fe6a6-306">Las aplicaciones no deben usar este <strong>ALG_ID</strong> .</span><span class="sxs-lookup"><span data-stu-id="fe6a6-306">This <strong>ALG_ID</strong> should not be used by applications.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="fe6a6-307">Para el proveedor de servicios criptográficos [básicos](microsoft-base-cryptographic-provider.md)de Microsoft, el [proveedor de servicios](microsoft-strong-cryptographic-provider.md)criptográficos seguros de Microsoft y el [proveedor de servicios criptográficos mejorados de Microsoft](microsoft-enhanced-cryptographic-provider.md), los **ALG_IDs** que se usan para las especificaciones clave **AT_KEYEXCHANGE** y **AT_SIGNATURE** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="fe6a6-307">For the [Microsoft Base Cryptographic Provider](microsoft-base-cryptographic-provider.md), the [Microsoft Strong Cryptographic Provider](microsoft-strong-cryptographic-provider.md), and the [Microsoft Enhanced Cryptographic Provider](microsoft-enhanced-cryptographic-provider.md), the **ALG_IDs** used for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are as follows:</span></span>

-   <span data-ttu-id="fe6a6-308">**CALG_RSA_KEYX** se utiliza para **AT_KEYEXCHANGE**.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-308">**CALG_RSA_KEYX** is used for **AT_KEYEXCHANGE**.</span></span>
-   <span data-ttu-id="fe6a6-309">**CALG_RSA_SIGN** se utiliza para **AT_SIGNATURE**.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-309">**CALG_RSA_SIGN** is used for **AT_SIGNATURE**.</span></span>

<span data-ttu-id="fe6a6-310">En el caso de [Microsoft base DSS y Diffie-Hellman proveedor de servicios criptográficos](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), el **ALG_IDs** que se usa para las especificaciones clave **AT_KEYEXCHANGE** y **AT_SIGNATURE** son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="fe6a6-310">For the [Microsoft Base DSS and Diffie-Hellman Cryptographic Provider](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md), the **ALG_IDs** used for the key specifications **AT_KEYEXCHANGE** and **AT_SIGNATURE** are as follows:</span></span>

-   <span data-ttu-id="fe6a6-311">**CALG_DH_SF** se utiliza para **AT_KEYEXCHANGE**.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-311">**CALG_DH_SF** is used for **AT_KEYEXCHANGE**.</span></span>
-   <span data-ttu-id="fe6a6-312">**CALG_DSS_SIGN** se utiliza para **AT_SIGNATURE**.</span><span class="sxs-lookup"><span data-stu-id="fe6a6-312">**CALG_DSS_SIGN** is used for **AT_SIGNATURE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe6a6-313">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe6a6-313">Requirements</span></span>



| <span data-ttu-id="fe6a6-314">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe6a6-314">Requirement</span></span> | <span data-ttu-id="fe6a6-315">Value</span><span class="sxs-lookup"><span data-stu-id="fe6a6-315">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fe6a6-316">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe6a6-316">Minimum supported client</span></span><br/> | <span data-ttu-id="fe6a6-317">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="fe6a6-317">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fe6a6-318">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fe6a6-318">Minimum supported server</span></span><br/> | <span data-ttu-id="fe6a6-319">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fe6a6-319">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fe6a6-320">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fe6a6-320">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe6a6-321"><dt>Wincrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe6a6-321"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe6a6-322">Vea también</span><span class="sxs-lookup"><span data-stu-id="fe6a6-322">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe6a6-323">Funciones de criptografía</span><span class="sxs-lookup"><span data-stu-id="fe6a6-323">Cryptography Functions</span></span>](cryptography-functions.md)
</dt> <dt>

[<span data-ttu-id="fe6a6-324">**CRYPT_ALGORITHM_IDENTIFIER**</span><span class="sxs-lookup"><span data-stu-id="fe6a6-324">**CRYPT_ALGORITHM_IDENTIFIER**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_algorithm_identifier)
</dt> <dt>

[<span data-ttu-id="fe6a6-325">**CryptFindOIDInfo**</span><span class="sxs-lookup"><span data-stu-id="fe6a6-325">**CryptFindOIDInfo**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> </dl>

 

 
