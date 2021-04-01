---
title: RpcTryExcept (RPC. h)
description: La instrucción RpcTryExcept proporciona control de excepciones estructurado para las aplicaciones RPC.
ms.assetid: 3addb367-4bdc-4c11-bf4d-b5b94da45b26
keywords:
- RPC RpcTryExcept
topic_type:
- apiref
api_name:
- RpcTryExcept
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5876a3fe0b33f96a5e10a9c712bdcadcbfca10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150518"
---
# <a name="rpctryexcept"></a><span data-ttu-id="5d2ca-104">RpcTryExcept</span><span class="sxs-lookup"><span data-stu-id="5d2ca-104">RpcTryExcept</span></span>

<span data-ttu-id="5d2ca-105">La instrucción **RpcTryExcept** proporciona control de excepciones estructurado para las aplicaciones RPC.</span><span class="sxs-lookup"><span data-stu-id="5d2ca-105">The **RpcTryExcept** statement provides structured exception handling for RPC applications.</span></span> <span data-ttu-id="5d2ca-106">Si alguna de las instrucciones de programa de **RpcTryExcept** produce una excepción, se ejecutan las instrucciones del bloque de código [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) .</span><span class="sxs-lookup"><span data-stu-id="5d2ca-106">If any of the program statements in the **RpcTryExcept** cause an exception, the statements in the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) code block are executed.</span></span> <span data-ttu-id="5d2ca-107">Todas las instrucciones **RpcTryExcept** deben terminarse con la instrucción [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) .</span><span class="sxs-lookup"><span data-stu-id="5d2ca-107">All **RpcTryExcept** statements must be terminated by the [**RpcEndExcept**](/previous-versions/aa375629(v=vs.80)) statement.</span></span>

<span data-ttu-id="5d2ca-108">Para obtener más información, vea [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span><span class="sxs-lookup"><span data-stu-id="5d2ca-108">For more information, see [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span></span>

<span data-ttu-id="5d2ca-109">**Windows Vista y versiones posteriores de Windows:**  [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) se recomienda para el control estructurado de excepciones para las excepciones más comunes como alternativa a los filtros personalizados con [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span><span class="sxs-lookup"><span data-stu-id="5d2ca-109">**Windows Vista and later versions of Windows:**  [**RpcExceptionFilter**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter) is recommended for structured exception handling for the most common exceptions as an alternative to custom filters with [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept).</span></span>

## <a name="requirements"></a><span data-ttu-id="5d2ca-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5d2ca-110">Requirements</span></span>



| <span data-ttu-id="5d2ca-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="5d2ca-111">Requirement</span></span> | <span data-ttu-id="5d2ca-112">Value</span><span class="sxs-lookup"><span data-stu-id="5d2ca-112">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="5d2ca-113">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d2ca-113">Minimum supported client</span></span><br/> | <span data-ttu-id="5d2ca-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5d2ca-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="5d2ca-115">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5d2ca-115">Minimum supported server</span></span><br/> | <span data-ttu-id="5d2ca-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5d2ca-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="5d2ca-117">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5d2ca-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d2ca-118"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d2ca-118"><dt>Rpc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5d2ca-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="5d2ca-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d2ca-120">**RpcExcept**</span><span class="sxs-lookup"><span data-stu-id="5d2ca-120">**RpcExcept**</span></span>](/windows/desktop/api/Rpc/nf-rpc-rpcexcept)
</dt> <dt>

[<span data-ttu-id="5d2ca-121">**RpcExceptionFilter**</span><span class="sxs-lookup"><span data-stu-id="5d2ca-121">**RpcExceptionFilter**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcexceptionfilter)
</dt> <dt>

[<span data-ttu-id="5d2ca-122">**RpcTryFinally**</span><span class="sxs-lookup"><span data-stu-id="5d2ca-122">**RpcTryFinally**</span></span>](rpctryfinally.md)
</dt> </dl>

 

