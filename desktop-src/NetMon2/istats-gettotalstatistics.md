---
description: 'Método IStats::GetTotalStatistics: el método GetTotalStatistics recupera las estadísticas totales de la captura actual.'
ms.assetid: 494634f6-a9b3-4a50-8920-2387be9ba30f
title: Método IStats::GetTotalStatistics (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.GetTotalStatistics
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: e6566a58212e8f20d0d999302f41ab97cb9f005e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098413"
---
# <a name="istatsgettotalstatistics-method"></a><span data-ttu-id="03cb5-103">Método IStats::GetTotalStatistics</span><span class="sxs-lookup"><span data-stu-id="03cb5-103">IStats::GetTotalStatistics method</span></span>

<span data-ttu-id="03cb5-104">El **método GetTotalStatistics** recupera las [*estadísticas totales*](t.md) de la captura [*actual.*](c.md)</span><span class="sxs-lookup"><span data-stu-id="03cb5-104">The **GetTotalStatistics** method retrieves the [*total statistics*](t.md) for the current [*capture*](c.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="03cb5-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="03cb5-105">Syntax</span></span>


```C++
HRESULT STDMETHODCALLTYPE GetTotalStatistics(
  [out] LPSTATISTICS lpStats,
  [in]  BOOL         fClearAfterReading
);
```



## <a name="parameters"></a><span data-ttu-id="03cb5-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="03cb5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03cb5-107">*lpStats* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="03cb5-107">*lpStats* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03cb5-108">Puntero a una [estructura STATISTICS](statistics.md)que proporciona las estadísticas totales de la captura.</span><span class="sxs-lookup"><span data-stu-id="03cb5-108">Pointer to a [STATISTICS](statistics.md)structure that provides the total statistics for the capture.</span></span> <span data-ttu-id="03cb5-109">Es responsabilidad del autor de la llamada asignar y liberar la memoria usada por la **estructura STATISTICS.**</span><span class="sxs-lookup"><span data-stu-id="03cb5-109">It is the caller's responsibility to allocate and free the memory used by the **STATISTICS** structure.</span></span>

</dd> <dt>

<span data-ttu-id="03cb5-110">*fClearAfterReading* \[ En\]</span><span class="sxs-lookup"><span data-stu-id="03cb5-110">*fClearAfterReading* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03cb5-111">Marca que se usa para Monitor de red cómo controlar el almacenamiento interno de las estadísticas totales.</span><span class="sxs-lookup"><span data-stu-id="03cb5-111">Flag used to tell Network Monitor how to handle the internal storage of the total statistics.</span></span> <span data-ttu-id="03cb5-112">Una configuración de TRUE indica Monitor de red borrar el almacenamiento interno de las estadísticas totales después de recuperar la información actual.</span><span class="sxs-lookup"><span data-stu-id="03cb5-112">A setting of TRUE tells Network Monitor to clear out the internal storage of the total statistics after the current information is retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03cb5-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="03cb5-113">Return value</span></span>

<span data-ttu-id="03cb5-114">Si el método es correcto, el valor devuelto es NMERR \_ SUCCESS.</span><span class="sxs-lookup"><span data-stu-id="03cb5-114">If the method is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="03cb5-115">Si el método no es correcto, el valor devuelto es uno de los siguientes códigos de error:</span><span class="sxs-lookup"><span data-stu-id="03cb5-115">If the method is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="03cb5-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="03cb5-116">Return code</span></span>                                                                                            | <span data-ttu-id="03cb5-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="03cb5-117">Description</span></span>                                                                                                                                  |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="03cb5-118"><dt>**NMERR \_ NO \_ CONECTADO**</dt></span><span class="sxs-lookup"><span data-stu-id="03cb5-118"><dt>**NMERR\_NOT\_CONNECTED**</dt></span></span> </dl>   | <span data-ttu-id="03cb5-119">El NPP no está conectado a la red.</span><span class="sxs-lookup"><span data-stu-id="03cb5-119">The NPP is not connected to the network.</span></span> <span data-ttu-id="03cb5-120">Llame al [método IStats::Connect](istats-connect.md) para conectar el NPP a la red.</span><span class="sxs-lookup"><span data-stu-id="03cb5-120">Call the [IStats::Connect](istats-connect.md) method to connect the NPP to the network.</span></span><br/> |
| <dl> <span data-ttu-id="03cb5-121"><dt>**NMERR \_ NO SOLO \_ \_ ESTADÍSTICAS**</dt></span><span class="sxs-lookup"><span data-stu-id="03cb5-121"><dt>**NMERR\_NOT\_STATS\_ONLY**</dt></span></span> </dl> | <span data-ttu-id="03cb5-122">El NPP está conectado a la red, pero no con el [método IStats::Connect.](istats-connect.md)</span><span class="sxs-lookup"><span data-stu-id="03cb5-122">The NPP is connected to the network but not with the [IStats::Connect](istats-connect.md) method.</span></span><br/>                                |
| <dl> <span data-ttu-id="03cb5-123"><dt>**NMERR \_ NO \_ CAPTURA**</dt></span><span class="sxs-lookup"><span data-stu-id="03cb5-123"><dt>**NMERR\_NOT\_CAPTURING**</dt></span></span> </dl>   | <span data-ttu-id="03cb5-124">El NPP no captura datos.</span><span class="sxs-lookup"><span data-stu-id="03cb5-124">The NPP is not capturing data.</span></span> <span data-ttu-id="03cb5-125">Llame al [método IStats::Start](istats-start.md) para empezar a capturar datos.</span><span class="sxs-lookup"><span data-stu-id="03cb5-125">Call the [IStats::Start](istats-start.md) method to start capturing data.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="03cb5-126">Comentarios</span><span class="sxs-lookup"><span data-stu-id="03cb5-126">Remarks</span></span>

<span data-ttu-id="03cb5-127">Este método devuelve datos solo mientras hay una captura en curso, incluso mientras la captura está en pausa.</span><span class="sxs-lookup"><span data-stu-id="03cb5-127">This method returns data only while a capture is in progress, including while the capture is paused.</span></span>

<span data-ttu-id="03cb5-128">Monitor de red también almacena [*estadísticas*](c.md)de conversación, que se pueden recuperar llamando al [método IStats::GetConversationStatistics.](istats-getconversationstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="03cb5-128">Network Monitor also stores [*conversation statistics*](c.md), which can be retrieved by calling the [IStats::GetConversationStatistics](istats-getconversationstatistics.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="03cb5-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="03cb5-129">Requirements</span></span>



| <span data-ttu-id="03cb5-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="03cb5-130">Requirement</span></span> | <span data-ttu-id="03cb5-131">Valor</span><span class="sxs-lookup"><span data-stu-id="03cb5-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03cb5-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03cb5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="03cb5-133">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="03cb5-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                               |
| <span data-ttu-id="03cb5-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="03cb5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="03cb5-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="03cb5-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                     |
| <span data-ttu-id="03cb5-136">Encabezado</span><span class="sxs-lookup"><span data-stu-id="03cb5-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="03cb5-137"><dt>Netmon.h</dt></span><span class="sxs-lookup"><span data-stu-id="03cb5-137"><dt>Netmon.h</dt></span></span> </dl>                                                                      |
| <span data-ttu-id="03cb5-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="03cb5-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03cb5-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03cb5-139"><dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03cb5-140">Consulte también</span><span class="sxs-lookup"><span data-stu-id="03cb5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03cb5-141">IStats</span><span class="sxs-lookup"><span data-stu-id="03cb5-141">IStats</span></span>](istats.md)
</dt> <dt>

[<span data-ttu-id="03cb5-142">IStats::Connect</span><span class="sxs-lookup"><span data-stu-id="03cb5-142">IStats::Connect</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="03cb5-143">IStats::GetConversationStatistics</span><span class="sxs-lookup"><span data-stu-id="03cb5-143">IStats::GetConversationStatistics</span></span>](istats-getconversationstatistics.md)
</dt> <dt>

[<span data-ttu-id="03cb5-144">IStats::Start,</span><span class="sxs-lookup"><span data-stu-id="03cb5-144">IStats::Start,</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="03cb5-145">Estadísticas</span><span class="sxs-lookup"><span data-stu-id="03cb5-145">STATISTICS</span></span>](statistics.md)
</dt> </dl>

 

 




