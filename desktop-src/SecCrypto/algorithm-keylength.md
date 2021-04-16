---
description: Establece o recupera la longitud de la clave.
ms.assetid: c0176d2d-c000-4529-af45-1cc9060ca56a
title: Algorithm. KeyLength (propiedad)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Algorithm.KeyLength
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0aa5dbaeeebe2daaf925b5d5f3aa82b36053fc39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689987"
---
# <a name="algorithmkeylength-property"></a><span data-ttu-id="4ac15-103">Algorithm. KeyLength (propiedad)</span><span class="sxs-lookup"><span data-stu-id="4ac15-103">Algorithm.KeyLength property</span></span>

<span data-ttu-id="4ac15-104">\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP.</span><span class="sxs-lookup"><span data-stu-id="4ac15-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="4ac15-105">En su lugar, use la [**clase AlgorithmIdentifier**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]</span><span class="sxs-lookup"><span data-stu-id="4ac15-105">Instead, use the [**AlgorithmIdentifier Class**](/dotnet/api/system.security.cryptography.pkcs.algorithmidentifier?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="4ac15-106">La propiedad **KeyLength** establece o recupera la longitud de la clave.</span><span class="sxs-lookup"><span data-stu-id="4ac15-106">The **KeyLength** property sets or retrieves the length of the key.</span></span>

<span data-ttu-id="4ac15-107">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="4ac15-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ac15-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4ac15-108">Syntax</span></span>


```VB
Algorithm.KeyLength As CAPICOM_ENCRYPTION_KEY_LENGTH
```



## <a name="property-value"></a><span data-ttu-id="4ac15-109">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="4ac15-109">Property value</span></span>

<span data-ttu-id="4ac15-110">Un valor de la enumeración de longitud de la [**\_ \_ clave \_ de cifrado CAPICOM**](capicom-encryption-key-length.md) que especifica la longitud de la clave.</span><span class="sxs-lookup"><span data-stu-id="4ac15-110">A value of the [**CAPICOM\_ENCRYPTION\_KEY\_LENGTH**](capicom-encryption-key-length.md) enumeration that specifies the key length.</span></span> <span data-ttu-id="4ac15-111">En la siguiente tabla se muestran los valores posibles.</span><span class="sxs-lookup"><span data-stu-id="4ac15-111">The following table shows the possible values.</span></span>



| <span data-ttu-id="4ac15-112">Valor</span><span class="sxs-lookup"><span data-stu-id="4ac15-112">Value</span></span>                                                                                                                                                                                                                                        | <span data-ttu-id="4ac15-113">Significado</span><span class="sxs-lookup"><span data-stu-id="4ac15-113">Meaning</span></span>                                                                                  |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_MAXIMUM"></span><span id="capicom_encryption_key_length_maximum"></span><dl> <span data-ttu-id="4ac15-114"><dt>**\_ \_ \_ longitud máxima de la clave de CIFRAdo de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="4ac15-114"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_MAXIMUM**</dt></span></span> </dl>     | <span data-ttu-id="4ac15-115">Usar la longitud de clave máxima disponible con el algoritmo de cifrado indicado.</span><span class="sxs-lookup"><span data-stu-id="4ac15-115">Use the maximum key length available with the indicated encryption algorithm.</span></span><br/> |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_40_BITS"></span><span id="capicom_encryption_key_length_40_bits"></span><dl> <span data-ttu-id="4ac15-116"><dt>**La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 40 \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="4ac15-116"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_40\_BITS**</dt></span></span> </dl>    | <span data-ttu-id="4ac15-117">Usar claves de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="4ac15-117">Use 40-bit keys.</span></span><br/>                                                              |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_56_BITS"></span><span id="capicom_encryption_key_length_56_bits"></span><dl> <span data-ttu-id="4ac15-118"><dt>**La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 56 \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="4ac15-118"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_56\_BITS**</dt></span></span> </dl>    | <span data-ttu-id="4ac15-119">Use claves de 56 bits si está disponible.</span><span class="sxs-lookup"><span data-stu-id="4ac15-119">Use 56-bit keys if available.</span></span><br/>                                                 |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_128_BITS"></span><span id="capicom_encryption_key_length_128_bits"></span><dl> <span data-ttu-id="4ac15-120"><dt>**La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 128 \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="4ac15-120"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_128\_BITS**</dt></span></span> </dl> | <span data-ttu-id="4ac15-121">Use claves de 128 bits si está disponible.</span><span class="sxs-lookup"><span data-stu-id="4ac15-121">Use 128-bit keys if available.</span></span><br/>                                                |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_192_BITS"></span><span id="capicom_encryption_key_length_192_bits"></span><dl> <span data-ttu-id="4ac15-122"><dt>**La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 192 \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="4ac15-122"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_192\_BITS**</dt></span></span> </dl> | <span data-ttu-id="4ac15-123">Usar claves de 192 bits.</span><span class="sxs-lookup"><span data-stu-id="4ac15-123">Use 192-bit keys.</span></span> <span data-ttu-id="4ac15-124">Esta longitud de clave solo está disponible para AES.</span><span class="sxs-lookup"><span data-stu-id="4ac15-124">This key length is available only for AES.</span></span><br/>                  |
| <span id="CAPICOM_ENCRYPTION_KEY_LENGTH_256_BITS"></span><span id="capicom_encryption_key_length_256_bits"></span><dl> <span data-ttu-id="4ac15-125"><dt>**La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 256 \_ bits**</dt></span><span class="sxs-lookup"><span data-stu-id="4ac15-125"><dt>**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_256\_BITS**</dt></span></span> </dl> | <span data-ttu-id="4ac15-126">Usar claves de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="4ac15-126">Use 256-bit keys.</span></span> <span data-ttu-id="4ac15-127">Esta longitud de clave solo está disponible para AES.</span><span class="sxs-lookup"><span data-stu-id="4ac15-127">This key length is available only for AES.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="4ac15-128">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4ac15-128">Remarks</span></span>

<span data-ttu-id="4ac15-129">Cuando se utilizan algoritmos de cifrado DES y 3DES, las longitudes de clave son estándar y se omite la propiedad **KeyLength** .</span><span class="sxs-lookup"><span data-stu-id="4ac15-129">When DES and 3DES encryption algorithms are used, the key lengths are standard and the **KeyLength** property is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ac15-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4ac15-130">Requirements</span></span>



| <span data-ttu-id="4ac15-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ac15-131">Requirement</span></span> | <span data-ttu-id="4ac15-132">Value</span><span class="sxs-lookup"><span data-stu-id="4ac15-132">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4ac15-133">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="4ac15-133">End of client support</span></span><br/> | <span data-ttu-id="4ac15-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4ac15-134">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="4ac15-135">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="4ac15-135">End of server support</span></span><br/> | <span data-ttu-id="4ac15-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4ac15-136">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="4ac15-137">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="4ac15-137">Redistributable</span></span><br/>       | <span data-ttu-id="4ac15-138">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="4ac15-138">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="4ac15-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4ac15-139">DLL</span></span><br/>                   | <dl> <span data-ttu-id="4ac15-140"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4ac15-140"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ac15-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="4ac15-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ac15-142">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="4ac15-142">**Algorithm**</span></span>](algorithm.md)
</dt> </dl>

 

 
