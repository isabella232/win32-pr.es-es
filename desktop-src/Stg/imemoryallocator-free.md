---
title: IMemoryAllocator Free (método)
description: El método Free libera la memoria asignada por el método allocate.
ms.assetid: 41f81cba-4431-4ff7-ac84-8ff5bea71b65
keywords:
- Almacenamiento estructurado de método gratuito
- Método gratuito de almacenamiento estructurado, interfaz IMemoryAllocator
- IMemoryAllocator interface Structured Storage, Free (método)
topic_type:
- apiref
api_name:
- IMemoryAllocator.Free
api_location:
- Ole32.lib
- Ole32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c07731f60aba7d847c79467b2b2c166b363d807
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078970"
---
# <a name="imemoryallocatorfree-method"></a><span data-ttu-id="b362a-106">IMemoryAllocator:: Free (método)</span><span class="sxs-lookup"><span data-stu-id="b362a-106">IMemoryAllocator::Free method</span></span>

<span data-ttu-id="b362a-107">El método **Free** libera la memoria asignada por el método [**allocate**](imemoryallocator-allocate.md) .</span><span class="sxs-lookup"><span data-stu-id="b362a-107">The **Free** method frees the memory allocated by the [**Allocate**](imemoryallocator-allocate.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b362a-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b362a-108">Syntax</span></span>


```C++
virtual void Free(
   void* pv
);
```



## <a name="parameters"></a><span data-ttu-id="b362a-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b362a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b362a-110">*FV*</span><span class="sxs-lookup"><span data-stu-id="b362a-110">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="b362a-111">Puntero a la memoria que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="b362a-111">Pointer to the memory to be freed.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b362a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b362a-112">Requirements</span></span>



| <span data-ttu-id="b362a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="b362a-113">Requirement</span></span> | <span data-ttu-id="b362a-114">Value</span><span class="sxs-lookup"><span data-stu-id="b362a-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b362a-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b362a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b362a-116">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b362a-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b362a-117">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b362a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b362a-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b362a-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b362a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b362a-119">Library</span></span><br/>                  | <dl> <span data-ttu-id="b362a-120"><dt>Ole32. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b362a-120"><dt>Ole32.lib</dt></span></span> </dl> |



 

 





