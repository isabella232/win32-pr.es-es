---
title: Elemento InnerEapOptional (EapType)
description: Obtenga información sobre el elemento InnerEapOptional (EapType). Este elemento indica si se va a realizar el acceso de invitado.
ms.assetid: 2d314c89-5415-407f-84c3-c4c5c8957b39
keywords:
- Elemento InnerEapOptional EAPHost
topic_type:
- apiref
api_name:
- InnerEapOptional
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be63845f389936656172b4cbb4e42de659bbf0e1
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149620"
---
# <a name="innereapoptional-eaptype-element"></a><span data-ttu-id="88267-105">Elemento InnerEapOptional (EapType)</span><span class="sxs-lookup"><span data-stu-id="88267-105">InnerEapOptional (EapType) Element</span></span>

<span data-ttu-id="88267-106">El elemento **InnerEapOptional (EapType)** indica si se va a realizar el acceso de invitado.</span><span class="sxs-lookup"><span data-stu-id="88267-106">The **InnerEapOptional (EapType)** element indicates whether to perform GUEST access.</span></span>

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

<span data-ttu-id="88267-107">El elemento **InnerEapOptional** se define mediante el elemento [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="88267-107">The **InnerEapOptional** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="88267-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="88267-108">Remarks</span></span>

<span data-ttu-id="88267-109">Si el elemento **InnerEapOptional** es true, el elemento [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) debe estar presente y describir el método interno y su configuración; Si es FALSE, PEAP realizará el acceso de invitado.</span><span class="sxs-lookup"><span data-stu-id="88267-109">If the **InnerEapOptional** element is TRUE, then the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present and describe the inner method and it's configuration; if FALSE, then PEAP will perform GUEST access.</span></span> <span data-ttu-id="88267-110">El elemento **InnerEapOptional** es opcional.</span><span class="sxs-lookup"><span data-stu-id="88267-110">The **InnerEapOptional** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="88267-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88267-111">Requirements</span></span>



| <span data-ttu-id="88267-112">Role</span><span class="sxs-lookup"><span data-stu-id="88267-112">Role</span></span> | <span data-ttu-id="88267-113">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="88267-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="88267-114">Remoto</span><span class="sxs-lookup"><span data-stu-id="88267-114">Client</span></span><br/> | <span data-ttu-id="88267-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="88267-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="88267-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="88267-116">Server</span></span><br/> | <span data-ttu-id="88267-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="88267-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88267-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="88267-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="88267-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="88267-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="88267-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="88267-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="88267-121">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="88267-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="88267-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="88267-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="88267-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="88267-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="88267-124">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="88267-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="88267-125">Esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="88267-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="88267-126">Elementos de esquema mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="88267-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





