---
title: Elemento PerformServerValidation (PeapExtensionsType) (esquema V2)
description: Obtenga información sobre el elemento PerformServerValidation (PeapExtensionsType). Este elemento indica si se realiza la validación del servidor. | Elemento PerformServerValidation (PeapExtensionsType) (esquema V2)
ms.assetid: a9c383d4-2582-47dd-bdf1-dd4e6c1689f7
keywords:
- Elemento PerformServerValidation EAPHost
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
ms.openlocfilehash: 32bc213aa67e87eb8af0643a15f16b298cfb3204
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104280107"
---
# <a name="performservervalidation-peapextensionstype-element-v2-schema"></a><span data-ttu-id="0a9e2-106">Elemento PerformServerValidation (PeapExtensionsType) (esquema V2)</span><span class="sxs-lookup"><span data-stu-id="0a9e2-106">PerformServerValidation (PeapExtensionsType) Element (V2 schema)</span></span>

<span data-ttu-id="0a9e2-107">El elemento **PerformServerValidation (PeapExtensionsType)** indica si se realiza la validación del servidor.</span><span class="sxs-lookup"><span data-stu-id="0a9e2-107">The **PerformServerValidation (PeapExtensionsType)** element indicates whether server validation is performed.</span></span>

``` syntax
<xs:element name="PerformServerValidation"
    type="xs:boolean"
 />
```

<span data-ttu-id="0a9e2-108">El elemento **PerformServerValidation** se define mediante el elemento [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0a9e2-108">The **PerformServerValidation** element is defined by the [**PeapExtensionsType**](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a9e2-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0a9e2-109">Remarks</span></span>

<span data-ttu-id="0a9e2-110">El elemento **PerformServerValidation** es opcional.</span><span class="sxs-lookup"><span data-stu-id="0a9e2-110">The **PerformServerValidation** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a9e2-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0a9e2-111">Requirements</span></span>



| <span data-ttu-id="0a9e2-112">Role</span><span class="sxs-lookup"><span data-stu-id="0a9e2-112">Role</span></span> | <span data-ttu-id="0a9e2-113">Versión de SO mínima</span><span class="sxs-lookup"><span data-stu-id="0a9e2-113">Minimum OS version</span></span> |
|------|--------------------|
| <span data-ttu-id="0a9e2-114">Remoto</span><span class="sxs-lookup"><span data-stu-id="0a9e2-114">Client</span></span><br/> | <span data-ttu-id="0a9e2-115">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a9e2-115">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="0a9e2-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="0a9e2-116">Server</span></span><br/> | <span data-ttu-id="0a9e2-117">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="0a9e2-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0a9e2-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a9e2-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="0a9e2-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="0a9e2-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0a9e2-120">**PeapExtensionsType**</span><span class="sxs-lookup"><span data-stu-id="0a9e2-120">**PeapExtensionsType**</span></span>](mspeapconnectionpropertiesv1schema-peapextensionstype-complextype.md)
</dt> <dt>

<span data-ttu-id="0a9e2-121">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="0a9e2-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0a9e2-122">**PeapExtensions**</span><span class="sxs-lookup"><span data-stu-id="0a9e2-122">**PeapExtensions**</span></span>](mspeapconnectionpropertiesv1schema-peapextensions-eaptype-element.md)
<span data-ttu-id="0a9e2-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="0a9e2-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="0a9e2-124">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="0a9e2-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="0a9e2-125">Esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="0a9e2-125">mspeapconnectionpropertiesv2 Schema</span></span>](mspeapconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="0a9e2-126">Elementos de esquema mspeapconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="0a9e2-126">mspeapconnectionpropertiesv2 Schema Elements</span></span>](mspeapconnectionpropertiesv2schema-elements.md)
</dt> </dl>

 

 





