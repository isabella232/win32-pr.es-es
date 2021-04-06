---
description: Especifica el origen de la configuración de seguridad de 802.1 X usada por un componente de seguridad IHV.
ms.assetid: 9c216319-d962-4c68-89a3-116eff3f4376
title: Elemento useMSOneX (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- useMSOneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: aa9f2092ac0e76feae89b02f333ae3098288ccef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002188"
---
# <a name="usemsonex-ihv-element"></a><span data-ttu-id="3c1fa-103">Elemento useMSOneX (IHV)</span><span class="sxs-lookup"><span data-stu-id="3c1fa-103">useMSOneX (IHV) Element</span></span>

<span data-ttu-id="3c1fa-104">El elemento **useMSOneX** (IHV) especifica el origen de la configuración de seguridad de 802.1 x usada por un componente de seguridad IHV.</span><span class="sxs-lookup"><span data-stu-id="3c1fa-104">The **useMSOneX** (IHV) element specifies the origin of 802.1X security settings used by an IHV security component.</span></span>

<span data-ttu-id="3c1fa-105">Cuando **useMSOneX** es true, los componentes de seguridad de IHV usan la configuración de 802.1 x definida por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3c1fa-105">When **useMSOneX** is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="3c1fa-106">Cuando **useMSOneX** es false, los componentes de seguridad de IHV usan la configuración de 802.1 x suministrada por el proveedor.</span><span class="sxs-lookup"><span data-stu-id="3c1fa-106">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span>

<span data-ttu-id="3c1fa-107">**Windows XP con SP3 y API de LAN inalámbrica para Windows XP con SP2:** Este elemento no se admite.</span><span class="sxs-lookup"><span data-stu-id="3c1fa-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="useMSOneX"
    type="boolean"
    minOccurs="0"
 />
```

<span data-ttu-id="3c1fa-108">El elemento está definido por el elemento [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3c1fa-108">The element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c1fa-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3c1fa-109">Requirements</span></span>



| <span data-ttu-id="3c1fa-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c1fa-110">Requirement</span></span> | <span data-ttu-id="3c1fa-111">Value</span><span class="sxs-lookup"><span data-stu-id="3c1fa-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3c1fa-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c1fa-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3c1fa-113">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3c1fa-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3c1fa-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3c1fa-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3c1fa-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="3c1fa-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3c1fa-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="3c1fa-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="3c1fa-117">**Contexto de definición del elemento en el esquema**</span><span class="sxs-lookup"><span data-stu-id="3c1fa-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3c1fa-118">**IHV**</span><span class="sxs-lookup"><span data-stu-id="3c1fa-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="3c1fa-119">**Posible elemento primario inmediato en la instancia de esquema**</span><span class="sxs-lookup"><span data-stu-id="3c1fa-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3c1fa-120">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="3c1fa-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




