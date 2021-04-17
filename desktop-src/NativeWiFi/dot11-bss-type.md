---
description: Define un tipo de red de Basic Service Set (BSS).
ms.assetid: 13d57339-655e-4978-974e-e7b12a83d18a
title: Enumeración DOT11_BSS_TYPE (Wlantypes. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSS_TYPE
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 7815e75f3ef7ef8d908b7d2b26f2e5f9d3630009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678016"
---
# <a name="dot11_bss_type-enumeration"></a><span data-ttu-id="ba4f7-103">\_Enumeración de tipo BSS de DOT11 \_</span><span class="sxs-lookup"><span data-stu-id="ba4f7-103">DOT11\_BSS\_TYPE enumeration</span></span>

<span data-ttu-id="ba4f7-104">El tipo enumerado de BSS de DOT11 define un tipo de red de conjunto de servicio básico (BSS). **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="ba4f7-104">The **DOT11\_BSS\_TYPE** enumerated type defines a basic service set (BSS) network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba4f7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ba4f7-105">Syntax</span></span>


```C++
typedef enum _DOT11_BSS_TYPE { 
  dot11_BSS_type_infrastructure  = 1,
  dot11_BSS_type_independent     = 2,
  dot11_BSS_type_any             = 3
} DOT11_BSS_TYPE, *PDOT11_BSS_TYPE;
```



## <a name="constants"></a><span data-ttu-id="ba4f7-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="ba4f7-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ba4f7-107"><span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**\_infraestructura de \_ tipo \_ BSS de dot11**</span><span class="sxs-lookup"><span data-stu-id="ba4f7-107"><span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**dot11\_BSS\_type\_infrastructure**</span></span>
</dt> <dd>

<span data-ttu-id="ba4f7-108">Especifica una red BSS de infraestructura.</span><span class="sxs-lookup"><span data-stu-id="ba4f7-108">Specifies an infrastructure BSS network.</span></span>

</dd> <dt>

<span data-ttu-id="ba4f7-109"><span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**\_independiente del \_ tipo \_ BSS de dot11**</span><span class="sxs-lookup"><span data-stu-id="ba4f7-109"><span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**dot11\_BSS\_type\_independent**</span></span>
</dt> <dd>

<span data-ttu-id="ba4f7-110">Especifica una red BSS independiente (IBSS).</span><span class="sxs-lookup"><span data-stu-id="ba4f7-110">Specifies an independent BSS (IBSS) network.</span></span>

</dd> <dt>

<span data-ttu-id="ba4f7-111"><span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**\_tipo BSS de dot11 \_ \_ any**</span><span class="sxs-lookup"><span data-stu-id="ba4f7-111"><span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**dot11\_BSS\_type\_any**</span></span>
</dt> <dd>

<span data-ttu-id="ba4f7-112">Especifica una red de infraestructura o IBSS.</span><span class="sxs-lookup"><span data-stu-id="ba4f7-112">Specifies either infrastructure or IBSS network.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba4f7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba4f7-113">Requirements</span></span>



| <span data-ttu-id="ba4f7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba4f7-114">Requirement</span></span> | <span data-ttu-id="ba4f7-115">Value</span><span class="sxs-lookup"><span data-stu-id="ba4f7-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba4f7-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba4f7-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ba4f7-117">Windows Vista, Windows XP con SP3 \[ solo aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="ba4f7-117">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ba4f7-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ba4f7-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ba4f7-119">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="ba4f7-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="ba4f7-120">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="ba4f7-120">Redistributable</span></span><br/>          | <span data-ttu-id="ba4f7-121">API de LAN inalámbrica para Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="ba4f7-121">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="ba4f7-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ba4f7-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba4f7-123"><dt>Wlantypes. h (incluye Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba4f7-123"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba4f7-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="ba4f7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba4f7-125">**\_entrada de BSS de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="ba4f7-125">**WLAN\_BSS\_ENTRY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> <dt>

[<span data-ttu-id="ba4f7-126">**\_parámetros de conexión de WLAN \_**</span><span class="sxs-lookup"><span data-stu-id="ba4f7-126">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[<span data-ttu-id="ba4f7-127">**WlanGetNetworkBssList**</span><span class="sxs-lookup"><span data-stu-id="ba4f7-127">**WlanGetNetworkBssList**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> </dl>

 

 




