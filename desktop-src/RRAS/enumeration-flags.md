---
title: Marcas de enumeración
description: Marcas de enumeración
ms.assetid: d5677e3a-c0c1-4768-aae4-f6564a40ee99
keywords:
- Enumeración
- Marcas de enumeración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1cbec08496ccd6338de77ebdddf76547a48258
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994237"
---
# <a name="enumeration-flags"></a><span data-ttu-id="bf9d9-105">Marcas de enumeración</span><span class="sxs-lookup"><span data-stu-id="bf9d9-105">Enumeration Flags</span></span>



| <span data-ttu-id="bf9d9-106">Constante</span><span class="sxs-lookup"><span data-stu-id="bf9d9-106">Constant</span></span>               | <span data-ttu-id="bf9d9-107">Value</span><span class="sxs-lookup"><span data-stu-id="bf9d9-107">Value</span></span>      | <span data-ttu-id="bf9d9-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="bf9d9-108">Description</span></span>                                                                                                                                               |
|------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf9d9-109">Inicio de la \_ enumeración RTM \_</span><span class="sxs-lookup"><span data-stu-id="bf9d9-109">RTM\_ENUM\_START</span></span>       | <span data-ttu-id="bf9d9-110">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf9d9-110">0x00000000</span></span> | <span data-ttu-id="bf9d9-111">Enumerar rutas o destinos a partir de 0/0.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-111">Enumerate routes or destinations starting at 0/0.</span></span>                                                                                                         |
| <span data-ttu-id="bf9d9-112">\_siguiente enumeración RTM \_</span><span class="sxs-lookup"><span data-stu-id="bf9d9-112">RTM\_ENUM\_NEXT</span></span>        | <span data-ttu-id="bf9d9-113">0x00000001</span><span class="sxs-lookup"><span data-stu-id="bf9d9-113">0x00000001</span></span> | <span data-ttu-id="bf9d9-114">Enumerar rutas o destinos a partir de la longitud especificada de máscara/dirección (por ejemplo, 10/8).</span><span class="sxs-lookup"><span data-stu-id="bf9d9-114">Enumerate routes or destinations starting at the specified address/mask length (such as 10/8).</span></span> <span data-ttu-id="bf9d9-115">La enumeración continúa hasta el final de la tabla de enrutamiento.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-115">The enumeration continues to the end of the routing table.</span></span> |
| <span data-ttu-id="bf9d9-116">\_intervalo enum de RTM \_</span><span class="sxs-lookup"><span data-stu-id="bf9d9-116">RTM\_ENUM\_RANGE</span></span>       | <span data-ttu-id="bf9d9-117">0x00000002</span><span class="sxs-lookup"><span data-stu-id="bf9d9-117">0x00000002</span></span> | <span data-ttu-id="bf9d9-118">Enumerar rutas o destinos en el subárbol especificado especificados por la longitud de dirección/máscara (por ejemplo, 10/8).</span><span class="sxs-lookup"><span data-stu-id="bf9d9-118">Enumerate routes or destinations in the specified subtree specified by the address/mask length (such as 10/8).</span></span>                                            |
| <span data-ttu-id="bf9d9-119">\_enumeración de \_ todos los \_ DESTs de RTM</span><span class="sxs-lookup"><span data-stu-id="bf9d9-119">RTM\_ENUM\_ALL\_DESTS</span></span>  | <span data-ttu-id="bf9d9-120">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf9d9-120">0x00000000</span></span> | <span data-ttu-id="bf9d9-121">Devuelve todos los destinos.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-121">Return all destinations.</span></span>                                                                                                                                  |
| <span data-ttu-id="bf9d9-122">\_destino enum \_ de la versión RTM \_</span><span class="sxs-lookup"><span data-stu-id="bf9d9-122">RTM\_ENUM\_OWN\_DESTS</span></span>  | <span data-ttu-id="bf9d9-123">0x01000000</span><span class="sxs-lookup"><span data-stu-id="bf9d9-123">0x01000000</span></span> | <span data-ttu-id="bf9d9-124">Devuelve solo los destinos que posee el cliente.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-124">Return only those destinations that the client owns.</span></span>                                                                                                      |
| <span data-ttu-id="bf9d9-125">versión RTM \_ enumerar \_ todas las \_ rutas</span><span class="sxs-lookup"><span data-stu-id="bf9d9-125">RTM\_ENUM\_ALL\_ROUTES</span></span> | <span data-ttu-id="bf9d9-126">0x00000000</span><span class="sxs-lookup"><span data-stu-id="bf9d9-126">0x00000000</span></span> | <span data-ttu-id="bf9d9-127">Devuelve todas las rutas.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-127">Return all routes.</span></span>                                                                                                                                        |
| <span data-ttu-id="bf9d9-128">las \_ rutas de enumeración de RTM son \_ propias \_</span><span class="sxs-lookup"><span data-stu-id="bf9d9-128">RTM\_ENUM\_OWN\_ROUTES</span></span> | <span data-ttu-id="bf9d9-129">0x00010000</span><span class="sxs-lookup"><span data-stu-id="bf9d9-129">0x00010000</span></span> | <span data-ttu-id="bf9d9-130">Devuelve solo las rutas que posee el cliente.</span><span class="sxs-lookup"><span data-stu-id="bf9d9-130">Return only those routes that the client owns.</span></span>                                                                                                            |



 

 

 




