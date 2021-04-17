---
title: Elemento ServerNames (ServerValidationParameters) (TLS)
description: Obtenga información sobre el elemento ServerNames (ServerValidationParameters). Este elemento representa una lista de nombres de servidor delimitados por punto y coma. | Elemento ServerNames (ServerValidationParameters) (TLS)
ms.assetid: c6cfcc67-4e6a-4bf0-87d9-37cc1d504598
keywords:
- Elemento ServerNames EAPHost
topic_type:
- apiref
api_name:
- ServerNames
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ef94bc650432c4fb87abf00a93841d0d4d42e965
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105698156"
---
# <a name="servernames-servervalidationparameters-element-tls"></a><span data-ttu-id="fd1dd-106">Elemento ServerNames (ServerValidationParameters) (TLS)</span><span class="sxs-lookup"><span data-stu-id="fd1dd-106">ServerNames (ServerValidationParameters) element (TLS)</span></span>

<span data-ttu-id="fd1dd-107">El elemento **servernames (ServerValidationParameters)** representa una lista de nombres de servidor delimitados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-107">The **ServerNames (ServerValidationParameters)** element represents a list of semicolon delimited server names.</span></span>

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="fd1dd-108">El elemento **servernames** se define mediante el tipo complejo [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="fd1dd-108">The **ServerNames** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd1dd-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fd1dd-109">Remarks</span></span>

<span data-ttu-id="fd1dd-110">Cada nombre de servidor está delimitado por punto y coma, y se puede representar mediante expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-110">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <span data-ttu-id="fd1dd-111">El elemento **servernames** es opcional.</span><span class="sxs-lookup"><span data-stu-id="fd1dd-111">The **ServerNames** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd1dd-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd1dd-112">Requirements</span></span>



| <span data-ttu-id="fd1dd-113">Role</span><span class="sxs-lookup"><span data-stu-id="fd1dd-113">Role</span></span> | <span data-ttu-id="fd1dd-114">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="fd1dd-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="fd1dd-115">Remoto</span><span class="sxs-lookup"><span data-stu-id="fd1dd-115">Client</span></span><br/> | <span data-ttu-id="fd1dd-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fd1dd-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fd1dd-117">Servidor</span><span class="sxs-lookup"><span data-stu-id="fd1dd-117">Server</span></span><br/> | <span data-ttu-id="fd1dd-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fd1dd-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fd1dd-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd1dd-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="fd1dd-120">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="fd1dd-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fd1dd-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="fd1dd-121">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="fd1dd-122">**Posibles elementos primarios inmediatos en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="fd1dd-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fd1dd-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="fd1dd-123">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="fd1dd-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="fd1dd-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="fd1dd-125">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="fd1dd-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="fd1dd-126">Esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fd1dd-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="fd1dd-127">Elementos de esquema eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fd1dd-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





