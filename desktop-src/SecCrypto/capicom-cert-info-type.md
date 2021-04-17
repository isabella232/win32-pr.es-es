---
description: Define la información que se va a consultar desde un certificado.
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: Enumeración CAPICOM_CERT_INFO_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERT_INFO_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8e38bb8940645bbefecb3822bce8de8c2e0eb902
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670784"
---
# <a name="capicom_cert_info_type-enumeration"></a><span data-ttu-id="9786a-103">\_ \_ Enumeración de tipo de información de certificado de CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="9786a-103">CAPICOM\_CERT\_INFO\_TYPE enumeration</span></span>

<span data-ttu-id="9786a-104">El tipo de enumeración de tipo de información de certificado de CAPICOM define qué información se va a consultar desde un certificado. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9786a-104">The **CAPICOM\_CERT\_INFO\_TYPE** enumeration type defines what information is to be queried from a certificate.</span></span>

## <a name="members"></a><span data-ttu-id="9786a-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="9786a-105">Members</span></span>



| <span data-ttu-id="9786a-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="9786a-106">Member</span></span>                                         | <span data-ttu-id="9786a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="9786a-107">Description</span></span>                                                                                  | <span data-ttu-id="9786a-108">Value</span><span class="sxs-lookup"><span data-stu-id="9786a-108">Value</span></span> |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="9786a-109">**\_ \_ \_ nombre simple del asunto de información \_ de certificado de CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="9786a-109">**CAPICOM\_CERT\_INFO\_SUBJECT\_SIMPLE\_NAME**</span></span> | <span data-ttu-id="9786a-110">Devuelve el nombre para mostrar del asunto del certificado.</span><span class="sxs-lookup"><span data-stu-id="9786a-110">Returns the display name of the certificate subject.</span></span><br/>                              | <span data-ttu-id="9786a-111">0</span><span class="sxs-lookup"><span data-stu-id="9786a-111">0</span></span>     |
| <span data-ttu-id="9786a-112">**\_ \_ \_ nombre simple del emisor de información de \_ certificado de \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="9786a-112">**CAPICOM\_CERT\_INFO\_ISSUER\_SIMPLE\_NAME**</span></span>  | <span data-ttu-id="9786a-113">Devuelve el nombre para mostrar del emisor del certificado.</span><span class="sxs-lookup"><span data-stu-id="9786a-113">Returns the display name of the issuer of the certificate.</span></span><br/>                        | <span data-ttu-id="9786a-114">1</span><span class="sxs-lookup"><span data-stu-id="9786a-114">1</span></span>     |
| <span data-ttu-id="9786a-115">**\_nombre de \_ \_ \_ correo electrónico del asunto de información de certificado de CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="9786a-115">**CAPICOM\_CERT\_INFO\_SUBJECT\_EMAIL\_NAME**</span></span>  | <span data-ttu-id="9786a-116">Devuelve la dirección de correo electrónico del firmante del certificado.</span><span class="sxs-lookup"><span data-stu-id="9786a-116">Returns the email address of the certificate subject.</span></span><br/>                             | <span data-ttu-id="9786a-117">2</span><span class="sxs-lookup"><span data-stu-id="9786a-117">2</span></span>     |
| <span data-ttu-id="9786a-118">**\_nombre de \_ \_ \_ correo electrónico del emisor de información \_ de certificado de CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="9786a-118">**CAPICOM\_CERT\_INFO\_ISSUER\_EMAIL\_NAME**</span></span>   | <span data-ttu-id="9786a-119">Devuelve la dirección de correo electrónico del emisor del certificado.</span><span class="sxs-lookup"><span data-stu-id="9786a-119">Returns the email address of the issuer of the certificate.</span></span><br/>                       | <span data-ttu-id="9786a-120">3</span><span class="sxs-lookup"><span data-stu-id="9786a-120">3</span></span>     |
| <span data-ttu-id="9786a-121">**\_UPN de \_ asunto de información de certificado de CAPICOM \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9786a-121">**CAPICOM\_CERT\_INFO\_SUBJECT\_UPN**</span></span>          | <span data-ttu-id="9786a-122">Devuelve el UPN del firmante del certificado.</span><span class="sxs-lookup"><span data-stu-id="9786a-122">Returns the UPN of the certificate subject.</span></span> <span data-ttu-id="9786a-123">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="9786a-123">Introduced in CAPICOM 2.0.</span></span><br/>            | <span data-ttu-id="9786a-124">4</span><span class="sxs-lookup"><span data-stu-id="9786a-124">4</span></span>     |
| <span data-ttu-id="9786a-125">**\_UPN del \_ emisor de información de certificado de \_ CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="9786a-125">**CAPICOM\_CERT\_INFO\_ISSUER\_UPN**</span></span>           | <span data-ttu-id="9786a-126">Devuelve el UPN del emisor del certificado.</span><span class="sxs-lookup"><span data-stu-id="9786a-126">Returns the UPN of the issuer of the certificate.</span></span> <span data-ttu-id="9786a-127">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="9786a-127">Introduced in CAPICOM 2.0.</span></span><br/>      | <span data-ttu-id="9786a-128">5</span><span class="sxs-lookup"><span data-stu-id="9786a-128">5</span></span>     |
| <span data-ttu-id="9786a-129">**\_ \_ \_ nombre DNS del asunto de información \_ de certificado de CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="9786a-129">**CAPICOM\_CERT\_INFO\_SUBJECT\_DNS\_NAME**</span></span>    | <span data-ttu-id="9786a-130">Devuelve el nombre DNS del firmante del certificado.</span><span class="sxs-lookup"><span data-stu-id="9786a-130">Returns the DNS name of the certificate subject.</span></span> <span data-ttu-id="9786a-131">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="9786a-131">Introduced in CAPICOM 2.0.</span></span><br/>       | <span data-ttu-id="9786a-132">6</span><span class="sxs-lookup"><span data-stu-id="9786a-132">6</span></span>     |
| <span data-ttu-id="9786a-133">**\_ \_ \_ nombre DNS del emisor de información de \_ certificado de \_ CAPICOM**</span><span class="sxs-lookup"><span data-stu-id="9786a-133">**CAPICOM\_CERT\_INFO\_ISSUER\_DNS\_NAME**</span></span>     | <span data-ttu-id="9786a-134">Devuelve el nombre DNS del emisor del certificado.</span><span class="sxs-lookup"><span data-stu-id="9786a-134">Returns the DNS name of the issuer of the certificate.</span></span> <span data-ttu-id="9786a-135">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="9786a-135">Introduced in CAPICOM 2.0.</span></span><br/> | <span data-ttu-id="9786a-136">7</span><span class="sxs-lookup"><span data-stu-id="9786a-136">7</span></span>     |



## <a name="remarks"></a><span data-ttu-id="9786a-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9786a-137">Remarks</span></span>

<span data-ttu-id="9786a-138">El tipo de enumeración de tipo de información de certificado de CAPICOM lo usa el método [**Certificate. GetInfo**](certificate-getinfo.md) . **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9786a-138">The **CAPICOM\_CERT\_INFO\_TYPE** enumeration type is used by the [**Certificate.GetInfo**](certificate-getinfo.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="9786a-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9786a-139">Requirements</span></span>



| <span data-ttu-id="9786a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9786a-140">Requirement</span></span> | <span data-ttu-id="9786a-141">Value</span><span class="sxs-lookup"><span data-stu-id="9786a-141">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9786a-142">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="9786a-142">Redistributable</span></span><br/> | <span data-ttu-id="9786a-143">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="9786a-143">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="9786a-144">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9786a-144">Header</span></span><br/>          | <dl> <span data-ttu-id="9786a-145"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="9786a-145"><dt>Capicom.h</dt></span></span> </dl> |



 

 




