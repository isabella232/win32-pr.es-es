---
title: WS_SECURITY_TOKEN (webservices. h)
description: Identificador opaco que representa un token de seguridad.
ms.assetid: 050a2ce5-279e-48fb-85da-1d0b11cd8229
keywords:
- WS_SECURITY_TOKEN
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d52e69a46f206f1def7cc2e7e2d03c2e5f1369f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491242"
---
# <a name="ws_security_token"></a><span data-ttu-id="f7824-104">\_token de seguridad de WS \_</span><span class="sxs-lookup"><span data-stu-id="f7824-104">WS\_SECURITY\_TOKEN</span></span>

<span data-ttu-id="f7824-105">Identificador opaco que representa un [token de seguridad](security-processing-results.md).</span><span class="sxs-lookup"><span data-stu-id="f7824-105">The opaque handle representing a [security token](security-processing-results.md).</span></span>


```C++
typedef struct _WS_SECURITY_TOKEN WS_SECURITY_TOKEN;
```



## <a name="remarks"></a><span data-ttu-id="f7824-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f7824-106">Remarks</span></span>

<span data-ttu-id="f7824-107">Este objeto no es seguro para subprocesos.</span><span class="sxs-lookup"><span data-stu-id="f7824-107">This object is not thread safe.</span></span> <span data-ttu-id="f7824-108">Para obtener más información, vea [seguridad para subprocesos](thread-safety.md).</span><span class="sxs-lookup"><span data-stu-id="f7824-108">For more information, see [thread safety](thread-safety.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f7824-109">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f7824-109">Requirements</span></span>



| <span data-ttu-id="f7824-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="f7824-110">Requirement</span></span> | <span data-ttu-id="f7824-111">Value</span><span class="sxs-lookup"><span data-stu-id="f7824-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7824-112">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7824-112">Minimum supported client</span></span><br/> | <span data-ttu-id="f7824-113">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="f7824-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="f7824-114">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f7824-114">Minimum supported server</span></span><br/> | <span data-ttu-id="f7824-115">\[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="f7824-115">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f7824-116">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f7824-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7824-117"><dt>Webservices. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7824-117"><dt>WebServices.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7824-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="f7824-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7824-119">Resultados de procesamiento de seguridad</span><span class="sxs-lookup"><span data-stu-id="f7824-119">Security Processing Results</span></span>](security-processing-results.md)
</dt> <dt>

[<span data-ttu-id="f7824-120">Seguridad para subprocesos</span><span class="sxs-lookup"><span data-stu-id="f7824-120">Thread Safety</span></span>](thread-safety.md)
</dt> </dl>

 

 





