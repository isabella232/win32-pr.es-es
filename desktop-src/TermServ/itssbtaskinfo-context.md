---
title: Propiedad de contexto ITsSbTaskInfo
description: Recupera los bytes de contexto asociados a la tarea.
ms.assetid: ce55ce2a-957f-4b50-b632-42079277102b
ms.tgt_platform: multiple
keywords:
- Propiedad de contexto Servicios de Escritorio remoto
- Propiedad de contexto Servicios de Escritorio remoto, interfaz ITsSbTaskInfo
- Servicios de Escritorio remoto de la interfaz ITsSbTaskInfo, propiedad de contexto
topic_type:
- apiref
api_name:
- ITsSbTaskInfo.Context
- ITsSbTaskInfo.get_Context
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2adc4715f23b2c23ac6dfbdcdd8a489b2b0f5fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151087"
---
# <a name="itssbtaskinfocontext-property"></a><span data-ttu-id="66f54-106">ITsSbTaskInfo:: context (propiedad)</span><span class="sxs-lookup"><span data-stu-id="66f54-106">ITsSbTaskInfo::Context property</span></span>

<span data-ttu-id="66f54-107">Recupera los bytes de contexto asociados a la tarea.</span><span class="sxs-lookup"><span data-stu-id="66f54-107">Retrieves the context bytes associated with the task.</span></span>

<span data-ttu-id="66f54-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="66f54-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="66f54-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66f54-109">Syntax</span></span>


```C++
HRESULT get_Context(
  [out, retval] SAFEARRAY(BYTE) *pContext
);
```



## <a name="property-value"></a><span data-ttu-id="66f54-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="66f54-110">Property value</span></span>

<span data-ttu-id="66f54-111">Contexto de la tarea.</span><span class="sxs-lookup"><span data-stu-id="66f54-111">The context of the task.</span></span>

## <a name="requirements"></a><span data-ttu-id="66f54-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66f54-112">Requirements</span></span>



| <span data-ttu-id="66f54-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="66f54-113">Requirement</span></span> | <span data-ttu-id="66f54-114">Value</span><span class="sxs-lookup"><span data-stu-id="66f54-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="66f54-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66f54-115">Minimum supported client</span></span><br/> | <span data-ttu-id="66f54-116">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="66f54-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="66f54-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66f54-117">Minimum supported server</span></span><br/> | <span data-ttu-id="66f54-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="66f54-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="66f54-119">IDL</span><span class="sxs-lookup"><span data-stu-id="66f54-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="66f54-120"><dt>Sbtsv. idl</dt></span><span class="sxs-lookup"><span data-stu-id="66f54-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66f54-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="66f54-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66f54-122">**ITsSbTaskInfo**</span><span class="sxs-lookup"><span data-stu-id="66f54-122">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> </dl>

 

 





