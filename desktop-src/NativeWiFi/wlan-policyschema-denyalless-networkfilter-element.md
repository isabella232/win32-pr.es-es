---
description: Especifica si el acceso a todas las redes de infraestructura está bloqueado.
ms.assetid: d57ae27c-3cd3-4e53-b5c9-cd3cbb91289b
title: Elemento denyAllESS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllESS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c3e83aeb14e0572f8e2ccc49bf2d04718afa7f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275325"
---
# <a name="denyalless-networkfilter-element"></a><span data-ttu-id="2a02b-103">Elemento denyAllESS (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="2a02b-103">denyAllESS (networkFilter) Element</span></span>

<span data-ttu-id="2a02b-104">El elemento denyAllESS (networkFilter) especifica si el acceso a todas las redes de infraestructura está bloqueado.</span><span class="sxs-lookup"><span data-stu-id="2a02b-104">The denyAllESS (networkFilter) element specifies if access to all infrastructure networks is blocked.</span></span> <span data-ttu-id="2a02b-105">Cuando **denyAllESS** tiene un valor true, las máquinas no se pueden conectar a una red de infraestructura; de lo contrario, las máquinas pueden conectarse a redes de infraestructura.</span><span class="sxs-lookup"><span data-stu-id="2a02b-105">When **denyAllESS** has a value of TRUE, machines cannot connect to an infrastructure network; otherwise, machines may connect to infrastructure networks.</span></span>

<span data-ttu-id="2a02b-106">El valor predeterminado de este elemento es FALSE.</span><span class="sxs-lookup"><span data-stu-id="2a02b-106">The default value for this element is FALSE.</span></span> <span data-ttu-id="2a02b-107">Si **denyAllESS** no se especifica en un perfil, los equipos pueden conectarse a las redes de infraestructura de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="2a02b-107">If **denyAllESS** is not specified in a profile, then by default machines may connect to infrastructure networks.</span></span>

``` syntax
<xs:element name="denyAllESS"
    type="boolean"
 />
```

<span data-ttu-id="2a02b-108">El elemento **denyAllESS** se define mediante el elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2a02b-108">The **denyAllESS** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a02b-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a02b-109">Requirements</span></span>



| <span data-ttu-id="2a02b-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a02b-110">Requirement</span></span> | <span data-ttu-id="2a02b-111">Value</span><span class="sxs-lookup"><span data-stu-id="2a02b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2a02b-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a02b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="2a02b-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="2a02b-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2a02b-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2a02b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="2a02b-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="2a02b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a02b-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="2a02b-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="2a02b-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="2a02b-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2a02b-118">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="2a02b-118">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="2a02b-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="2a02b-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2a02b-120">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="2a02b-120">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




