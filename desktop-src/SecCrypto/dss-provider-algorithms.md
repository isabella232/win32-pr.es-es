---
description: En la tabla siguiente se enumeran los algoritmos admitidos por el proveedor de servicios criptográficos de Microsoft DSS.
ms.assetid: 2a7aecf8-e242-4087-83ee-aaa637a9ec71
title: Algoritmos del proveedor de DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0bd9346da7a9ab1490e2646d9d2559c07359b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648377"
---
# <a name="dss-provider-algorithms"></a><span data-ttu-id="dfb8b-103">Algoritmos del proveedor de DSS</span><span class="sxs-lookup"><span data-stu-id="dfb8b-103">DSS Provider Algorithms</span></span>

<span data-ttu-id="dfb8b-104">En la tabla siguiente se enumeran los algoritmos admitidos por el proveedor de servicios criptográficos de Microsoft DSS.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-104">The following table lists the algorithms supported by the Microsoft DSS Cryptographic Provider.</span></span>



| <span data-ttu-id="dfb8b-105">IDENTIFICADOR de algoritmo</span><span class="sxs-lookup"><span data-stu-id="dfb8b-105">Algorithm ID</span></span>    | <span data-ttu-id="dfb8b-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfb8b-106">Description</span></span>                                 | <span data-ttu-id="dfb8b-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="dfb8b-107">Comments</span></span>                                                                                                        |
|-----------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfb8b-108">CALG \_ MD5</span><span class="sxs-lookup"><span data-stu-id="dfb8b-108">CALG\_MD5</span></span>       | <span data-ttu-id="dfb8b-109">Algoritmo de hash MD5.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-109">MD5 hashing algorithm.</span></span>                      | <span data-ttu-id="dfb8b-110">Solo se proporciona para el hash.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-110">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="dfb8b-111">CALG \_ Sha</span><span class="sxs-lookup"><span data-stu-id="dfb8b-111">CALG\_SHA</span></span>       | <span data-ttu-id="dfb8b-112">Algoritmo de hash SHA.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-112">SHA hashing algorithm.</span></span>                      | <span data-ttu-id="dfb8b-113">Debe usarse para las firmas de DSS.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-113">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="dfb8b-114">CALG \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="dfb8b-114">CALG\_SHA1</span></span>      | <span data-ttu-id="dfb8b-115">Igual que CALG \_ Sha.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-115">Same as CALG\_SHA.</span></span>                          | <span data-ttu-id="dfb8b-116">Sin comentarios.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-116">No comment.</span></span>                                                                                                     |
| <span data-ttu-id="dfb8b-117">\_firma DSS de CALG \_</span><span class="sxs-lookup"><span data-stu-id="dfb8b-117">CALG\_DSS\_SIGN</span></span> | <span data-ttu-id="dfb8b-118">Algoritmo de firma de clave pública y privada de DSS.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-118">DSS public/private key signature algorithm.</span></span> | <span data-ttu-id="dfb8b-119">Longitud de clave: se puede establecer, de 512 bits a 1.024 bits en incrementos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-119">Key length: can be set, 512 bits to 1,024 bits in 64 bit increments.</span></span> <span data-ttu-id="dfb8b-120">Longitud de clave predeterminada: 1.024 bits.</span><span class="sxs-lookup"><span data-stu-id="dfb8b-120">Default key length: 1,024 bits.</span></span><br/> |



 

 

 




