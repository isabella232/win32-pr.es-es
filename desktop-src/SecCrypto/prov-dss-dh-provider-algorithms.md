---
description: Algoritmos admitidos por Microsoft base DSS y Diffie-Hellman proveedor de servicios criptográficos.
ms.assetid: 8db1c7cb-41e0-470b-b927-989da4c09324
title: Algoritmos de proveedor de PROV_DSS_DH
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 098625153d4d447d7290827dcad44a6c78f55561
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105649287"
---
# <a name="prov_dss_dh-provider-algorithms"></a><span data-ttu-id="d0b49-103">\_Algoritmos de proveedor de DSS DSS \_ DH</span><span class="sxs-lookup"><span data-stu-id="d0b49-103">PROV\_DSS\_DH Provider Algorithms</span></span>

<span data-ttu-id="d0b49-104">En la tabla siguiente se enumeran los algoritmos admitidos por Microsoft base DSS y Diffie-Hellman proveedor de servicios criptográficos.</span><span class="sxs-lookup"><span data-stu-id="d0b49-104">The following table lists the algorithms supported by the Microsoft Base DSS and Diffie-Hellman Cryptographic Provider.</span></span>



| <span data-ttu-id="d0b49-105">IDENTIFICADOR de algoritmo</span><span class="sxs-lookup"><span data-stu-id="d0b49-105">Algorithm ID</span></span>      | <span data-ttu-id="d0b49-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0b49-106">Description</span></span>                                 | <span data-ttu-id="d0b49-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d0b49-107">Comments</span></span>                                                                                                        |
|-------------------|---------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b49-108">CALG \_ MD5</span><span class="sxs-lookup"><span data-stu-id="d0b49-108">CALG\_MD5</span></span>         | <span data-ttu-id="d0b49-109">Algoritmo de hash MD5.</span><span class="sxs-lookup"><span data-stu-id="d0b49-109">MD5 hashing algorithm.</span></span>                      | <span data-ttu-id="d0b49-110">Solo se proporciona para el hash.</span><span class="sxs-lookup"><span data-stu-id="d0b49-110">Provided only for hashing.</span></span>                                                                                      |
| <span data-ttu-id="d0b49-111">CALG \_ Sha</span><span class="sxs-lookup"><span data-stu-id="d0b49-111">CALG\_SHA</span></span>         | <span data-ttu-id="d0b49-112">Algoritmo de hash SHA.</span><span class="sxs-lookup"><span data-stu-id="d0b49-112">SHA hashing algorithm.</span></span>                      | <span data-ttu-id="d0b49-113">Debe usarse para las firmas de DSS.</span><span class="sxs-lookup"><span data-stu-id="d0b49-113">Must be used for DSS signatures.</span></span>                                                                                |
| <span data-ttu-id="d0b49-114">CALG \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="d0b49-114">CALG\_SHA1</span></span>        | <span data-ttu-id="d0b49-115">Igual que CALG \_ Sha.</span><span class="sxs-lookup"><span data-stu-id="d0b49-115">Same as CALG\_SHA.</span></span>                          | <span data-ttu-id="d0b49-116">Sin comentarios.</span><span class="sxs-lookup"><span data-stu-id="d0b49-116">No comment.</span></span>                                                                                                     |
| <span data-ttu-id="d0b49-117">\_firma DSS de CALG \_</span><span class="sxs-lookup"><span data-stu-id="d0b49-117">CALG\_DSS\_SIGN</span></span>   | <span data-ttu-id="d0b49-118">Algoritmo de firma de clave pública y privada de DSS.</span><span class="sxs-lookup"><span data-stu-id="d0b49-118">DSS public/private key signature algorithm.</span></span> | <span data-ttu-id="d0b49-119">Longitud de clave: se puede establecer, de 512 bits a 1.024 bits en incrementos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="d0b49-119">Key length: can be set, 512 bits to 1,024 bits in 64 bit increments.</span></span> <span data-ttu-id="d0b49-120">Longitud de clave predeterminada: 1.024 bits.</span><span class="sxs-lookup"><span data-stu-id="d0b49-120">Default key length: 1,024 bits.</span></span><br/> |
| <span data-ttu-id="d0b49-121">CALG \_ DH \_ SF</span><span class="sxs-lookup"><span data-stu-id="d0b49-121">CALG\_DH\_SF</span></span>      | <span data-ttu-id="d0b49-122">Almacenar y reenviar el intercambio de claves D-H.</span><span class="sxs-lookup"><span data-stu-id="d0b49-122">Store and Forward D-H key exchange.</span></span>         | <span data-ttu-id="d0b49-123">Longitud de clave: se puede establecer, de 384 bits a 512 bits en incrementos de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="d0b49-123">Key length: can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="d0b49-124">Longitud de clave predeterminada: 512 bits.</span><span class="sxs-lookup"><span data-stu-id="d0b49-124">Default key length: 512 bits.</span></span><br/>      |
| <span data-ttu-id="d0b49-125">CALG \_ DH \_ EPHEM</span><span class="sxs-lookup"><span data-stu-id="d0b49-125">CALG\_DH\_EPHEM</span></span>   | <span data-ttu-id="d0b49-126">Intercambio de claves en D-H efímero.</span><span class="sxs-lookup"><span data-stu-id="d0b49-126">Ephemeral D-H key exchange.</span></span>                 | <span data-ttu-id="d0b49-127">Longitud de clave: se puede establecer, de 384 bits a 512 bits en incrementos de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="d0b49-127">Key length: can be set, 384 bits to 512 bits in 8 bit increments.</span></span> <span data-ttu-id="d0b49-128">Longitud de clave predeterminada: 512 bits.</span><span class="sxs-lookup"><span data-stu-id="d0b49-128">Default key length: 512 bits.</span></span><br/>      |
| <span data-ttu-id="d0b49-129">CALG \_ CYLINK \_ clave MEK</span><span class="sxs-lookup"><span data-stu-id="d0b49-129">CALG\_CYLINK\_MEK</span></span> | <span data-ttu-id="d0b49-130">Una variante de 40 bits de una clave DES.</span><span class="sxs-lookup"><span data-stu-id="d0b49-130">A 40-bit variant of a DES key.</span></span>              | <span data-ttu-id="d0b49-131">Longitud de clave: 40 bits.</span><span class="sxs-lookup"><span data-stu-id="d0b49-131">Key Length: 40 bits.</span></span>                                                                                            |



 

 

 




