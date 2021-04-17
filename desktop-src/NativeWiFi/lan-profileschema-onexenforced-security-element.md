---
description: Especifica si el servicio de configuración automática para redes cableadas requiere el uso de 802.1 X para la autenticación de puertos.
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: Elemento OneXEnforced (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnforced
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e6656238b0745f8bfef9aff5bcb0b80775dd1da2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678133"
---
# <a name="onexenforced-security-element"></a><span data-ttu-id="8a083-103">Elemento OneXEnforced (Security)</span><span class="sxs-lookup"><span data-stu-id="8a083-103">OneXEnforced (security) Element</span></span>

<span data-ttu-id="8a083-104">El elemento **OneXEnforced** (Security) especifica si el servicio de configuración automática para redes cableadas requiere el uso de 802.1 x para la autenticación de puertos.</span><span class="sxs-lookup"><span data-stu-id="8a083-104">The **OneXEnforced** (security) element specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <span data-ttu-id="8a083-105">Cuando **OneXEnforced** es true, el servicio de configuración automática debe usar 802.1 x para la autenticación de puertos.</span><span class="sxs-lookup"><span data-stu-id="8a083-105">When **OneXEnforced** is TRUE, the automatic configuration service must use 802.1X for port authentication.</span></span> <span data-ttu-id="8a083-106">Cuando **OneXEnforced** es false, el servicio de configuración automática intentará usar 802.1 x para la autenticación de puerto, pero el servicio revertirá a ninguna autenticación si se produce un error en la autenticación 802.1 x por cualquier motivo.</span><span class="sxs-lookup"><span data-stu-id="8a083-106">When **OneXEnforced** is FALSE, then the automatic configuration service will attempt to use 802.1X for port authentication, but the service will fall back to no authentication if 802.1X authentication fails for any reason.</span></span>

<span data-ttu-id="8a083-107">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="8a083-107">This element is optional.</span></span> <span data-ttu-id="8a083-108">El valor predeterminado es FALSE.</span><span class="sxs-lookup"><span data-stu-id="8a083-108">The default value is FALSE.</span></span>

<span data-ttu-id="8a083-109">Este elemento solo tiene un valor significativo si [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) es true.</span><span class="sxs-lookup"><span data-stu-id="8a083-109">This element only has a meaningful value if [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) is TRUE.</span></span> <span data-ttu-id="8a083-110">Si **OneXEnabled** es false, se omite el valor de este elemento.</span><span class="sxs-lookup"><span data-stu-id="8a083-110">If **OneXEnabled** is FALSE, then the value of this element is ignored.</span></span>

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

<span data-ttu-id="8a083-111">El elemento **OneXEnforced** se define mediante el elemento [**Security**](lan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8a083-111">The **OneXEnforced** element is defined by the [**security**](lan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a083-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8a083-112">Requirements</span></span>



| <span data-ttu-id="8a083-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="8a083-113">Requirement</span></span> | <span data-ttu-id="8a083-114">Value</span><span class="sxs-lookup"><span data-stu-id="8a083-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8a083-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a083-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8a083-116">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="8a083-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8a083-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8a083-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8a083-118">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="8a083-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a083-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="8a083-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="8a083-120">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="8a083-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8a083-121">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="8a083-121">**security**</span></span>](lan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="8a083-122">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="8a083-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8a083-123">**seguridad (MSM)**</span><span class="sxs-lookup"><span data-stu-id="8a083-123">**security (MSM)**</span></span>](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




