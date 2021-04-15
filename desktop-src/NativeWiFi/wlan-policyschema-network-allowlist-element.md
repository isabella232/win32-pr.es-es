---
description: Define una red permitida.
ms.assetid: 6dd90924-ded4-427d-a6cd-7742acf89c21
title: Elemento Network (permitidos)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- network
api_type:
- Schema
api_location: ''
ms.openlocfilehash: eb89a3037b7684c4e20e26ef3a2b0502be69251a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688540"
---
# <a name="network-allowlist-element"></a><span data-ttu-id="d4308-103">Elemento Network (permitidos)</span><span class="sxs-lookup"><span data-stu-id="d4308-103">network (allowList) Element</span></span>

<span data-ttu-id="d4308-104">El elemento de red (permitidos) define una red permitida.</span><span class="sxs-lookup"><span data-stu-id="d4308-104">The network (allowList) element defines an allowed network.</span></span> <span data-ttu-id="d4308-105">Un equipo debe tener permiso para conectarse a una red permitida.</span><span class="sxs-lookup"><span data-stu-id="d4308-105">A machine must be allowed to connect to an allowed network.</span></span>

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

<span data-ttu-id="d4308-106">El elemento de **red** se define mediante el elemento [**permitidos**](wlan-policyschema-allowlist-networkfilter-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d4308-106">The **network** element is defined by the [**allowList**](wlan-policyschema-allowlist-networkfilter-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4308-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4308-107">Requirements</span></span>



| <span data-ttu-id="d4308-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4308-108">Requirement</span></span> | <span data-ttu-id="d4308-109">Value</span><span class="sxs-lookup"><span data-stu-id="d4308-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d4308-110">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4308-110">Minimum supported client</span></span><br/> | <span data-ttu-id="d4308-111">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d4308-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d4308-112">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d4308-112">Minimum supported server</span></span><br/> | <span data-ttu-id="d4308-113">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d4308-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d4308-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="d4308-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="d4308-115">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="d4308-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d4308-116">**Permitidos**</span><span class="sxs-lookup"><span data-stu-id="d4308-116">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> <dt>

<span data-ttu-id="d4308-117">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="d4308-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d4308-118">**Permitidos (networkFilter)**</span><span class="sxs-lookup"><span data-stu-id="d4308-118">**allowList (networkFilter)**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)
</dt> </dl>

 

 




