---
description: Para comprobar una firma, cree un objeto hash mediante CryptCreateHash. Este objeto hash acumula los datos que se van a comprobar. A continuación, los datos se agregan al objeto hash con la función CryptHashData.
ms.assetid: 3779f83b-0d87-4f47-949b-9eb39690adfb
title: Comprobar una firma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9a416dc2c3f7523af781e68fe78b066accbe6d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155072"
---
# <a name="verifying-a-signature"></a><span data-ttu-id="bb4f3-105">Comprobar una firma</span><span class="sxs-lookup"><span data-stu-id="bb4f3-105">Verifying a Signature</span></span>

<span data-ttu-id="bb4f3-106">Para comprobar una firma, cree un [*objeto hash*](../secgloss/h-gly.md) mediante [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="bb4f3-106">To verify a signature, create a [*hash object*](../secgloss/h-gly.md) using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="bb4f3-107">Este objeto hash acumula los datos que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="bb4f3-107">This hash object accumulates the data to be verified.</span></span> <span data-ttu-id="bb4f3-108">A continuación, los datos se agregan al objeto hash con la función [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .</span><span class="sxs-lookup"><span data-stu-id="bb4f3-108">The data is then added to the hash object with the [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) function.</span></span>

<span data-ttu-id="bb4f3-109">Después de agregar el último bloque de datos al hash, use [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) para comprobar la firma.</span><span class="sxs-lookup"><span data-stu-id="bb4f3-109">After the last block of data is added to the hash, use [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) to verify the signature.</span></span> <span data-ttu-id="bb4f3-110">La dirección de los datos de la firma, un identificador para el objeto hash y el identificador de las claves públicas se pasan a **CryptVerifySignature**.</span><span class="sxs-lookup"><span data-stu-id="bb4f3-110">The address of the signature data, a handle to the hash object, and the handle of the public keys are passed to **CryptVerifySignature**.</span></span>

<span data-ttu-id="bb4f3-111">Una vez comprobada la firma (o no haya superado la comprobación), destruya el objeto hash mediante la función [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) .</span><span class="sxs-lookup"><span data-stu-id="bb4f3-111">After the signature has been verified (or has failed the verification), destroy the hash object using the [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) function.</span></span>

 

 
