---
description: Microsoft Enhanced Cryptographic Provider proporciona una aplicación con una seguridad más segura que la que actualmente está disponible con el proveedor de servicios criptográficos de base de Microsoft. Una mayor longitud de clave proporciona a los usuarios más protección para los datos confidenciales.
ms.assetid: cd16705c-c617-4843-a303-52d1019a60bb
title: Comparación de longitud de clave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a82bd4ffe942a58bba4c246f92e83fa1e1ef03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913630"
---
# <a name="key-length-comparison"></a><span data-ttu-id="458ce-104">Comparación de longitud de clave</span><span class="sxs-lookup"><span data-stu-id="458ce-104">Key Length Comparison</span></span>

<span data-ttu-id="458ce-105">Microsoft Enhanced Cryptographic Provider proporciona una aplicación con una seguridad más segura que la que actualmente está disponible con el proveedor de servicios criptográficos de base de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="458ce-105">The Microsoft Enhanced Cryptographic Provider provides an application with stronger security than currently available with the Microsoft Base Cryptographic Provider.</span></span> <span data-ttu-id="458ce-106">Una mayor longitud de clave proporciona a los usuarios más protección para los datos confidenciales.</span><span class="sxs-lookup"><span data-stu-id="458ce-106">Greater key length gives users more protection for sensitive data.</span></span>

<span data-ttu-id="458ce-107">En la tabla siguiente se enumeran las [*longitudes de clave*](../secgloss/k-gly.md) predeterminadas admitidas por el proveedor base y el proveedor mejorado para los algoritmos estándar.</span><span class="sxs-lookup"><span data-stu-id="458ce-107">The following table lists the default [*key lengths*](../secgloss/k-gly.md) supported by the Base Provider and the Enhanced Provider for standard algorithms.</span></span>



| <span data-ttu-id="458ce-108">Algoritmo</span><span class="sxs-lookup"><span data-stu-id="458ce-108">Algorithm</span></span>                                                                                | <span data-ttu-id="458ce-109">Proveedor base</span><span class="sxs-lookup"><span data-stu-id="458ce-109">Base Provider</span></span> | <span data-ttu-id="458ce-110">Proveedores sólidos y mejorados</span><span class="sxs-lookup"><span data-stu-id="458ce-110">Strong and Enhanced Providers</span></span> |
|------------------------------------------------------------------------------------------|---------------|-------------------------------|
| <span data-ttu-id="458ce-111">Intercambio de claves RSA</span><span class="sxs-lookup"><span data-stu-id="458ce-111">RSA Key Exchange</span></span>                                                                         | <span data-ttu-id="458ce-112">512 bits</span><span class="sxs-lookup"><span data-stu-id="458ce-112">512-bit</span></span>       | <span data-ttu-id="458ce-113">1.024 bits</span><span class="sxs-lookup"><span data-stu-id="458ce-113">1,024-bit</span></span>                     |
| <span data-ttu-id="458ce-114">Firma RSA</span><span class="sxs-lookup"><span data-stu-id="458ce-114">RSA Signature</span></span>                                                                            | <span data-ttu-id="458ce-115">512 bits</span><span class="sxs-lookup"><span data-stu-id="458ce-115">512-bit</span></span>       | <span data-ttu-id="458ce-116">1.024 bits</span><span class="sxs-lookup"><span data-stu-id="458ce-116">1,024-bit</span></span>                     |
| <span data-ttu-id="458ce-117">RC2</span><span class="sxs-lookup"><span data-stu-id="458ce-117">RC2</span></span>                                                                                      | <span data-ttu-id="458ce-118">40 bits</span><span class="sxs-lookup"><span data-stu-id="458ce-118">40-bit</span></span>        | <span data-ttu-id="458ce-119">128 bits</span><span class="sxs-lookup"><span data-stu-id="458ce-119">128-bit</span></span>                       |
| <span data-ttu-id="458ce-120">RC4</span><span class="sxs-lookup"><span data-stu-id="458ce-120">RC4</span></span>                                                                                      | <span data-ttu-id="458ce-121">40 bits</span><span class="sxs-lookup"><span data-stu-id="458ce-121">40-bit</span></span>        | <span data-ttu-id="458ce-122">128 bits</span><span class="sxs-lookup"><span data-stu-id="458ce-122">128-bit</span></span>                       |
| <span data-ttu-id="458ce-123">DES</span><span class="sxs-lookup"><span data-stu-id="458ce-123">DES</span></span>                                                                                      | <span data-ttu-id="458ce-124">No compatible</span><span class="sxs-lookup"><span data-stu-id="458ce-124">Not supported</span></span> | <span data-ttu-id="458ce-125">56 bits</span><span class="sxs-lookup"><span data-stu-id="458ce-125">56-bit</span></span>                        |
| <span data-ttu-id="458ce-126">[*Triple des*](../secgloss/t-gly.md) (2 teclas)</span><span class="sxs-lookup"><span data-stu-id="458ce-126">[*Triple DES*](../secgloss/t-gly.md) (2-key)</span></span> | <span data-ttu-id="458ce-127">No compatible</span><span class="sxs-lookup"><span data-stu-id="458ce-127">Not supported</span></span> | <span data-ttu-id="458ce-128">112 bits</span><span class="sxs-lookup"><span data-stu-id="458ce-128">112-bit</span></span>                       |
| <span data-ttu-id="458ce-129">Triple DES (3 teclas)</span><span class="sxs-lookup"><span data-stu-id="458ce-129">Triple DES (3-key)</span></span>                                                                       | <span data-ttu-id="458ce-130">No compatible</span><span class="sxs-lookup"><span data-stu-id="458ce-130">Not supported</span></span> | <span data-ttu-id="458ce-131">168 bits</span><span class="sxs-lookup"><span data-stu-id="458ce-131">168-bit</span></span>                       |



 

<span data-ttu-id="458ce-132">Los algoritmos [*des*](../secgloss/d-gly.md) y [*triple des*](../secgloss/t-gly.md) se admiten en el proveedor mejorado.</span><span class="sxs-lookup"><span data-stu-id="458ce-132">[*DES*](../secgloss/d-gly.md) and [*Triple DES*](../secgloss/t-gly.md) algorithms are supported in the Enhanced Provider.</span></span>

<span data-ttu-id="458ce-133">El proveedor mejorado es compatible con versiones anteriores del proveedor base distribuido con versiones anteriores de CryptoAPI con la siguiente excepción.</span><span class="sxs-lookup"><span data-stu-id="458ce-133">The Enhanced Provider is backward-compatible with the Base Provider distributed with earlier versions of CryptoAPI with the following exception.</span></span> <span data-ttu-id="458ce-134">Tanto el proveedor base como el proveedor mejorado solo pueden generar claves de sesión de longitud de clave predeterminada.</span><span class="sxs-lookup"><span data-stu-id="458ce-134">Both the base provider and the Enhanced Provider can only generate session keys of default key length.</span></span> <span data-ttu-id="458ce-135">La longitud predeterminada de las claves de sesión para el proveedor base es 40 bits.</span><span class="sxs-lookup"><span data-stu-id="458ce-135">The default length of session keys for the Base Provider is 40 bits.</span></span> <span data-ttu-id="458ce-136">La longitud de clave predeterminada para el proveedor mejorado es 128 bits.</span><span class="sxs-lookup"><span data-stu-id="458ce-136">The default key length for the Enhanced Provider is 128 bits.</span></span> <span data-ttu-id="458ce-137">El proveedor mejorado no puede crear claves con longitudes de clave compatibles con el proveedor base.</span><span class="sxs-lookup"><span data-stu-id="458ce-137">The Enhanced Provider cannot create keys with Base Provider-compatible key lengths.</span></span> <span data-ttu-id="458ce-138">Sin embargo, el proveedor mejorado puede importar longitudes de clave de cualquier tamaño, hasta 128 bits.</span><span class="sxs-lookup"><span data-stu-id="458ce-138">However, the Enhanced Provider can import key lengths of any size, up to 128 bits.</span></span>

 

 
