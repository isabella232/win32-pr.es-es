---
description: Se usan para definir una dirección IEEE Media Access Control (MAC).
ms.assetid: c1335127-a2d2-4f44-a895-1abbc5eaf98d
title: DOT11_MAC_ADDRESS (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77b43635462c4b48890599512cc1a413461de72e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910658"
---
# <a name="dot11_mac_address"></a><span data-ttu-id="be6ec-103">\_Dirección Mac de DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="be6ec-103">DOT11\_MAC\_ADDRESS</span></span>

<span data-ttu-id="be6ec-104">Los tipos de **\_ \_ dirección Mac de DOT11** se usan para definir una dirección de Media Access Control IEEE (Mac).</span><span class="sxs-lookup"><span data-stu-id="be6ec-104">The **DOT11\_MAC\_ADDRESS** types are used to define an IEEE media access control (MAC) address.</span></span>


```C++
typedef UCHAR DOT11_MAC_ADDRESS[6];
typedef DOT11_MAC_ADDRESS* PDOT11_MAC_ADDRESS;
```



<dl> <dt>

<span data-ttu-id="be6ec-105">**\_Dirección Mac de DOT11 \_ \[ 6\]**</span><span class="sxs-lookup"><span data-stu-id="be6ec-105">**DOT11\_MAC\_ADDRESS\[6\]**</span></span>
</dt> <dd>

<span data-ttu-id="be6ec-106">Una dirección MAC en formato de unidifusión, multidifusión o difusión.</span><span class="sxs-lookup"><span data-stu-id="be6ec-106">A MAC address in unicast, multicast, or broadcast format.</span></span>

</dd> <dt>

<span data-ttu-id="be6ec-107">**\_Dirección Mac \_ PDOT11**</span><span class="sxs-lookup"><span data-stu-id="be6ec-107">**PDOT11\_MAC\_ADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="be6ec-108">Puntero a una dirección MAC en formato de unidifusión, multidifusión o difusión.</span><span class="sxs-lookup"><span data-stu-id="be6ec-108">Pointer to a MAC address in unicast, multicast, or broadcast format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="be6ec-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="be6ec-109">Requirements</span></span>



| <span data-ttu-id="be6ec-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="be6ec-110">Requirement</span></span> | <span data-ttu-id="be6ec-111">Value</span><span class="sxs-lookup"><span data-stu-id="be6ec-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be6ec-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be6ec-112">Minimum supported client</span></span><br/> | <span data-ttu-id="be6ec-113">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="be6ec-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="be6ec-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="be6ec-114">Minimum supported server</span></span><br/> | <span data-ttu-id="be6ec-115">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="be6ec-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="be6ec-116">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="be6ec-116">Redistributable</span></span><br/>          | <span data-ttu-id="be6ec-117">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="be6ec-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="be6ec-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="be6ec-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="be6ec-119"><dt>Windot11. h (incluye Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be6ec-119"><dt>Windot11.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be6ec-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="be6ec-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be6ec-121">**\_Lista de BSSID de DOT11 \_**</span><span class="sxs-lookup"><span data-stu-id="be6ec-121">**DOT11\_BSSID\_LIST**</span></span>](dot11-bssid-list.md)
</dt> <dt>

[<span data-ttu-id="be6ec-122">**atributos de la Asociación de WLAN \_ \_**</span><span class="sxs-lookup"><span data-stu-id="be6ec-122">**WLAN\_ASSOCIATION\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[<span data-ttu-id="be6ec-123">**\_entrada de BSS de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="be6ec-123">**WLAN\_BSS\_ENTRY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> </dl>

 

 




