---
description: Un hash de un texto u otra cadena de bytes es un valor de longitud fija, estadísticamente único y asociado.
ms.assetid: e54d5a3b-cae1-47dd-a565-7bf1ccef7f52
title: Hashes de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed785c79bef67f5a54b0d91c0c2686f8fd1b967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913045"
---
# <a name="data-hashes"></a><span data-ttu-id="0075d-103">Hashes de datos</span><span class="sxs-lookup"><span data-stu-id="0075d-103">Data Hashes</span></span>

<span data-ttu-id="0075d-104">Un [*hash*](../secgloss/h-gly.md) de un texto u otra cadena de bytes es un valor de longitud fija, estadísticamente único y asociado.</span><span class="sxs-lookup"><span data-stu-id="0075d-104">A [*hash*](../secgloss/h-gly.md) of a text or other string of bytes is an associated, statistically unique, fixed-length value.</span></span> <span data-ttu-id="0075d-105">En algunos documentos, un *hash* de un texto también se denomina síntesis; sin embargo, en esta documentación se usará siempre el término hash.</span><span class="sxs-lookup"><span data-stu-id="0075d-105">In some documents, a *hash* of a text is also called a digest; however, in this documentation the term hash will always be used.</span></span> <span data-ttu-id="0075d-106">Las funciones CryptoAPI proporcionan un medio para crear un hash para cualquier texto u otra cadena de bytes.</span><span class="sxs-lookup"><span data-stu-id="0075d-106">CryptoAPI functions provide a means to create a hash for any text or other string of bytes.</span></span> <span data-ttu-id="0075d-107">Ese hash, a continuación, se puede usar como identificador único de sus datos asociados.</span><span class="sxs-lookup"><span data-stu-id="0075d-107">That hash, then, can be used as a unique identifier of its associated data.</span></span>

<span data-ttu-id="0075d-108">Para garantizar la [*integridad*](../secgloss/i-gly.md) de un texto, se puede enviar un [*hash*](../secgloss/h-gly.md) de un texto para acompañar el texto.</span><span class="sxs-lookup"><span data-stu-id="0075d-108">To ensure the [*integrity*](../secgloss/i-gly.md) of a text, a [*hash*](../secgloss/h-gly.md) of a text can be sent to accompany the text.</span></span> <span data-ttu-id="0075d-109">A continuación, el receptor puede calcular un hash en los datos recibidos y comparar el hash calculado con el hash recibido.</span><span class="sxs-lookup"><span data-stu-id="0075d-109">The receiver can then compute a hash on the data received and compare the hash computed with the hash received.</span></span> <span data-ttu-id="0075d-110">Si los dos coinciden, los datos recibidos deben ser los mismos que los datos de los que se creó el hash recibido.</span><span class="sxs-lookup"><span data-stu-id="0075d-110">If the two match, the data received must be the same as the data from which the received hash was created.</span></span>

<span data-ttu-id="0075d-111">Para obtener un valor hash, cree un objeto hash mediante [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span><span class="sxs-lookup"><span data-stu-id="0075d-111">To obtain a hash value, create a hash object using [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash).</span></span> <span data-ttu-id="0075d-112">Este objeto acumulará los datos que se van a comprobar.</span><span class="sxs-lookup"><span data-stu-id="0075d-112">This object will accumulate the data to be verified.</span></span> <span data-ttu-id="0075d-113">A continuación, los datos se agregan al objeto hash con la función [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) .</span><span class="sxs-lookup"><span data-stu-id="0075d-113">The data is then added to the hash object with the [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) function.</span></span>

<span data-ttu-id="0075d-114">Después de agregar el último bloque de datos al hash, se usa la función [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) para obtener el valor hash de los datos.</span><span class="sxs-lookup"><span data-stu-id="0075d-114">After the last block of data is added to the hash, the [**CryptGetHashParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam) function is used to obtain the hash value of the data.</span></span>

<span data-ttu-id="0075d-115">Se proporciona una mejor seguridad al destruir el objeto hash con [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) en cuanto se obtiene el valor hash.</span><span class="sxs-lookup"><span data-stu-id="0075d-115">Better security is provided by destroying the hash object with [**CryptDestroyHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash) as soon as the hash value has been obtained.</span></span>

 

 
