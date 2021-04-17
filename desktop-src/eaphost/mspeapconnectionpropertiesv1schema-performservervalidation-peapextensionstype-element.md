---
title: Elemento PerformServerValidation (PeapExtensionsType) (esquema V1)
description: Obtenga información sobre el elemento PerformServerValidation (PeapExtensionsType). Este elemento indica si se realiza la validación del servidor. | Elemento PerformServerValidation (PeapExtensionsType) (esquema V1)
ms.assetid: b0483ed0-a02f-4f60-b1ae-7c5e6be8e196
keywords:
- elemento EAPHost
topic_type:
- apiref
api_name:
- PerformServerValidation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 256d942d68c30788180f2d8080f963c1d79b401a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105717464"
---
# <a name="performservervalidation-peapextensionstype-element-v1-schema"></a><span data-ttu-id="2c4b3-106">Elemento PerformServerValidation (PeapExtensionsType) (esquema V1)</span><span class="sxs-lookup"><span data-stu-id="2c4b3-106">PerformServerValidation (PeapExtensionsType) element (v1 schema)</span></span>

<span data-ttu-id="2c4b3-107">El elemento **PerformServerValidation (PeapExtensionsType)** indica si se realiza la validación del servidor.</span><span class="sxs-lookup"><span data-stu-id="2c4b3-107">The **PerformServerValidation (PeapExtensionsType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    ref="extendedPeap:PerformServerValidation"
 />
```

<span data-ttu-id="2c4b3-108">El elemento se define mediante el elemento [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="2c4b3-108">The element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c4b3-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2c4b3-109">Remarks</span></span>

<span data-ttu-id="2c4b3-110">El elemento **PerformServerValidation** es opcional.</span><span class="sxs-lookup"><span data-stu-id="2c4b3-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c4b3-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2c4b3-111">Requirements</span></span>



| <span data-ttu-id="2c4b3-112">Role</span><span class="sxs-lookup"><span data-stu-id="2c4b3-112">Role</span></span> | <span data-ttu-id="2c4b3-113">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2c4b3-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="2c4b3-114">Remoto</span><span class="sxs-lookup"><span data-stu-id="2c4b3-114">Client</span></span><br/> | <span data-ttu-id="2c4b3-115">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c4b3-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="2c4b3-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="2c4b3-116">Server</span></span><br/> | <span data-ttu-id="2c4b3-117">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2c4b3-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2c4b3-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="2c4b3-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="2c4b3-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="2c4b3-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2c4b3-120">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="2c4b3-120">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="2c4b3-121">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="2c4b3-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2c4b3-122">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="2c4b3-122">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="2c4b3-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="2c4b3-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="2c4b3-124">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="2c4b3-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2c4b3-125">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2c4b3-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="2c4b3-126">Elementos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2c4b3-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="2c4b3-127">**PerformServerValidation(PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="2c4b3-127">**PerformServerValidation(PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv2-performservervalidation-peapextensionstype-element.md)
</dt> </dl>

 

 





