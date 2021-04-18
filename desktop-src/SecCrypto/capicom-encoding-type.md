---
description: Indica el tipo de codificación utilizado.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: Enumeración CAPICOM_ENCODING_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCODING_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: a546831d6e88b3e35706df59adabe0627ad9fccb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671518"
---
# <a name="capicom_encoding_type-enumeration"></a><span data-ttu-id="0dc0f-103">\_Enumeración de tipo de codificación de CAPICOM \_</span><span class="sxs-lookup"><span data-stu-id="0dc0f-103">CAPICOM\_ENCODING\_TYPE enumeration</span></span>

<span data-ttu-id="0dc0f-104">El tipo de enumeración de **\_ \_ tipo de codificación de CAPICOM** indica el tipo de codificación utilizado.</span><span class="sxs-lookup"><span data-stu-id="0dc0f-104">The **CAPICOM\_ENCODING\_TYPE** enumeration type indicates the encoding type used.</span></span>

## <a name="members"></a><span data-ttu-id="0dc0f-105">Miembros</span><span class="sxs-lookup"><span data-stu-id="0dc0f-105">Members</span></span>



| <span data-ttu-id="0dc0f-106">Miembro</span><span class="sxs-lookup"><span data-stu-id="0dc0f-106">Member</span></span>                      | <span data-ttu-id="0dc0f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0dc0f-107">Description</span></span>                                                                                                                                                                                 | <span data-ttu-id="0dc0f-108">Value</span><span class="sxs-lookup"><span data-stu-id="0dc0f-108">Value</span></span>      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| <span data-ttu-id="0dc0f-109">**CAPICOM \_ codificar \_ any**</span><span class="sxs-lookup"><span data-stu-id="0dc0f-109">**CAPICOM\_ENCODE\_ANY**</span></span>    | <span data-ttu-id="0dc0f-110">Los datos se guardan como una cadena codificada en base64 o en una secuencia binaria pura.</span><span class="sxs-lookup"><span data-stu-id="0dc0f-110">Data is saved as a base64-encoded string or a pure binary sequence.</span></span> <span data-ttu-id="0dc0f-111">Este tipo de codificación solo se usa para los datos de entrada que tienen un tipo de codificación desconocido.</span><span class="sxs-lookup"><span data-stu-id="0dc0f-111">This encoding type is used only for input data that has an unknown encoding type.</span></span> <span data-ttu-id="0dc0f-112">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="0dc0f-112">Introduced in CAPICOM 2.0.</span></span><br/> | <span data-ttu-id="0dc0f-113">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="0dc0f-113">0xffffffff</span></span> |
| <span data-ttu-id="0dc0f-114">**CAPICOM, codificación \_ \_ Base64**</span><span class="sxs-lookup"><span data-stu-id="0dc0f-114">**CAPICOM\_ENCODE\_BASE64**</span></span> | <span data-ttu-id="0dc0f-115">Los datos se guardan como una cadena codificada en Base64.</span><span class="sxs-lookup"><span data-stu-id="0dc0f-115">Data is saved as a base64-encoded string.</span></span><br/>                                                                                                                                        | <span data-ttu-id="0dc0f-116">0</span><span class="sxs-lookup"><span data-stu-id="0dc0f-116">0</span></span>          |
| <span data-ttu-id="0dc0f-117">**\_código binario de codificación de CAPICOM \_**</span><span class="sxs-lookup"><span data-stu-id="0dc0f-117">**CAPICOM\_ENCODE\_BINARY**</span></span> | <span data-ttu-id="0dc0f-118">Los datos se guardan como una secuencia binaria pura.</span><span class="sxs-lookup"><span data-stu-id="0dc0f-118">Data is saved as a pure binary sequence.</span></span><br/>                                                                                                                                         | <span data-ttu-id="0dc0f-119">1</span><span class="sxs-lookup"><span data-stu-id="0dc0f-119">1</span></span>          |



## <a name="remarks"></a><span data-ttu-id="0dc0f-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0dc0f-120">Remarks</span></span>

<span data-ttu-id="0dc0f-121">Este tipo de enumeración se usa en los siguientes métodos y propiedades de CAPICOM:</span><span class="sxs-lookup"><span data-stu-id="0dc0f-121">This enumeration type is used by the following CAPICOM methods and properties:</span></span>

-   <span data-ttu-id="0dc0f-122">Método [**Certificate. Export**](certificate-export.md)</span><span class="sxs-lookup"><span data-stu-id="0dc0f-122">[**Certificate.Export**](certificate-export.md) method</span></span>
-   <span data-ttu-id="0dc0f-123">[**EncodedData. Value**](encodeddata-value.md) (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0dc0f-123">[**EncodedData.Value**](encodeddata-value.md) property</span></span>
-   <span data-ttu-id="0dc0f-124">[**EncryptedData. Encrypt**](encrypteddata-encrypt.md) (método)</span><span class="sxs-lookup"><span data-stu-id="0dc0f-124">[**EncryptedData.Encrypt**](encrypteddata-encrypt.md) method</span></span>
-   <span data-ttu-id="0dc0f-125">[**EnvelopedData. Encrypt**](envelopeddata-encrypt.md) (método)</span><span class="sxs-lookup"><span data-stu-id="0dc0f-125">[**EnvelopedData.Encrypt**](envelopeddata-encrypt.md) method</span></span>
-   <span data-ttu-id="0dc0f-126">[**ExtendedProperty. Value**](extendedproperty-value.md) (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0dc0f-126">[**ExtendedProperty.Value**](extendedproperty-value.md) property</span></span>
-   <span data-ttu-id="0dc0f-127">[**SignedData. Sign**](signeddata-sign.md) (método)</span><span class="sxs-lookup"><span data-stu-id="0dc0f-127">[**SignedData.Sign**](signeddata-sign.md) method</span></span>
-   <span data-ttu-id="0dc0f-128">[**SignedData. Cosign**](signeddata-cosign.md) (método)</span><span class="sxs-lookup"><span data-stu-id="0dc0f-128">[**SignedData.CoSign**](signeddata-cosign.md) method</span></span>
-   <span data-ttu-id="0dc0f-129">[**Store. Export**](store-export.md) (método)</span><span class="sxs-lookup"><span data-stu-id="0dc0f-129">[**Store.Export**](store-export.md) method</span></span>
-   <span data-ttu-id="0dc0f-130">[**Utilities. GetRandom**](utilities-getrandom.md) (método)</span><span class="sxs-lookup"><span data-stu-id="0dc0f-130">[**Utilities.GetRandom**](utilities-getrandom.md) method</span></span>

## <a name="requirements"></a><span data-ttu-id="0dc0f-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0dc0f-131">Requirements</span></span>



| <span data-ttu-id="0dc0f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0dc0f-132">Requirement</span></span> | <span data-ttu-id="0dc0f-133">Value</span><span class="sxs-lookup"><span data-stu-id="0dc0f-133">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0dc0f-134">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="0dc0f-134">Redistributable</span></span><br/> | <span data-ttu-id="0dc0f-135">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="0dc0f-135">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="0dc0f-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0dc0f-136">Header</span></span><br/>          | <dl> <span data-ttu-id="0dc0f-137"><dt>CAPICOM. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dc0f-137"><dt>Capicom.h</dt></span></span> </dl> |



 

 




