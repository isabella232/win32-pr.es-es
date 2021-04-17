---
title: Elemento DifferentUsername (EapType)
description: Obtenga información sobre el elemento DifferentUsername (EapType). Este elemento determina el nombre de usuario EAP-TLS que se va a usar.
ms.assetid: f0ce41a9-c774-4d12-8a5a-a8eb1eb84cb0
keywords:
- Elemento DifferentUsername EAPHost
topic_type:
- apiref
api_name:
- DifferentUsername
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 505e23c74d4c1c8c74a50906809d0acc9ce06c42
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105705025"
---
# <a name="differentusername-eaptype-element"></a><span data-ttu-id="44a8c-105">Elemento DifferentUsername (EapType)</span><span class="sxs-lookup"><span data-stu-id="44a8c-105">DifferentUsername (EapType) Element</span></span>

<span data-ttu-id="44a8c-106">El elemento **DifferentUsername (EapType)** determina el nombre de usuario EAP-TLS que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="44a8c-106">The **DifferentUsername (EapType)** element determines which user name EAP-TLS is to use.</span></span>

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

<span data-ttu-id="44a8c-107">El elemento **DifferentUsername** se define mediante el elemento [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="44a8c-107">The **DifferentUsername** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="44a8c-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44a8c-108">Remarks</span></span>

<span data-ttu-id="44a8c-109">Si el elemento **DifferentUserName** es true, EAP-TLS debe usar un nombre de usuario distinto del nombre que aparece en el certificado.</span><span class="sxs-lookup"><span data-stu-id="44a8c-109">If the **DifferentUserName** element is TRUE, EAP-TLS should use a user name other than the name that appears on the certificate.</span></span> <span data-ttu-id="44a8c-110">Si el elemento **DifferentUserName** es false, EAP-TLS usa el nombre de usuario que aparece en el certificado.</span><span class="sxs-lookup"><span data-stu-id="44a8c-110">If the **DifferentUserName** element is FALSE, EAP-TLS uses the user name that appears on the certificate.</span></span>

<span data-ttu-id="44a8c-111">El elemento **DifferentUserName** es opcional.</span><span class="sxs-lookup"><span data-stu-id="44a8c-111">The **DifferentUserName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="44a8c-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="44a8c-112">Requirements</span></span>



| <span data-ttu-id="44a8c-113">Role</span><span class="sxs-lookup"><span data-stu-id="44a8c-113">Role</span></span> | <span data-ttu-id="44a8c-114">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="44a8c-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="44a8c-115">Remoto</span><span class="sxs-lookup"><span data-stu-id="44a8c-115">Client</span></span><br/> | <span data-ttu-id="44a8c-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="44a8c-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="44a8c-117">Servidor</span><span class="sxs-lookup"><span data-stu-id="44a8c-117">Server</span></span><br/> | <span data-ttu-id="44a8c-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="44a8c-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44a8c-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="44a8c-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="44a8c-120">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="44a8c-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="44a8c-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="44a8c-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="44a8c-122">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="44a8c-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="44a8c-123">**EapType**</span><span class="sxs-lookup"><span data-stu-id="44a8c-123">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="44a8c-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="44a8c-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="44a8c-125">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="44a8c-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="44a8c-126">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="44a8c-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="44a8c-127">Elementos de esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="44a8c-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





