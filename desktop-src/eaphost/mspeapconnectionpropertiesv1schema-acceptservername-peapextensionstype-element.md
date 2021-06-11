---
title: Elemento AcceptServerName (PeapExtensionsType) (EAPHost)
description: El elemento AcceptServerName (PeapExtensionsType) indica si el nombre del servidor se valida con la cadena de nombre especificada en ServerNames en el esquema mspeapconnectionpropertiesv1.
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
ms.openlocfilehash: 64565b24da0b4a93fd35fd3c4a6e7075546024c4
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989101"
---
# <a name="acceptservername-peapextensionstype-element-eaphost"></a><span data-ttu-id="5a06d-104">Elemento AcceptServerName (PeapExtensionsType) (EAPHost)</span><span class="sxs-lookup"><span data-stu-id="5a06d-104">AcceptServerName (PeapExtensionsType) Element (EAPHost)</span></span>

<span data-ttu-id="5a06d-105">El **elemento AcceptServerName (PeapExtensionsType)** indica si el nombre del servidor se valida con la cadena de nombre especificada en el elemento [**ServerNames (ServerValidationParameters).**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md)</span><span class="sxs-lookup"><span data-stu-id="5a06d-105">The **AcceptServerName (PeapExtensionsType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](mspeapconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:AcceptServerName"
 />
```

<span data-ttu-id="5a06d-106">El elemento [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) define el elemento .</span><span class="sxs-lookup"><span data-stu-id="5a06d-106">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a06d-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5a06d-107">Remarks</span></span>

<span data-ttu-id="5a06d-108">El **elemento AcceptServerName** es opcional.</span><span class="sxs-lookup"><span data-stu-id="5a06d-108">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a06d-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a06d-109">Requirements</span></span>



| <span data-ttu-id="5a06d-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a06d-110">Requirement</span></span> | <span data-ttu-id="5a06d-111">Valor</span><span class="sxs-lookup"><span data-stu-id="5a06d-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="5a06d-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a06d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5a06d-113">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a06d-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="5a06d-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a06d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5a06d-115">Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="5a06d-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a06d-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a06d-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="5a06d-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="5a06d-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5a06d-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="5a06d-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="5a06d-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="5a06d-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5a06d-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="5a06d-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="5a06d-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="5a06d-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="5a06d-122">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="5a06d-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="5a06d-123">Mspeapconnectionpropertiesv1 Schema</span><span class="sxs-lookup"><span data-stu-id="5a06d-123">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="5a06d-124">Elementos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="5a06d-124">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="5a06d-125">**AcceptServerName**</span><span class="sxs-lookup"><span data-stu-id="5a06d-125">**AcceptServerName**</span></span>](mspeapconnectionpropertiesv2-acceptservername-peapextensionstype-element.md)
</dt> </dl>

 

 





