---
title: Elemento ServerNames (ServerValidationParameters) (PEAP)
description: Obtenga información sobre el elemento ServerNames (ServerValidationParameters). Este elemento representa una lista de nombres de servidor delimitados por punto y coma. | Elemento ServerNames (ServerValidationParameters) (PEAP)
ms.assetid: 2595daa1-9f1b-40cf-9219-0e7295fdd5c3
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
ms.openlocfilehash: 40aa7ba317b7ba7c3f7a06cce87ef57c2906fe4b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105649345"
---
# <a name="servernames-servervalidationparameters-element-peap"></a><span data-ttu-id="412d1-106">Elemento ServerNames (ServerValidationParameters) (PEAP)</span><span class="sxs-lookup"><span data-stu-id="412d1-106">ServerNames (ServerValidationParameters) element (PEAP)</span></span>

<span data-ttu-id="412d1-107">El elemento **servernames (ServerValidationParameters)** representa una lista de nombres de servidor delimitados por punto y coma.</span><span class="sxs-lookup"><span data-stu-id="412d1-107">The **ServerNames (ServerValidationParameters)** element represents a list of semicolon delimited server names.</span></span>

``` syntax
<xs:element name="ServerNames"
    type="string"
    minOccurs="0"
 />
```

<span data-ttu-id="412d1-108">El elemento **servernames** se define mediante el tipo complejo [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="412d1-108">The **ServerNames** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="412d1-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="412d1-109">Remarks</span></span>

<span data-ttu-id="412d1-110">Cada nombre de servidor está delimitado por punto y coma, y se puede representar mediante expresiones regulares.</span><span class="sxs-lookup"><span data-stu-id="412d1-110">Each server name is delimited by semicolons, and can be represented by regular expressions.</span></span> <span data-ttu-id="412d1-111">El elemento **servernames** es opcional.</span><span class="sxs-lookup"><span data-stu-id="412d1-111">The **ServerNames** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="412d1-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="412d1-112">Requirements</span></span>



| <span data-ttu-id="412d1-113">Role</span><span class="sxs-lookup"><span data-stu-id="412d1-113">Role</span></span> | <span data-ttu-id="412d1-114">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="412d1-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="412d1-115">Remoto</span><span class="sxs-lookup"><span data-stu-id="412d1-115">Client</span></span><br/> | <span data-ttu-id="412d1-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="412d1-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="412d1-117">Servidor</span><span class="sxs-lookup"><span data-stu-id="412d1-117">Server</span></span><br/> | <span data-ttu-id="412d1-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="412d1-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="412d1-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="412d1-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="412d1-120">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="412d1-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="412d1-121">**ServerValidationParameters**</span><span class="sxs-lookup"><span data-stu-id="412d1-121">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="412d1-122">**Posibles elementos primarios inmediatos en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="412d1-122">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="412d1-123">**ServerValidation (EapType)**</span><span class="sxs-lookup"><span data-stu-id="412d1-123">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="412d1-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="412d1-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="412d1-125">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="412d1-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="412d1-126">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="412d1-126">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="412d1-127">Elementos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="412d1-127">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





