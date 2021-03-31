---
title: Elemento EnableQuarantineChecks (EapType)
description: Obtenga información sobre el elemento EnableQuarantineChecks (EapType). Este elemento indica si se deben realizar comprobaciones de protección de acceso a redes (NAP).
ms.assetid: bd5c7efc-f857-4e21-9cd8-0a1cbe5a87d8
keywords:
- Elemento EnableQuarantineChecks EAPHost
topic_type:
- apiref
api_name:
- EnableQuarantineChecks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0becd1add038bb91307095eaf5cd0743d383632b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995647"
---
# <a name="enablequarantinechecks-eaptype-element"></a><span data-ttu-id="0ca98-105">Elemento EnableQuarantineChecks (EapType)</span><span class="sxs-lookup"><span data-stu-id="0ca98-105">EnableQuarantineChecks (EapType) Element</span></span>

<span data-ttu-id="0ca98-106">El elemento **EnableQuarantineChecks (EapType)** indica si se deben realizar comprobaciones de protección de acceso a redes (NAP).</span><span class="sxs-lookup"><span data-stu-id="0ca98-106">The **EnableQuarantineChecks (EapType)** element indicates whether to perform Network Access Protection (NAP) checks.</span></span>

``` syntax
<xs:element name="EnableQuarantineChecks"
    type="boolean"
 />
```

<span data-ttu-id="0ca98-107">El elemento **EnableQuarantineChecks** se define mediante el elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="0ca98-107">The **EnableQuarantineChecks** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ca98-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0ca98-108">Remarks</span></span>

<span data-ttu-id="0ca98-109">Si el elemento **EnableQuarantineChecks** es true, PEAP realizará comprobaciones de NAP; Si es FALSE, PEAP no realizará comprobaciones de NAP.</span><span class="sxs-lookup"><span data-stu-id="0ca98-109">If the **EnableQuarantineChecks** element is TRUE, then PEAP will perform NAP checks; if FALSE, PEAP will not perform NAP checks.</span></span> <span data-ttu-id="0ca98-110">El elemento **EnableQuarantineChecks** es opcional.</span><span class="sxs-lookup"><span data-stu-id="0ca98-110">The **EnableQuarantineChecks** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ca98-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0ca98-111">Requirements</span></span>



| <span data-ttu-id="0ca98-112">Role</span><span class="sxs-lookup"><span data-stu-id="0ca98-112">Role</span></span> | <span data-ttu-id="0ca98-113">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="0ca98-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="0ca98-114">Remoto</span><span class="sxs-lookup"><span data-stu-id="0ca98-114">Client</span></span><br/> | <span data-ttu-id="0ca98-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="0ca98-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0ca98-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="0ca98-116">Server</span></span><br/> | <span data-ttu-id="0ca98-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="0ca98-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0ca98-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="0ca98-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="0ca98-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="0ca98-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0ca98-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="0ca98-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="0ca98-121">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="0ca98-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0ca98-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="0ca98-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="0ca98-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="0ca98-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="0ca98-124">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="0ca98-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="0ca98-125">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="0ca98-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="0ca98-126">Elementos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="0ca98-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





