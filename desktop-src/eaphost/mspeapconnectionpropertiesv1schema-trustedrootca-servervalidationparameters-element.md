---
title: Elemento TrustedRootCA (ServerValidationParameters)
description: Captura la impresión en miniatura de las entidades de certificación (CA) raíz en las que confía el cliente. | Elemento TrustedRootCA (ServerValidationParameters)
ms.assetid: f0485dcc-8610-4c5b-b4db-6f2a77057489
keywords:
- Elemento TrustedRootCA EAPHost
topic_type:
- apiref
api_name:
- TrustedRootCA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e62b691c5075f1a42f87e558a9a1f0795b90e8bb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914302"
---
# <a name="trustedrootca-servervalidationparameters-element"></a><span data-ttu-id="ef8a4-105">Elemento TrustedRootCA (ServerValidationParameters)</span><span class="sxs-lookup"><span data-stu-id="ef8a4-105">TrustedRootCA (ServerValidationParameters) Element</span></span>

<span data-ttu-id="ef8a4-106">El elemento del elemento **TrustedRootCA (ServerValidationParameters)** captura la impresión en miniatura de las entidades de certificación (CA) raíz que son de confianza para el cliente.</span><span class="sxs-lookup"><span data-stu-id="ef8a4-106">The **TrustedRootCA (ServerValidationParameters)** element element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="ef8a4-107">El elemento **TrustedRootCA** se define mediante el tipo complejo de [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ef8a4-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef8a4-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ef8a4-108">Remarks</span></span>

<span data-ttu-id="ef8a4-109">La impresión en miniatura es una cadena hexadecimal que contiene el hash SHA-1 del certificado.</span><span class="sxs-lookup"><span data-stu-id="ef8a4-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="ef8a4-110">El elemento **TrustedRootCA** es opcional.</span><span class="sxs-lookup"><span data-stu-id="ef8a4-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef8a4-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ef8a4-111">Requirements</span></span>



| <span data-ttu-id="ef8a4-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef8a4-112">Requirement</span></span> | <span data-ttu-id="ef8a4-113">Value</span><span class="sxs-lookup"><span data-stu-id="ef8a4-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ef8a4-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef8a4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="ef8a4-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ef8a4-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ef8a4-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ef8a4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="ef8a4-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ef8a4-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ef8a4-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="ef8a4-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="ef8a4-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="ef8a4-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ef8a4-120">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="ef8a4-120">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="ef8a4-121">**Posibles elementos primarios inmediatos en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="ef8a4-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ef8a4-122">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="ef8a4-122">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="ef8a4-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="ef8a4-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="ef8a4-124">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="ef8a4-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="ef8a4-125">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ef8a4-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="ef8a4-126">Elementos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="ef8a4-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





