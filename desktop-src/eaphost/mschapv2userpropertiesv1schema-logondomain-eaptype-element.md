---
title: Elemento LogonDomain (EapType)
description: Obtenga información sobre el elemento LogonDomain (EapType). Este elemento identifica el dominio del usuario o equipo que se va a autenticar.
ms.assetid: a93793cd-29ee-47f9-8d91-895844c08bae
keywords:
- Elemento LogonDomain EAPHost
topic_type:
- apiref
api_name:
- LogonDomain
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3dbbe57bcd29459f6e9807d8f39aedb4faa72a1b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078356"
---
# <a name="logondomain-eaptype-element"></a><span data-ttu-id="36808-105">Elemento LogonDomain (EapType)</span><span class="sxs-lookup"><span data-stu-id="36808-105">LogonDomain (EapType) Element</span></span>

<span data-ttu-id="36808-106">El elemento **LogonDomain (EapType)** identifica el dominio del usuario o equipo que se va a autenticar.</span><span class="sxs-lookup"><span data-stu-id="36808-106">The **LogonDomain (EapType)** element identifies the domain of the user or machine being authenticated.</span></span>

``` syntax
<xs:element name="LogonDomain
          
        "
    type="string"
 />
```

<span data-ttu-id="36808-107">El elemento **LogonDomain** se define mediante el elemento [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="36808-107">The **LogonDomain** element is defined by the [**EapType**](mschapv2userpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="36808-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="36808-108">Remarks</span></span>

<span data-ttu-id="36808-109">Si el elemento **LogonDomain (EapType)** no está presente, se usa el dominio de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="36808-109">If the **LogonDomain (EapType)** element is not present, the domain from winlogon is used.</span></span> <span data-ttu-id="36808-110">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="36808-110">This element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="36808-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36808-111">Requirements</span></span>



| <span data-ttu-id="36808-112">Role</span><span class="sxs-lookup"><span data-stu-id="36808-112">Role</span></span> | <span data-ttu-id="36808-113">Versión mínima admitida del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="36808-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="36808-114">Remoto</span><span class="sxs-lookup"><span data-stu-id="36808-114">Client</span></span><br/> | <span data-ttu-id="36808-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="36808-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="36808-116">Servidor</span><span class="sxs-lookup"><span data-stu-id="36808-116">Server</span></span><br/> | <span data-ttu-id="36808-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="36808-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="36808-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="36808-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="36808-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="36808-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="36808-120">**EapType**</span><span class="sxs-lookup"><span data-stu-id="36808-120">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="36808-121">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="36808-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="36808-122">**EapType**</span><span class="sxs-lookup"><span data-stu-id="36808-122">**EapType**</span></span>](mschapv2userpropertiesv1schema-eaptype-element.md)
</dt> <dt>

[<span data-ttu-id="36808-123">EAPHost y esquema heredado</span><span class="sxs-lookup"><span data-stu-id="36808-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="36808-124">Esquema mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="36808-124">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





