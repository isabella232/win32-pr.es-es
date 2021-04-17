---
description: Especifica si el acceso a todas las redes ad hoc está bloqueado.
ms.assetid: 9001ccbb-c158-44d7-8d31-38c91881886e
title: Elemento denyAllIBSS (networkFilter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- denyAllIBSS
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 78a34b506f4db72d8b61d7c0918c93658e18a062
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677341"
---
# <a name="denyallibss-networkfilter-element"></a><span data-ttu-id="70ac6-103">Elemento denyAllIBSS (networkFilter)</span><span class="sxs-lookup"><span data-stu-id="70ac6-103">denyAllIBSS (networkFilter) Element</span></span>

<span data-ttu-id="70ac6-104">El elemento denyAllIBSS (networkFilter) especifica si se bloquea el acceso a todas las redes ad hoc.</span><span class="sxs-lookup"><span data-stu-id="70ac6-104">The denyAllIBSS (networkFilter) element specifies if access to all ad-hoc networks is blocked.</span></span> <span data-ttu-id="70ac6-105">Cuando **denyAllIBSS** tiene un valor true, las máquinas no se pueden conectar a una red ad hoc; de lo contrario, es posible que los equipos se conecten a redes ad hoc.</span><span class="sxs-lookup"><span data-stu-id="70ac6-105">When **denyAllIBSS** has a value of TRUE, machines cannot connect to an ad-hoc network; otherwise, machines may connect to ad-hoc networks.</span></span>

<span data-ttu-id="70ac6-106">El valor predeterminado de este elemento es FALSE.</span><span class="sxs-lookup"><span data-stu-id="70ac6-106">The default value for this element is FALSE.</span></span> <span data-ttu-id="70ac6-107">Si **denyAllIBSS** no se especifica en un perfil, los equipos pueden conectarse a las redes ad hoc de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="70ac6-107">If **denyAllIBSS** is not specified in a profile, then by default machines may connect to ad-hoc networks.</span></span>

``` syntax
<xs:element name="denyAllIBSS"
    type="boolean"
 />
```

<span data-ttu-id="70ac6-108">El elemento **denyAllIBSS** se define mediante el elemento [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="70ac6-108">The **denyAllIBSS** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="70ac6-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70ac6-109">Requirements</span></span>



| <span data-ttu-id="70ac6-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="70ac6-110">Requirement</span></span> | <span data-ttu-id="70ac6-111">Value</span><span class="sxs-lookup"><span data-stu-id="70ac6-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="70ac6-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70ac6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="70ac6-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="70ac6-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="70ac6-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70ac6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="70ac6-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="70ac6-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70ac6-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="70ac6-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="70ac6-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="70ac6-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="70ac6-118">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="70ac6-118">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="70ac6-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="70ac6-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="70ac6-120">**networkFilter (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="70ac6-120">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




