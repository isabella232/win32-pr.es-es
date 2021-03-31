---
description: Se usa con el proveedor de estándar de firma digital (DSS) para exportar claves desde el proveedor de servicios de cifrado (CSP) e importarlas en él.
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: Blobs de clave del proveedor de DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27a73e35cccd6fad672f4c94d589d754f970c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001052"
---
# <a name="dss-provider-key-blobs"></a><span data-ttu-id="3daa9-103">Blobs de clave del proveedor de DSS</span><span class="sxs-lookup"><span data-stu-id="3daa9-103">DSS Provider Key BLOBs</span></span>

<span data-ttu-id="3daa9-104">Los [*blobs*](../secgloss/b-gly.md) se utilizan con el proveedor de [*estándar de firma digital*](../secgloss/d-gly.md) (DSS) para exportar claves desde el proveedor de [*servicios de cifrado*](../secgloss/c-gly.md) (CSP) e importarlas en él.</span><span class="sxs-lookup"><span data-stu-id="3daa9-104">[*BLOBs*](../secgloss/b-gly.md) are used with the [*Digital Signature Standard*](../secgloss/d-gly.md) (DSS) provider to export keys from, and import keys into, the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

-   [<span data-ttu-id="3daa9-105">Blobs de clave pública</span><span class="sxs-lookup"><span data-stu-id="3daa9-105">Public Key BLOBs</span></span>](#public-key-blobs)
-   [<span data-ttu-id="3daa9-106">Blobs de clave privada</span><span class="sxs-lookup"><span data-stu-id="3daa9-106">Private Key BLOBs</span></span>](#private-key-blobs)

## <a name="public-key-blobs"></a><span data-ttu-id="3daa9-107">Blobs de clave pública</span><span class="sxs-lookup"><span data-stu-id="3daa9-107">Public Key BLOBs</span></span>

<span data-ttu-id="3daa9-108">Una [*clave pública*](../secgloss/p-gly.md) de DSS se exporta e importa como un BLOB, una secuencia de bytes estructurada de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="3daa9-108">A DSS [*public key*](../secgloss/p-gly.md) is exported and imported as a BLOB, a sequence of bytes structured as follows.</span></span>

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

<span data-ttu-id="3daa9-109">En la tabla siguiente se describen estos componentes.</span><span class="sxs-lookup"><span data-stu-id="3daa9-109">The following table describes these components.</span></span> <span data-ttu-id="3daa9-110">Todos los valores están en formato [*Little-Endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="3daa9-110">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="3daa9-111">Campo</span><span class="sxs-lookup"><span data-stu-id="3daa9-111">Field</span></span>          | <span data-ttu-id="3daa9-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="3daa9-112">Description</span></span>                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3daa9-113">dsspubkey</span><span class="sxs-lookup"><span data-stu-id="3daa9-113">dsspubkey</span></span>      | <span data-ttu-id="3daa9-114">Estructura [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3daa9-114">A [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) structure.</span></span> <span data-ttu-id="3daa9-115">El miembro **mágico** debe tener un valor de 0x31535344.</span><span class="sxs-lookup"><span data-stu-id="3daa9-115">The **magic** member must have a value of 0x31535344.</span></span> <span data-ttu-id="3daa9-116">Este número hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de DSS1.</span><span class="sxs-lookup"><span data-stu-id="3daa9-116">This hexadecimal number is the [*ASCII*](../secgloss/a-gly.md) encoding of DSS1.</span></span> |
| <span data-ttu-id="3daa9-117">e</span><span class="sxs-lookup"><span data-stu-id="3daa9-117">g</span></span>              | <span data-ttu-id="3daa9-118">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="3daa9-118">A **BYTE** sequence.</span></span> <span data-ttu-id="3daa9-119">El generador, g.</span><span class="sxs-lookup"><span data-stu-id="3daa9-119">The generator, g.</span></span> <span data-ttu-id="3daa9-120">Debe tener la misma longitud que p.</span><span class="sxs-lookup"><span data-stu-id="3daa9-120">Must be the same length as p.</span></span> <span data-ttu-id="3daa9-121">Si no tiene la misma longitud que p, debe rellenarse con 0x00 bytes.</span><span class="sxs-lookup"><span data-stu-id="3daa9-121">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                      |
| <span data-ttu-id="3daa9-122">p</span><span class="sxs-lookup"><span data-stu-id="3daa9-122">p</span></span>              | <span data-ttu-id="3daa9-123">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="3daa9-123">A **BYTE** sequence.</span></span> <span data-ttu-id="3daa9-124">El módulo primo, p.</span><span class="sxs-lookup"><span data-stu-id="3daa9-124">The prime modulus, p.</span></span> <span data-ttu-id="3daa9-125">El bit más significativo del byte más significativo debe establecerse en uno.</span><span class="sxs-lookup"><span data-stu-id="3daa9-125">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                                 |
| <span data-ttu-id="3daa9-126">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="3daa9-126">publickeystruc</span></span> | <span data-ttu-id="3daa9-127">Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="3daa9-127">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                                |
| <span data-ttu-id="3daa9-128">q</span><span class="sxs-lookup"><span data-stu-id="3daa9-128">q</span></span>              | <span data-ttu-id="3daa9-129">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="3daa9-129">A **BYTE** sequence.</span></span> <span data-ttu-id="3daa9-130">La longitud Prime, q, 20 bytes.</span><span class="sxs-lookup"><span data-stu-id="3daa9-130">The prime, q, 20 bytes in length.</span></span> <span data-ttu-id="3daa9-131">El bit más significativo del byte más significativo debe establecerse en uno.</span><span class="sxs-lookup"><span data-stu-id="3daa9-131">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                     |
| <span data-ttu-id="3daa9-132">seedstruct</span><span class="sxs-lookup"><span data-stu-id="3daa9-132">seedstruct</span></span>     | <span data-ttu-id="3daa9-133">Estructura [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) .</span><span class="sxs-lookup"><span data-stu-id="3daa9-133">A [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) structure.</span></span> <span data-ttu-id="3daa9-134">Valores de inicialización y contador para comprobar los primos.</span><span class="sxs-lookup"><span data-stu-id="3daa9-134">Seed and counter values for verifying primes.</span></span>                                                                                                                                |
| <span data-ttu-id="3daa9-135">y</span><span class="sxs-lookup"><span data-stu-id="3daa9-135">y</span></span>              | <span data-ttu-id="3daa9-136">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="3daa9-136">A **BYTE** sequence.</span></span> <span data-ttu-id="3daa9-137">La clave pública, y.</span><span class="sxs-lookup"><span data-stu-id="3daa9-137">The public key, y.</span></span> <span data-ttu-id="3daa9-138">Debe tener la misma longitud que p.</span><span class="sxs-lookup"><span data-stu-id="3daa9-138">Must be same length as p.</span></span> <span data-ttu-id="3daa9-139">Si no tiene la misma longitud que p, debe rellenarse con 0x00 bytes.</span><span class="sxs-lookup"><span data-stu-id="3daa9-139">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                         |



 

> [!Note]  
> <span data-ttu-id="3daa9-140">No se cifran los [*blobs de clave pública*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="3daa9-140">[*Public key BLOBs*](../secgloss/p-gly.md) are not encrypted.</span></span> <span data-ttu-id="3daa9-141">Contienen claves públicas en formato de [*texto simple*](../secgloss/p-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="3daa9-141">They contain public keys in [*plaintext*](../secgloss/p-gly.md) form.</span></span>

 

## <a name="private-key-blobs"></a><span data-ttu-id="3daa9-142">Blobs de clave privada</span><span class="sxs-lookup"><span data-stu-id="3daa9-142">Private Key BLOBs</span></span>

<span data-ttu-id="3daa9-143">Una [*clave privada*](../secgloss/p-gly.md) de DSS se exporta e importa como una secuencia de bytes estructurada como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="3daa9-143">A DSS [*private key*](../secgloss/p-gly.md) is exported and imported as a sequence of bytes structured as follows.</span></span>

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

<span data-ttu-id="3daa9-144">En la tabla siguiente se describe cada componente.</span><span class="sxs-lookup"><span data-stu-id="3daa9-144">The following table describes each component.</span></span> <span data-ttu-id="3daa9-145">Todos los valores están en formato [*Little-Endian*](../secgloss/l-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="3daa9-145">All values are in [*little-endian*](../secgloss/l-gly.md) format.</span></span>



| <span data-ttu-id="3daa9-146">Campo</span><span class="sxs-lookup"><span data-stu-id="3daa9-146">Field</span></span>          | <span data-ttu-id="3daa9-147">Descripción</span><span class="sxs-lookup"><span data-stu-id="3daa9-147">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3daa9-148">dsspubkey</span><span class="sxs-lookup"><span data-stu-id="3daa9-148">dsspubkey</span></span>      | <span data-ttu-id="3daa9-149">Estructura [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3daa9-149">A [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85)) structure.</span></span> <span data-ttu-id="3daa9-150">El miembro **mágico** debe establecerse en 0x32535344.</span><span class="sxs-lookup"><span data-stu-id="3daa9-150">The **magic** member must be set to 0x32535344.</span></span> <span data-ttu-id="3daa9-151">Este número hexadecimal es la codificación [*ASCII*](../secgloss/a-gly.md) de DSS2.</span><span class="sxs-lookup"><span data-stu-id="3daa9-151">This hexadecimal number is the [*ASCII*](../secgloss/a-gly.md) encoding of DSS2.</span></span> |
| <span data-ttu-id="3daa9-152">e</span><span class="sxs-lookup"><span data-stu-id="3daa9-152">g</span></span>              | <span data-ttu-id="3daa9-153">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="3daa9-153">A **BYTE** sequence.</span></span> <span data-ttu-id="3daa9-154">El generador, g.</span><span class="sxs-lookup"><span data-stu-id="3daa9-154">The generator, g.</span></span> <span data-ttu-id="3daa9-155">Debe tener la misma longitud que p.</span><span class="sxs-lookup"><span data-stu-id="3daa9-155">Must be the same length as p.</span></span> <span data-ttu-id="3daa9-156">Si no tiene la misma longitud que p, debe rellenarse con 0x00 bytes.</span><span class="sxs-lookup"><span data-stu-id="3daa9-156">If it is not the same length as p, then it must be padded with 0x00 bytes.</span></span>                                                                |
| <span data-ttu-id="3daa9-157">publickeystruc</span><span class="sxs-lookup"><span data-stu-id="3daa9-157">publickeystruc</span></span> | <span data-ttu-id="3daa9-158">Estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) .</span><span class="sxs-lookup"><span data-stu-id="3daa9-158">A [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) structure.</span></span>                                                                                                                                                          |
| <span data-ttu-id="3daa9-159">p</span><span class="sxs-lookup"><span data-stu-id="3daa9-159">p</span></span>              | <span data-ttu-id="3daa9-160">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="3daa9-160">A **BYTE** sequence.</span></span> <span data-ttu-id="3daa9-161">El módulo primo, p.</span><span class="sxs-lookup"><span data-stu-id="3daa9-161">The prime modulus, p.</span></span> <span data-ttu-id="3daa9-162">El bit más significativo del byte más significativo debe establecerse en uno.</span><span class="sxs-lookup"><span data-stu-id="3daa9-162">The most significant bit of the most significant byte must be set to one.</span></span>                                                                                           |
| <span data-ttu-id="3daa9-163">q</span><span class="sxs-lookup"><span data-stu-id="3daa9-163">q</span></span>              | <span data-ttu-id="3daa9-164">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="3daa9-164">A **BYTE** sequence.</span></span> <span data-ttu-id="3daa9-165">El primo, q.</span><span class="sxs-lookup"><span data-stu-id="3daa9-165">The prime, q.</span></span> <span data-ttu-id="3daa9-166">q tiene una longitud de 20 bytes.</span><span class="sxs-lookup"><span data-stu-id="3daa9-166">q is 20 bytes in length.</span></span> <span data-ttu-id="3daa9-167">El bit más significativo del byte más significativo debe establecerse en uno.</span><span class="sxs-lookup"><span data-stu-id="3daa9-167">The most significant bit of the most significant byte must be set to one.</span></span>                                                                          |
| <span data-ttu-id="3daa9-168">seedstruct</span><span class="sxs-lookup"><span data-stu-id="3daa9-168">seedstruct</span></span>     | <span data-ttu-id="3daa9-169">Estructura [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) .</span><span class="sxs-lookup"><span data-stu-id="3daa9-169">A [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed) structure.</span></span> <span data-ttu-id="3daa9-170">Valores de inicialización y contador para comprobar los primos.</span><span class="sxs-lookup"><span data-stu-id="3daa9-170">Seed and counter values for verifying primes.</span></span>                                                                                                                          |
| <span data-ttu-id="3daa9-171">x</span><span class="sxs-lookup"><span data-stu-id="3daa9-171">x</span></span>              | <span data-ttu-id="3daa9-172">Secuencia de **bytes** .</span><span class="sxs-lookup"><span data-stu-id="3daa9-172">A **BYTE** sequence.</span></span> <span data-ttu-id="3daa9-173">El exponente secreto, x.</span><span class="sxs-lookup"><span data-stu-id="3daa9-173">The secret exponent, x.</span></span> <span data-ttu-id="3daa9-174">Siempre debe tener una longitud de 20 bytes.</span><span class="sxs-lookup"><span data-stu-id="3daa9-174">Must always be 20 bytes in length.</span></span> <span data-ttu-id="3daa9-175">Si x tiene menos de 20 bytes de longitud, debe rellenarse con 0x00.</span><span class="sxs-lookup"><span data-stu-id="3daa9-175">If x is smaller than 20 bytes in length, then it must be padded with 0x00.</span></span>                                                     |



 

<span data-ttu-id="3daa9-176">Al llamar a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), el desarrollador puede elegir si desea cifrar la clave.</span><span class="sxs-lookup"><span data-stu-id="3daa9-176">When calling [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), the developer can choose whether to encrypt the key.</span></span> <span data-ttu-id="3daa9-177">El **PRIVATEKEYBLOB** se cifra si el parámetro *hExpKey* contiene un identificador válido para una clave de sesión.</span><span class="sxs-lookup"><span data-stu-id="3daa9-177">The **PRIVATEKEYBLOB** is encrypted if the *hExpKey* parameter contains a valid handle to a session key.</span></span> <span data-ttu-id="3daa9-178">Todo excepto la parte [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) del BLOB está cifrado.</span><span class="sxs-lookup"><span data-stu-id="3daa9-178">Everything but the [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) portion of the BLOB is encrypted.</span></span>

> [!Note]  
> <span data-ttu-id="3daa9-179">Los parámetros de algoritmo de cifrado y clave de cifrado no se almacenan junto con el BLOB de clave privada.</span><span class="sxs-lookup"><span data-stu-id="3daa9-179">The encryption algorithm and encryption key parameters are not stored along with the private key BLOB.</span></span> <span data-ttu-id="3daa9-180">La aplicación debe administrar y almacenar esta información.</span><span class="sxs-lookup"><span data-stu-id="3daa9-180">The application must manage and store this information.</span></span> <span data-ttu-id="3daa9-181">Si se pasa cero para *hExpKey*, la clave privada se exportará sin cifrado.</span><span class="sxs-lookup"><span data-stu-id="3daa9-181">If zero is passed for *hExpKey*, the private key will be exported without encryption.</span></span>

 

> [!Caution]  
> <span data-ttu-id="3daa9-182">Es peligroso exportar las claves privadas sin cifrado, ya que son vulnerables a la interceptación y el uso por parte de entidades no autorizadas.</span><span class="sxs-lookup"><span data-stu-id="3daa9-182">It is dangerous to export private keys without encryption because they are then vulnerable to interception and use by unauthorized entities.</span></span>

 

 

 
