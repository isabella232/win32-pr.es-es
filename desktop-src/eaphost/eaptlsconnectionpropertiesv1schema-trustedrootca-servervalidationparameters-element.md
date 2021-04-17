---
title: 'Elemento TrustedRootCA (ServerValidationParameters): conexión'
description: Captura la impresión en miniatura de las entidades de certificación (CA) raíz en las que confía el cliente. | Elemento TrustedRootCA (ServerValidationParameters)
ms.assetid: 81e3b6ca-6360-42dc-bfd3-298e81e66c1a
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
ms.openlocfilehash: e6f91816ba90300a76545a7a22cea6d037b4e897
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/16/2021
ms.locfileid: "105698460"
---
# <a name="trustedrootca-servervalidationparameters-element-for-connection-properties"></a><span data-ttu-id="39c25-105">Elemento TrustedRootCA (ServerValidationParameters) para propiedades de conexión</span><span class="sxs-lookup"><span data-stu-id="39c25-105">TrustedRootCA (ServerValidationParameters) Element for connection properties</span></span>

<span data-ttu-id="39c25-106">El elemento **TrustedRootCA (ServerValidationParameters)** captura la impresión en miniatura de las entidades de certificación (CA) raíz que son de confianza para el cliente.</span><span class="sxs-lookup"><span data-stu-id="39c25-106">The **TrustedRootCA (ServerValidationParameters)** element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="39c25-107">El elemento **TrustedRootCA** se define mediante el tipo complejo de [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="39c25-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="39c25-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="39c25-108">Remarks</span></span>

<span data-ttu-id="39c25-109">La impresión en miniatura es una cadena hexadecimal que contiene el hash SHA-1 del certificado.</span><span class="sxs-lookup"><span data-stu-id="39c25-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="39c25-110">El elemento **TrustedRootCA** es opcional.</span><span class="sxs-lookup"><span data-stu-id="39c25-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="39c25-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39c25-111">Requirements</span></span>



| <span data-ttu-id="39c25-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="39c25-112">Requirement</span></span> | <span data-ttu-id="39c25-113">Value</span><span class="sxs-lookup"><span data-stu-id="39c25-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="39c25-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39c25-114">Minimum supported client</span></span><br/> | <span data-ttu-id="39c25-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="39c25-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="39c25-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="39c25-116">Minimum supported server</span></span><br/> | <span data-ttu-id="39c25-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="39c25-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39c25-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="39c25-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="39c25-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="39c25-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="39c25-120">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="39c25-120">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="39c25-121">**Posibles elementos primarios inmediatos en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="39c25-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="39c25-122">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="39c25-122">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="39c25-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="39c25-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="39c25-124">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="39c25-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="39c25-125">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="39c25-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="39c25-126">Elementos de esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="39c25-126">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





