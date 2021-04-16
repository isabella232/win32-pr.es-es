---
description: Define la longitud de la clave que se va a utilizar en el cifrado.
ms.assetid: a91e75db-f81e-4908-b795-34be7a1c242d
title: Enumeración CAPICOM_ENCRYPTION_KEY_LENGTH (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCRYPTION_KEY_LENGTH
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 4f3e64df1e706ef20a83f4da5c81cda2a08ed331
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671788"
---
# <a name="capicom_encryption_key_length-enumeration"></a><span data-ttu-id="d560e-103">\_ \_ Enumeración de longitud de clave de cifrado de CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="d560e-103">CAPICOM\_ENCRYPTION\_KEY\_LENGTH enumeration</span></span>

<span data-ttu-id="d560e-104">El tipo de enumeración longitud de la **\_ \_ clave \_ de cifrado de CAPICOM** define la [*longitud de clave*](../secgloss/k-gly.md) que se va a utilizar en el cifrado.</span><span class="sxs-lookup"><span data-stu-id="d560e-104">The **CAPICOM\_ENCRYPTION\_KEY\_LENGTH** enumeration type defines the [*key length*](../secgloss/k-gly.md) to be used in encryption.</span></span>

## <a name="members"></a><span data-ttu-id="d560e-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="d560e-105">Members</span></span>



| <span data-ttu-id="d560e-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="d560e-106">Member</span></span>                                          | <span data-ttu-id="d560e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d560e-107">Description</span></span>                                                                               | <span data-ttu-id="d560e-108">Value</span><span class="sxs-lookup"><span data-stu-id="d560e-108">Value</span></span>     |
|-------------------------------------------------|-------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d560e-109">**\_ \_ \_ longitud máxima de la clave de CIFRAdo de CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="d560e-109">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_MAXIMUM**</span></span>   | <span data-ttu-id="d560e-110">Utiliza la longitud de clave máxima disponible con el algoritmo de cifrado indicado.</span><span class="sxs-lookup"><span data-stu-id="d560e-110">Uses the maximum key length available with the indicated encryption algorithm.</span></span><br/> | <span data-ttu-id="d560e-111">0</span><span class="sxs-lookup"><span data-stu-id="d560e-111">0</span></span>         |
| <span data-ttu-id="d560e-112">**La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 40 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="d560e-112">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_40\_BITS**</span></span>  | <span data-ttu-id="d560e-113">Utiliza claves de 40 bits.</span><span class="sxs-lookup"><span data-stu-id="d560e-113">Uses 40-bit keys.</span></span><br/>                                                              | <span data-ttu-id="d560e-114">1</span><span class="sxs-lookup"><span data-stu-id="d560e-114">1</span></span>         |
| <span data-ttu-id="d560e-115">**La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 56 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="d560e-115">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_56\_BITS**</span></span>  | <span data-ttu-id="d560e-116">Utiliza claves de 56 bits si están disponibles.</span><span class="sxs-lookup"><span data-stu-id="d560e-116">Uses 56-bit keys if available.</span></span><br/>                                                 | <span data-ttu-id="d560e-117">2</span><span class="sxs-lookup"><span data-stu-id="d560e-117">2</span></span>         |
| <span data-ttu-id="d560e-118">**La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 128 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="d560e-118">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_128\_BITS**</span></span> | <span data-ttu-id="d560e-119">Utiliza claves de 128 bits si están disponibles.</span><span class="sxs-lookup"><span data-stu-id="d560e-119">Uses 128-bit keys if available.</span></span><br/>                                                | <span data-ttu-id="d560e-120">3</span><span class="sxs-lookup"><span data-stu-id="d560e-120">3</span></span>         |
| <span data-ttu-id="d560e-121">**La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 192 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="d560e-121">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_192\_BITS**</span></span> | <span data-ttu-id="d560e-122">Utiliza claves de 192 bits.</span><span class="sxs-lookup"><span data-stu-id="d560e-122">Uses 192-bit keys.</span></span> <span data-ttu-id="d560e-123">Esta longitud de clave solo está disponible para AES.</span><span class="sxs-lookup"><span data-stu-id="d560e-123">This key length is available only for AES.</span></span><br/>                  | <span data-ttu-id="d560e-124">4//v 2.0</span><span class="sxs-lookup"><span data-stu-id="d560e-124">4 // v2.0</span></span> |
| <span data-ttu-id="d560e-125">**La longitud de la clave de cifrado de CAPICOM es \_ \_ \_ \_ 256 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="d560e-125">**CAPICOM\_ENCRYPTION\_KEY\_LENGTH\_256\_BITS**</span></span> | <span data-ttu-id="d560e-126">Utiliza claves de 256 bits.</span><span class="sxs-lookup"><span data-stu-id="d560e-126">Uses 256-bit keys.</span></span> <span data-ttu-id="d560e-127">Esta longitud de clave solo está disponible para AES.</span><span class="sxs-lookup"><span data-stu-id="d560e-127">This key length is available only for AES.</span></span><br/>                  | <span data-ttu-id="d560e-128">5//v 2.0</span><span class="sxs-lookup"><span data-stu-id="d560e-128">5 // v2.0</span></span> |



## <a name="remarks"></a><span data-ttu-id="d560e-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d560e-129">Remarks</span></span>

<span data-ttu-id="d560e-130">La propiedad [**algorithm. KeyLength**](algorithm-keylength.md) usa el tipo de enumeración longitud de la **\_ \_ clave \_ de cifrado CAPICOM** .</span><span class="sxs-lookup"><span data-stu-id="d560e-130">The **CAPICOM\_ENCRYPTION\_KEY\_LENGTH** enumeration type is used by the [**Algorithm.KeyLength**](algorithm-keylength.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d560e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d560e-131">Requirements</span></span>



| <span data-ttu-id="d560e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="d560e-132">Requirement</span></span> | <span data-ttu-id="d560e-133">Value</span><span class="sxs-lookup"><span data-stu-id="d560e-133">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d560e-134">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="d560e-134">Redistributable</span></span><br/> | <span data-ttu-id="d560e-135">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="d560e-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="d560e-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d560e-136">Header</span></span><br/>          | <dl> <span data-ttu-id="d560e-137"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="d560e-137"><dt>Capicom.h</dt></span></span> </dl> |



 

 
