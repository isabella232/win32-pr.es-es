---
title: RPC_NS_HANDLE (Rpcnsi. h)
description: El tipo de datos \_ \_ identificador de RPC NS define un identificador de servicio de nombres.
ms.assetid: d9c2a376-4972-4f16-aa8d-f0e43d5ddb8d
keywords:
- RPC_NS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e72ee694e08be1b30a75dc1f5b986619043d592
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535104"
---
# <a name="rpc_ns_handle"></a><span data-ttu-id="ab5ae-104">identificador de RPC \_ NS \_</span><span class="sxs-lookup"><span data-stu-id="ab5ae-104">RPC\_NS\_HANDLE</span></span>

<span data-ttu-id="ab5ae-105">El tipo de **datos \_ \_ identificador de RPC NS** define un identificador de servicio de nombres.</span><span class="sxs-lookup"><span data-stu-id="ab5ae-105">The data type **RPC\_NS\_HANDLE** defines a name-service handle.</span></span>


```C++
typedef void* RPC_NS_HANDLE;
```



## <a name="remarks"></a><span data-ttu-id="ab5ae-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab5ae-106">Remarks</span></span>

<span data-ttu-id="ab5ae-107">Un identificador de servicio de nombre es una variable opaca que contiene información que la biblioteca en tiempo de ejecución de RPC utiliza para devolver los siguientes datos de RPC desde la base de datos de nombre-servicio:</span><span class="sxs-lookup"><span data-stu-id="ab5ae-107">A name-service handle is an opaque variable containing information the RPC run-time library uses to return the following RPC data from the name-service database:</span></span>

-   <span data-ttu-id="ab5ae-108">Identificadores de enlace de servidor</span><span class="sxs-lookup"><span data-stu-id="ab5ae-108">Server-binding handles</span></span>
-   <span data-ttu-id="ab5ae-109">UUID de recursos ofrecidos por los miembros del perfil de servidor</span><span class="sxs-lookup"><span data-stu-id="ab5ae-109">UUIDs of resources offered by server profile members</span></span>
-   <span data-ttu-id="ab5ae-110">Miembros del grupo</span><span class="sxs-lookup"><span data-stu-id="ab5ae-110">Group members</span></span>

<span data-ttu-id="ab5ae-111">El ámbito de un identificador de servicio de nombre es de una rutina "begin" a través de la rutina "Done" correspondiente.</span><span class="sxs-lookup"><span data-stu-id="ab5ae-111">The scope of a name-service handle is from a "Begin" routine through the corresponding "Done" routine.</span></span>

<span data-ttu-id="ab5ae-112">Las aplicaciones son responsables del control de simultaneidad de los identificadores de servicio de nombre entre subprocesos.</span><span class="sxs-lookup"><span data-stu-id="ab5ae-112">Applications are responsible for concurrency control of name-service handles across threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab5ae-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab5ae-113">Requirements</span></span>



| <span data-ttu-id="ab5ae-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab5ae-114">Requirement</span></span> | <span data-ttu-id="ab5ae-115">Value</span><span class="sxs-lookup"><span data-stu-id="ab5ae-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab5ae-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab5ae-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ab5ae-117">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ab5ae-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="ab5ae-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab5ae-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ab5ae-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ab5ae-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ab5ae-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab5ae-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab5ae-121"><dt>Rpcnsi. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab5ae-121"><dt>Rpcnsi.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab5ae-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab5ae-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab5ae-123">**RpcNsBindingImportBegin**</span><span class="sxs-lookup"><span data-stu-id="ab5ae-123">**RpcNsBindingImportBegin**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina)
</dt> <dt>

[<span data-ttu-id="ab5ae-124">**RpcNsBindingImportDone**</span><span class="sxs-lookup"><span data-stu-id="ab5ae-124">**RpcNsBindingImportDone**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone)
</dt> <dt>

[<span data-ttu-id="ab5ae-125">**RpcNsBindingImportNext**</span><span class="sxs-lookup"><span data-stu-id="ab5ae-125">**RpcNsBindingImportNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext)
</dt> <dt>

[<span data-ttu-id="ab5ae-126">**RpcNsBindingLookupBegin**</span><span class="sxs-lookup"><span data-stu-id="ab5ae-126">**RpcNsBindingLookupBegin**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupbegina)
</dt> <dt>

[<span data-ttu-id="ab5ae-127">**RpcNsBindingLookupDone**</span><span class="sxs-lookup"><span data-stu-id="ab5ae-127">**RpcNsBindingLookupDone**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupdone)
</dt> <dt>

[<span data-ttu-id="ab5ae-128">**RpcNsBindingLookupNext**</span><span class="sxs-lookup"><span data-stu-id="ab5ae-128">**RpcNsBindingLookupNext**</span></span>](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindinglookupnext)
</dt> </dl>

 

 





