---
description: Especifica el identificador del conjunto de servicios (SSID) de una red inalámbrica.
ms.assetid: 103808f2-9e5f-4605-b42a-337a13455294
title: Elemento networkName (networkItemType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkName
api_type:
- Schema
api_location: ''
ms.openlocfilehash: da635c392a29419e7b151cc2c4fb080ff7d3fca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912526"
---
# <a name="networkname-networkitemtype-element"></a><span data-ttu-id="ccc30-103">Elemento networkName (networkItemType)</span><span class="sxs-lookup"><span data-stu-id="ccc30-103">networkName (networkItemType) Element</span></span>

<span data-ttu-id="ccc30-104">El elemento networkName (networkItemType) especifica el identificador del conjunto de servicios (SSID) de una red inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="ccc30-104">The networkName (networkItemType) element specifies the service set identifier (SSID) of a wireless network.</span></span>

``` syntax
<xs:element name="networkName"
    type="networkNameType"
 />
```

<span data-ttu-id="ccc30-105">El elemento **networkName** se define mediante el tipo complejo de [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="ccc30-105">The **networkName** element is defined by the [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccc30-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccc30-106">Requirements</span></span>



| <span data-ttu-id="ccc30-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccc30-107">Requirement</span></span> | <span data-ttu-id="ccc30-108">Value</span><span class="sxs-lookup"><span data-stu-id="ccc30-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ccc30-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccc30-109">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc30-110">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ccc30-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ccc30-111">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ccc30-111">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc30-112">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ccc30-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ccc30-113">Vea también</span><span class="sxs-lookup"><span data-stu-id="ccc30-113">See also</span></span>

<dl> <dt>

<span data-ttu-id="ccc30-114">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="ccc30-114">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="ccc30-115">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="ccc30-115">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

<span data-ttu-id="ccc30-116">**Posibles elementos primarios inmediatos en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="ccc30-116">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="ccc30-117">**red (permitidos)**</span><span class="sxs-lookup"><span data-stu-id="ccc30-117">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[<span data-ttu-id="ccc30-118">**red (bloqueo de listas)**</span><span class="sxs-lookup"><span data-stu-id="ccc30-118">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




