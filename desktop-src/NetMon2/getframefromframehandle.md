---
description: La función GetFrameFromFrameHandle devuelve un puntero a un marco de un identificador de marco.
ms.assetid: 790fe5fe-a857-4947-a471-d0538c0f0d61
title: Función GetFrameFromFrameHandle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameFromFrameHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ce8151b2f4c81c61dea5969ff52e9ddf2d6615a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666282"
---
# <a name="getframefromframehandle-function"></a><span data-ttu-id="55672-103">GetFrameFromFrameHandle función)</span><span class="sxs-lookup"><span data-stu-id="55672-103">GetFrameFromFrameHandle function</span></span>

<span data-ttu-id="55672-104">La función **GetFrameFromFrameHandle** devuelve un puntero a un marco de un identificador de marco.</span><span class="sxs-lookup"><span data-stu-id="55672-104">The **GetFrameFromFrameHandle** function returns a pointer to a frame from a frame handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="55672-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="55672-105">Syntax</span></span>


```C++
ULPFRAME WINAPI GetFrameFromFrameHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="55672-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="55672-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55672-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="55672-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55672-108">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="55672-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55672-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="55672-109">Return value</span></span>

<span data-ttu-id="55672-110">Si la función se realiza correctamente, el valor devuelto es un puntero al marco.</span><span class="sxs-lookup"><span data-stu-id="55672-110">If the function is successful, the return value is a pointer to the frame.</span></span>

<span data-ttu-id="55672-111">Si la función no se realiza correctamente, el valor devuelto es 0.</span><span class="sxs-lookup"><span data-stu-id="55672-111">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="55672-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="55672-112">Remarks</span></span>

<span data-ttu-id="55672-113">La función **GetFrameFromFrameHandle** recupera datos que las demás funciones auxiliares que monitor de red proporciona no pueden recuperar.</span><span class="sxs-lookup"><span data-stu-id="55672-113">The **GetFrameFromFrameHandle** function retrieves data that cannot be retrieved by the other helper functions that Network Monitor provides.</span></span> <span data-ttu-id="55672-114">Utilice las siguientes funciones siempre que sea posible.</span><span class="sxs-lookup"><span data-stu-id="55672-114">Use the following functions whenever possible.</span></span>

<dl>

[<span data-ttu-id="55672-115">**GetFrameDstAddressOffset**</span><span class="sxs-lookup"><span data-stu-id="55672-115">**GetFrameDstAddressOffset**</span></span>](getframedstaddressoffset.md)  
[<span data-ttu-id="55672-116">**GetFrameSrcAddressOffset**</span><span class="sxs-lookup"><span data-stu-id="55672-116">**GetFrameSrcAddressOffset**</span></span>](getframesrcaddressoffset.md)  
[<span data-ttu-id="55672-117">**GetFrameCaptureHandle**</span><span class="sxs-lookup"><span data-stu-id="55672-117">**GetFrameCaptureHandle**</span></span>](getframecapturehandle.md)  
[<span data-ttu-id="55672-118">**GetFrameDestAddress**</span><span class="sxs-lookup"><span data-stu-id="55672-118">**GetFrameDestAddress**</span></span>](getframedestaddress.md)  
[<span data-ttu-id="55672-119">**GetFrameSourceAddress**</span><span class="sxs-lookup"><span data-stu-id="55672-119">**GetFrameSourceAddress**</span></span>](getframesourceaddress.md)  
[<span data-ttu-id="55672-120">**GetFrameMacHeaderLength**</span><span class="sxs-lookup"><span data-stu-id="55672-120">**GetFrameMacHeaderLength**</span></span>](getframemacheaderlength.md)  
[<span data-ttu-id="55672-121">**GetFrameLength**</span><span class="sxs-lookup"><span data-stu-id="55672-121">**GetFrameLength**</span></span>](getframelength.md)  
[<span data-ttu-id="55672-122">**GetFrameStoredLength**</span><span class="sxs-lookup"><span data-stu-id="55672-122">**GetFrameStoredLength**</span></span>](getframestoredlength.md)  
[<span data-ttu-id="55672-123">**GetFrameMacType**</span><span class="sxs-lookup"><span data-stu-id="55672-123">**GetFrameMacType**</span></span>](getframemactype.md)  
[<span data-ttu-id="55672-124">**GetFrameNumber**</span><span class="sxs-lookup"><span data-stu-id="55672-124">**GetFrameNumber**</span></span>](getframenumber.md)  
[<span data-ttu-id="55672-125">**GetFrameTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="55672-125">**GetFrameTimeStamp**</span></span>](getframetimestamp.md)  
</dl>

<span data-ttu-id="55672-126">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameFromFrameHandle** .</span><span class="sxs-lookup"><span data-stu-id="55672-126">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameFromFrameHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="55672-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55672-127">Requirements</span></span>



| <span data-ttu-id="55672-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="55672-128">Requirement</span></span> | <span data-ttu-id="55672-129">Value</span><span class="sxs-lookup"><span data-stu-id="55672-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="55672-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55672-130">Minimum supported client</span></span><br/> | <span data-ttu-id="55672-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="55672-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="55672-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="55672-132">Minimum supported server</span></span><br/> | <span data-ttu-id="55672-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="55672-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="55672-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="55672-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="55672-135"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="55672-135"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="55672-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55672-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="55672-137"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55672-137"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="55672-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="55672-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55672-139"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55672-139"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




