---
description: 'Método IRTC::GetTotalStatistics: el método GetTotalStatistics recupera las estadísticas totales de la captura actual.'
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: Método IRTC::GetTotalStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRTC.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 8ed659efe388f4eb9c9ac8afd6aa2c74fd0af7d3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108110693"
---
# <a name="irtcgettotalstatistics-method"></a><span data-ttu-id="94fd1-103">Método IRTC::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="94fd1-103">IRTC::GetTotalStatistics method</span></span>

<span data-ttu-id="94fd1-104">El **método GetTotalStatistics** recupera las [*estadísticas totales*](t.md) de la captura [*actual.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="94fd1-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="94fd1-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="94fd1-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="94fd1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="94fd1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94fd1-107">*lpStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="94fd1-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="94fd1-108">Puntero a una [estructura STATISTICS](statistics.md) que proporciona las estadísticas totales de la captura.</span><span class="sxs-lookup"><span data-stu-id="94fd1-108">Pointer to a [STATISTICS](statistics.md) structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="94fd1-109">Es responsabilidad de los autores de llamadas asignar y liberar la memoria usada por la **estructura STATISTICS.**</span><span class="sxs-lookup"><span data-stu-id="94fd1-109">It is the callers responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="94fd1-110">*fClearAfterReading* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="94fd1-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94fd1-111">Marca que se usa para Monitor de red cómo controlar el almacenamiento interno de las estadísticas totales.</span><span class="sxs-lookup"><span data-stu-id="94fd1-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="94fd1-112">Una configuración **de TRUE** indica Monitor de red borrar el almacenamiento interno de las estadísticas totales después de recuperar la información actual.</span><span class="sxs-lookup"><span data-stu-id="94fd1-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94fd1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="94fd1-113">Return value</span></span>

<span data-ttu-id="94fd1-114">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="94fd1-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="94fd1-115">Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="94fd1-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="94fd1-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="94fd1-116">Return code</span></span>                                                                                          | <span data-ttu-id="94fd1-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="94fd1-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="94fd1-118"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="94fd1-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="94fd1-119">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="94fd1-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="94fd1-120">Llame [a IRTC::Connect](irtc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="94fd1-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="94fd1-121"><dt>**NMERR \_ NOT \_ REALTIME**</dt></span><span class="sxs-lookup"><span data-stu-id="94fd1-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="94fd1-122">El NPP está conectado a la red, pero no con el [método IRTC::Connect.](irtc-connect.md)</span><span class="sxs-lookup"><span data-stu-id="94fd1-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |
| <dl> <span data-ttu-id="94fd1-123"><dt>**NMERR \_ NO \_ CAPTURA**</dt></span><span class="sxs-lookup"><span data-stu-id="94fd1-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="94fd1-124">El NPP no captura datos.</span><span class="sxs-lookup"><span data-stu-id="94fd1-124">The NPP is not capturing data.</span></span> <span data-ttu-id="94fd1-125">Llame [a IRTC::Start para](irtc-start.md) empezar a capturar datos.</span><span class="sxs-lookup"><span data-stu-id="94fd1-125">Call [IRTC::Start](irtc-start.md) to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="94fd1-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="94fd1-126">Remarks</span></span>

<span data-ttu-id="94fd1-127">Este método devuelve datos solo mientras hay una captura en curso, incluso mientras la captura está en pausa.</span><span class="sxs-lookup"><span data-stu-id="94fd1-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="94fd1-128">Monitor de red también almacena [*las estadísticas de conversación.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="94fd1-128">Network Monitor also stores [*conversation statistics*](c.md).</span></span> <span data-ttu-id="94fd1-129">Para recuperar las estadísticas de conversación, llame [al método IRTC::GetConversationStatistics.](irtc-getconversationstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="94fd1-129">To retrieve conversation statistics, call the [IRTC::GetConversationStatistics](irtc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="94fd1-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94fd1-130">Requirements</span></span>



| <span data-ttu-id="94fd1-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="94fd1-131">Requirement</span></span> | <span data-ttu-id="94fd1-132">Valor</span><span class="sxs-lookup"><span data-stu-id="94fd1-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94fd1-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94fd1-133">Minimum supported client</span></span><br/> | <span data-ttu-id="94fd1-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="94fd1-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="94fd1-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="94fd1-135">Minimum supported server</span></span><br/> | <span data-ttu-id="94fd1-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="94fd1-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="94fd1-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="94fd1-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="94fd1-138"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="94fd1-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="94fd1-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="94fd1-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94fd1-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94fd1-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94fd1-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="94fd1-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94fd1-142">IRTC</span><span class="sxs-lookup"><span data-stu-id="94fd1-142">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="94fd1-143">IRTC::Connect</span><span class="sxs-lookup"><span data-stu-id="94fd1-143">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="94fd1-144">IRTC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="94fd1-144">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="94fd1-145">IRTC::Start</span><span class="sxs-lookup"><span data-stu-id="94fd1-145">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="94fd1-146">Estadísticas</span><span class="sxs-lookup"><span data-stu-id="94fd1-146">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




