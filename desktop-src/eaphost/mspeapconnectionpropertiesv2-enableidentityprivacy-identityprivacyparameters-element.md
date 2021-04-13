---
title: Elemento EnableIdentityPrivacy (IdentityPrivacyParameters)
description: Indica si se envía la verdadera identidad de un usuario o una identidad anónima. | Elemento EnableIdentityPrivacy (IdentityPrivacyParameters)
ms.assetid: 7751e5fa-895e-47f7-99d9-aa7ef2451eb1
keywords:
- Elemento EnableIdentityPrivacy EAPHost
topic_type:
- apiref
api_name:
- Username
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a96b49fe462f4ef8cedad550d1a6c87d680939
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362353"
---
# <a name="enableidentityprivacy-identityprivacyparameters-element"></a><span data-ttu-id="4c7b4-105">Elemento EnableIdentityPrivacy (IdentityPrivacyParameters)</span><span class="sxs-lookup"><span data-stu-id="4c7b4-105">EnableIdentityPrivacy (IdentityPrivacyParameters) Element</span></span>

<span data-ttu-id="4c7b4-106">El elemento **EnableIdentityPrivacy (IdentityPrivacyParameters)** indica si se envía la verdadera identidad de un usuario o una identidad anónima.</span><span class="sxs-lookup"><span data-stu-id="4c7b4-106">The **EnableIdentityPrivacy (IdentityPrivacyParameters)** element Indicates whether a user's true identity or an anonymous identity is sent.</span></span>

``` syntax
<xs:element name="EnableIdentityPrivacy"
    type="xs:Boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="4c7b4-107">El elemento **EnableIdentityPrivacy** se define mediante [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4c7b4-107">The **EnableIdentityPrivacy** element is defined by the [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span></span>

## <a name="remarks"></a><span data-ttu-id="4c7b4-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c7b4-108">Remarks</span></span>

<span data-ttu-id="4c7b4-109">El elemento **EnableIdentityPrivacy** es opcional.</span><span class="sxs-lookup"><span data-stu-id="4c7b4-109">The **EnableIdentityPrivacy** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c7b4-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4c7b4-110">Requirements</span></span>



| <span data-ttu-id="4c7b4-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c7b4-111">Requirement</span></span> | <span data-ttu-id="4c7b4-112">Value</span><span class="sxs-lookup"><span data-stu-id="4c7b4-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="4c7b4-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c7b4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4c7b4-114">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="4c7b4-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="4c7b4-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4c7b4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4c7b4-116">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4c7b4-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4c7b4-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="4c7b4-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="4c7b4-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="4c7b4-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4c7b4-119">IdentityPrivacyParameters</span><span class="sxs-lookup"><span data-stu-id="4c7b4-119">IdentityPrivacyParameters</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="4c7b4-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="4c7b4-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4c7b4-121">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="4c7b4-121">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="4c7b4-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="4c7b4-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="4c7b4-123">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="4c7b4-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4c7b4-124">Esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="4c7b4-124">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="4c7b4-125">Elementos de esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="4c7b4-125">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





