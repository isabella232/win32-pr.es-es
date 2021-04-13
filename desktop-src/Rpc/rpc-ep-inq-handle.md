---
title: RPC_EP_INQ_HANDLE (Rpcasync. h)
description: El \_ \_ \_ tipo de datos de identificador de INQ de RPC EP declara un identificador para un contexto de consulta. Las aplicaciones RPC lo usan para ver la información de dirección del servidor almacenada en la asignación de extremo.
ms.assetid: e18ce800-0110-4450-9a1b-a3f777d00f2d
keywords:
- RPC_EP_INQ_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c34c64b5601b31485808924fc57dbe3412b6009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422551"
---
# <a name="rpc_ep_inq_handle"></a><span data-ttu-id="f59cd-105">\_ \_ controlador INQ de RPC EP \_</span><span class="sxs-lookup"><span data-stu-id="f59cd-105">RPC\_EP\_INQ\_HANDLE</span></span>

<span data-ttu-id="f59cd-106">El tipo de datos de **\_ identificador de \_ INQ \_ de RPC EP** declara un identificador para un contexto de consulta.</span><span class="sxs-lookup"><span data-stu-id="f59cd-106">The **RPC\_EP\_INQ\_HANDLE** data type declares a handle for an inquiry context.</span></span> <span data-ttu-id="f59cd-107">Las aplicaciones RPC lo usan para ver la información de dirección del servidor almacenada en la asignación de extremo.</span><span class="sxs-lookup"><span data-stu-id="f59cd-107">RPC applications use it to view server address information stored in the endpoint map.</span></span>


```C++
typedef I_RPC_HANDLE* RPC_EP_INQ_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="f59cd-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f59cd-108">Requirements</span></span>



| <span data-ttu-id="f59cd-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="f59cd-109">Requirement</span></span> | <span data-ttu-id="f59cd-110">Value</span><span class="sxs-lookup"><span data-stu-id="f59cd-110">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f59cd-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f59cd-111">Minimum supported client</span></span><br/> | <span data-ttu-id="f59cd-112">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f59cd-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f59cd-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f59cd-113">Minimum supported server</span></span><br/> | <span data-ttu-id="f59cd-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f59cd-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="f59cd-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f59cd-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="f59cd-116"><dt>Rpcasync. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f59cd-116"><dt>Rpcasync.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f59cd-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="f59cd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f59cd-118">**RpcMgmtEpEltInqBegin**</span><span class="sxs-lookup"><span data-stu-id="f59cd-118">**RpcMgmtEpEltInqBegin**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqbegin)
</dt> <dt>

[<span data-ttu-id="f59cd-119">**RpcMgmtEpEltInqNext**</span><span class="sxs-lookup"><span data-stu-id="f59cd-119">**RpcMgmtEpEltInqNext**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqnext)
</dt> <dt>

[<span data-ttu-id="f59cd-120">**RpcMgmtEpEltInqDone**</span><span class="sxs-lookup"><span data-stu-id="f59cd-120">**RpcMgmtEpEltInqDone**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtepeltinqdone)
</dt> </dl>

 

 





