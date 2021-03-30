---
title: RPC_STATUS (Rpcdce. h)
description: El tipo de datos \_ Estado de RPC representa un tipo de código de estado específico de la plataforma.
ms.assetid: 0f929916-f3aa-477f-9c61-742f3fbbab29
keywords:
- RPC_STATUS
- RPC_STATUS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066022ce33676caadcf25a6814f3b4974701998e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079338"
---
# <a name="rpc_status"></a><span data-ttu-id="00664-105">Estado de RPC \_</span><span class="sxs-lookup"><span data-stu-id="00664-105">RPC\_STATUS</span></span>

<span data-ttu-id="00664-106">El tipo de **datos \_ Estado de RPC** representa un tipo de código de estado específico de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="00664-106">The data type **RPC\_STATUS** represents a platform-specific status code type.</span></span>


```C++
typedef long RPC_STATUS;
typedef unsigned short RPC_STATUS;
```



## <a name="remarks"></a><span data-ttu-id="00664-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00664-107">Remarks</span></span>

<span data-ttu-id="00664-108">La mayoría de las funciones RPC devuelven el tipo de **\_ Estado de RPC** y forma parte de la definición de tipo de función [**\_ \_ INQ \_ FN del objeto RPC**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) .</span><span class="sxs-lookup"><span data-stu-id="00664-108">The **RPC\_STATUS** type is returned by most RPC functions and is part of the [**RPC\_OBJECT\_INQ\_FN**](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn) function type definition.</span></span>

## <a name="requirements"></a><span data-ttu-id="00664-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00664-109">Requirements</span></span>



| <span data-ttu-id="00664-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="00664-110">Requirement</span></span> | <span data-ttu-id="00664-111">Value</span><span class="sxs-lookup"><span data-stu-id="00664-111">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="00664-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00664-112">Minimum supported client</span></span><br/> | <span data-ttu-id="00664-113">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="00664-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="00664-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="00664-114">Minimum supported server</span></span><br/> | <span data-ttu-id="00664-115">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="00664-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="00664-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="00664-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="00664-117"><dt>Rpcdce. h (incluir RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="00664-117"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00664-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="00664-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00664-119">**\_INQ de objeto RPC \_ \_ FN**</span><span class="sxs-lookup"><span data-stu-id="00664-119">**RPC\_OBJECT\_INQ\_FN**</span></span>](/windows/desktop/api/Rpcdce/nc-rpcdce-rpc_object_inq_fn)
</dt> </dl>

 

 





