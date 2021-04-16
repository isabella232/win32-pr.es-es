---
description: Especifica un tipo de red.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: Elemento networkType (networkItemType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c63b8afdaf699fde6871c198a8235772c59da1ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678308"
---
# <a name="networktype-networkitemtype-element"></a><span data-ttu-id="40e73-103">Elemento networkType (networkItemType)</span><span class="sxs-lookup"><span data-stu-id="40e73-103">networkType (networkItemType) Element</span></span>

<span data-ttu-id="40e73-104">El elemento networkType (networkItemType) especifica un tipo de red.</span><span class="sxs-lookup"><span data-stu-id="40e73-104">The networkType (networkItemType) element specifies a network type.</span></span> <span data-ttu-id="40e73-105">Hay dos tipos de redes: redes de infraestructura (ESS) y redes ad hoc (IBSS).</span><span class="sxs-lookup"><span data-stu-id="40e73-105">There are two types of networks: infrastructure networks (ESS) and ad-hoc networks (IBSS).</span></span>

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

<span data-ttu-id="40e73-106">El elemento **NetworkType** se define mediante el tipo complejo de [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="40e73-106">The **networkType** element is defined by the [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="40e73-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="40e73-107">Requirements</span></span>



| <span data-ttu-id="40e73-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="40e73-108">Requirement</span></span> | <span data-ttu-id="40e73-109">Value</span><span class="sxs-lookup"><span data-stu-id="40e73-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="40e73-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40e73-110">Minimum supported client</span></span><br/> | <span data-ttu-id="40e73-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="40e73-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="40e73-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="40e73-112">Minimum supported server</span></span><br/> | <span data-ttu-id="40e73-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="40e73-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="40e73-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="40e73-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="40e73-115">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="40e73-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="40e73-116">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="40e73-116">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

<span data-ttu-id="40e73-117">**Posibles elementos primarios inmediatos en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="40e73-117">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="40e73-118">**red (permitidos)**</span><span class="sxs-lookup"><span data-stu-id="40e73-118">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[<span data-ttu-id="40e73-119">**red (bloqueo de listas)**</span><span class="sxs-lookup"><span data-stu-id="40e73-119">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




