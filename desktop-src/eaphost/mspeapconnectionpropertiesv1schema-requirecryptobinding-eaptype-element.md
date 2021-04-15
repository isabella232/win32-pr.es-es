---
title: Elemento RequireCryptoBinding (EapType)
description: Indica si se va a autenticar con servidores que admiten cryptobinding.
ms.assetid: 6b6a131d-8fce-4a5c-a649-891c4617b0f2
keywords:
- Elemento RequireCryptoBinding EAPHost
topic_type:
- apiref
api_name:
- RequireCryptoBinding
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 63ee456f87205346a935ad047cb8db9828febba6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422526"
---
# <a name="requirecryptobinding-eaptype-element"></a><span data-ttu-id="13400-104">Elemento RequireCryptoBinding (EapType)</span><span class="sxs-lookup"><span data-stu-id="13400-104">RequireCryptoBinding (EapType) Element</span></span>

<span data-ttu-id="13400-105">El elemento **RequireCryptoBinding (EapType)** indica si se va a autenticar con servidores que admiten cryptobinding.</span><span class="sxs-lookup"><span data-stu-id="13400-105">The **RequireCryptoBinding (EapType)** element indicates whether to authenticate with servers that support cryptobinding.</span></span>

``` syntax
<xs:element name="RequireCryptoBinding"
    type="boolean"
 />
```

<span data-ttu-id="13400-106">El elemento **RequireCryptoBinding** se define mediante el elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="13400-106">The **RequireCryptoBinding** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="13400-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13400-107">Remarks</span></span>

<span data-ttu-id="13400-108">Si el elemento **RequireCryptoBinding** es true, PEAP se autenticará con servidores que no admitan cryptobinding; Si es FALSE, PEAP solo se autenticará con servidores que admitan cryptobinding.</span><span class="sxs-lookup"><span data-stu-id="13400-108">If the **RequireCryptoBinding** element is TRUE, then PEAP will authenticate with servers that don't support cryptobinding; if FALSE, then PEAP will only authenticate with servers that support cryptobinding.</span></span> <span data-ttu-id="13400-109">El elemento **RequireCryptoBinding** es opcional.</span><span class="sxs-lookup"><span data-stu-id="13400-109">The **RequireCryptoBinding** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="13400-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13400-110">Requirements</span></span>



| <span data-ttu-id="13400-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="13400-111">Requirement</span></span> | <span data-ttu-id="13400-112">Value</span><span class="sxs-lookup"><span data-stu-id="13400-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="13400-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13400-113">Minimum supported client</span></span><br/> | <span data-ttu-id="13400-114">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="13400-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="13400-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="13400-115">Minimum supported server</span></span><br/> | <span data-ttu-id="13400-116">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="13400-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="13400-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="13400-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="13400-118">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="13400-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="13400-119">**EapType**</span><span class="sxs-lookup"><span data-stu-id="13400-119">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="13400-120">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="13400-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="13400-121">**EapType**</span><span class="sxs-lookup"><span data-stu-id="13400-121">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="13400-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="13400-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="13400-123">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="13400-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="13400-124">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="13400-124">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="13400-125">Elementos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="13400-125">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





