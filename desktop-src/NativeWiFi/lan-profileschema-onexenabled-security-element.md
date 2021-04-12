---
description: Especifica si el servicio de configuración automática de redes cableadas intentará la autenticación del puerto mediante 802.1 X.
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: Elemento OneXEnabled (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnabled
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c76fce3b42cff648d03f520ddeb569a39e99f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277729"
---
# <a name="onexenabled-security-element"></a><span data-ttu-id="d8720-103">Elemento OneXEnabled (Security)</span><span class="sxs-lookup"><span data-stu-id="d8720-103">OneXEnabled (security) Element</span></span>

<span data-ttu-id="d8720-104">El elemento **OneXEnabled** (Security) especifica si el servicio de configuración automática de redes cableadas intentará la autenticación del puerto mediante 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="d8720-104">The **OneXEnabled** (security) element specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <span data-ttu-id="d8720-105">Cuando **OneXEnabled** es false, el servicio de configuración automática nunca usa 802.1 x para la autenticación de puertos.</span><span class="sxs-lookup"><span data-stu-id="d8720-105">When **OneXEnabled** is FALSE, the automatic configuration service never uses 802.1X for port authentication.</span></span> <span data-ttu-id="d8720-106">Cuando **OneXEnabled** es true, el servicio de configuración automática intenta la autenticación del puerto mediante 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="d8720-106">When **OneXEnabled** is TRUE, then the automatic configuration service attempts port authentication using 802.1X.</span></span>

<span data-ttu-id="d8720-107">Este elemento es opcional.</span><span class="sxs-lookup"><span data-stu-id="d8720-107">This element is optional.</span></span> <span data-ttu-id="d8720-108">El valor predeterminado es TRUE.</span><span class="sxs-lookup"><span data-stu-id="d8720-108">The default value is TRUE.</span></span> <span data-ttu-id="d8720-109">Cuando **OneXEnabled** no se especifica en un perfil, se puede usar 802.1 x para la autenticación de puertos.</span><span class="sxs-lookup"><span data-stu-id="d8720-109">When **OneXEnabled** is not specified in a profile, then 802.1X may be used for port authentication.</span></span>

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

<span data-ttu-id="d8720-110">El elemento **OneXEnabled** se define mediante el elemento [**Security**](lan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d8720-110">The **OneXEnabled** element is defined by the [**security**](lan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8720-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8720-111">Requirements</span></span>



| <span data-ttu-id="d8720-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8720-112">Requirement</span></span> | <span data-ttu-id="d8720-113">Value</span><span class="sxs-lookup"><span data-stu-id="d8720-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d8720-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8720-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d8720-115">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d8720-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d8720-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d8720-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d8720-117">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="d8720-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8720-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="d8720-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="d8720-119">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="d8720-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d8720-120">**bursátil**</span><span class="sxs-lookup"><span data-stu-id="d8720-120">**security**</span></span>](lan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="d8720-121">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="d8720-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d8720-122">**seguridad (MSM)**</span><span class="sxs-lookup"><span data-stu-id="d8720-122">**security (MSM)**</span></span>](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




