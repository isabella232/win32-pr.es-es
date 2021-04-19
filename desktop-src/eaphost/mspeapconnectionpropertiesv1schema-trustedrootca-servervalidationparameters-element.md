---
title: Elemento TrustedRootCA (ServerValidationParameters) (V1)
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
ms.openlocfilehash: 17e1b81e080d48ac8fae4f082c3cf4b46bac858e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389083"
---
# <a name="trustedrootca-servervalidationparameters-element"></a><span data-ttu-id="3b192-105">Elemento TrustedRootCA (ServerValidationParameters)</span><span class="sxs-lookup"><span data-stu-id="3b192-105">TrustedRootCA (ServerValidationParameters) Element</span></span>

<span data-ttu-id="3b192-106">El elemento del elemento **TrustedRootCA (ServerValidationParameters)** captura la impresión en miniatura de las entidades de certificación (CA) raíz que son de confianza para el cliente.</span><span class="sxs-lookup"><span data-stu-id="3b192-106">The **TrustedRootCA (ServerValidationParameters)** element element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="3b192-107">El elemento **TrustedRootCA** se define mediante el tipo complejo de [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="3b192-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b192-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3b192-108">Remarks</span></span>

<span data-ttu-id="3b192-109">La impresión en miniatura es una cadena hexadecimal que contiene el hash SHA-1 del certificado.</span><span class="sxs-lookup"><span data-stu-id="3b192-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="3b192-110">El elemento **TrustedRootCA** es opcional.</span><span class="sxs-lookup"><span data-stu-id="3b192-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b192-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b192-111">Requirements</span></span>



| <span data-ttu-id="3b192-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b192-112">Requirement</span></span> | <span data-ttu-id="3b192-113">Valor</span><span class="sxs-lookup"><span data-stu-id="3b192-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3b192-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b192-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3b192-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3b192-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3b192-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3b192-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3b192-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3b192-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b192-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="3b192-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="3b192-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="3b192-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3b192-120">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="3b192-120">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="3b192-121">**Posibles elementos primarios inmediatos en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="3b192-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3b192-122">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="3b192-122">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="3b192-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3b192-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="3b192-124">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="3b192-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3b192-125">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3b192-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3b192-126">Elementos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="3b192-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





