---
title: Elemento IdentityPrivacy (PeapExtensionsType)
description: El elemento IdentityPrivacy (PeapExtensionsType) indica si la identidad verdadera de un usuario se envía en el esquema mspeapconnectionpropertiesv2.
ms.assetid: 57b8747e-6919-4243-a379-3a85c4a2023a
keywords:
- Elemento IdentityPrivacy EAPHost
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
ms.openlocfilehash: d0a23ce28a1a807bb948c114435463102561570b
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/10/2021
ms.locfileid: "111988951"
---
# <a name="the-identityprivacy-peapextensionstype-element"></a><span data-ttu-id="d5e62-104">Elemento IdentityPrivacy (PeapExtensionsType)</span><span class="sxs-lookup"><span data-stu-id="d5e62-104">The IdentityPrivacy (PeapExtensionsType) Element</span></span>

<span data-ttu-id="d5e62-105">El **elemento IdentityPrivacy (PeapExtensionsType)** indica si se envía la identidad verdadera de un usuario o una identidad anónima.</span><span class="sxs-lookup"><span data-stu-id="d5e62-105">The **IdentityPrivacy (PeapExtensionsType)** element indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element name="IdentityPrivacy"
    type="IdentityPrivacyParameters"
 />
```

<span data-ttu-id="d5e62-106">El **elemento IdentityPrivacy** se define mediante el [**elemento PeapExtensionsType.**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)</span><span class="sxs-lookup"><span data-stu-id="d5e62-106">The **IdentityPrivacy** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5e62-107">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d5e62-107">Remarks</span></span>

<span data-ttu-id="d5e62-108">El **elemento IdentityPrivacy** es opcional.</span><span class="sxs-lookup"><span data-stu-id="d5e62-108">The **IdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5e62-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5e62-109">Requirements</span></span>



| <span data-ttu-id="d5e62-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5e62-110">Requirement</span></span> | <span data-ttu-id="d5e62-111">Valor</span><span class="sxs-lookup"><span data-stu-id="d5e62-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d5e62-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5e62-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d5e62-113">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="d5e62-113">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d5e62-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d5e62-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d5e62-115">Solo aplicaciones de escritorio de Windows Server 2008 \[ R2\]</span><span class="sxs-lookup"><span data-stu-id="d5e62-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5e62-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="d5e62-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5e62-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="d5e62-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d5e62-118">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="d5e62-118">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="d5e62-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="d5e62-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d5e62-120">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="d5e62-120">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="d5e62-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="d5e62-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="d5e62-122">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="d5e62-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="d5e62-123">Mspeapconnectionpropertiesv2 Schema</span><span class="sxs-lookup"><span data-stu-id="d5e62-123">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="d5e62-124">Elementos de esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="d5e62-124">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





