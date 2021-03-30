---
description: La estructura de \_ direcciones IP de Vines \_ es una dirección IP en una red de Vines.
ms.assetid: 681753a5-08a2-48e6-9e46-c028c12ad9c1
title: Estructura de VINES_IP_ADDRESS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VINES_IP_ADDRESS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: c198c8c109d5aa5b841272173966ec7d9fd22299
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360858"
---
# <a name="vines_ip_address-structure"></a><span data-ttu-id="d3e16-103">Estructura de \_ direcciones IP de Vines \_</span><span class="sxs-lookup"><span data-stu-id="d3e16-103">VINES\_IP\_ADDRESS structure</span></span>

<span data-ttu-id="d3e16-104">La estructura de **\_ \_ direcciones IP de Vines** es una dirección IP en una red de Vines.</span><span class="sxs-lookup"><span data-stu-id="d3e16-104">The **VINES\_IP\_ADDRESS** structure is an IP address on a Vines network.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3e16-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3e16-105">Syntax</span></span>


```C++
typedef struct _VINES_IP_ADDRESS {
  DWORD NetID;
  WORD  SubnetID;
} VINES_IP_ADDRESS, *LPVINES_IP_ADDRESS;
```



## <a name="members"></a><span data-ttu-id="d3e16-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="d3e16-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d3e16-107">**NetId**</span><span class="sxs-lookup"><span data-stu-id="d3e16-107">**NetID**</span></span>
</dt> <dd>

<span data-ttu-id="d3e16-108">El identificador de un equipo específico en una subred específica.</span><span class="sxs-lookup"><span data-stu-id="d3e16-108">The identifier of a specific machine on a specific subnet.</span></span>

</dd> <dt>

<span data-ttu-id="d3e16-109">**SubnetID**</span><span class="sxs-lookup"><span data-stu-id="d3e16-109">**SubnetID**</span></span>
</dt> <dd>

<span data-ttu-id="d3e16-110">El identificador de una subred específica en toda la red.</span><span class="sxs-lookup"><span data-stu-id="d3e16-110">The identifier of a specific subnet on the whole network.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d3e16-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d3e16-111">Requirements</span></span>



| <span data-ttu-id="d3e16-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="d3e16-112">Requirement</span></span> | <span data-ttu-id="d3e16-113">Value</span><span class="sxs-lookup"><span data-stu-id="d3e16-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d3e16-114">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3e16-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d3e16-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d3e16-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d3e16-116">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d3e16-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d3e16-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d3e16-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d3e16-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d3e16-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3e16-119"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d3e16-119"><dt>Netmon.h</dt></span></span> </dl> |



 

 




