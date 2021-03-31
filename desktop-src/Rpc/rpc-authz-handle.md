---
title: RPC_AUTHZ_HANDLE (Rpcdce. h)
description: El tipo de datos de identificador de RPC \_ AUTHZ \_ declara un identificador de autorización. Este identificador apunta a la información de privilegios de la aplicación cliente que realizó la llamada a procedimiento remoto.
ms.assetid: 35b6a3f4-1703-4244-98fd-fad7de48b262
keywords:
- RPC_AUTHZ_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b095100e1e224590ef6a285785da632e198e1b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151187"
---
# <a name="rpc_authz_handle"></a><span data-ttu-id="fd70d-105">identificador de RPC \_ AUTHZ \_</span><span class="sxs-lookup"><span data-stu-id="fd70d-105">RPC\_AUTHZ\_HANDLE</span></span>

<span data-ttu-id="fd70d-106">El tipo de datos de **\_ \_ identificador de RPC AUTHZ** declara un identificador de autorización.</span><span class="sxs-lookup"><span data-stu-id="fd70d-106">The **RPC\_AUTHZ\_HANDLE** data type declares an authorization handle.</span></span> <span data-ttu-id="fd70d-107">Este identificador apunta a la información de privilegios de la aplicación cliente que realizó la llamada a procedimiento remoto.</span><span class="sxs-lookup"><span data-stu-id="fd70d-107">This handle points to the privileges information for the client application that made the remote procedure call.</span></span>


```C++
typedef void* RPC_AUTHZ_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="fd70d-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd70d-108">Requirements</span></span>



| <span data-ttu-id="fd70d-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="fd70d-109">Requirement</span></span> | <span data-ttu-id="fd70d-110">Value</span><span class="sxs-lookup"><span data-stu-id="fd70d-110">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd70d-111">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd70d-111">Minimum supported client</span></span><br/> | <span data-ttu-id="fd70d-112">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="fd70d-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fd70d-113">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fd70d-113">Minimum supported server</span></span><br/> | <span data-ttu-id="fd70d-114">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="fd70d-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="fd70d-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fd70d-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="fd70d-116"><dt>Rpcdce. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fd70d-116"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd70d-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="fd70d-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd70d-118">**RpcBindingInqAuthClient**</span><span class="sxs-lookup"><span data-stu-id="fd70d-118">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> </dl>

 

 





