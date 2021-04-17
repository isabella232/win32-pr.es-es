---
description: Explica cómo crear un hash CALG \_ de \_ SHAMD5 SSL3.
ms.assetid: dad6fc7f-8abd-4f90-b3e4-8d0169e95087
title: Crear un hash de CALG_SSL3_SHAMD5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f38b5939dc64467ef813b354f33a90f009619f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667716"
---
# <a name="creating-a-calg_ssl3_shamd5-hash"></a><span data-ttu-id="ea320-103">Creación de un \_ hash CALG de \_ SHAMD5 SSL3</span><span class="sxs-lookup"><span data-stu-id="ea320-103">Creating a CALG\_SSL3\_SHAMD5 Hash</span></span>

<span data-ttu-id="ea320-104">**Para crear un \_ \_ hash SHAMD5 de CALG SSL3**</span><span class="sxs-lookup"><span data-stu-id="ea320-104">**To create a CALG\_SSL3\_SHAMD5 hash**</span></span>

1.  <span data-ttu-id="ea320-105">Mediante la metodología estándar de CryptoAPI, cree un hash MD5 y un [*algoritmo hash*](../secgloss/h-gly.md) [*Sha*](../secgloss/s-gly.md) de los datos de destino.</span><span class="sxs-lookup"><span data-stu-id="ea320-105">Using standard CryptoAPI methodology, create both a MD5 and a [*SHA*](../secgloss/s-gly.md) [*hash*](../secgloss/h-gly.md) of the target data.</span></span>
2.  <span data-ttu-id="ea320-106">Concatene los dos hashes, con el valor MD5 a la izquierda y el valor SHA a la derecha.</span><span class="sxs-lookup"><span data-stu-id="ea320-106">Concatenate the two hashes, with the MD5 value leftmost and the SHA value rightmost.</span></span> <span data-ttu-id="ea320-107">Esto da como resultado un valor de 36 byte (16 bytes + 20 bytes).</span><span class="sxs-lookup"><span data-stu-id="ea320-107">This results in a 36-byte value (16 bytes + 20 bytes).</span></span>
3.  <span data-ttu-id="ea320-108">Obtener un identificador de un [*objeto hash*](../secgloss/h-gly.md) llamando a [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) con CALG \_ SSL3 \_ SHAMD5 pasado en el parámetro *algid* .</span><span class="sxs-lookup"><span data-stu-id="ea320-108">Get a handle to a [*hash object*](../secgloss/h-gly.md) by calling [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) with CALG\_SSL3\_SHAMD5 passed in the *Algid* parameter.</span></span>
4.  <span data-ttu-id="ea320-109">Establezca el valor hash con una llamada a [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam).</span><span class="sxs-lookup"><span data-stu-id="ea320-109">Set the hash value with a call to [**CryptSetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam).</span></span> <span data-ttu-id="ea320-110">Los valores hash concatenados se pasan como **bytes** \* en el parámetro *pbData* y el \_ valor HASHVAL de HP se debe pasar en el parámetro *dwParam* .</span><span class="sxs-lookup"><span data-stu-id="ea320-110">The concatenated hash values are passed as a **BYTE**\* in the *pbData* parameter, and the HP\_HASHVAL value must be passed in the *dwParam* parameter.</span></span> <span data-ttu-id="ea320-111">Se producirá un error al llamar a [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) mediante el identificador devuelto por [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) en el paso 3.</span><span class="sxs-lookup"><span data-stu-id="ea320-111">Calling [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) using the handle returned by [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) in step 3 will fail.</span></span>
5.  <span data-ttu-id="ea320-112">Llame a [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) para generar la firma.</span><span class="sxs-lookup"><span data-stu-id="ea320-112">Call [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) to generate the signature.</span></span>
6.  <span data-ttu-id="ea320-113">Llame a [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) para destruir el objeto hash.</span><span class="sxs-lookup"><span data-stu-id="ea320-113">Call [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) to destroy the hash object.</span></span>

 

 
