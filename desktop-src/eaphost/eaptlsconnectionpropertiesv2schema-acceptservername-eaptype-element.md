---
title: Elemento AcceptServerName
description: Indica si el nombre del servidor se valida con respecto a la cadena de nombre especificada en el elemento ServerNames (ServerValidationParameters). | Elemento AcceptServerName
ms.assetid: 307b2d2a-1678-4aa9-82ed-46d401cf0e0f
keywords:
- Elemento AcceptServerName EAPHost
topic_type:
- apiref
api_name:
- AcceptServerName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b48c43bce2bd71f4d761ea58fcdf5e0632107f87
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698076"
---
# <a name="acceptservername-element"></a><span data-ttu-id="6d03c-105">Elemento AcceptServerName</span><span class="sxs-lookup"><span data-stu-id="6d03c-105">AcceptServerName element</span></span>

<span data-ttu-id="6d03c-106">El elemento **AcceptServerName (EapType)** indica si el nombre del servidor se valida con respecto a la cadena de nombre especificada en el elemento [**servernames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6d03c-106">The **AcceptServerName (EapType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="6d03c-107">El elemento **AcceptServerName** se define mediante el elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6d03c-107">The **AcceptServerName** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d03c-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6d03c-108">Remarks</span></span>

<span data-ttu-id="6d03c-109">El elemento **AcceptServerName** es opcional.</span><span class="sxs-lookup"><span data-stu-id="6d03c-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d03c-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d03c-110">Requirements</span></span>



| <span data-ttu-id="6d03c-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d03c-111">Requirement</span></span> | <span data-ttu-id="6d03c-112">Value</span><span class="sxs-lookup"><span data-stu-id="6d03c-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="6d03c-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d03c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6d03c-114">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="6d03c-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="6d03c-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6d03c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6d03c-116">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6d03c-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d03c-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="6d03c-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="6d03c-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="6d03c-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6d03c-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="6d03c-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="6d03c-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="6d03c-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6d03c-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="6d03c-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="6d03c-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="6d03c-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="6d03c-123">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="6d03c-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="6d03c-124">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="6d03c-124">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="6d03c-125">Elementos de esquema eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="6d03c-125">eaptlsconnectionpropertiesv2 Schema Elements</span></span>](eaptlsconnectionpropertiesv2schema-elements.md)
</dt> <dt>

[<span data-ttu-id="6d03c-126">**AcceptServerName (EapType)**</span><span class="sxs-lookup"><span data-stu-id="6d03c-126">**AcceptServerName (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)
</dt> </dl>

 

 





