---
title: Elemento FastReconnect (EapType)
description: Obtenga información sobre el elemento FastReconnect (EapType). Este elemento indica si se va a realizar una reconexión rápida.
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- Elemento FastReconnect EAPHost
topic_type:
- apiref
api_name:
- FastReconnect
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2214519db68b8c95b0e0efa91d68a7cd667b5f87
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "105695754"
---
# <a name="fastreconnect-eaptype-element"></a><span data-ttu-id="fee35-105">Elemento FastReconnect (EapType)</span><span class="sxs-lookup"><span data-stu-id="fee35-105">FastReconnect (EapType) Element</span></span>

<span data-ttu-id="fee35-106">El elemento **FastReconnect (EapType)** indica si se va a realizar una reconexión rápida.</span><span class="sxs-lookup"><span data-stu-id="fee35-106">The **FastReconnect (EapType)** element indicates whether to perform a fast reconnect.</span></span>

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

<span data-ttu-id="fee35-107">El elemento **FastReconnect** se define mediante el elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fee35-107">The **FastReconnect** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="fee35-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fee35-108">Remarks</span></span>

<span data-ttu-id="fee35-109">Si el elemento **FastReconnect** es true, PEAP intenta realizar una reconexión rápida. Si es FALSE, PEAP realiza la autenticación completa.</span><span class="sxs-lookup"><span data-stu-id="fee35-109">If the **FastReconnect** element is TRUE, then PEAP attempts to perform a fast reconnect; if FALSE, PEAP performs the full authentication.</span></span> <span data-ttu-id="fee35-110">El elemento **FastReconnect** es opcional.</span><span class="sxs-lookup"><span data-stu-id="fee35-110">The **FastReconnect** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="fee35-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fee35-111">Requirements</span></span>



| <span data-ttu-id="fee35-112">Role</span><span class="sxs-lookup"><span data-stu-id="fee35-112">Role</span></span> | <span data-ttu-id="fee35-113">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="fee35-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="fee35-114">Remoto</span><span class="sxs-lookup"><span data-stu-id="fee35-114">Client</span></span><br/> | <span data-ttu-id="fee35-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fee35-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fee35-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="fee35-116">Server</span></span><br/> | <span data-ttu-id="fee35-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="fee35-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fee35-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="fee35-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="fee35-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="fee35-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fee35-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="fee35-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="fee35-121">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="fee35-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fee35-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="fee35-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="fee35-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="fee35-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="fee35-124">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="fee35-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="fee35-125">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fee35-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="fee35-126">Elementos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="fee35-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





