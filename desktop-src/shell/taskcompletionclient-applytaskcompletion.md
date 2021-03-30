---
description: Comienza la finalización de la tarea.
ms.assetid: 75C84DD9-D815-45C2-A28E-EAE437EAFF89
title: 'TaskCompletionClient:: ApplyTaskCompletion (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TaskCompletionClient.ApplyTaskCompletion
api_type:
- COM
api_location:
- ExecModelClient.dll
ms.openlocfilehash: 950d96ac46c18d741d5cf2337326f116fb79e36a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997849"
---
# <a name="taskcompletionclientapplytaskcompletion-method"></a><span data-ttu-id="5db28-103">TaskCompletionClient:: ApplyTaskCompletion (método)</span><span class="sxs-lookup"><span data-stu-id="5db28-103">TaskCompletionClient::ApplyTaskCompletion method</span></span>

<span data-ttu-id="5db28-104">Comienza la finalización de la tarea.</span><span class="sxs-lookup"><span data-stu-id="5db28-104">Begins the task completion.</span></span>

## <a name="syntax"></a><span data-ttu-id="5db28-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5db28-105">Syntax</span></span>


```C++
HRESULT ApplyTaskCompletion(
    UINT32   ptcfCategory
);
```



## <a name="parameters"></a><span data-ttu-id="5db28-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5db28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5db28-107">*ptcfCategory*</span><span class="sxs-lookup"><span data-stu-id="5db28-107">*ptcfCategory*</span></span> 
</dt> <dd>

<span data-ttu-id="5db28-108">Valor que indica la categoría de la tarea.</span><span class="sxs-lookup"><span data-stu-id="5db28-108">A value indicating the category of the task.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5db28-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5db28-109">Return value</span></span>

<span data-ttu-id="5db28-110">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5db28-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5db28-111">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5db28-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5db28-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5db28-112">Remarks</span></span>

<span data-ttu-id="5db28-113">El único valor admitido para *ptcfCategory* es 0x08000000.</span><span class="sxs-lookup"><span data-stu-id="5db28-113">The only supported value for *ptcfCategory* is 0x08000000.</span></span>

## <a name="requirements"></a><span data-ttu-id="5db28-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5db28-114">Requirements</span></span>



| <span data-ttu-id="5db28-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5db28-115">Requirement</span></span> | <span data-ttu-id="5db28-116">Value</span><span class="sxs-lookup"><span data-stu-id="5db28-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5db28-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5db28-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5db28-118">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="5db28-118">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5db28-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5db28-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5db28-120">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="5db28-120">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5db28-121">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5db28-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5db28-122"><dt>ExecModelClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5db28-122"><dt>ExecModelClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5db28-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="5db28-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5db28-124">**TaskCompletionClient**</span><span class="sxs-lookup"><span data-stu-id="5db28-124">**TaskCompletionClient**</span></span>](taskcompletionclient.md)
</dt> </dl>

 

 




