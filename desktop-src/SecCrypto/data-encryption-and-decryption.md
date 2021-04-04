---
description: El cifrado es el proceso de traducir los datos de texto sin formato (texto simple) en algo que parece ser aleatorio e insignificante (texto cifrado). El descifrado es el proceso de convertir texto cifrado de nuevo en texto sin formato.
ms.assetid: 6a4b5c82-f74c-4cc8-b824-690f165453bd
title: Cifrado y descifrado de datos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfa6f9633cabf4a41aec59d9224c2579acb7a983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154083"
---
# <a name="data-encryption-and-decryption"></a><span data-ttu-id="f4dc5-104">Cifrado y descifrado de datos</span><span class="sxs-lookup"><span data-stu-id="f4dc5-104">Data Encryption and Decryption</span></span>

<span data-ttu-id="f4dc5-105">El cifrado es el proceso de traducir los datos de texto sin formato ([*texto simple*](../secgloss/p-gly.md)) en algo que parece ser aleatorio e insignificante ([*texto cifrado*](../secgloss/c-gly.md)).</span><span class="sxs-lookup"><span data-stu-id="f4dc5-105">Encryption is the process of translating plain text data ([*plaintext*](../secgloss/p-gly.md)) into something that appears to be random and meaningless ([*ciphertext*](../secgloss/c-gly.md)).</span></span> <span data-ttu-id="f4dc5-106">El descifrado es el proceso de convertir texto cifrado de nuevo en texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="f4dc5-106">Decryption is the process of converting ciphertext back to plaintext.</span></span>

<span data-ttu-id="f4dc5-107">Para cifrar más que una pequeña cantidad de datos, se usa el [*cifrado simétrico*](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="f4dc5-107">To encrypt more than a small amount of data, [*symmetric encryption*](../secgloss/s-gly.md) is used.</span></span> <span data-ttu-id="f4dc5-108">Se utiliza una [*clave simétrica*](../secgloss/s-gly.md) durante los procesos de cifrado y descifrado.</span><span class="sxs-lookup"><span data-stu-id="f4dc5-108">A [*symmetric key*](../secgloss/s-gly.md) is used during both the encryption and decryption processes.</span></span> <span data-ttu-id="f4dc5-109">Para descifrar un fragmento determinado de texto cifrado, se debe usar la clave utilizada para cifrar los datos.</span><span class="sxs-lookup"><span data-stu-id="f4dc5-109">To decrypt a particular piece of ciphertext, the key that was used to encrypt the data must be used.</span></span>

<span data-ttu-id="f4dc5-110">El objetivo de todos los algoritmos de cifrado es que sea lo más difícil posible para descifrar el texto cifrado generado sin utilizar la clave.</span><span class="sxs-lookup"><span data-stu-id="f4dc5-110">The goal of every encryption algorithm is to make it as difficult as possible to decrypt the generated ciphertext without using the key.</span></span> <span data-ttu-id="f4dc5-111">Si se usa un algoritmo de cifrado realmente bueno, no hay ninguna técnica significativamente mejor que probar cada clave posible.</span><span class="sxs-lookup"><span data-stu-id="f4dc5-111">If a really good encryption algorithm is used, there is no technique significantly better than methodically trying every possible key.</span></span> <span data-ttu-id="f4dc5-112">Para este tipo de algoritmo, cuanto más larga sea la clave, más difícil será descifrar un fragmento de texto sin poseer la clave.</span><span class="sxs-lookup"><span data-stu-id="f4dc5-112">For such an algorithm, the longer the key, the more difficult it is to decrypt a piece of ciphertext without possessing the key.</span></span>

<span data-ttu-id="f4dc5-113">Es difícil determinar la calidad de un algoritmo de cifrado.</span><span class="sxs-lookup"><span data-stu-id="f4dc5-113">It is difficult to determine the quality of an encryption algorithm.</span></span> <span data-ttu-id="f4dc5-114">Los algoritmos que buscan el compromiso a veces resultan muy fáciles de romper, dado el ataque adecuado.</span><span class="sxs-lookup"><span data-stu-id="f4dc5-114">Algorithms that look promising sometimes turn out to be very easy to break, given the proper attack.</span></span> <span data-ttu-id="f4dc5-115">Al seleccionar un algoritmo de cifrado, se recomienda elegir uno que se haya usado durante varios años y que se hayan aprovechado correctamente todos los ataques.</span><span class="sxs-lookup"><span data-stu-id="f4dc5-115">When selecting an encryption algorithm, it is a good idea to choose one that has been in use for several years and has successfully resisted all attacks.</span></span>

<span data-ttu-id="f4dc5-116">Para obtener más información, vea [funciones de cifrado y descifrado de datos](cryptography-functions.md).</span><span class="sxs-lookup"><span data-stu-id="f4dc5-116">For more information, see [Data Encryption and Decryption Functions](cryptography-functions.md).</span></span>

 

 
