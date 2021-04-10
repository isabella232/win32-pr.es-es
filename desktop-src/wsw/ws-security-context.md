---
title: WS_SECURITY_CONTEXT (webservices. h)
description: Tipo opaco que se usa para hacer referencia a un objeto de contexto de seguridad.
ms.assetid: 8d23357b-bff8-45fe-80ef-df3f3b0edde1
keywords:
- WS_SECURITY_CONTEXT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c041307eadd1ebcea379f9de0880fc011bd137ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150472"
---
# <a name="ws_security_context"></a><span data-ttu-id="6c372-104">\_contexto de seguridad de WS \_</span><span class="sxs-lookup"><span data-stu-id="6c372-104">WS\_SECURITY\_CONTEXT</span></span>

<span data-ttu-id="6c372-105">Tipo opaco que se usa para hacer referencia a un [objeto de contexto de seguridad](security-context.md).</span><span class="sxs-lookup"><span data-stu-id="6c372-105">An opaque type used to reference a [security context object](security-context.md).</span></span>


```C++
typedef struct _WS_SECURITY_CONTEXT WS_SECURITY_CONTEXT;
```



## <a name="remarks"></a><span data-ttu-id="6c372-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6c372-106">Remarks</span></span>

<span data-ttu-id="6c372-107">Este objeto no es seguro para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="6c372-107">This object is not thread safe.</span></span> <span data-ttu-id="6c372-108">Para obtener más información, vea [seguridad para subprocesos](thread-safety.md).</span><span class="sxs-lookup"><span data-stu-id="6c372-108">For more information, see [thread safety](thread-safety.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c372-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6c372-109">Requirements</span></span>



| <span data-ttu-id="6c372-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c372-110">Requirement</span></span> | <span data-ttu-id="6c372-111">Value</span><span class="sxs-lookup"><span data-stu-id="6c372-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c372-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c372-112">Minimum supported client</span></span><br/> | <span data-ttu-id="6c372-113">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="6c372-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="6c372-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6c372-114">Minimum supported server</span></span><br/> | <span data-ttu-id="6c372-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="6c372-115">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="6c372-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6c372-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c372-117"><dt>Webservices. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c372-117"><dt>WebServices.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c372-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="6c372-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c372-119">Contexto de seguridad</span><span class="sxs-lookup"><span data-stu-id="6c372-119">Security Context</span></span>](security-context.md)
</dt> <dt>

[<span data-ttu-id="6c372-120">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="6c372-120">Thread Safety</span></span>](thread-safety.md)
</dt> </dl>

 

 





