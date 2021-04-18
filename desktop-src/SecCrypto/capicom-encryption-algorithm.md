---
description: Define los algoritmos que se van a usar en el cifrado y el descifrado.
ms.assetid: c7aacd1c-02f6-4cf5-9305-50e2330f243c
title: Enumeración CAPICOM_ENCRYPTION_ALGORITHM (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_ALGORITHM
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 19626ba560ead406005612db3ed90cabc61d98ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670856"
---
# <a name="capicom_encryption_algorithm-enumeration"></a><span data-ttu-id="42a02-103">\_Enumeración del algoritmo de cifrado CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="42a02-103">CAPICOM\_ENCRYPTION\_ALGORITHM enumeration</span></span>

<span data-ttu-id="42a02-104">El tipo de enumeración del **\_ \_ algoritmo de cifrado de CAPICOM** define los algoritmos que se van a utilizar en el cifrado y descifrado.</span><span class="sxs-lookup"><span data-stu-id="42a02-104">The **CAPICOM\_ENCRYPTION\_ALGORITHM** enumeration type defines the algorithms to be used in encryption and decryption.</span></span>

## <a name="members"></a><span data-ttu-id="42a02-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="42a02-105">Members</span></span>



| <span data-ttu-id="42a02-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="42a02-106">Member</span></span>                                   | <span data-ttu-id="42a02-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="42a02-107">Description</span></span>                                                                                                                                                                                              | <span data-ttu-id="42a02-108">Value</span><span class="sxs-lookup"><span data-stu-id="42a02-108">Value</span></span>     |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="42a02-109">**\_Algoritmo de cifrado de CAPICOM \_ \_ RC2**</span><span class="sxs-lookup"><span data-stu-id="42a02-109">**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC2**</span></span>  | <span data-ttu-id="42a02-110">Use el cifrado RSA RC2.</span><span class="sxs-lookup"><span data-stu-id="42a02-110">Use RSA RC2 encryption.</span></span><br/>                                                                                                                                                                       | <span data-ttu-id="42a02-111">0</span><span class="sxs-lookup"><span data-stu-id="42a02-111">0</span></span>         |
| <span data-ttu-id="42a02-112">**\_Algoritmo de cifrado de CAPICOM \_ \_ RC4**</span><span class="sxs-lookup"><span data-stu-id="42a02-112">**CAPICOM\_ENCRYPTION\_ALGORITHM\_RC4**</span></span>  | <span data-ttu-id="42a02-113">Usar el cifrado RSA RC4.</span><span class="sxs-lookup"><span data-stu-id="42a02-113">Use RSA RC4 encryption.</span></span><br/>                                                                                                                                                                       | <span data-ttu-id="42a02-114">1</span><span class="sxs-lookup"><span data-stu-id="42a02-114">1</span></span>         |
| <span data-ttu-id="42a02-115">**\_ \_ algoritmo des de cifrado de CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="42a02-115">**CAPICOM\_ENCRYPTION\_ALGORITHM\_DES**</span></span>  | <span data-ttu-id="42a02-116">Use el cifrado DES.</span><span class="sxs-lookup"><span data-stu-id="42a02-116">Use DES encryption.</span></span><br/>                                                                                                                                                                           | <span data-ttu-id="42a02-117">2</span><span class="sxs-lookup"><span data-stu-id="42a02-117">2</span></span>         |
| <span data-ttu-id="42a02-118">**\_Algoritmo de cifrado \_ \_ 3DES de CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="42a02-118">**CAPICOM\_ENCRYPTION\_ALGORITHM\_3DES**</span></span> | <span data-ttu-id="42a02-119">Use el cifrado Triple DES.</span><span class="sxs-lookup"><span data-stu-id="42a02-119">Use triple DES encryption.</span></span><br/>                                                                                                                                                                    | <span data-ttu-id="42a02-120">3</span><span class="sxs-lookup"><span data-stu-id="42a02-120">3</span></span>         |
| <span data-ttu-id="42a02-121">**\_algoritmo de cifrado de CAPICOM \_ \_ AES**</span><span class="sxs-lookup"><span data-stu-id="42a02-121">**CAPICOM\_ENCRYPTION\_ALGORITHM\_AES**</span></span>  | <span data-ttu-id="42a02-122">Use el algoritmo [*estándar de cifrado avanzado*](../secgloss/a-gly.md) (AES).</span><span class="sxs-lookup"><span data-stu-id="42a02-122">Use the [*Advanced Encryption Standard*](../secgloss/a-gly.md) (AES) algorithm.</span></span> <span data-ttu-id="42a02-123">Este valor solo es válido para el objeto [**EncryptedData**](encrypteddata.md) .</span><span class="sxs-lookup"><span data-stu-id="42a02-123">This value is valid for the [**EncryptedData**](encrypteddata.md) object only.</span></span><br/> | <span data-ttu-id="42a02-124">4//v 2.0</span><span class="sxs-lookup"><span data-stu-id="42a02-124">4 // v2.0</span></span> |



## <a name="remarks"></a><span data-ttu-id="42a02-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42a02-125">Remarks</span></span>

<span data-ttu-id="42a02-126">La propiedad [**algorithm.Name**](algorithm-name.md) usa el tipo de enumeración del **\_ \_ algoritmo de cifrado CAPICOM** .</span><span class="sxs-lookup"><span data-stu-id="42a02-126">The **CAPICOM\_ENCRYPTION\_ALGORITHM** enumeration type is used by the [**Algorithm.Name**](algorithm-name.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="42a02-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42a02-127">Requirements</span></span>



| <span data-ttu-id="42a02-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="42a02-128">Requirement</span></span> | <span data-ttu-id="42a02-129">Value</span><span class="sxs-lookup"><span data-stu-id="42a02-129">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="42a02-130">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="42a02-130">Redistributable</span></span><br/> | <span data-ttu-id="42a02-131">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="42a02-131">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="42a02-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42a02-132">Header</span></span><br/>          | <dl> <span data-ttu-id="42a02-133"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="42a02-133"><dt>Capicom.h</dt></span></span> </dl> |



 

 
