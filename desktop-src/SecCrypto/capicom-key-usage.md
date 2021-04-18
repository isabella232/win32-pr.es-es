---
description: La \_ \_ enumeración de uso de claves de CAPICOM define las maneras en las que se puede usar una clave. Introducido en CAPICOM 2,0.
ms.assetid: 7143567b-5882-44a3-ae30-fb8965fb7997
title: Enumeración CAPICOM_KEY_USAGE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_USAGE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 1d44c7f3ecf35ddeb55dd96e5513261691010990
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649779"
---
# <a name="capicom_key_usage-enumeration"></a><span data-ttu-id="2f460-104">\_Enumeración de uso de clave de CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="2f460-104">CAPICOM\_KEY\_USAGE enumeration</span></span>

<span data-ttu-id="2f460-105">La enumeración de **\_ \_ uso de claves de CAPICOM** define las maneras en las que se puede usar una clave.</span><span class="sxs-lookup"><span data-stu-id="2f460-105">The **CAPICOM\_KEY\_USAGE** enumeration defines the ways in which a key can be used.</span></span> <span data-ttu-id="2f460-106">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="2f460-106">Introduced in CAPICOM 2.0.</span></span>

## <a name="members"></a><span data-ttu-id="2f460-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="2f460-107">Members</span></span>



| <span data-ttu-id="2f460-108">Miembro</span><span class="sxs-lookup"><span data-stu-id="2f460-108">Member</span></span>                                      | <span data-ttu-id="2f460-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="2f460-109">Description</span></span>                                                                                                                      | <span data-ttu-id="2f460-110">Value</span><span class="sxs-lookup"><span data-stu-id="2f460-110">Value</span></span>      |
|---------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|------------|
| <span data-ttu-id="2f460-111">**uso de la \_ \_ clave de firma digital \_ de CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="2f460-111">**CAPICOM\_DIGITAL\_SIGNATURE\_KEY\_USAGE**</span></span> | <span data-ttu-id="2f460-112">La clave se puede utilizar para crear una firma digital.</span><span class="sxs-lookup"><span data-stu-id="2f460-112">The key can be used to create a digital signature.</span></span><br/>                                                                    | <span data-ttu-id="2f460-113">0x00000080</span><span class="sxs-lookup"><span data-stu-id="2f460-113">0x00000080</span></span> |
| <span data-ttu-id="2f460-114">**uso de la clave de CAPICOM \_ sin \_ repudio \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2f460-114">**CAPICOM\_NON\_REPUDIATION\_KEY\_USAGE**</span></span>   | <span data-ttu-id="2f460-115">La clave se puede utilizar para el no [*rechazo*](../secgloss/n-gly.md).</span><span class="sxs-lookup"><span data-stu-id="2f460-115">The key can be used for [*nonrepudiation*](../secgloss/n-gly.md).</span></span><br/> | <span data-ttu-id="2f460-116">0x00000040</span><span class="sxs-lookup"><span data-stu-id="2f460-116">0x00000040</span></span> |
| <span data-ttu-id="2f460-117">**uso de la \_ \_ clave de cifrado de clave de \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="2f460-117">**CAPICOM\_KEY\_ENCIPHERMENT\_KEY\_USAGE**</span></span>  | <span data-ttu-id="2f460-118">La clave se puede usar para cifrar una clave.</span><span class="sxs-lookup"><span data-stu-id="2f460-118">The key can be used to encrypt a key.</span></span><br/>                                                                                 | <span data-ttu-id="2f460-119">0x00000020</span><span class="sxs-lookup"><span data-stu-id="2f460-119">0x00000020</span></span> |
| <span data-ttu-id="2f460-120">**uso de la \_ \_ clave de cifrado de datos de \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="2f460-120">**CAPICOM\_DATA\_ENCIPHERMENT\_KEY\_USAGE**</span></span> | <span data-ttu-id="2f460-121">La clave se puede usar para cifrar los datos.</span><span class="sxs-lookup"><span data-stu-id="2f460-121">The key can be used to encrypt data.</span></span><br/>                                                                                  | <span data-ttu-id="2f460-122">0x00000010</span><span class="sxs-lookup"><span data-stu-id="2f460-122">0x00000010</span></span> |
| <span data-ttu-id="2f460-123">**uso de la clave del acuerdo de \_ tecla CAPICOM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2f460-123">**CAPICOM\_KEY\_AGREEMENT\_KEY\_USAGE**</span></span>     | <span data-ttu-id="2f460-124">La clave se puede usar para el acuerdo de claves.</span><span class="sxs-lookup"><span data-stu-id="2f460-124">The key can be used for key agreement.</span></span><br/>                                                                                | <span data-ttu-id="2f460-125">0x00000008</span><span class="sxs-lookup"><span data-stu-id="2f460-125">0x00000008</span></span> |
| <span data-ttu-id="2f460-126">**uso de la \_ \_ clave de firma de certificado \_ \_ \_ de CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="2f460-126">**CAPICOM\_KEY\_CERT\_SIGN\_KEY\_USAGE**</span></span>    | <span data-ttu-id="2f460-127">La clave se puede usar para la firma de certificados de clave.</span><span class="sxs-lookup"><span data-stu-id="2f460-127">The key can be used for key certificate signing.</span></span> <span data-ttu-id="2f460-128">Este valor es equivalente al uso de la \_ clave de signo de CRL sin conexión de CAPICOM \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2f460-128">This value is equivalent to CAPICOM\_OFFLINE\_CRL\_SIGN\_KEY\_USAGE.</span></span><br/> | <span data-ttu-id="2f460-129">0x00000004</span><span class="sxs-lookup"><span data-stu-id="2f460-129">0x00000004</span></span> |
| <span data-ttu-id="2f460-130">**uso de la \_ clave de signo de CRL sin conexión de CAPICOM \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2f460-130">**CAPICOM\_OFFLINE\_CRL\_SIGN\_KEY\_USAGE**</span></span> | <span data-ttu-id="2f460-131">La clave se puede usar para la firma de certificados de clave.</span><span class="sxs-lookup"><span data-stu-id="2f460-131">The key can be used for key certificate signing.</span></span> <span data-ttu-id="2f460-132">Este valor es equivalente al uso de la clave de firma de certificado de CAPICOM \_ \_ \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="2f460-132">This value is equivalent to CAPICOM\_KEY\_CERT\_SIGN\_KEY\_USAGE.</span></span><br/>    | <span data-ttu-id="2f460-133">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2f460-133">0x00000002</span></span> |
| <span data-ttu-id="2f460-134">**uso de la clave de signo de \_ CRL de CAPICOM \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2f460-134">**CAPICOM\_CRL\_SIGN\_KEY\_USAGE**</span></span>          | <span data-ttu-id="2f460-135">La clave se puede utilizar para firmar.</span><span class="sxs-lookup"><span data-stu-id="2f460-135">The key can be used for signing.</span></span><br/>                                                                                      | <span data-ttu-id="2f460-136">0x00000002</span><span class="sxs-lookup"><span data-stu-id="2f460-136">0x00000002</span></span> |
| <span data-ttu-id="2f460-137">**CAPICOM \_ \_ solo cifrado \_ uso de claves \_**</span><span class="sxs-lookup"><span data-stu-id="2f460-137">**CAPICOM\_ENCIPHER\_ONLY\_KEY\_USAGE**</span></span>     | <span data-ttu-id="2f460-138">La clave solo se puede usar para cifrar.</span><span class="sxs-lookup"><span data-stu-id="2f460-138">The key can only be used to encrypt.</span></span><br/>                                                                                  | <span data-ttu-id="2f460-139">0x00000001</span><span class="sxs-lookup"><span data-stu-id="2f460-139">0x00000001</span></span> |
| <span data-ttu-id="2f460-140">**CAPICOM \_ descifrar \_ solo el \_ uso de claves \_**</span><span class="sxs-lookup"><span data-stu-id="2f460-140">**CAPICOM\_DECIPHER\_ONLY\_KEY\_USAGE**</span></span>     | <span data-ttu-id="2f460-141">La clave solo se puede usar para descifrar.</span><span class="sxs-lookup"><span data-stu-id="2f460-141">The key can only be used to decrypt.</span></span><br/>                                                                                  | <span data-ttu-id="2f460-142">0x00008000</span><span class="sxs-lookup"><span data-stu-id="2f460-142">0x00008000</span></span> |



## <a name="requirements"></a><span data-ttu-id="2f460-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f460-143">Requirements</span></span>



| <span data-ttu-id="2f460-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f460-144">Requirement</span></span> | <span data-ttu-id="2f460-145">Value</span><span class="sxs-lookup"><span data-stu-id="2f460-145">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2f460-146">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="2f460-146">Redistributable</span></span><br/> | <span data-ttu-id="2f460-147">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="2f460-147">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="2f460-148">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f460-148">Header</span></span><br/>          | <dl> <span data-ttu-id="2f460-149"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f460-149"><dt>Capicom.h</dt></span></span> </dl> |



 

 
