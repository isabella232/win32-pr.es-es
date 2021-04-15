---
title: Elemento AnonymousUserName (IdentityPrivacyParameters)
description: Contiene una identidad anónima que se utiliza en lugar de la verdadera identificación de un usuario. Se envía durante la primera fase de la autenticación PEAP cuando la identidad se envía como texto sin formato.
ms.assetid: 74a33a75-cf21-4346-a984-f2f8564c3b57
keywords:
- Elemento AnonymousUserName EAPHost
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
ms.openlocfilehash: 6bbc973160a8865e246a6cec87ce02ced136d786
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422456"
---
# <a name="anonymoususername-identityprivacyparameters-element"></a><span data-ttu-id="bbc86-105">Elemento AnonymousUserName (IdentityPrivacyParameters)</span><span class="sxs-lookup"><span data-stu-id="bbc86-105">AnonymousUserName (IdentityPrivacyParameters) Element</span></span>

<span data-ttu-id="bbc86-106">El elemento **AnonymousUserName (IdentityPrivacyParameters)** contiene una identidad anónima que se utiliza en lugar de la verdadera identificación de un usuario.</span><span class="sxs-lookup"><span data-stu-id="bbc86-106">The **AnonymousUserName (IdentityPrivacyParameters)** element contains an anonymous identity used in place of a user's true identify.</span></span> <span data-ttu-id="bbc86-107">Se envía durante la primera fase de la autenticación PEAP cuando la **identidad** se envía como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="bbc86-107">It is sent during the 1st Phase of PEAP authentication when **Identity** is sent as plain text.</span></span>

<span data-ttu-id="bbc86-108">El uso de identidades anónimas viene determinado por el elemento [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bbc86-108">Anonymous identity usage is determined by the [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AnonymousUserName"
    type="xs:String"
    minOccurs="0"
 />
```

<span data-ttu-id="bbc86-109">El elemento **AnonymousUserName** se define mediante [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="bbc86-109">The **AnonymousUserName** element is defined by the [IdentityPrivacyParameters](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md) .</span></span>

## <a name="remarks"></a><span data-ttu-id="bbc86-110">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bbc86-110">Remarks</span></span>

<span data-ttu-id="bbc86-111">El elemento **AnonymousUserName** es opcional.</span><span class="sxs-lookup"><span data-stu-id="bbc86-111">The **AnonymousUserName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbc86-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bbc86-112">Requirements</span></span>



| <span data-ttu-id="bbc86-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="bbc86-113">Requirement</span></span> | <span data-ttu-id="bbc86-114">Value</span><span class="sxs-lookup"><span data-stu-id="bbc86-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="bbc86-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbc86-115">Minimum supported client</span></span><br/> | <span data-ttu-id="bbc86-116">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="bbc86-116">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="bbc86-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="bbc86-117">Minimum supported server</span></span><br/> | <span data-ttu-id="bbc86-118">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="bbc86-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbc86-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="bbc86-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="bbc86-120">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="bbc86-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bbc86-121">IdentityPrivacyParameters</span><span class="sxs-lookup"><span data-stu-id="bbc86-121">IdentityPrivacyParameters</span></span>](mspeapconnectionpropertiesv2-identityprivacyparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="bbc86-122">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="bbc86-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bbc86-123">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="bbc86-123">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="bbc86-124">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="bbc86-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="bbc86-125">Esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="bbc86-125">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="bbc86-126">Elementos de esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="bbc86-126">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





