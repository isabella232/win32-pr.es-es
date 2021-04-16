---
title: Constantes de tiempo de espera de enlace (Rpcdce. h)
description: La biblioteca RPC utiliza las constantes de tiempo de espera de enlace para especificar la cantidad relativa de tiempo que se debe gastar para establecer un enlace con el servidor antes de abandonarlo.
ms.assetid: bf5f3f08-ab29-4732-9ce3-d6d7ad699369
topic_type:
- apiref
api_name:
- RPC_C_BINDING_INFINITE_TIMEOUT
- RPC_C_BINDING_MIN_TIMEOUT
- RPC_C_BINDING_DEFAULT_TIMEOUT
- RPC_C_BINDING_MAX_TIMEOUT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d096fd320e1341f9affc35ae6ff1d355fcf12d41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676687"
---
# <a name="binding-time-out-constants"></a><span data-ttu-id="d11ee-103">Constantes de tiempo de espera de enlace</span><span class="sxs-lookup"><span data-stu-id="d11ee-103">Binding Time-out Constants</span></span>

<span data-ttu-id="d11ee-104">La biblioteca RPC utiliza las constantes de tiempo de espera de enlace para especificar la cantidad relativa de tiempo que se debe gastar para establecer un enlace con el servidor antes de abandonarlo.</span><span class="sxs-lookup"><span data-stu-id="d11ee-104">The RPC library uses the binding time-out constants to specify the relative amount of time that should be spent to establish a binding to the server before giving up.</span></span> <span data-ttu-id="d11ee-105">El tiempo de espera se puede habilitar con una llamada a la función [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) .</span><span class="sxs-lookup"><span data-stu-id="d11ee-105">The timeout can be enabled with a call to the [**RpcMgmtSetComTimeout**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetcomtimeout) function.</span></span> <span data-ttu-id="d11ee-106">La lista siguiente contiene los valores de tiempo de espera válidos.</span><span class="sxs-lookup"><span data-stu-id="d11ee-106">The following list contains the valid time-out values.</span></span>



| <span data-ttu-id="d11ee-107">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="d11ee-107">Constant/value</span></span>                                                                                                                                                                                                                                                                | <span data-ttu-id="d11ee-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="d11ee-108">Description</span></span>                                                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_BINDING_INFINITE_TIMEOUT"></span><span id="rpc_c_binding_infinite_timeout"></span><dl> <span data-ttu-id="d11ee-109"><dt>**RPC \_ \_Tiempo de \_ \_ espera infinito de enlace C**</dt> <dt> 10</dt></span><span class="sxs-lookup"><span data-stu-id="d11ee-109"><dt>**RPC\_C\_BINDING\_INFINITE\_TIMEOUT**</dt> <dt> 10 </dt></span></span> </dl> | <span data-ttu-id="d11ee-110">Sigue intentando establecer comunicaciones indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="d11ee-110">Keeps trying to establish communications forever.</span></span><br/>                                                                                                                                                             |
| <span id="RPC_C_BINDING_MIN_TIMEOUT"></span><span id="rpc_c_binding_min_timeout"></span><dl> <span data-ttu-id="d11ee-111"><dt>**RPC \_ \_Tiempo de \_ \_ espera mínimo de enlace C**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="d11ee-111"><dt>**RPC\_C\_BINDING\_MIN\_TIMEOUT**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="d11ee-112">Intenta la cantidad mínima de tiempo para el protocolo de red que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="d11ee-112">Tries the minimum amount of time for the network protocol being used.</span></span> <span data-ttu-id="d11ee-113">Este valor favorece el tiempo de respuesta con respecto a la corrección a la hora de determinar si el servidor se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="d11ee-113">This value favors response time over correctness in determining whether the server is running.</span></span><br/>                                          |
| <span id="RPC_C_BINDING_DEFAULT_TIMEOUT"></span><span id="rpc_c_binding_default_timeout"></span><dl> <span data-ttu-id="d11ee-114"><dt>**RPC \_ \_Tiempo de \_ \_ espera predeterminado de enlace de C**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="d11ee-114"><dt>**RPC\_C\_BINDING\_DEFAULT\_TIMEOUT**</dt> <dt>5</dt></span></span> </dl>       | <span data-ttu-id="d11ee-115">Intenta un promedio de tiempo para el protocolo de red que se utiliza.</span><span class="sxs-lookup"><span data-stu-id="d11ee-115">Tries an average amount of time for the network protocol being used.</span></span> <span data-ttu-id="d11ee-116">Este valor proporciona exactitud a la hora de determinar si un servidor se está ejecutando y proporciona un tiempo de respuesta igual.</span><span class="sxs-lookup"><span data-stu-id="d11ee-116">This value gives correctness in determining whether a server is running and gives response time equal weight.</span></span> <span data-ttu-id="d11ee-117">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="d11ee-117">This is the default value.</span></span><br/> |
| <span id="RPC_C_BINDING_MAX_TIMEOUT"></span><span id="rpc_c_binding_max_timeout"></span><dl> <span data-ttu-id="d11ee-118"><dt>**RPC \_ \_Tiempo de \_ \_ espera máximo de enlace de C**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="d11ee-118"><dt>**RPC\_C\_BINDING\_MAX\_TIMEOUT**</dt> <dt>9</dt></span></span> </dl>                   | <span data-ttu-id="d11ee-119">Intenta la cantidad más larga de tiempo para el protocolo de red que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="d11ee-119">Tries the longest amount of time for the network protocol being used.</span></span> <span data-ttu-id="d11ee-120">Este valor favorece la corrección a la hora de determinar si un servidor se está ejecutando a lo largo del tiempo de respuesta.</span><span class="sxs-lookup"><span data-stu-id="d11ee-120">This value favors correctness in determining whether a server is running over response time.</span></span><br/>                                            |



## <a name="remarks"></a><span data-ttu-id="d11ee-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d11ee-121">Remarks</span></span>

<span data-ttu-id="d11ee-122">Los valores de la tabla anterior no están en segundos.</span><span class="sxs-lookup"><span data-stu-id="d11ee-122">The values in the preceding table are not in seconds.</span></span> <span data-ttu-id="d11ee-123">Estos valores representan una cantidad de tiempo relativa en una escala de cero a 10.</span><span class="sxs-lookup"><span data-stu-id="d11ee-123">These values represent a relative amount of time on a scale of zero to 10.</span></span> <span data-ttu-id="d11ee-124">Para obtener más información acerca de cómo evitar los retrasos de la comunicación, consulte evitar bloqueos del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="d11ee-124">For more information on avoiding communication delays, refer to Preventing Client-side Hangs.</span></span>

## <a name="requirements"></a><span data-ttu-id="d11ee-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d11ee-125">Requirements</span></span>



| <span data-ttu-id="d11ee-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="d11ee-126">Requirement</span></span> | <span data-ttu-id="d11ee-127">Value</span><span class="sxs-lookup"><span data-stu-id="d11ee-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d11ee-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d11ee-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d11ee-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d11ee-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d11ee-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d11ee-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d11ee-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d11ee-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d11ee-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d11ee-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d11ee-133"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="d11ee-133"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





