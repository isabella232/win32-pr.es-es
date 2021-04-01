---
description: Función de devolución de llamada que se usa para notificar al host la información de la pila de llamadas.
MS-HAID: vspixengine.ICallStackCallback\_ResultCallback\_DWORD\_CallStackFrame\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'ICallStackCallback:: ResultCallback (método)'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9C083298-6FD5-4414-8E0C-625F6A144668
api_name:
- ICallStackCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4bd77ea22fd31b31081d72707b1fd7a2efbda607
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103906657"
---
# <a name="span-idvspixengineicallstackcallback_resultcallback_dword_callstackframe_arrspanicallstackcallbackresultcallback-method"></a><span data-ttu-id="43a1d-103"><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>ICallStackCallback:: ResultCallback (método)</span><span class="sxs-lookup"><span data-stu-id="43a1d-103"><span id="vspixengine.icallstackcallback_resultcallback_dword_callstackframe_arr"></span>ICallStackCallback::ResultCallback method</span></span>

<span data-ttu-id="43a1d-104">Función de devolución de llamada que se usa para notificar al host la información de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="43a1d-104">A callback function used to notify the host of call stack information.</span></span>

## <a name="syntax"></a><span data-ttu-id="43a1d-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="43a1d-105">Syntax</span></span>


```C++
HRESULT ResultCallback(
   DWORD             count,
   CallStackFrame [] count0_callStackFrameBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="43a1d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="43a1d-106">Parameters</span></span>

<span data-ttu-id="43a1d-107">*contabiliza* </span><span class="sxs-lookup"><span data-stu-id="43a1d-107">*count* </span></span>  
<span data-ttu-id="43a1d-108">Número de framebuffers de pila de llamadas devueltos.</span><span class="sxs-lookup"><span data-stu-id="43a1d-108">The number of callstack framebuffers returned.</span></span>

<span data-ttu-id="43a1d-109">*count0 \_ callStackFrameBuffer* </span><span class="sxs-lookup"><span data-stu-id="43a1d-109">*count0\_callStackFrameBuffer* </span></span>  
<span data-ttu-id="43a1d-110">Información de la pila de llamadas.</span><span class="sxs-lookup"><span data-stu-id="43a1d-110">The callstack information.</span></span>

## <a name="return-value"></a><span data-ttu-id="43a1d-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="43a1d-111">Return value</span></span>

<span data-ttu-id="43a1d-112">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="43a1d-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="43a1d-113">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="43a1d-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a1d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43a1d-114">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="43a1d-115">Encabezado</span><span class="sxs-lookup"><span data-stu-id="43a1d-115">Header</span></span></p></td><td><span data-ttu-id="43a1d-116">Vspixengine. h</span><span class="sxs-lookup"><span data-stu-id="43a1d-116">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="43a1d-117"><span id="see_also"></span>Vea también</span><span class="sxs-lookup"><span data-stu-id="43a1d-117"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="43a1d-118">**ICallStackCallback**</span><span class="sxs-lookup"><span data-stu-id="43a1d-118">**ICallStackCallback**</span></span>](/windows/desktop/direct3dtools/icallstackcallback)

 

 
