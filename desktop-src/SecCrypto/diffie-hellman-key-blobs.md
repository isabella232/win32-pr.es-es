---
description: Los blobs se utilizan con el proveedor de Diffie-Hellman para exportar las claves del proveedor de servicios de cifrado (CSP) e importarlas en él.
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: Diffie-Hellman blobs de clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9194a9c12542fc0acf36aa0064a2f3e304e25f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667190"
---
# <a name="diffie-hellman-key-blobs"></a><span data-ttu-id="e9202-103">Diffie-Hellman blobs de clave</span><span class="sxs-lookup"><span data-stu-id="e9202-103">Diffie-Hellman Key BLOBs</span></span>

<span data-ttu-id="e9202-104">Los [*blobs*](../secgloss/b-gly.md) se utilizan con el proveedor de [*Diffie-Hellman*](../secgloss/d-gly.md) para exportar claves desde el [*proveedor de servicios de cifrado*](../secgloss/c-gly.md) (CSP) e importarlas en él.</span><span class="sxs-lookup"><span data-stu-id="e9202-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Diffie-Hellman*](../secgloss/d-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="e9202-105">Blobs de clave pública</span><span class="sxs-lookup"><span data-stu-id="e9202-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="e9202-106">Blobs de clave privada</span><span class="sxs-lookup"><span data-stu-id="e9202-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="e9202-107">Blobs de clave pública</span><span class="sxs-lookup"><span data-stu-id="e9202-107">Public Key BLOBs</span></span>

<span data-ttu-id="e9202-108">Diffie-Hellman los [*blobs de clave pública*](../secgloss/p-gly.md), tipo **PUBLICKEYBLOB**, se usan para intercambiar el valor de mod P (G ^ X) en un intercambio de claves Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="e9202-108">Diffie-Hellman [*public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to exchange the (G^X) mod P value in a Diffie-Hellman key exchange.</span></span> <span data-ttu-id="e9202-109">Estas claves se exportan e importan como una secuencia de bytes con el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="e9202-109">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

<span data-ttu-id="e9202-110">En la tabla siguiente se describe cada componente del [*BLOB de clave*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e9202-110">The following table describes each component of the [*key BLOB*](../secgloss/k-gly.md).</span></span>



| <span data-ttu-id="e9202-111">Campo</span><span class="sxs-lookup"><span data-stu-id="e9202-111">Field</span></span>          | <span data-ttu-id="e9202-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9202-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9202-113">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="e9202-113">dhpubkey</span></span>       | <span data-ttu-id="e9202-114">Estructura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="e9202-114">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="e9202-115">El miembro **mágico** debe establecerse en 0x31484400.</span><span class="sxs-lookup"><span data-stu-id="e9202-115">The **magic** member should be set to 0x31484400.</span></span> <span data-ttu-id="e9202-116">Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de "DH1".</span><span class="sxs-lookup"><span data-stu-id="e9202-116">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of "DH1".</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="e9202-117">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="e9202-117">publickeystruc</span></span> | <span data-ttu-id="e9202-118">Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="e9202-118">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="e9202-119">y</span><span class="sxs-lookup"><span data-stu-id="e9202-119">y</span></span>              | <span data-ttu-id="e9202-120">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="e9202-120">A **BYTE** sequence.</span></span> <span data-ttu-id="e9202-121">El valor Y, (G ^ X) mod P, se encuentra directamente después de la estructura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) y siempre debe ser la longitud, en bytes, del campo **DHPUBKEY bitlen** (longitud de bit de P) dividido entre ocho.</span><span class="sxs-lookup"><span data-stu-id="e9202-121">The Y value, (G^X) mod P, is located directly after the [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure, and should always be the length, in bytes, of the **DHPUBKEY bitlen** field (bit length of P) divided by eight.</span></span> <span data-ttu-id="e9202-122">Si la longitud de los datos resultante del cálculo de (G ^ X) mod P es uno o varios bytes más cortos que P divididos por ocho, los datos se deben rellenar con los bytes necesarios (de valor cero) para que los datos tengan la longitud deseada (formato [*Little-Endian*](../secgloss/l-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="e9202-122">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by eight, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span> |



 

## <a name="private-key-blobs"></a><span data-ttu-id="e9202-123">Blobs de clave privada</span><span class="sxs-lookup"><span data-stu-id="e9202-123">Private Key BLOBs</span></span>

<span data-ttu-id="e9202-124">Diffie-Hellman los [*blobs de clave privada*](../secgloss/p-gly.md), escriba **PRIVATEKEYBLOB**, se usan para almacenar la información pública o privada de una clave de Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="e9202-124">Diffie-Hellman [*private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to store the public/private information of a Diffie-Hellman key.</span></span> <span data-ttu-id="e9202-125">Estas claves se exportan e importan como una secuencia de bytes con el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="e9202-125">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

<span data-ttu-id="e9202-126">En la tabla siguiente se describe cada componente del BLOB de clave.</span><span class="sxs-lookup"><span data-stu-id="e9202-126">The following table describes each component of the key BLOB.</span></span>



| <span data-ttu-id="e9202-127">Campo</span><span class="sxs-lookup"><span data-stu-id="e9202-127">Field</span></span>          | <span data-ttu-id="e9202-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9202-128">Description</span></span>                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9202-129">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="e9202-129">dhpubkey</span></span>       | <span data-ttu-id="e9202-130">Estructura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="e9202-130">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="e9202-131">El miembro **mágico** debe establecerse en 0x32484400.</span><span class="sxs-lookup"><span data-stu-id="e9202-131">The **magic** member must be set to 0x32484400.</span></span> <span data-ttu-id="e9202-132">Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de "DH2".</span><span class="sxs-lookup"><span data-stu-id="e9202-132">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of "DH2".</span></span> |
| <span data-ttu-id="e9202-133">generador</span><span class="sxs-lookup"><span data-stu-id="e9202-133">generator</span></span>      | <span data-ttu-id="e9202-134">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="e9202-134">A **BYTE** sequence.</span></span> <span data-ttu-id="e9202-135">El generador, G.</span><span class="sxs-lookup"><span data-stu-id="e9202-135">The generator, G.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="e9202-136">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="e9202-136">publickeystruc</span></span> | <span data-ttu-id="e9202-137">Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="e9202-137">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                        |
| <span data-ttu-id="e9202-138">principal</span><span class="sxs-lookup"><span data-stu-id="e9202-138">prime</span></span>          | <span data-ttu-id="e9202-139">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="e9202-139">A **BYTE** sequence.</span></span> <span data-ttu-id="e9202-140">El módulo primo, P. Estos datos siempre deben tener el bit más significativo establecido en uno.</span><span class="sxs-lookup"><span data-stu-id="e9202-140">The prime modulus, P. This data must always have the most significant bit of the most significant byte set to one.</span></span>                                                                      |
| <span data-ttu-id="e9202-141">secret</span><span class="sxs-lookup"><span data-stu-id="e9202-141">secret</span></span>         | <span data-ttu-id="e9202-142">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="e9202-142">A **BYTE** sequence.</span></span> <span data-ttu-id="e9202-143">El exponente secreto, X.</span><span class="sxs-lookup"><span data-stu-id="e9202-143">The secret exponent, X.</span></span>                                                                                                                                                                 |



 

> [!Note]  
> <span data-ttu-id="e9202-144">El generador y el secreto deben tener siempre la misma longitud, en bytes.</span><span class="sxs-lookup"><span data-stu-id="e9202-144">The generator and secret must always have the same length, in bytes.</span></span> <span data-ttu-id="e9202-145">Si es un byte o más corto que el otro, se debe rellenar con el número necesario de bytes de valor cero para que sean iguales.</span><span class="sxs-lookup"><span data-stu-id="e9202-145">If either is one byte or more shorter than the other, it must be padded with the necessary number of zero value bytes to make them the same.</span></span> <span data-ttu-id="e9202-146">Tanto el generador como el secreto están en formato [*Little-Endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="e9202-146">Both the generator and the secret are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>

 

 

 
