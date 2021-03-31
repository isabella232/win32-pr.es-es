---
title: RPC_AUTH_IDENTITY_HANDLE (Rpcdce. h)
description: El \_ tipo de datos de identificador de identidad de autenticación RPC \_ \_ declara un identificador que apunta a una estructura que contiene las credenciales de autenticación y autorización del cliente especificadas para llamadas a procedimientos remotos.
ms.assetid: 06e45348-a392-45be-9f8a-e77ef887f26c
keywords:
- RPC_AUTH_IDENTITY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86559e7852172d34898d48f13bb2975ed792d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151188"
---
# <a name="rpc_auth_identity_handle"></a><span data-ttu-id="314be-104">\_identificador de \_ identidad de autenticación RPC \_</span><span class="sxs-lookup"><span data-stu-id="314be-104">RPC\_AUTH\_IDENTITY\_HANDLE</span></span>

<span data-ttu-id="314be-105">El tipo de datos de **\_ identificador de \_ identidad \_ de autenticación RPC** declara un identificador que apunta a una estructura que contiene las credenciales de autenticación y autorización del cliente especificadas para llamadas a procedimientos remotos.</span><span class="sxs-lookup"><span data-stu-id="314be-105">The **RPC\_AUTH\_IDENTITY\_HANDLE** data type declares a handle that points to a structure containing the client's authentication and authorization credentials specified for remote procedure calls.</span></span>


```C++
typedef void* RPC_AUTH_IDENTITY_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="314be-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="314be-106">Requirements</span></span>



| <span data-ttu-id="314be-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="314be-107">Requirement</span></span> | <span data-ttu-id="314be-108">Value</span><span class="sxs-lookup"><span data-stu-id="314be-108">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="314be-109">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="314be-109">Minimum supported client</span></span><br/> | <span data-ttu-id="314be-110">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="314be-110">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="314be-111">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="314be-111">Minimum supported server</span></span><br/> | <span data-ttu-id="314be-112">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="314be-112">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="314be-113">Encabezado</span><span class="sxs-lookup"><span data-stu-id="314be-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="314be-114"><dt>Rpcdce. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="314be-114"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="314be-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="314be-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="314be-116">**RpcBindingInqAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="314be-116">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="314be-117">**RpcBindingSetAuthInfo**</span><span class="sxs-lookup"><span data-stu-id="314be-117">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> </dl>

 

 





