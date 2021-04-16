---
description: Establece o recupera el tipo de algoritmo hash que se usa.
ms.assetid: 3f8e83f2-0e46-494b-ac63-658e663680ea
title: HashedData. algorithm (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- HashedData.Algorithm
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: a27dc275ce900bfd6412599cb81ad14038f96405
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690108"
---
# <a name="hasheddataalgorithm-property"></a><span data-ttu-id="9703a-103">HashedData. algorithm (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9703a-103">HashedData.Algorithm property</span></span>

<span data-ttu-id="9703a-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="9703a-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="9703a-105">En su lugar, use la [**clase HashAlgorithm**](/previous-versions/windows/) en el espacio de nombres [**System. Security. Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="9703a-105">Instead, use the [**HashAlgorithm Class**](/previous-versions/windows/) in the [**System.Security.Cryptography**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="9703a-106">La propiedad del **algoritmo** establece o recupera el tipo de algoritmo hash que se usa.</span><span class="sxs-lookup"><span data-stu-id="9703a-106">The **Algorithm** property sets or retrieves the type of hashing algorithm used.</span></span>

## <a name="syntax"></a><span data-ttu-id="9703a-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9703a-107">Syntax</span></span>


```VB
HashedData.Algorithm As CAPICOM_HASH_ALGORITHM
```



## <a name="property-value"></a><span data-ttu-id="9703a-108">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9703a-108">Property value</span></span>

<span data-ttu-id="9703a-109">Un valor de la enumeración del [**\_ \_ algoritmo hash CAPICOM**](capicom-hash-algorithm.md) que define un algoritmo hash.</span><span class="sxs-lookup"><span data-stu-id="9703a-109">A value of the [**CAPICOM\_HASH\_ALGORITHM**](capicom-hash-algorithm.md) enumeration that defines a hash algorithm.</span></span> <span data-ttu-id="9703a-110">El valor predeterminado es el \_ algoritmo hash de CAPICOM \_ \_ SHA1.</span><span class="sxs-lookup"><span data-stu-id="9703a-110">The default value is CAPICOM\_HASH\_ALGORITHM\_SHA1.</span></span> <span data-ttu-id="9703a-111">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="9703a-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="9703a-112">Valor</span><span class="sxs-lookup"><span data-stu-id="9703a-112">Value</span></span>                                                                                                                                                                                                               | <span data-ttu-id="9703a-113">Significado</span><span class="sxs-lookup"><span data-stu-id="9703a-113">Meaning</span></span>                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_HASH_ALGORITHM_SHA1"></span><span id="capicom_hash_algorithm_sha1"></span><dl> <span data-ttu-id="9703a-114"><dt>**\_Algoritmo hash de CAPICOM \_ \_ SHA1**</dt></span><span class="sxs-lookup"><span data-stu-id="9703a-114"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA1**</dt></span></span> </dl>           | <span data-ttu-id="9703a-115">Algoritmo hash SHA1.</span><span class="sxs-lookup"><span data-stu-id="9703a-115">SHA1 hashing algorithm.</span></span><br/>                                                                          |
| <span id="CAPICOM_HASH_ALGORITHM_MD2"></span><span id="capicom_hash_algorithm_md2"></span><dl> <span data-ttu-id="9703a-116"><dt>**\_Algoritmo hash de CAPICOM \_ \_ MD2**</dt></span><span class="sxs-lookup"><span data-stu-id="9703a-116"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD2**</dt></span></span> </dl>              | <span data-ttu-id="9703a-117">Algoritmo de hash MD2.</span><span class="sxs-lookup"><span data-stu-id="9703a-117">MD2 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD4"></span><span id="capicom_hash_algorithm_md4"></span><dl> <span data-ttu-id="9703a-118"><dt>**\_Algoritmo hash \_ CAPICOM \_ MD4**</dt></span><span class="sxs-lookup"><span data-stu-id="9703a-118"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD4**</dt></span></span> </dl>              | <span data-ttu-id="9703a-119">Algoritmo de hash MD4.</span><span class="sxs-lookup"><span data-stu-id="9703a-119">MD4 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_MD5"></span><span id="capicom_hash_algorithm_md5"></span><dl> <span data-ttu-id="9703a-120"><dt>**\_Algoritmo hash de CAPICOM \_ \_ MD5**</dt></span><span class="sxs-lookup"><span data-stu-id="9703a-120"><dt>**CAPICOM\_HASH\_ALGORITHM\_MD5**</dt></span></span> </dl>              | <span data-ttu-id="9703a-121">Algoritmo de hash MD5.</span><span class="sxs-lookup"><span data-stu-id="9703a-121">MD5 hashing algorithm.</span></span><br/>                                                                           |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_256"></span><span id="capicom_hash_algorithm_sha_256"></span><dl> <span data-ttu-id="9703a-122"><dt>**\_Algoritmo hash de CAPICOM \_ \_ Sha \_ 256**</dt></span><span class="sxs-lookup"><span data-stu-id="9703a-122"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_256**</dt></span></span> </dl> | <span data-ttu-id="9703a-123">Algoritmo hash SHA-256.</span><span class="sxs-lookup"><span data-stu-id="9703a-123">SHA-256 hash algorithm.</span></span><br/> <span data-ttu-id="9703a-124">**CAPICOM 2.0.0.3 y versiones anteriores:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="9703a-124">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_384"></span><span id="capicom_hash_algorithm_sha_384"></span><dl> <span data-ttu-id="9703a-125"><dt>**\_Algoritmo hash de CAPICOM \_ \_ Sha \_ 384**</dt></span><span class="sxs-lookup"><span data-stu-id="9703a-125"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_384**</dt></span></span> </dl> | <span data-ttu-id="9703a-126">Algoritmo hash SHA-384.</span><span class="sxs-lookup"><span data-stu-id="9703a-126">SHA-384 hash algorithm.</span></span><br/> <span data-ttu-id="9703a-127">**CAPICOM 2.0.0.3 y versiones anteriores:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="9703a-127">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |
| <span id="CAPICOM_HASH_ALGORITHM_SHA_512"></span><span id="capicom_hash_algorithm_sha_512"></span><dl> <span data-ttu-id="9703a-128"><dt>**\_Algoritmo hash de CAPICOM \_ \_ Sha \_ 512**</dt></span><span class="sxs-lookup"><span data-stu-id="9703a-128"><dt>**CAPICOM\_HASH\_ALGORITHM\_SHA\_512**</dt></span></span> </dl> | <span data-ttu-id="9703a-129">Algoritmo hash SHA-512.</span><span class="sxs-lookup"><span data-stu-id="9703a-129">SHA-512 hash algorithm.</span></span><br/> <span data-ttu-id="9703a-130">**CAPICOM 2.0.0.3 y versiones anteriores:** Este valor no se admite.</span><span class="sxs-lookup"><span data-stu-id="9703a-130">**CAPICOM 2.0.0.3 and earlier:** This value is not supported.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9703a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9703a-131">Requirements</span></span>



| <span data-ttu-id="9703a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="9703a-132">Requirement</span></span> | <span data-ttu-id="9703a-133">Value</span><span class="sxs-lookup"><span data-stu-id="9703a-133">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9703a-134">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="9703a-134">End of client support</span></span><br/> | <span data-ttu-id="9703a-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9703a-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9703a-136">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="9703a-136">End of server support</span></span><br/> | <span data-ttu-id="9703a-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9703a-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9703a-138">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="9703a-138">Redistributable</span></span><br/>       | <span data-ttu-id="9703a-139">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="9703a-139">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="9703a-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9703a-140">DLL</span></span><br/>                   | <dl> <span data-ttu-id="9703a-141"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9703a-141"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9703a-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="9703a-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9703a-143">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="9703a-143">**HashedData**</span></span>](hasheddata.md)
</dt> </dl>

 

 
