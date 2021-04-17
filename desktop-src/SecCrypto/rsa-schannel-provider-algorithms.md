---
description: Es posible que el proveedor de servicios criptográficos de Microsoft RSA/Schannel admita los algoritmos.
ms.assetid: 8793f0e8-a368-42be-8351-c60d99c34fb9
title: Algoritmos de proveedor RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9dc3293b0938e9c9e89e955b26eac2a40ac198b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666521"
---
# <a name="rsaschannel-provider-algorithms"></a><span data-ttu-id="c1f6d-103">Algoritmos de proveedor RSA/Schannel</span><span class="sxs-lookup"><span data-stu-id="c1f6d-103">RSA/Schannel Provider Algorithms</span></span>

<span data-ttu-id="c1f6d-104">Es posible que el proveedor de servicios criptográficos de Microsoft [*RSA*](../secgloss/r-gly.md)Schannel admita los siguientes algoritmos / [](../secgloss/s-gly.md) .</span><span class="sxs-lookup"><span data-stu-id="c1f6d-104">The following algorithms might be supported by the Microsoft [*RSA*](../secgloss/r-gly.md)/[*Schannel*](../secgloss/s-gly.md) Cryptographic Provider.</span></span>



| <span data-ttu-id="c1f6d-105">IDENTIFICADOR de algoritmo</span><span class="sxs-lookup"><span data-stu-id="c1f6d-105">Algorithm ID</span></span>    | <span data-ttu-id="c1f6d-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="c1f6d-106">Description</span></span>                                                                                                                         | <span data-ttu-id="c1f6d-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="c1f6d-107">Comments</span></span>                                                                                                        |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1f6d-108">CALG \_ RSA \_ KEYX</span><span class="sxs-lookup"><span data-stu-id="c1f6d-108">CALG\_RSA\_KEYX</span></span> | <span data-ttu-id="c1f6d-109">[ *Algoritmo de intercambio de claves* de clave pública RSA](../secgloss/k-gly.md)</span><span class="sxs-lookup"><span data-stu-id="c1f6d-109">RSA public key [*key exchange algorithm*](../secgloss/k-gly.md)</span></span> | <span data-ttu-id="c1f6d-110">Longitud de clave: se puede establecer, de 384 bits a 16.384 bits en incrementos de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="c1f6d-110">Key length: Can be set, 384 bits to 16,384 bits in 8 bit increments.</span></span> <span data-ttu-id="c1f6d-111">Longitud de clave predeterminada: 1.024 bits.</span><span class="sxs-lookup"><span data-stu-id="c1f6d-111">Default key length: 1,024 bits.</span></span><br/> |
| <span data-ttu-id="c1f6d-112">CALG \_ MD5</span><span class="sxs-lookup"><span data-stu-id="c1f6d-112">CALG\_MD5</span></span>       | <span data-ttu-id="c1f6d-113">Algoritmo de hash MD5.</span><span class="sxs-lookup"><span data-stu-id="c1f6d-113">MD5 hashing algorithm.</span></span>                                                                                                              | <span data-ttu-id="c1f6d-114">Solo se proporciona para el hash.</span><span class="sxs-lookup"><span data-stu-id="c1f6d-114">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="c1f6d-115">CALG \_ Sha</span><span class="sxs-lookup"><span data-stu-id="c1f6d-115">CALG\_SHA</span></span>       | <span data-ttu-id="c1f6d-116">Algoritmo de hash SHA.</span><span class="sxs-lookup"><span data-stu-id="c1f6d-116">SHA hashing algorithm.</span></span>                                                                                                              | <span data-ttu-id="c1f6d-117">Debe usarse para las firmas de DSS.</span><span class="sxs-lookup"><span data-stu-id="c1f6d-117">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="c1f6d-118">CALG \_ RC2</span><span class="sxs-lookup"><span data-stu-id="c1f6d-118">CALG\_RC2</span></span>       | <span data-ttu-id="c1f6d-119">Algoritmo de cifrado de bloques RC2.</span><span class="sxs-lookup"><span data-stu-id="c1f6d-119">RC2 block encryption algorithm.</span></span>                                                                                                     | <span data-ttu-id="c1f6d-120">Longitud de clave: de 40 a 88 bits</span><span class="sxs-lookup"><span data-stu-id="c1f6d-120">Key length: 40 to 88 bits</span></span>                                                                                       |
| <span data-ttu-id="c1f6d-121">CALG \_ RC4</span><span class="sxs-lookup"><span data-stu-id="c1f6d-121">CALG\_RC4</span></span>       | <span data-ttu-id="c1f6d-122">Algoritmo de cifrado de flujo RC4.</span><span class="sxs-lookup"><span data-stu-id="c1f6d-122">RC4 stream encryption algorithm.</span></span>                                                                                                    | <span data-ttu-id="c1f6d-123">Longitud de clave: de 40 a 88 bits</span><span class="sxs-lookup"><span data-stu-id="c1f6d-123">Key length: 40 to 88 bits</span></span>                                                                                       |



 

 

 
