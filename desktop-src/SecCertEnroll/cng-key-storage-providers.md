---
description: 'A diferencia de Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separa los proveedores de servicios criptográficos de los proveedores de almacenamiento de claves (KSP).'
ms.assetid: bd4aadc5-d953-4971-b862-00f6d4db0572
title: Proveedores de almacenamiento de claves CNG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feded42b7796d05e5cec6e255df981b571eb16c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423671"
---
# <a name="cng-key-storage-providers"></a><span data-ttu-id="ebb1b-103">Proveedores de almacenamiento de claves CNG</span><span class="sxs-lookup"><span data-stu-id="ebb1b-103">CNG Key Storage Providers</span></span>

<span data-ttu-id="ebb1b-104">A diferencia de Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separa los proveedores de servicios criptográficos de los proveedores de almacenamiento de claves (KSP).</span><span class="sxs-lookup"><span data-stu-id="ebb1b-104">Unlike Cryptography API (CryptoAPI), Cryptography API: Next Generation (CNG) separates cryptographic providers from key storage providers (KSPs).</span></span> <span data-ttu-id="ebb1b-105">KSP se puede usar para crear, eliminar, exportar, importar, abrir y almacenar claves.</span><span class="sxs-lookup"><span data-stu-id="ebb1b-105">KSPs can be used to create, delete, export, import, open and store keys.</span></span> <span data-ttu-id="ebb1b-106">En función de la implementación, también se pueden usar para el cifrado asimétrico, el acuerdo secreto y la firma.</span><span class="sxs-lookup"><span data-stu-id="ebb1b-106">Depending on implementation, they can also be used for asymmetric encryption, secret agreement, and signing.</span></span> <span data-ttu-id="ebb1b-107">Microsoft instala los siguientes KSP a partir de Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="ebb1b-107">Microsoft installs the following KSPs beginning with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="ebb1b-108">Los proveedores pueden crear e instalar otros proveedores.</span><span class="sxs-lookup"><span data-stu-id="ebb1b-108">Vendors can create and install other providers.</span></span>

## <a name="microsoft-software-key-storage-provider"></a><span data-ttu-id="ebb1b-109">Proveedor de almacenamiento de claves de software de Microsoft</span><span class="sxs-lookup"><span data-stu-id="ebb1b-109">Microsoft Software Key Storage Provider</span></span>

<span data-ttu-id="ebb1b-110">Admite la creación y el almacenamiento de claves de software y los algoritmos siguientes.</span><span class="sxs-lookup"><span data-stu-id="ebb1b-110">Supports software key creation and storage and the following algorithms.</span></span>



| <span data-ttu-id="ebb1b-111">Algoritmo</span><span class="sxs-lookup"><span data-stu-id="ebb1b-111">Algorithm</span></span>                                          | <span data-ttu-id="ebb1b-112">Propósito</span><span class="sxs-lookup"><span data-stu-id="ebb1b-112">Purpose</span></span>                           | <span data-ttu-id="ebb1b-113">Longitud de clave (bits)</span><span class="sxs-lookup"><span data-stu-id="ebb1b-113">Key length (bits)</span></span>                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| <span data-ttu-id="ebb1b-114">Diffie-Hellman (DH)</span><span class="sxs-lookup"><span data-stu-id="ebb1b-114">Diffie-Hellman (DH)</span></span>                                | <span data-ttu-id="ebb1b-115">Acuerdo confidencial e intercambio de claves</span><span class="sxs-lookup"><span data-stu-id="ebb1b-115">Secret agreement and key exchange</span></span> | <span data-ttu-id="ebb1b-116">de 512 a 4096 en incrementos de 64 bits</span><span class="sxs-lookup"><span data-stu-id="ebb1b-116">512 to 4096 in 64-bit increments</span></span>  |
| <span data-ttu-id="ebb1b-117">Algoritmo de firma digital (DSA)</span><span class="sxs-lookup"><span data-stu-id="ebb1b-117">Digital Signature Algorithm (DSA)</span></span>                  | <span data-ttu-id="ebb1b-118">Prototipos</span><span class="sxs-lookup"><span data-stu-id="ebb1b-118">Signatures</span></span>                        | <span data-ttu-id="ebb1b-119">de 512 a 1024 en incrementos de 64 bits</span><span class="sxs-lookup"><span data-stu-id="ebb1b-119">512 to 1024 in 64-bit increments</span></span>  |
| <span data-ttu-id="ebb1b-120">Diffie-Hellman de curva elíptica (ECDH)</span><span class="sxs-lookup"><span data-stu-id="ebb1b-120">Elliptic Curve Diffie-Hellman (ECDH)</span></span>               | <span data-ttu-id="ebb1b-121">Acuerdo confidencial e intercambio de claves</span><span class="sxs-lookup"><span data-stu-id="ebb1b-121">Secret agreement and key exchange</span></span> | <span data-ttu-id="ebb1b-122">P256, CLAVE P384, P521</span><span class="sxs-lookup"><span data-stu-id="ebb1b-122">P256, P384, P521</span></span>                  |
| <span data-ttu-id="ebb1b-123">Algoritmo de firma digital de curva elíptica (ECDSA)</span><span class="sxs-lookup"><span data-stu-id="ebb1b-123">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span> | <span data-ttu-id="ebb1b-124">Prototipos</span><span class="sxs-lookup"><span data-stu-id="ebb1b-124">Signatures</span></span>                        | <span data-ttu-id="ebb1b-125">P256, CLAVE P384, P521</span><span class="sxs-lookup"><span data-stu-id="ebb1b-125">P256, P384, P521</span></span>                  |
| <span data-ttu-id="ebb1b-126">RSA</span><span class="sxs-lookup"><span data-stu-id="ebb1b-126">RSA</span></span>                                                | <span data-ttu-id="ebb1b-127">Firma y cifrado asimétrico</span><span class="sxs-lookup"><span data-stu-id="ebb1b-127">Asymmetric encryption and signing</span></span> | <span data-ttu-id="ebb1b-128">de 512 a 16384 en incrementos de 64 bits</span><span class="sxs-lookup"><span data-stu-id="ebb1b-128">512 to 16384 in 64-bit increments</span></span> |



 

## <a name="microsoft-smart-card-key-storage-provider"></a><span data-ttu-id="ebb1b-129">Proveedor de almacenamiento de claves de tarjeta inteligente de Microsoft</span><span class="sxs-lookup"><span data-stu-id="ebb1b-129">Microsoft Smart Card Key Storage Provider</span></span>

<span data-ttu-id="ebb1b-130">Admite la creación y el almacenamiento de claves de tarjeta inteligente y los algoritmos siguientes.</span><span class="sxs-lookup"><span data-stu-id="ebb1b-130">Supports smart card key creation and storage and the following algorithms.</span></span>



| <span data-ttu-id="ebb1b-131">Algoritmo</span><span class="sxs-lookup"><span data-stu-id="ebb1b-131">Algorithm</span></span>                                          | <span data-ttu-id="ebb1b-132">Propósito</span><span class="sxs-lookup"><span data-stu-id="ebb1b-132">Purpose</span></span>                           | <span data-ttu-id="ebb1b-133">Longitud de clave (bits)</span><span class="sxs-lookup"><span data-stu-id="ebb1b-133">Key length (bits)</span></span>                 |
|----------------------------------------------------|-----------------------------------|-----------------------------------|
| <span data-ttu-id="ebb1b-134">Diffie-Hellman (DH)</span><span class="sxs-lookup"><span data-stu-id="ebb1b-134">Diffie-Hellman (DH)</span></span>                                | <span data-ttu-id="ebb1b-135">Acuerdo confidencial e intercambio de claves</span><span class="sxs-lookup"><span data-stu-id="ebb1b-135">Secret agreement and key exchange</span></span> | <span data-ttu-id="ebb1b-136">de 512 a 4096 en incrementos de 64 bits</span><span class="sxs-lookup"><span data-stu-id="ebb1b-136">512 to 4096 in 64-bit increments</span></span>  |
| <span data-ttu-id="ebb1b-137">Diffie-Hellman de curva elíptica (ECDH)</span><span class="sxs-lookup"><span data-stu-id="ebb1b-137">Elliptic Curve Diffie-Hellman (ECDH)</span></span>               | <span data-ttu-id="ebb1b-138">Acuerdo confidencial e intercambio de claves</span><span class="sxs-lookup"><span data-stu-id="ebb1b-138">Secret agreement and key exchange</span></span> | <span data-ttu-id="ebb1b-139">P256, CLAVE P384, P521</span><span class="sxs-lookup"><span data-stu-id="ebb1b-139">P256, P384, P521</span></span>                  |
| <span data-ttu-id="ebb1b-140">Algoritmo de firma digital de curva elíptica (ECDSA)</span><span class="sxs-lookup"><span data-stu-id="ebb1b-140">Elliptic Curve Digital Signature Algorithm (ECDSA)</span></span> | <span data-ttu-id="ebb1b-141">Prototipos</span><span class="sxs-lookup"><span data-stu-id="ebb1b-141">Signatures</span></span>                        | <span data-ttu-id="ebb1b-142">P256, CLAVE P384, P521</span><span class="sxs-lookup"><span data-stu-id="ebb1b-142">P256, P384, P521</span></span>                  |
| <span data-ttu-id="ebb1b-143">RSA</span><span class="sxs-lookup"><span data-stu-id="ebb1b-143">RSA</span></span>                                                | <span data-ttu-id="ebb1b-144">Firma y cifrado asimétrico</span><span class="sxs-lookup"><span data-stu-id="ebb1b-144">Asymmetric encryption and signing</span></span> | <span data-ttu-id="ebb1b-145">de 512 a 16384 en incrementos de 64 bits</span><span class="sxs-lookup"><span data-stu-id="ebb1b-145">512 to 16384 in 64-bit increments</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ebb1b-146">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ebb1b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebb1b-147">**Identificadores de algoritmo CNG**</span><span class="sxs-lookup"><span data-stu-id="ebb1b-147">**CNG Algorithm Identifiers**</span></span>](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[<span data-ttu-id="ebb1b-148">Funciones de almacenamiento de claves CNG</span><span class="sxs-lookup"><span data-stu-id="ebb1b-148">CNG Key Storage Functions</span></span>](/windows/desktop/SecCNG/cng-key-storage-functions)
</dt> <dt>

[<span data-ttu-id="ebb1b-149">Descripción de los proveedores de servicios criptográficos</span><span class="sxs-lookup"><span data-stu-id="ebb1b-149">Understanding Cryptographic Providers</span></span>](understanding-cryptographic-providers.md)
</dt> </dl>

 

 
