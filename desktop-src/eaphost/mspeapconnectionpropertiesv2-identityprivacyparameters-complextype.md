---
title: Tipo complejo de IdentityPrivacyParameters
description: Contiene información sobre el uso de identidad anónima durante la autenticación PEAP.
ms.assetid: 81cf2403-ef25-4256-8d18-9d7b71792e6c
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8360065e2ce124531bec63637e2b6560cfc32f54
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "104149021"
---
# <a name="identityprivacyparameters-complex-type"></a><span data-ttu-id="3fe37-103">Tipo complejo de IdentityPrivacyParameters</span><span class="sxs-lookup"><span data-stu-id="3fe37-103">IdentityPrivacyParameters Complex Type</span></span>

<span data-ttu-id="3fe37-104">El tipo complejo **IdentityPrivacyParameters** contiene información sobre el uso de identidad anónima durante la autenticación PEAP.</span><span class="sxs-lookup"><span data-stu-id="3fe37-104">The **IdentityPrivacyParameters** complex type contains information about anonymous identity usage during PEAP authentication.</span></span>


```XML
<xs:complexType name="IdentityPrivacyParameters">
    <xs:sequence>
        <xs:element name="EnableIdentityPrivacy"
            type="xs:boolean"
            minOccurs="0"
        />
        <xs:element name="AnonymousUserName"
            type="xs:string"
            minOccurs="0"
        />
    </xs:sequence>
</xs:complexType>
```





| <span data-ttu-id="3fe37-105">Elemento</span><span class="sxs-lookup"><span data-stu-id="3fe37-105">Element</span></span>                                                                                                               | <span data-ttu-id="3fe37-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="3fe37-106">Type</span></span>    | <span data-ttu-id="3fe37-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="3fe37-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fe37-108">**EnableIdentityPrivacy**</span><span class="sxs-lookup"><span data-stu-id="3fe37-108">**EnableIdentityPrivacy**</span></span>](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) | <span data-ttu-id="3fe37-109">boolean</span><span class="sxs-lookup"><span data-stu-id="3fe37-109">boolean</span></span> | <span data-ttu-id="3fe37-110">Indica si se envía la verdadera identidad de un usuario o una identidad anónima.</span><span class="sxs-lookup"><span data-stu-id="3fe37-110">Indicates whether a user's true identity or an anonymous identity is sent.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="3fe37-111">**AnonymousUserName**</span><span class="sxs-lookup"><span data-stu-id="3fe37-111">**AnonymousUserName**</span></span>](mspeapconnectionpropertiesv2-anonymoususername-identityprivacyparameters-element.md)         | <span data-ttu-id="3fe37-112">string</span><span class="sxs-lookup"><span data-stu-id="3fe37-112">string</span></span>  | <span data-ttu-id="3fe37-113">contiene una identidad anónima que se utiliza en lugar de la verdadera identificación de un usuario.</span><span class="sxs-lookup"><span data-stu-id="3fe37-113">contains an anonymous identity used in place of a user's true identify.</span></span> <span data-ttu-id="3fe37-114">Se envía durante la primera fase de la autenticación PEAP cuando la **identidad** se envía como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="3fe37-114">It is sent during the 1st Phase of PEAP authentication when **Identity** is sent as plain text.</span></span> <span data-ttu-id="3fe37-115">El uso de identidades anónimas viene determinado por el elemento [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3fe37-115">Anonymous identity usage is determined by the [**EnableIdentityPrivacy**](mspeapconnectionpropertiesv2-enableidentityprivacy-identityprivacyparameters-element.md) element.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="3fe37-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3fe37-116">Remarks</span></span>

<span data-ttu-id="3fe37-117">El elemento IdentityPrivacyParameters es opcional.</span><span class="sxs-lookup"><span data-stu-id="3fe37-117">The IdentityPrivacyParameters element is optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fe37-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3fe37-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fe37-119">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="3fe37-119">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="3fe37-120">Esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="3fe37-120">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="3fe37-121">Tipos complejos de mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="3fe37-121">mspeapconnectionpropertiesv2 Complex Types</span></span>](mspeapconnectionpropertiesv2schema-complex-types.md)
</dt> </dl>

 

 




