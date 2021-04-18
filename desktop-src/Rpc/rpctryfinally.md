---
title: RpcTryFinally (RPC. h)
description: La instrucción RpcTryFinally proporciona un control de terminación estructurado.
ms.assetid: e9ed748a-db15-4c91-b8a4-b510f99042d8
keywords:
- RPC RpcTryFinally
topic_type:
- apiref
api_name:
- RpcTryFinally
api_location:
- Rpc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 909d65013fb3fb83ffb926fea6a6b3f30980a3b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491398"
---
# <a name="rpctryfinally"></a><span data-ttu-id="e748f-104">RpcTryFinally</span><span class="sxs-lookup"><span data-stu-id="e748f-104">RpcTryFinally</span></span>

<span data-ttu-id="e748f-105">La instrucción **RpcTryFinally** proporciona un control de terminación estructurado.</span><span class="sxs-lookup"><span data-stu-id="e748f-105">The **RpcTryFinally** statement provides structured termination handling.</span></span> <span data-ttu-id="e748f-106">Se produce una excepción durante las instrucciones de ejecución del bloque de código asociado a la instrucción **RpcTryFinally** , se ejecutan las instrucciones del bloque de código asociado a la instrucción [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) .</span><span class="sxs-lookup"><span data-stu-id="e748f-106">It an exception occurs during the execution statements of the code block associated with the **RpcTryFinally** statement, the statements in the code block associated with the [**RpcFinally**](/previous-versions/aa375699(v=vs.80)) statement are executed.</span></span> <span data-ttu-id="e748f-107">Todas las instrucciones **RpcTryFinally** deben terminar con una instrucción [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) .</span><span class="sxs-lookup"><span data-stu-id="e748f-107">All **RpcTryFinally** statements must be terminated by an [**RpcEndFinally**](/previous-versions/aa375634(v=vs.80)) statement.</span></span>

<span data-ttu-id="e748f-108">Para obtener más información, vea [**RpcFinally**](/previous-versions/aa375699(v=vs.80)).</span><span class="sxs-lookup"><span data-stu-id="e748f-108">For more information, see [**RpcFinally**](/previous-versions/aa375699(v=vs.80)).</span></span>

## <a name="requirements"></a><span data-ttu-id="e748f-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e748f-109">Requirements</span></span>



| <span data-ttu-id="e748f-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="e748f-110">Requirement</span></span> | <span data-ttu-id="e748f-111">Value</span><span class="sxs-lookup"><span data-stu-id="e748f-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e748f-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e748f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="e748f-113">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e748f-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e748f-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e748f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="e748f-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e748f-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e748f-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e748f-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="e748f-117"><dt>RPC. h</dt></span><span class="sxs-lookup"><span data-stu-id="e748f-117"><dt>Rpc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e748f-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="e748f-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="e748f-119">[**RpcFinally**](/previous-versions/aa375699(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="e748f-119">[**RpcFinally**](/previous-versions/aa375699(v=vs.80))</span></span>
</dt> <dt>

<span data-ttu-id="e748f-120">[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))</span><span class="sxs-lookup"><span data-stu-id="e748f-120">[**RpcEndFinally**](/previous-versions/aa375634(v=vs.80))</span></span>
</dt> </dl>

 

