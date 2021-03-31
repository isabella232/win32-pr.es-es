---
title: Enumeración CB_ADDRESS_TYPE (Cbclient. h)
description: Especifica el tipo de dirección.
ms.assetid: 1F6ECFA6-8876-4C9B-A883-BD630D54B8E2
ms.tgt_platform: multiple
keywords:
- CB_ADDRESS_TYPE enumeración Servicios de Escritorio remoto
topic_type:
- apiref
api_name:
- CB_ADDRESS_TYPE
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ecf17cea6ffc19743868b266236738839f9f917
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801591"
---
# <a name="cb_address_type-enumeration"></a><span data-ttu-id="42536-104">\_Enumeración de tipo de dirección CB \_</span><span class="sxs-lookup"><span data-stu-id="42536-104">CB\_ADDRESS\_TYPE enumeration</span></span>

<span data-ttu-id="42536-105">Especifica el tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="42536-105">Specifies the address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="42536-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42536-106">Syntax</span></span>


```C++
typedef enum _CB_ADDRESS_TYPE { 
  CB_ADDR_UNDEFINED  = 0,
  CB_ADDR_IPv4       = 4,
  CB_ADDR_IPv6       = 6
} CB_ADDRESS_TYPE;
```



## <a name="constants"></a><span data-ttu-id="42536-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="42536-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="42536-108"><span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**Dirección CB no \_ \_ definida**</span><span class="sxs-lookup"><span data-stu-id="42536-108"><span id="CB_ADDR_UNDEFINED"></span><span id="cb_addr_undefined"></span>**CB\_ADDR\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="42536-109">El tipo de dirección es indefinido.</span><span class="sxs-lookup"><span data-stu-id="42536-109">The address type is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="42536-110"><span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**CB \_ dir \_ IPv4**</span><span class="sxs-lookup"><span data-stu-id="42536-110"><span id="CB_ADDR_IPv4"></span><span id="cb_addr_ipv4"></span><span id="CB_ADDR_IPV4"></span>**CB\_ADDR\_IPv4**</span></span>
</dt> <dd>

<span data-ttu-id="42536-111">La dirección es una dirección IPv4.</span><span class="sxs-lookup"><span data-stu-id="42536-111">The address is an IPv4 address.</span></span>

</dd> <dt>

<span data-ttu-id="42536-112"><span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**CB \_ dir \_ IPv6**</span><span class="sxs-lookup"><span data-stu-id="42536-112"><span id="CB_ADDR_IPv6"></span><span id="cb_addr_ipv6"></span><span id="CB_ADDR_IPV6"></span>**CB\_ADDR\_IPv6**</span></span>
</dt> <dd>

<span data-ttu-id="42536-113">La dirección es una dirección IPv6.</span><span class="sxs-lookup"><span data-stu-id="42536-113">The address is an IPv6 address.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="42536-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42536-114">Requirements</span></span>



| <span data-ttu-id="42536-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="42536-115">Requirement</span></span> | <span data-ttu-id="42536-116">Value</span><span class="sxs-lookup"><span data-stu-id="42536-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42536-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42536-117">Minimum supported client</span></span><br/> | <span data-ttu-id="42536-118">Windows 8</span><span class="sxs-lookup"><span data-stu-id="42536-118">Windows 8</span></span><br/>                                                                  |
| <span data-ttu-id="42536-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="42536-119">Minimum supported server</span></span><br/> | <span data-ttu-id="42536-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="42536-120">Windows Server 2012</span></span><br/>                                                        |
| <span data-ttu-id="42536-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="42536-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="42536-122"><dt>Cbclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="42536-122"><dt>Cbclient.h</dt></span></span> </dl> |



 

 





