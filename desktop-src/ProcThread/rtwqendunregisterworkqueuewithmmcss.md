---
description: Completa una solicitud asincrónica para anular el registro de una cola de trabajo con una tarea del servicio de programador de clases multimedia (MMCSS).
ms.assetid: 0E8F9BF6-AC1E-4FC0-BFAE-F292C4859F1F
title: RtwqEndUnregisterWorkQueueWithMMCSS función)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtwqEndUnregisterWorkQueueWithMMCSS
api_type:
- DllExport
api_location:
- RTWorkQ.dll
ms.openlocfilehash: b55386b2a018b0e311a1d4dbb2084b136d49c2f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910354"
---
# <a name="rtwqendunregisterworkqueuewithmmcss-function"></a><span data-ttu-id="6eddd-103">RtwqEndUnregisterWorkQueueWithMMCSS función)</span><span class="sxs-lookup"><span data-stu-id="6eddd-103">RtwqEndUnregisterWorkQueueWithMMCSS function</span></span>

<span data-ttu-id="6eddd-104">Completa una solicitud asincrónica para anular el registro de una cola de trabajo con una tarea del servicio de programador de clases multimedia (MMCSS).</span><span class="sxs-lookup"><span data-stu-id="6eddd-104">Completes an asynchronous request to unregister a work queue with a Multimedia Class Scheduler Service (MMCSS) task.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eddd-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6eddd-105">Syntax</span></span>


```C++
HRESULT WINAPI RtwqEndUnregisterWorkQueueWithMMCSS(
    IMFAsyncResult  *pResult 
);
```



## <a name="parameters"></a><span data-ttu-id="6eddd-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6eddd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eddd-107">*pResult*</span><span class="sxs-lookup"><span data-stu-id="6eddd-107">*pResult*</span></span> 
</dt> <dd>

<span data-ttu-id="6eddd-108">Puntero a la interfaz [**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="6eddd-108">Pointer to the [**IMFAsyncResult**](/windows/win32/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="6eddd-109">Pase el mismo puntero que el objeto de devolución de llamada recibido en el método [**IRtwqAsyncCallback:: Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="6eddd-109">Pass in the same pointer that your callback object received in the [**IRtwqAsyncCallback::Invoke**](/windows/win32/api/rtworkq/nf-rtworkq-irtwqasynccallback-invoke) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eddd-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6eddd-110">Return value</span></span>

<span data-ttu-id="6eddd-111">Si esta función se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="6eddd-111">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6eddd-112">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6eddd-112">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="6eddd-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6eddd-113">Requirements</span></span>



| <span data-ttu-id="6eddd-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6eddd-114">Requirement</span></span> | <span data-ttu-id="6eddd-115">Value</span><span class="sxs-lookup"><span data-stu-id="6eddd-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6eddd-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6eddd-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6eddd-117">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="6eddd-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6eddd-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6eddd-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6eddd-119">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="6eddd-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6eddd-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6eddd-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6eddd-121"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="6eddd-121"><dt>None</dt></span></span> </dl>        |
| <span data-ttu-id="6eddd-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6eddd-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="6eddd-123"><dt>Rtworkq. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6eddd-123"><dt>Rtworkq.lib</dt></span></span> </dl> |
| <span data-ttu-id="6eddd-124">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6eddd-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6eddd-125"><dt>RTWorkQ.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6eddd-125"><dt>RTWorkQ.dll</dt></span></span> </dl> |



 

 
