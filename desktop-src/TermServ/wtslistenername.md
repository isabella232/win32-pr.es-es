---
title: WTSLISTENERNAME (WtsApi32. h)
description: Representa el nombre de una Servicios de Escritorio remoto agentes de escucha en un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).
ms.assetid: 3C41F507-6A67-4244-860F-E89B0F9E33B0
ms.tgt_platform: multiple
keywords:
- WTSLISTENERNAMEW
- WTSLISTENERNAMEA
- WTSLISTENERNAME
- PWTSLISTENERNAME
- WTSLISTENERNAME
- PWTSLISTENERNAME
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82576fc9f4490b133916852441c50dcf77e849d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422460"
---
# <a name="wtslistenername"></a><span data-ttu-id="a5945-109">WTSLISTENERNAME</span><span class="sxs-lookup"><span data-stu-id="a5945-109">WTSLISTENERNAME</span></span>

<span data-ttu-id="a5945-110">Representa el nombre de una Servicios de Escritorio remoto agentes de escucha en un servidor host de sesión de Escritorio remoto (host de sesión de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="a5945-110">Represents the name of a Remote Desktop Services listeners on a Remote Desktop Session Host (RD Session Host) server.</span></span>


```C++
typedef WCHAR WTSLISTENERNAMEW[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEW;
typedef CHAR WTSLISTENERNAMEA[WTS_LISTENER_NAME_LENGTH + 1 ], *PWTSLISTENERNAMEA;
#if UNICODE
typedef WTSLISTENERNAMEW WTSLISTENERNAME;
typedef PWTSLISTENERNAMEW PWTSLISTENERNAME;
#else 
typedef WTSLISTENERNAMEA WTSLISTENERNAME;
typedef PWTSLISTENERNAMEA PWTSLISTENERNAME;
#endif 
```



<dl> <dt>

<span data-ttu-id="a5945-111">**WTSLISTENERNAMEW**</span><span class="sxs-lookup"><span data-stu-id="a5945-111">**WTSLISTENERNAMEW**</span></span>
</dt> <dd>

<span data-ttu-id="a5945-112">Nombre Unicode del agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="a5945-112">The Unicode name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="a5945-113">**WTSLISTENERNAMEA**</span><span class="sxs-lookup"><span data-stu-id="a5945-113">**WTSLISTENERNAMEA**</span></span>
</dt> <dd>

<span data-ttu-id="a5945-114">Puntero al nombre ANSI del agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="a5945-114">A pointer to the ANSI name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="a5945-115">**WTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="a5945-115">**WTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="a5945-116">Nombre del agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="a5945-116">The name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="a5945-117">**PWTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="a5945-117">**PWTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="a5945-118">Puntero al nombre del agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="a5945-118">A pointer to the name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="a5945-119">**WTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="a5945-119">**WTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="a5945-120">Nombre del agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="a5945-120">The name of the listener.</span></span>

</dd> <dt>

<span data-ttu-id="a5945-121">**PWTSLISTENERNAME**</span><span class="sxs-lookup"><span data-stu-id="a5945-121">**PWTSLISTENERNAME**</span></span>
</dt> <dd>

<span data-ttu-id="a5945-122">Puntero al nombre del agente de escucha.</span><span class="sxs-lookup"><span data-stu-id="a5945-122">A pointer to the name of the listener.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a5945-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a5945-123">Requirements</span></span>



| <span data-ttu-id="a5945-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5945-124">Requirement</span></span> | <span data-ttu-id="a5945-125">Value</span><span class="sxs-lookup"><span data-stu-id="a5945-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5945-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5945-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a5945-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5945-127">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="a5945-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a5945-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a5945-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5945-129">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="a5945-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a5945-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5945-131"><dt>WtsApi32. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5945-131"><dt>WtsApi32.h</dt></span></span> </dl> |



 

 





