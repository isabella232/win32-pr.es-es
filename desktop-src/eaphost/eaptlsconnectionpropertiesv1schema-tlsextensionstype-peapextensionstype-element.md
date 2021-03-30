---
title: AcceptServerName
description: Indica si el nombre del servidor se valida con respecto a la cadena de nombre especificada en el elemento ServerNames (ServerValidationParameters). | AcceptServerName
ms.assetid: 440a46ae-7fef-4e97-9fd7-cbd20143597b
keywords:
- elemento EAPHost
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
ms.openlocfilehash: beb12da9897cc0e77480f609edee632c135b5c5d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280070"
---
# <a name="acceptservername"></a><span data-ttu-id="42279-105">AcceptServerName</span><span class="sxs-lookup"><span data-stu-id="42279-105">AcceptServerName</span></span>

<span data-ttu-id="42279-106">El elemento **AcceptServerName (EapType)** indica si el nombre del servidor se valida con respecto a la cadena de nombre especificada en el elemento [**servernames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="42279-106">The **AcceptServerName (EapType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS: AcceptServerName"
 />
```

<span data-ttu-id="42279-107">El elemento se define mediante el elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="42279-107">The element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="42279-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="42279-108">Remarks</span></span>

<span data-ttu-id="42279-109">El elemento **AcceptServerName** es opcional.</span><span class="sxs-lookup"><span data-stu-id="42279-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="42279-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42279-110">Requirements</span></span>



| <span data-ttu-id="42279-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="42279-111">Requirement</span></span> | <span data-ttu-id="42279-112">Value</span><span class="sxs-lookup"><span data-stu-id="42279-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="42279-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42279-113">Minimum supported client</span></span><br/> | <span data-ttu-id="42279-114">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="42279-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="42279-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42279-115">Minimum supported server</span></span><br/> | <span data-ttu-id="42279-116">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="42279-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42279-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="42279-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="42279-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="42279-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="42279-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="42279-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="42279-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="42279-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="42279-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="42279-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="42279-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="42279-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="42279-123">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="42279-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="42279-124">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="42279-124">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="42279-125">Elementos de esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="42279-125">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="42279-126">**AcceptServerName (EapType)**</span><span class="sxs-lookup"><span data-stu-id="42279-126">**AcceptServerName (EapType)**</span></span>](eaptlsconnectionpropertiesv2schema-acceptservername-eaptype-element.md)
</dt> </dl>

 

 





