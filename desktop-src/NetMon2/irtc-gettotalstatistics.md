---
description: El método GetTotalStatistics recupera las estadísticas totales de la captura actual.
ms.assetid: e5098984-c69e-4cd5-9143-d85dfcbd7b92
title: 'IRTC:: GetTotalStatistics (método) (Netmon. h)'
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
ms.openlocfilehash: 27128048b4326aae14ae6a2e2e6c0540b1105538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677651"
---
# <a name="irtcgettotalstatistics-method"></a><span data-ttu-id="1c1a6-103">IRTC:: GetTotalStatistics (método)</span><span class="sxs-lookup"><span data-stu-id="1c1a6-103">IRTC::GetTotalStatistics method</span></span>

<span data-ttu-id="1c1a6-104">El método **GetTotalStatistics** recupera las [*Estadísticas totales*](t.md) de la [*captura*](c.md)actual.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1c1a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c1a6-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="1c1a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1c1a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1c1a6-107">*lpStats* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="1c1a6-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1a6-108">Puntero a una estructura de [estadísticas](statistics.md) que proporciona las estadísticas totales de la captura.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-108">Pointer to a [STATISTICS](statistics.md) structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="1c1a6-109">Es responsabilidad del llamador asignar y liberar la memoria que usa la estructura de **estadísticas** .</span><span class="sxs-lookup"><span data-stu-id="1c1a6-109">It is the callers responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="1c1a6-110">*fClearAfterReading* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1c1a6-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1c1a6-111">Marca usada para indicar a Monitor de red cómo controlar el almacenamiento interno de las estadísticas totales.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="1c1a6-112">Un valor **true** indica a monitor de red que borre el almacenamiento interno de las estadísticas totales una vez recuperada la información actual.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-112">A setting of **TRUE** tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1c1a6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1c1a6-113">Return value</span></span>

<span data-ttu-id="1c1a6-114">Si el método se realiza correctamente, el valor devuelto es NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="1c1a6-115">Si el método no se realiza correctamente, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="1c1a6-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="1c1a6-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="1c1a6-116">Return code</span></span>                                                                                          | <span data-ttu-id="1c1a6-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="1c1a6-117">Description</span></span>                                                                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1c1a6-118"><dt>**NMERR \_ no \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="1c1a6-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="1c1a6-119">NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="1c1a6-120">Llame a [IRTC:: Connect](irtc-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-120">Call [IRTC::Connect](irtc-connect.md) to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="1c1a6-121"><dt>**NMERR \_ no es en \_ tiempo real**</dt></span><span class="sxs-lookup"><span data-stu-id="1c1a6-121"><dt>**NMERR\_NOT\_REALTIME**</dt></span></span> </dl>  | <span data-ttu-id="1c1a6-122">NPP está conectado a la red, pero no con el método [IRTC:: Connect](irtc-connect.md) .</span><span class="sxs-lookup"><span data-stu-id="1c1a6-122">The NPP is connected to the network but not with the [IRTC::Connect](irtc-connect.md) method.</span></span><br/>                     |
| <dl> <span data-ttu-id="1c1a6-123"><dt>**NMERR \_ no se \_ captura**</dt></span><span class="sxs-lookup"><span data-stu-id="1c1a6-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="1c1a6-124">NPP no está capturando datos.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-124">The NPP is not capturing data.</span></span> <span data-ttu-id="1c1a6-125">Llame a [IRTC:: Start](irtc-start.md) para empezar a capturar datos.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-125">Call [IRTC::Start](irtc-start.md) to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="1c1a6-126">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1c1a6-126">Remarks</span></span>

<span data-ttu-id="1c1a6-127">Este método devuelve los datos solo mientras una captura está en curso, incluso mientras la captura está en pausa.</span><span class="sxs-lookup"><span data-stu-id="1c1a6-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="1c1a6-128">Monitor de red también almacena [*estadísticas de conversación*](c.md).</span><span class="sxs-lookup"><span data-stu-id="1c1a6-128">Network Monitor also stores [*conversation statistics*](c.md).</span></span> <span data-ttu-id="1c1a6-129">Para recuperar las estadísticas de conversación, llame al método [IRTC:: GetConversationStatistics](irtc-getconversationstatistics.md) .</span><span class="sxs-lookup"><span data-stu-id="1c1a6-129">To retrieve conversation statistics, call the [IRTC::GetConversationStatistics](irtc-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c1a6-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c1a6-130">Requirements</span></span>



| <span data-ttu-id="1c1a6-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c1a6-131">Requirement</span></span> | <span data-ttu-id="1c1a6-132">Value</span><span class="sxs-lookup"><span data-stu-id="1c1a6-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c1a6-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c1a6-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1c1a6-134">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1c1a6-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="1c1a6-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c1a6-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1c1a6-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1c1a6-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="1c1a6-137">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c1a6-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c1a6-138"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c1a6-138"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="1c1a6-139">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1c1a6-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c1a6-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c1a6-140"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c1a6-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="1c1a6-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c1a6-142">IRTC</span><span class="sxs-lookup"><span data-stu-id="1c1a6-142">IRTC</span></span>](irtc.md)
</dt> <dt>

[<span data-ttu-id="1c1a6-143">IRTC:: Connect</span><span class="sxs-lookup"><span data-stu-id="1c1a6-143">IRTC::Connect</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="1c1a6-144">IRTC::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="1c1a6-144">IRTC::GetConversationStatistics</span></span>](irtc-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="1c1a6-145">IRTC:: Start</span><span class="sxs-lookup"><span data-stu-id="1c1a6-145">IRTC::Start</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="1c1a6-146">¡</span><span class="sxs-lookup"><span data-stu-id="1c1a6-146">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




