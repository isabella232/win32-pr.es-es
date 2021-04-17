---
title: Elemento IdentityPrivacy (PeapExtensionsType)
description: Indica si se envía la verdadera identidad de un usuario o una identidad anónima. | Elemento IdentityPrivacy (PeapExtensionsType)
ms.assetid: 1ae5b6e8-b1f8-45a7-ad22-fdb57cc756a2
keywords:
- elemento EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ed566e9be0b9e194d24106f1c82d9a9d6d1a199d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105678719"
---
# <a name="identityprivacy-peapextensionstype-element"></a><span data-ttu-id="c8c60-105">Elemento IdentityPrivacy (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="c8c60-105">IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="c8c60-106">El elemento **IdentityPrivacy (PeapExtensionsType)** indica si se envía la verdadera identidad de un usuario o una identidad anónima.</span><span class="sxs-lookup"><span data-stu-id="c8c60-106">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:IdentityPrivacy"
 />
```

<span data-ttu-id="c8c60-107">El elemento se define mediante el elemento [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c8c60-107">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8c60-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8c60-108">Remarks</span></span>

<span data-ttu-id="c8c60-109">El elemento **IdentityPrivacy** es opcional.</span><span class="sxs-lookup"><span data-stu-id="c8c60-109">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8c60-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8c60-110">Requirements</span></span>



| <span data-ttu-id="c8c60-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8c60-111">Requirement</span></span> | <span data-ttu-id="c8c60-112">Value</span><span class="sxs-lookup"><span data-stu-id="c8c60-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c8c60-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8c60-113">Minimum supported client</span></span><br/> | <span data-ttu-id="c8c60-114">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8c60-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="c8c60-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8c60-115">Minimum supported server</span></span><br/> | <span data-ttu-id="c8c60-116">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8c60-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c8c60-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="c8c60-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="c8c60-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="c8c60-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c8c60-119">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="c8c60-119">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="c8c60-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="c8c60-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c8c60-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="c8c60-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="c8c60-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c8c60-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="c8c60-123">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="c8c60-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="c8c60-124">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c8c60-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="c8c60-125">Elementos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c8c60-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="c8c60-126">**IdentityPrivacy(PeapExtensionsType)**</span><span class="sxs-lookup"><span data-stu-id="c8c60-126">**IdentityPrivacy(PeapExtensionsType)**</span></span>](mspeapconnectionpropertiesv2-identityprivacy-peapextensionstype-element.md)
</dt> </dl>

 

 





