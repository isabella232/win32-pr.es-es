---
description: Los blobs se utilizan con el proveedor de Diffie-Hellman/Schannel para exportar claves desde el proveedor de servicios criptográficos (CSP) e importarlas en él.
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: Blobs de clave Diffie-Hellman/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a76869c6c6239e17a5ae14921805a076c9381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813739"
---
# <a name="diffie-hellmanschannel-key-blobs"></a><span data-ttu-id="c7895-103">Blobs de clave Diffie-Hellman/Schannel</span><span class="sxs-lookup"><span data-stu-id="c7895-103">Diffie-Hellman/Schannel Key BLOBs</span></span>

<span data-ttu-id="c7895-104">Los [*blobs*](../secgloss/b-gly.md) se utilizan con el proveedor de de [*Diffie-Hellman*](../secgloss/d-gly.md) / [*Schannel*](../secgloss/s-gly.md) para exportar claves desde el proveedor de [*servicios de cifrado*](../secgloss/c-gly.md) (CSP), e importarlas en él.</span><span class="sxs-lookup"><span data-stu-id="c7895-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Diffie-Hellman*](../secgloss/d-gly.md)/[*Schannel*](../secgloss/s-gly.md) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="c7895-105">Blobs de clave pública</span><span class="sxs-lookup"><span data-stu-id="c7895-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="c7895-106">Blobs de clave privada</span><span class="sxs-lookup"><span data-stu-id="c7895-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="c7895-107">Blobs de clave pública</span><span class="sxs-lookup"><span data-stu-id="c7895-107">Public Key BLOBs</span></span>

<span data-ttu-id="c7895-108">Diffie-Hellman los [*blobs de clave pública*](../secgloss/p-gly.md), tipo **PUBLICKEYBLOB**, se usan para intercambiar el valor de mod P (G ^ X) en un intercambio de claves Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="c7895-108">Diffie-Hellman [*public key BLOBs*](../secgloss/p-gly.md), type **PUBLICKEYBLOB**, are used to exchange the (G^X) mod P value in a Diffie-Hellman key exchange.</span></span> <span data-ttu-id="c7895-109">Estas claves se exportan e importan como una secuencia de bytes con el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="c7895-109">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

<span data-ttu-id="c7895-110">En la tabla siguiente se describe cada componente del [*BLOB de clave*](../secgloss/k-gly.md).</span><span class="sxs-lookup"><span data-stu-id="c7895-110">The following table describes each component of the [*key BLOB*](../secgloss/k-gly.md).</span></span>



| <span data-ttu-id="c7895-111">Campo</span><span class="sxs-lookup"><span data-stu-id="c7895-111">Field</span></span>          | <span data-ttu-id="c7895-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7895-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7895-113">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="c7895-113">dhpubkey</span></span>       | <span data-ttu-id="c7895-114">Estructura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="c7895-114">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="c7895-115">El miembro **mágico** debe establecerse en 0x31484400.</span><span class="sxs-lookup"><span data-stu-id="c7895-115">The **magic** member must be set to 0x31484400.</span></span> <span data-ttu-id="c7895-116">Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de DH1.</span><span class="sxs-lookup"><span data-stu-id="c7895-116">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of DH1.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="c7895-117">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="c7895-117">publickeystruc</span></span> | <span data-ttu-id="c7895-118">Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="c7895-118">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="c7895-119">y</span><span class="sxs-lookup"><span data-stu-id="c7895-119">y</span></span>              | <span data-ttu-id="c7895-120">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="c7895-120">A **BYTE** sequence.</span></span> <span data-ttu-id="c7895-121">El valor y, (G ^ X) mod P, se encuentra directamente después de la estructura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="c7895-121">The y value, (G^X) mod P, is located directly after the [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="c7895-122">La longitud, en bytes, de la secuencia es el miembro **bitlen** de **DHPUBKEY** dividido por ocho.</span><span class="sxs-lookup"><span data-stu-id="c7895-122">The length, in bytes, of the sequence is the **bitlen** member of **DHPUBKEY** divided by eight.</span></span> <span data-ttu-id="c7895-123">Si la longitud de los datos resultante del cálculo de (G ^ X) mod P es uno o varios bytes más cortos que P divididos por ocho, los datos se deben rellenar con los bytes necesarios (de valor cero) para que los datos tengan la longitud deseada (formato [*Little-Endian*](../secgloss/l-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="c7895-123">If the length of the data that results from the calculation of (G^X) mod P is one or more bytes shorter than P divided by eight, the data must be padded with the necessary bytes (of zero value) to make the data the desired length ([*little-endian*](../secgloss/l-gly.md) format).</span></span> |



 

## <a name="private-key-blobs"></a><span data-ttu-id="c7895-124">Blobs de clave privada</span><span class="sxs-lookup"><span data-stu-id="c7895-124">Private Key BLOBs</span></span>

<span data-ttu-id="c7895-125">Los [*blobs de clave privada*](../secgloss/p-gly.md)d-h, tipo **PRIVATEKEYBLOB**, se usan para exportar e importar información privada de una clave D-H.</span><span class="sxs-lookup"><span data-stu-id="c7895-125">D-H [*private key BLOBs*](../secgloss/p-gly.md), type **PRIVATEKEYBLOB**, are used to export and import private information of a D-H key.</span></span> <span data-ttu-id="c7895-126">Estas claves se exportan e importan como una secuencia de bytes con el siguiente formato.</span><span class="sxs-lookup"><span data-stu-id="c7895-126">These keys are exported and imported as a sequence of bytes with the following format.</span></span>

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

<span data-ttu-id="c7895-127">En la tabla siguiente se describe cada componente del BLOB de clave.</span><span class="sxs-lookup"><span data-stu-id="c7895-127">The following table describes each component of the key BLOB.</span></span>



| <span data-ttu-id="c7895-128">Campo</span><span class="sxs-lookup"><span data-stu-id="c7895-128">Field</span></span>          | <span data-ttu-id="c7895-129">Descripción</span><span class="sxs-lookup"><span data-stu-id="c7895-129">Description</span></span>                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7895-130">dhpubkey</span><span class="sxs-lookup"><span data-stu-id="c7895-130">dhpubkey</span></span>       | <span data-ttu-id="c7895-131">Estructura [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) .</span><span class="sxs-lookup"><span data-stu-id="c7895-131">A [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) structure.</span></span> <span data-ttu-id="c7895-132">El miembro **mágico** debe establecerse en 0x32484400.</span><span class="sxs-lookup"><span data-stu-id="c7895-132">The **magic** member must be set to 0x32484400.</span></span> <span data-ttu-id="c7895-133">Este valor hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de DH2.</span><span class="sxs-lookup"><span data-stu-id="c7895-133">This hexadecimal value is the [*ASCII*](../secgloss/a-gly.md) encoding of DH2.</span></span> |
| <span data-ttu-id="c7895-134">generador</span><span class="sxs-lookup"><span data-stu-id="c7895-134">generator</span></span>      | <span data-ttu-id="c7895-135">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="c7895-135">A **BYTE** sequence.</span></span> <span data-ttu-id="c7895-136">El generador G.</span><span class="sxs-lookup"><span data-stu-id="c7895-136">The generator G.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="c7895-137">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="c7895-137">publickeystruc</span></span> | <span data-ttu-id="c7895-138">Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="c7895-138">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                      |
| <span data-ttu-id="c7895-139">principal</span><span class="sxs-lookup"><span data-stu-id="c7895-139">prime</span></span>          | <span data-ttu-id="c7895-140">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="c7895-140">A **BYTE** sequence.</span></span> <span data-ttu-id="c7895-141">El módulo primo, P. Estos datos siempre deben tener el bit más significativo establecido en uno.</span><span class="sxs-lookup"><span data-stu-id="c7895-141">The prime modulus, P. This data must always have the most significant bit of the most significant byte set to one.</span></span>                                                                    |
| <span data-ttu-id="c7895-142">secret</span><span class="sxs-lookup"><span data-stu-id="c7895-142">secret</span></span>         | <span data-ttu-id="c7895-143">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="c7895-143">A **BYTE** sequence.</span></span> <span data-ttu-id="c7895-144">El exponente secreto X.</span><span class="sxs-lookup"><span data-stu-id="c7895-144">The secret exponent X.</span></span>                                                                                                                                                                |



 

> [!Note]  
> <span data-ttu-id="c7895-145">Los valores primo, generator y secreto siempre deben tener la misma longitud, en bytes.</span><span class="sxs-lookup"><span data-stu-id="c7895-145">The prime, generator, and secret values must always have the same length, in bytes.</span></span> <span data-ttu-id="c7895-146">Si un valor es de un byte o más corto que el resto, debe rellenarse con el número de cero bytes necesario para que sean iguales.</span><span class="sxs-lookup"><span data-stu-id="c7895-146">If any value is one byte or more shorter than the others, it must be padded with the necessary number of zero bytes to make them the same.</span></span> <span data-ttu-id="c7895-147">El primo, el generador y el secreto están en formato [*Little-Endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c7895-147">The prime, generator, and secret are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>

 

 

 
