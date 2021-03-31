---
title: Elemento AcceptServerName (PeapExtensionsType)
description: Indica si el nombre del servidor se valida con respecto a la cadena de nombre especificada en el elemento ServerNames (ServerValidationParameters). | Elemento AcceptServerName (PeapExtensionsType)
ms.assetid: 95173b57-8100-44e4-98f0-4f2a3deabce7
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
ms.openlocfilehash: 1c877819fd559cb26cd93c5d5456631a93a49545
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104083648"
---
# <a name="acceptservername-peapextensionstype-element"></a><span data-ttu-id="d1d49-105">Elemento AcceptServerName (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="d1d49-105">AcceptServerName (PeapExtensionsType) Element</span></span>

<span data-ttu-id="d1d49-106">El elemento **AcceptServerName (PeapExtensionsType)** indica si el nombre del servidor se valida con respecto a la cadena de nombre especificada en el elemento [**servernames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d1d49-106">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

<span data-ttu-id="d1d49-107">El elemento se define mediante el elemento [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="d1d49-107">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1d49-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d1d49-108">Remarks</span></span>

<span data-ttu-id="d1d49-109">El elemento **AcceptServerName** es opcional.</span><span class="sxs-lookup"><span data-stu-id="d1d49-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1d49-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1d49-110">Requirements</span></span>



| <span data-ttu-id="d1d49-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1d49-111">Requirement</span></span> | <span data-ttu-id="d1d49-112">Value</span><span class="sxs-lookup"><span data-stu-id="d1d49-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d1d49-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1d49-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d1d49-114">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1d49-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d1d49-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d1d49-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d1d49-116">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="d1d49-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1d49-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="d1d49-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="d1d49-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="d1d49-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d1d49-119">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="d1d49-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="d1d49-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="d1d49-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d1d49-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="d1d49-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="d1d49-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="d1d49-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="d1d49-123">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="d1d49-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d1d49-124">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="d1d49-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="d1d49-125">Elementos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="d1d49-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="d1d49-126">**AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="d1d49-126">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





